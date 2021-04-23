---
description: В следующем списке перечислены возможные значения поля flags в записи управления доступом WMI (ACE).
ms.assetid: bd09691d-e285-40e0-8686-edd5a132a06e
ms.tgt_platform: multiple
title: Константы флагов пространства имен ACE (Winnt. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- OBJECT_INHERIT_ACE
- CONTAINER_INHERIT_ACE
- NO_PROPAGATE_INHERIT_ACE
- INHERIT_ONLY_ACE
- INHERITED_ACE
api_type:
- HeaderDef
api_location:
- Winnt.h
ms.openlocfilehash: 053d4166882b6254dec313cb10fbf10588ba0071
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105649000"
---
# <a name="namespace-ace-flag-constants"></a><span data-ttu-id="051ef-103">Константы флагов пространства имен ACE</span><span class="sxs-lookup"><span data-stu-id="051ef-103">Namespace ACE Flag Constants</span></span>

<span data-ttu-id="051ef-104">В следующем списке перечислены возможные значения поля **flags** в записи управления доступом WMI (ACE).</span><span class="sxs-lookup"><span data-stu-id="051ef-104">The following list lists the possible values of the **Flags** field in a WMI Access Control Entry (ACE).</span></span>

<dl> <dt>

<span data-ttu-id="051ef-105"><span id="OBJECT_INHERIT_ACE"></span><span id="object_inherit_ace"></span>**Объект \_ наследует \_ ACE**</span><span class="sxs-lookup"><span data-stu-id="051ef-105"><span id="OBJECT_INHERIT_ACE"></span><span id="object_inherit_ace"></span>**OBJECT\_INHERIT\_ACE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="051ef-106">1 (0x1)</span><span class="sxs-lookup"><span data-stu-id="051ef-106">1 (0x1)</span></span>
</dt> <dt>



<span data-ttu-id="051ef-107">Дочерние объекты, не являющиеся контейнерами, наследуют ACE как эффективный элемент ACE.</span><span class="sxs-lookup"><span data-stu-id="051ef-107">Non-container child objects inherit the ACE as an effective ACE.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="051ef-108"><span id="CONTAINER_INHERIT_ACE"></span><span id="container_inherit_ace"></span>**КОНТЕЙНЕР \_ наследует \_ ACE**</span><span class="sxs-lookup"><span data-stu-id="051ef-108"><span id="CONTAINER_INHERIT_ACE"></span><span id="container_inherit_ace"></span>**CONTAINER\_INHERIT\_ACE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="051ef-109">2 (0x2)</span><span class="sxs-lookup"><span data-stu-id="051ef-109">2 (0x2)</span></span>
</dt> <dt>



<span data-ttu-id="051ef-110">ACE влияет на дочерние пространства имен, а также на текущее пространство имен.</span><span class="sxs-lookup"><span data-stu-id="051ef-110">The ACE has an effect on child namespaces as well as the current namespace.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="051ef-111"><span id="NO_PROPAGATE_INHERIT_ACE"></span><span id="no_propagate_inherit_ace"></span>**НЕТ \_ распространения \_ наследования \_ ACE**</span><span class="sxs-lookup"><span data-stu-id="051ef-111"><span id="NO_PROPAGATE_INHERIT_ACE"></span><span id="no_propagate_inherit_ace"></span>**NO\_PROPAGATE\_INHERIT\_ACE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="051ef-112">4 (0x4)</span><span class="sxs-lookup"><span data-stu-id="051ef-112">4 (0x4)</span></span>
</dt> <dt>



<span data-ttu-id="051ef-113">ACE применяется только к текущему пространству имен и непосредственным дочерним элементам.</span><span class="sxs-lookup"><span data-stu-id="051ef-113">The ACE applies only to the current namespace and immediate children .</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="051ef-114"><span id="INHERIT_ONLY_ACE"></span><span id="inherit_only_ace"></span>**наследовать \_ только \_ ACE**</span><span class="sxs-lookup"><span data-stu-id="051ef-114"><span id="INHERIT_ONLY_ACE"></span><span id="inherit_only_ace"></span>**INHERIT\_ONLY\_ACE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="051ef-115">8 (0x8)</span><span class="sxs-lookup"><span data-stu-id="051ef-115">8 (0x8)</span></span>
</dt> <dt>



<span data-ttu-id="051ef-116">ACE применяется только к дочерним пространствам имен.</span><span class="sxs-lookup"><span data-stu-id="051ef-116">The ACE applies only to child namespaces.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="051ef-117"><span id="INHERITED_ACE"></span><span id="inherited_ace"></span>**УНАСЛЕДОВАНный \_ элемент ACE**</span><span class="sxs-lookup"><span data-stu-id="051ef-117"><span id="INHERITED_ACE"></span><span id="inherited_ace"></span>**INHERITED\_ACE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="051ef-118">16 (0x10)</span><span class="sxs-lookup"><span data-stu-id="051ef-118">16 (0x10)</span></span>
</dt> <dt>



<span data-ttu-id="051ef-119">Это значение не задается клиентами, но сообщается клиентам, если источником ACE является родительское пространство имен.</span><span class="sxs-lookup"><span data-stu-id="051ef-119">This is not set by clients, but is reported to clients when the source of an ACE is a parent namespace.</span></span>


</dt> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="051ef-120">Требования</span><span class="sxs-lookup"><span data-stu-id="051ef-120">Requirements</span></span>



| <span data-ttu-id="051ef-121">Требование</span><span class="sxs-lookup"><span data-stu-id="051ef-121">Requirement</span></span> | <span data-ttu-id="051ef-122">Значение</span><span class="sxs-lookup"><span data-stu-id="051ef-122">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="051ef-123">Header</span><span class="sxs-lookup"><span data-stu-id="051ef-123">Header</span></span><br/> | <dl> <span data-ttu-id="051ef-124"><dt>Файл Winnt. h</dt></span><span class="sxs-lookup"><span data-stu-id="051ef-124"><dt>Winnt.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="051ef-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="051ef-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="051ef-126">Константы безопасности WMI</span><span class="sxs-lookup"><span data-stu-id="051ef-126">WMI Security Constants</span></span>](wmi-security-constants.md)
</dt> <dt>

[<span data-ttu-id="051ef-127">Настройка дескрипторов безопасности Намепаце</span><span class="sxs-lookup"><span data-stu-id="051ef-127">Setting Namepace Security Descriptors</span></span>](setting-namespace-security-descriptors.md)
</dt> <dt>

[<span data-ttu-id="051ef-128">Установка наследования безопасности пространства имен</span><span class="sxs-lookup"><span data-stu-id="051ef-128">Establishing Inheritance of Namespace Security</span></span>](establishing-inheritance-of-namespace-security.md)
</dt> <dt>

[<span data-ttu-id="051ef-129">**\_\_системсекурити**</span><span class="sxs-lookup"><span data-stu-id="051ef-129">**\_\_SystemSecurity**</span></span>](--systemsecurity.md)
</dt> </dl>

 

 




