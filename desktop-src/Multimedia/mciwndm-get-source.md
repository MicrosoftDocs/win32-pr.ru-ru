---
title: Сообщение MCIWNDM_GET_SOURCE (VFW. h)
description: '\_ \_ Сообщение источника мЦивндм Get получает координаты исходного прямоугольника, используемого для обрезки изображений файла AVI во время воспроизведения. Это сообщение можно отправить явно или с помощью макроса МЦивнджетсаурце.'
ms.assetid: d5f25926-5a3d-412e-8248-fbf307583757
keywords:
- MCIWNDM_GET_SOURCE сообщения Windows мультимедиа
topic_type:
- apiref
api_name:
- MCIWNDM_GET_SOURCE
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 85147182d06386efed73229fcdd6c75372244fd6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104415900"
---
# <a name="mciwndm_get_source-message"></a>МЦИВНДМ \_ Получение \_ исходного сообщения

Сообщение **\_ \_ источника мЦивндм Get** получает координаты исходного прямоугольника, используемого для обрезки изображений файла AVI во время воспроизведения. Это сообщение можно отправить явно или с помощью макроса [**мЦивнджетсаурце**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetsource) .


```C++
MCIWNDM_GET_SOURCE 
wParam = 0; 
lParam = (LPARAM) (LPRECT) prc; 
```



## <a name="parameters"></a>Параметры

<dl> <dt>

<span id="prc"></span><span id="PRC"></span>*PRC*
</dt> <dd>

Указатель на структуру [**Rect**](/previous-versions//dd162897(v=vs.85)) , в которой должны содержаться координаты исходного прямоугольника.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает нуль в случае успеха или ошибку в противном случае.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional \[только классические приложения\]<br/>                       |
| Минимальная версия сервера<br/> | Windows 2000 Server \[только классические приложения\]<br/>                             |
| Заголовок<br/>                   | <dl> <dt>VFW. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**мЦивнджетсаурце**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetsource)
</dt> </dl>

 

