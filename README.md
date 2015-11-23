# lisp-learning


##commonlisp setup：

http://www.jonathanfischer.net/modern-common-lisp-on-windows/

http://www.gigamonkeys.com/book

https://yoo2080.wordpress.com/2013/08/18/how-to-install-common-lisp-and-slime-on-ms-windows/#sec-1

##quicklisp
(load "C:/my_programs/clisp_workspace/quicklisp.lisp")
(quicklisp-quickstart:install :path "C:\\quicklisp\\")
(ql:quickload "quicklisp-slime-helper")

##clisprc position：
C:\Users\username\AppData\Roaming\.clisprc.lisp

;;; Load Quicklisp when CLISP launches
#-quicklisp
(let ((quicklisp-init "C:\\my_programs\\quicklisp\\setup.lisp"))
  (when (probe-file quicklisp-init)
    (load quicklisp-init)))

;;; Fix for CLISP on Windows.
(setf temporary-file-directory "C:\\Users\\CaoLijuan\\AppData\\Local\\Temp")
(setf (ext:getenv "temp") temporary-file-directory)
(setf (ext:getenv "tmp") temporary-file-directory)
