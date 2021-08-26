---
title: Сообщение EM_CALLAUTOCORRECTPROC (RichEdit. h)
description: Вызывает функцию обратного вызова автозамены, которая хранится в \_ сообщении СЕТАУТОКОРРЕКТПРОК EM при условии, что текст, предшествующий точке вставки, является кандидатом на автозамену.
ms.assetid: 93116467-B345-4FD9-9162-3E01CF3C6F20
keywords:
- элементы управления Windows сообщений EM_CALLAUTOCORRECTPROC
topic_type:
- apiref
api_name:
- EM_CALLAUTOCORRECTPROC
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1ad76ec66018b4e673913c433ce16a1294944f69c9d33a5dbaedb85ba21f985a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119916084"
---
# <a name="em_callautocorrectproc-message"></a>\_Сообщение КАЛЛАУТОКОРРЕКТПРОК EM

Вызывает функцию обратного вызова автозамены, которая хранится в сообщении [**\_ сетаутокорректпрок EM**](em-setautocorrectproc.md) при условии, что текст, предшествующий точке вставки, является кандидатом на автозамену.


```C++
#define EM_CALLAUTOCORRECTPROC       (WM_USER + 255)
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*wParam* 
</dt> <dd>

Символ типа **WCHAR**. Если этот символ является вкладкой (U + 0009), а символ, предшествующий точке вставки, — t a TAB, то символ, предшествующий точке вставки, обрабатывается как часть строки кандидатов для автозамены, а не как разделитель строк. в противном случае *wParam* не оказывает никакого влияния.

</dd> <dt>

*lParam* 
</dt> <dd>

Не используется; должно быть равно нулю.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращаемое значение равно нулю, если сообщение прошло удачно, или ненулевой при возникновении ошибки.

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

[**EM \_ жетаутокорректпрок**](em-getautocorrectproc.md)
</dt> <dt>

[**EM \_ сетаутокорректпрок**](em-setautocorrectproc.md)
</dt> </dl>

 

 





