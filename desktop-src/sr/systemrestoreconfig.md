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
# <a name="systemrestoreconfig-class"></a>Класс Системрестореконфиг

Предоставляет свойства для управления частотой создания точек восстановления по расписанию и объемом дискового пространства, используемого на каждом диске.

## <a name="syntax"></a>Синтаксис

``` syntax
class SystemRestoreConfig
{
  uint32 RPSessionInterval;
  uint32 RPGlobalInterval;
  uint32 RPLifeInterval;
  uint32 DiskPercent;
};
```

## <a name="members"></a>Члены

Класс **системрестореконфиг** имеет следующие типы членов:

-   [Свойства](#properties)

### <a name="properties"></a>Свойства

Класс **системрестореконфиг** имеет следующие свойства.

<dl> <dt>

**дискперцент**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Максимальный объем дискового пространства на каждом диске, который может использоваться при восстановлении системы. Это значение указывается в процентах от общего пространства на диске. Значение по умолчанию — 12 процентов.

**Windows Vista:** Получает значение из служба теневого копирования томов (VSS). Это максимальный объем дискового пространства на каждом диске, который может использоваться при восстановлении системы. Значение по умолчанию — 15% от общего места на диске или 30 процентов доступного свободного пространства, в зависимости от того, что меньше.

</dd> <dt>

**рпглобалинтервал**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Абсолютный интервал времени, в течение которого создаются запланированные системные контрольные точки. Значение по умолчанию — 86 400 (24 часа).

**Windows Vista:** Получает значение от планировщика заданий для восстановления системы. Нуль, если задача отключена.

</dd> <dt>

**рплифеинтервал**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Интервал времени, в течение которого сохраняются точки восстановления, в секундах. Когда точка восстановления становится старше указанного интервала, она удаляется. По умолчанию предел возраста составляет 90 дней.

**Windows Vista:** Получает значение **уинтмакс**.

</dd> <dt>

**рпсессионинтервал**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Интервал времени в секундах, в течение которого запланированные системные контрольные точки создаются в течение сеанса. Значение по умолчанию равно нулю, что означает, что функция отключена.

**Windows Vista:** Получает нуль, если восстановление системы отключено.

</dd> </dl>

## <a name="examples"></a>Примеры

Следующий образец кода не поддерживается. Используйте программу командной строки Vssadmin.exe, чтобы изменить размер зарезервированного пространства на диске.

**Windows XP:** Этот образец поддерживается.


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



## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows XP\]<br/>                                       |
| Минимальная версия сервера<br/> | Ни одна версия не поддерживается<br/>                                                         |
| Пространство имен<br/>                | Корневой каталог \\ по умолчанию<br/>                                                          |
| MOF<br/>                      | <dl> <dt>SR. mof</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Точки восстановления](restore-points.md)
</dt> <dt>

[Инструментарий управления Windows (WMI)](/windows/desktop/WmiSdk/wmi-start-page)
</dt> </dl>

 

