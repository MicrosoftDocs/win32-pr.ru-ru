---
title: Функции служебной программы NAP
description: Следующие служебные функции поддерживают интерфейс API NAP.
ms.assetid: 0819067c-cca5-4140-8b4d-f3b996826152
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 260c423909011c81f52ea89ce8d3137b35c55167
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103775335"
---
# <a name="nap-utility-functions"></a>Функции служебной программы NAP

> [!Note]  
> Платформа защиты доступа к сети недоступна начиная с Windows 10

 

Следующие служебные функции поддерживают интерфейс API NAP.

Все COM-интерфейсы, поддерживаемые системой защиты доступа к сети, используют стандартные правила управления памятью COM и распределитель памяти COM (CoTaskMemAlloc и CoTaskMemFree).

-   В параметрах — выделяются и освобождаются вызывающей стороной.
-   ВЫХОДНЫЕ параметры, выделенные вызываемым методом, освобожденные вызывающим объектом с помощью Котаскмем \* ()
-   ВХОДные и выходные параметры, вызываемые вызывающей стороной, освобождаются и перераспределяются вызывающей стороной в конечном итоге с помощью Котаскмем \* ()

В функциях Фрикскскс () все внедренные указатели также будут освобождены.

-   [**аллокконнектионс**](allocconnections-func.md)
-   [**аллоккаунтедстринг**](alloccountedstring-func.md)
-   [**аллокфиксупинфо**](allocfixupinfo-func.md)
-   [**фриконнектионс**](freeconnections-func.md)
-   [**фрикаунтедстринг**](freecountedstring-func.md)
-   [**фрификсупинфо**](freefixupinfo-func.md)
-   [**фриисолатионинфо**](freeisolationinfo-func.md)
-   [**фриисолатионинфоекс**](freeisolationinfoex.md)
-   [**фринапкомпонентрегистратионинфоаррай**](freenapcomponentregistrationinfoarray-func.md)
-   [**фринетворксох**](freenetworksoh-func.md)
-   [**фриприватедата**](freeprivatedata-func.md)
-   [**фрисох**](freesoh-func.md)
-   [**фрисохаттрибутевалуе**](freesohattributevalue-func.md)
-   [**фрисистемхеалсажентстате**](freesystemhealthagentstate-func.md)
-   [**инитиализенапажентнотифиер**](initializenapagentnotifier.md)
-   [**унинитиализенапажентнотифиер**](uninitializenapagentnotifier.md)

 

 




