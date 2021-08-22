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
ms.openlocfilehash: 81bbb5f4f93026e0d6910cb7f23d0a7d2ddeea5595e87f816faa016d22986d0e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119223074"
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
| Минимальная версия клиента<br/> | Windows XP Tablet PC Edition \[ только классические приложения\]<br/>                          |
| Минимальная версия сервера<br/> | Ни одна версия не поддерживается<br/>                                                              |
| Библиотека<br/>                  | <dl> <dt>Wisptis.exe</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**итаблеткурсор**](itabletcursor.md)
</dt> <dt>

[**Интерфейс Итаблеткурсорбуттон**](itabletcursorbutton.md)
</dt> </dl>

 

 




