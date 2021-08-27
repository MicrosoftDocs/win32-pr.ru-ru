---
title: Сообщение EM_GETELLIPSISSTATE (RichEdit. h)
description: Извлекает текущее состояние многоточия.
ms.assetid: D02AE225-F5BF-401A-9877-55C68946CDBE
keywords:
- элементы управления Windows сообщений EM_GETELLIPSISSTATE
topic_type:
- apiref
api_name:
- EM_GETELLIPSISSTATE
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7aaa02fa5ecfdaa5e9f24a41a28ab696e6f2e76224cff8443fab3aa558d1e5a8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120049254"
---
# <a name="em_getellipsisstate-message"></a>\_Сообщение ЖЕТЕЛЛИПСИССТАТЕ EM

Извлекает текущее состояние многоточия.


```C++
#define EM_GETELLIPSISSTATE       (WM_USER + 322)
```



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

Возвращаемое значение равно TRUE, если отображается многоточие, и FALSE в противном случае.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 8 \[ только классические приложения\]<br/>                                            |
| Минимальная версия сервера<br/> | Windows Server 2012 \[ только классические приложения\]<br/>                                  |
| Заголовок<br/>                   | <dl> <dt>RichEdit. h</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**EM \_ жетеллипсисмоде**](em-getellipsismode.md)
</dt> <dt>

[**EM \_ сетеллипсисмоде**](em-setellipsismode.md)
</dt> </dl>

 

 





