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
ms.openlocfilehash: 0b9e8e1337cacdb26d8c124d10e0a886748e70fe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105712359"
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



 

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только классические приложения Windows XP Tablet PC Edition \[\]<br/>                          |
| Минимальная версия сервера<br/> | Ни одна версия не поддерживается<br/>                                                              |
| Библиотека<br/>                  | <dl> <dt>Wisptis.exe</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Интерфейс Итаблеткурсор**](itabletcursor.md)
</dt> </dl>

 

 




