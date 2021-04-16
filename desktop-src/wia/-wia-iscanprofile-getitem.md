---
description: Возвращает идентификатор GUID категории элемента для получения образа Windows (WIA) 2,0, с которым связан профиль.
ms.assetid: 2c816789-ad66-4b06-9160-7a86289ff373
title: Метод Исканпрофиле::-Item (Сканпрофиле. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IScanProfile.GetItem
api_type:
- COM
api_location:
- Scanprofile.h
ms.openlocfilehash: 888a3bb5bcb6e6c4fc2fefff2d976eb7fc1c7f82
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105650588"
---
# <a name="iscanprofilegetitem-method"></a>Метод Исканпрофиле:: Item

Возвращает идентификатор GUID категории элемента для получения образа Windows (WIA) 2,0, с которым связан профиль.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT GetItem(
  [out] GUID *pguidCategory
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*пгуидкатегори* \[ заполняет\]
</dt> <dd>

Тип: **GUID \** _

Указатель на идентификатор GUID категории элемента WIA 2,0. Это всегда одна из \_ \_ констант категории элемента WIA IPA \_ .

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: _ *HRESULT**

Если этот метод завершается успешно, возвращается значение **S \_ ОК**. В противном случае возвращается код ошибки **HRESULT** .

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

 

 




