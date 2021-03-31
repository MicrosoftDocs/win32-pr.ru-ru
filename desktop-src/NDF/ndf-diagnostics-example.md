---
title: Пример диагностики NDF
description: В следующем примере показано, как запустить пользовательский интерфейс NDF и диагностировать подключение к веб-сайту http//www.microsoft.com.
ms.assetid: 6fe3af13-7216-4ac9-91ac-c497d25521ab
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 75fca4d54519988c3182b50a7c304f9c76a86392
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104067834"
---
# <a name="ndf-diagnostics-example"></a>Пример диагностики NDF

В следующем примере показано, как запустить пользовательский интерфейс NDF и диагностировать подключение к веб-сайту https://www.microsoft.com .


```C++
#include "ndfapi.h"

NDFHANDLE hNDF;
HRESULT hr = NdfCreateWebIncident (
                    L"https://www.microsoft.com",
                    &hNDF);

if(SUCCEEDED(hr))
{
    NdfExecuteDiagnosis(hNDF, NULL); // launches the NDF UI
                                     // the UI is not modal to the original window
    NdfCloseIncident(hNDF);
}
```



Пользовательский интерфейс NDF можно запустить в виде модального окна. Для этого измените второй параметр [**ндфексекутедиагносис**](/windows/desktop/api/Ndfapi/nf-ndfapi-ndfexecutediagnosis) с **null** на Handle (HWND) родительского окна.

Этот пример можно изменить для диагностики других областей сети. Для этого замените вызов [**ндфкреатевебинЦидент**](/windows/desktop/api/Ndfapi/nf-ndfapi-ndfcreatewebincident) одной из других функций создания инцидентов, таких как [**ндфкреатеднсинЦидент**](/windows/desktop/api/Ndfapi/nf-ndfapi-ndfcreatednsincident) или [**ндфкреатевинсоккинЦидент**](/windows/desktop/api/Ndfapi/nf-ndfapi-ndfcreatewinsockincident).

## <a name="related-topics"></a>См. также

<dl> <dt>

[**ндфклосеинЦидент**](/windows/desktop/api/Ndfapi/nf-ndfapi-ndfcloseincident)
</dt> <dt>

[**ндфкреатевебинЦидент**](/windows/desktop/api/Ndfapi/nf-ndfapi-ndfcreatewebincident)
</dt> <dt>

[**ндфексекутедиагносис**](/windows/desktop/api/Ndfapi/nf-ndfapi-ndfexecutediagnosis)
</dt> </dl>

 

 




