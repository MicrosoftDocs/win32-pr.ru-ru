---
description: Происходит, когда перо попадает в диапазон обнаружения дигитайзера.
ms.assetid: 22be233a-fc33-4a8f-91b6-28b2f2910b69
title: 'Метод Итаблетевентсинк:: Курсоринранже'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITabletEventSink.CursorInRange
api_type:
- COM
api_location:
- wisptis.exe
- wisptis.exe.dll
ms.openlocfilehash: 2c9878b4c3cd28727c5d54e59a52f3fe85a44832203f70b6ff042c6beeb579dd
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119883484"
---
# <a name="itableteventsinkcursorinrange-method"></a>Метод Итаблетевентсинк:: Курсоринранже

Происходит, когда перо попадает в диапазон обнаружения дигитайзера.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT CursorInRange(
  [in] TABLET_CONTEXT_ID tcid,
       t                 cid
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*тЦид* \[ окне\]
</dt> <dd>

Идентификатор объекта планшета, который обнаружил перо.

</dd> <dt>

*согласуется* 
</dt> <dd>

Идентификатор объекта пера, который находится в диапазоне диджитайзера.

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

[**Интерфейс Итаблетевентсинк**](itableteventsink.md)
</dt> </dl>

 

 




