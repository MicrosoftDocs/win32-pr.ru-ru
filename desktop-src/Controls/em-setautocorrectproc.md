---
title: Сообщение EM_SETAUTOCORRECTPROC (RichEdit. h)
description: Определяет текущую процедуру обратного вызова для автозамены.
ms.assetid: 2FA48CFC-0D7C-41EF-8207-5EDC644FF3BC
keywords:
- элементы управления Windows сообщений EM_SETAUTOCORRECTPROC
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
ms.openlocfilehash: b46e838cf18a345272b7983de1522a0c55a2565c5df3e11e3c89cd820653fb73
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118958723"
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
| Минимальная версия клиента<br/> | Windows 8 \[ только классические приложения\]<br/>                                            |
| Минимальная версия сервера<br/> | Windows Server 2012 \[ только классические приложения\]<br/>                                  |
| Header<br/>                   | <dl> <dt>RichEdit. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[*аутокорректпрок*](/windows/desktop/api/Richedit/nc-richedit-autocorrectproc)
</dt> <dt>

[**EM \_ каллаутокорректпрок**](em-callautocorrectproc.md)
</dt> <dt>

[**EM \_ жетаутокорректпрок**](em-getautocorrectproc.md)
</dt> </dl>

 

 





