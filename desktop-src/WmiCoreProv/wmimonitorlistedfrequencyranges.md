---
description: Список частотных диапазонов, поддерживаемых монитором.
ms.assetid: e4713650-5f8c-4808-8b4f-1d29c54ab4e3
title: Класс Вмимониторлистедфрекуенциранжес
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WmiMonitorListedFrequencyRanges
- WmiMonitorListedFrequencyRanges.Active
- WmiMonitorListedFrequencyRanges.InstanceName
- WmiMonitorListedFrequencyRanges.NumOfMonitorFreqRanges
- WmiMonitorListedFrequencyRanges.MonitorFreqRanges
api_type:
- DllExport
api_location:
- WmiProv.dll
ms.openlocfilehash: e13828f6d5e844147fc0b041617c8452c503ceef
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105712282"
---
# <a name="wmimonitorlistedfrequencyranges-class"></a><span data-ttu-id="7b805-103">Класс Вмимониторлистедфрекуенциранжес</span><span class="sxs-lookup"><span data-stu-id="7b805-103">WmiMonitorListedFrequencyRanges class</span></span>

<span data-ttu-id="7b805-104">Класс WMI **вмимониторлистедфрекуенциранжес** перечисляет диапазоны частот, поддерживаемые монитором.</span><span class="sxs-lookup"><span data-stu-id="7b805-104">The **WmiMonitorListedFrequencyRanges** WMI class lists the frequency ranges supported by the monitor.</span></span> <span data-ttu-id="7b805-105">Эти диапазоны находятся в определении видеовходов с расширенным расширенным отображаемым идентификационными данными (E-EDID), а также в файле INF Windows, содержащем данные драйвера устройства.</span><span class="sxs-lookup"><span data-stu-id="7b805-105">These ranges are found in Video Input Definition of Video Electronics Standard Association (VESA) Enhanced Extended Display Identification Data (E-EDID) block or in the Windows INF file that contains device driver data.</span></span>

## <a name="syntax"></a><span data-ttu-id="7b805-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="7b805-106">Syntax</span></span>

``` syntax
class WmiMonitorListedFrequencyRanges : MSMonitorClass
{
  boolean                  Active;
  string                   InstanceName;
  uint16                   NumOfMonitorFreqRanges;
  FrequencyRangeDescriptor MonitorFreqRanges[];
};
```

## <a name="members"></a><span data-ttu-id="7b805-107">Члены</span><span class="sxs-lookup"><span data-stu-id="7b805-107">Members</span></span>

<span data-ttu-id="7b805-108">Класс **вмимониторлистедфрекуенциранжес** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="7b805-108">The **WmiMonitorListedFrequencyRanges** class has these types of members:</span></span>

-   [<span data-ttu-id="7b805-109">Свойства</span><span class="sxs-lookup"><span data-stu-id="7b805-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="7b805-110">Свойства</span><span class="sxs-lookup"><span data-stu-id="7b805-110">Properties</span></span>

<span data-ttu-id="7b805-111">Класс **вмимониторлистедфрекуенциранжес** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="7b805-111">The **WmiMonitorListedFrequencyRanges** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="7b805-112">**Активен**</span><span class="sxs-lookup"><span data-stu-id="7b805-112">**Active**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7b805-113">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="7b805-113">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="7b805-114">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="7b805-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7b805-115">Указывает активный монитор.</span><span class="sxs-lookup"><span data-stu-id="7b805-115">Indicates the active monitor.</span></span>

</dd> <dt>

<span data-ttu-id="7b805-116">**InstanceName**</span><span class="sxs-lookup"><span data-stu-id="7b805-116">**InstanceName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7b805-117">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="7b805-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7b805-118">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="7b805-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7b805-119">Квалификаторы: **ключ**</span><span class="sxs-lookup"><span data-stu-id="7b805-119">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="7b805-120">Имя конкретного экземпляра монитора.</span><span class="sxs-lookup"><span data-stu-id="7b805-120">Name of the specific monitor instance.</span></span>

</dd> <dt>

<span data-ttu-id="7b805-121">**мониторфрекранжес**</span><span class="sxs-lookup"><span data-stu-id="7b805-121">**MonitorFreqRanges**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7b805-122">Тип данных: массив **фрекуенциранжедескриптор**</span><span class="sxs-lookup"><span data-stu-id="7b805-122">Data type: **FrequencyRangeDescriptor** array</span></span>
</dt> <dt>

<span data-ttu-id="7b805-123">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="7b805-123">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7b805-124">Список диапазонов частот монитора, представленных экземплярами класса [**фрекуенциранжедескриптор**](frequencyrangedescriptor.md) .</span><span class="sxs-lookup"><span data-stu-id="7b805-124">List of monitor frequency ranges represented by instances of the [**FrequencyRangeDescriptor**](frequencyrangedescriptor.md) class.</span></span>

</dd> <dt>

<span data-ttu-id="7b805-125">**нумофмониторфрекранжес**</span><span class="sxs-lookup"><span data-stu-id="7b805-125">**NumOfMonitorFreqRanges**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7b805-126">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="7b805-126">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="7b805-127">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="7b805-127">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7b805-128">Число перечисленных поддерживаемых диапазонов частоты мониторов.</span><span class="sxs-lookup"><span data-stu-id="7b805-128">Number of listed supported monitor frequency ranges.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="7b805-129">Требования</span><span class="sxs-lookup"><span data-stu-id="7b805-129">Requirements</span></span>



| <span data-ttu-id="7b805-130">Требование</span><span class="sxs-lookup"><span data-stu-id="7b805-130">Requirement</span></span> | <span data-ttu-id="7b805-131">Значение</span><span class="sxs-lookup"><span data-stu-id="7b805-131">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="7b805-132">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="7b805-132">Minimum supported client</span></span><br/> | <span data-ttu-id="7b805-133">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="7b805-133">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="7b805-134">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="7b805-134">Minimum supported server</span></span><br/> | <span data-ttu-id="7b805-135">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="7b805-135">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="7b805-136">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="7b805-136">Namespace</span></span><br/>                | <span data-ttu-id="7b805-137">Корневой \\ инструментарий WMI</span><span class="sxs-lookup"><span data-stu-id="7b805-137">Root\\wmi</span></span><br/>                                                                   |
| <span data-ttu-id="7b805-138">MOF</span><span class="sxs-lookup"><span data-stu-id="7b805-138">MOF</span></span><br/>                      | <dl> <span data-ttu-id="7b805-139"><dt>Вмикоре. mof</dt></span><span class="sxs-lookup"><span data-stu-id="7b805-139"><dt>WmiCore.mof</dt></span></span> </dl> |
| <span data-ttu-id="7b805-140">DLL</span><span class="sxs-lookup"><span data-stu-id="7b805-140">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7b805-141"><dt>WmiProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7b805-141"><dt>WmiProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7b805-142">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="7b805-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7b805-143">**мсмониторкласс**</span><span class="sxs-lookup"><span data-stu-id="7b805-143">**MSMonitorClass**</span></span>](msmonitorclass.md)
</dt> </dl>

 

 




