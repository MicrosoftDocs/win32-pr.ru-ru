---
description: Задает понятное имя профиля.
ms.assetid: a0a2de8b-ab7b-49a8-b513-32af0052975f
title: 'Метод Исканпрофиле:: SetName (Сканпрофиле. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IScanProfile.SetName
api_type:
- COM
api_location:
- Scanprofile.h
ms.openlocfilehash: 0023353f298d5b6690345d559517c3840d33da6eb836c983b85924b5c4ac4260
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118441484"
---
# <a name="iscanprofilesetname-method"></a>Метод Исканпрофиле:: SetName

Задает понятное имя профиля.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT SetName(
  [in] BSTR bstrName
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*bstrName* \[ окне\]
</dt> <dd>

Тип: **BSTR**

Понятное имя профиля.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **HRESULT**

Если этот метод завершается успешно, возвращается значение **S \_ ОК**. В противном случае возвращается код ошибки **HRESULT** .

## <a name="remarks"></a>Remarks

Этот метод является обязательным, поскольку идентификатор GUID профиля не может использоваться для вывода профиля сканирования пользователю.

Пользователь может изменить понятное имя профиля с помощью метода [**сканпрофиледиалог**](-wia-iscanprofileui-scanprofiledialog.md) .

Изменения в профиле не сохраняются на диск, пока приложение не вызовет метод [**исканпрофиле:: Save**](-wia-iscanprofile-save.md) .

Если два приложения создают объекты профиля сканирования из одного и того же XML-файла и каждое приложение записывает изменения в свой объект, только изменения, внесенные приложением, которое вызывает [**исканпрофиле:: Save**](-wia-iscanprofile-save.md) Last, сохраняются на диске.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>                                              |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2008\]<br/>                                        |
| Header<br/>                   | <dl> <dt>Сканпрофиле. h</dt> </dl>    |
| IDL<br/>                      | <dl> <dt>Сканпрофилес. idl</dt> </dl> |



 

 




