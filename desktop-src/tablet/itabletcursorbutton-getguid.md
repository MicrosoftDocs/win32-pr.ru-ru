---
description: Извлекает уникальный идентификатор кнопки пера.
ms.assetid: 06bd6a84-46cd-4c62-92d6-50caae359e43
title: 'Метод Итаблеткурсорбуттон::'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITabletCursorButton.GetGuid
api_type:
- COM
api_location:
- wisptis.exe
- wisptis.exe.dll
ms.openlocfilehash: f4492aa98630491730435080981172bc60a1eeccfe0c84ed76e3b4d504a79ad1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119844284"
---
# <a name="itabletcursorbuttongetguid-method"></a>Метод Итаблеткурсорбуттон::

Извлекает уникальный идентификатор кнопки пера.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT GetGuid(
  [out] GUID *pguidBtn
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*пгуидбтн* \[ заполняет\]
</dt> <dd>

Уникальное значение, идентифицирующее кнопку пера.

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

[**Интерфейс Итаблеткурсорбуттон**](itabletcursorbutton.md)
</dt> </dl>

 

 




