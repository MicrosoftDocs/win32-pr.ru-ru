---
description: Возвращает число объектов Cursor, связанных с планшетом.
ms.assetid: 7aa5802c-1255-41a4-b1fa-23e5f56c0b80
title: 'Метод Итаблет:: Жеткурсоркаунт'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITablet.GetCursorCount
api_type:
- COM
api_location:
- wisptis.exe
- wisptis.exe.dll
ms.openlocfilehash: 02ad52e5ad75d4c71129ec7987347121c6152c01071e797c7b169327fdeb3614
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119883864"
---
# <a name="itabletgetcursorcount-method"></a>Метод Итаблет:: Жеткурсоркаунт

Возвращает число объектов Cursor, связанных с планшетом.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT GetCursorCount(
  [out] ULONG *pcCurs
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*пккурс* \[ заполняет\]
</dt> <dd>

Число объектов Cursor, связанных с планшетом.

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
| Минимальная версия клиента<br/> | Windows XP Tablet PC Edition \[ только классические приложения\]<br/>                          |
| Минимальная версия сервера<br/> | Ни одна версия не поддерживается<br/>                                                              |
| Библиотека<br/>                  | <dl> <dt>Wisptis.exe</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Интерфейс Итаблет**](itablet.md)
</dt> </dl>

 

 




