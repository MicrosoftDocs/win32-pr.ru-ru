---
description: Представляет связь между компьютерной системой и ее последним примененным моментальным снимком виртуальной системы.
ms.assetid: 722491a3-1c46-4d37-8bd6-7c7d6648a806
title: Класс CIM_LastAppliedSnapshot
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_LastAppliedSnapshot
- CIM_LastAppliedSnapshot.Antecedent
- CIM_LastAppliedSnapshot.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 38efa9c5f02cd0ea40d993cc39ba05ac0b6fde3b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105684708"
---
# <a name="cim_lastappliedsnapshot-class"></a><span data-ttu-id="24dd8-103">\_Класс CIM ластапплиедснапшот</span><span class="sxs-lookup"><span data-stu-id="24dd8-103">CIM\_LastAppliedSnapshot class</span></span>

<span data-ttu-id="24dd8-104">Представляет связь между компьютерной системой и ее последним примененным моментальным снимком виртуальной системы.</span><span class="sxs-lookup"><span data-stu-id="24dd8-104">Represents an association between a computer system and its most recently applied virtual system snapshot.</span></span>

## <a name="syntax"></a><span data-ttu-id="24dd8-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="24dd8-105">Syntax</span></span>

``` syntax
[Association, Abstract, Version("2.22.0"), AMENDMENT]
class CIM_LastAppliedSnapshot : CIM_Dependency
{
  CIM_VirtualSystemSettingData REF Antecedent;
  CIM_ComputerSystem           REF Dependent;
};
```

## <a name="members"></a><span data-ttu-id="24dd8-106">Члены</span><span class="sxs-lookup"><span data-stu-id="24dd8-106">Members</span></span>

<span data-ttu-id="24dd8-107">Класс **CIM \_ ластапплиедснапшот** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="24dd8-107">The **CIM\_LastAppliedSnapshot** class has these types of members:</span></span>

-   [<span data-ttu-id="24dd8-108">Свойства</span><span class="sxs-lookup"><span data-stu-id="24dd8-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="24dd8-109">Свойства</span><span class="sxs-lookup"><span data-stu-id="24dd8-109">Properties</span></span>

<span data-ttu-id="24dd8-110">Класс **CIM \_ ластапплиедснапшот** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="24dd8-110">The **CIM\_LastAppliedSnapshot** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="24dd8-111">**Завершил**</span><span class="sxs-lookup"><span data-stu-id="24dd8-111">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="24dd8-112">Тип данных: **CIM \_ виртуалсистемсеттингдата**</span><span class="sxs-lookup"><span data-stu-id="24dd8-112">Data type: **CIM\_VirtualSystemSettingData**</span></span>
</dt> <dt>

<span data-ttu-id="24dd8-113">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="24dd8-113">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="24dd8-114">Квалификаторы: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent"), [**min**](/windows/desktop/WmiSdk/standard-qualifiers) (0), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span><span class="sxs-lookup"><span data-stu-id="24dd8-114">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent"), [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (0), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span></span>
</dt> </dl>

<span data-ttu-id="24dd8-115">Моментальный снимок виртуальной системы, который последний раз был применен к компьютерной системе.</span><span class="sxs-lookup"><span data-stu-id="24dd8-115">The virtual system snapshot that was last applied to the computer system.</span></span>

</dd> <dt>

<span data-ttu-id="24dd8-116">**Него**</span><span class="sxs-lookup"><span data-stu-id="24dd8-116">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="24dd8-117">Тип данных: **CIM \_ ComputerSystem**</span><span class="sxs-lookup"><span data-stu-id="24dd8-117">Data type: **CIM\_ComputerSystem**</span></span>
</dt> <dt>

<span data-ttu-id="24dd8-118">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="24dd8-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="24dd8-119">Квалификаторы: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("зависимый"), [**min**](/windows/desktop/WmiSdk/standard-qualifiers) (0), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span><span class="sxs-lookup"><span data-stu-id="24dd8-119">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent"), [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (0), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span></span>
</dt> </dl>

<span data-ttu-id="24dd8-120">Компьютерная система.</span><span class="sxs-lookup"><span data-stu-id="24dd8-120">The computer system.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="24dd8-121">Требования</span><span class="sxs-lookup"><span data-stu-id="24dd8-121">Requirements</span></span>



| <span data-ttu-id="24dd8-122">Требование</span><span class="sxs-lookup"><span data-stu-id="24dd8-122">Requirement</span></span> | <span data-ttu-id="24dd8-123">Значение</span><span class="sxs-lookup"><span data-stu-id="24dd8-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="24dd8-124">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="24dd8-124">Minimum supported client</span></span><br/> | <span data-ttu-id="24dd8-125">Windows 8</span><span class="sxs-lookup"><span data-stu-id="24dd8-125">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="24dd8-126">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="24dd8-126">Minimum supported server</span></span><br/> | <span data-ttu-id="24dd8-127">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="24dd8-127">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="24dd8-128">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="24dd8-128">Namespace</span></span><br/>                | <span data-ttu-id="24dd8-129">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="24dd8-129">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="24dd8-130">MOF</span><span class="sxs-lookup"><span data-stu-id="24dd8-130">MOF</span></span><br/>                      | <dl> <span data-ttu-id="24dd8-131"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="24dd8-131"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="24dd8-132">DLL</span><span class="sxs-lookup"><span data-stu-id="24dd8-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="24dd8-133"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="24dd8-133"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="24dd8-134">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="24dd8-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="24dd8-135">**\_Зависимость CIM**</span><span class="sxs-lookup"><span data-stu-id="24dd8-135">**CIM\_Dependency**</span></span>](cim-dependency.md)
</dt> </dl>

 

