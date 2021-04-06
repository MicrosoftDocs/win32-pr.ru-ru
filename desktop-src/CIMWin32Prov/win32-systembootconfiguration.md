---
description: '\_Класс WMI взаимосвязей Win32 систембутконфигуратион связывает компьютерную систему и конфигурацию загрузки.'
ms.assetid: 1c6bce81-84d9-4949-92da-6111b4ecc939
ms.tgt_platform: multiple
title: Класс Win32_SystemBootConfiguration
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_SystemBootConfiguration
- Win32_SystemBootConfiguration.Element
- Win32_SystemBootConfiguration.Setting
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 863e4103f7e87681e25ccf53679bfe006ed3ff75
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103895934"
---
# <a name="win32_systembootconfiguration-class"></a><span data-ttu-id="5e54e-103">\_Класс Win32 систембутконфигуратион</span><span class="sxs-lookup"><span data-stu-id="5e54e-103">Win32\_SystemBootConfiguration class</span></span>

<span data-ttu-id="5e54e-104">[Класс WMI](../wmisdk/retrieving-a-class.md) взаимосвязей **Win32 \_ систембутконфигуратион** связывает компьютерную систему и конфигурацию загрузки.</span><span class="sxs-lookup"><span data-stu-id="5e54e-104">The **Win32\_SystemBootConfiguration** association [WMI class](../wmisdk/retrieving-a-class.md) relates a computer system and its boot configuration.</span></span>

<span data-ttu-id="5e54e-105">Следующий пример синтаксиса — упрощенный MOF-код, который включает все наследуемые свойства.</span><span class="sxs-lookup"><span data-stu-id="5e54e-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="5e54e-106">Свойства и методы имеют алфавитный порядок, а не порядок MOF.</span><span class="sxs-lookup"><span data-stu-id="5e54e-106">Properties and methods are in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="5e54e-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="5e54e-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8502C507-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_SystemBootConfiguration : Win32_SystemSetting
{
  Win32_ComputerSystem    REF Element;
  Win32_BootConfiguration REF Setting;
};
```

## <a name="members"></a><span data-ttu-id="5e54e-108">Члены</span><span class="sxs-lookup"><span data-stu-id="5e54e-108">Members</span></span>

<span data-ttu-id="5e54e-109">Класс **Win32 \_ систембутконфигуратион** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="5e54e-109">The **Win32\_SystemBootConfiguration** class has these types of members:</span></span>

-   [<span data-ttu-id="5e54e-110">Свойства</span><span class="sxs-lookup"><span data-stu-id="5e54e-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="5e54e-111">Свойства</span><span class="sxs-lookup"><span data-stu-id="5e54e-111">Properties</span></span>

<span data-ttu-id="5e54e-112">Класс **Win32 \_ систембутконфигуратион** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="5e54e-112">The **Win32\_SystemBootConfiguration** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="5e54e-113">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="5e54e-113">**Element**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e54e-114">Тип данных: **Win32 \_ ComputerSystem**</span><span class="sxs-lookup"><span data-stu-id="5e54e-114">Data type: **Win32\_ComputerSystem**</span></span>
</dt> <dt>

<span data-ttu-id="5e54e-115">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="5e54e-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5e54e-116">Квалификаторы: [**override**](../wmisdk/standard-qualifiers.md) ("элемент"), [**Маппингстрингс**](../wmisdk/standard-qualifiers.md) ("WMI \| Win32 \_ ComputerSystem")</span><span class="sxs-lookup"><span data-stu-id="5e54e-116">Qualifiers: [**Override**](../wmisdk/standard-qualifiers.md) ("Element"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI\|Win32\_ComputerSystem")</span></span>
</dt> </dl>

<span data-ttu-id="5e54e-117">Ссылка на экземпляр, представляющий компьютерную систему с помощью конфигурации загрузки.</span><span class="sxs-lookup"><span data-stu-id="5e54e-117">Reference to the instance representing the computer system using the boot configuration.</span></span>

</dd> <dt>

<span data-ttu-id="5e54e-118">**Параметр**</span><span class="sxs-lookup"><span data-stu-id="5e54e-118">**Setting**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e54e-119">Тип данных: **Win32 \_ бутконфигуратион**</span><span class="sxs-lookup"><span data-stu-id="5e54e-119">Data type: **Win32\_BootConfiguration**</span></span>
</dt> <dt>

<span data-ttu-id="5e54e-120">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="5e54e-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5e54e-121">Квалификаторы: [**override**](../wmisdk/standard-qualifiers.md) ("параметр"), [**Маппингстрингс**](../wmisdk/standard-qualifiers.md) ("WMI \| Win32 \_ бутконфигуратион")</span><span class="sxs-lookup"><span data-stu-id="5e54e-121">Qualifiers: [**Override**](../wmisdk/standard-qualifiers.md) ("Setting"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI\|Win32\_BootConfiguration")</span></span>
</dt> </dl>

<span data-ttu-id="5e54e-122">Ссылка на экземпляр, представляющий конфигурацию загрузки для компьютерной системы.</span><span class="sxs-lookup"><span data-stu-id="5e54e-122">Reference to the instance representing the boot configuration for the computer system.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="5e54e-123">Комментарии</span><span class="sxs-lookup"><span data-stu-id="5e54e-123">Remarks</span></span>

<span data-ttu-id="5e54e-124">Класс **Win32 \_ систембутконфигуратион** является производным от [**Win32 \_ системсеттинг**](win32-systemsetting.md).</span><span class="sxs-lookup"><span data-stu-id="5e54e-124">The **Win32\_SystemBootConfiguration** class is derived from [**Win32\_SystemSetting**](win32-systemsetting.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="5e54e-125">Требования</span><span class="sxs-lookup"><span data-stu-id="5e54e-125">Requirements</span></span>



| <span data-ttu-id="5e54e-126">Требование</span><span class="sxs-lookup"><span data-stu-id="5e54e-126">Requirement</span></span> | <span data-ttu-id="5e54e-127">Значение</span><span class="sxs-lookup"><span data-stu-id="5e54e-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="5e54e-128">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="5e54e-128">Minimum supported client</span></span><br/> | <span data-ttu-id="5e54e-129">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="5e54e-129">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="5e54e-130">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="5e54e-130">Minimum supported server</span></span><br/> | <span data-ttu-id="5e54e-131">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="5e54e-131">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="5e54e-132">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="5e54e-132">Namespace</span></span><br/>                | <span data-ttu-id="5e54e-133">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="5e54e-133">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="5e54e-134">MOF</span><span class="sxs-lookup"><span data-stu-id="5e54e-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="5e54e-135"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="5e54e-135"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="5e54e-136">DLL</span><span class="sxs-lookup"><span data-stu-id="5e54e-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5e54e-137"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5e54e-137"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5e54e-138">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="5e54e-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5e54e-139">**\_Системсеттинг Win32**</span><span class="sxs-lookup"><span data-stu-id="5e54e-139">**Win32\_SystemSetting**</span></span>](win32-systemsetting.md)
</dt> <dt>

[<span data-ttu-id="5e54e-140">Классы операционной системы</span><span class="sxs-lookup"><span data-stu-id="5e54e-140">Operating System Classes</span></span>](./operating-system-classes.md)
</dt> </dl>

 

 
