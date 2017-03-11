---
title: "Dostęp"
bg: '#ffa64d'
color: black
fa-icon: terminal
---

Ponieważ klaster wykorzystuje komputery znajdujące się na pracowni studenckiej, **nie może być eksploatowany w czasie zajęć dydaktycznych**. Prosimy o konsultację czasu wykorzystania klastra z [zespołem dydaktycznym Wydziału Biotechnologii Uniwersytetu Wrocławskiego](mailto:joanna.janicka@uwr.edu.pl). 

W celu użycia klastra w katalogu *share* należy przygotować skrypt zarządzający kolejką (**queue.sh**) i skrypt pojedynczego zadania (**single_job.sh**). Należy się upewnić, że oprogramowanie (w tym kompilatory) niezbędne do wykonania obliczeń jest zainstalowane na klastrze.

Przykładowy plik **queue.sh**.

{% highlight bash %}
#!/bin/bash

iterator=1

while [ ${iterator} -le 2 ]
do

./single_job.sh ${iterator}

iterator=$((iterator+1))
done
{% endhighlight %}

Więcej przykładowych skryptów można pobrać z [repozytorium klastra](https://github.com/michbur/cluster_example).

Inne informacje o użytkowniu klastrów opartych na TORQUE można znaleźć np. [TUTAJ](http://qcd.phys.cmu.edu/QCDcluster/pbs/run_serial.html).