---
description: Список поддерживаемых режимов исходного кода для видеомонитора в дескрипторе монитора (при наличии).
ms.assetid: cca59d28-bd93-4df2-989e-0516dd8eae83
title: Класс Вмимониторлистедсуппортедсаурцемодес
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WmiMonitorListedSupportedSourceModes
- WmiMonitorListedSupportedSourceModes.Active
- WmiMonitorListedSupportedSourceModes.InstanceName
- WmiMonitorListedSupportedSourceModes.NumOfMonitorSourceModes
- WmiMonitorListedSupportedSourceModes.PreferredMonitorSourceModeIndex
- WmiMonitorListedSupportedSourceModes.MonitorSourceModes
api_type:
- DllExport
api_location:
- WmiProv.dll
ms.openlocfilehash: 35cb4b3548654c72686a8843cc697f109f661d87
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105712281"
---
# <a name="wmimonitorlistedsupportedsourcemodes-class"></a><span data-ttu-id="faf4d-103">Класс Вмимониторлистедсуппортедсаурцемодес</span><span class="sxs-lookup"><span data-stu-id="faf4d-103">WmiMonitorListedSupportedSourceModes class</span></span>

<span data-ttu-id="faf4d-104">**Вмимониторлистедсуппортедсаурцемодес** перечисляет поддерживаемые режимы источника для видеомонитора в дескрипторе монитора, если таковые имеются.</span><span class="sxs-lookup"><span data-stu-id="faf4d-104">The **WmiMonitorListedSupportedSourceModes** lists the supported source modes for a video monitor in its monitor descriptor, if any exist.</span></span> <span data-ttu-id="faf4d-105">Для мониторов, не имеющих описания, этот список режимов создается на основе типа монитора, как указано в драйвере монитора шины.</span><span class="sxs-lookup"><span data-stu-id="faf4d-105">For monitors that have no description, this list of modes is generated based on the type of monitor, as specified by the monitor bus driver.</span></span>

## <a name="syntax"></a><span data-ttu-id="faf4d-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="faf4d-106">Syntax</span></span>

``` syntax
class WmiMonitorListedSupportedSourceModes : MSMonitorClass
{
  boolean             Active;
  string              InstanceName;
  uint16              NumOfMonitorSourceModes;
  uint16              PreferredMonitorSourceModeIndex;
  VideoModeDescriptor MonitorSourceModes[];
};
```

## <a name="members"></a><span data-ttu-id="faf4d-107">Члены</span><span class="sxs-lookup"><span data-stu-id="faf4d-107">Members</span></span>

<span data-ttu-id="faf4d-108">Класс **вмимониторлистедсуппортедсаурцемодес** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="faf4d-108">The **WmiMonitorListedSupportedSourceModes** class has these types of members:</span></span>

