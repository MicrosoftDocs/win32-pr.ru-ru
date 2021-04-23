---
description: Квалификаторы meta уточняют определение мета-конструкций в модели CIM путем уточнения фактического использования объявления класса или свойства в синтаксисе MOF.
ms.assetid: 3674a051-3756-4d09-a70e-46a57b442104
ms.tgt_platform: multiple
title: Квалификаторы Meta
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c8618ef8258f403a43e08be54b3acbd5bb1e923c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105656638"
---
# <a name="meta-qualifiers"></a><span data-ttu-id="3973c-103">Квалификаторы Meta</span><span class="sxs-lookup"><span data-stu-id="3973c-103">Meta Qualifiers</span></span>

<span data-ttu-id="3973c-104">Квалификаторы meta уточняют определение мета-конструкций в модели CIM путем уточнения фактического использования объявления класса или свойства в синтаксисе MOF.</span><span class="sxs-lookup"><span data-stu-id="3973c-104">Meta qualifiers refine the definition of meta-constructs in the CIM model by clarifying the actual usage of a class or property declaration within the MOF syntax.</span></span>

<dt>

<span data-ttu-id="3973c-105"><span id="Association"></span><span id="association"></span><span id="ASSOCIATION"></span>**Связке**</span><span class="sxs-lookup"><span data-stu-id="3973c-105"><span id="Association"></span><span id="association"></span><span id="ASSOCIATION"></span>**Association**</span></span>
</dt> <dd>

<span data-ttu-id="3973c-106">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="3973c-106">Data type: **boolean**</span></span>

<span data-ttu-id="3973c-107">Область применения: классы</span><span class="sxs-lookup"><span data-stu-id="3973c-107">Applies to: classes</span></span>

<span data-ttu-id="3973c-108">Указывает, является ли класс классом ассоциации, используемым для описания связи между двумя другими классами.</span><span class="sxs-lookup"><span data-stu-id="3973c-108">Indicates whether the class is an association class used to describe a relationship between two other classes.</span></span> <span data-ttu-id="3973c-109">Отсутствие этого квалификатора указывает на то, что класс не является классом ассоциации.</span><span class="sxs-lookup"><span data-stu-id="3973c-109">The absence of this qualifier indicates that the class is not an association class.</span></span> <span data-ttu-id="3973c-110">Этот квалификатор является взаимоисключающим с **указанием**.</span><span class="sxs-lookup"><span data-stu-id="3973c-110">This qualifier is mutually exclusive with **Indication**.</span></span> <span data-ttu-id="3973c-111">Дополнительные сведения см. в разделе [объявление класса ассоциации](declaring-an-association-class.md).</span><span class="sxs-lookup"><span data-stu-id="3973c-111">For more information, see [Declaring an Association Class](declaring-an-association-class.md).</span></span>

</dd> <dt>

<span data-ttu-id="3973c-112"><span id="Indication"></span><span id="indication"></span><span id="INDICATION"></span>**Указание**</span><span class="sxs-lookup"><span data-stu-id="3973c-112"><span id="Indication"></span><span id="indication"></span><span id="INDICATION"></span>**Indication**</span></span>
</dt> <dd>

<span data-ttu-id="3973c-113">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="3973c-113">Data type: **boolean**</span></span>

<span data-ttu-id="3973c-114">Область применения: классы</span><span class="sxs-lookup"><span data-stu-id="3973c-114">Applies to: classes</span></span>

<span data-ttu-id="3973c-115">Указывает, определяет ли класс объекта указание.</span><span class="sxs-lookup"><span data-stu-id="3973c-115">Indicates whether the object class defines an indication.</span></span> <span data-ttu-id="3973c-116">Этот квалификатор является взаимоисключающим с **Ассоциацией**.</span><span class="sxs-lookup"><span data-stu-id="3973c-116">This qualifier is mutually exclusive with **Association**.</span></span> <span data-ttu-id="3973c-117">Значение по умолчанию — **false**.</span><span class="sxs-lookup"><span data-stu-id="3973c-117">The default is **FALSE**.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="3973c-118">Требования</span><span class="sxs-lookup"><span data-stu-id="3973c-118">Requirements</span></span>



| <span data-ttu-id="3973c-119">Требование</span><span class="sxs-lookup"><span data-stu-id="3973c-119">Requirement</span></span> | <span data-ttu-id="3973c-120">Значение</span><span class="sxs-lookup"><span data-stu-id="3973c-120">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="3973c-121">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="3973c-121">Minimum supported client</span></span><br/> | <span data-ttu-id="3973c-122">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="3973c-122">Windows Vista</span></span><br/>       |
| <span data-ttu-id="3973c-123">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="3973c-123">Minimum supported server</span></span><br/> | <span data-ttu-id="3973c-124">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="3973c-124">Windows Server 2008</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="3973c-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="3973c-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3973c-126">Квалификаторы WMI</span><span class="sxs-lookup"><span data-stu-id="3973c-126">WMI Qualifiers</span></span>](wmi-qualifiers.md)
</dt> <dt>

[<span data-ttu-id="3973c-127">Добавление квалификатора</span><span class="sxs-lookup"><span data-stu-id="3973c-127">Adding a Qualifier</span></span>](adding-a-qualifier.md)
</dt> </dl>

 

 




