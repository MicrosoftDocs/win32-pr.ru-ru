---
title: Сообщение EM_SETSTORYTYPE (RichEdit. h)
description: Задает тип истории.
ms.assetid: 8FA335E1-EE0A-4F31-B800-C79F617A6019
keywords:
- элементы управления Windows сообщений EM_SETSTORYTYPE
topic_type:
- apiref
api_name:
- EM_SETSTORYTYPE
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b7e09c62c50441857aac6f4018800de7a145081d64de49cdf7e9ca673a5370db
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120062884"
---
# <a name="em_setstorytype-message"></a>\_Сообщение СЕТСТОРИТИПЕ EM

Задает тип истории.


```C++
#define EM_SETSTORYTYPE       (WM_USER + 291)
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*wParam* 
</dt> <dd>

Индекс истории.

</dd> <dt>

*lParam* 
</dt> <dd>

Новый тип истории. Список типов истории см. в разделе [**EM \_ жетсторитипе**](em-getstorytype.md).

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Заданный тип истории.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 8 \[ только классические приложения\]<br/>                                            |
| Минимальная версия сервера<br/> | Windows Server 2012 \[ только классические приложения\]<br/>                                  |
| Заголовок<br/>                   | <dl> <dt>RichEdit. h</dt> </dl> |



 

 





