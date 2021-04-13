---
description: Указывает, будет ли вызывающий объект распределять текстуры, используемые для вывода.
ms.assetid: CAB41B22-AD96-4932-9686-66474CB26C38
title: Атрибут MF_XVP_CALLER_ALLOCATES_OUTPUT (Мфидл. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: def1b1d138c031393e1a1b1a3832c1ad6d066306
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104543218"
---
# <a name="mf_xvp_caller_allocates_output-attribute"></a>\_ \_ Вызывающий объект MF ксвп \_ выделяет \_ выходной атрибут

Указывает, будет ли вызывающий объект распределять текстуры, используемые для вывода.

## <a name="data-type"></a>Тип данных

**Bool** , сохраненный как **UINT32**

## <a name="remarks"></a>Комментарии

Если этот атрибут имеет **значение true**, обработчик видео ждет выделения выходных текстур вызывающей стороной, даже если работает в режиме ускорения DirectX Video (дксва). Если этот атрибут имеет **значение false**, процессор видео выделит выходные текстуры при работе в режиме дксва и завершится ошибкой, если предоставлены выходные текстуры, предоставленные абонентом.

Чтобы задать этот атрибут, сделайте следующее:

1.  Вызовите [**имфтрансформ:: OutAttribute**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes) в обработчике видео.
2.  Вызовите [**имфаттрибутес:: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).

Задайте атрибут перед началом потоковой передачи.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ настольных приложений Windows 10\]<br/>                                          |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2016\]<br/>                                 |
| Header<br/>                   | <dl> <dt>Мфидл. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>Мфидл. idl</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Алфавитный список атрибутов Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 




