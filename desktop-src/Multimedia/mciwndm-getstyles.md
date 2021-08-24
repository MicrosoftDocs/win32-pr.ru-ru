---
title: Сообщение MCIWNDM_GETSTYLES (VFW. h)
description: Сообщение МЦИВНДМ- \_ styles Получает флаги, указывающие текущие стили окна мЦивнд, используемые окном. Это сообщение можно отправить явно или с помощью макроса МЦивнджетстилес.
ms.assetid: cd34ba05-47cb-488e-a6c6-4ec1c0d25de8
keywords:
- сообщение MCIWNDM_GETSTYLES Windows мультимедиа
topic_type:
- apiref
api_name:
- MCIWNDM_GETSTYLES
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 036bd687c5d7828fade23994b9141488354added5ee38d38bafc9c5ce22a954c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119783294"
---
# <a name="mciwndm_getstyles-message"></a>Сообщение МЦИВНДМных \_ стилей

Сообщение **мЦивндм- \_ styles** Получает флаги, указывающие текущие стили окна мЦивнд, используемые окном. Это сообщение можно отправить явно или с помощью макроса [**мЦивнджетстилес**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetstyles) .


```C++
MCIWNDM_GETSTYLES 
wParam = 0; 
lParam = 0; 
```



## <a name="return-value"></a>Возвращаемое значение

Возвращает значение, представляющее текущие стили окна МЦивнд. Возвращаемое значение является побитовым оператором или в стилях окна МЦивнд (флаги МЦИВНДФ).

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional \[только классические приложения\]<br/>                       |
| Минимальная версия сервера<br/> | Windows 2000 Server \[только классические приложения\]<br/>                             |
| Заголовок<br/>                   | <dl> <dt>VFW. h</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**мЦивнджетстилес**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetstyles)
</dt> </dl>

 

 





