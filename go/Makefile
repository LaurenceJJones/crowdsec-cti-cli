BINARY_NAME=cscti

LDFLAGS=-ldflags "-s -w"

all: clean

build:
	CGO_ENABLED=0 go build -o $(BINARY_NAME) $(LDFLAGS) -v

clean:
	go clean
	rm -f $(BINARY_NAME)

run: build
	./$(BINARY_NAME)

release: build
	tar -czvf $(BINARY_NAME).tar.gz $(BINARY_NAME)
