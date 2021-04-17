---
description: Задает идентификатор GUID категории элемента для получения образа Windows (WIA) 2,0, с которым связан профиль.
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
ms.openlocfilehash: d4b20aae0740656b46dd26824947fc27513afcac
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105711257"
---
# <a name="iscanprofilesetitem-method"></a>Метод Исканпрофиле:: Сетитем

Задает идентификатор GUID категории элемента для получения образа Windows (WIA) 2,0, с которым связан профиль.

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

## <a name="remarks"></a>Комментарии

Пользователи могут изменить категорию с помощью метода [**сканпрофиледиалог**](-wia-iscanprofileui-scanprofiledialog.md) .

Изменения в профиле не сохраняются на диск, пока приложение не вызовет метод [**исканпрофиле:: Save**](-wia-iscanprofile-save.md) .

Если два приложения создают объекты профиля сканирования из одного и того же XML-файла и каждое приложение записывает изменения в свой объект, только изменения, внесенные приложением, которое вызывает [**исканпрофиле:: Save**](-wia-iscanprofile-save.md) Last, сохраняются на диске.

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

 

 




