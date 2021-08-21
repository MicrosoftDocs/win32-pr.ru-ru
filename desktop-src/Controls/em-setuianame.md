---
title: Сообщение EM_SETUIANAME (RichEdit. h)
description: Задает имя элемента управления расширенным редактированием для модели автоматизации пользовательского интерфейса (UIA).
ms.assetid: 60506FEE-9708-4668-8846-42B0B696DD9A
keywords:
- элементы управления Windows сообщений EM_SETUIANAME
topic_type:
- apiref
api_name:
- EM_SETUIANAME
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 603d59b7bf246ee8ed7987d42399281ac1b0520ef27e206f2f8eeddf8f363d87
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118412329"
---
# <a name="em_setuianame-message"></a>\_Сообщение СЕТУИАНАМЕ EM

Задает имя элемента управления расширенным редактированием для модели автоматизации пользовательского интерфейса (UIA).


```C++
#define EM_SETUIANAME       (WM_USER + 320)
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*wParam* 
</dt> <dd>

Не используется; должно быть равно нулю.

</dd> <dt>

*lParam* 
</dt> <dd>

Указатель на строку имени, заканчивающуюся нулем.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Значение TRUE, если имя для UIA успешно установлено; в противном случае — значение FALSE.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 8 \[ только классические приложения\]<br/>                                            |
| Минимальная версия сервера<br/> | Windows Server 2012 \[ только классические приложения\]<br/>                                  |
| Header<br/>                   | <dl> <dt>RichEdit. h</dt> </dl> |



 

 





