---
title: Сообщение EM_SETSTORYTYPE (RichEdit. h)
description: Задает тип истории.
ms.assetid: 8FA335E1-EE0A-4F31-B800-C79F617A6019
keywords:
- Элементы управления Windows для EM_SETSTORYTYPE сообщений
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
ms.openlocfilehash: be6d1df04f93fca0119b58f978a6a0cb36ddf464
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103891714"
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

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | \[Только классические приложения Windows 8\]<br/>                                            |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2012\]<br/>                                  |
| Header<br/>                   | <dl> <dt>RichEdit. h</dt> </dl> |



 

 





