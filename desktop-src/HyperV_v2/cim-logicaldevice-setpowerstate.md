---
description: Задает состояние электропитания устройства. Использование этого метода является устаревшим. Вместо этого используйте метод SetPowerState в связанном классе Поверманажементсервице.
ms.assetid: 2f53a8bd-18a8-45aa-92ad-68a33b6a42ab
title: Метод SetPowerState класса CIM_LogicalDevice (Управление Hyper-V)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_LogicalDevice.SetPowerState
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: a29f71806747e6d63f53618acd09d472ac8bdea5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103999035"
---
# <a name="setpowerstate-method-of-the-cim_logicaldevice-class-hyper-v-management"></a><span data-ttu-id="d88ff-105">Метод SetPowerState класса CIM_LogicalDevice (Управление Hyper-V)</span><span class="sxs-lookup"><span data-stu-id="d88ff-105">SetPowerState method of the CIM_LogicalDevice class (Hyper-V management)</span></span>

<span data-ttu-id="d88ff-106">Задает состояние электропитания устройства.</span><span class="sxs-lookup"><span data-stu-id="d88ff-106">Sets the power state of the Device.</span></span> <span data-ttu-id="d88ff-107">Использование этого метода является устаревшим.</span><span class="sxs-lookup"><span data-stu-id="d88ff-107">The use of this method has been deprecated.</span></span> <span data-ttu-id="d88ff-108">Вместо этого используйте метод **SetPowerState** в связанном классе **поверманажементсервице** .</span><span class="sxs-lookup"><span data-stu-id="d88ff-108">Instead, use the **SetPowerState** method in the associated **PowerManagementService** class.</span></span>

## <a name="syntax"></a><span data-ttu-id="d88ff-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="d88ff-109">Syntax</span></span>


```mof
uint32 SetPowerState(
  [in] uint16   PowerState,
  [in] datetime Time
);
```



## <a name="parameters"></a><span data-ttu-id="d88ff-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="d88ff-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d88ff-111">*PowerState* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="d88ff-111">*PowerState* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d88ff-112">Заданное состояние питания.</span><span class="sxs-lookup"><span data-stu-id="d88ff-112">The power state to set.</span></span>

<dt>

<span id="Full_Power"></span><span id="full_power"></span><span id="FULL_POWER"></span>

<span data-ttu-id="d88ff-113">**Полная мощность** (1)</span><span class="sxs-lookup"><span data-stu-id="d88ff-113">**Full Power** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

<span data-ttu-id="d88ff-114">Энергосбережение **— режим низкого энергопотребления** (2)</span><span class="sxs-lookup"><span data-stu-id="d88ff-114">**Power Save - Low Power Mode** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

<span data-ttu-id="d88ff-115">Энергосбережение **— ждущий режим** (3)</span><span class="sxs-lookup"><span data-stu-id="d88ff-115">**Power Save - Standby** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Other"></span><span id="power_save_-_other"></span><span id="POWER_SAVE_-_OTHER"></span>

<span data-ttu-id="d88ff-116">**Энергосбережение — другие** (4)</span><span class="sxs-lookup"><span data-stu-id="d88ff-116">**Power Save - Other** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

<span data-ttu-id="d88ff-117">**Цикл электропитания** (5)</span><span class="sxs-lookup"><span data-stu-id="d88ff-117">**Power Cycle** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>

<span data-ttu-id="d88ff-118">**Выключение питания** (6)</span><span class="sxs-lookup"><span data-stu-id="d88ff-118">**Power Off** (6)</span></span>


</dt> <dd></dd> </dl> </dd> <dt>

<span data-ttu-id="d88ff-119">*Время* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="d88ff-119">*Time* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d88ff-120">Время указывает, когда должно быть установлено состояние электропитания: как обычное значение даты-времени или как значение интервала (где интервал начинается при получении вызова метода).</span><span class="sxs-lookup"><span data-stu-id="d88ff-120">Time indicates when the power state should be set, either as a regular date-time value or as an interval value (where the interval begins when the method invocation is received).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d88ff-121">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="d88ff-121">Return value</span></span>

<span data-ttu-id="d88ff-122">Возвращает значение 0 в случае успешного выполнения; в противном случае возвращает ошибку.</span><span class="sxs-lookup"><span data-stu-id="d88ff-122">Returns a 0 on success; otherwise, returns an error.</span></span>

## <a name="requirements"></a><span data-ttu-id="d88ff-123">Требования</span><span class="sxs-lookup"><span data-stu-id="d88ff-123">Requirements</span></span>



| <span data-ttu-id="d88ff-124">Требование</span><span class="sxs-lookup"><span data-stu-id="d88ff-124">Requirement</span></span> | <span data-ttu-id="d88ff-125">Значение</span><span class="sxs-lookup"><span data-stu-id="d88ff-125">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d88ff-126">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="d88ff-126">Minimum supported client</span></span><br/> | <span data-ttu-id="d88ff-127">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="d88ff-127">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="d88ff-128">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="d88ff-128">Minimum supported server</span></span><br/> | <span data-ttu-id="d88ff-129">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="d88ff-129">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="d88ff-130">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="d88ff-130">Namespace</span></span><br/>                | <span data-ttu-id="d88ff-131">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="d88ff-131">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="d88ff-132">MOF</span><span class="sxs-lookup"><span data-stu-id="d88ff-132">MOF</span></span><br/>                      | <dl> <span data-ttu-id="d88ff-133"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="d88ff-133"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="d88ff-134">DLL</span><span class="sxs-lookup"><span data-stu-id="d88ff-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d88ff-135"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="d88ff-135"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="d88ff-136">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="d88ff-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d88ff-137">**Модель \_ CIM**</span><span class="sxs-lookup"><span data-stu-id="d88ff-137">**CIM\_LogicalDevice**</span></span>](cim-logicaldevice.md)
</dt> </dl>

 

 




