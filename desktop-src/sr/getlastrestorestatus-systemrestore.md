---
title: Метод Жетластресторестатус класса SystemRestore
description: Возвращает состояние последнего восстановления системы.
ms.assetid: 03f9fd71-9f20-428e-bdca-4692e838581a
keywords:
- Восстановление системы метода Жетластресторестатус
- Восстановление системы метода Жетластресторестатус, класс SystemRestore
- Восстановление системы класса SystemRestore, метод Жетластресторестатус
topic_type:
- apiref
api_name:
- SystemRestore.GetLastRestoreStatus
api_location:
- Root\Default
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8cd1ef0e62f7874bb92f3c8e9ecec7b62a1b3ff3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105701021"
---
# <a name="getlastrestorestatus-method-of-the-systemrestore-class"></a>Метод Жетластресторестатус класса SystemRestore

Возвращает состояние последнего восстановления системы.

## <a name="syntax"></a>Синтаксис


```mof
uint32 GetLastRestoreStatus();
```



## <a name="parameters"></a>Параметры

Этот метод не имеет параметров.

## <a name="return-value"></a>Возвращаемое значение

Метод возвращает одно из следующих значений состояния.



| Возвращаемое значение                                                                 | Описание                                  |
|------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <dt>0</dt> </dl> | Последнее восстановление завершилось сбоем.<br/>          |
| <dl> <dt>1</dt> </dl> | Последнее восстановление прошло успешно.<br/>  |
| <dl> <dt>2</dt> </dl> | Последнее восстановление было прервано.<br/> |



 

## <a name="examples"></a>Примеры


```VB
'GetLastRestoreStatus Method of the SystemRestore Class
'Retrieves the status of the last system restore.
Set obj = GetObject("winmgmts:{impersonationLevel=impersonate}!root/default:SystemRestore")
stat = obj.GetLastRestoreStatus()
If stat = 0 Then
    wscript.Echo "Failed"
ElseIf stat = 1 Then 
    wscript.Echo "Success"
ElseIf stat = 2 Then
    wscript.Echo "Interrrupted"
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

 

 





