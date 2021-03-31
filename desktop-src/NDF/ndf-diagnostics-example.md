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
# <a name="ndf-diagnostics-example"></a><span data-ttu-id="dffd4-103">Пример диагностики NDF</span><span class="sxs-lookup"><span data-stu-id="dffd4-103">NDF Diagnostics Example</span></span>

<span data-ttu-id="dffd4-104">В следующем примере показано, как запустить пользовательский интерфейс NDF и диагностировать подключение к веб-сайту https://www.microsoft.com .</span><span class="sxs-lookup"><span data-stu-id="dffd4-104">The following example shows how to launch the NDF user interface and diagnose connectivity to the website https://www.microsoft.com.</span></span>


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



<span data-ttu-id="dffd4-105">Пользовательский интерфейс NDF можно запустить в виде модального окна.</span><span class="sxs-lookup"><span data-stu-id="dffd4-105">The NDF UI can be launched as a modal window.</span></span> <span data-ttu-id="dffd4-106">Для этого измените второй параметр [**ндфексекутедиагносис**](/windows/desktop/api/Ndfapi/nf-ndfapi-ndfexecutediagnosis) с **null** на Handle (HWND) родительского окна.</span><span class="sxs-lookup"><span data-stu-id="dffd4-106">To do so, change the second parameter of [**NdfExecuteDiagnosis**](/windows/desktop/api/Ndfapi/nf-ndfapi-ndfexecutediagnosis) from **NULL** to the handle (HWND) of the parent window.</span></span>

<span data-ttu-id="dffd4-107">Этот пример можно изменить для диагностики других областей сети.</span><span class="sxs-lookup"><span data-stu-id="dffd4-107">This example can be modified to diagnose other areas of networking.</span></span> <span data-ttu-id="dffd4-108">Для этого замените вызов [**ндфкреатевебинЦидент**](/windows/desktop/api/Ndfapi/nf-ndfapi-ndfcreatewebincident) одной из других функций создания инцидентов, таких как [**ндфкреатеднсинЦидент**](/windows/desktop/api/Ndfapi/nf-ndfapi-ndfcreatednsincident) или [**ндфкреатевинсоккинЦидент**](/windows/desktop/api/Ndfapi/nf-ndfapi-ndfcreatewinsockincident).</span><span class="sxs-lookup"><span data-stu-id="dffd4-108">To do so, replace the [**NdfCreateWebIncident**](/windows/desktop/api/Ndfapi/nf-ndfapi-ndfcreatewebincident) call with one of the other incident creation functions, such as [**NdfCreateDNSIncident**](/windows/desktop/api/Ndfapi/nf-ndfapi-ndfcreatednsincident) or [**NdfCreateWinSockIncident**](/windows/desktop/api/Ndfapi/nf-ndfapi-ndfcreatewinsockincident).</span></span>

## <a name="related-topics"></a><span data-ttu-id="dffd4-109">См. также</span><span class="sxs-lookup"><span data-stu-id="dffd4-109">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="dffd4-110">**ндфклосеинЦидент**</span><span class="sxs-lookup"><span data-stu-id="dffd4-110">**NdfCloseIncident**</span></span>](/windows/desktop/api/Ndfapi/nf-ndfapi-ndfcloseincident)
</dt> <dt>

[<span data-ttu-id="dffd4-111">**ндфкреатевебинЦидент**</span><span class="sxs-lookup"><span data-stu-id="dffd4-111">**NdfCreateWebIncident**</span></span>](/windows/desktop/api/Ndfapi/nf-ndfapi-ndfcreatewebincident)
</dt> <dt>

[<span data-ttu-id="dffd4-112">**ндфексекутедиагносис**</span><span class="sxs-lookup"><span data-stu-id="dffd4-112">**NdfExecuteDiagnosis**</span></span>](/windows/desktop/api/Ndfapi/nf-ndfapi-ndfexecutediagnosis)
</dt> </dl>

 

 




