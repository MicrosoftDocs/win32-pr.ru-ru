---
title: Enable, метод класса SystemRestore
description: Включает наблюдение на определенном диске.
ms.assetid: f3140f6d-d190-46a4-8587-c2e928ac8ecf
keywords:
- Включить восстановление системы метода
- Включить восстановление системы методов, класс SystemRestore
- SystemRestore класс System Restore, Enable, метод
topic_type:
- apiref
api_name:
- SystemRestore.Enable
api_location:
- Root\Default
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 090aa01b4028a7146ea1d7f271ba4390f43ca260
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105710503"
---
# <a name="enable-method-of-the-systemrestore-class"></a>Enable, метод класса SystemRestore

Включает наблюдение на определенном диске.

## <a name="syntax"></a>Синтаксис


```mof
uint32 Enable(
  [in] String Drive
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Диск* \[ окне\]
</dt> <dd>

Диск, который должен быть включен. Строка диска должна иметь формат "C: \\ ". Если этот параметр является системным диском или пустой строкой (""), отслеживаются все диски.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Если метод выполнен успешно, возвращается значение S \_ . В противном случае метод возвращает один из кодов ошибок COM, определенных в файле WinError. h.

## <a name="remarks"></a>Комментарии

Метод **Enable** не ждет, пока наблюдение будет включено полностью перед возвратом, так как это может занять некоторое время. Вместо этого он возвращается сразу после запуска службы восстановления системы и драйвера фильтра.

Чтобы включить восстановление системы на несистемном диске, необходимо сначала включить функцию восстановления системы на системном диске.

Этот метод завершает работу неудачно в режиме безопасного режима.

## <a name="examples"></a>Примеры


```VB
'Enable Method of the SystemRestore Class
'Enables monitoring on a particular drive.

Set Args = wscript.Arguments
If Args.Count() > 0 Then
    Drive = Args.item(0)
Else 
    Drive = ""
End If

Set obj = GetObject("winmgmts:{impersonationLevel=impersonate}!root/default:SystemRestore")
If (obj.Enable(Drive)) = 0 Then
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

 

 





