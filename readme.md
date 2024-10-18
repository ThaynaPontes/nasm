# Estudo de comando NASM
## primeiros comandos

* Programa hello world

```Assembly

global _star
   Section .text
   _start:
     mov rax,1        ; prepara o sistema para fazer a escrita de um texto
     mov rdi,1        ; prepara a saida do texto na tela
     mov rsi,mensagem ;imprimeir ou exiber a mensagem na tela
     mov rdx,13       ;quantidade de caracteres
     syscall          ;chama o sistema para preparar a saida
     mov rax,60       ;chama para a saida do sistema
     xor rdi, rdi      ; executar a saida do sistema 
     syscall          ;inovocar o sistema operacional para fechar

     Section .data
     mensagem:db 'Hello.world',10    ;o valor 10 representa a quebra de linha

```