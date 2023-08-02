# Terminal_HW_2

_____
### 1. Make directory dir_1
    mkdir dir_1
### 2. Go to directory dir_1
    сd dir_1
### 3. Make directory inner_dir_1
    mkdir inner_dir_1
### 4. See where you are
    pwd
### 5. Make file tf_1.txt
    touch tf_1.txt
### 6. Make file via cat.
    cat > tf_2.txt
### 7. Go to directory inner_dir_1
    cd inner_dir_1
### 8. Make file via cat.
    cat > tf_3.txt
### 9. Add the string "the second 2" to file tf_3.txt
    cat >> tf_3.txt
### 10. Add the string "the sec 2" to file tf_3.txt 
    cat >> tf_3.txt
### 11. Add the string "the sec 3" to file tf_2.txt
    cat >> ~/YARIK/dir_1/tf_2.txt
### 12. Add the string "the SeConD 3" to file tf_3.txt
    cat >> tf_3.txt
### 13. Add the string "the seConD 2" to file tf_2.txt
    cat >> ~/YARIK/dir_1/tf_2.txt
### 14. Make file tf_4.txt with 15 strings
    seq 15 | cat >> tf_4.txt
### 15. Make file tf_5.txt with 13 strings
    seq 13 | cat > tf_5.txt
### 16. Output all files in directory
    ls -la
### 17. Go out from inner_dir_1
    cd ..
### 18. Output content tf_3.txt
    cat inner_dir_1/tf_3.txt
### 19. Find way to the 'tf_4.txt' file
    find $(pwd) -name "tf_4.txt" 
or

    find . -name "tf_4.txt"    
### 20. Clear tf_4.txt content
    cat /dev/null > inner_dir_1/tf_4.txt
### 21. Find way to the files, which have "tf" in name 
    find . -name "tf*"
### 22. Find way to the files, which have "tf" in name, regardless of letter case
    find . -iname "tf*"
### 23. Find the strings in files, which have combination "sec"
    grep "sec" *
### 24. Find the strings in files, which have combination "sec", regardless of letter case
    grep -i "sec" *.*
### 25. Find the strings in files, which only have combination "sec"
    grep -w "sec" *.*
### 26. Find the strings in files, which only have combination "sec", regardless of letter case
    grep -iw "sec" *.*
### 27. Find the strings in files, which only have combination "second"
    grep -w "second" *.*
### 28. Find the strings in files, which only have combination "second", regardless of letter case
    grep -iw "second" *.*
### 29. Find the strings in files, which only have combination "second" in bellow directory
    grep -r "second" *
    
or

    grep -r "second" */
find only in bellow dir
### 30. Find only way and name the files, whic have combination "second"
    grep -rl "second" *
### 31. Find the strings in all files, which don't have combination "second"
    grep -rv "second" *
### 32. Find only way and name the files, which don't have combination "second"
    grep -rvl "second"
### 33.Output the last 4 strings 
    tail -4 inner_dir_1/tf_5.txt
### 34. Output the firs 4 strings
    head -4 inner_dir_1/tf_5.txt
### 35. One line command. Make a directory and a file with content.
    mkdir fold2 | echo "NEW TXT FILE" > n1.txt
### 36. One line command. Move text files, which have combination "sec" to any directory
    grep -rl "sec" | xargs -I{} mv {} fold2
### 37. One line command. Copy text files, which have combination "sec" to any directory
    grep -rl "sec" | xargs -I{} cp {} fold2
### 38. One line command. Find all strings with combination "sec". Add these strings to new file.
    grep -rh "sec" | cat > n1.txt
### 39. One line command. Find all strings with combination "sec". Delete these files.
    grep -rlw sec | xargs rm
### 40. Output the string "Good Job"
    echo "Good Job!!"
    
    

 
