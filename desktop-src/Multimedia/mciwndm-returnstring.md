---
title: Сообщение MCIWNDM_RETURNSTRING (VFW. h)
description: Сообщение МЦИВНДМ \_ ретурнстринг извлекает ответ на последнюю командную строку MCI, отправленную на устройство MCI.
ms.assetid: 36a5222c-a63c-4b8c-ad0c-a00477e95b96
keywords:
- сообщение MCIWNDM_RETURNSTRING Windows мультимедиа
topic_type:
- apiref
api_name:
- MCIWNDM_RETURNSTRING
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d2ea9624c70245c67f0f6a78af68bf291ae3ce60ba65ae2cd273008bbc914ec2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118137661"
---
# <a name="mciwndm_returnstring-message"></a>\_Сообщение мЦивндм ретурнстринг

Сообщение **мЦивндм \_ ретурнстринг** извлекает ответ на последнюю командную строку MCI, отправленную на устройство MCI. Сведения в ответе передаются в виде строки, завершающейся нулем. Это сообщение можно отправить явно или с помощью макроса [**мЦивндретурнстринг**](/windows/desktop/api/Vfw/nf-vfw-mciwndreturnstring) .


```C++
MCIWNDM_RETURNSTRING 
wParam = (WPARAM) (UINT) len; 
lParam = (LPARAM) (LPVOID) lp; 
```



## <a name="parameters"></a>Параметры

<dl> <dt>

<span id="len"></span><span id="LEN"></span>*len*
</dt> <dd>

Размер буфера в байтах.

</dd> <dt>

<span id="lp"></span><span id="LP"></span>*LP*
</dt> <dd>

Указатель на определенный приложением буфер, содержащий строку, завершающуюся нулем.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает целое число, соответствующее строке MCI.

## <a name="remarks"></a>Remarks

Если строка, завершающаяся нулем, длиннее, чем буфер, строка усекается.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional \[только классические приложения\]<br/>                       |
| Минимальная версия сервера<br/> | Windows 2000 Server \[только классические приложения\]<br/>                             |
| Заголовок<br/>                   | <dl> <dt>VFW. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**мЦивндретурнстринг**](/windows/desktop/api/Vfw/nf-vfw-mciwndreturnstring)
</dt> </dl>

 

 





