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
# <a name="winsnmp-descriptors"></a><span data-ttu-id="50ce7-103">Дескрипторы WinSNMP</span><span class="sxs-lookup"><span data-stu-id="50ce7-103">WinSNMP Descriptors</span></span>

<span data-ttu-id="50ce7-104">В среде программирования WinSNMP *дескриптор* является одной из следующих двух структур:</span><span class="sxs-lookup"><span data-stu-id="50ce7-104">In the WinSNMP programming environment a *descriptor* is one of the following two structures:</span></span>

-   <span data-ttu-id="50ce7-105">Структура [**смиоктетс**](/windows/desktop/api/Winsnmp/ns-winsnmp-smioctets) , описывающая строковую переменную октета</span><span class="sxs-lookup"><span data-stu-id="50ce7-105">An [**smiOCTETS**](/windows/desktop/api/Winsnmp/ns-winsnmp-smioctets) structure which describes an octet string variable</span></span>
-   <span data-ttu-id="50ce7-106">Структура [**смиоид**](/windows/desktop/api/Winsnmp/ns-winsnmp-smioid) , описывающая переменную идентификатора SNMP-объекта</span><span class="sxs-lookup"><span data-stu-id="50ce7-106">An [**smiOID**](/windows/desktop/api/Winsnmp/ns-winsnmp-smioid) structure which describes an SNMP object identifier variable</span></span>

<span data-ttu-id="50ce7-107">WinSNMP-дескриптор — это структура, которая имеет два члена: Length, **Len** и pointer-Member, **ptr**.</span><span class="sxs-lookup"><span data-stu-id="50ce7-107">A WinSNMP descriptor is a structure that has two members: a length member, **len**, and a pointer member, **ptr**.</span></span> <span data-ttu-id="50ce7-108">Элемент **ptr** указывает на строку октета или интересующий идентификатор объекта.</span><span class="sxs-lookup"><span data-stu-id="50ce7-108">The **ptr** member points to the octet string or object identifier of interest.</span></span> <span data-ttu-id="50ce7-109">Элемент **ptr** может быть либо типом данных **Смилпбите** , либо **smiLPUINT32** .</span><span class="sxs-lookup"><span data-stu-id="50ce7-109">The **ptr** member can be either the **smiLPBYTE** or **smiLPUINT32** data type.</span></span>

<span data-ttu-id="50ce7-110">Дескриптор [**смиоктетс**](/windows/desktop/api/Winsnmp/ns-winsnmp-smioctets) или дескриптор [**смиоид**](/windows/desktop/api/Winsnmp/ns-winsnmp-smioid) может быть членом **value** структуры **смивалуе** .</span><span class="sxs-lookup"><span data-stu-id="50ce7-110">An [**smiOCTETS**](/windows/desktop/api/Winsnmp/ns-winsnmp-smioctets) descriptor or an [**smiOID**](/windows/desktop/api/Winsnmp/ns-winsnmp-smioid) descriptor can be the **value** member of an **smiVALUE** structure.</span></span> <span data-ttu-id="50ce7-111">Структура [**смивалуе**](/windows/desktop/api/Winsnmp/ns-winsnmp-smivalue) описывает значение, связанное с именем переменной в записи привязки переменной.</span><span class="sxs-lookup"><span data-stu-id="50ce7-111">The [**smiVALUE**](/windows/desktop/api/Winsnmp/ns-winsnmp-smivalue) structure describes the value associated with a variable name in a variable binding entry.</span></span>

<span data-ttu-id="50ce7-112">Реализация Microsoft WinSNMP выделяет и освобождает память для всех **смиоктетс** выходных и **смиоид** структур.</span><span class="sxs-lookup"><span data-stu-id="50ce7-112">The Microsoft WinSNMP implementation allocates and deallocates memory for all output **smiOCTETS** and **smiOID** structures.</span></span> <span data-ttu-id="50ce7-113">Поэтому приложение должно вызвать функцию [**снмпфридескриптор**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpfreedescriptor) , чтобы освободить память для элемента **ptr** в этих структурах.</span><span class="sxs-lookup"><span data-stu-id="50ce7-113">Therefore, the application must call the [**SnmpFreeDescriptor**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpfreedescriptor) function to free the memory for the **ptr** member of these structures.</span></span>

<span data-ttu-id="50ce7-114">Для строковых элементов в дескрипторах не требуется завершающий байт, **равный null** .</span><span class="sxs-lookup"><span data-stu-id="50ce7-114">String members in descriptors do not require a **NULL** terminating byte.</span></span> <span data-ttu-id="50ce7-115">Дополнительные сведения об управлении памятью, выделенной для дескрипторов, см. в разделе [выделение объектов WinSNMP Memory](allocating-winsnmp-memory-objects.md).</span><span class="sxs-lookup"><span data-stu-id="50ce7-115">For additional information about managing the memory allocated for descriptors, see [Allocating WinSNMP Memory Objects](allocating-winsnmp-memory-objects.md).</span></span>

 

 




