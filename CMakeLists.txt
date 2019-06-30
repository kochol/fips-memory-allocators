# CMake entry point
cmake_minimum_required (VERSION 3.5)

# include the fips main cmake file
get_filename_component(FIPS_ROOT_DIR "../fips" ABSOLUTE)
include("${FIPS_ROOT_DIR}/cmake/fips.cmake")

fips_setup()
    fips_project(fips-memory-allocators)

    fips_begin_lib(memory-allocators)

        fips_dir(src)
        fips_files(
            Allocator.cpp 
            CAllocator.cpp 
            LinearAllocator.cpp 
            StackAllocator.cpp
            PoolAllocator.cpp
            FreeListAllocator.cpp 
        )

    fips_end_lib(memory-allocators)

fips_finish()
