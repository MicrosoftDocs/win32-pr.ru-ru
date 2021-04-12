---
description: Возвращает понятное имя профиля.
ms.assetid: db2f8229-ce43-4608-af3f-a06011b4fac0
title: Метод Исканпрофиле::-Name (Сканпрофиле. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IScanProfile.GetName
api_type:
- COM
api_location:
- Scanprofile.h
ms.openlocfilehash: 81d1a0293802ea137f4e23b4571d32fd3d54ee44
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104263311"
---
# <a name="iscanprofilegetname-method"></a>Метод Исканпрофиле:: Name

Возвращает понятное имя профиля.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT GetName(
  [out] BSTR *pbstrName
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*пбстрнаме* \[ заполняет\]
</dt> <dd>

Тип: **BSTR \** _

Понятное имя профиля.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: _ *HRESULT**

Если этот метод завершается успешно, возвращается значение **S \_ ОК**. В противном случае возвращается код ошибки **HRESULT** .

## <a name="remarks"></a>Комментарии

Этот метод является обязательным, поскольку идентификатор GUID профиля не может использоваться для вывода профиля сканирования пользователю.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>                                              |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2008\]<br/>                                        |
| Header<br/>                   | <dl> <dt>Сканпрофиле. h</dt> </dl>    |
| IDL<br/>                      | <dl> <dt>Сканпрофилес. idl</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**исканпрофиле**](-wia-iscanprofile.md)
</dt> <dt>

[Схема профиля сканирования](-wia-scan-profile-schema.md)
</dt> </dl>

 

 




