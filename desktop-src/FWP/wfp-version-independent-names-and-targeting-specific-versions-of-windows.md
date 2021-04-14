---
title: Имена Version-Independent WFP и нацелены на конкретные версии Windows
description: Во многих случаях API платформы фильтрации Windows (WFP) предоставляет более одной версии функции или структуры.
ms.assetid: FBDF53E5-F7DE-4DEB-AC18-6D2BB59FE670
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 41be83a50b4786aa4b98cd7f8dd7405a33fe94be
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "105661499"
---
# <a name="wfp-version-independent-names-and-targeting-specific-versions-of-windows"></a>Имена Version-Independent WFP и нацелены на конкретные версии Windows

Во многих случаях API платформы фильтрации Windows (WFP) предоставляет более одной версии функции или структуры.

Большинство имен данных и функций в API WFP заканчиваются номером версии, например "0" или "1", даже если имеется только одна версия.

## <a name="version-mapping-in-fwpvih"></a>Сопоставление версий в фвпви. h

Файл заголовка фвпви. h включается начиная с пакета SDK для Windows 7 и WDK. Этот заголовочный файл сопоставляет имя API без версий с версией, которая подходит для использования с данной операционной системой.

Например, ниже приведен краткий фрагмент из версии фвпви. h, включенной в пакет SDK для Windows 8.


```C++
#define FwpmNetEventCreateEnumHandle FwpmNetEventCreateEnumHandle0
#if (NTDDI_VERSION >= NTDDI_WIN8)
#define FwpmNetEventEnum FwpmNetEventEnum2
#elif (NTDDI_VERSION >= NTDDI_WIN7)
#define FwpmNetEventEnum FwpmNetEventEnum1
#else
#define FwpmNetEventEnum FwpmNetEventEnum0
#endif
```



Как показано выше, существует только одна версия **фвпмнетевенткреатинумхандле** – [**FwpmNetEventCreateEnumHandle0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmneteventcreateenumhandle0) — поэтому любой вызов **фвпмнетевенткреатинумхандле** всегда будет вызывать **FwpmNetEventCreateEnumHandle0**, независимо от целевой операционной системы.

Однако существуют три версии **фвпмнетевентенум**: [**FwpmNetEventEnum0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmneteventenum0), [**FwpmNetEventEnum1**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmneteventenum1)и [**FwpmNetEventEnum2**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmneteventenum2). Файл заголовка фвпви. h гарантирует, что вызов **фвпмнетевентенум** будет вызывать версию, наиболее подходящую для целевой операционной системы:

-   [**FwpmNetEventEnum2**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmneteventenum2) для Windows 8 (или более поздней версии)
-   [**FwpmNetEventEnum1**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmneteventenum1) для Windows 7 нацелена
-   [**FwpmNetEventEnum0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmneteventenum0) для более ранних операционных систем (например, Windows Vista или Windows Vista с пакетом обновления 1 (SP1))

## <a name="calling-version-independent-functions-and-structures"></a>Вызов функций и структур Version-Independent

Разработчикам WFP, предназначенным для конкретной операционной системы или версии WDK, рекомендуется всегда программироваться с помощью макросов, не зависящих от версии. При этом будет автоматически выбрана последняя версия, поддерживаемая в целевой операционной системе. Рекомендуется использовать самые последние файлы заголовков, даже при использовании более ранней операционной системы. Это позволит обеспечить использование последней поддерживаемой версии, а также упростить обслуживание и обновление кода.

В [справочной документации по API WFP](fwp-reference.md) описывается каждая версия нумерованного API. Если существует более одной версии, задается Целевая операционная система. Однако разработчики, как правило, хотят вызывать ненезависимые от версии интерфейсы API (не имеющие номера) и указывать целевую операционную систему (например, **нтдди \_ WIN6** для Windows Vista или **нтдди \_ WIN8** для Windows 8).

Чтобы обеспечить правильную обработку функций, которые принимают разные параметры в разных версиях, можно включить условные блоки, такие как `#if (NTDDI_VERSION >= NTDDI_WIN7)` .

 

 




