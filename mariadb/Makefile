VERSIONS = 10.5 11.6 11.7

.PHONY: build
build: fetch
	for version in $(VERSIONS); do \
		echo "building $${version}"; \
		cd mariadb-docker/$${version}; \
		docker buildx build --tag mariadb/$${version}-ubuntu .; \
		cd ../..; \
	done

.PHONY: fetch
fetch:
	git clone https://github.com/MariaDB/mariadb-docker.git \
