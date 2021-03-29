---
description: '\_Класс WMI взаимосвязей Win32 усердесктоп связывает учетную запись пользователя и параметры рабочего стола, относящиеся к нему.'
ms.assetid: 5ea83ad6-bd0a-4c16-85b2-e3e61ef05903
ms.tgt_platform: multiple
title: Класс Win32_UserDesktop
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_UserDesktop
- Win32_UserDesktop.Element
- Win32_UserDesktop.Setting
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 39b45ee7859fea9f1068123041a87309cf40c2d2
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103895590"
---
# <a name="win32_userdesktop-class"></a><span data-ttu-id="5a1a7-103">\_Класс Win32 усердесктоп</span><span class="sxs-lookup"><span data-stu-id="5a1a7-103">Win32\_UserDesktop class</span></span>

<span data-ttu-id="5a1a7-104">[Класс WMI](../wmisdk/retrieving-a-class.md) взаимосвязей **Win32 \_ усердесктоп** связывает учетную запись пользователя и параметры рабочего стола, относящиеся к нему.</span><span class="sxs-lookup"><span data-stu-id="5a1a7-104">The **Win32\_UserDesktop** association [WMI class](../wmisdk/retrieving-a-class.md) relates a user account and desktop settings that are specific to it.</span></span>

<span data-ttu-id="5a1a7-105">Следующий пример синтаксиса — упрощенный MOF-код, который включает все наследуемые свойства.</span><span class="sxs-lookup"><span data-stu-id="5a1a7-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="5a1a7-106">Свойства и методы имеют алфавитный порядок, а не порядок MOF.</span><span class="sxs-lookup"><span data-stu-id="5a1a7-106">Properties and methods are in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="5a1a7-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="5a1a7-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8502C4FF-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_UserDesktop : CIM_ElementSetting
{
  Win32_UserAccount REF Element;
  Win32_Desktop     REF Setting;
};
```

## <a name="members"></a><span data-ttu-id="5a1a7-108">Члены</span><span class="sxs-lookup"><span data-stu-id="5a1a7-108">Members</span></span>

<span data-ttu-id="5a1a7-109">Класс **Win32 \_ усердесктоп** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="5a1a7-109">The **Win32\_UserDesktop** class has these types of members:</span></span>

-   [<span data-ttu-id="5a1a7-110">Свойства</span><span class="sxs-lookup"><span data-stu-id="5a1a7-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="5a1a7-111">Свойства</span><span class="sxs-lookup"><span data-stu-id="5a1a7-111">Properties</span></span>

<span data-ttu-id="5a1a7-112">Класс **Win32 \_ усердесктоп** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="5a1a7-112">The **Win32\_UserDesktop** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="5a1a7-113">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="5a1a7-113">**Element**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5a1a7-114">Тип данных: **Win32 \_ UserAccount**</span><span class="sxs-lookup"><span data-stu-id="5a1a7-114">Data type: **Win32\_UserAccount**</span></span>
</dt> <dt>

<span data-ttu-id="5a1a7-115">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="5a1a7-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5a1a7-116">Квалификаторы: [**ключ**](../wmisdk/key-qualifier.md), [**Переопределение**](../wmisdk/standard-qualifiers.md) ("элемент"), [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("WMI \| Win32 \_ UserAccount")</span><span class="sxs-lookup"><span data-stu-id="5a1a7-116">Qualifiers: [**key**](../wmisdk/key-qualifier.md), [**Override**](../wmisdk/standard-qualifiers.md) ("Element"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI\|Win32\_UserAccount")</span></span>
</dt> </dl>

<span data-ttu-id="5a1a7-117">Ссылка на экземпляр, представляющий учетную запись пользователя, Рабочий стол которой можно настроить с помощью свойства **Settings** этого класса.</span><span class="sxs-lookup"><span data-stu-id="5a1a7-117">Reference to the instance representing the user account whose desktop can be customized by the **Settings** property of this class.</span></span>

</dd> <dt>

<span data-ttu-id="5a1a7-118">**Параметр**</span><span class="sxs-lookup"><span data-stu-id="5a1a7-118">**Setting**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5a1a7-119">Тип данных: **\_ классическую панель Win32**</span><span class="sxs-lookup"><span data-stu-id="5a1a7-119">Data type: **Win32\_Desktop**</span></span>
</dt> <dt>

<span data-ttu-id="5a1a7-120">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="5a1a7-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5a1a7-121">Квалификаторы: [**ключ**](../wmisdk/key-qualifier.md), [**Переопределение**](../wmisdk/standard-qualifiers.md) ("параметр"), [**Маппингстрингс**](../wmisdk/standard-qualifiers.md) ("Инструментарий WMI \| Win32 \_ Desktop")</span><span class="sxs-lookup"><span data-stu-id="5a1a7-121">Qualifiers: [**key**](../wmisdk/key-qualifier.md), [**Override**](../wmisdk/standard-qualifiers.md) ("Setting"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI\|Win32\_Desktop")</span></span>
</dt> </dl>

<span data-ttu-id="5a1a7-122">Ссылка на экземпляр, представляющий параметры рабочего стола, которые служат для настройки конкретной учетной записи пользователя.</span><span class="sxs-lookup"><span data-stu-id="5a1a7-122">Reference to the instance representing the desktop settings that serve to customize a specific user account desktop.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="5a1a7-123">Комментарии</span><span class="sxs-lookup"><span data-stu-id="5a1a7-123">Remarks</span></span>

<span data-ttu-id="5a1a7-124">Класс **Win32 \_ усердесктоп** является производным от [**CIM \_ елементсеттинг**](cim-elementsetting.md).</span><span class="sxs-lookup"><span data-stu-id="5a1a7-124">The **Win32\_UserDesktop** class is derived from [**CIM\_ElementSetting**](cim-elementsetting.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="5a1a7-125">Требования</span><span class="sxs-lookup"><span data-stu-id="5a1a7-125">Requirements</span></span>



| <span data-ttu-id="5a1a7-126">Требование</span><span class="sxs-lookup"><span data-stu-id="5a1a7-126">Requirement</span></span> | <span data-ttu-id="5a1a7-127">Значение</span><span class="sxs-lookup"><span data-stu-id="5a1a7-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="5a1a7-128">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="5a1a7-128">Minimum supported client</span></span><br/> | <span data-ttu-id="5a1a7-129">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="5a1a7-129">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="5a1a7-130">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="5a1a7-130">Minimum supported server</span></span><br/> | <span data-ttu-id="5a1a7-131">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="5a1a7-131">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="5a1a7-132">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="5a1a7-132">Namespace</span></span><br/>                | <span data-ttu-id="5a1a7-133">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="5a1a7-133">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="5a1a7-134">MOF</span><span class="sxs-lookup"><span data-stu-id="5a1a7-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="5a1a7-135"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="5a1a7-135"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="5a1a7-136">DLL</span><span class="sxs-lookup"><span data-stu-id="5a1a7-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5a1a7-137"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5a1a7-137"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5a1a7-138">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="5a1a7-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5a1a7-139">**\_ЕЛЕМЕНТСЕТТИНГ CIM**</span><span class="sxs-lookup"><span data-stu-id="5a1a7-139">**CIM\_ElementSetting**</span></span>](cim-elementsetting.md)
</dt> <dt>

[<span data-ttu-id="5a1a7-140">Классы операционной системы</span><span class="sxs-lookup"><span data-stu-id="5a1a7-140">Operating System Classes</span></span>](./operating-system-classes.md)
</dt> </dl>

 

 
