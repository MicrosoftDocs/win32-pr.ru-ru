---
description: Происходит при наведении курсора мыши на планшетном дигитайзере.
ms.assetid: cd2863af-59a9-4dd0-a679-84861a70ef53
title: 'Метод Итаблетевентсинк:: Курсормове'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITabletEventSink.CursorMove
api_type:
- COM
api_location:
- wisptis.exe
- wisptis.exe.dll
ms.openlocfilehash: 030fa5ba4adc725288d5135ccd24409d4fc02cddbc16da52aa375a275a73be5a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119843494"
---
# <a name="itableteventsinkcursormove-method"></a>Метод Итаблетевентсинк:: Курсормове

Происходит при наведении курсора мыши на планшетном дигитайзере.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT CursorMove(
   TABLET_CONTEXT_ID tcid,
   CURSOR_ID         cid,
   HWND              hWnd,
   LONG              xPos,
   LONG              yPos
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*тЦид* 
</dt> <dd>

Уникальный дентифиер планшетного дигитайзера.

</dd> <dt>

*согласуется* 
</dt> <dd>

Уникальный идентификатор пера планшета.

</dd> <dt>

*hWnd* 
</dt> <dd>

Окно, в которое переместился курсор.

</dd> <dt>

*кспос* 
</dt> <dd>

Координата X пера.

</dd> <dt>

*ипос* 
</dt> <dd>

Координата Y пера.

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

 

 




