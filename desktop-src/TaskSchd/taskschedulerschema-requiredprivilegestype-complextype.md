---
title: Сложный тип Рекуиредпривилежестипе
description: Определяет дочерние элементы и сведения о последовательности для элемента Рекуиредпривилежес (Рекуиредпривилежестипе).
ms.assetid: ae96282a-d167-47ea-9d37-2d682f746d23
keywords:
- планировщик задач сложного типа Рекуиредпривилежестипе
topic_type:
- apiref
api_name:
- requiredPrivilegesType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 2a5ce81d96858488395e34f84232ca758ddabc59
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104493119"
---
# <a name="requiredprivilegestype-complex-type"></a><span data-ttu-id="65b2c-104">Сложный тип Рекуиредпривилежестипе</span><span class="sxs-lookup"><span data-stu-id="65b2c-104">requiredPrivilegesType Complex Type</span></span>

<span data-ttu-id="65b2c-105">Определяет дочерние элементы и сведения о последовательности для элемента [**рекуиредпривилежес (рекуиредпривилежестипе)**](taskschedulerschema-requiredprivileges-requiredprivilegestype-element.md) .</span><span class="sxs-lookup"><span data-stu-id="65b2c-105">Defines the child elements and sequencing information for the [**RequiredPrivileges (requiredPrivilegesType)**](taskschedulerschema-requiredprivileges-requiredprivilegestype-element.md) element.</span></span>

``` syntax
<xs:complexType name="requiredPrivilegesType">
    <xs:all>
        <xs:element name="Privilege"
            type="privilegeType"
            minOccurs="1"
            maxOccurs="64"
         />
    </xs:all>
</xs:complexType>
```

## <a name="child-elements"></a><span data-ttu-id="65b2c-106">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="65b2c-106">Child elements</span></span>



| <span data-ttu-id="65b2c-107">Элемент</span><span class="sxs-lookup"><span data-stu-id="65b2c-107">Element</span></span>                                                                           | <span data-ttu-id="65b2c-108">Тип</span><span class="sxs-lookup"><span data-stu-id="65b2c-108">Type</span></span>                                                                  | <span data-ttu-id="65b2c-109">Описание</span><span class="sxs-lookup"><span data-stu-id="65b2c-109">Description</span></span>                                                |
|-----------------------------------------------------------------------------------|-----------------------------------------------------------------------|------------------------------------------------------------|
| [<span data-ttu-id="65b2c-110">**Правом**</span><span class="sxs-lookup"><span data-stu-id="65b2c-110">**Privilege**</span></span>](taskschedulerschema-privilege-requiredprivilegestype-element.md) | [<span data-ttu-id="65b2c-111">**привилежетипе**</span><span class="sxs-lookup"><span data-stu-id="65b2c-111">**privilegeType**</span></span>](taskschedulerschema-privilegetype-simpletype.md) | <span data-ttu-id="65b2c-112">Указывает необходимые привилегии для задачи.</span><span class="sxs-lookup"><span data-stu-id="65b2c-112">Specifies the required privileges of the task.</span></span> <br/> |



## <a name="requirements"></a><span data-ttu-id="65b2c-113">Требования</span><span class="sxs-lookup"><span data-stu-id="65b2c-113">Requirements</span></span>



| <span data-ttu-id="65b2c-114">Требование</span><span class="sxs-lookup"><span data-stu-id="65b2c-114">Requirement</span></span> | <span data-ttu-id="65b2c-115">Значение</span><span class="sxs-lookup"><span data-stu-id="65b2c-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="65b2c-116">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="65b2c-116">Minimum supported client</span></span><br/> | <span data-ttu-id="65b2c-117">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="65b2c-117">Windows 7 \[desktop apps only\]</span></span><br/>              |
| <span data-ttu-id="65b2c-118">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="65b2c-118">Minimum supported server</span></span><br/> | <span data-ttu-id="65b2c-119">Только классические приложения Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="65b2c-119">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="65b2c-120">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="65b2c-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="65b2c-121">планировщик задач сложные типы схемы</span><span class="sxs-lookup"><span data-stu-id="65b2c-121">Task Scheduler Schema Complex Types</span></span>](task-scheduler-schema-complex-types.md)
</dt> <dt>

[<span data-ttu-id="65b2c-122">Планировщик заданий</span><span class="sxs-lookup"><span data-stu-id="65b2c-122">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





