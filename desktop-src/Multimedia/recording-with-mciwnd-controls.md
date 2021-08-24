---
title: Запись с помощью элементов управления МЦивнд
description: Запись с помощью элементов управления МЦивнд
ms.assetid: 65a57400-aeea-4a27-8d51-37d3d9e9bd55
keywords:
- Функция МЦивндкреате
- Макрос МЦивнднев
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4a02dfd62985b0267c685e6893512f977340f47f95801e8821d46005d5371397
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119805564"
---
# <a name="recording-with-mciwnd-controls"></a>Запись с помощью элементов управления МЦивнд

В следующем примере записывается звук звукозаписи с помощью встроенных элементов управления окна МЦивнд. В примере создается окно МЦивнд с помощью \_ стиля окна записи мЦивндф с функцией [**мЦивндкреате**](/windows/desktop/api/Vfw/nf-vfw-mciwndcreatea) для добавления кнопки **записи** на панель инструментов. Макрос [**мЦивнднев**](/windows/desktop/api/Vfw/nf-vfw-mciwndnew) указывает, что новый файл связан с окном мЦивнд и что устройство аудио аудио будет предоставлять свое содержимое. Вторая команда меню, IDM \_ савемЦивнд, позволяет пользователю сохранить запись и выбрать имя файла с помощью макроса [**мЦивндсаведиалог**](/windows/desktop/api/Vfw/nf-vfw-mciwndsavedialog) .


```C++
case WM_COMMAND: 
    switch (wParam) { 
    case IDM_CREATEMCIWND: 
        g_hwndMCIWnd = MCIWndCreate(hwnd, g_hinst, 
            WS_VISIBLE | MCIWNDF_RECORD, NULL); 
        MCIWndNew(g_hwndMCIWnd, "waveaudio"); 
        break;    
    case IDM_SAVEMCIWND: 
        MCIWndSaveDialog(g_hwndMCIWnd); 
        break; 
    } 
```



 

 




