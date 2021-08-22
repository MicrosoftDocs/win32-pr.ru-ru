---
title: Код уведомления EN_ENDCOMPOSITION (RichEdit. h)
description: Сообщает родительскому окну форматированного элемента управления, что пользователь вводит новые данные, или завершил ввод данных при использовании IME или платформы текстовых служб.
ms.assetid: 3956313F-F82F-41A2-AEDA-52E63218977C
keywords:
- EN_ENDCOMPOSITION кода уведомления Windows элементы управления
topic_type:
- apiref
api_name:
- EN_ENDCOMPOSITION
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5d9fe75910ea018cf9d72dd14696067eb0b2bc00dabd4456cca63e41a099a75d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119436853"
---
# <a name="en_endcomposition-notification-code"></a>\_Код уведомления EN ендкомпоситион

Сообщает родительскому окну форматированного элемента управления, что пользователь вводит новые данные, или завершил ввод данных при использовании IME или [платформы текстовых служб](/windows/desktop/TSF/text-services-framework).


```C++
EN_ENDCOMPOSITION

     pEndComp = (ENDCOMPOSITIONNOTIFY *)lParam;
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*lParam* 
</dt> <dd>

Структура [**ендкомпоситионнотифи**](/windows/win32/api/richedit/ns-richedit-endcompositionnotify) , которая получает сведения о условии End композиция.

</dd> </dl>

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 8 \[ только классические приложения\]<br/>                                            |
| Минимальная версия сервера<br/> | Windows Server 2012 \[ только классические приложения\]<br/>                                  |
| Header<br/>                   | <dl> <dt>RichEdit. h</dt> </dl> |



 

