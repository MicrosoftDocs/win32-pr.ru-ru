---
title: Метод Disable класса SystemRestore
description: Отключает мониторинг на определенном диске.
ms.assetid: 2ad37dd4-7d80-4697-9dbb-abb329a34ff7
keywords:
- Отключить восстановление системы метода
- Отключение метода Restore системы, класс SystemRestore
- SystemRestore класс System Restore, метод Disable
topic_type:
- apiref
api_name:
- SystemRestore.Disable
api_location:
- Root\Default
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 19556833684aeab0cc126eff7aff0a258335c8e3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104136154"
---
# <a name="disable-method-of-the-systemrestore-class"></a>Метод Disable класса SystemRestore

Отключает мониторинг на определенном диске.

## <a name="syntax"></a>Синтаксис


```mof
uint32 Disable(
  [in] String Drive
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Диск* \[ окне\]
</dt> <dd>

Диск, который должен быть отключен. Строка диска должна иметь формат "C: \\ ". Если этот параметр является системным диском или пустой строкой (""), диски не отслеживаются.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Если метод выполнен успешно, возвращается значение S \_ . В противном случае метод возвращает один из кодов ошибок COM, определенных в файле WinError. h.

## <a name="examples"></a>Примеры


```VB
'Disable Method of the SystemRestore Class
'Disables monitoring on a particular drive.
Set Args = wscript.Arguments
If Args.Count() > 0 Then
    Drive = Args.item(0)
Else
    Drive = ""
End If

Set obj = GetObject("winmgmts:{impersonationLevel=impersonate}!root/default:SystemRestore")

If (obj.Disable(Drive)) = 0 Then
    wscript.Echo "Success"
Else 
    wscript.Echo "Failed"
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

[**SystemRestore**](systemrestore.md)
</dt> </dl>

 

 





