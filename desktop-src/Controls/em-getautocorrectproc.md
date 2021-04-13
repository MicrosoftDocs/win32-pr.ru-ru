---
title: Сообщение EM_GETAUTOCORRECTPROC (RichEdit. h)
description: Возвращает указатель на определяемую приложением функцию Аутокорректпрок.
ms.assetid: 90821036-F27D-4AC3-9AB8-40A94486B938
keywords:
- Элементы управления Windows для EM_GETAUTOCORRECTPROC сообщений
topic_type:
- apiref
api_name:
- EM_GETAUTOCORRECTPROC
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dc4d730d15ca8631e6d663e3d4f971f115d5c268
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104491007"
---
# <a name="em_getautocorrectproc-message"></a>\_Сообщение ЖЕТАУТОКОРРЕКТПРОК EM

Возвращает указатель на определяемую приложением функцию [*аутокорректпрок*](/windows/desktop/api/Richedit/nc-richedit-autocorrectproc) .

## <a name="parameters"></a>Параметры

<dl> <dt>

*wParam* 
</dt> <dd>

Не используется; должно быть равно нулю.

</dd> <dt>

*lParam* 
</dt> <dd>

Не используется; должно быть равно нулю.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает указатель на определяемую приложением функцию [*аутокорректпрок*](/windows/desktop/api/Richedit/nc-richedit-autocorrectproc) .

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

[**EM \_ сетаутокорректпрок**](em-setautocorrectproc.md)
</dt> </dl>

 

 





