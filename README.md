# 2020-monash-summer-project

this project is under supervision of Dr. Khalajzadeh &amp; Dr. Obie in monash university

# Detecting values-violating defects in source code (mobile apps)


### program structure


\begin{algorithm}
\footnotesize
	\caption{Media API/Universalism value violation detector}
    \label{algorithm:Media universalism}
	\begin{flushleft}
        \textbf{INPUT:} : $JavaPath$ java file path\\
        \textbf{OUTPUT:} return a boolean value: \\
            \qquad $True$: violation exist \\
            \qquad $False$: violation does not exist
    \end{flushleft}
	\begin{algorithmic}[1]
	    \State /*using deep first search to search all the AST nodes out*/
	    \State $AstNodes \leftarrow $ search( $JavaPath$ )
		\State $ViolationList\leftarrow $ an empty list
		\State $VarNames\leftarrow $ an empty list
		\For {\textbf{all} $AstNode$ $in$ $AstNodes$}
		\If{$AstNode$ $is$ Import Decelerator Node}
		\If{\textbf{``com.google.android.exoplayer"} = $AstNode$.path}
		\State append \textbf{"Violation"} $in$ $ViolationList$
		\EndIf
		\EndIf
		\EndFor
		
		\For{ \textbf{all} $ListElement$ $in$ $ViolationList$}
		\If{$ListElement$ = \textbf{``Violation"}}
		\State \textbf{Return} True
		\EndIf
		\EndFor
		\State \textbf{Return} False
		
	\end{algorithmic} 
\end{algorithm} 



#### 1. animation


#### 2. hardware


#### 3. media


#### 4. mtp


#### 5. nfc


#### 6. telephony