-   [<span data-ttu-id="faf4d-109">Свойства</span><span class="sxs-lookup"><span data-stu-id="faf4d-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="faf4d-110">Свойства</span><span class="sxs-lookup"><span data-stu-id="faf4d-110">Properties</span></span>

<span data-ttu-id="faf4d-111">Класс **вмимониторлистедсуппортедсаурцемодес** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="faf4d-111">The **WmiMonitorListedSupportedSourceModes** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="faf4d-112">**Активен**</span><span class="sxs-lookup"><span data-stu-id="faf4d-112">**Active**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="faf4d-113">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="faf4d-113">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="faf4d-114">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="faf4d-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="faf4d-115">Указывает активный монитор.</span><span class="sxs-lookup"><span data-stu-id="faf4d-115">Indicates the active monitor.</span></span>

</dd> <dt>

<span data-ttu-id="faf4d-116">**InstanceName**</span><span class="sxs-lookup"><span data-stu-id="faf4d-116">**InstanceName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="faf4d-117">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="faf4d-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="faf4d-118">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="faf4d-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="faf4d-119">Квалификаторы: **ключ**</span><span class="sxs-lookup"><span data-stu-id="faf4d-119">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="faf4d-120">Имя конкретного экземпляра монитора.</span><span class="sxs-lookup"><span data-stu-id="faf4d-120">Name of the specific monitor instance.</span></span>

</dd> <dt>

<span data-ttu-id="faf4d-121">**мониторсаурцемодес**</span><span class="sxs-lookup"><span data-stu-id="faf4d-121">**MonitorSourceModes**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="faf4d-122">Тип данных: массив **видеомодедескриптор**</span><span class="sxs-lookup"><span data-stu-id="faf4d-122">Data type: **VideoModeDescriptor** array</span></span>
</dt> <dt>

<span data-ttu-id="faf4d-123">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="faf4d-123">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="faf4d-124">Перечисляет режимы работы с исходным кодом, представленные экземплярами класса [**видеомодедескриптор**](videomodedescriptor.md) .</span><span class="sxs-lookup"><span data-stu-id="faf4d-124">Lists monitor source modes represented by instances of the [**VideoModeDescriptor**](videomodedescriptor.md) class.</span></span>

</dd> <dt>

<span data-ttu-id="faf4d-125">**нумофмониторсаурцемодес**</span><span class="sxs-lookup"><span data-stu-id="faf4d-125">**NumOfMonitorSourceModes**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="faf4d-126">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="faf4d-126">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="faf4d-127">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="faf4d-127">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="faf4d-128">Число перечисленных поддерживаемых режимов отслеживания источника.</span><span class="sxs-lookup"><span data-stu-id="faf4d-128">Number of listed supported monitor source mode.</span></span>

</dd> <dt>

<span data-ttu-id="faf4d-129">**преферредмониторсаурцемодеиндекс**</span><span class="sxs-lookup"><span data-stu-id="faf4d-129">**PreferredMonitorSourceModeIndex**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="faf4d-130">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="faf4d-130">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="faf4d-131">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="faf4d-131">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="faf4d-132">Индекс основного режима источника монитора.</span><span class="sxs-lookup"><span data-stu-id="faf4d-132">Preferred monitor source mode index.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="faf4d-133">Требования</span><span class="sxs-lookup"><span data-stu-id="faf4d-133">Requirements</span></span>



| <span data-ttu-id="faf4d-134">Требование</span><span class="sxs-lookup"><span data-stu-id="faf4d-134">Requirement</span></span> | <span data-ttu-id="faf4d-135">Значение</span><span class="sxs-lookup"><span data-stu-id="faf4d-135">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="faf4d-136">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="faf4d-136">Minimum supported client</span></span><br/> | <span data-ttu-id="faf4d-137">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="faf4d-137">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="faf4d-138">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="faf4d-138">Minimum supported server</span></span><br/> | <span data-ttu-id="faf4d-139">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="faf4d-139">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="faf4d-140">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="faf4d-140">Namespace</span></span><br/>                | <span data-ttu-id="faf4d-141">Корневой \\ инструментарий WMI</span><span class="sxs-lookup"><span data-stu-id="faf4d-141">Root\\wmi</span></span><br/>                                                                   |
| <span data-ttu-id="faf4d-142">MOF</span><span class="sxs-lookup"><span data-stu-id="faf4d-142">MOF</span></span><br/>                      | <dl> <span data-ttu-id="faf4d-143"><dt>Вмикоре. mof</dt></span><span class="sxs-lookup"><span data-stu-id="faf4d-143"><dt>WmiCore.mof</dt></span></span> </dl> |
| <span data-ttu-id="faf4d-144">DLL</span><span class="sxs-lookup"><span data-stu-id="faf4d-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="faf4d-145"><dt>WmiProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="faf4d-145"><dt>WmiProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="faf4d-146">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="faf4d-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="faf4d-147">**мсмониторкласс**</span><span class="sxs-lookup"><span data-stu-id="faf4d-147">**MSMonitorClass**</span></span>](msmonitorclass.md)
</dt> </dl>

 

 




