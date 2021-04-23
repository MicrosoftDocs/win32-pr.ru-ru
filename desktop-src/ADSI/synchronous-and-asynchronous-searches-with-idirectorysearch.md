---
title: Синхронный и асинхронный поиск с помощью IDirectorySearch
description: При выполнении поиска с помощью интерфейса IDirectorySearch метод IDirectorySearch ExecuteSearch не отправляет запрос на поиск на сервер.
ms.assetid: c4387202-22a0-497a-af0a-20aa8ede905d
ms.tgt_platform: multiple
keywords:
- Синхронный и асинхронный поиск с помощью IDirectorySearch ADSI
- ADSI, поиск, IDirectorySearch, другие параметры поиска, синхронный и асинхронный поиск
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f369d45aaf4453d310c4bac2259bfa9cd089f567
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104410595"
---
# <a name="synchronous-and-asynchronous-searches-with-idirectorysearch"></a><span data-ttu-id="d080f-105">Синхронный и асинхронный поиск с помощью IDirectorySearch</span><span class="sxs-lookup"><span data-stu-id="d080f-105">Synchronous and Asynchronous Searches with IDirectorySearch</span></span>

<span data-ttu-id="d080f-106">При выполнении поиска с помощью интерфейса [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) метод [**IDirectorySearch:: ExecuteSearch**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-executesearch) не отправляет запрос на поиск на сервер.</span><span class="sxs-lookup"><span data-stu-id="d080f-106">When you perform a search using the [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) interface, the [**IDirectorySearch::ExecuteSearch**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-executesearch) method does not send the search request to the server.</span></span> <span data-ttu-id="d080f-107">Этот метод сохраняет только параметры поиска.</span><span class="sxs-lookup"><span data-stu-id="d080f-107">This method only saves the search parameters.</span></span> <span data-ttu-id="d080f-108">Запрос на поиск фактически отправляется при вызове [**IDirectorySearch:: жетфирстров**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getfirstrow) или [**IDirectorySearch:: GetNextRow**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getnextrow).</span><span class="sxs-lookup"><span data-stu-id="d080f-108">The search request is actually sent when you call [**IDirectorySearch::GetFirstRow**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getfirstrow) or [**IDirectorySearch::GetNextRow**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getnextrow).</span></span>

<span data-ttu-id="d080f-109">При поиске Active Directory основное различие между синхронным и асинхронным — при возвращении первой строки результата, то есть при возврате первого вызова [**жетфирстров**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getfirstrow) или [**GetNextRow**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getnextrow) .</span><span class="sxs-lookup"><span data-stu-id="d080f-109">For Active Directory searches, the primary difference between synchronous and asynchronous is when the first row of the result is returned, that is, when the first [**GetFirstRow**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getfirstrow) or [**GetNextRow**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getnextrow) call returns.</span></span>

<span data-ttu-id="d080f-110">В синхронном поиске, если разбиение по страницам не включено, первая строка возвращается, когда сервер конструирует и возвращает клиенту весь результирующий набор.</span><span class="sxs-lookup"><span data-stu-id="d080f-110">In a synchronous search, if paging is not enabled, the first row is returned when the server has constructed and returned the entire result set to the client.</span></span> <span data-ttu-id="d080f-111">Если разбиение по страницам включено, первая строка возвращается при возвращении первой страницы результирующего набора.</span><span class="sxs-lookup"><span data-stu-id="d080f-111">If paging is enabled, the first row is returned when the first page of the result set is returned.</span></span>

<span data-ttu-id="d080f-112">При асинхронном поиске, если разбиение по страницам не включено, первая строка возвращается при создании сервером первой строки результирующего набора.</span><span class="sxs-lookup"><span data-stu-id="d080f-112">In an asynchronous search, if paging is not enabled, the first row is returned when the server has constructed the first row of the result set.</span></span> <span data-ttu-id="d080f-113">Если разбиение по страницам включено, первая строка возвращается при возвращении первой страницы результирующего набора.</span><span class="sxs-lookup"><span data-stu-id="d080f-113">If paging is enabled, the first row is returned when the first page of the result set is returned.</span></span>

<span data-ttu-id="d080f-114">Тип поиска по умолчанию — синхронный.</span><span class="sxs-lookup"><span data-stu-id="d080f-114">The default search type is synchronous.</span></span> <span data-ttu-id="d080f-115">Чтобы указать асинхронный поиск, установите параметр **ADS \_ сеарчпреф \_ асинхронного** поиска с **адстипе \_ логическим** значением **true** в массиве [**\_ \_ сведений об ADS сеарчпреф**](/windows/desktop/api/Iads/ns-iads-ads_searchpref_info) , переданном в метод [**IDirectorySearch:: сетсеарчпреференце**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-setsearchpreference) .</span><span class="sxs-lookup"><span data-stu-id="d080f-115">To specify an asynchronous search, set an **ADS\_SEARCHPREF\_ASYNCHRONOUS** search option with an **ADSTYPE\_BOOLEAN** value of **TRUE** in the [**ADS\_SEARCHPREF\_INFO**](/windows/desktop/api/Iads/ns-iads-ads_searchpref_info) array passed to the [**IDirectorySearch::SetSearchPreference**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-setsearchpreference) method.</span></span> <span data-ttu-id="d080f-116">Эта операция показана в следующем примере кода.</span><span class="sxs-lookup"><span data-stu-id="d080f-116">This operation is shown in the following code example.</span></span>


```C++
ADS_SEARCHPREF_INFO SearchPref;
SearchPref.dwSearchPref = ADS_SEARCHPREF_ASYNCHRONOUS;
SearchPref.vValue.dwType = ADSTYPE_BOOLEAN;
SearchPref.vValue.Boolean = TRUE;
```



 

 




