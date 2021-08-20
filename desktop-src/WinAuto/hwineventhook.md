---
title: ХВИНЕВЕНСУК (Виндеф. h)
description: Используется для объявления функции обработчика событий окна.
ms.assetid: fa193e8e-46a8-46d4-83e1-e6274276b218
keywords:
- хвиневенсук
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1a26a2593af7db4520248b5ee319fd4143a79ab1393cef02365d1fe3ea8cc3f2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118994154"
---
# <a name="hwineventhook"></a>хвиневенсук

Используется для объявления функции обработчика событий окна.


```C++
typedef HANDLE HWINEVENTHOOK;
```



## <a name="remarks"></a>Remarks

Этот тип данных используется с функцией обратного вызова [*виневентпрок*](/windows/desktop/api/Winuser/nc-winuser-wineventproc) и функциями [**сетвиневенсук**](/windows/desktop/api/Winuser/nf-winuser-setwineventhook) и [**унхуквиневент**](/windows/desktop/api/Winuser/nf-winuser-unhookwinevent) .

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional \[только классические приложения\]<br/>                                                                    |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2003\]<br/>                                                                          |
| Распространяемые компоненты<br/>          | Active Accessibility 1,3 Windows NT 4,0 с пакетом обновления SP6 и более поздней версии и Windows 95<br/>                                   |
| Заголовок<br/>                   | <dl> <dt>виндеф. h (WINVER >= 0x0500) (include Windows. h)</dt> </dl> |



 

 





