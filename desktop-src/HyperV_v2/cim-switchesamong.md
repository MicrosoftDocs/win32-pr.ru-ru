---
description: Представляет службу коммутатора, которая переключает кадры между портами коммутатора.
ms.assetid: ee2d4831-df00-408c-b350-26d2d1d3e8aa
title: Класс CIM_SwitchesAmong
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_SwitchesAmong
- CIM_SwitchesAmong.Antecedent
- CIM_SwitchesAmong.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 16a87797b4a138ef79be3d5ea8c6304d2ce4a942
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104154535"
---
# <a name="cim_switchesamong-class"></a><span data-ttu-id="c4b7e-103">\_Класс CIM свитчесамонг</span><span class="sxs-lookup"><span data-stu-id="c4b7e-103">CIM\_SwitchesAmong class</span></span>

<span data-ttu-id="c4b7e-104">Представляет службу коммутатора, которая переключает кадры между портами коммутатора.</span><span class="sxs-lookup"><span data-stu-id="c4b7e-104">Represents a switch service, which switches frames between switch ports.</span></span>

## <a name="syntax"></a><span data-ttu-id="c4b7e-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="c4b7e-105">Syntax</span></span>

``` syntax
[Association, Abstract, Version("2.6.0"), UMLPackagePath("CIM::Network::SwitchingBridging")]
class CIM_SwitchesAmong : CIM_ForwardsAmong
{
  CIM_SwitchPort    REF Antecedent;
  CIM_SwitchService REF Dependent;
};
```

## <a name="members"></a><span data-ttu-id="c4b7e-106">Члены</span><span class="sxs-lookup"><span data-stu-id="c4b7e-106">Members</span></span>

<span data-ttu-id="c4b7e-107">Класс **CIM \_ свитчесамонг** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="c4b7e-107">The **CIM\_SwitchesAmong** class has these types of members:</span></span>

-   [<span data-ttu-id="c4b7e-108">Свойства</span><span class="sxs-lookup"><span data-stu-id="c4b7e-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="c4b7e-109">Свойства</span><span class="sxs-lookup"><span data-stu-id="c4b7e-109">Properties</span></span>

<span data-ttu-id="c4b7e-110">Класс **CIM \_ свитчесамонг** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="c4b7e-110">The **CIM\_SwitchesAmong** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="c4b7e-111">**Завершил**</span><span class="sxs-lookup"><span data-stu-id="c4b7e-111">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c4b7e-112">Тип данных: **CIM \_ свитчпорт**</span><span class="sxs-lookup"><span data-stu-id="c4b7e-112">Data type: **CIM\_SwitchPort**</span></span>
</dt> <dt>

<span data-ttu-id="c4b7e-113">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c4b7e-113">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c4b7e-114">Квалификаторы: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span><span class="sxs-lookup"><span data-stu-id="c4b7e-114">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="c4b7e-115">Ссылка [**на \_ свитчпорт CIM**](cim-switchport.md) для порта коммутатора.</span><span class="sxs-lookup"><span data-stu-id="c4b7e-115">A [**CIM\_SwitchPort**](cim-switchport.md) reference to the switch port.</span></span>

</dd> <dt>

<span data-ttu-id="c4b7e-116">**Него**</span><span class="sxs-lookup"><span data-stu-id="c4b7e-116">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c4b7e-117">Тип данных: **CIM \_ свитчсервице**</span><span class="sxs-lookup"><span data-stu-id="c4b7e-117">Data type: **CIM\_SwitchService**</span></span>
</dt> <dt>

<span data-ttu-id="c4b7e-118">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c4b7e-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c4b7e-119">Квалификаторы: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("зависимый"), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span><span class="sxs-lookup"><span data-stu-id="c4b7e-119">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent"), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span></span>
</dt> </dl>

<span data-ttu-id="c4b7e-120">Ссылка [**CIM \_ свитчсервице**](cim-switchservice.md) на службу коммутации.</span><span class="sxs-lookup"><span data-stu-id="c4b7e-120">A [**CIM\_SwitchService**](cim-switchservice.md) reference to the switching service.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="c4b7e-121">Требования</span><span class="sxs-lookup"><span data-stu-id="c4b7e-121">Requirements</span></span>



| <span data-ttu-id="c4b7e-122">Требование</span><span class="sxs-lookup"><span data-stu-id="c4b7e-122">Requirement</span></span> | <span data-ttu-id="c4b7e-123">Значение</span><span class="sxs-lookup"><span data-stu-id="c4b7e-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c4b7e-124">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="c4b7e-124">Minimum supported client</span></span><br/> | <span data-ttu-id="c4b7e-125">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="c4b7e-125">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="c4b7e-126">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="c4b7e-126">Minimum supported server</span></span><br/> | <span data-ttu-id="c4b7e-127">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="c4b7e-127">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="c4b7e-128">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="c4b7e-128">Namespace</span></span><br/>                | <span data-ttu-id="c4b7e-129">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="c4b7e-129">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="c4b7e-130">MOF</span><span class="sxs-lookup"><span data-stu-id="c4b7e-130">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c4b7e-131"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="c4b7e-131"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="c4b7e-132">DLL</span><span class="sxs-lookup"><span data-stu-id="c4b7e-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c4b7e-133"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="c4b7e-133"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="c4b7e-134">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="c4b7e-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c4b7e-135">**\_ФОРВАРДСАМОНГ CIM**</span><span class="sxs-lookup"><span data-stu-id="c4b7e-135">**CIM\_ForwardsAmong**</span></span>](cim-forwardsamong.md)
</dt> </dl>

 

