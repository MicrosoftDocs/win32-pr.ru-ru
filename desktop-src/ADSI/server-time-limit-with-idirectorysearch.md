---
title: Ограничение времени сервера на IDirectorySearch
description: Чтобы избежать использования всего времени ЦП и предотвращения выполнения других операций, укажите для параметра предельное время поиска небольшое значение, а затем повторно запустите приложение, если не удается создать отчет.
ms.assetid: 0fd4d8a2-36fc-4179-aeee-1cd3f3996e19
ms.tgt_platform: multiple
keywords:
- Ограничение времени сервера с помощью IDirectorySearch ADSI
- ADSI, поиск, IDirectorySearch, другие параметры поиска, ограничение времени сервера
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7ba5f80f9b83f20affaf7ad03de6b1609e9951b7
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103986088"
---
# <a name="server-time-limit-with-idirectorysearch"></a><span data-ttu-id="22dfe-105">Ограничение времени сервера на IDirectorySearch</span><span class="sxs-lookup"><span data-stu-id="22dfe-105">Server Time Limit with IDirectorySearch</span></span>

<span data-ttu-id="22dfe-106">При запросе поиска на занятом сервере может потребоваться запросить сервер для ограничения поиска до указанного времени.</span><span class="sxs-lookup"><span data-stu-id="22dfe-106">When you request a search on a busy server, you may want to request that the server to restrict the search to a specified time limit.</span></span> <span data-ttu-id="22dfe-107">Например, необходимо запустить приложение для создания еженедельного отчета на сервере, работающем рядом с его емкостью.</span><span class="sxs-lookup"><span data-stu-id="22dfe-107">For example, you want to run an application to generate a weekly report on a server that is running near its capacity.</span></span> <span data-ttu-id="22dfe-108">Чтобы избежать использования всего времени ЦП и предотвращения выполнения других операций, укажите для параметра предельное время поиска небольшое значение, а затем повторно запустите приложение, если не удается создать отчет.</span><span class="sxs-lookup"><span data-stu-id="22dfe-108">To avoid using all the CPU time and preventing other operations from running, specify the search time limit to a small value and then rerun the application later if it fails to generate the report.</span></span>

<span data-ttu-id="22dfe-109">Некоторые серверы могут накладывать собственное административное ограничение по времени.</span><span class="sxs-lookup"><span data-stu-id="22dfe-109">Some servers might impose their own administrative time limit.</span></span> <span data-ttu-id="22dfe-110">В таких случаях при указании предельного времени поиска, превышающего предел времени администратора, сервер игнорирует вашу спецификацию и вместо этого будет использовать его внутреннее предельное значение времени.</span><span class="sxs-lookup"><span data-stu-id="22dfe-110">In these cases, if you specify a search time limit value greater than the administrative time limit, the server will ignore your specification and use its internal time limit value instead.</span></span>

<span data-ttu-id="22dfe-111">Значение по умолчанию для ограничения по времени сервера не ограничено.</span><span class="sxs-lookup"><span data-stu-id="22dfe-111">The default for the server time limit is no limit.</span></span> <span data-ttu-id="22dfe-112">Чтобы установить предельное время сервера, установите параметр поиска **\_ сеарчпреф с \_ \_ ограничением по времени** на **адстипе \_ целочисленное** значение, которое содержит предельное время сервера в секундах в массиве [**\_ \_ сведений об ADS сеарчпреф**](/windows/desktop/api/Iads/ns-iads-ads_searchpref_info) , переданном в метод [**IDirectorySearch:: сетсеарчпреференце**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-setsearchpreference) .</span><span class="sxs-lookup"><span data-stu-id="22dfe-112">To set a server time limit, set an **ADS\_SEARCHPREF\_TIME\_LIMIT** search option with an **ADSTYPE\_INTEGER** value that contains the server time limit, in seconds, in the [**ADS\_SEARCHPREF\_INFO**](/windows/desktop/api/Iads/ns-iads-ads_searchpref_info) array passed to the [**IDirectorySearch::SetSearchPreference**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-setsearchpreference) method.</span></span> <span data-ttu-id="22dfe-113">Эта операция показана в следующем примере кода.</span><span class="sxs-lookup"><span data-stu-id="22dfe-113">This operation is shown in the following code example.</span></span> <span data-ttu-id="22dfe-114">Ограничение времени сервера, равное нулю, указывает на отсутствие ограничения по времени.</span><span class="sxs-lookup"><span data-stu-id="22dfe-114">A server time limit of zero indicates no time limit.</span></span>


```C++
ADS_SEARCHPREF_INFO SearchPref;
SearchPref.dwSearchPref = ADS_SEARCHPREF_TIME_LIMIT;
SearchPref.vValue.dwType = ADSTYPE_INTEGER;
SearchPref.vValue.Integer = 10;
```



 

 




