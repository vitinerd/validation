build:  ## To build the Go-Hugo website in /dist directory
	@hugo > /dev/null
clean:  ## To remove the Go-Hugo website from the /dist directory preserving all content
	@rm -rf dist/*
post:   ## To create a new post for existing website
ifdef $(and POST_NAME, POST_TITLE)
	@hugo new posts/"${POST_NAME}.md" > /dev/null
	@sed -i "s/${POST_NAME}/${POST_TITLE}/gi" "./content/posts/${POST_NAME}.md"
endif
help:	## Displays the help information
	@fgrep -h "##" $(MAKEFILE_LIST) | fgrep -v frep | sed -e 's/\\$$//' | sed -e 's/##//'

