---
title: Сообщение EM_GETAUTOCORRECTPROC (RichEdit. h)
description: Возвращает указатель на определяемую приложением функцию Аутокорректпрок.
ms.assetid: 90821036-F27D-4AC3-9AB8-40A94486B938
keywords:
- элементы управления Windows сообщений EM_GETAUTOCORRECTPROC
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
ms.openlocfilehash: 4dc6b5068c1e72c05d7a1b85ee02e57b788cf417f732fe3c2bab8c66d0dcf383
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119541094"
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

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 8 \[ только классические приложения\]<br/>                                            |
| Минимальная версия сервера<br/> | Windows Server 2012 \[ только классические приложения\]<br/>                                  |
| Заголовок<br/>                   | <dl> <dt>RichEdit. h</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[*аутокорректпрок*](/windows/desktop/api/Richedit/nc-richedit-autocorrectproc)
</dt> <dt>

[**EM \_ каллаутокорректпрок**](em-callautocorrectproc.md)
</dt> <dt>

[**EM \_ сетаутокорректпрок**](em-setautocorrectproc.md)
</dt> </dl>

 

 





