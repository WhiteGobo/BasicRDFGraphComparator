include(FetchContent)

FetchContent_Declare(
    Corrosion
    GIT_REPOSITORY https://github.com/corrosion-rs/corrosion.git
    GIT_TAG v0.6 # Optionally specify a commit hash, version tag or branch here
)
FetchContent_MakeAvailable(Corrosion)

corrosion_import_crate(MANIFEST_PATH Cargo.toml)
target_sources(BasicRDFGraphComparator INTERFACE
        FILE_SET HEADERS
        BASE_DIRS ./
        FILES
	BasicRDFGraphComparator.h
)

