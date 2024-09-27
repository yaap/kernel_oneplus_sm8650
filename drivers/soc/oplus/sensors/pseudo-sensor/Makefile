ifeq ($(OPLUS_FEATURE_BSP_DRV_VND_INJECT_TEST),1)
KBUILD_OPTIONS += CONFIG_PSEUDO_SENSOR=m
$(info OPLUS_FEATURE_BSP_DRV_VND_INJECT_TEST and CONFIG_PSEUDO_SENSOR is module)
else
KBUILD_OPTIONS += CONFIG_PSEUDO_SENSOR=n
$(info OPLUS_FEATURE_BSP_DRV_VND_INJECT_TEST and CONFIG_PSEUDO_SENSOR is nothing)
endif

KERNEL_SRC ?= /lib/modules/$(shell uname -r)/build
M ?= $(shell pwd)
modules modules_install clean:
	$(MAKE) -C $(KERNEL_SRC) M=$(M) $(KBUILD_OPTIONS) W=1 $(@)

