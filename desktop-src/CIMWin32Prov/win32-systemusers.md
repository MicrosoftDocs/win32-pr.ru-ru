---
description: '\_Класс WMI взаимосвязей Win32 SystemUsers связывает компьютерную систему и учетную запись пользователя в этой системе.'
ms.assetid: 0f6cba69-86f7-4795-a47d-6fb8ed0a00b8
ms.tgt_platform: multiple
title: Класс Win32_SystemUsers
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_SystemUsers
- Win32_SystemUsers.GroupComponent
- Win32_SystemUsers.PartComponent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: a2239983d5b9c080c60d301a557b5487f8cf7fcf
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103990757"
---
# <a name="win32_systemusers-class"></a><span data-ttu-id="9675d-103">\_Класс Win32 SystemUsers</span><span class="sxs-lookup"><span data-stu-id="9675d-103">Win32\_SystemUsers class</span></span>

<span data-ttu-id="9675d-104">[Класс WMI](../wmisdk/retrieving-a-class.md) взаимосвязей **Win32 \_ SystemUsers** связывает компьютерную систему и учетную запись пользователя в этой системе.</span><span class="sxs-lookup"><span data-stu-id="9675d-104">The **Win32\_SystemUsers** association [WMI class](../wmisdk/retrieving-a-class.md) relates a computer system and a user account on that system.</span></span>

<span data-ttu-id="9675d-105">Следующий пример синтаксиса — упрощенный MOF-код, который включает все наследуемые свойства.</span><span class="sxs-lookup"><span data-stu-id="9675d-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="9675d-106">Свойства и методы имеют алфавитный порядок, а не порядок MOF.</span><span class="sxs-lookup"><span data-stu-id="9675d-106">Properties and methods are in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="9675d-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="9675d-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8502C4F2-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_SystemUsers : CIM_SystemComponent
{
  Win32_ComputerSystem REF GroupComponent;
  Win32_UserAccount    REF PartComponent;
};
```

## <a name="members"></a><span data-ttu-id="9675d-108">Члены</span><span class="sxs-lookup"><span data-stu-id="9675d-108">Members</span></span>

<span data-ttu-id="9675d-109">Класс **Win32 \_ SystemUsers** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="9675d-109">The **Win32\_SystemUsers** class has these types of members:</span></span>

-   [<span data-ttu-id="9675d-110">Свойства</span><span class="sxs-lookup"><span data-stu-id="9675d-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="9675d-111">Свойства</span><span class="sxs-lookup"><span data-stu-id="9675d-111">Properties</span></span>

<span data-ttu-id="9675d-112">Класс **Win32 \_ SystemUsers** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="9675d-112">The **Win32\_SystemUsers** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="9675d-113">**Ссылка**</span><span class="sxs-lookup"><span data-stu-id="9675d-113">**GroupComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9675d-114">Тип данных: **Win32 \_ ComputerSystem**</span><span class="sxs-lookup"><span data-stu-id="9675d-114">Data type: **Win32\_ComputerSystem**</span></span>
</dt> <dt>

<span data-ttu-id="9675d-115">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="9675d-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9675d-116">Квалификаторы: [**ключ**](../wmisdk/key-qualifier.md), [**Переопределение**](../wmisdk/standard-qualifiers.md) ("GroupComponent"), [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("WMI \| Win32 \_ ComputerSystem")</span><span class="sxs-lookup"><span data-stu-id="9675d-116">Qualifiers: [**key**](../wmisdk/key-qualifier.md), [**Override**](../wmisdk/standard-qualifiers.md) ("GroupComponent"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI\|Win32\_ComputerSystem")</span></span>
</dt> </dl>

<span data-ttu-id="9675d-117">Ссылка на экземпляр, представляющий компьютерную систему, содержащую учетную запись пользователя.</span><span class="sxs-lookup"><span data-stu-id="9675d-117">Reference to the instance representing the computer system containing the user account.</span></span>

</dd> <dt>

<span data-ttu-id="9675d-118">**PartComponent**</span><span class="sxs-lookup"><span data-stu-id="9675d-118">**PartComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9675d-119">Тип данных: **Win32 \_ UserAccount**</span><span class="sxs-lookup"><span data-stu-id="9675d-119">Data type: **Win32\_UserAccount**</span></span>
</dt> <dt>

<span data-ttu-id="9675d-120">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="9675d-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9675d-121">Квалификаторы: [**ключ**](../wmisdk/key-qualifier.md), [**Переопределение**](../wmisdk/standard-qualifiers.md) ("PartComponent"), [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("WMI \| Win32 \_ UserAccount")</span><span class="sxs-lookup"><span data-stu-id="9675d-121">Qualifiers: [**key**](../wmisdk/key-qualifier.md), [**Override**](../wmisdk/standard-qualifiers.md) ("PartComponent"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI\|Win32\_UserAccount")</span></span>
</dt> </dl>

<span data-ttu-id="9675d-122">Ссылка на экземпляр, представляющий учетную запись пользователя в системе компьютера.</span><span class="sxs-lookup"><span data-stu-id="9675d-122">Reference to the instance representing the user account on the computer system.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="9675d-123">Комментарии</span><span class="sxs-lookup"><span data-stu-id="9675d-123">Remarks</span></span>

<span data-ttu-id="9675d-124">Класс **Win32 \_ SystemUsers** является производным от [**CIM \_ системкомпонент**](cim-systemcomponent.md).</span><span class="sxs-lookup"><span data-stu-id="9675d-124">The **Win32\_SystemUsers** class is derived from [**CIM\_SystemComponent**](cim-systemcomponent.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="9675d-125">Требования</span><span class="sxs-lookup"><span data-stu-id="9675d-125">Requirements</span></span>



| <span data-ttu-id="9675d-126">Требование</span><span class="sxs-lookup"><span data-stu-id="9675d-126">Requirement</span></span> | <span data-ttu-id="9675d-127">Значение</span><span class="sxs-lookup"><span data-stu-id="9675d-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="9675d-128">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="9675d-128">Minimum supported client</span></span><br/> | <span data-ttu-id="9675d-129">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="9675d-129">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="9675d-130">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="9675d-130">Minimum supported server</span></span><br/> | <span data-ttu-id="9675d-131">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="9675d-131">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="9675d-132">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="9675d-132">Namespace</span></span><br/>                | <span data-ttu-id="9675d-133">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="9675d-133">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="9675d-134">MOF</span><span class="sxs-lookup"><span data-stu-id="9675d-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="9675d-135"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="9675d-135"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="9675d-136">DLL</span><span class="sxs-lookup"><span data-stu-id="9675d-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9675d-137"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9675d-137"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9675d-138">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="9675d-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9675d-139">**\_СИСТЕМКОМПОНЕНТ CIM**</span><span class="sxs-lookup"><span data-stu-id="9675d-139">**CIM\_SystemComponent**</span></span>](cim-systemcomponent.md)
</dt> <dt>

[<span data-ttu-id="9675d-140">Классы операционной системы</span><span class="sxs-lookup"><span data-stu-id="9675d-140">Operating System Classes</span></span>](./operating-system-classes.md)
</dt> </dl>

 

 
