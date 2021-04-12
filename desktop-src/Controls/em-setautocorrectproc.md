---
title: Сообщение EM_SETAUTOCORRECTPROC (RichEdit. h)
description: Определяет текущую процедуру обратного вызова для автозамены.
ms.assetid: 2FA48CFC-0D7C-41EF-8207-5EDC644FF3BC
keywords:
- Элементы управления Windows для EM_SETAUTOCORRECTPROC сообщений
topic_type:
- apiref
api_name:
- EM_SETAUTOCORRECTPROC
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a7359c86c3fdabe4c410f600d0af3100dde4c4ed
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104492483"
---
# <a name="em_setautocorrectproc-message"></a>\_Сообщение СЕТАУТОКОРРЕКТПРОК EM

Определяет текущую процедуру обратного вызова для автозамены.


```C++
#define EM_SETAUTOCORRECTPROC       (WM_USER + 234)
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*wParam* 
</dt> <dd>

Функция обратного вызова [*аутокорректпрок*](/windows/desktop/api/Richedit/nc-richedit-autocorrectproc) .

</dd> <dt>

*lParam* 
</dt> <dd>

Не используется; должно быть равно нулю

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Если операция выполнена удачно, возвращаемое значение равно нулю. Если операция завершается неудачно, возвращаемое значение будет ненулевым.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | \[Только классические приложения Windows 8\]<br/>                                            |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2012\]<br/>                                  |
| Header<br/>                   | <dl> <dt>RichEdit. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[*аутокорректпрок*](/windows/desktop/api/Richedit/nc-richedit-autocorrectproc)
</dt> <dt>

[**EM \_ каллаутокорректпрок**](em-callautocorrectproc.md)
</dt> <dt>

[**EM \_ жетаутокорректпрок**](em-getautocorrectproc.md)
</dt> </dl>

 

 





