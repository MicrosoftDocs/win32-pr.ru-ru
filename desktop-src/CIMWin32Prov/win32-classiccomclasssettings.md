---
description: '\_Класс WMI взаимосвязей Win32 классиккомкласссеттингс связывает класс модели COM и параметры, используемые для настройки экземпляров класса COM.'
ms.assetid: 50f253cc-b8ae-41ac-b01f-ea816f5ca3d4
ms.tgt_platform: multiple
title: Класс Win32_ClassicCOMClassSettings
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_ClassicCOMClassSettings
- Win32_ClassicCOMClassSettings.Setting
- Win32_ClassicCOMClassSettings.Element
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: fb9c190157742aeca7c1ba6008a784005d054ca6
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103895466"
---
# <a name="win32_classiccomclasssettings-class"></a><span data-ttu-id="e7ab4-103">\_Класс Win32 классиккомкласссеттингс</span><span class="sxs-lookup"><span data-stu-id="e7ab4-103">Win32\_ClassicCOMClassSettings class</span></span>

<span data-ttu-id="e7ab4-104">[Класс WMI](/windows/desktop/WmiSdk/retrieving-a-class) взаимосвязей **Win32 \_ КЛАССИККОМКЛАСССЕТТИНГС** связывает класс модели COM и параметры, используемые для настройки экземпляров класса COM.</span><span class="sxs-lookup"><span data-stu-id="e7ab4-104">The **Win32\_ClassicCOMClassSettings** association [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) relates a Component Object Model (COM) class and the settings used to configure instances of the COM class.</span></span>

