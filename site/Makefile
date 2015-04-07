all: generate

server:
	npm start

generate: clean
	npm run generate

commit:
	git commit -m 'Generated site'

release:
	rsync -a htdocs/ dirac.chilts.org:/var/lib/chilts-static/nodejs.nz

clean:
	npm run clean
	git checkout htdocs/
	find . -name '*~' -delete

.PHONY: clean
