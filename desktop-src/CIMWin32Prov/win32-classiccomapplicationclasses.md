---
description: '\_Класс WMI взаимосвязей Win32 классиккомаппликатионклассес связывает приложение COM и компонент COM, сгруппированный под ним.'
ms.assetid: 77f24461-9ca0-4fc3-8728-4a4b9a1edbc3
ms.tgt_platform: multiple
title: Класс Win32_ClassicCOMApplicationClasses
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_ClassicCOMApplicationClasses
- Win32_ClassicCOMApplicationClasses.PartComponent
- Win32_ClassicCOMApplicationClasses.GroupComponent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: dfd451c1c5d4819f1ec1d21f890b207a06d6fb82
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103896286"
---
# <a name="win32_classiccomapplicationclasses-class"></a><span data-ttu-id="1107c-103">\_Класс Win32 классиккомаппликатионклассес</span><span class="sxs-lookup"><span data-stu-id="1107c-103">Win32\_ClassicCOMApplicationClasses class</span></span>

<span data-ttu-id="1107c-104">[Класс WMI](/windows/desktop/WmiSdk/retrieving-a-class) взаимосвязей **Win32 \_ классиккомаппликатионклассес** связывает приложение COM и компонент COM, сгруппированный под ним.</span><span class="sxs-lookup"><span data-stu-id="1107c-104">The **Win32\_ClassicCOMApplicationClasses** association [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) relates a COM application and a COM component grouped under it.</span></span>

<span data-ttu-id="1107c-105">Следующий пример синтаксиса — упрощенный MOF-код, который включает все наследуемые свойства.</span><span class="sxs-lookup"><span data-stu-id="1107c-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="1107c-106">Свойства перечислены в алфавитном порядке, а не в MOF.</span><span class="sxs-lookup"><span data-stu-id="1107c-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="1107c-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="1107c-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{0F73ED54-8ED9-11d2-B340-00105A1F8569}"), AMENDMENT]
class Win32_ClassicCOMApplicationClasses : Win32_COMApplicationClasses
{
  Win32_ClassicCOMClass REF PartComponent;
  Win32_DCOMApplication REF GroupComponent;
};
```

## <a name="members"></a><span data-ttu-id="1107c-108">Члены</span><span class="sxs-lookup"><span data-stu-id="1107c-108">Members</span></span>

<span data-ttu-id="1107c-109">Класс **Win32 \_ классиккомаппликатионклассес** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="1107c-109">The **Win32\_ClassicCOMApplicationClasses** class has these types of members:</span></span>

-   [<span data-ttu-id="1107c-110">Свойства</span><span class="sxs-lookup"><span data-stu-id="1107c-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="1107c-111">Свойства</span><span class="sxs-lookup"><span data-stu-id="1107c-111">Properties</span></span>

<span data-ttu-id="1107c-112">Класс **Win32 \_ классиккомаппликатионклассес** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="1107c-112">The **Win32\_ClassicCOMApplicationClasses** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="1107c-113">**Ссылка**</span><span class="sxs-lookup"><span data-stu-id="1107c-113">**GroupComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1107c-114">Тип данных: **Win32 \_ дкомаппликатион**</span><span class="sxs-lookup"><span data-stu-id="1107c-114">Data type: **Win32\_DCOMApplication**</span></span>
</dt> <dt>

<span data-ttu-id="1107c-115">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="1107c-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1107c-116">Квалификаторы: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent"), [**Маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI \| Win32 \_ дкомаппликатион")</span><span class="sxs-lookup"><span data-stu-id="1107c-116">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI\|Win32\_DCOMApplication")</span></span>
</dt> </dl>

<span data-ttu-id="1107c-117">[**\_ Дкомаппликатион Win32**](win32-dcomapplication.md) , представляющий приложение DCOM, содержащее или использующее COM-компонент.</span><span class="sxs-lookup"><span data-stu-id="1107c-117">A [**Win32\_DCOMApplication**](win32-dcomapplication.md) that represents a DCOM application containing or using the COM component.</span></span>

</dd> <dt>

<span data-ttu-id="1107c-118">**PartComponent**</span><span class="sxs-lookup"><span data-stu-id="1107c-118">**PartComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1107c-119">Тип данных: **Win32 \_ классиккомкласс**</span><span class="sxs-lookup"><span data-stu-id="1107c-119">Data type: **Win32\_ClassicCOMClass**</span></span>
</dt> <dt>

<span data-ttu-id="1107c-120">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="1107c-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1107c-121">Квалификаторы: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent"), [**Маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI \| Win32 \_ классиккомкласс")</span><span class="sxs-lookup"><span data-stu-id="1107c-121">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI\|Win32\_ClassicCOMClass")</span></span>
</dt> </dl>

<span data-ttu-id="1107c-122">[**\_ Классиккомкласс Win32**](win32-classiccomclass.md) , представляющий COM-компонент, существующий в или используемый приложением DCOM.</span><span class="sxs-lookup"><span data-stu-id="1107c-122">A [**Win32\_ClassicCOMClass**](win32-classiccomclass.md) that represents the COM component existing in or used by the DCOM application.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="1107c-123">Комментарии</span><span class="sxs-lookup"><span data-stu-id="1107c-123">Remarks</span></span>

<span data-ttu-id="1107c-124">Класс **Win32 \_ классиккомаппликатионклассес** является производным от [**Win32 \_ комаппликатионклассес**](win32-comapplicationclasses.md).</span><span class="sxs-lookup"><span data-stu-id="1107c-124">The **Win32\_ClassicCOMApplicationClasses** class is derived from [**Win32\_COMApplicationClasses**](win32-comapplicationclasses.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="1107c-125">Требования</span><span class="sxs-lookup"><span data-stu-id="1107c-125">Requirements</span></span>



| <span data-ttu-id="1107c-126">Требование</span><span class="sxs-lookup"><span data-stu-id="1107c-126">Requirement</span></span> | <span data-ttu-id="1107c-127">Значение</span><span class="sxs-lookup"><span data-stu-id="1107c-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="1107c-128">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="1107c-128">Minimum supported client</span></span><br/> | <span data-ttu-id="1107c-129">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="1107c-129">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="1107c-130">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="1107c-130">Minimum supported server</span></span><br/> | <span data-ttu-id="1107c-131">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="1107c-131">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="1107c-132">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="1107c-132">Namespace</span></span><br/>                | <span data-ttu-id="1107c-133">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="1107c-133">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="1107c-134">MOF</span><span class="sxs-lookup"><span data-stu-id="1107c-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="1107c-135"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="1107c-135"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="1107c-136">DLL</span><span class="sxs-lookup"><span data-stu-id="1107c-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1107c-137"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1107c-137"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1107c-138">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="1107c-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1107c-139">**\_Комаппликатионклассес Win32**</span><span class="sxs-lookup"><span data-stu-id="1107c-139">**Win32\_COMApplicationClasses**</span></span>](win32-comapplicationclasses.md)
</dt> <dt>

<span data-ttu-id="1107c-140">[Классы операционной системы](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="1107c-140">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> </dl>

 

