---
title: Сообщение MCIWNDM_GET_DEST (VFW. h)
description: Сообщение МЦИВНДМ \_ Get \_ dest получает координаты прямоугольника назначения, используемого для масштабирования или растяжения изображений файла AVI во время воспроизведения. Это сообщение можно отправить явно или с помощью макроса МЦивнджетдест.
ms.assetid: d4d8a3eb-aad4-4435-a23b-7a9c55fc194d
keywords:
- MCIWNDM_GET_DEST сообщения Windows мультимедиа
topic_type:
- apiref
api_name:
- MCIWNDM_GET_DEST
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ab5f16b434caef56e6c6aa97bfd767770dc05ee1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104071091"
---
# <a name="mciwndm_get_dest-message"></a>МЦИВНДМ \_ Получение \_ сообщения о приемнике

Сообщение **мЦивндм \_ Get \_ dest** получает координаты прямоугольника назначения, используемого для масштабирования или растяжения изображений файла AVI во время воспроизведения. Это сообщение можно отправить явно или с помощью макроса [**мЦивнджетдест**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetdest) .


```C++
MCIWNDM_GET_DEST 
wParam = 0; 
lParam = (LPARAM) (LPRECT) prc; 
```



## <a name="parameters"></a>Параметры

<dl> <dt>

<span id="prc"></span><span id="PRC"></span>*PRC*
</dt> <dd>

Указатель на структуру [**Rect**](/previous-versions//dd162897(v=vs.85)) , чтобы вернуть координаты прямоугольника назначения.

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

[**мЦивнджетдест**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetdest)
</dt> </dl>

 

