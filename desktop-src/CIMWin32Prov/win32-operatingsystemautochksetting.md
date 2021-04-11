---
description: Этот класс представляет связь между операционной системой и параметрами Autochk, которые применяются к дискам на компьютере. Обратите внимание, что этот параметр связан с операционной системой, а не с компьютерной системой, так как на компьютере может быть установлена одна или несколько операционных систем, каждая из которых имеет собственные параметры Autochk.
ms.assetid: 11178459-85c2-41c0-83b3-5b967e3311cf
ms.tgt_platform: multiple
title: Класс Win32_OperatingSystemAutochkSetting
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- kbSyntax
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 905ffc92273b46bb36b7b3e2909afea32e6baeff
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104142475"
---
# <a name="win32_operatingsystemautochksetting-class"></a><span data-ttu-id="cfe00-103">\_Класс Win32 оператингсистемауточксеттинг</span><span class="sxs-lookup"><span data-stu-id="cfe00-103">Win32\_OperatingSystemAutochkSetting class</span></span>

<span data-ttu-id="cfe00-104">Этот класс представляет связь между операционной системой и параметрами Autochk, которые применяются к дискам на компьютере. Обратите внимание, что этот параметр связан с операционной системой, а не с компьютерной системой, так как на компьютере может быть установлена одна или несколько операционных систем, каждая из которых имеет собственные параметры Autochk.</span><span class="sxs-lookup"><span data-stu-id="cfe00-104">This class represents the association between an operating system and the autochk settings that apply to the disks on the machine.Note that the setting is associated to operating system rather than computer system since there can be one or more operating systems installed on the machine, each with its own autochk settings.</span></span>

<span data-ttu-id="cfe00-105">Следующий пример синтаксиса — упрощенный MOF-код, который включает все наследуемые свойства.</span><span class="sxs-lookup"><span data-stu-id="cfe00-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="cfe00-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="cfe00-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32a"), AMENDMENT]
class Win32_OperatingSystemAutochkSetting : CIM_ElementSetting
{
  Win32_OperatingSystem REF Element;
  Win32_AutochkSetting  REF Setting;
};
```

## <a name="members"></a><span data-ttu-id="cfe00-107">Члены</span><span class="sxs-lookup"><span data-stu-id="cfe00-107">Members</span></span>

<span data-ttu-id="cfe00-108">Класс **Win32 \_ оператингсистемауточксеттинг** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="cfe00-108">The **Win32\_OperatingSystemAutochkSetting** class has these types of members:</span></span>

-   [<span data-ttu-id="cfe00-109">Свойства</span><span class="sxs-lookup"><span data-stu-id="cfe00-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="cfe00-110">Свойства</span><span class="sxs-lookup"><span data-stu-id="cfe00-110">Properties</span></span>

<span data-ttu-id="cfe00-111">Класс **Win32 \_ оператингсистемауточксеттинг** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="cfe00-111">The **Win32\_OperatingSystemAutochkSetting** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="cfe00-112">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="cfe00-112">**Element**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cfe00-113">Тип данных: **Win32 с \_ операционной** системы</span><span class="sxs-lookup"><span data-stu-id="cfe00-113">Data type: **Win32\_OperatingSystem**</span></span>
</dt> <dt>

<span data-ttu-id="cfe00-114">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="cfe00-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cfe00-115">Квалификаторы: [**override**](../wmisdk/standard-qualifiers.md) ("элемент"), [**ключ**](../wmisdk/key-qualifier.md)</span><span class="sxs-lookup"><span data-stu-id="cfe00-115">Qualifiers: [**Override**](../wmisdk/standard-qualifiers.md) ("Element"), [**key**](../wmisdk/key-qualifier.md)</span></span>
</dt> </dl>

<span data-ttu-id="cfe00-116">TBD</span><span class="sxs-lookup"><span data-stu-id="cfe00-116">TBD</span></span>

</dd> <dt>

<span data-ttu-id="cfe00-117">**Параметр**</span><span class="sxs-lookup"><span data-stu-id="cfe00-117">**Setting**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cfe00-118">Тип данных: **Win32 \_ ауточксеттинг**</span><span class="sxs-lookup"><span data-stu-id="cfe00-118">Data type: **Win32\_AutochkSetting**</span></span>
</dt> <dt>

<span data-ttu-id="cfe00-119">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="cfe00-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cfe00-120">Квалификаторы: [**override**](../wmisdk/standard-qualifiers.md) ("параметр"), [**Key**](../wmisdk/key-qualifier.md)</span><span class="sxs-lookup"><span data-stu-id="cfe00-120">Qualifiers: [**Override**](../wmisdk/standard-qualifiers.md) ("Setting"), [**key**](../wmisdk/key-qualifier.md)</span></span>
</dt> </dl>

<span data-ttu-id="cfe00-121">TBD</span><span class="sxs-lookup"><span data-stu-id="cfe00-121">TBD</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="cfe00-122">Требования</span><span class="sxs-lookup"><span data-stu-id="cfe00-122">Requirements</span></span>



| <span data-ttu-id="cfe00-123">Требование</span><span class="sxs-lookup"><span data-stu-id="cfe00-123">Requirement</span></span> | <span data-ttu-id="cfe00-124">Значение</span><span class="sxs-lookup"><span data-stu-id="cfe00-124">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="cfe00-125">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="cfe00-125">Minimum supported client</span></span><br/> | <span data-ttu-id="cfe00-126">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="cfe00-126">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="cfe00-127">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="cfe00-127">Minimum supported server</span></span><br/> | <span data-ttu-id="cfe00-128">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="cfe00-128">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="cfe00-129">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="cfe00-129">Namespace</span></span><br/>                | <span data-ttu-id="cfe00-130">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="cfe00-130">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="cfe00-131">MOF</span><span class="sxs-lookup"><span data-stu-id="cfe00-131">MOF</span></span><br/>                      | <dl> <span data-ttu-id="cfe00-132"><dt>CimWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="cfe00-132"><dt>CimWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="cfe00-133">DLL</span><span class="sxs-lookup"><span data-stu-id="cfe00-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="cfe00-134"><dt>Cimwin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="cfe00-134"><dt>Cimwin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cfe00-135">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="cfe00-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cfe00-136">**\_ЕЛЕМЕНТСЕТТИНГ CIM**</span><span class="sxs-lookup"><span data-stu-id="cfe00-136">**CIM\_ElementSetting**</span></span>](cim-elementsetting.md)
</dt> </dl>

 

 
