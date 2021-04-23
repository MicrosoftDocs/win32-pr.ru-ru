---
description: '\_Класс WMI взаимосвязей Win32 системдриверпнпентити связывает устройство Самонастраивающийся в компьютерной системе под Windows и драйвер, поддерживающий устройство Самонастраивающийся.'
ms.assetid: 2696c8e5-3bc3-42e3-807b-a387607c7c09
ms.tgt_platform: multiple
title: Класс Win32_SystemDriverPNPEntity
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_SystemDriverPNPEntity
- Win32_SystemDriverPNPEntity.Antecedent
- Win32_SystemDriverPNPEntity.Dependent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 8b5a7eedfbd7a545e37cb9cda38c19cf61308761
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104538915"
---
# <a name="win32_systemdriverpnpentity-class"></a><span data-ttu-id="a4c1c-103">\_Класс Win32 системдриверпнпентити</span><span class="sxs-lookup"><span data-stu-id="a4c1c-103">Win32\_SystemDriverPNPEntity class</span></span>

<span data-ttu-id="a4c1c-104">[Класс WMI](../wmisdk/retrieving-a-class.md) взаимосвязей **Win32 \_ системдриверпнпентити** связывает устройство Самонастраивающийся в компьютерной системе под Windows и драйвер, поддерживающий устройство Самонастраивающийся.</span><span class="sxs-lookup"><span data-stu-id="a4c1c-104">The **Win32\_SystemDriverPNPEntity** association [WMI class](../wmisdk/retrieving-a-class.md) relates a Plug and Play device on the computer system running Windows and the driver that supports the Plug and Play device.</span></span>

