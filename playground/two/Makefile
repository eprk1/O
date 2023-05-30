

MAKEFILES_DIR := $(dir $(lastword $(MAKEFILE_LIST)))
$(info $(MAKEFILES_DIR))




build/abc/foo/bar/eugene.egg: hello
	echo Building $(notdir $@)
	echo $(dir $@)

.PHONY: hello
hello:
	if [[ "${BUILD_WHEEL}" -eq 1  ]]; \
	then \
		echo "BUILD WHEEL"; \
	else \
		echo "NOT BUILD WHEEL"; \
	fi

include $(MAKEFILES_DIR)/Makefile.2