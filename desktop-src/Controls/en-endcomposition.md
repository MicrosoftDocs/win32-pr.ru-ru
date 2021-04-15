---
title: Код уведомления EN_ENDCOMPOSITION (RichEdit. h)
description: Сообщает родительскому окну форматированного элемента управления, что пользователь вводит новые данные, или завершил ввод данных при использовании IME или платформы текстовых служб.
ms.assetid: 3956313F-F82F-41A2-AEDA-52E63218977C
keywords:
- EN_ENDCOMPOSITION кода уведомления элементы управления Windows
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
ms.openlocfilehash: 9df1c2b5d08b2da73c67edeb6fe7ca4ac639000c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104489282"
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

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | \[Только классические приложения Windows 8\]<br/>                                            |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2012\]<br/>                                  |
| Header<br/>                   | <dl> <dt>RichEdit. h</dt> </dl> |



 