<span data-ttu-id="a4c1c-105">Следующий пример синтаксиса — упрощенный MOF-код, который включает все наследуемые свойства.</span><span class="sxs-lookup"><span data-stu-id="a4c1c-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="a4c1c-106">Свойства перечислены в алфавитном порядке, а не в MOF.</span><span class="sxs-lookup"><span data-stu-id="a4c1c-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="a4c1c-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="a4c1c-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{0800F074-CB98-11d2-B35D-00104BC97924}"), AMENDMENT]
class Win32_SystemDriverPNPEntity : CIM_Dependency
{
  Win32_PNPEntity    REF Antecedent;
  Win32_SystemDriver REF Dependent;
};
```

## <a name="members"></a><span data-ttu-id="a4c1c-108">Члены</span><span class="sxs-lookup"><span data-stu-id="a4c1c-108">Members</span></span>

<span data-ttu-id="a4c1c-109">Класс **Win32 \_ системдриверпнпентити** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="a4c1c-109">The **Win32\_SystemDriverPNPEntity** class has these types of members:</span></span>

-   [<span data-ttu-id="a4c1c-110">Свойства</span><span class="sxs-lookup"><span data-stu-id="a4c1c-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="a4c1c-111">Свойства</span><span class="sxs-lookup"><span data-stu-id="a4c1c-111">Properties</span></span>

<span data-ttu-id="a4c1c-112">Класс **Win32 \_ системдриверпнпентити** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="a4c1c-112">The **Win32\_SystemDriverPNPEntity** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="a4c1c-113">**Завершил**</span><span class="sxs-lookup"><span data-stu-id="a4c1c-113">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a4c1c-114">Тип данных: **Win32 \_ пнпентити**</span><span class="sxs-lookup"><span data-stu-id="a4c1c-114">Data type: **Win32\_PNPEntity**</span></span>
</dt> <dt>

<span data-ttu-id="a4c1c-115">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="a4c1c-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a4c1c-116">Квалификаторы: [**ключ**](../wmisdk/key-qualifier.md), [**Переопределение**](../wmisdk/standard-qualifiers.md) ("Antecedent"), [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("WMI \| Win32 \_ пнпентити")</span><span class="sxs-lookup"><span data-stu-id="a4c1c-116">Qualifiers: [**Key**](../wmisdk/key-qualifier.md), [**Override**](../wmisdk/standard-qualifiers.md) ("Antecedent"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI\|Win32\_PNPEntity")</span></span>
</dt> </dl>

<span data-ttu-id="a4c1c-117">Представляет самонастраивающийся устройство, управляемое драйвером.</span><span class="sxs-lookup"><span data-stu-id="a4c1c-117">Represents the Plug and Play device controlled by the driver.</span></span>

</dd> <dt>

<span data-ttu-id="a4c1c-118">**Него**</span><span class="sxs-lookup"><span data-stu-id="a4c1c-118">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a4c1c-119">Тип данных: **Win32 \_ SystemDriver**</span><span class="sxs-lookup"><span data-stu-id="a4c1c-119">Data type: **Win32\_SystemDriver**</span></span>
</dt> <dt>

<span data-ttu-id="a4c1c-120">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="a4c1c-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a4c1c-121">Квалификаторы: [**ключ**](../wmisdk/key-qualifier.md), [**Переопределение**](../wmisdk/standard-qualifiers.md) ("Dependent"), [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("WMI \| Win32 \_ SystemDriver")</span><span class="sxs-lookup"><span data-stu-id="a4c1c-121">Qualifiers: [**Key**](../wmisdk/key-qualifier.md), [**Override**](../wmisdk/standard-qualifiers.md) ("Dependent"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI\|Win32\_SystemDriver")</span></span>
</dt> </dl>

<span data-ttu-id="a4c1c-122">[**\_ SystemDriver Win32**](win32-systemdriver.md) , который представляет драйвер, поддерживающий устройство Самонастраивающийся.</span><span class="sxs-lookup"><span data-stu-id="a4c1c-122">A [**Win32\_SystemDriver**](win32-systemdriver.md) that represents the driver that supports the Plug and Play device.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="a4c1c-123">Комментарии</span><span class="sxs-lookup"><span data-stu-id="a4c1c-123">Remarks</span></span>

<span data-ttu-id="a4c1c-124">Класс **Win32 \_ системдриверпнпентити** является производным от [**\_ зависимости CIM**](cim-dependency.md).</span><span class="sxs-lookup"><span data-stu-id="a4c1c-124">The **Win32\_SystemDriverPNPEntity** class is derived from [**CIM\_Dependency**](cim-dependency.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="a4c1c-125">Требования</span><span class="sxs-lookup"><span data-stu-id="a4c1c-125">Requirements</span></span>



| <span data-ttu-id="a4c1c-126">Требование</span><span class="sxs-lookup"><span data-stu-id="a4c1c-126">Requirement</span></span> | <span data-ttu-id="a4c1c-127">Значение</span><span class="sxs-lookup"><span data-stu-id="a4c1c-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a4c1c-128">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="a4c1c-128">Minimum supported client</span></span><br/> | <span data-ttu-id="a4c1c-129">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="a4c1c-129">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="a4c1c-130">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="a4c1c-130">Minimum supported server</span></span><br/> | <span data-ttu-id="a4c1c-131">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="a4c1c-131">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="a4c1c-132">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="a4c1c-132">Namespace</span></span><br/>                | <span data-ttu-id="a4c1c-133">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="a4c1c-133">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="a4c1c-134">MOF</span><span class="sxs-lookup"><span data-stu-id="a4c1c-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="a4c1c-135"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="a4c1c-135"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="a4c1c-136">DLL</span><span class="sxs-lookup"><span data-stu-id="a4c1c-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a4c1c-137"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a4c1c-137"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a4c1c-138">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="a4c1c-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a4c1c-139">**\_Зависимость CIM**</span><span class="sxs-lookup"><span data-stu-id="a4c1c-139">**CIM\_Dependency**</span></span>](cim-dependency.md)
</dt> <dt>

[<span data-ttu-id="a4c1c-140">Аппаратные классы системы компьютера</span><span class="sxs-lookup"><span data-stu-id="a4c1c-140">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> </dl>

 

 
