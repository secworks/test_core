#===================================================================
#
# Makefile
# --------
# Makefile for building test_core simulations.
#
#
# Author: Joachim Strombergson
# Copyright (c) 2014, Secworks Sweden AB
# All rights reserved.
# 
# Redistribution and use in source and binary forms, with or 
# without modification, are permitted provided that the following 
# conditions are met: 
# 
# 1. Redistributions of source code must retain the above copyright 
#    notice, this list of conditions and the following disclaimer. 
# 
# 2. Redistributions in binary form must reproduce the above copyright 
#    notice, this list of conditions and the following disclaimer in 
#    the documentation and/or other materials provided with the 
#    distribution. 
# 
# THIS SOFTWARE IS PROVIDED BY THE COPYRIGHT HOLDERS AND CONTRIBUTORS 
# "AS IS" AND ANY EXPRESS OR IMPLIED WARRANTIES, INCLUDING, BUT NOT 
# LIMITED TO, THE IMPLIED WARRANTIES OF MERCHANTABILITY AND FITNESS 
# FOR A PARTICULAR PURPOSE ARE DISCLAIMED. IN NO EVENT SHALL THE 
# COPYRIGHT OWNER OR CONTRIBUTORS BE LIABLE FOR ANY DIRECT, INDIRECT, 
# INCIDENTAL, SPECIAL, EXEMPLARY, OR CONSEQUENTIAL DAMAGES (INCLUDING, 
# BUT NOT LIMITED TO, PROCUREMENT OF SUBSTITUTE GOODS OR SERVICES;
# LOSS OF USE, DATA, OR PROFITS; OR BUSINESS INTERRUPTION) HOWEVER 
# CAUSED AND ON ANY THEORY OF LIABILITY, WHETHER IN CONTRACT, 
# STRICT LIABILITY, OR TORT (INCLUDING NEGLIGENCE OR OTHERWISE) 
# ARISING IN ANY WAY OUT OF THE USE OF THIS SOFTWARE, EVEN IF 
# ADVISED OF THE POSSIBILITY OF SUCH DAMAGE.
#
#===================================================================

TEST_CORE_SRC=../src/rtl/test_core.v
TEST_CORE_TB_SRC=../src/tb/tb_test_core.v

CC=iverilog


all: test_core


test_core:  $(TEST_CORE_TB_SRC) $(TEST_CORE_SRC)
	$(CC) -o test_core.sim $(TEST_CORE_TB_SRC) $(TEST_CORE_SRC)

sim-test_core: test_core.sim
	./test_core.sim	


clean:
	rm -f test_core.sim


help:
	@echo "Supported targets:"
	@echo "------------------"
	@echo "all:           Build all simulation targets."
	@echo "test_core:     Build the uart simulation target."
	@echo "sim-test_core: Run the uart simulation."
	@echo "clean:         Delete all built files."

#===================================================================
# EOF Makefile
#===================================================================

