---
title: ХВИНЕВЕНСУК (Виндеф. h)
description: Используется для объявления функции обработчика событий окна.
ms.assetid: fa193e8e-46a8-46d4-83e1-e6274276b218
keywords:
- хвиневенсук
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dbf526846916dfdd701f4f5ee98778dbbe9e66d9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105691848"
---
# <a name="hwineventhook"></a>хвиневенсук

Используется для объявления функции обработчика событий окна.


```C++
typedef HANDLE HWINEVENTHOOK;
```



## <a name="remarks"></a>Комментарии

Этот тип данных используется с функцией обратного вызова [*виневентпрок*](/windows/desktop/api/Winuser/nc-winuser-wineventproc) и функциями [**сетвиневенсук**](/windows/desktop/api/Winuser/nf-winuser-setwineventhook) и [**унхуквиневент**](/windows/desktop/api/Winuser/nf-winuser-unhookwinevent) .

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional \[только классические приложения\]<br/>                                                                    |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2003\]<br/>                                                                          |
| Распространяемые компоненты<br/>          | Active Accessibility 1,3 RDK в Windows NT 4,0 с пакетом обновления SP6 и более поздней версии и Windows 95<br/>                                   |
| Header<br/>                   | <dl> <dt>Виндеф. h (WINVER >= 0x0500) (включение Windows. h)</dt> </dl> |



 

 





