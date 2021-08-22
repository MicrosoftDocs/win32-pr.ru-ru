---
title: Функции служебной программы NAP
description: Следующие служебные функции поддерживают интерфейс API NAP.
ms.assetid: 0819067c-cca5-4140-8b4d-f3b996826152
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d9b421069804a4047b511b775c7ffafe5b4b987eb0b0ad5105f48df0ed990e22
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118620785"
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

 

 




