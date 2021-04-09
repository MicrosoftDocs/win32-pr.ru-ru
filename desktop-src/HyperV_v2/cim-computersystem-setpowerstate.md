---
description: Задает состояние электропитания компьютера. Использование этого метода является устаревшим. Вместо этого используйте метод SetPowerState в связанном классе Поверманажементсервице.
ms.assetid: c2196f35-f687-4d82-a068-f8499f77473a
title: Метод SetPowerState класса CIM_ComputerSystem
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ComputerSystem.SetPowerState
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 9c9e264e8ec62c1e49e92226d1abc8ac902c0b2b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104080934"
---
# <a name="setpowerstate-method-of-the-cim_computersystem-class"></a><span data-ttu-id="b2b92-105">Метод SetPowerState \_ класса COMPUTERSYSTEM CIM</span><span class="sxs-lookup"><span data-stu-id="b2b92-105">SetPowerState method of the CIM\_ComputerSystem class</span></span>

<span data-ttu-id="b2b92-106">Задает состояние электропитания компьютера.</span><span class="sxs-lookup"><span data-stu-id="b2b92-106">Sets the power state of the computer.</span></span> <span data-ttu-id="b2b92-107">Использование этого метода является устаревшим.</span><span class="sxs-lookup"><span data-stu-id="b2b92-107">The use of this method has been deprecated.</span></span> <span data-ttu-id="b2b92-108">Вместо этого используйте метод **SetPowerState** в связанном классе **поверманажементсервице** .</span><span class="sxs-lookup"><span data-stu-id="b2b92-108">Instead, use the **SetPowerState** method in the associated **PowerManagementService** class.</span></span>

## <a name="syntax"></a><span data-ttu-id="b2b92-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="b2b92-109">Syntax</span></span>


```mof
uint32 SetPowerState(
  [in] uint32   PowerState,
  [in] datetime Time
);
```



## <a name="parameters"></a><span data-ttu-id="b2b92-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="b2b92-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b2b92-111">*PowerState* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="b2b92-111">*PowerState* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b2b92-112">Требуемое состояние для компьютерной системы.</span><span class="sxs-lookup"><span data-stu-id="b2b92-112">The desired state for the computer system.</span></span>

<dt>

<span id="Full_Power"></span><span id="full_power"></span><span id="FULL_POWER"></span>

<span data-ttu-id="b2b92-113">**Полная мощность** (1)</span><span class="sxs-lookup"><span data-stu-id="b2b92-113">**Full Power** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

<span data-ttu-id="b2b92-114">Энергосбережение **— режим низкого энергопотребления** (2)</span><span class="sxs-lookup"><span data-stu-id="b2b92-114">**Power Save - Low Power Mode** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

<span data-ttu-id="b2b92-115">Энергосбережение **— ждущий режим** (3)</span><span class="sxs-lookup"><span data-stu-id="b2b92-115">**Power Save - Standby** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Other"></span><span id="power_save_-_other"></span><span id="POWER_SAVE_-_OTHER"></span>

<span data-ttu-id="b2b92-116">**Энергосбережение — другие** (4)</span><span class="sxs-lookup"><span data-stu-id="b2b92-116">**Power Save - Other** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

<span data-ttu-id="b2b92-117">**Цикл электропитания** (5)</span><span class="sxs-lookup"><span data-stu-id="b2b92-117">**Power Cycle** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>

<span data-ttu-id="b2b92-118">**Выключение питания** (6)</span><span class="sxs-lookup"><span data-stu-id="b2b92-118">**Power Off** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Hibernate"></span><span id="hibernate"></span><span id="HIBERNATE"></span>

<span data-ttu-id="b2b92-119">**Режим гибернации** (7)</span><span class="sxs-lookup"><span data-stu-id="b2b92-119">**Hibernate** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Soft_Off"></span><span id="soft_off"></span><span id="SOFT_OFF"></span>

<span data-ttu-id="b2b92-120">**Мягкое отключение** (8)</span><span class="sxs-lookup"><span data-stu-id="b2b92-120">**Soft Off** (8)</span></span>


</dt> <dd></dd> </dl> </dd> <dt>

<span data-ttu-id="b2b92-121">*Время* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="b2b92-121">*Time* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b2b92-122">Время указывает, когда должно быть установлено состояние электропитания: как обычное значение даты-времени или как значение интервала (где интервал начинается при получении вызова метода).</span><span class="sxs-lookup"><span data-stu-id="b2b92-122">Time indicates when the power state should be set, either as a regular date-time value or as an interval value (where the interval begins when the method invocation is received).</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="b2b92-123">Требования</span><span class="sxs-lookup"><span data-stu-id="b2b92-123">Requirements</span></span>



| <span data-ttu-id="b2b92-124">Требование</span><span class="sxs-lookup"><span data-stu-id="b2b92-124">Requirement</span></span> | <span data-ttu-id="b2b92-125">Значение</span><span class="sxs-lookup"><span data-stu-id="b2b92-125">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b2b92-126">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="b2b92-126">Minimum supported client</span></span><br/> | <span data-ttu-id="b2b92-127">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="b2b92-127">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="b2b92-128">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="b2b92-128">Minimum supported server</span></span><br/> | <span data-ttu-id="b2b92-129">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="b2b92-129">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="b2b92-130">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="b2b92-130">Namespace</span></span><br/>                | <span data-ttu-id="b2b92-131">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="b2b92-131">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="b2b92-132">MOF</span><span class="sxs-lookup"><span data-stu-id="b2b92-132">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b2b92-133"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="b2b92-133"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="b2b92-134">DLL</span><span class="sxs-lookup"><span data-stu-id="b2b92-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b2b92-135"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="b2b92-135"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="b2b92-136">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="b2b92-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b2b92-137">**CIM \_ ComputerSystem**</span><span class="sxs-lookup"><span data-stu-id="b2b92-137">**CIM\_ComputerSystem**</span></span>](cim-computersystem.md)
</dt> </dl>

 

 




