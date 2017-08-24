XML2RFC=xml2rfc

OUT = \
	jsonschema-code.html jsonschema-code.txt
	

all: $(OUT)

%.txt: %.xml
	$(XML2RFC) --text $< -o $@

%.html: %.xml
	$(XML2RFC) --html $< -o $@

json-schema.tar.gz: $(OUT)
	mkdir json-schema
	git clone . json-schema
	(cd json-schema && make)
	tar -czf json-schema.tar.gz --exclude '.*' json-schema
	rm -rf json-schema

clean:
	rm -f $(OUT) json-schema.tar.gz

.PHONY: clean
