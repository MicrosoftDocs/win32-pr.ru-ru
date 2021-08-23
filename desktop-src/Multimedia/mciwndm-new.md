---
title: Сообщение MCIWNDM_NEW (VFW. h)
description: '\_Новое сообщение мЦивндм создает новый файл для текущего устройства MCI. Это сообщение можно отправить явно или с помощью макроса МЦивнднев.'
ms.assetid: 18b2340d-8303-415a-867f-bd346034db2a
keywords:
- сообщение MCIWNDM_NEW Windows мультимедиа
topic_type:
- apiref
api_name:
- MCIWNDM_NEW
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bca9c03aff08c07f3ab1d8337547de776aeab5c6623a34ddaa71bfada0bca4f8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119783084"
---
# <a name="mciwndm_new-message"></a>МЦИВНДМ \_ новое сообщение

**\_ Новое сообщение мЦивндм** создает новый файл для текущего устройства MCI. Это сообщение можно отправить явно или с помощью макроса [**мЦивнднев**](/windows/desktop/api/Vfw/nf-vfw-mciwndnew) .


```C++
MCIWNDM_NEW 
wParam = 0; 
lParam = (LPARAM) (LPVOID) lp; 
```



## <a name="parameters"></a>Параметры

<dl> <dt>

<span id="lp"></span><span id="LP"></span>*LP*
</dt> <dd>

Указатель на буфер, содержащий имя устройства MCI, которое будет использовать файл.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает нуль в случае успеха или ошибку в противном случае.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional \[только классические приложения\]<br/>                       |
| Минимальная версия сервера<br/> | Windows 2000 Server \[только классические приложения\]<br/>                             |
| Заголовок<br/>                   | <dl> <dt>VFW. h</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**мЦивнднев**](/windows/desktop/api/Vfw/nf-vfw-mciwndnew)
</dt> </dl>

 

 





