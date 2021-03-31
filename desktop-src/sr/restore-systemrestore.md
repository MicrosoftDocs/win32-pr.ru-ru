---
title: Метод Restore класса SystemRestore
description: Инициирует восстановление системы.
ms.assetid: ca4aa97b-fa59-407d-b127-951d46932c33
keywords:
- Восстановление системы метода восстановления
- Восстановление системы метода Restore, класс SystemRestore
- SystemRestore класс System Restore, метод Restore
topic_type:
- apiref
api_name:
- SystemRestore.Restore
api_location:
- Root\\Default
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f8b7747b710801718d9b169c8999c51dd30cefde
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103801384"
---
# <a name="restore-method-of-the-systemrestore-class"></a>Метод Restore класса SystemRestore

Инициирует восстановление системы. Вызывающий объект должен принудительно выполнить перезагрузку системы. Фактическое восстановление происходит во время перезагрузки.

## <a name="syntax"></a>Синтаксис


```mof
uint32 Restore(
  [in] uint32 SequenceNumber
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*SequenceNumber* \[ окне\]
</dt> <dd>

Порядковый номер точки восстановления. Чтобы определить порядковый номер для определенной точки восстановления, перечислите все точки восстановления в системе.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Если метод выполнен успешно, возвращается значение S \_ . В противном случае метод возвращает один из кодов ошибок COM, определенных в файле WinError. h.

## <a name="examples"></a>Примеры


```VB
'Restore Method of the SystemRestore Class
'Initiates a system restore. The caller must 
'force a system reboot. The actual restoration 
'occurs during the reboot.
Set Args = wscript.Arguments
RpNum = Args.item(0)
Set obj = GetObject("winmgmts:{impersonationLevel=impersonate}!root/default:SystemRestore")
if obj.Restore(RpNum) <> 0 Then
    wscript.Echo "Restore failed"
End If
Set OpSysSet = GetObject("winmgmts:{(Shutdown)}//./root/cimv2").ExecQuery("select * from Win32_OperatingSystem where Primary=true")
for each OpSys in OpSysSet
    OpSys.Reboot()
next
```



## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows XP\]<br/>                                       |
| Минимальная версия сервера<br/> | Ни одна версия не поддерживается<br/>                                                         |
| Пространство имен<br/>                | Корневой каталог \\ \\ по умолчанию<br/>                                                        |
| MOF<br/>                      | <dl> <dt>SR. mof</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**SystemRestore**](systemrestore.md)
</dt> </dl>

 

 





