---
description: '\_Класс WMI взаимосвязей Win32 системпрограмграупс связывает компьютерную систему и логическую группу программ.'
ms.assetid: cbf810c8-a967-4d60-889c-e47c43b039ea
ms.tgt_platform: multiple
title: Класс Win32_SystemProgramGroups
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_SystemProgramGroups
- Win32_SystemProgramGroups.Element
- Win32_SystemProgramGroups.Setting
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 1a8ca556c24295e2c4b04ab851610ef35ec9b715
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104142670"
---
# <a name="win32_systemprogramgroups-class"></a><span data-ttu-id="b155c-103">\_Класс Win32 системпрограмграупс</span><span class="sxs-lookup"><span data-stu-id="b155c-103">Win32\_SystemProgramGroups class</span></span>

<span data-ttu-id="b155c-104">[Класс WMI](../wmisdk/retrieving-a-class.md) взаимосвязей **Win32 \_ системпрограмграупс** связывает компьютерную систему и логическую группу программ.</span><span class="sxs-lookup"><span data-stu-id="b155c-104">The **Win32\_SystemProgramGroups** association [WMI class](../wmisdk/retrieving-a-class.md) relates a computer system and a logical program group.</span></span>

<span data-ttu-id="b155c-105">Следующий пример синтаксиса — упрощенный MOF-код, который включает все наследуемые свойства.</span><span class="sxs-lookup"><span data-stu-id="b155c-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="b155c-106">Свойства и методы имеют алфавитный порядок, а не порядок MOF.</span><span class="sxs-lookup"><span data-stu-id="b155c-106">Properties and methods are in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="b155c-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="b155c-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8502C505-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_SystemProgramGroups : Win32_SystemSetting
{
  Win32_ComputerSystem      REF Element;
  Win32_LogicalProgramGroup REF Setting;
};
```

## <a name="members"></a><span data-ttu-id="b155c-108">Члены</span><span class="sxs-lookup"><span data-stu-id="b155c-108">Members</span></span>

<span data-ttu-id="b155c-109">Класс **Win32 \_ системпрограмграупс** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="b155c-109">The **Win32\_SystemProgramGroups** class has these types of members:</span></span>

-   [<span data-ttu-id="b155c-110">Свойства</span><span class="sxs-lookup"><span data-stu-id="b155c-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="b155c-111">Свойства</span><span class="sxs-lookup"><span data-stu-id="b155c-111">Properties</span></span>

<span data-ttu-id="b155c-112">Класс **Win32 \_ системпрограмграупс** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="b155c-112">The **Win32\_SystemProgramGroups** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="b155c-113">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="b155c-113">**Element**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b155c-114">Тип данных: **Win32 \_ ComputerSystem**</span><span class="sxs-lookup"><span data-stu-id="b155c-114">Data type: **Win32\_ComputerSystem**</span></span>
</dt> <dt>

<span data-ttu-id="b155c-115">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="b155c-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b155c-116">Квалификаторы: [**override**](../wmisdk/standard-qualifiers.md) ("элемент"), [**Маппингстрингс**](../wmisdk/standard-qualifiers.md) ("WMI \| Win32 \_ ComputerSystem")</span><span class="sxs-lookup"><span data-stu-id="b155c-116">Qualifiers: [**Override**](../wmisdk/standard-qualifiers.md) ("Element"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI\|Win32\_ComputerSystem")</span></span>
</dt> </dl>

<span data-ttu-id="b155c-117">Ссылка на экземпляр, представляющий компьютерную систему, содержащую логическую группу программ.</span><span class="sxs-lookup"><span data-stu-id="b155c-117">Reference to the instance representing the computer system containing the logical program group.</span></span>

</dd> <dt>

<span data-ttu-id="b155c-118">**Параметр**</span><span class="sxs-lookup"><span data-stu-id="b155c-118">**Setting**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b155c-119">Тип данных: **Win32 \_ логикалпрограмграуп**</span><span class="sxs-lookup"><span data-stu-id="b155c-119">Data type: **Win32\_LogicalProgramGroup**</span></span>
</dt> <dt>

<span data-ttu-id="b155c-120">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="b155c-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b155c-121">Квалификаторы: [**override**](../wmisdk/standard-qualifiers.md) ("параметр"), [**Маппингстрингс**](../wmisdk/standard-qualifiers.md) ("WMI \| Win32 \_ логикалпрограмграуп")</span><span class="sxs-lookup"><span data-stu-id="b155c-121">Qualifiers: [**Override**](../wmisdk/standard-qualifiers.md) ("Setting"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI\|Win32\_LogicalProgramGroup")</span></span>
</dt> </dl>

<span data-ttu-id="b155c-122">Ссылка на экземпляр, представляющий логическую группу программ в компьютерной системе.</span><span class="sxs-lookup"><span data-stu-id="b155c-122">Reference to the instance representing the logical program group on the computer system.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="b155c-123">Комментарии</span><span class="sxs-lookup"><span data-stu-id="b155c-123">Remarks</span></span>

<span data-ttu-id="b155c-124">Класс **Win32 \_ системпрограмграупс** является производным от [**Win32 \_ системсеттинг**](win32-systemsetting.md).</span><span class="sxs-lookup"><span data-stu-id="b155c-124">The **Win32\_SystemProgramGroups** class is derived from [**Win32\_SystemSetting**](win32-systemsetting.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="b155c-125">Требования</span><span class="sxs-lookup"><span data-stu-id="b155c-125">Requirements</span></span>



| <span data-ttu-id="b155c-126">Требование</span><span class="sxs-lookup"><span data-stu-id="b155c-126">Requirement</span></span> | <span data-ttu-id="b155c-127">Значение</span><span class="sxs-lookup"><span data-stu-id="b155c-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b155c-128">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="b155c-128">Minimum supported client</span></span><br/> | <span data-ttu-id="b155c-129">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="b155c-129">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="b155c-130">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="b155c-130">Minimum supported server</span></span><br/> | <span data-ttu-id="b155c-131">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="b155c-131">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="b155c-132">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="b155c-132">Namespace</span></span><br/>                | <span data-ttu-id="b155c-133">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="b155c-133">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="b155c-134">MOF</span><span class="sxs-lookup"><span data-stu-id="b155c-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b155c-135"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="b155c-135"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="b155c-136">DLL</span><span class="sxs-lookup"><span data-stu-id="b155c-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b155c-137"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b155c-137"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b155c-138">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="b155c-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b155c-139">**\_Системсеттинг Win32**</span><span class="sxs-lookup"><span data-stu-id="b155c-139">**Win32\_SystemSetting**</span></span>](win32-systemsetting.md)
</dt> <dt>

[<span data-ttu-id="b155c-140">Классы операционной системы</span><span class="sxs-lookup"><span data-stu-id="b155c-140">Operating System Classes</span></span>](./operating-system-classes.md)
</dt> </dl>

 

 
