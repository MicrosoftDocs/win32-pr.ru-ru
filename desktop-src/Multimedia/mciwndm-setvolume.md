---
title: Сообщение MCIWNDM_SETVOLUME (VFW. h)
description: В \_ сообщении мЦивндм сетволуме задается уровень громкости устройства MCI. Это сообщение можно отправить явно или с помощью макроса МЦивндсетволуме.
ms.assetid: 04151588-b761-447a-9a57-808c034c3059
keywords:
- сообщение MCIWNDM_SETVOLUME Windows мультимедиа
topic_type:
- apiref
api_name:
- MCIWNDM_SETVOLUME
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e8c40d2c8b2c7c4cb309b5c6e5b21dcd29e6c8ee27b9ca8c97556cb14927a121
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119428544"
---
# <a name="mciwndm_setvolume-message"></a>\_Сообщение мЦивндм сетволуме

В сообщении **мЦивндм \_ сетволуме** задается уровень громкости устройства MCI. Это сообщение можно отправить явно или с помощью макроса [**мЦивндсетволуме**](/windows/desktop/api/Vfw/nf-vfw-mciwndsetvolume) .


```C++
MCIWNDM_SETVOLUME 
wParam = 0; 
lParam = (LPARAM) (UINT) iVol; 
```



## <a name="parameters"></a>Параметры

<dl> <dt>

<span id="iVol"></span><span id="ivol"></span><span id="IVOL"></span>*ивол*
</dt> <dd>

Новый уровень громкости. Укажите 1000 для обычного уровня громкости. Укажите более высокое значение громкости или более низкое значение для звукового тома.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает нуль в случае успеха или ошибку в противном случае.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional \[только классические приложения\]<br/>                       |
| Минимальная версия сервера<br/> | Windows 2000 Server \[только классические приложения\]<br/>                             |
| Заголовок<br/>                   | <dl> <dt>VFW. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**мЦивндсетволуме**](/windows/desktop/api/Vfw/nf-vfw-mciwndsetvolume)
</dt> </dl>

 

 





