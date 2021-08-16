---
description: Извлекает типы сетевых адресов, принимаемые указанным элементом управления сетью.
title: Сообщение NCM_GETALLOWTYPE (Шеллапи. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 1B06463F-0CA6-4e8e-BD3B-917562A6A244
api_name:
- NCM_GETALLOWTYPE
api_type:
- HeaderDef
api_location:
- Shellapi.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 11b937ca851f00c51090683db4aebfc3db63cbf83efc95bad7a6f456d8f58988
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117858813"
---
# <a name="ncm_getallowtype-message"></a>\_Сообщение НКМ жеталловтипе

Извлекает типы сетевых адресов, принимаемые указанным элементом управления сетью.


```C++
NCM_GETALLOWTYPE

    wParam = 0;

    lParam = 0;            

            
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*wParam* 
</dt> <dd>Должен равняться нулю.</dd> <dt>

*lParam* 
</dt> <dd>Должен равняться нулю.</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает разрешенные типы сетевых адресов в виде одной или нескольких констант типа "сеть — [**\_ строка**](net-string.md) ".

## <a name="remarks"></a>Remarks

Возвращенная маска — это критерий, используемый для проверки сетевого адреса в сообщении [**НКМ- \_ Address**](ncm-getaddress.md) .

Это сообщение используется только для управления сетевыми адресами. Чтобы создать экземпляр, используйте класс **мсктлс \_ нетаддресс** , определенный в шеллапи. h. Вызовите [**инитнетворкаддрессконтрол**](/windows/desktop/api/Shellapi/nf-shellapi-initnetworkaddresscontrol) во время выполнения перед отправкой этого сообщения. Будет инициализирована библиотека общих элементов управления, содержащая элемент управления "сетевой адрес".

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2008\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Шеллапи. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**НКМ \_ сеталловтипе**](ncm-setallowtype.md)
</dt> <dt>

[**Нетаддр \_ жеталловтипе**](/windows/desktop/api/Shellapi/nf-shellapi-netaddr_getallowtype)
</dt> </dl>

 

 




