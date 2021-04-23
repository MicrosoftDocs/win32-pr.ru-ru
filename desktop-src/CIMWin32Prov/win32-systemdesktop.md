---
description: '\_Класс WMI взаимосвязей Win32 системдесктоп связывает компьютерную систему и конфигурацию рабочего стола.'
ms.assetid: 2b024660-d707-4463-8207-73df74bfa7d6
ms.tgt_platform: multiple
title: Класс Win32_SystemDesktop
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_SystemDesktop
- Win32_SystemDesktop.Element
- Win32_SystemDesktop.Setting
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 3e14cab58a445fd645b9d59c1aea713bf6c40ac0
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103990759"
---
# <a name="win32_systemdesktop-class"></a><span data-ttu-id="e0b00-103">\_Класс Win32 системдесктоп</span><span class="sxs-lookup"><span data-stu-id="e0b00-103">Win32\_SystemDesktop class</span></span>

<span data-ttu-id="e0b00-104">[Класс WMI](../wmisdk/retrieving-a-class.md) взаимосвязей **Win32 \_ системдесктоп** связывает компьютерную систему и конфигурацию рабочего стола.</span><span class="sxs-lookup"><span data-stu-id="e0b00-104">The **Win32\_SystemDesktop** association [WMI class](../wmisdk/retrieving-a-class.md) relates a computer system and its desktop configuration.</span></span>

<span data-ttu-id="e0b00-105">Следующий пример синтаксиса — упрощенный MOF-код, который включает все наследуемые свойства.</span><span class="sxs-lookup"><span data-stu-id="e0b00-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="e0b00-106">Свойства и методы имеют алфавитный порядок, а не порядок MOF.</span><span class="sxs-lookup"><span data-stu-id="e0b00-106">Properties and methods are in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="e0b00-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="e0b00-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8502C506-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_SystemDesktop : Win32_SystemSetting
{
  Win32_ComputerSystem REF Element;
  Win32_Desktop        REF Setting;
};
```

## <a name="members"></a><span data-ttu-id="e0b00-108">Члены</span><span class="sxs-lookup"><span data-stu-id="e0b00-108">Members</span></span>

<span data-ttu-id="e0b00-109">Класс **Win32 \_ системдесктоп** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="e0b00-109">The **Win32\_SystemDesktop** class has these types of members:</span></span>

-   [<span data-ttu-id="e0b00-110">Свойства</span><span class="sxs-lookup"><span data-stu-id="e0b00-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="e0b00-111">Свойства</span><span class="sxs-lookup"><span data-stu-id="e0b00-111">Properties</span></span>

<span data-ttu-id="e0b00-112">Класс **Win32 \_ системдесктоп** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="e0b00-112">The **Win32\_SystemDesktop** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="e0b00-113">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="e0b00-113">**Element**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e0b00-114">Тип данных: **Win32 \_ ComputerSystem**</span><span class="sxs-lookup"><span data-stu-id="e0b00-114">Data type: **Win32\_ComputerSystem**</span></span>
</dt> <dt>

<span data-ttu-id="e0b00-115">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="e0b00-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e0b00-116">Квалификаторы: [**override**](../wmisdk/standard-qualifiers.md) ("элемент"), [**Маппингстрингс**](../wmisdk/standard-qualifiers.md) ("WMI \| Win32 \_ ComputerSystem")</span><span class="sxs-lookup"><span data-stu-id="e0b00-116">Qualifiers: [**Override**](../wmisdk/standard-qualifiers.md) ("Element"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI\|Win32\_ComputerSystem")</span></span>
</dt> </dl>

<span data-ttu-id="e0b00-117">Ссылка на экземпляр, представляющий компьютерную систему, в которой существует конфигурация рабочего стола.</span><span class="sxs-lookup"><span data-stu-id="e0b00-117">Reference to the instance representing the computer system where the desktop configuration exists.</span></span>

</dd> <dt>

<span data-ttu-id="e0b00-118">**Параметр**</span><span class="sxs-lookup"><span data-stu-id="e0b00-118">**Setting**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e0b00-119">Тип данных: **\_ классическую панель Win32**</span><span class="sxs-lookup"><span data-stu-id="e0b00-119">Data type: **Win32\_Desktop**</span></span>
</dt> <dt>

<span data-ttu-id="e0b00-120">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="e0b00-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e0b00-121">Квалификаторы: [**override**](../wmisdk/standard-qualifiers.md) ("параметр"), [**Маппингстрингс**](../wmisdk/standard-qualifiers.md) ("Инструментарий WMI \| Win32 \_ Desktop")</span><span class="sxs-lookup"><span data-stu-id="e0b00-121">Qualifiers: [**Override**](../wmisdk/standard-qualifiers.md) ("Setting"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI\|Win32\_Desktop")</span></span>
</dt> </dl>

<span data-ttu-id="e0b00-122">Ссылка на экземпляр, представляющий конфигурацию, существующую в компьютерной системе.</span><span class="sxs-lookup"><span data-stu-id="e0b00-122">Reference to the instance representing the configuration existing on the computer system.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="e0b00-123">Комментарии</span><span class="sxs-lookup"><span data-stu-id="e0b00-123">Remarks</span></span>

<span data-ttu-id="e0b00-124">Класс **Win32 \_ системдесктоп** является производным от [**Win32 \_ системсеттинг**](win32-systemsetting.md).</span><span class="sxs-lookup"><span data-stu-id="e0b00-124">The **Win32\_SystemDesktop** class is derived from [**Win32\_SystemSetting**](win32-systemsetting.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="e0b00-125">Требования</span><span class="sxs-lookup"><span data-stu-id="e0b00-125">Requirements</span></span>



| <span data-ttu-id="e0b00-126">Требование</span><span class="sxs-lookup"><span data-stu-id="e0b00-126">Requirement</span></span> | <span data-ttu-id="e0b00-127">Значение</span><span class="sxs-lookup"><span data-stu-id="e0b00-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e0b00-128">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="e0b00-128">Minimum supported client</span></span><br/> | <span data-ttu-id="e0b00-129">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="e0b00-129">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="e0b00-130">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="e0b00-130">Minimum supported server</span></span><br/> | <span data-ttu-id="e0b00-131">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="e0b00-131">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="e0b00-132">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="e0b00-132">Namespace</span></span><br/>                | <span data-ttu-id="e0b00-133">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="e0b00-133">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="e0b00-134">MOF</span><span class="sxs-lookup"><span data-stu-id="e0b00-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e0b00-135"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="e0b00-135"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="e0b00-136">DLL</span><span class="sxs-lookup"><span data-stu-id="e0b00-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e0b00-137"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e0b00-137"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e0b00-138">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="e0b00-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e0b00-139">**\_Системсеттинг Win32**</span><span class="sxs-lookup"><span data-stu-id="e0b00-139">**Win32\_SystemSetting**</span></span>](win32-systemsetting.md)
</dt> <dt>

[<span data-ttu-id="e0b00-140">Классы операционной системы</span><span class="sxs-lookup"><span data-stu-id="e0b00-140">Operating System Classes</span></span>](./operating-system-classes.md)
</dt> </dl>

 

 
