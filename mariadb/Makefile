.PHONY: rock
rock:
	rockcraft pack --verbosity=debug

.PHONY: docker
docker: rock
	for rock in *.rock; do \
		rockcraft.skopeo copy oci-archive:$${rock} docker-daemon:$${rock}:latest; \
	done
