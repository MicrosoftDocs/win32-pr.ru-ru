---
description: Делает недействительным кэш имен пользователей с ИДЕНТИФИКАТОРом безопасности.
ms.assetid: 52f4a051-0caf-43c1-b190-c83c20e9fcf8
title: Дисккуотаконтрол. Инвалидатесиднамекаче, метод (Дсккуота. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DiskQuotaControl.InvalidateSidNameCache
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 4e7202c1293d32d55e12e88671ed9960d376f63e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103990956"
---
# <a name="diskquotacontrolinvalidatesidnamecache-method"></a>Дисккуотаконтрол. Инвалидатесиднамекаче, метод

Делает недействительным кэш имен пользователей с ИДЕНТИФИКАТОРом безопасности.

## <a name="syntax"></a>Синтаксис


```JScript
DiskQuotaControl.InvalidateSidNameCache()
```



## <a name="parameters"></a>Параметры

Этот метод не имеет параметров.

## <a name="return-value"></a>Возвращаемое значение

Этот метод не возвращает значение.

## <a name="remarks"></a>Примечания

Имена пользователей и связанные с ними идентификаторы безопасности хранятся в кэше. Вы можете очистить этот кэш, вызвав **инвалидатесиднамекаче**. Если впоследствии вы создадите новый объект пользователя, то эти сведения необходимо будет получить с контроллера домена, а кэш потребуется будет повторно установить.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional \[только классические приложения\]<br/>                                                    |
| Минимальная версия сервера<br/> | Windows 2000 Server \[только классические приложения\]<br/>                                                          |
| Заголовок<br/>                   | <dl> <dt>Дсккуота. h</dt> </dl>                         |
| DLL<br/>                      | <dl> <dt>Shell32.dll (версия 5,0 или более поздняя)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Объект Дисккуотаконтрол**](diskquotacontrol-object.md)
</dt> </dl>

 

 




