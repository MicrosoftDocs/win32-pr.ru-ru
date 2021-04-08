---
title: Строки в стиле C
description: WinSNMP-приложение может использовать заканчивающиеся нулем строки в стиле C для преобразования объектов сущностей и идентификаторов объектов (OID) в строковые представления и обратно.
ms.assetid: df04071c-df46-410b-ad92-6adecbfcd454
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 878398b6d8691982aa90b9f1376a38214030e52e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103887451"
---
# <a name="c-style-strings"></a>Строки в стиле C

WinSNMP-приложение **может использовать заканчивающиеся нулем строки** в стиле C для преобразования объектов сущностей и идентификаторов объектов (OID) в строковые представления и обратно.

Функции WinSNMP, управляющие строками в стиле C, включают [**снмпстртоентити**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpstrtoentity), [**снмпентититостр**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpentitytostr), [**снмпстртуид**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpstrtooid)и [**снмпоидтостр**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpoidtostr). Поскольку [**снмпентититостр**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpentitytostr) и [**снмпоидтостр**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpoidtostr) возвращают указатель на строковую переменную в стиле C, при вызове этих функций WinSNMP-приложение должно передать соответствующее значение в параметре *size* . Дополнительные сведения см. на страницах справочника по этим функциям.

> [!Note]  
> Параметр *context* функций [**снмпстртоконтекст**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpstrtocontext) и [**снмпконтексттостр**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcontexttostr) должен быть структурой строки октета, то есть структурой [**смиоктетс**](/windows/desktop/api/Winsnmp/ns-winsnmp-smioctets) . Параметр *контекста* не может быть строкой в стиле C. Строка, содержащаяся в структуре **смиоктетс** , не требует нулевого байта, заканчивающегося **нулевым значением**.

 

 

 




