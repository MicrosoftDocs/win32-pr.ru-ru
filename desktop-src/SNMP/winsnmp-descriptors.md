---
title: Дескрипторы WinSNMP
description: В среде программирования WinSNMP дескриптор является одной из следующих двух структур.
ms.assetid: a329963b-cdb9-40d2-9a82-6f0d9f4ac73a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8cd7f844ab1365d6020afce0ca7bfeb3afa244a8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104328803"
---
# <a name="winsnmp-descriptors"></a>Дескрипторы WinSNMP

В среде программирования WinSNMP *дескриптор* является одной из следующих двух структур:

-   Структура [**смиоктетс**](/windows/desktop/api/Winsnmp/ns-winsnmp-smioctets) , описывающая строковую переменную октета
-   Структура [**смиоид**](/windows/desktop/api/Winsnmp/ns-winsnmp-smioid) , описывающая переменную идентификатора SNMP-объекта

WinSNMP-дескриптор — это структура, которая имеет два члена: Length, **Len** и pointer-Member, **ptr**. Элемент **ptr** указывает на строку октета или интересующий идентификатор объекта. Элемент **ptr** может быть либо типом данных **Смилпбите** , либо **smiLPUINT32** .

Дескриптор [**смиоктетс**](/windows/desktop/api/Winsnmp/ns-winsnmp-smioctets) или дескриптор [**смиоид**](/windows/desktop/api/Winsnmp/ns-winsnmp-smioid) может быть членом **value** структуры **смивалуе** . Структура [**смивалуе**](/windows/desktop/api/Winsnmp/ns-winsnmp-smivalue) описывает значение, связанное с именем переменной в записи привязки переменной.

Реализация Microsoft WinSNMP выделяет и освобождает память для всех **смиоктетс** выходных и **смиоид** структур. Поэтому приложение должно вызвать функцию [**снмпфридескриптор**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpfreedescriptor) , чтобы освободить память для элемента **ptr** в этих структурах.

Для строковых элементов в дескрипторах не требуется завершающий байт, **равный null** . Дополнительные сведения об управлении памятью, выделенной для дескрипторов, см. в разделе [выделение объектов WinSNMP Memory](allocating-winsnmp-memory-objects.md).

 

 




