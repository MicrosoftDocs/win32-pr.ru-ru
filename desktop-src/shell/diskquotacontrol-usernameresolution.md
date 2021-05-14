---
description: Задает или возвращает значение, которое управляет способом разрешения идентификатора безопасности (SID) пользователя в имена пользователей.
title: Дисккуотаконтрол. Усернамересолутион, свойство
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DiskQuotaControl.UserNameResolution
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: dc936421-e66d-4762-912a-c586f9cdace4
ms.openlocfilehash: 169f4db6e135392e9548767520f6d2b0bd2d527c
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/12/2021
ms.locfileid: "109841465"
---
# <a name="diskquotacontrolusernameresolution-property"></a>Дисккуотаконтрол. Усернамересолутион, свойство

Задает или возвращает значение, которое управляет способом разрешения идентификатора безопасности (SID) пользователя в имена пользователей.

Это свойство доступно для чтения и записи.

## <a name="syntax"></a>Синтаксис


```JScript
iUserNameResolution = DiskQuotaControl.UserNameResolution
DiskQuotaControl.UserNameResolution = iUserNameResolution
```



## <a name="property-value"></a>Значение свойства

Этому свойству можно присвоить одно из следующих значений.



| Тип разрешения | Значение | Описание                                                                                                                                              |
|-----------------|-------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| дкресолвеноне   | 0     | Не разрешать сведения о имени пользователя.                                                                                                                    |
| дкресолвесинк   | 1     | Подождите, пока разрешаются сведения о имени.                                                                                                                   |
| дкресолвеасинк  | 2     | Не следует ждать при разрешении сведений о имени. Событие [**онусернамечанжед**](diskquotacontrol-onusernamechanged.md) срабатывает при разрешении имени. |



 

## <a name="remarks"></a>Remarks

Это свойство влияет на перечисление объектов [**дидисккуотаусер**](didiskquotauser-object.md) , а также на методы [**adduser**](diskquotacontrol-adduser.md) и [**финдусер**](diskquotacontrol-finduser.md) .

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional \[только классические приложения\]<br/>                                                    |
| Минимальная версия сервера<br/> | Windows 2000 Server \[только классические приложения\]<br/>                                                          |
| DLL<br/>                      | <dl> <dt>Shell32.dll (версия 5,0 или более поздняя)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Объект Дисккуотаконтрол**](diskquotacontrol-object.md)
</dt> </dl>

 

 




