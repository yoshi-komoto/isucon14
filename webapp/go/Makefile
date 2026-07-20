.PHONY: build deploy restart all

build:
	go build -o isuride .
deploy:
	sudo mv isuride ~/../isucon/webapp/go
restart:
	sudo systemctl daemon-reload
	sudo systemctl restart isuride-go.service
	sudo systemctl restart nginx
all: build deploy restart