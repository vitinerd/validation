build:
	@hugo > /dev/null
clean:
	@rm -rf dist/*
post:
ifdef $(and POST_NAME, POST_TITLE)
	@hugo new posts/"${POST_NAME}.md" > /dev/null
	@sed -i "s/${POST_NAME}/${POST_TITLE}/gi" "./content/posts/${POST_NAME}.md"
endif
