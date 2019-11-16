# SharperSearch

## Description

Note: Credit for the original SharpSearch goes to https://github.com/djhohnstein, thanks for the work.
I've added the following features:
  - Verbose
  - year
  - ext_whitelist
  - ext_blacklist
  - search_whitelist
  - searchterms

## Usage

```
Usage:
    Arguments:
        Required:
            path          - Path to search for files. Note: If using quoted paths, ensure you
                            escape backslashes properly.
        
        Optional:
            patttern      - Type of files to search for, e.g. "*.txt" (Optional)
            searchterm    - Regex to search for within files. (Optional)
            -V            - Verbose: Print lines contraining matches (Optional)
            year          - Filter by year e.g. year:2019 (Optional)
            ext_whitelist     - Specify file extension whitelist: (Optional)
                              - This should speed up performance
                                InputFile:       ext.txt:   
                                                __________                                                     
                                                |.txt    |
                                                |.aspx   |
                                                |________|
                                e.g. whitelist:"path\\to\\ext.txt"
           ext_blacklist      - Specify file extension blacklist: (Optional)
                                e.g. blacklist:"path\\to\\ext.txt"
           search_whitelist      - Specify searchterm whitelist: (Optional)
                                e.g. search_whitelist:"path\\to\\ext.txt"
           searchterms        - Specify a comma deliminated list of searchterms (Optional)
                                e.g. searchterms:foo,bar,asdf
    Examples:
        
        Find all files that have the phrase ""password"" in them.
        
            SharpSearch.exe path:""C:\\Users\\User\\My Documents\\"" searchterm:password

        Search for all batch files on a remote share that contain the word ""Administrator""

            SharpSearch.exe path:""\\\\server01\\SYSVOL\\domain\\scripts\\"" pattern:*.bat searchTerm:Administrator 
```

## Examples

- Search for all text files in C:\Users\EXAMPLE\hashcat-4.2.1\wordlists

```
Directory of C:\Users\EXAMPLE\hashcat-4.2.1\wordlists
        12/12/2018 12:00:00 AM       736.78 MB 899_have-i-been-pwned-v3--v2-excluded-_found_hash_plain.txt

               1 Files(s)       736.78 MB

Directory of C:\Users\EXAMPLE\hashcat-4.2.1\wordlists\crackstation-human-only.txt
        9/5/2010 12:00:00 AM       683.25 MB realhuman_phill.txt

               1 Files(s)       683.25 MB

Directory of C:\Users\EXAMPLE\hashcat-4.2.1\wordlists\ProbWL-v2-Real-Passwords-7z\Top2Billion-probable-v2
        2/16/2018 12:00:00 AM        20.25 GB Top2Billion-probable-v2.txt

               1 Files(s)        20.25 GB

        Total Files Listed:
               3 File(s)     21.64 GB
               3 Dir(s)
```




