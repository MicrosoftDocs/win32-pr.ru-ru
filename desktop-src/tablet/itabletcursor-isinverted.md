---
description: Указывает, является ли перо перевернутым.
ms.assetid: 04b05287-000d-455f-88e5-821c7fdb8119
title: 'Метод Итаблеткурсор:: инверсия'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITabletCursor.IsInverted
api_type:
- COM
api_location:
- wisptis.exe
- wisptis.exe.dll
ms.openlocfilehash: 041b81c38f3370421c96a4c0d66201254a715e62
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105656641"
---
# <a name="itabletcursorisinverted-method"></a>Метод Итаблеткурсор:: инверсия

Указывает, является ли перо перевернутым.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT IsInverted();
```



## <a name="parameters"></a>Параметры

Этот метод не имеет параметров.

## <a name="return-value"></a>Возвращаемое значение

Этот метод может возвращать одно из этих значений.



| Код возврата                                                                             | Описание                               |
|-----------------------------------------------------------------------------------------|-------------------------------------------|
| <dl> <dt>**\_ОК**</dt> </dl>    | Перо инвертировано.<br/>        |
| <dl> <dt>**S \_ false**</dt> </dl> | Перо не инвертировано.<br/>    |
| <dl> <dt>**\_Ошибка E**</dt> </dl>  | Произошла неизвестная ошибка.<br/> |



 

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только классические приложения Windows XP Tablet PC Edition \[\]<br/>                          |
| Минимальная версия сервера<br/> | Ни одна версия не поддерживается<br/>                                                              |
| Библиотека<br/>                  | <dl> <dt>Wisptis.exe</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**итаблеткурсор**](itabletcursor.md)
</dt> <dt>

[**Интерфейс Итаблеткурсорбуттон**](itabletcursorbutton.md)
</dt> </dl>

 

 




