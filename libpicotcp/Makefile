#
# Copyright 2017, Data61
# Commonwealth Scientific and Industrial Research Organisation (CSIRO)
# ABN 41 687 119 230.
#
# This software may be distributed and modified according to the terms of
# the BSD 2-Clause license. Note that NO WARRANTY is provided.
# See "LICENSE_BSD2.txt" for details.
#
# @TAG(DATA61_BSD)
#

# Targets
TARGETS := libpicotcp.a

# Source files required to build the target
CFILES := $(sort $(patsubst $(SOURCE_DIR)/%,%,$(wildcard $(SOURCE_DIR)/stack/*.c)))
CFILES += $(sort $(patsubst $(SOURCE_DIR)/%,%,$(wildcard $(SOURCE_DIR)/modules/pico_tcp.c)))
CFILES += $(sort $(patsubst $(SOURCE_DIR)/%,%,$(wildcard $(SOURCE_DIR)/modules/pico_socket_tcp.c)))
CFILES += $(sort $(patsubst $(SOURCE_DIR)/%,%,$(wildcard $(SOURCE_DIR)/modules/pico_ipv4.c)))
CFILES += $(sort $(patsubst $(SOURCE_DIR)/%,%,$(wildcard $(SOURCE_DIR)/modules/pico_arp.c)))
CFILES += $(sort $(patsubst $(SOURCE_DIR)/%,%,$(wildcard $(SOURCE_DIR)/modules/pico_udp.c)))
CFILES += $(sort $(patsubst $(SOURCE_DIR)/%,%,$(wildcard $(SOURCE_DIR)/modules/pico_socket_udp.c)))
CFILES += $(sort $(patsubst $(SOURCE_DIR)/%,%,$(wildcard $(SOURCE_DIR)/modules/pico_icmp4.c)))
CFILES += $(sort $(patsubst $(SOURCE_DIR)/%,%,$(wildcard $(SOURCE_DIR)/modules/pico_dev_mock.c)))
CFILES += $(sort $(patsubst $(SOURCE_DIR)/%,%,$(wildcard $(SOURCE_DIR)/modules/pico_dev_dhcp_common.c)))
CFILES += $(sort $(patsubst $(SOURCE_DIR)/%,%,$(wildcard $(SOURCE_DIR)/modules/pico_dev_dhcp_client.c)))
CFILES += $(sort $(patsubst $(SOURCE_DIR)/%,%,$(wildcard $(SOURCE_DIR)/modules/pico_igmp.c)))
CFILES += $(sort $(patsubst $(SOURCE_DIR)/%,%,$(wildcard $(SOURCE_DIR)/modules/pico_dns_client.c)))
CFILES += $(sort $(patsubst $(SOURCE_DIR)/%,%,$(wildcard $(SOURCE_DIR)/modules/pico_dns_common.c)))
CFILES += $(sort $(patsubst $(SOURCE_DIR)/%,%,$(wildcard $(SOURCE_DIR)/modules/pico_ethernet.c)))

CORE_OBJ= stack/pico_stack.o \
          stack/pico_frame.o \
          stack/pico_device.o \
          stack/pico_protocol.o \
          stack/pico_socket.o \
          stack/pico_socket_multicast.o \
          stack/pico_tree.o \
          stack/pico_md5.o

# Header files/directories this library provides
HDRFILES := $(sort $(wildcard $(SOURCE_DIR)/include/*))
HDRFILES += $(sort $(wildcard $(SOURCE_DIR)/include/arch/*))
HDRFILES += $(sort $(wildcard $(SOURCE_DIR)/modules/*.h))
HDRFILES += $(sort $(wildcard $(SOURCE_DIR)/pico_defines.h))
# picoopts.h will be copied to $(SOURCE_DIR)/pico_defines.h by manifest


include $(SEL4_COMMON)/common.mk
