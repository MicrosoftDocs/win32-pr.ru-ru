---
description: '\_Класс WMI абстрактных ассоциаций Win32 комаппликатионклассес связывает компонент модели COM и COM-приложение, в котором оно находится.'
ms.assetid: 7c188199-86fb-45ba-b318-9d9529b831b8
ms.tgt_platform: multiple
title: Класс Win32_COMApplicationClasses
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_COMApplicationClasses
- Win32_COMApplicationClasses.PartComponent
- Win32_COMApplicationClasses.GroupComponent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 01413128f7457049a4383c1148938e2136645337
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104142298"
---
# <a name="win32_comapplicationclasses-class"></a><span data-ttu-id="7213f-103">\_Класс Win32 комаппликатионклассес</span><span class="sxs-lookup"><span data-stu-id="7213f-103">Win32\_COMApplicationClasses class</span></span>

<span data-ttu-id="7213f-104">[Класс WMI](/windows/desktop/WmiSdk/retrieving-a-class) абстрактных ассоциаций **Win32 \_ КОМАППЛИКАТИОНКЛАССЕС** связывает компонент модели COM и COM-приложение, в котором оно находится.</span><span class="sxs-lookup"><span data-stu-id="7213f-104">The **Win32\_COMApplicationClasses** abstract association [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) relates a Component Object Model (COM) component and the COM application where it resides.</span></span>

<span data-ttu-id="7213f-105">Следующий пример синтаксиса — упрощенный MOF-код, который включает все наследуемые свойства.</span><span class="sxs-lookup"><span data-stu-id="7213f-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="7213f-106">Свойства перечислены в алфавитном порядке, а не в MOF.</span><span class="sxs-lookup"><span data-stu-id="7213f-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="7213f-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="7213f-107">Syntax</span></span>

``` syntax
[abstract, UUID("{0F73ED51-8ED9-11d2-B340-00105A1F8569}"), AMENDMENT]
class Win32_COMApplicationClasses : CIM_Component
{
  Win32_COMClass       REF PartComponent;
  Win32_COMApplication REF GroupComponent;
};
```

## <a name="members"></a><span data-ttu-id="7213f-108">Члены</span><span class="sxs-lookup"><span data-stu-id="7213f-108">Members</span></span>

<span data-ttu-id="7213f-109">Класс **Win32 \_ комаппликатионклассес** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="7213f-109">The **Win32\_COMApplicationClasses** class has these types of members:</span></span>

-   [<span data-ttu-id="7213f-110">Свойства</span><span class="sxs-lookup"><span data-stu-id="7213f-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="7213f-111">Свойства</span><span class="sxs-lookup"><span data-stu-id="7213f-111">Properties</span></span>

<span data-ttu-id="7213f-112">Класс **Win32 \_ комаппликатионклассес** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="7213f-112">The **Win32\_COMApplicationClasses** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="7213f-113">**Ссылка**</span><span class="sxs-lookup"><span data-stu-id="7213f-113">**GroupComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7213f-114">Тип данных: **Win32 \_ комаппликатион**</span><span class="sxs-lookup"><span data-stu-id="7213f-114">Data type: **Win32\_COMApplication**</span></span>
</dt> <dt>

<span data-ttu-id="7213f-115">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="7213f-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7213f-116">Квалификаторы: [**ключ**](/windows/desktop/WmiSdk/key-qualifier), [**Переопределение**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent"), [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI \| Win32 \_ комаппликатион")</span><span class="sxs-lookup"><span data-stu-id="7213f-116">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI\|Win32\_COMApplication")</span></span>
</dt> </dl>

<span data-ttu-id="7213f-117">[**\_ Комаппликатион Win32**](win32-comapplication.md) , представляющий COM-приложение, содержащее COM-компонент.</span><span class="sxs-lookup"><span data-stu-id="7213f-117">A [**Win32\_COMApplication**](win32-comapplication.md) that represents the COM application containing the COM component.</span></span>

</dd> <dt>

<span data-ttu-id="7213f-118">**PartComponent**</span><span class="sxs-lookup"><span data-stu-id="7213f-118">**PartComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7213f-119">Тип данных: **Win32 \_ COMClass**</span><span class="sxs-lookup"><span data-stu-id="7213f-119">Data type: **Win32\_COMClass**</span></span>
</dt> <dt>

<span data-ttu-id="7213f-120">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="7213f-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7213f-121">Квалификаторы: [**ключ**](/windows/desktop/WmiSdk/key-qualifier), [**Переопределение**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent"), [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI \| Win32 \_ COMClass")</span><span class="sxs-lookup"><span data-stu-id="7213f-121">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI\|Win32\_COMClass")</span></span>
</dt> </dl>

<span data-ttu-id="7213f-122">[**\_ COMClass Win32**](win32-comclass.md) , представляющий COM-компонент, СГРУППИРОВАННЫЙ в COM-приложении.</span><span class="sxs-lookup"><span data-stu-id="7213f-122">A [**Win32\_COMClass**](win32-comclass.md) that represents the COM component grouped under the COM application.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="7213f-123">Комментарии</span><span class="sxs-lookup"><span data-stu-id="7213f-123">Remarks</span></span>

<span data-ttu-id="7213f-124">Класс **Win32 \_ комаппликатионклассес** является производным от [**\_ компонента CIM**](cim-component.md).</span><span class="sxs-lookup"><span data-stu-id="7213f-124">The **Win32\_COMApplicationClasses** class is derived from [**CIM\_Component**](cim-component.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="7213f-125">Требования</span><span class="sxs-lookup"><span data-stu-id="7213f-125">Requirements</span></span>



| <span data-ttu-id="7213f-126">Требование</span><span class="sxs-lookup"><span data-stu-id="7213f-126">Requirement</span></span> | <span data-ttu-id="7213f-127">Значение</span><span class="sxs-lookup"><span data-stu-id="7213f-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="7213f-128">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="7213f-128">Minimum supported client</span></span><br/> | <span data-ttu-id="7213f-129">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="7213f-129">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="7213f-130">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="7213f-130">Minimum supported server</span></span><br/> | <span data-ttu-id="7213f-131">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="7213f-131">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="7213f-132">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="7213f-132">Namespace</span></span><br/>                | <span data-ttu-id="7213f-133">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="7213f-133">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="7213f-134">MOF</span><span class="sxs-lookup"><span data-stu-id="7213f-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="7213f-135"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="7213f-135"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="7213f-136">DLL</span><span class="sxs-lookup"><span data-stu-id="7213f-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7213f-137"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7213f-137"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7213f-138">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="7213f-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7213f-139">**\_Компонент CIM**</span><span class="sxs-lookup"><span data-stu-id="7213f-139">**CIM\_Component**</span></span>](cim-component.md)
</dt> <dt>

<span data-ttu-id="7213f-140">[Классы операционной системы](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="7213f-140">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> </dl>

 

