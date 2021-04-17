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
ms.openlocfilehash: f6950e0b30c1b8fc8ccf3e60a8aaa05b9eeb3215
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105684406"
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



 

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только классические приложения Windows XP Tablet PC Edition \[\]<br/>                          |
| Минимальная версия сервера<br/> | Ни одна версия не поддерживается<br/>                                                              |
| Библиотека<br/>                  | <dl> <dt>Wisptis.exe</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Интерфейс Итаблетевентсинк**](itableteventsink.md)
</dt> </dl>

 

 




