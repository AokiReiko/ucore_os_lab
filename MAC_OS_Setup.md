##在MAC OS下配置实验环境
1. **install homebrew**  
  
2. **install binutils, gcc, gdb targeting i386-elf**  
	注意在第一步完成后，需要修改rb文件。  
	一是SHA256验证码错误，修改/usr/local/Homebrew/Library/Taps/altkatz/homebrew-gcc_cross_compilers路径下相应的SHA256值。  
	二是修改上述路径的i386-elf-gcc.rb文件。将"binutils = Formula.factory 'i386-elf-binutils'"修改为“binutils = Formulary.factory 'i386-elf-binutils'”

	````
	brew tap altkatz/homebrew-gcc_cross_compilers  
	brew install i386-elf-gcc # may take an hour  
	brew install i386-elf-gdb  
	````
3. **install qemu-system-i386**  
brew install qemu