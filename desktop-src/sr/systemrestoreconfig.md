---
title: Класс Системрестореконфиг
description: Предоставляет свойства для управления частотой создания точек восстановления по расписанию и объемом дискового пространства, используемого на каждом диске.
ms.assetid: ed09e03f-8cc1-4923-8f39-bbe7d9a19b44
keywords:
- Восстановление системы класса Системрестореконфиг
- Восстановление системы класса Системрестореконфиг, описание
topic_type:
- apiref
api_name:
- SystemRestoreConfig
- SystemRestoreConfig.RPSessionInterval
- SystemRestoreConfig.RPGlobalInterval
- SystemRestoreConfig.RPLifeInterval
- SystemRestoreConfig.DiskPercent
api_location:
- Root\Default
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 58ded8a17cc4800e1aa2917ba7750c6c69434916
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104415720"
---
# <a name="systemrestoreconfig-class"></a><span data-ttu-id="40eb6-105">Класс Системрестореконфиг</span><span class="sxs-lookup"><span data-stu-id="40eb6-105">SystemRestoreConfig class</span></span>

<span data-ttu-id="40eb6-106">Предоставляет свойства для управления частотой создания точек восстановления по расписанию и объемом дискового пространства, используемого на каждом диске.</span><span class="sxs-lookup"><span data-stu-id="40eb6-106">Provides properties for controlling the frequency of scheduled restore point creation and the amount of disk space consumed on each drive.</span></span>

## <a name="syntax"></a><span data-ttu-id="40eb6-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="40eb6-107">Syntax</span></span>

``` syntax
class SystemRestoreConfig
{
  uint32 RPSessionInterval;
  uint32 RPGlobalInterval;
  uint32 RPLifeInterval;
  uint32 DiskPercent;
};
```

## <a name="members"></a><span data-ttu-id="40eb6-108">Члены</span><span class="sxs-lookup"><span data-stu-id="40eb6-108">Members</span></span>

<span data-ttu-id="40eb6-109">Класс **системрестореконфиг** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="40eb6-109">The **SystemRestoreConfig** class has these types of members:</span></span>

