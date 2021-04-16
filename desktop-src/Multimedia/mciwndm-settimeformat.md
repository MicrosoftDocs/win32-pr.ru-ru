---
title: Сообщение MCIWNDM_SETTIMEFORMAT (VFW. h)
description: Сообщение МЦИВНДМ \_ сеттимеформат задает формат времени для устройства MCI. Это сообщение можно отправить явно или с помощью макроса МЦивндсеттимеформат.
ms.assetid: 7de82094-6d35-44fd-88e7-ebd18a558cfd
keywords:
- MCIWNDM_SETTIMEFORMAT сообщения Windows мультимедиа
topic_type:
- apiref
api_name:
- MCIWNDM_SETTIMEFORMAT
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bcec1f0db5accad93211bf1eb6f1c9297e2b9f33
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104533800"
---
# <a name="mciwndm_settimeformat-message"></a>\_Сообщение мЦивндм сеттимеформат

Сообщение **мЦивндм \_ сеттимеформат** задает формат времени для устройства MCI. Это сообщение можно отправить явно или с помощью макроса [**мЦивндсеттимеформат**](/windows/desktop/api/Vfw/nf-vfw-mciwndsettimeformat) .


```C++
MCIWNDM_SETTIMEFORMAT 
wParam = 0; 
lParam = (LPARAM) (LPSTR) lp; 
```



## <a name="parameters"></a>Параметры

<dl> <dt>

<span id="lp"></span><span id="LP"></span>*LP*
</dt> <dd>

Указатель на буфер, содержащий строку, завершающуюся нулем, указывающую формат времени. Укажите "кадры", чтобы задать формат времени "кадры", или "MS", чтобы задать формат времени равным миллисекундам.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает нуль в случае успеха или ошибку в противном случае.

## <a name="remarks"></a>Комментарии

Приложение может указывать форматы времени, отличные от кадров, или миллисекунды, если форматы поддерживаются устройством MCI. Непостоянное форматирование, например дорожные и SMPTE, может привести к нестабильному поведению TrackBar. Для этих форматов времени может потребоваться отключить панель инструментов с помощью макроса [**мЦивндчанжестилес**](/windows/desktop/api/Vfw/nf-vfw-mciwndchangestyles) и указать \_ стиль окна мЦивндф ноплайбар.

Если необходимо задать формат времени для кадров или миллисекунд, можно также использовать макрос [**мЦивндусефрамес**](/windows/desktop/api/Vfw/nf-vfw-mciwnduseframes) или [**мЦивндусетиме**](/windows/desktop/api/Vfw/nf-vfw-mciwndusetime) . Список форматов времени см. в разделе макрос [**мЦивнджеттимеформат**](/windows/desktop/api/Vfw/nf-vfw-mciwndgettimeformat) .

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional \[только классические приложения\]<br/>                       |
| Минимальная версия сервера<br/> | Windows 2000 Server \[только классические приложения\]<br/>                             |
| Заголовок<br/>                   | <dl> <dt>VFW. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**мЦивндчанжестилес**](/windows/desktop/api/Vfw/nf-vfw-mciwndchangestyles)
</dt> <dt>

[**мЦивнджеттимеформат**](/windows/desktop/api/Vfw/nf-vfw-mciwndgettimeformat)
</dt> <dt>

[**мЦивндсеттимеформат**](/windows/desktop/api/Vfw/nf-vfw-mciwndsettimeformat)
</dt> <dt>

[**мЦивндусефрамес**](/windows/desktop/api/Vfw/nf-vfw-mciwnduseframes)
</dt> <dt>

[**мЦивндусетиме**](/windows/desktop/api/Vfw/nf-vfw-mciwndusetime)
</dt> </dl>

 

 





