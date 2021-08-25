---
title: Сообщение MCIWNDM_SETZOOM (VFW. h)
description: Сообщение МЦИВНДМ \_ сетзум изменяет размер изображения видео в соответствии с коэффициентом масштабирования. Этот Марко корректирует размер МЦивнд окна, сохраняя постоянную пропорцию. Это сообщение можно отправить явно или с помощью макроса МЦивндсетзум.
ms.assetid: c899b678-5ba7-4f0a-9ef9-c5370b3b4ea8
keywords:
- сообщение MCIWNDM_SETZOOM Windows мультимедиа
topic_type:
- apiref
api_name:
- MCIWNDM_SETZOOM
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fbcdd40206332df442bbae32975b0d888bbe39bc377a189d40e215888e4a6d0f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119807584"
---
# <a name="mciwndm_setzoom-message"></a>\_Сообщение мЦивндм сетзум

Сообщение **мЦивндм \_ сетзум** изменяет размер изображения видео в соответствии с коэффициентом масштабирования. Этот Марко корректирует размер МЦивнд окна, сохраняя постоянную пропорцию. Это сообщение можно отправить явно или с помощью макроса [**мЦивндсетзум**](/windows/desktop/api/Vfw/nf-vfw-mciwndsetzoom) .


```C++
MCIWNDM_SETZOOM 
wParam = 0; 
lParam = (LPARAM) (UINT) iZoom; 
```



## <a name="parameters"></a>Параметры

<dl> <dt>

<span id="iZoom"></span><span id="izoom"></span><span id="IZOOM"></span>*изум*
</dt> <dd>

Коэффициент масштабирования выражается в процентах от исходного изображения. Укажите 100, чтобы изображение отображалось в созданном размере, 200, чтобы изображение отображалось в два раза больше обычного размера, или 50, чтобы изображение отображалось с половиной его обычного размера.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Это сообщение не возвращает значение.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional \[только классические приложения\]<br/>                       |
| Минимальная версия сервера<br/> | Windows 2000 Server \[только классические приложения\]<br/>                             |
| Заголовок<br/>                   | <dl> <dt>VFW. h</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**мЦивндсетзум**](/windows/desktop/api/Vfw/nf-vfw-mciwndsetzoom)
</dt> </dl>

 

 





