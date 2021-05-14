---
description: Очищает кэшированные данные пользователя объекта.
title: Дидисккуотаусер. unvalidate, метод
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DIDiskQuotaUser.Invalidate
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: e0ffd5b7-db1d-40a4-810a-ff43549b0c9b
ms.openlocfilehash: 9f8ad77c9697ed5d284cf782f431ec59b38ca415
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/12/2021
ms.locfileid: "109843275"
---
# <a name="didiskquotauserinvalidate-method"></a>Дидисккуотаусер. unvalidate, метод

Очищает кэшированные данные пользователя объекта.

## <a name="syntax"></a>Синтаксис


```JScript
DIDiskQuotaUser.Invalidate()
```



## <a name="parameters"></a>Параметры

Этот метод не имеет параметров.

## <a name="return-value"></a>Возвращаемое значение

Этот метод не возвращает значение.

## <a name="remarks"></a>Remarks

Этот метод очищает сведения о пользователе, хранящиеся в кэше объекта. При следующем запросе данных, относящихся к квотам, объект получает сведения из тома NTFS и обновляет кэш.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional \[только классические приложения\]<br/>                                                    |
| Минимальная версия сервера<br/> | Windows 2000 Server \[только классические приложения\]<br/>                                                          |
| DLL<br/>                      | <dl> <dt>Shell32.dll (версия 5,0 или более поздняя)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Объект Дидисккуотаусер**](didiskquotauser-object.md)
</dt> </dl>

 

 




