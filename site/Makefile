all: clean
	npm run generate

commit:
	git commit -m 'Generated site'

release:
	rsync -a htdocs/ dirac.chilts.org:/var/lib/chilts-static/nodejs.nz

clean:
	find . -name '*~' -delete

.PHONY: clean
