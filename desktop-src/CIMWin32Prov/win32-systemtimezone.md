---
description: '\_Класс WMI взаимосвязей Win32 системтимезоне связывает компьютерную систему и часовой пояс.'
ms.assetid: 53c74a61-c91d-4daa-933e-4cc7b9583d98
ms.tgt_platform: multiple
title: Класс Win32_SystemTimeZone
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_SystemTimeZone
- Win32_SystemTimeZone.Element
- Win32_SystemTimeZone.Setting
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 9ec294600fdc81f085bf29f5e664bcbec961417c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103895925"
---
# <a name="win32_systemtimezone-class"></a><span data-ttu-id="a862a-103">\_Класс Win32 системтимезоне</span><span class="sxs-lookup"><span data-stu-id="a862a-103">Win32\_SystemTimeZone class</span></span>

<span data-ttu-id="a862a-104">[Класс WMI](../wmisdk/retrieving-a-class.md) взаимосвязей **Win32 \_ системтимезоне** связывает компьютерную систему и часовой пояс.</span><span class="sxs-lookup"><span data-stu-id="a862a-104">The **Win32\_SystemTimeZone** association [WMI class](../wmisdk/retrieving-a-class.md) relates a computer system and a time zone.</span></span>

<span data-ttu-id="a862a-105">Следующий пример синтаксиса — упрощенный MOF-код, который включает все наследуемые свойства.</span><span class="sxs-lookup"><span data-stu-id="a862a-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="a862a-106">Свойства и методы имеют алфавитный порядок, а не порядок MOF.</span><span class="sxs-lookup"><span data-stu-id="a862a-106">Properties and methods are in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="a862a-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="a862a-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8502C504-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_SystemTimeZone : Win32_SystemSetting
{
  Win32_ComputerSystem REF Element;
  Win32_TimeZone       REF Setting;
};
```

## <a name="members"></a><span data-ttu-id="a862a-108">Члены</span><span class="sxs-lookup"><span data-stu-id="a862a-108">Members</span></span>

<span data-ttu-id="a862a-109">Класс **Win32 \_ системтимезоне** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="a862a-109">The **Win32\_SystemTimeZone** class has these types of members:</span></span>

-   [<span data-ttu-id="a862a-110">Свойства</span><span class="sxs-lookup"><span data-stu-id="a862a-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="a862a-111">Свойства</span><span class="sxs-lookup"><span data-stu-id="a862a-111">Properties</span></span>

<span data-ttu-id="a862a-112">Класс **Win32 \_ системтимезоне** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="a862a-112">The **Win32\_SystemTimeZone** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="a862a-113">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="a862a-113">**Element**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a862a-114">Тип данных: **Win32 \_ ComputerSystem**</span><span class="sxs-lookup"><span data-stu-id="a862a-114">Data type: **Win32\_ComputerSystem**</span></span>
</dt> <dt>

<span data-ttu-id="a862a-115">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="a862a-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a862a-116">Квалификаторы: [**override**](../wmisdk/standard-qualifiers.md) ("элемент"), [**Маппингстрингс**](../wmisdk/standard-qualifiers.md) ("WMI \| Win32 \_ ComputerSystem")</span><span class="sxs-lookup"><span data-stu-id="a862a-116">Qualifiers: [**Override**](../wmisdk/standard-qualifiers.md) ("Element"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI\|Win32\_ComputerSystem")</span></span>
</dt> </dl>

<span data-ttu-id="a862a-117">Ссылка на экземпляр, представляющий компьютерную систему, отслеживающую часовой пояс системы.</span><span class="sxs-lookup"><span data-stu-id="a862a-117">Reference to the instance representing the computer system keeping track of the system time zone.</span></span>

</dd> <dt>

<span data-ttu-id="a862a-118">**Параметр**</span><span class="sxs-lookup"><span data-stu-id="a862a-118">**Setting**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a862a-119">Тип данных: **\_ Часовой пояс Win32**</span><span class="sxs-lookup"><span data-stu-id="a862a-119">Data type: **Win32\_TimeZone**</span></span>
</dt> <dt>

<span data-ttu-id="a862a-120">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="a862a-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a862a-121">Квалификаторы: [**override**](../wmisdk/standard-qualifiers.md) ("параметр"), [**Маппингстрингс**](../wmisdk/standard-qualifiers.md) ("WMI \| Win32 \_ TimeZone")</span><span class="sxs-lookup"><span data-stu-id="a862a-121">Qualifiers: [**Override**](../wmisdk/standard-qualifiers.md) ("Setting"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI\|Win32\_TimeZone")</span></span>
</dt> </dl>

<span data-ttu-id="a862a-122">Ссылка на экземпляр, представляющий свойства часового пояса, которые отписываются в системе компьютера.</span><span class="sxs-lookup"><span data-stu-id="a862a-122">Reference to the instance representing the time zone properties tracked by the computer system.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="a862a-123">Комментарии</span><span class="sxs-lookup"><span data-stu-id="a862a-123">Remarks</span></span>

<span data-ttu-id="a862a-124">Класс **Win32 \_ системтимезоне** является производным от [**Win32 \_ системсеттинг**](win32-systemsetting.md).</span><span class="sxs-lookup"><span data-stu-id="a862a-124">The **Win32\_SystemTimeZone** class is derived from [**Win32\_SystemSetting**](win32-systemsetting.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="a862a-125">Требования</span><span class="sxs-lookup"><span data-stu-id="a862a-125">Requirements</span></span>



| <span data-ttu-id="a862a-126">Требование</span><span class="sxs-lookup"><span data-stu-id="a862a-126">Requirement</span></span> | <span data-ttu-id="a862a-127">Значение</span><span class="sxs-lookup"><span data-stu-id="a862a-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a862a-128">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="a862a-128">Minimum supported client</span></span><br/> | <span data-ttu-id="a862a-129">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="a862a-129">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="a862a-130">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="a862a-130">Minimum supported server</span></span><br/> | <span data-ttu-id="a862a-131">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="a862a-131">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="a862a-132">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="a862a-132">Namespace</span></span><br/>                | <span data-ttu-id="a862a-133">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="a862a-133">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="a862a-134">MOF</span><span class="sxs-lookup"><span data-stu-id="a862a-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="a862a-135"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="a862a-135"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="a862a-136">DLL</span><span class="sxs-lookup"><span data-stu-id="a862a-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a862a-137"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a862a-137"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a862a-138">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="a862a-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a862a-139">**\_Системсеттинг Win32**</span><span class="sxs-lookup"><span data-stu-id="a862a-139">**Win32\_SystemSetting**</span></span>](win32-systemsetting.md)
</dt> <dt>

[<span data-ttu-id="a862a-140">Классы операционной системы</span><span class="sxs-lookup"><span data-stu-id="a862a-140">Operating System Classes</span></span>](./operating-system-classes.md)
</dt> </dl>

 

 
