https://swish.swi-prolog.org/p/Hangout.swinb


homem(cesar).
homem(davi).
homem(paulo).
homem(joao).
mulher(ana).
mulher(maria).
mulher(lucia).
mulher(joana).
pai(cesar,davi). % cesar é pai de davi
pai(cesar,joao). % cesar é pai de joao
pai(davi,paulo). % davi é pai de paulo
pai(davi,ana). % davi é pai de ana
pai(davi,joana). % davi é pai de joana
mae(maria,joana). % maria é mae de joana
mae(maria,lucia). % maria é mae de lucia
%
irmaos(I,X) :- homem(I), pai(P,I), pai(P,X), I\=X.
irmaos(I,X) :- homem(I), mae(M,I), mae(M,X), I\=X.
irmas(I,X) :- mulher(I), pai(P,I), pai(P,X), I\=X.
irmas(I,X) :- mulher(I), mae(M,I), mae(M,X), I\=X.


irmaos(X,joana)


irmas(J,lucia)