<span data-ttu-id="e7ab4-105">Следующий пример синтаксиса — упрощенный MOF-код, который включает все наследуемые свойства.</span><span class="sxs-lookup"><span data-stu-id="e7ab4-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="e7ab4-106">Свойства перечислены в алфавитном порядке, а не в MOF.</span><span class="sxs-lookup"><span data-stu-id="e7ab4-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="e7ab4-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="e7ab4-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{E5D8A564-F6C0-11d2-B35E-00105A1F8569}"), AMENDMENT]
class Win32_ClassicCOMClassSettings : CIM_ElementSetting
{
  Win32_ClassicCOMClassSetting REF Setting;
  Win32_ClassicCOMClass        REF Element;
};
```

## <a name="members"></a><span data-ttu-id="e7ab4-108">Члены</span><span class="sxs-lookup"><span data-stu-id="e7ab4-108">Members</span></span>

<span data-ttu-id="e7ab4-109">Класс **Win32 \_ классиккомкласссеттингс** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="e7ab4-109">The **Win32\_ClassicCOMClassSettings** class has these types of members:</span></span>

-   [<span data-ttu-id="e7ab4-110">Свойства</span><span class="sxs-lookup"><span data-stu-id="e7ab4-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="e7ab4-111">Свойства</span><span class="sxs-lookup"><span data-stu-id="e7ab4-111">Properties</span></span>

<span data-ttu-id="e7ab4-112">Класс **Win32 \_ классиккомкласссеттингс** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="e7ab4-112">The **Win32\_ClassicCOMClassSettings** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="e7ab4-113">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="e7ab4-113">**Element**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e7ab4-114">Тип данных: **Win32 \_ классиккомкласс**</span><span class="sxs-lookup"><span data-stu-id="e7ab4-114">Data type: **Win32\_ClassicCOMClass**</span></span>
</dt> <dt>

<span data-ttu-id="e7ab4-115">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="e7ab4-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e7ab4-116">Квалификаторы: [**ключ**](/windows/desktop/WmiSdk/key-qualifier), [**Переопределение**](/windows/desktop/WmiSdk/standard-qualifiers) ("элемент"), [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI \| Win32 \_ классиккомкласс")</span><span class="sxs-lookup"><span data-stu-id="e7ab4-116">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Element"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI\|Win32\_ClassicCOMClass")</span></span>
</dt> </dl>

<span data-ttu-id="e7ab4-117">[**\_ Классиккомкласс Win32**](win32-classiccomclass.md) , представляющий COM-класс, к которому применяются параметры.</span><span class="sxs-lookup"><span data-stu-id="e7ab4-117">A [**Win32\_ClassicCOMClass**](win32-classiccomclass.md) that represents the COM class where the settings are applied.</span></span>

</dd> <dt>

<span data-ttu-id="e7ab4-118">**Параметр**</span><span class="sxs-lookup"><span data-stu-id="e7ab4-118">**Setting**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e7ab4-119">Тип данных: **Win32 \_ классиккомкласссеттинг**</span><span class="sxs-lookup"><span data-stu-id="e7ab4-119">Data type: **Win32\_ClassicCOMClassSetting**</span></span>
</dt> <dt>

<span data-ttu-id="e7ab4-120">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="e7ab4-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e7ab4-121">Квалификаторы: [**ключ**](/windows/desktop/WmiSdk/key-qualifier), [**Переопределение**](/windows/desktop/WmiSdk/standard-qualifiers) ("параметр"), [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI \| Win32 \_ классиккомкласссеттинг")</span><span class="sxs-lookup"><span data-stu-id="e7ab4-121">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Setting"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI\|Win32\_ClassicCOMClassSetting")</span></span>
</dt> </dl>

<span data-ttu-id="e7ab4-122">[**\_ Классиккомкласссеттинг Win32**](win32-classiccomclasssetting.md) , представляющий параметры конфигурации, связанные с COM-классом.</span><span class="sxs-lookup"><span data-stu-id="e7ab4-122">A [**Win32\_ClassicCOMClassSetting**](win32-classiccomclasssetting.md) that represents configuration settings associated with the COM class.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="e7ab4-123">Комментарии</span><span class="sxs-lookup"><span data-stu-id="e7ab4-123">Remarks</span></span>

<span data-ttu-id="e7ab4-124">Класс **Win32 \_ классиккомкласссеттингс** является производным от [**CIM \_ елементсеттинг**](cim-elementsetting.md).</span><span class="sxs-lookup"><span data-stu-id="e7ab4-124">The **Win32\_ClassicCOMClassSettings** class is derived from [**CIM\_ElementSetting**](cim-elementsetting.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="e7ab4-125">Требования</span><span class="sxs-lookup"><span data-stu-id="e7ab4-125">Requirements</span></span>



| <span data-ttu-id="e7ab4-126">Требование</span><span class="sxs-lookup"><span data-stu-id="e7ab4-126">Requirement</span></span> | <span data-ttu-id="e7ab4-127">Значение</span><span class="sxs-lookup"><span data-stu-id="e7ab4-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e7ab4-128">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="e7ab4-128">Minimum supported client</span></span><br/> | <span data-ttu-id="e7ab4-129">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="e7ab4-129">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="e7ab4-130">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="e7ab4-130">Minimum supported server</span></span><br/> | <span data-ttu-id="e7ab4-131">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="e7ab4-131">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="e7ab4-132">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="e7ab4-132">Namespace</span></span><br/>                | <span data-ttu-id="e7ab4-133">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="e7ab4-133">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="e7ab4-134">MOF</span><span class="sxs-lookup"><span data-stu-id="e7ab4-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e7ab4-135"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="e7ab4-135"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="e7ab4-136">DLL</span><span class="sxs-lookup"><span data-stu-id="e7ab4-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e7ab4-137"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e7ab4-137"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e7ab4-138">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="e7ab4-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e7ab4-139">**\_ЕЛЕМЕНТСЕТТИНГ CIM**</span><span class="sxs-lookup"><span data-stu-id="e7ab4-139">**CIM\_ElementSetting**</span></span>](cim-elementsetting.md)
</dt> <dt>

<span data-ttu-id="e7ab4-140">[Классы операционной системы](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="e7ab4-140">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> </dl>

 

