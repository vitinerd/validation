build: ## To build the website in configured /dist directory
	@hugo > /dev/null
clean: ## The clean the existing build from the /dist directory
	@rm -rf dist/*
post: ## To post option will create a new post. Refer to help for more use case.
ifdef $(and POST_NAME, POST_TITLE)
	@hugo new posts/"${POST_NAME}.md" > /dev/null
	@sed -i "s/${POST_NAME}/${POST_TITLE}/gi" "./content/posts/${POST_NAME}.md"
endif
help:
	@echo "build: To build the website in configured /dist directory"
	@echo "post: To create a new post using POST_NAME as filename and  POST_TITLE as the title of the post"
	@echo "clean: To clean the existing build from the /dist directory"
	@echo "help: Prints help"
