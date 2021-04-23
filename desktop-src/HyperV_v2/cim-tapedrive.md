---
description: Представляет возможности и управление ленточным накопителем.
ms.assetid: 8140fd9a-8a12-43b4-bc61-ec143e5d754c
title: Класс CIM_TapeDrive (Управление Hyper-V)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_TapeDrive
- CIM_TapeDrive.EOTWarningZoneSize
- CIM_TapeDrive.MaxPartitionCount
- CIM_TapeDrive.Padding
- CIM_TapeDrive.MaxRewindTime
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: b92360388b71abcb0b67d30fddea9b4f5ed7920f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105662814"
---
# <a name="cim_tapedrive-class-hyper-v-management"></a><span data-ttu-id="e10ef-103">Класс CIM_TapeDrive (Управление Hyper-V)</span><span class="sxs-lookup"><span data-stu-id="e10ef-103">CIM_TapeDrive class (Hyper-V management)</span></span>

<span data-ttu-id="e10ef-104">Представляет возможности и управление ленточным накопителем.</span><span class="sxs-lookup"><span data-stu-id="e10ef-104">Represents the capabilities and management of a tape drive.</span></span>

## <a name="syntax"></a><span data-ttu-id="e10ef-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="e10ef-105">Syntax</span></span>

``` syntax
[Abstract, Version("2.6.0"), UMLPackagePath("CIM::Device::StorageDevices")]
class CIM_TapeDrive : CIM_MediaAccessDevice
{
  uint32 EOTWarningZoneSize;
  uint32 MaxPartitionCount;
  uint32 Padding;
  uint64 MaxRewindTime;
};
```

## <a name="members"></a><span data-ttu-id="e10ef-106">Члены</span><span class="sxs-lookup"><span data-stu-id="e10ef-106">Members</span></span>

<span data-ttu-id="e10ef-107">Класс **CIM \_ TapeDrive** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="e10ef-107">The **CIM\_TapeDrive** class has these types of members:</span></span>

-   [<span data-ttu-id="e10ef-108">Свойства</span><span class="sxs-lookup"><span data-stu-id="e10ef-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="e10ef-109">Свойства</span><span class="sxs-lookup"><span data-stu-id="e10ef-109">Properties</span></span>

<span data-ttu-id="e10ef-110">Класс **CIM \_ TapeDrive** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="e10ef-110">The **CIM\_TapeDrive** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="e10ef-111">**еотварнингзонесизе**</span><span class="sxs-lookup"><span data-stu-id="e10ef-111">**EOTWarningZoneSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e10ef-112">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="e10ef-112">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="e10ef-113">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="e10ef-113">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e10ef-114">Квалификаторы: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes"), **Пунит** ("Byte")</span><span class="sxs-lookup"><span data-stu-id="e10ef-114">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("Bytes"), **PUnit** ("byte")</span></span>
</dt> </dl>

<span data-ttu-id="e10ef-115">Размер (в байтах) области, обозначенной как "конец ленты".</span><span class="sxs-lookup"><span data-stu-id="e10ef-115">The size, in bytes, of the area designated as "end of tape".</span></span> <span data-ttu-id="e10ef-116">Доступ в этой области приводит к возникновению предупреждения "конец ленты".</span><span class="sxs-lookup"><span data-stu-id="e10ef-116">Access in this area generates an "end of tape" warning.</span></span>

</dd> <dt>

<span data-ttu-id="e10ef-117">**MaxPartitionCount**</span><span class="sxs-lookup"><span data-stu-id="e10ef-117">**MaxPartitionCount**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e10ef-118">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="e10ef-118">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="e10ef-119">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="e10ef-119">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e10ef-120">Максимальное число разделов для ленточного накопителя.</span><span class="sxs-lookup"><span data-stu-id="e10ef-120">The maximum partition count for the tape drive.</span></span>

</dd> <dt>

<span data-ttu-id="e10ef-121">**максревиндтиме**</span><span class="sxs-lookup"><span data-stu-id="e10ef-121">**MaxRewindTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e10ef-122">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="e10ef-122">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="e10ef-123">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="e10ef-123">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e10ef-124">Квалификаторы: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("миллисекунды"), **Пунит** ("Second \* 10 ^-3")</span><span class="sxs-lookup"><span data-stu-id="e10ef-124">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("MilliSeconds"), **PUnit** ("second \* 10^-3")</span></span>
</dt> </dl>

<span data-ttu-id="e10ef-125">Время (в миллисекундах) перехода с наиболее физической точки на ленте к началу.</span><span class="sxs-lookup"><span data-stu-id="e10ef-125">The time, in milliseconds, to move from the most physically distant point on the tape to the beginning.</span></span>

</dd> <dt>

<span data-ttu-id="e10ef-126">**Заполнение**</span><span class="sxs-lookup"><span data-stu-id="e10ef-126">**Padding**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e10ef-127">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="e10ef-127">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="e10ef-128">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="e10ef-128">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e10ef-129">Квалификаторы: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes"), **Пунит** ("Byte")</span><span class="sxs-lookup"><span data-stu-id="e10ef-129">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("Bytes"), **PUnit** ("byte")</span></span>
</dt> </dl>

<span data-ttu-id="e10ef-130">Число байтов, вставленных между блоками на ленточном носителе.</span><span class="sxs-lookup"><span data-stu-id="e10ef-130">The number of bytes inserted between blocks on tape media.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="e10ef-131">Требования</span><span class="sxs-lookup"><span data-stu-id="e10ef-131">Requirements</span></span>



| <span data-ttu-id="e10ef-132">Требование</span><span class="sxs-lookup"><span data-stu-id="e10ef-132">Requirement</span></span> | <span data-ttu-id="e10ef-133">Значение</span><span class="sxs-lookup"><span data-stu-id="e10ef-133">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e10ef-134">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="e10ef-134">Minimum supported client</span></span><br/> | <span data-ttu-id="e10ef-135">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="e10ef-135">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="e10ef-136">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="e10ef-136">Minimum supported server</span></span><br/> | <span data-ttu-id="e10ef-137">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="e10ef-137">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="e10ef-138">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="e10ef-138">Namespace</span></span><br/>                | <span data-ttu-id="e10ef-139">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="e10ef-139">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="e10ef-140">MOF</span><span class="sxs-lookup"><span data-stu-id="e10ef-140">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e10ef-141"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="e10ef-141"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="e10ef-142">DLL</span><span class="sxs-lookup"><span data-stu-id="e10ef-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e10ef-143"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="e10ef-143"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="e10ef-144">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="e10ef-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e10ef-145">**\_МЕДИААКЦЕССДЕВИЦЕ CIM**</span><span class="sxs-lookup"><span data-stu-id="e10ef-145">**CIM\_MediaAccessDevice**</span></span>](cim-mediaaccessdevice.md)
</dt> </dl>

 

