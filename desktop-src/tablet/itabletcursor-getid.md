---
description: Получает идентификатор пера.
ms.assetid: 27320a2f-1e4a-4d7d-a1f8-5244f4a03415
title: 'Метод Итаблеткурсор:: GetId'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITabletCursor.GetId
api_type:
- COM
api_location:
- wisptis.exe
- wisptis.exe.dll
ms.openlocfilehash: a7dc053b880c3ebaf4b94ae88a09c85f32f1dd5b8dc335756c8906c9a6f0fb4a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119938624"
---
# <a name="itabletcursorgetid-method"></a>Метод Итаблеткурсор:: GetId

Получает идентификатор пера.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT GetId(
  [out] CURSOR_ID *pCid
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*pCid* \[ заполняет\]
</dt> <dd>

Идентификатор пера планшета.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Этот метод может возвращать одно из этих значений.



| Код возврата                                                                            | Описание                               |
|----------------------------------------------------------------------------------------|-------------------------------------------|
| <dl> <dt>**\_ОК**</dt> </dl>   | Успешно.<br/>                       |
| <dl> <dt>**\_Ошибка E**</dt> </dl> | Произошла неизвестная ошибка.<br/> |



 

## <a name="remarks"></a>Remarks

Идентификатор КУРСОРа \_ определен как DWORD.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows XP Tablet PC Edition \[ только классические приложения\]<br/>                          |
| Минимальная версия сервера<br/> | Ни одна версия не поддерживается<br/>                                                              |
| Библиотека<br/>                  | <dl> <dt>Wisptis.exe</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**Интерфейс Итаблеткурсор**](itabletcursor.md)
</dt> </dl>

 

 




