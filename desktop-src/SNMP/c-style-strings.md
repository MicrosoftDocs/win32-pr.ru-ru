---
title: Строки в стиле C
description: WinSNMP-приложение может использовать заканчивающиеся нулем строки в стиле C для преобразования объектов сущностей и идентификаторов объектов (OID) в строковые представления и обратно.
ms.assetid: df04071c-df46-410b-ad92-6adecbfcd454
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6449514d4c08baae638d950a42f7f553e0037efe6bdc45b8045dbd315c1a2c65
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119009756"
---
# <a name="c-style-strings"></a>Строки в стиле C

WinSNMP-приложение **может использовать заканчивающиеся нулем строки** в стиле C для преобразования объектов сущностей и идентификаторов объектов (OID) в строковые представления и обратно.

Функции WinSNMP, управляющие строками в стиле C, включают [**снмпстртоентити**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpstrtoentity), [**снмпентититостр**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpentitytostr), [**снмпстртуид**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpstrtooid)и [**снмпоидтостр**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpoidtostr). Поскольку [**снмпентититостр**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpentitytostr) и [**снмпоидтостр**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpoidtostr) возвращают указатель на строковую переменную в стиле C, при вызове этих функций WinSNMP-приложение должно передать соответствующее значение в параметре *size* . Дополнительные сведения см. на страницах справочника по этим функциям.

> [!Note]  
> Параметр *context* функций [**снмпстртоконтекст**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpstrtocontext) и [**снмпконтексттостр**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcontexttostr) должен быть структурой строки октета, то есть структурой [**смиоктетс**](/windows/desktop/api/Winsnmp/ns-winsnmp-smioctets) . Параметр *контекста* не может быть строкой в стиле C. Строка, содержащаяся в структуре **смиоктетс** , не требует нулевого байта, заканчивающегося **нулевым значением**.

 

 

 




