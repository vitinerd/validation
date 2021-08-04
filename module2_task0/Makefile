build:  ## To build the Awesome-api webserver
	@go mod init github.com/vitinerd/awesome-api
	@go build
run: 	## To run the webserver in the background
	@./awesome-api >./awesome.log 2>&1 &
stop: 	## To stop the server if running
	@kill "$(pgrep awesome-api)"
clean:  ## To remove the awesome binary and its log file
	@rm awesome-api
	@rm awesome.log
	@rm go.mod
test:   ## To test behavior of website awesome
	@curl http://localhost:9999
	@curl http://localhost:9999/health	
help:	## Displays the help information
	@fgrep -h "##" $(MAKEFILE_LIST) | fgrep -v frep | sed -e 's/\\$$//' | sed -e 's/##//'

