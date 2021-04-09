---
title: Сообщение MCIWNDM_GETERROR (VFW. h)
description: МЦИВНДМ \_ сообщение об ошибке извлекает последнюю обнаруженную ошибку MCI. Это сообщение можно отправить явно или с помощью макроса МЦивнджетеррор.
ms.assetid: f110a9b3-5b05-4bf0-85d1-b49ce7396222
keywords:
- MCIWNDM_GETERROR сообщения Windows мультимедиа
topic_type:
- apiref
api_name:
- MCIWNDM_GETERROR
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5c2977bb079351824b48da21f4ba3cc2dc5afe7e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103891546"
---
# <a name="mciwndm_geterror-message"></a>\_Сообщение об ошибке мЦивндм

МЦивндм сообщение об **\_ ошибке** извлекает последнюю обнаруженную ошибку MCI. Это сообщение можно отправить явно или с помощью макроса [**мЦивнджетеррор**](/windows/desktop/api/Vfw/nf-vfw-mciwndgeterror) .


```C++
MCIWNDM_GETERROR 
wParam = (WPARAM) (UINT) len; 
lParam = (LPARAM) (LPVOID) lp; 
```



## <a name="parameters"></a>Параметры

<dl> <dt>

<span id="len"></span><span id="LEN"></span>*len*
</dt> <dd>

Размер буфера ошибок в байтах.

</dd> <dt>

<span id="lp"></span><span id="LP"></span>*LP*
</dt> <dd>

Указатель на определенный приложением буфер, используемый для возврата строки ошибки.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает целочисленное значение ошибки в случае успеха.

## <a name="remarks"></a>Комментарии

Если *LP* является допустимым указателем, в его буфере возвращается строка, завершающаяся нулем, соответствующая ошибке. Если строка ошибки длиннее, чем буфер, МЦивнд усекает ее.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional \[только классические приложения\]<br/>                       |
| Минимальная версия сервера<br/> | Windows 2000 Server \[только классические приложения\]<br/>                             |
| Заголовок<br/>                   | <dl> <dt>VFW. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**мЦивнджетеррор**](/windows/desktop/api/Vfw/nf-vfw-mciwndgeterror)
</dt> </dl>

 

 





