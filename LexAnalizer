import re
import ply.lex as lex
import codecs
import sys
import os

    PalabrasReservadas = ['MODULE','SUB','END','MOD','IMPORTS','PROGRAM','MAIN','ARGS','AS','STRING',
'CONSOLE','WRITELINE','VBCRLF','DIM','READLINE','DATETIME','NOW','READKEY','TRUE','FALSE','BOOLEAN','SYSTEM']

    Tokens=PalabrasReservadas+['ID','NUMERO','SUMA','RESTA','DIV','MULTI','MENORQ','MAYORQ','IGUAL','NOIGUAL',
'PIZQ','PDER','LLIZQ','LLDER','PUNTO','UPDATE']

t_tab =r'\t '
t_suma = r'\+'
t_resta = r'\-'
t_producto = r'\*'
t_division = r'/'
t_igual = r'='
t_menorQue = r'<'
t_mayorQue = r'>'
t_parentesisIzq = r'\('
t_parentesisDer = r'\)'
t_punto = r'\.'
t_desigual = r'~='
t_llaveIzq = r'\{'
t_llaveDer = r'\}'
t_actualizar = r':=

def t_ID(t):
	r'[a-zA-Z_][a-zA-Z0-9_]*'
	if t.value.upper() in PalabrasReservadas:
		t.value = t.value.upper()		
		t.type = t.value

	return t

def t_NUMERO(t):
	r'\d+'
	t.value = int(t.value)
	return t

def t_error(t):	
	t.lexer.skip(1)

def t_newline(t):
	r'\n+'
	t.lexer.lineno += len(t.value)

def t_COMMENT(t):
	r'\'.*'
	pass

archivo= codecs.open(PROGRAMA.txt)
cadena= archivo.read()
archivo.close()

analizer= lex.lex()

analizer.input(cadena)

while True:
	token= analizador.token()
	if not token : break
	print (token)
