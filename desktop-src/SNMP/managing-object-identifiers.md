---
title: Управление идентификаторами объектов
description: API-интерфейс WinSNMP предоставляет несколько служебных функций WinSNMP, упрощающих обработку идентификаторов объектов для WinSNMP Applications.
ms.assetid: 6ca5f5bc-aa49-4826-97a7-2ea4a882dc2d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f9745cb8018b6833a1ef0569e69f201c621aa38e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104486984"
---
# <a name="managing-object-identifiers"></a>Управление идентификаторами объектов

API-интерфейс WinSNMP предоставляет несколько [служебных функций WinSNMP](winsnmp-functions.md) , упрощающих обработку идентификаторов объектов для WinSNMP Applications.

Функция [**снмпоидтостр**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpoidtostr) преобразует внутреннее двоичное представление идентификатора объекта в формат числовой строки с точками. При вызове [**снмпоидтостр**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpoidtostr)укажите БУФЕР строки максобжидстрсизе length (1408 байт), чтобы размер выходного буфера был достаточно большим, чтобы вместить преобразованную строку. Чтобы преобразовать идентификатор объекта из числового формата, разделенного точками, во внутреннее двоичное представление, вызовите функцию [**снмпстртуид**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpstrtooid) .

Чтобы скопировать идентификатор объекта SNMP, вызовите функцию [**снмпоидкопи**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpoidcopy) . Эта функция выделяет необходимую память для нового идентификатора объекта.

Для освобождения ресурсов, выделенных для элемента **ptr** структуры [**смиоид**](/windows/desktop/api/Winsnmp/ns-winsnmp-smioid) , заданной в функциях [**Снмпстртуид**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpstrtooid) и [**Снмпоидкопи**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpoidcopy) , приложение WinSNMP должно вызывать функцию [**снмпфридескриптор**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpfreedescriptor) .

Функция [**снмпоидкомпаре**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpoidcompare) сравнивает два идентификатора объектов SNMP. В приложении WinSNMP можно указать количество подидентификаторов для сравнения. Вызовите **снмпоидкомпаре** , чтобы определить, имеют ли два идентификатора объектов общие префиксы.

Дополнительные сведения об управлении памятью, выделенной для идентификаторов объектов, см. в разделе [выделение объектов WinSNMP Memory](allocating-winsnmp-memory-objects.md).

 

 




