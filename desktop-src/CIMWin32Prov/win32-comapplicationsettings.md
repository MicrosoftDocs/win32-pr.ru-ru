---
description: '\_Класс WMI взаимосвязей Win32 комаппликатионсеттингс связывает приложение DCOM и его параметры конфигурации.'
ms.assetid: b08eaff1-b42a-42f3-abf7-3664b6195acd
ms.tgt_platform: multiple
title: Класс Win32_COMApplicationSettings
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_COMApplicationSettings
- Win32_COMApplicationSettings.Setting
- Win32_COMApplicationSettings.Element
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 8f2fd5953d770d541e704b7dc7fe8580e98b3066
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104262532"
---
# <a name="win32_comapplicationsettings-class"></a><span data-ttu-id="3d421-103">\_Класс Win32 комаппликатионсеттингс</span><span class="sxs-lookup"><span data-stu-id="3d421-103">Win32\_COMApplicationSettings class</span></span>

<span data-ttu-id="3d421-104">[Класс WMI](/windows/desktop/WmiSdk/retrieving-a-class) взаимосвязей **Win32 \_ комаппликатионсеттингс** связывает приложение DCOM и его параметры конфигурации.</span><span class="sxs-lookup"><span data-stu-id="3d421-104">The **Win32\_COMApplicationSettings** association [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) relates a DCOM application and its configuration settings.</span></span>

<span data-ttu-id="3d421-105">Приведенный ниже синтаксис является упрощенной версией кода MOF и включает все унаследованные свойства.</span><span class="sxs-lookup"><span data-stu-id="3d421-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="3d421-106">Свойства перечислены в алфавитном порядке, а не в MOF.</span><span class="sxs-lookup"><span data-stu-id="3d421-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="3d421-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="3d421-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{E5D8A563-F6C0-11d2-B35E-00105A1F8569}"), AMENDMENT]
class Win32_COMApplicationSettings : CIM_ElementSetting
{
  Win32_DCOMApplicationSetting REF Setting;
  Win32_DCOMApplication        REF Element;
};
```

## <a name="members"></a><span data-ttu-id="3d421-108">Члены</span><span class="sxs-lookup"><span data-stu-id="3d421-108">Members</span></span>

<span data-ttu-id="3d421-109">Класс **Win32 \_ комаппликатионсеттингс** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="3d421-109">The **Win32\_COMApplicationSettings** class has these types of members:</span></span>

-   [<span data-ttu-id="3d421-110">Свойства</span><span class="sxs-lookup"><span data-stu-id="3d421-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="3d421-111">Свойства</span><span class="sxs-lookup"><span data-stu-id="3d421-111">Properties</span></span>

<span data-ttu-id="3d421-112">Класс **Win32 \_ комаппликатионсеттингс** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="3d421-112">The **Win32\_COMApplicationSettings** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="3d421-113">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="3d421-113">**Element**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3d421-114">Тип данных: **Win32 \_ дкомаппликатион**</span><span class="sxs-lookup"><span data-stu-id="3d421-114">Data type: **Win32\_DCOMApplication**</span></span>
</dt> <dt>

<span data-ttu-id="3d421-115">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="3d421-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3d421-116">Квалификаторы: [**ключ**](/windows/desktop/WmiSdk/key-qualifier), [**Переопределение**](/windows/desktop/WmiSdk/standard-qualifiers) ("элемент"), [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI \| Win32 \_ дкомаппликатион")</span><span class="sxs-lookup"><span data-stu-id="3d421-116">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Element"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI\|Win32\_DCOMApplication")</span></span>
</dt> </dl>

<span data-ttu-id="3d421-117">[**\_ Дкомаппликатион Win32**](win32-dcomapplication.md) , представляющий DCOM-приложение, в котором применяются параметры.</span><span class="sxs-lookup"><span data-stu-id="3d421-117">A [**Win32\_DCOMApplication**](win32-dcomapplication.md) that represents the DCOM application where the settings are applied.</span></span>

</dd> <dt>

<span data-ttu-id="3d421-118">**Параметр**</span><span class="sxs-lookup"><span data-stu-id="3d421-118">**Setting**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3d421-119">Тип данных: **Win32 \_ дкомаппликатионсеттинг**</span><span class="sxs-lookup"><span data-stu-id="3d421-119">Data type: **Win32\_DCOMApplicationSetting**</span></span>
</dt> <dt>

<span data-ttu-id="3d421-120">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="3d421-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3d421-121">Квалификаторы: [**ключ**](/windows/desktop/WmiSdk/key-qualifier), [**Переопределение**](/windows/desktop/WmiSdk/standard-qualifiers) ("параметр"), [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI \| Win32 \_ дкомаппликатионсеттинг")</span><span class="sxs-lookup"><span data-stu-id="3d421-121">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Setting"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI\|Win32\_DCOMApplicationSetting")</span></span>
</dt> </dl>

<span data-ttu-id="3d421-122">[**\_ Дкомаппликатионсеттинг Win32**](win32-dcomapplicationsetting.md) , представляющий параметры конфигурации, связанные с приложением DCOM.</span><span class="sxs-lookup"><span data-stu-id="3d421-122">A [**Win32\_DCOMApplicationSetting**](win32-dcomapplicationsetting.md) that represents the configuration settings associated with the DCOM application.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="3d421-123">Комментарии</span><span class="sxs-lookup"><span data-stu-id="3d421-123">Remarks</span></span>

<span data-ttu-id="3d421-124">Класс **Win32 \_ комаппликатионсеттингс** является производным от [**CIM \_ елементсеттинг**](cim-elementsetting.md).</span><span class="sxs-lookup"><span data-stu-id="3d421-124">The **Win32\_COMApplicationSettings** class is derived from [**CIM\_ElementSetting**](cim-elementsetting.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="3d421-125">Требования</span><span class="sxs-lookup"><span data-stu-id="3d421-125">Requirements</span></span>



| <span data-ttu-id="3d421-126">Требование</span><span class="sxs-lookup"><span data-stu-id="3d421-126">Requirement</span></span> | <span data-ttu-id="3d421-127">Значение</span><span class="sxs-lookup"><span data-stu-id="3d421-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="3d421-128">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="3d421-128">Minimum supported client</span></span><br/> | <span data-ttu-id="3d421-129">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="3d421-129">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="3d421-130">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="3d421-130">Minimum supported server</span></span><br/> | <span data-ttu-id="3d421-131">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="3d421-131">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="3d421-132">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="3d421-132">Namespace</span></span><br/>                | <span data-ttu-id="3d421-133">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="3d421-133">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="3d421-134">MOF</span><span class="sxs-lookup"><span data-stu-id="3d421-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="3d421-135"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="3d421-135"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="3d421-136">DLL</span><span class="sxs-lookup"><span data-stu-id="3d421-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3d421-137"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3d421-137"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3d421-138">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="3d421-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3d421-139">**\_ЕЛЕМЕНТСЕТТИНГ CIM**</span><span class="sxs-lookup"><span data-stu-id="3d421-139">**CIM\_ElementSetting**</span></span>](cim-elementsetting.md)
</dt> <dt>

<span data-ttu-id="3d421-140">[Классы операционной системы](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="3d421-140">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> </dl>

 

