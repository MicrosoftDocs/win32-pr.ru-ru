---
description: '\_Объект конфигурации CIM позволяет группировать наборы параметров (определенные в \_ объектах параметров CIM) и зависимости для одного или нескольких управляемых системных элементов.'
ms.assetid: f597fe78-be50-4d31-b1eb-d219acaf1751
ms.tgt_platform: multiple
title: Класс CIM_Configuration
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_Configuration
- CIM_Configuration.Caption
- CIM_Configuration.Description
- CIM_Configuration.Name
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: c069f5c7186d08f01b54fe02c0568dbb4ff43d26
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103807601"
---
# <a name="cim_configuration-class"></a><span data-ttu-id="33da8-103">\_Класс конфигурации CIM</span><span class="sxs-lookup"><span data-stu-id="33da8-103">CIM\_Configuration class</span></span>

<span data-ttu-id="33da8-104">Объект **\_ конфигурации CIM** позволяет группировать наборы параметров (определенные в объектах [**\_ параметров CIM**](cim-setting.md) ) и зависимости для одного или нескольких управляемых системных элементов.</span><span class="sxs-lookup"><span data-stu-id="33da8-104">The **CIM\_Configuration** object allows the grouping of parameter sets (defined in [**CIM\_Setting**](cim-setting.md) objects) and dependencies for one or more managed system elements.</span></span> <span data-ttu-id="33da8-105">Этот объект представляет определенное поведение или требуемое функциональное состояние для управляемых системных элементов.</span><span class="sxs-lookup"><span data-stu-id="33da8-105">This object represents a certain behavior, or a desired functional state for the managed system elements.</span></span> <span data-ttu-id="33da8-106">Требуемое функциональное состояние обычно определяется внешними требованиями, такими как время или расположение.</span><span class="sxs-lookup"><span data-stu-id="33da8-106">The desired functional state is typically driven by external requirements, such as time or location.</span></span> <span data-ttu-id="33da8-107">Например, для подключения к почтовой системе из дома существует зависимость от модема. в то же время зависимость от сетевого адаптера существует на работе.</span><span class="sxs-lookup"><span data-stu-id="33da8-107">For example, to connect to a mail system from home, a dependency on a modem exists; whereas, a dependency on a network adapter exists at work.</span></span> <span data-ttu-id="33da8-108">Параметры для соответствующих логических устройств (в этом примере — POTS-модем и сетевой адаптер) можно определить и объединить в **\_ конфигурации CIM**.</span><span class="sxs-lookup"><span data-stu-id="33da8-108">Settings for the pertinent logical devices (in this example, POTS modem and network adapter) can be defined and aggregated by **CIM\_Configuration**.</span></span> <span data-ttu-id="33da8-109">Поэтому две конфигурации "подключение к почте" можно определить, группируя соответствующие зависимости и объекты [**\_ параметров CIM**](cim-setting.md) .</span><span class="sxs-lookup"><span data-stu-id="33da8-109">Therefore, two "Connect to Mail" configurations can be defined by grouping the relevant dependencies and [**CIM\_Setting**](cim-setting.md) objects.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="33da8-110">Классы CIM (модель CIM) в DMTF (распределенная задача управления) являются родительскими классами, на которых строятся классы WMI.</span><span class="sxs-lookup"><span data-stu-id="33da8-110">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="33da8-111">В настоящее время WMI поддерживает только [схемы версии CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="33da8-111">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="33da8-112">Приведенный ниже синтаксис является упрощенной версией кода MOF и включает все унаследованные свойства.</span><span class="sxs-lookup"><span data-stu-id="33da8-112">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="33da8-113">Свойства перечислены в алфавитном порядке, а не в MOF.</span><span class="sxs-lookup"><span data-stu-id="33da8-113">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="33da8-114">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="33da8-114">Syntax</span></span>

``` syntax
[Abstract, UUID("{4C51D7AE-DB22-11d2-85FC-0000F8102E5F}"), AMENDMENT]
class CIM_Configuration
{
  string Caption;
  string Description;
  string Name;
};
```

## <a name="members"></a><span data-ttu-id="33da8-115">Члены</span><span class="sxs-lookup"><span data-stu-id="33da8-115">Members</span></span>

<span data-ttu-id="33da8-116">Класс **\_ конфигурации CIM** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="33da8-116">The **CIM\_Configuration** class has these types of members:</span></span>

-   [<span data-ttu-id="33da8-117">Свойства</span><span class="sxs-lookup"><span data-stu-id="33da8-117">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="33da8-118">Свойства</span><span class="sxs-lookup"><span data-stu-id="33da8-118">Properties</span></span>

<span data-ttu-id="33da8-119">Класс **\_ конфигурации CIM** имеет эти свойства.</span><span class="sxs-lookup"><span data-stu-id="33da8-119">The **CIM\_Configuration** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="33da8-120">**Заголовок**</span><span class="sxs-lookup"><span data-stu-id="33da8-120">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="33da8-121">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="33da8-121">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="33da8-122">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="33da8-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="33da8-123">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="33da8-123">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="33da8-124">Краткое текстовое описание объекта **\_ конфигурации CIM** .</span><span class="sxs-lookup"><span data-stu-id="33da8-124">Short textual description of the **CIM\_Configuration** object.</span></span>

</dd> <dt>

<span data-ttu-id="33da8-125">**Описание**</span><span class="sxs-lookup"><span data-stu-id="33da8-125">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="33da8-126">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="33da8-126">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="33da8-127">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="33da8-127">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="33da8-128">Текстовое описание объекта **\_ конфигурации CIM** .</span><span class="sxs-lookup"><span data-stu-id="33da8-128">Textual description of the **CIM\_Configuration** object.</span></span>

</dd> <dt>

<span data-ttu-id="33da8-129">**Name**</span><span class="sxs-lookup"><span data-stu-id="33da8-129">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="33da8-130">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="33da8-130">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="33da8-131">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="33da8-131">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="33da8-132">Квалификаторы: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="33da8-132">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="33da8-133">Метка, по которой известен объект **\_ конфигурации CIM** .</span><span class="sxs-lookup"><span data-stu-id="33da8-133">Label by which the **CIM\_Configuration** object is known.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="33da8-134">Комментарии</span><span class="sxs-lookup"><span data-stu-id="33da8-134">Remarks</span></span>

<span data-ttu-id="33da8-135">Инструментарий WMI не реализует этот класс.</span><span class="sxs-lookup"><span data-stu-id="33da8-135">WMI does not implement this class.</span></span>

<span data-ttu-id="33da8-136">Эта документация является производной от описаний класса CIM, опубликованных в формате DMTF.</span><span class="sxs-lookup"><span data-stu-id="33da8-136">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="33da8-137">Корпорация Майкрософт могла внести изменения в Исправление незначительных ошибок, соответствовать стандартам документации пакета Microsoft SDK или предоставить дополнительные сведения.</span><span class="sxs-lookup"><span data-stu-id="33da8-137">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="33da8-138">Требования</span><span class="sxs-lookup"><span data-stu-id="33da8-138">Requirements</span></span>



| <span data-ttu-id="33da8-139">Требование</span><span class="sxs-lookup"><span data-stu-id="33da8-139">Requirement</span></span> | <span data-ttu-id="33da8-140">Значение</span><span class="sxs-lookup"><span data-stu-id="33da8-140">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="33da8-141">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="33da8-141">Minimum supported client</span></span><br/> | <span data-ttu-id="33da8-142">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="33da8-142">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="33da8-143">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="33da8-143">Minimum supported server</span></span><br/> | <span data-ttu-id="33da8-144">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="33da8-144">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="33da8-145">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="33da8-145">Namespace</span></span><br/>                | <span data-ttu-id="33da8-146">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="33da8-146">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="33da8-147">MOF</span><span class="sxs-lookup"><span data-stu-id="33da8-147">MOF</span></span><br/>                      | <dl> <span data-ttu-id="33da8-148"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="33da8-148"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="33da8-149">DLL</span><span class="sxs-lookup"><span data-stu-id="33da8-149">DLL</span></span><br/>                      | <dl> <span data-ttu-id="33da8-150"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="33da8-150"><dt>CIMWin32.dll</dt></span></span> </dl> |



 

