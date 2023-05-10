export COMPONENT_REPOS := aiops-server
export COMPONENT_REPOS := minerva-nvm minerva-cvm minerva-pc


hello: package
	echo "hello"

package:
	echo "package"
	$(foreach comp, $(COMPONENT_REPOS), \
		echo ${comp}; \
	) \
	if [[ "$(COMPONENT_REPOS)" =~ "minerva-nvm" ]]; then \
		echo "FOUND IT"; \
	else \
		echo "NOT FOUND IT"; \
	fi




