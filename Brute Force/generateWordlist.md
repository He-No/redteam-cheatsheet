CAREFUL! Crunch can create very big files in the GB's very quickly. Use the -o flag with care!

Use crunch to generate wordlists:

	syntax : crunch <minLength> <maxLength> <characterSet>
	example: crunch 1 6 abcdABCDE

	syntax : crunch <minLength> <maxLength> -t <pattern>
	example: crunch 1 3 -t @@,%

		@ will insert lower case characters
		, will insert upper case characters
		% will insert numbers
		^ will insert symbols


Use crunch to generate a wordlist from existing character sets(check the file for possible character sets):

	syntax : crunch <minLength> <maxLength> -f <charSetFile> <charSet> -o <outFile>
	example: crunch 1 4 -f /usr/share/crunch/charset.lst lalpha -o dictionary.txt

# curated by ProfessorBobeye