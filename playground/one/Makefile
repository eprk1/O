export COMPONENT_REPOS := aiops-server
export COMPONENT_REPOS := minerva-nvm minerva-cvm minerva-pc

MAKEFILES_DIR := $(dir $(lastword $(MAKEFILE_LIST)))
$(info $(MAKEFILES_DIR))

BUILDSTREAM ?= 0
include $(MAKEFILES_DIR)/Makefile.2

#make: *** No rule to make target `Makefile.secret'.  Stop.
-include Makefile.secret



hello: $(PYTHON2_BASE_STAMP) helloo Makefile.secret
	echo "hello from Makefile"
	echo $(SECRET_SAUCE)




$(PYTHON2_BASE_STAMP):
	echo "hola from Makefile"

Makefile.secret:
	cp secret/Makefile.secret .

package:
	echo "package from Makefile"
	$(foreach comp, $(COMPONENT_REPOS), \
		echo ${comp}; \
	) \
	if [[ "$(COMPONENT_REPOS)" =~ "minerva-nvm" ]]; then \
		echo "FOUND IT"; \
	else \
		echo "NOT FOUND IT"; \
	fi




