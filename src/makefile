all:

	#gcc -o Ash main.c cle.c builtins.c exec.c y.tab.c lex.yy.c err.c -lreadline
	gcc  -g -o Ash main.c cle.c  job.c y.tab.c lex.yy.c err.c -lreadline  -w

install:
	# copy configuration files in the user's home directory
	cp -r ../.Ash ~/
	
	# compress the man page
	gzip -k  ../doc/Ash.1
	
	# copy the man page to one of the directories search by man
	cp ../doc/Ash.1.gz "/usr/local/man/man1/Ash.1.gz"
	
	# copy the built binary to one of the directories in PATH
	cp Ash /usr/local/bin
	

clean:
	# clean up
	rm Ash
	rm ../doc/Ash.1.gz

