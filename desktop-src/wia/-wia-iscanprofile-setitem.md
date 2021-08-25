---
description: задает идентификатор GUID категории для элемента Windowsного получения образа (WIA) 2,0, с которым связан профиль.
ms.assetid: e359abcb-b5d5-45a4-b650-2b278ba1ff6a
title: 'Метод Исканпрофиле:: Сетитем (Сканпрофиле. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IScanProfile.SetItem
api_type:
- COM
api_location:
- Scanprofile.h
ms.openlocfilehash: fc4f79c44ff84bef1efbda4b09beee6b7dcf83f04023a5e2211e9f808b18446a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119814074"
---
# <a name="iscanprofilesetitem-method"></a>Метод Исканпрофиле:: Сетитем

задает идентификатор GUID категории для элемента Windowsного получения образа (WIA) 2,0, с которым связан профиль.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT SetItem(
  [in] GUID guidCategory
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*гуидкатегори* \[ окне\]
</dt> <dd>

Тип: **GUID**

Идентификатор GUID категории элемента WIA 2,0. Это должна быть одна из \_ \_ констант категории элемента WIA IPA \_ .

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **HRESULT**

Если этот метод завершается успешно, возвращается значение **S \_ ОК**. В противном случае возвращается код ошибки **HRESULT** .

## <a name="remarks"></a>Remarks

Пользователи могут изменить категорию с помощью метода [**сканпрофиледиалог**](-wia-iscanprofileui-scanprofiledialog.md) .

Изменения в профиле не сохраняются на диск, пока приложение не вызовет метод [**исканпрофиле:: Save**](-wia-iscanprofile-save.md) .

Если два приложения создают объекты профиля сканирования из одного и того же XML-файла и каждое приложение записывает изменения в свой объект, только изменения, внесенные приложением, которое вызывает [**исканпрофиле:: Save**](-wia-iscanprofile-save.md) Last, сохраняются на диске.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>                                              |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2008\]<br/>                                        |
| Заголовок<br/>                   | <dl> <dt>Сканпрофиле. h</dt> </dl>    |
| IDL<br/>                      | <dl> <dt>Сканпрофилес. idl</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**исканпрофиле**](-wia-iscanprofile.md)
</dt> <dt>

[Схема профиля сканирования](-wia-scan-profile-schema.md)
</dt> </dl>

 

 




