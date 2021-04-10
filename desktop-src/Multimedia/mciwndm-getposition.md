---
title: Сообщение MCIWNDM_GETPOSITION (VFW. h)
description: Сообщение МЦИВНДМ \_ Disposition извлекает числовое значение текущей позицией в содержимом устройства MCI.
ms.assetid: 6dc5d3bd-8515-4514-a2a5-c1bee07f7acf
keywords:
- MCIWNDM_GETPOSITION сообщения Windows мультимедиа
topic_type:
- apiref
api_name:
- MCIWNDM_GETPOSITION
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c2e7468b0e3698a72d3dce82bbd1591d59940d9a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103891545"
---
# <a name="mciwndm_getposition-message"></a>\_Сообщение мЦивндм

Сообщение **МЦИВНДМ \_ Disposition** извлекает числовое значение текущей позицией в содержимом устройства MCI. Этот макрос также предоставляет текущую точку в виде строки в определяемом приложением буфере. Это сообщение можно отправить явно или с помощью макроса [**мЦивнджетпоситион**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetposition) или [**мЦивнджетпоситионстринг**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetpositionstring) .


```C++
MCIWNDM_GETPOSITION 
wParam = (WPARAM) (UINT) len; 
lParam = (LPARAM) (LPTSTR) lp; 
```



## <a name="parameters"></a>Параметры

<dl> <dt>

<span id="len"></span><span id="LEN"></span>*len*
</dt> <dd>

Размер буфера в байтах. Если строка, завершающаяся нулем, длиннее, чем буфер, она усекается. Используйте ноль, чтобы запретить получение позиций в виде строки.

</dd> <dt>

<span id="lp"></span><span id="LP"></span>*LP*
</dt> <dd>

Указатель на определенный приложением буфер, используемый для возврата позиции. Используйте ноль, чтобы запретить получение позиций в виде строки. Если устройство поддерживает записи, сведения о положении строки возвращаются в формате TT: MM: SS: FF, где TT соответствует дорожкам, MM и SS соответствуют минутам и секундам, а FF соответствует кадрам.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает целое число, соответствующее текущему положению. Единицы для значения «значение» зависят от текущего формата времени.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional \[только классические приложения\]<br/>                       |
| Минимальная версия сервера<br/> | Windows 2000 Server \[только классические приложения\]<br/>                             |
| Заголовок<br/>                   | <dl> <dt>VFW. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**мЦивнджетпоситион**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetposition)
</dt> <dt>

[**мЦивнджетпоситионстринг**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetpositionstring)
</dt> </dl>

 

 





