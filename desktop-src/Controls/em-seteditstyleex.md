---
title: Сообщение EM_SETEDITSTYLEEX (RichEdit. h)
description: Задает текущие расширенные флаги стиля правки.
ms.assetid: C5CECC7C-6418-4A72-9F0B-6F55BE89E302
keywords:
- элементы управления Windows сообщений EM_SETEDITSTYLEEX
topic_type:
- apiref
api_name:
- EM_SETEDITSTYLEEX
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4b96a353b62dc3a31affd9e827ee803c481bcd806eaad9f8a5d0e9dd35388cf5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117831225"
---
# <a name="em_seteditstyleex-message"></a>\_Сообщение СЕТЕДИТСТИЛИКС EM

Задает текущие расширенные флаги стиля правки.


```C++
#define EM_SETEDITSTYLEEX       (WM_USER + 275)
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*wParam* 
</dt> <dd>

Указывает один или несколько расширенных флагов стиля редактирования. Список возможных значений см. в разделе [**EM \_ жетедитстиликс**](/windows/desktop/Controls/em-geteditstyleex).

</dd> <dt>

*lParam* 
</dt> <dd>

Маска, состоящая из одного или нескольких значений *wParam* . Будут установлены или сняты только значения, указанные в этой маске. Это позволяет устанавливать или снимать один флаг без считывания текущих состояний флагов.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращаемое значение является состоянием расширенных флагов стиля правки после того, как Расширенное редактирование попытается применить изменения стиля редактирования. Флаги редактирования стиля представляют собой набор флагов, указывающих текущий стиль редактирования.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 8 \[ только классические приложения\]<br/>                                            |
| Минимальная версия сервера<br/> | Windows Server 2012 \[ только классические приложения\]<br/>                                  |
| Header<br/>                   | <dl> <dt>RichEdit. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**EM \_ жетедитстиликс**](em-geteditstyleex.md)
</dt> </dl>

 

