---
description: возвращает идентификатор GUID категории элемента Windowsного получения изображений (WIA) 2,0, с которым связан профиль.
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
ms.openlocfilehash: 5a7f52a2d89bbd35b59febb25528fe493c4b5646afc70251fc19978d6d6265db
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119451044"
---
# <a name="iscanprofilegetitem-method"></a>Метод Исканпрофиле:: Item

возвращает идентификатор GUID категории элемента Windowsного получения изображений (WIA) 2,0, с которым связан профиль.

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

Тип: **GUID \***

Указатель на идентификатор GUID категории элемента WIA 2,0. Это всегда одна из \_ \_ констант категории элемента WIA IPA \_ .

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **HRESULT**

Если этот метод завершается успешно, возвращается значение **S \_ ОК**. В противном случае возвращается код ошибки **HRESULT** .

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>                                              |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2008\]<br/>                                        |
| Header<br/>                   | <dl> <dt>Сканпрофиле. h</dt> </dl>    |
| IDL<br/>                      | <dl> <dt>Сканпрофилес. idl</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**исканпрофиле**](-wia-iscanprofile.md)
</dt> <dt>

[Схема профиля сканирования](-wia-scan-profile-schema.md)
</dt> </dl>

 

 




