---
title: Сообщение EM_SETUIANAME (RichEdit. h)
description: Задает имя элемента управления расширенным редактированием для модели автоматизации пользовательского интерфейса (UIA).
ms.assetid: 60506FEE-9708-4668-8846-42B0B696DD9A
keywords:
- Элементы управления Windows для EM_SETUIANAME сообщений
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
ms.openlocfilehash: b0102b792a9eccfc6116acc3a534b00fb64b7ee5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103988821"
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
| Минимальная версия клиента<br/> | \[Только классические приложения Windows 8\]<br/>                                            |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2012\]<br/>                                  |
| Header<br/>                   | <dl> <dt>RichEdit. h</dt> </dl> |



 

 





