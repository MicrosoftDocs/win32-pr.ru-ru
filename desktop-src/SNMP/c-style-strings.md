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
# <a name="c-style-strings"></a><span data-ttu-id="c97f2-103">Строки в стиле C</span><span class="sxs-lookup"><span data-stu-id="c97f2-103">C-Style Strings</span></span>

<span data-ttu-id="c97f2-104">WinSNMP-приложение **может использовать заканчивающиеся нулем строки** в стиле C для преобразования объектов сущностей и идентификаторов объектов (OID) в строковые представления и обратно.</span><span class="sxs-lookup"><span data-stu-id="c97f2-104">A WinSNMP application can use **NULL**-terminated C-style strings to convert entity and object identifier (OID) objects to and from their string representations.</span></span>

<span data-ttu-id="c97f2-105">Функции WinSNMP, управляющие строками в стиле C, включают [**снмпстртоентити**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpstrtoentity), [**снмпентититостр**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpentitytostr), [**снмпстртуид**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpstrtooid)и [**снмпоидтостр**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpoidtostr).</span><span class="sxs-lookup"><span data-stu-id="c97f2-105">The WinSNMP functions that manipulate C-style strings include [**SnmpStrToEntity**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpstrtoentity), [**SnmpEntityToStr**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpentitytostr), [**SnmpStrToOid**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpstrtooid), and [**SnmpOidToStr**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpoidtostr).</span></span> <span data-ttu-id="c97f2-106">Поскольку [**снмпентититостр**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpentitytostr) и [**снмпоидтостр**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpoidtostr) возвращают указатель на строковую переменную в стиле C, при вызове этих функций WinSNMP-приложение должно передать соответствующее значение в параметре *size* .</span><span class="sxs-lookup"><span data-stu-id="c97f2-106">Because [**SnmpEntityToStr**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpentitytostr) and [**SnmpOidToStr**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpoidtostr) return a pointer to a C-style string variable, the WinSNMP application must pass an appropriate value in the *size* parameter when it makes calls to these functions.</span></span> <span data-ttu-id="c97f2-107">Дополнительные сведения см. на страницах справочника по этим функциям.</span><span class="sxs-lookup"><span data-stu-id="c97f2-107">For more information, see the reference pages for these functions.</span></span>

> [!Note]  
> <span data-ttu-id="c97f2-108">Параметр *context* функций [**снмпстртоконтекст**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpstrtocontext) и [**снмпконтексттостр**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcontexttostr) должен быть структурой строки октета, то есть структурой [**смиоктетс**](/windows/desktop/api/Winsnmp/ns-winsnmp-smioctets) .</span><span class="sxs-lookup"><span data-stu-id="c97f2-108">The *context* parameter of the [**SnmpStrToContext**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpstrtocontext) and [**SnmpContextToStr**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcontexttostr) functions must be an octet string structure, that is, an [**smiOCTETS**](/windows/desktop/api/Winsnmp/ns-winsnmp-smioctets) structure.</span></span> <span data-ttu-id="c97f2-109">Параметр *контекста* не может быть строкой в стиле C.</span><span class="sxs-lookup"><span data-stu-id="c97f2-109">The *context* parameter cannot be a C-style string.</span></span> <span data-ttu-id="c97f2-110">Строка, содержащаяся в структуре **смиоктетс** , не требует нулевого байта, заканчивающегося **нулевым значением**.</span><span class="sxs-lookup"><span data-stu-id="c97f2-110">The string contained in an **smiOCTETS** structure does not require a **NULL**-terminating byte.</span></span>

 

 

 




