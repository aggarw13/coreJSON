# Copyright Amazon.com, Inc. or its affiliates. All Rights Reserved.
# SPDX-License-Identifier: Apache-2.0

HARNESS_FILE=skipEscape_harness

# This value was experimentally chosen to provide 100% coverage
# without tripping unwinding assertions and without exhausting memory.
CBMC_MAX_BUFSIZE=14

UNWINDSET += skipEscape.0:$(CBMC_MAX_BUFSIZE)
UNWINDSET += skipHexEscape.0:$(CBMC_MAX_BUFSIZE)
UNWINDSET += skipOneHexEscape.0:$(CBMC_MAX_BUFSIZE)

include ../Makefile-json.common

$(PROOFDIR)/core_json.c: $(SRCDIR)/source/core_json.c
	sed 's/^static //' $< > $@
