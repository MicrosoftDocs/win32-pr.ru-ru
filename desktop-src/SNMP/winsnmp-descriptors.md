---
title: Дескрипторы WinSNMP
description: В среде программирования WinSNMP дескриптор является одной из следующих двух структур.
ms.assetid: a329963b-cdb9-40d2-9a82-6f0d9f4ac73a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 875112d8519f93f4b5ae6729401f2689294a84c55dc729f0ffa24d05076e300b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119142917"
---
# <a name="winsnmp-descriptors"></a>Дескрипторы WinSNMP

В среде программирования WinSNMP *дескриптор* является одной из следующих двух структур:

-   Структура [**смиоктетс**](/windows/desktop/api/Winsnmp/ns-winsnmp-smioctets) , описывающая строковую переменную октета
-   Структура [**смиоид**](/windows/desktop/api/Winsnmp/ns-winsnmp-smioid) , описывающая переменную идентификатора SNMP-объекта

WinSNMP-дескриптор — это структура, которая имеет два члена: Length, **Len** и pointer-Member, **ptr**. Элемент **ptr** указывает на строку октета или интересующий идентификатор объекта. Элемент **ptr** может быть либо типом данных **Смилпбите** , либо **smiLPUINT32** .

Дескриптор [**смиоктетс**](/windows/desktop/api/Winsnmp/ns-winsnmp-smioctets) или дескриптор [**смиоид**](/windows/desktop/api/Winsnmp/ns-winsnmp-smioid) может быть членом **value** структуры **смивалуе** . Структура [**смивалуе**](/windows/desktop/api/Winsnmp/ns-winsnmp-smivalue) описывает значение, связанное с именем переменной в записи привязки переменной.

Реализация Microsoft WinSNMP выделяет и освобождает память для всех **смиоктетс** выходных и **смиоид** структур. Поэтому приложение должно вызвать функцию [**снмпфридескриптор**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpfreedescriptor) , чтобы освободить память для элемента **ptr** в этих структурах.

Для строковых элементов в дескрипторах не требуется завершающий байт, **равный null** . Дополнительные сведения об управлении памятью, выделенной для дескрипторов, см. в разделе [выделение объектов WinSNMP Memory](allocating-winsnmp-memory-objects.md).

 

 




