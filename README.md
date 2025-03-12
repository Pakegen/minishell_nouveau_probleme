# minishell_nouveau_probleme

# probleme avec echo qui prends tous ce qui est apres lui en chaine de caractere voir ou est le probleme
## probleme de token malloc et et avec execv :
"==170880== Syscall param execve(filename) points to unaddressable byte(s)
==170880==    at 0x49B208B: execve (syscall-template.S:120)
==170880==    by 0x40503C: child_execute (in /home/quenalla/42/cercle_3/minishell/minishell_95%/minishell)
==170880==    by 0x404E5D: handle_fork_and_update (in /home/quenalla/42/cercle_3/minishell/minishell_95%/minishell)
==170880==    by 0x404D61: execute_pipeline (in /home/quenalla/42/cercle_3/minishell/minishell_95%/minishell)
==170880==    by 0x40361E: exec_command (in /home/quenalla/42/cercle_3/minishell/minishell_95%/minishell)
==170880==    by 0x4036D6: main (in /home/quenalla/42/cercle_3/minishell/minishell_95%/minishell)
==170880==  Address 0x0 is not stack'd, malloc'd or (recently) free'd
==170880== 
execve: Bad address
==170880== 
==170880== HEAP SUMMARY:
==170880==     in use at exit: 217,996 bytes in 596 blocks
==170880==   total heap usage: 904 allocs, 308 frees, 272,498 bytes allocated
==170880== 
==170880== 108 (96 direct, 12 indirect) bytes in 1 blocks are definitely lost in loss record 40 of 94
==170880==    at 0x4848899: malloc (in /usr/libexec/valgrind/vgpreload_memcheck-amd64-linux.so)
==170880==    by 0x4019A0: advanced_tokenize (in /home/quenalla/42/cercle_3/minishell/minishell_95%/minishell)
==170880==    by 0x404717: parse_command (in /home/quenalla/42/cercle_3/minishell/minishell_95%/minishell)
==170880==    by 0x4047A6: fill_pipeline (in /home/quenalla/42/cercle_3/minishell/minishell_95%/minishell)
==170880==    by 0x404894: parse_input (in /home/quenalla/42/cercle_3/minishell/minishell_95%/minishell)
==170880==    by 0x4035FE: exec_command (in /home/quenalla/42/cercle_3/minishell/minishell_95%/minishell)
==170880==    by 0x4036D6: main (in /home/quenalla/42/cercle_3/minishell/minishell_95%/minishell)
==170880== 
==170880== LEAK SUMMARY:
==170880==    definitely lost: 96 bytes in 1 blocks
==170880==    indirectly lost: 12 bytes in 1 blocks
==170880==      possibly lost: 0 bytes in 0 blocks
==170880==    still reachable: 217,888 bytes in 594 blocks
==170880==         suppressed: 0 bytes in 0 blocks
==170880== Reachable blocks (those to which a pointer was found) are not shown.
==170880== To see them, rerun with: --leak-check=full --show-leak-kinds=all
==170880== 
==170880== ERROR SUMMARY: 2 errors from 2 contexts (suppressed: 0 from 0)
==170880== 
==170880== 1 errors in context 1 of 2:
==170880== Syscall param execve(filename) points to unaddressable byte(s)
==170880==    at 0x49B208B: execve (syscall-template.S:120)
==170880==    by 0x40503C: child_execute (in /home/quenalla/42/cercle_3/minishell/minishell_95%/minishell)
==170880==    by 0x404E5D: handle_fork_and_update (in /home/quenalla/42/cercle_3/minishell/minishell_95%/minishell)
==170880==    by 0x404D61: execute_pipeline (in /home/quenalla/42/cercle_3/minishell/minishell_95%/minishell)
==170880==    by 0x40361E: exec_command (in /home/quenalla/42/cercle_3/minishell/minishell_95%/minishell)
==170880==    by 0x4036D6: main (in /home/quenalla/42/cercle_3/minishell/minishell_95%/minishell)
==170880==  Address 0x0 is not stack'd, malloc'd or (recently) free'd
==170880== 
==170880== ERROR SUMMARY: 2 errors from 2 contexts (suppressed: 0 from 0)
"



# signal finie vraiment finie 
