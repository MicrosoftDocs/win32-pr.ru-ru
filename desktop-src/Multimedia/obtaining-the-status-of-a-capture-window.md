---
title: Получение состояния окна записи
description: Получение состояния окна записи
ms.assetid: 5095dbd2-7cd4-48b6-bbb4-1f0bddfcfd06
keywords:
- макрос Капжетстатус
- Структура КАПСТАТУС
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8effedac3950f0f57aaa6e57ccd5a93fe3044982c3d6ec6d6bb69b56024a1255
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120038374"
---
# <a name="obtaining-the-status-of-a-capture-window"></a>Получение состояния окна записи

В следующем примере функция [SetWindowPos](/windows/win32/api/winuser/nf-winuser-setwindowpos) используется для установки размера окна отслеживания в соответствии с общими размерами входящего видеопотока на основе сведений, возвращаемых макросом [**Капжетстатус**](/windows/desktop/api/Vfw/nf-vfw-capgetstatus) в структуре [**капстатус**](/windows/win32/api/vfw/ns-vfw-capstatus) .


```C++
CAPSTATUS CapStatus;

capGetStatus(hWndC, &CapStatus, sizeof (CAPSTATUS)); 

SetWindowPos(hWndC, NULL, 0, 0, CapStatus.uiImageWidth, 
    CapStatus.uiImageHeight, SWP_NOZORDER | SWP_NOMOVE); 
```



## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Использование видеозаписи](using-video-capture.md)
</dt> </dl>

 

 