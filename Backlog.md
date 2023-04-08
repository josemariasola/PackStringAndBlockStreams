# Backlog
## To Refine
- [ ] string litrals "Hello"s.
- [ ] Braces for initialization, no equals.
## Requested
### 2.1.0 (Medium priority)
- [ ] Continue reviews of Silva's pull requests.
- [ ] Transalte readme comments to ES.
- [ ] `Makefile`: build, test, runexampls, clean install, uninstall.
- [ ] Add static_assert(std::is_pod<T>::value, "T must be POD");
	or
	is_trivial
	or
	is_standard_layout
	En este contexto bloque es un tipo de valor que no contenga referencias o punteros. 
- [ ] Add folders: `src`, `test`, `examples`, `project(?)`.
- [ ] Add Continuous Integration.
### 3.0.0 (Low priority)
- [ ] Add to Read and Write optional parameter n that defaults to 1.
- [ ] Make `<<` and `>>` part of BlockStram.h, right now I can't work arround the ambiguities: `o<<block` `o<<aChar` `o<<aString`.
- [ ] Incorporate full StringN type.
- [ ] Allow 
std::array<char,5> a{PackString("Hello, World!")}; 
instead of 
std::array<char,5> a = PackString("Hello, World!");
Initializer list?
- [ ] Incorporte Block Type
	template<typename T>
	struct Blockk{T data;};

	template<typename T>
	std::istream& RB(std::istream& in, Blockk<T>& block){
		return in.read(
			reinterpret_cast<char*>(&block.data),
			sizeof block
		);
	}
	std::istream& operator>>(std::istream& in, Curso& v){ return ReadBlock(in, v);}
	std::ostream& operator<<(std::ostream& out, const Curso& v){return WriteBlock(out, v);}
	static_assert(std::is_compound<T>::value,":("); // TODO: Test

## In Progress

## Done
### 2.0.0 (High priority)
- [x] !!! StringPackerDriver: Use braces for initialization, when possible.
- [x] ! `README.md`: Remove equals.
- [x] ! WriteAndReadRecordsBlocksWithStrings: use a temporary or litertal instead of variable in `WriteBlock(...);`
- [x] ! WriteAndReadRecordsBlocksWithoutStrings: use a temporary or litertal instead of variable in `WriteBlock(...);`
- [x] ! `StringPackerDriver.cpp`: Remove `using namespace std`.
- [x] ! `WriteAndReadRecordsBlocksWithoutStrings.cpp`: Use for instead of while.
- [x] ! `WriteAndReadRecordsBlocksWithStrings.cpp`: Use for instead of while.
- [x] ! `WriteAndReadRecordsBlocksWithStrings.cpp`: Remove `using namespace std`.
- [x] `WriteAndReadRecordsBlocksWithoutStrings.cpp`: Remove `using namespace std;`
- [x] ! `WriteAndReadRecordsBlocksWithoutStrings.cpp`: Remove equales for initialization.
- [x] ! `WriteAndReadRecordsBlocksWithStrings.cpp`: Remove equales for initialization.
- [x] ! `WriteAndReadRecordsBlocksWithoutStrings.cpp`: Use brace instead of constructors for both streams.
- [x] ! `WriteAndReadRecordsBlocksWithStrings.cpp`: Use brace instead of constructors for both streams.
- [x] `README.md`: Add includes and scopes.
- [x] `README.md`: Include examples from source file.
- [x] Make new type: `String<N>` templated alias of `array<char,N>`.
- [x] `StringPackerDriver.cpp`: Rename `PrintArrayWithString` to `PrintStringInsideArray`.
- [x] `StringPackerDriver.cpp`: Make a print table function.
- [x] `StringPackerDriver.cpp`: Remove `using namespace std`.
- [x] `BlockStreamDriver.cpp`: Add comments.
- [x] `BlockStreamDriver.cpp`: Remove `using namespace std;`.
- [x] `BlockStreamDriver.cpp`: Use brace instead of constructors for both streams.
- [x] `BlockStreamDriver.cpp`: Remove equales for initialization.
- [x] `StringN.h`: Simplify header, move example to new file or to adoc file.
- [x] `BlockStream.h`: Simplify header, move example to new file or to adoc file.
- [x] `BlockStreamDriver.cpp`: Make it a test file, rename it, divide in two separatefiles?.
- [x] Check Pull requests from Silva.
- [x] New release.
- [x] Write release notes.
### 1.0.0
- [x] Rename `PackString.h` to `StringPacker.h`.
