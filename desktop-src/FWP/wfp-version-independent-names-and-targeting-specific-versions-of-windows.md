---
title: Имена Version-Independent WFP и нацелены на конкретные версии Windows
description: во многих случаях API платформы фильтрации Windows (WFP) предоставляет более одной версии функции или структуры.
ms.assetid: FBDF53E5-F7DE-4DEB-AC18-6D2BB59FE670
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: baf5fbef08c3284d94eb215e0cce2fc44fc9b827b686e531057db22b60020132
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119766674"
---
# <a name="wfp-version-independent-names-and-targeting-specific-versions-of-windows"></a>Имена Version-Independent WFP и нацелены на конкретные версии Windows

во многих случаях API платформы фильтрации Windows (WFP) предоставляет более одной версии функции или структуры.

Большинство имен данных и функций в API WFP заканчиваются номером версии, например "0" или "1", даже если имеется только одна версия.

## <a name="version-mapping-in-fwpvih"></a>Сопоставление версий в фвпви. h

файл заголовка фвпви. h включается начиная с пакета SDK для Windows 7 и WDK. Этот заголовочный файл сопоставляет имя API без версий с версией, которая подходит для использования с данной операционной системой.

например, ниже приведен краткий фрагмент из версии фвпви. h, включенной в пакет SDK для Windows 8.


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
-   [**FwpmNetEventEnum1**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmneteventenum1) для Windows 7 предназначен
-   [**FwpmNetEventEnum0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmneteventenum0) для более ранних операционных систем (например, Windows Vista или Windows vista с пакетом обновления 1 (SP1))

## <a name="calling-version-independent-functions-and-structures"></a>Вызов функций и структур Version-Independent

Разработчикам WFP, предназначенным для конкретной операционной системы или версии WDK, рекомендуется всегда программироваться с помощью макросов, не зависящих от версии. При этом будет автоматически выбрана последняя версия, поддерживаемая в целевой операционной системе. Рекомендуется использовать самые последние файлы заголовков, даже при использовании более ранней операционной системы. Это позволит обеспечить использование последней поддерживаемой версии, а также упростить обслуживание и обновление кода.

В [справочной документации по API WFP](fwp-reference.md) описывается каждая версия нумерованного API. Если существует более одной версии, задается Целевая операционная система. однако разработчикам обычно требуется вызывать ненезависимые от версии интерфейсы api, а также указывать целевую операционную систему (например, **нтдди \_ WIN6** для Windows Vista или **нтдди \_ WIN8** для Windows 8).

Чтобы обеспечить правильную обработку функций, которые принимают разные параметры в разных версиях, можно включить условные блоки, такие как `#if (NTDDI_VERSION >= NTDDI_WIN7)` .

 

 




