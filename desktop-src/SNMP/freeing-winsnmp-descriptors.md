---
title: Освобождение дескрипторов WinSNMP
description: Среда WinSNMP — это назначение освобождения ресурсов дескриптора в реализацию WinSNMP или WinSNMP Application, в зависимости от того, какой компонент выделяет память для дескриптора.
ms.assetid: 3e4cbbc5-18bc-4731-971c-6e533d904f56
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 86081a69cd5455bc3c58ca2bcea50154d75920a17655a1feef30ac2d29675d0c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119009532"
---
# <a name="freeing-winsnmp-descriptors"></a>Освобождение дескрипторов WinSNMP

Среда WinSNMP — это назначение освобождения ресурсов дескриптора в реализацию WinSNMP или WinSNMP Application, в зависимости от того, какой компонент выделяет память для дескриптора.

Чтобы освободить ресурсы для [**смиоид**](/windows/desktop/api/Winsnmp/ns-winsnmp-smioid) или дескриптора [**смиоктетс**](/windows/desktop/api/Winsnmp/ns-winsnmp-smioctets) , применяются следующие правила.

-   Для входных параметров

    Поскольку приложение WinSNMP выделяет память для входных объектов с переменными длиной, приложение должно освободить эту память с помощью соответствующей функции. Например, если приложение выделило ресурсы с помощью вызова функции [**GlobalAlloc**](/windows/desktop/api/winbase/nf-winbase-globalalloc) , для освобождения ресурсов следует использовать функцию [**GlobalFree**](/windows/desktop/api/winbase/nf-winbase-globalfree) . Если приложение выделило ресурсы с помощью вызова функции [**хеапаллок**](/windows/desktop/api/heapapi/nf-heapapi-heapalloc) , оно должно вызвать функцию [**хеапфри**](/windows/desktop/api/heapapi/nf-heapapi-heapfree) .

-   Для выходных параметров

    Вызов любой из следующих функций приводит к реализации выделения памяти для дескриптора [**смиоид**](/windows/desktop/api/Winsnmp/ns-winsnmp-smioid) или [**смиоктетс**](/windows/desktop/api/Winsnmp/ns-winsnmp-smioctets) : [**снмпжетвб**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpgetvb), [**снмпенкодемсг**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpencodemsg), [**снмпоидкопи**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpoidcopy), [**снмпконтексттостр**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcontexttostr)и [**снмпстртуид**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpstrtooid).

    Поскольку реализация выделяет память для этих выходных объектов, приложение должно вызвать функцию [**снмпфридескриптор**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpfreedescriptor) для освобождения ресурсов. Эта функция позволяет реализации освободить память, выделенную для элемента **ptr** в этих структурах.

Чтобы освободить ресурсы для структуры [**смивалуе**](/windows/desktop/api/Winsnmp/ns-winsnmp-smivalue) , приложение WinSNMP должно проверить элемент **синтаксиса** структуры [**смивалуе**](/windows/desktop/api/Winsnmp/ns-winsnmp-smivalue) , чтобы правильно вычислить **значение** элемента структуры. Если элемент **синтаксиса** указывает, что элемент **value** является [**смиоктетс**](/windows/desktop/api/Winsnmp/ns-winsnmp-smioctets) или дескриптором [**смиоид**](/windows/desktop/api/Winsnmp/ns-winsnmp-smioid) , а реализация выделила ресурсы для дескриптора, приложение должно вызвать [**снмпфридескриптор**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpfreedescriptor). Это позволяет реализации освободить память. Если приложение выделило ресурсы, оно должно освободить память с помощью соответствующей функции, как показано выше.

Дополнительные сведения см. в разделе [выделение объектов WinSNMP Memory](allocating-winsnmp-memory-objects.md).

 

 