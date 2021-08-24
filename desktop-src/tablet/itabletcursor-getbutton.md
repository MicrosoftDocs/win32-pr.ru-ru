---
description: Извлекает указанный объект кнопки из пера планшета.
ms.assetid: 83a26703-4501-4f43-9e86-c5c753347012
title: 'Метод Итаблеткурсор:: "Button"'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITabletCursor.GetButton
api_type:
- COM
api_location:
- wisptis.exe
- wisptis.exe.dll
ms.openlocfilehash: 49306160a0c14badc23cb2f359400d0fb2947012078a9318315a6697050f48dc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119938634"
---
# <a name="itabletcursorgetbutton-method"></a>Метод Итаблеткурсор:: "Button"

Извлекает указанный объект кнопки из пера планшета.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT GetButton(
  [in]  ULONG               iButton,
  [out] ITabletCursorButton **ppButton
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*ибуттон* \[ окне\]
</dt> <dd>

Идентификатор извлекаемой кнопки.

</dd> <dt>

*ппбуттон* \[ заполняет\]
</dt> <dd>

Объект Button, заданный параметром *ибуттон* .

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Этот метод может возвращать одно из этих значений.



| Код возврата                                                                            | Описание                               |
|----------------------------------------------------------------------------------------|-------------------------------------------|
| <dl> <dt>**\_ОК**</dt> </dl>   | Успешно.<br/>                       |
| <dl> <dt>**\_Ошибка E**</dt> </dl> | Произошла неизвестная ошибка.<br/> |



 

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

 

 




