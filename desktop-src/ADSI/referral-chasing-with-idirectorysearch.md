---
title: Отслеживание ссылок с помощью IDirectorySearch
description: Ссылка — это механизм, который сервер каталогов использует для направления клиента на другой сервер, если он не содержит достаточно данных о объекте, запрошенном запросом.
ms.assetid: ef97eafd-5227-4dd7-9f8a-6b4591261f79
ms.tgt_platform: multiple
keywords:
- Отслеживание ссылок с помощью IDirectorySearch ADSI
- ADSI, поиск, IDirectorySearch, другие параметры поиска, отслеживание ссылок
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9fae76139dc1a68c9345cd7a7b3bb894a50a2d7b
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/21/2020
ms.locfileid: "103987882"
---
# <a name="referral-chasing-with-idirectorysearch"></a><span data-ttu-id="dad8c-105">Отслеживание ссылок с помощью IDirectorySearch</span><span class="sxs-lookup"><span data-stu-id="dad8c-105">Referral Chasing with IDirectorySearch</span></span>

<span data-ttu-id="dad8c-106">Ссылка — это механизм, который сервер каталогов использует для направления клиента на другой сервер, если он не содержит достаточно данных о объекте, запрошенном запросом.</span><span class="sxs-lookup"><span data-stu-id="dad8c-106">A referral is the mechanism that a directory server uses to direct a client to another server when it does not contain sufficient data about the object requested by a query.</span></span>

<span data-ttu-id="dad8c-107">При поиске на одном уровне или в поддереве ссылки возвращаются только для известных, немедленно подчиненного домена, схемы или контейнеров конфигурации. Это значит, что дочерние домены являются прямыми потомками.</span><span class="sxs-lookup"><span data-stu-id="dad8c-107">In a one-level or subtree search, referrals are returned for known, immediately subordinate domain, schema, or configuration containers only; that is, child domains that are direct descendants.</span></span> <span data-ttu-id="dad8c-108">Дополнительные сведения см. в разделе [область поиска](/windows/desktop/AD/search-scope).</span><span class="sxs-lookup"><span data-stu-id="dad8c-108">For more information, see [Search Scope](/windows/desktop/AD/search-scope).</span></span>

<span data-ttu-id="dad8c-109">В каталоге не все данные доступны на одном сервере, вместо этого они распределяются по нескольким различным серверам по сети.</span><span class="sxs-lookup"><span data-stu-id="dad8c-109">In a directory, not all data is available on a single server, rather, it is distributed over several different servers across the network.</span></span> <span data-ttu-id="dad8c-110">Если серверы совместно используют данные, предоставляемые другими серверами, они могут предоставить клиенту ссылки, если запрошенный запрос не может быть разрешен на сервере-источнике.</span><span class="sxs-lookup"><span data-stu-id="dad8c-110">If the servers share the data that other servers can provide, they can provide referrals to a client when a requested query cannot be resolved on the originating server.</span></span> <span data-ttu-id="dad8c-111">Например, когда клиент запрашивает у сервера A запрос к объекту пользователя (U), может предлагаться, что клиент продолжит поиск на сервере B, если U не находится в, но определен как на B. Клиент имеет возможность использовать ссылку или нет.</span><span class="sxs-lookup"><span data-stu-id="dad8c-111">For example, when a client asks Server A to query a user object (U), then A can suggest that the client continue the search on Server B if U does not reside on A, but is identified to be on B. The client has the choice to pursue the referral or not.</span></span> <span data-ttu-id="dad8c-112">Ссылки освобождают клиента от необходимости обладать предыдущими знаниями о возможности каждого сервера, но клиент должен указать тип ссылок, которые должен выполнить сервер.</span><span class="sxs-lookup"><span data-stu-id="dad8c-112">Referrals free the client from having to possess previous knowledge of the capability of each server, but the client must specify the type of referrals a server should perform.</span></span>

<span data-ttu-id="dad8c-113">Чтобы включить или отключить отслеживание ссылок, установите параметр поиска **ADS \_ сеарчпреф \_ \_** вести поиск по ссылкам, используя **\_ целочисленное значение адстипе** , которое содержит одну из [**баннеров. \_ \_ \_**](/windows/win32/api/iads/ne-iads-ads_chase_referrals_enum) перечисление значений перечисления см. в массиве [**\_ \_ сведений об ADS сеарчпреф**](/windows/desktop/api/Iads/ns-iads-ads_searchpref_info) , переданном в метод [**IDirectorySearch:: сетсеарчпреференце**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-setsearchpreference) .</span><span class="sxs-lookup"><span data-stu-id="dad8c-113">To enable or disable referral chasing, set an **ADS\_SEARCHPREF\_CHASE\_REFERRALS** search option with an **ADSTYPE\_INTEGER** value that contains one of the [**ADS\_CHASE\_REFERRALS\_ENUM**](/windows/win32/api/iads/ne-iads-ads_chase_referrals_enum) enumeration values in the [**ADS\_SEARCHPREF\_INFO**](/windows/desktop/api/Iads/ns-iads-ads_searchpref_info) array passed to the [**IDirectorySearch::SetSearchPreference**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-setsearchpreference) method.</span></span>

<span data-ttu-id="dad8c-114">В следующем примере кода показано, как включить ссылки «след».</span><span class="sxs-lookup"><span data-stu-id="dad8c-114">The following code example shows how to enable chase referrals.</span></span>


```C++
ADS_SEARCHPREF_INFO SearchPref;
SearchPref.dwSearchPref = ADS_SEARCHPREF_CHASE_REFERRALS;
SearchPref.vValue.dwType = ADSTYPE_INTEGER;
SearchPref.vValue.Integer = ADS_CHASE_REFERRALS_ALWAYS;
```



<span data-ttu-id="dad8c-115">Дополнительные сведения о ссылках в Active Directory см. в разделе [ссылки](/windows/desktop/AD/referrals).</span><span class="sxs-lookup"><span data-stu-id="dad8c-115">For more information about referrals in Active Directory, see [Referrals](/windows/desktop/AD/referrals).</span></span>

 

 