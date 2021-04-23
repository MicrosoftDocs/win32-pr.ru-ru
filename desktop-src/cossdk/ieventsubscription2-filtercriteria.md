---
description: Критерии фильтра, управляющие подпиской.
ms.assetid: cfc3ba9e-0566-45fd-917f-34842b8ff377
title: 'Свойство IEventSubscription2:: параметром filterCriteria'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IEventSubscription2.FilterCriteria
- IEventSubscription2.get_FilterCriteria
- IEventSubscription2.put_FilterCriteria
api_type:
- COM
api_location: ''
ms.openlocfilehash: 1443a89433cff91a298e8c390fce8f1f64b99f1b
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104142388"
---
# <a name="ieventsubscription2filtercriteria-property"></a><span data-ttu-id="5a9b0-103">Свойство IEventSubscription2:: параметром filterCriteria</span><span class="sxs-lookup"><span data-stu-id="5a9b0-103">IEventSubscription2::FilterCriteria property</span></span>

<span data-ttu-id="5a9b0-104">Критерии фильтра, управляющие подпиской.</span><span class="sxs-lookup"><span data-stu-id="5a9b0-104">The filter criteria governing the subscription.</span></span>

<span data-ttu-id="5a9b0-105">Это свойство доступно для чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="5a9b0-105">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="5a9b0-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="5a9b0-106">Syntax</span></span>


```C++
HRESULT put_FilterCriteria(
  [in]          BSTR bstrFilterCriteria
);

HRESULT get_FilterCriteria(
  [out, retval] BSTR *pbstrFilterCriteria
);
```



## <a name="property-value"></a><span data-ttu-id="5a9b0-107">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="5a9b0-107">Property value</span></span>

<span data-ttu-id="5a9b0-108">Условия фильтра или CLSID для класса, реализующего [**ипублишерфилтер**](/windows/desktop/api/EventSys/nn-eventsys-ipublisherfilter).</span><span class="sxs-lookup"><span data-stu-id="5a9b0-108">The filter criteria or the CLSID for a class implementing [**IPublisherFilter**](/windows/desktop/api/EventSys/nn-eventsys-ipublisherfilter).</span></span>

## <a name="error-codes"></a><span data-ttu-id="5a9b0-109">Коды ошибок</span><span class="sxs-lookup"><span data-stu-id="5a9b0-109">Error codes</span></span>

<span data-ttu-id="5a9b0-110">Этот метод может возвращать стандартные возвращаемые значения E \_ INVALIDARG, e \_ OUTOFMEMORY, e \_ непредвиденные, e \_ Fail и S \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="5a9b0-110">This method can return the standard return values E\_INVALIDARG, E\_OUTOFMEMORY, E\_UNEXPECTED, E\_FAIL, and S\_OK.</span></span>

## <a name="requirements"></a><span data-ttu-id="5a9b0-111">Требования</span><span class="sxs-lookup"><span data-stu-id="5a9b0-111">Requirements</span></span>



| <span data-ttu-id="5a9b0-112">Требование</span><span class="sxs-lookup"><span data-stu-id="5a9b0-112">Requirement</span></span> | <span data-ttu-id="5a9b0-113">Значение</span><span class="sxs-lookup"><span data-stu-id="5a9b0-113">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="5a9b0-114">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="5a9b0-114">Minimum supported client</span></span><br/> | <span data-ttu-id="5a9b0-115">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="5a9b0-115">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="5a9b0-116">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="5a9b0-116">Minimum supported server</span></span><br/> | <span data-ttu-id="5a9b0-117">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="5a9b0-117">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="5a9b0-118">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="5a9b0-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5a9b0-119">**IEventSubscription2**</span><span class="sxs-lookup"><span data-stu-id="5a9b0-119">**IEventSubscription2**</span></span>](ieventsubscription2.md)
</dt> </dl>

 

 




