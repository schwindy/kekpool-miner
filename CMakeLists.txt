cmake_minimum_required(VERSION 3.6)
project(zcash_xenon)

set(CMAKE_CXX_FLAGS "${CMAKE_CXX_FLAGS} -std=c++11")

set(SOURCE_FILES
    Linux/asm/assemble.sh
    Linux/asm/data_blake2b.asm
    Linux/asm/equihash_asm.asm
    Linux/asm/equihash_asm.o
    Linux/asm/fasm
    Linux/asm/macro_blake2b.asm
    Linux/asm/macro_eh.asm
    Linux/asm/params.inc
    Linux/asm/proc_ehprepare.asm
    Linux/asm/proc_ehsolver.asm
    Linux/asm/struct.inc
    Linux/asm/struct_eh.inc
    Linux/asm/t2.bin
    Linux/demo/simulation.c
    Linux/demo/solver.c
    "notes/algorithm description.pdf"
    Windows/data_blake2b.asm
    Windows/LICENSE.txt
    Windows/macro_blake2b.asm
    Windows/macro_eh.asm
    Windows/params.inc
    Windows/proc_ehprepare.asm
    Windows/proc_ehsolver.asm
    Windows/q.bat
    Windows/README.txt
    Windows/sim1.asm
    Windows/sim1.exe
    Windows/struct_eh.inc
    Windows/t2.bin
    Windows/test.asm
    Windows/test.exe
    history.log
    LICENSE)

add_executable(zcash_xenon ${SOURCE_FILES})