-   [<span data-ttu-id="40eb6-110">Свойства</span><span class="sxs-lookup"><span data-stu-id="40eb6-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="40eb6-111">Свойства</span><span class="sxs-lookup"><span data-stu-id="40eb6-111">Properties</span></span>

<span data-ttu-id="40eb6-112">Класс **системрестореконфиг** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="40eb6-112">The **SystemRestoreConfig** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="40eb6-113">**дискперцент**</span><span class="sxs-lookup"><span data-stu-id="40eb6-113">**DiskPercent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="40eb6-114">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="40eb6-114">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="40eb6-115">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="40eb6-115">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="40eb6-116">Максимальный объем дискового пространства на каждом диске, который может использоваться при восстановлении системы.</span><span class="sxs-lookup"><span data-stu-id="40eb6-116">The maximum amount of disk space on each drive that can be used by System Restore.</span></span> <span data-ttu-id="40eb6-117">Это значение указывается в процентах от общего пространства на диске.</span><span class="sxs-lookup"><span data-stu-id="40eb6-117">This value is specified as a percentage of the total drive space.</span></span> <span data-ttu-id="40eb6-118">Значение по умолчанию — 12 процентов.</span><span class="sxs-lookup"><span data-stu-id="40eb6-118">The default value is 12 percent.</span></span>

<span data-ttu-id="40eb6-119">**Windows Vista:** Получает значение из служба теневого копирования томов (VSS).</span><span class="sxs-lookup"><span data-stu-id="40eb6-119">**Windows Vista:** Receives a value from the Volume Shadow Copy Service (VSS).</span></span> <span data-ttu-id="40eb6-120">Это максимальный объем дискового пространства на каждом диске, который может использоваться при восстановлении системы.</span><span class="sxs-lookup"><span data-stu-id="40eb6-120">This this is the maximum amount of disk space on each drive that can be used by System Restore.</span></span> <span data-ttu-id="40eb6-121">Значение по умолчанию — 15% от общего места на диске или 30 процентов доступного свободного пространства, в зависимости от того, что меньше.</span><span class="sxs-lookup"><span data-stu-id="40eb6-121">The default value is 15 percent of the total drive space or 30 percent of the available free space, whichever is smaller.</span></span>

</dd> <dt>

<span data-ttu-id="40eb6-122">**рпглобалинтервал**</span><span class="sxs-lookup"><span data-stu-id="40eb6-122">**RPGlobalInterval**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="40eb6-123">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="40eb6-123">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="40eb6-124">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="40eb6-124">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="40eb6-125">Абсолютный интервал времени, в течение которого создаются запланированные системные контрольные точки.</span><span class="sxs-lookup"><span data-stu-id="40eb6-125">The absolute time interval at which scheduled system checkpoints are created, in seconds.</span></span> <span data-ttu-id="40eb6-126">Значение по умолчанию — 86 400 (24 часа).</span><span class="sxs-lookup"><span data-stu-id="40eb6-126">The default value is 86,400 (24 hours).</span></span>

<span data-ttu-id="40eb6-127">**Windows Vista:** Получает значение от планировщика заданий для восстановления системы.</span><span class="sxs-lookup"><span data-stu-id="40eb6-127">**Windows Vista:** Receives a value from the task scheduler for System Restore.</span></span> <span data-ttu-id="40eb6-128">Нуль, если задача отключена.</span><span class="sxs-lookup"><span data-stu-id="40eb6-128">Zero if the task is disabled.</span></span>

</dd> <dt>

<span data-ttu-id="40eb6-129">**рплифеинтервал**</span><span class="sxs-lookup"><span data-stu-id="40eb6-129">**RPLifeInterval**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="40eb6-130">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="40eb6-130">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="40eb6-131">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="40eb6-131">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="40eb6-132">Интервал времени, в течение которого сохраняются точки восстановления, в секундах.</span><span class="sxs-lookup"><span data-stu-id="40eb6-132">The time interval for which restore points are preserved, in seconds.</span></span> <span data-ttu-id="40eb6-133">Когда точка восстановления становится старше указанного интервала, она удаляется.</span><span class="sxs-lookup"><span data-stu-id="40eb6-133">When a restore point becomes older than this specified interval, it is deleted.</span></span> <span data-ttu-id="40eb6-134">По умолчанию предел возраста составляет 90 дней.</span><span class="sxs-lookup"><span data-stu-id="40eb6-134">The default age limit is 90 days.</span></span>

<span data-ttu-id="40eb6-135">**Windows Vista:** Получает значение **уинтмакс**.</span><span class="sxs-lookup"><span data-stu-id="40eb6-135">**Windows Vista:** Receives a value of **UINTMAX**.</span></span>

</dd> <dt>

<span data-ttu-id="40eb6-136">**рпсессионинтервал**</span><span class="sxs-lookup"><span data-stu-id="40eb6-136">**RPSessionInterval**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="40eb6-137">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="40eb6-137">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="40eb6-138">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="40eb6-138">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="40eb6-139">Интервал времени в секундах, в течение которого запланированные системные контрольные точки создаются в течение сеанса.</span><span class="sxs-lookup"><span data-stu-id="40eb6-139">The time interval at which scheduled system checkpoints are created during the session, in seconds.</span></span> <span data-ttu-id="40eb6-140">Значение по умолчанию равно нулю, что означает, что функция отключена.</span><span class="sxs-lookup"><span data-stu-id="40eb6-140">The default value is zero, indicating that the feature is turned off.</span></span>

<span data-ttu-id="40eb6-141">**Windows Vista:** Получает нуль, если восстановление системы отключено.</span><span class="sxs-lookup"><span data-stu-id="40eb6-141">**Windows Vista:** Receives zero if System Restore is disabled.</span></span>

</dd> </dl>

## <a name="examples"></a><span data-ttu-id="40eb6-142">Примеры</span><span class="sxs-lookup"><span data-stu-id="40eb6-142">Examples</span></span>

<span data-ttu-id="40eb6-143">Следующий образец кода не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="40eb6-143">The following sample code is not supported.</span></span> <span data-ttu-id="40eb6-144">Используйте программу командной строки Vssadmin.exe, чтобы изменить размер зарезервированного пространства на диске.</span><span class="sxs-lookup"><span data-stu-id="40eb6-144">Use the command-line tool Vssadmin.exe to change the size of reserved drive space.</span></span>

<span data-ttu-id="40eb6-145">**Windows XP:** Этот образец поддерживается.</span><span class="sxs-lookup"><span data-stu-id="40eb6-145">**Windows XP:** This sample is supported.</span></span>


```VB
'The SystemRestoreConfig class provides properties for controlling the frequency of 
'scheduled restore point creation and the amount of disk space consumed on each drive.

Set Args = wscript.Arguments
Set regSR = GetObject("winmgmts:{impersonationLevel=impersonate}!root/default:SystemRestoreConfig='SR'")

If Args.Count() = 0 Then
    Wscript.Echo "Usage: RegSR [RP{Session|Global|Life}Interval[=value]] [DiskPercent[=value]]"
Else    
For i = 0 To Args.Count() - 1
    Myarg = Args.Item(i)
    Pos = InStr(Myarg, "=")
    If Pos <> 0 Then
        Myarray = Split(Myarg, "=", -1, 1)
        myoption = Myarray(0)
        value = Myarray(1)
    Else 
        myoption = Myarg
    End If    
    If myoption = "RPSessionInterval" Then
        If Pos = 0 Then
            Wscript.Echo "RPSessionInterval = " & regSR.RPSessionInterval
        Else    
            regSR.RPSessionInterval = value
            regSR.Put_
        End If
    ElseIf myoption = "RPGlobalInterval" Then
        If Pos = 0 Then
            Wscript.Echo "RPGlobalInterval = " & regSR.RPGlobalInterval
        Else    
            regSR.RPGlobalInterval = value
            regSR.Put_
        End If
    ElseIf myoption = "RPLifeInterval" Then
        If Pos = 0 Then
            Wscript.Echo "RPLifeInterval = " & regSR.RPLifeInterval
        Else    
            regSR.RPLifeInterval = value
            regSR.Put_
        End If
    ElseIf myoption = "DiskPercent" Then
        If Pos = 0 Then
            Wscript.Echo "DiskPercent = " & regSR.DiskPercent
        Else    
            regSR.DiskPercent = value
            regSR.Put_
        End If
    End If
Next
End If
```



## <a name="requirements"></a><span data-ttu-id="40eb6-146">Требования</span><span class="sxs-lookup"><span data-stu-id="40eb6-146">Requirements</span></span>



| <span data-ttu-id="40eb6-147">Требование</span><span class="sxs-lookup"><span data-stu-id="40eb6-147">Requirement</span></span> | <span data-ttu-id="40eb6-148">Значение</span><span class="sxs-lookup"><span data-stu-id="40eb6-148">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="40eb6-149">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="40eb6-149">Minimum supported client</span></span><br/> | <span data-ttu-id="40eb6-150">Только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="40eb6-150">Windows XP \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="40eb6-151">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="40eb6-151">Minimum supported server</span></span><br/> | <span data-ttu-id="40eb6-152">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="40eb6-152">None supported</span></span><br/>                                                         |
| <span data-ttu-id="40eb6-153">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="40eb6-153">Namespace</span></span><br/>                | <span data-ttu-id="40eb6-154">Корневой каталог \\ по умолчанию</span><span class="sxs-lookup"><span data-stu-id="40eb6-154">Root\\Default</span></span><br/>                                                          |
| <span data-ttu-id="40eb6-155">MOF</span><span class="sxs-lookup"><span data-stu-id="40eb6-155">MOF</span></span><br/>                      | <dl> <span data-ttu-id="40eb6-156"><dt>SR. mof</dt></span><span class="sxs-lookup"><span data-stu-id="40eb6-156"><dt>Sr.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="40eb6-157">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="40eb6-157">See also</span></span>

<dl> <dt>

[<span data-ttu-id="40eb6-158">Точки восстановления</span><span class="sxs-lookup"><span data-stu-id="40eb6-158">Restore Points</span></span>](restore-points.md)
</dt> <dt>

[<span data-ttu-id="40eb6-159">Инструментарий управления Windows (WMI)</span><span class="sxs-lookup"><span data-stu-id="40eb6-159">Windows Management Instrumentation</span></span>](/windows/desktop/WmiSdk/wmi-start-page)
</dt> </dl>

 

