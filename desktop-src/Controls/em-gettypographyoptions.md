---
title: Сообщение EM_GETTYPOGRAPHYOPTIONS (RichEdit. h)
description: Возвращает текущее состояние типографских параметров элемента управления Rich Edit.
ms.assetid: 6ff5980e-3201-4b0f-9a03-3de78730ce33
keywords:
- элементы управления Windows сообщений EM_GETTYPOGRAPHYOPTIONS
topic_type:
- apiref
api_name:
- EM_GETTYPOGRAPHYOPTIONS
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d575550e2c239ee5b689deb5874a9803c581151b54100ab227a24d4f29941973
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117831174"
---
# <a name="em_gettypographyoptions-message"></a>\_Сообщение ЖЕТТИПОГРАФЙОПТИОНС EM

Возвращает текущее состояние типографских параметров элемента управления Rich Edit.

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

Возвращает текущие параметры оформления. Список параметров см. в разделе [**EM \_ сеттипографйоптионс**](em-settypographyoptions.md).

## <a name="remarks"></a>Remarks

Вы можете включить дополнительные разрывы строк, отправив сообщение [**EM \_ сеттипографйоптионс**](em-settypographyoptions.md) . Расширенные и нормальные разрывы строк также можно включить автоматически с помощью элемента управления Rich Edit, если это необходимо для определенных языков.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2003\]<br/>                                  |
| Распространяемые компоненты<br/>          | Расширенное редактирование 3,0<br/>                                                              |
| Header<br/>                   | <dl> <dt>RichEdit. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

**Ссылки**
</dt> <dt>

[**EM \_ сеттипографйоптионс**](em-settypographyoptions.md)
</dt> <dt>

**Зрения**
</dt> <dt>

[Общие сведения об элементах управления "поле ввода"](about-rich-edit-controls.md)
</dt> </dl>

 

 





