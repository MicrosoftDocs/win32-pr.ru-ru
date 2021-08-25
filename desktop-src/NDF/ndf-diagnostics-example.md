---
title: Пример диагностики NDF
description: В следующем примере показано, как запустить пользовательский интерфейс NDF и диагностировать подключение к веб-сайту http//www.microsoft.com.
ms.assetid: 6fe3af13-7216-4ac9-91ac-c497d25521ab
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7aa1971da12b7d707dc74b34497dff630ee8fdd8f93d5737ae3757bdde129fc9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119802374"
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

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[**ндфклосеинЦидент**](/windows/desktop/api/Ndfapi/nf-ndfapi-ndfcloseincident)
</dt> <dt>

[**ндфкреатевебинЦидент**](/windows/desktop/api/Ndfapi/nf-ndfapi-ndfcreatewebincident)
</dt> <dt>

[**ндфексекутедиагносис**](/windows/desktop/api/Ndfapi/nf-ndfapi-ndfexecutediagnosis)
</dt> </dl>

 

 




