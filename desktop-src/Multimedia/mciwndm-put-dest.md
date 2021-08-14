---
title: Сообщение MCIWNDM_PUT_DEST (VFW. h)
description: '\_Сообщение о мЦивндме размещения \_ переопределяет координаты прямоугольника назначения, используемого для масштабирования или растяжения изображений файла AVI во время воспроизведения. Это сообщение можно отправить явно или с помощью макроса МЦивндпутдест.'
ms.assetid: 0b13d473-ef93-41a2-bbb2-09fbf264493e
keywords:
- сообщение MCIWNDM_PUT_DEST Windows мультимедиа
topic_type:
- apiref
api_name:
- MCIWNDM_PUT_DEST
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 27eb2afdcec32d43b0352af1ead0b4c89715641fd370611542e1e5c6da9efa85
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118373525"
---
# <a name="mciwndm_put_dest-message"></a>МЦИВНДМ \_ Размещение \_ сообщения о приемнике

Сообщение о **мЦивндме \_ размещения \_** переопределяет координаты прямоугольника назначения, используемого для масштабирования или растяжения изображений файла AVI во время воспроизведения. Это сообщение можно отправить явно или с помощью макроса [**мЦивндпутдест**](/windows/desktop/api/Vfw/nf-vfw-mciwndputdest) .


```C++
MCIWNDM_PUT_DEST 
wParam = 0; 
lParam = (LPARAM) (LPRECT) prc; 
```



## <a name="parameters"></a>Параметры

<dl> <dt>

<span id="prc"></span><span id="PRC"></span>*PRC*
</dt> <dd>

Указатель на структуру [**Rect**](/previous-versions//dd162897(v=vs.85)) , содержащую координаты прямоугольника назначения.

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

[**мЦивндпутдест**](/windows/desktop/api/Vfw/nf-vfw-mciwndputdest)
</dt> </dl>

 

