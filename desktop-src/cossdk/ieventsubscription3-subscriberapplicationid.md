---
description: Идентификатор GUID приложения подписчика.
ms.assetid: 46c91cae-ca31-4eac-baa8-d36910917f0f
title: 'Свойство IEventSubscription3:: Субскрибераппликатионид'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IEventSubscription3.SubscriberApplicationID
- IEventSubscription3.get_SubscriberApplicationID
- IEventSubscription3.put_SubscriberApplicationID
api_type:
- COM
api_location: ''
ms.openlocfilehash: c2e726d97821a7a7143f4971a4918227235adb9c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104262598"
---
# <a name="ieventsubscription3subscriberapplicationid-property"></a><span data-ttu-id="2e5d8-103">Свойство IEventSubscription3:: Субскрибераппликатионид</span><span class="sxs-lookup"><span data-stu-id="2e5d8-103">IEventSubscription3::SubscriberApplicationID property</span></span>

<span data-ttu-id="2e5d8-104">Идентификатор GUID приложения подписчика.</span><span class="sxs-lookup"><span data-stu-id="2e5d8-104">The application GUID of the subscriber.</span></span>

<span data-ttu-id="2e5d8-105">Это свойство доступно для чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="2e5d8-105">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="2e5d8-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="2e5d8-106">Syntax</span></span>


```C++
HRESULT put_SubscriberApplicationID(
  [in]          BSTR bstrSubscriberApplicationID
);

HRESULT get_SubscriberApplicationID(
  [out, retval] BSTR *pbstrSubscriberApplicationID
);
```



## <a name="property-value"></a><span data-ttu-id="2e5d8-107">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="2e5d8-107">Property value</span></span>

<span data-ttu-id="2e5d8-108">Строка, содержащая идентификатор GUID приложения подписчика.</span><span class="sxs-lookup"><span data-stu-id="2e5d8-108">A string containing the GUID of the subscriber application.</span></span>

## <a name="error-codes"></a><span data-ttu-id="2e5d8-109">Коды ошибок</span><span class="sxs-lookup"><span data-stu-id="2e5d8-109">Error codes</span></span>

<span data-ttu-id="2e5d8-110">Этот метод может возвращать стандартные возвращаемые значения E \_ INVALIDARG, e \_ OUTOFMEMORY, e \_ непредвиденные, e \_ Fail и S \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="2e5d8-110">This method can return the standard return values E\_INVALIDARG, E\_OUTOFMEMORY, E\_UNEXPECTED, E\_FAIL, and S\_OK.</span></span>

## <a name="requirements"></a><span data-ttu-id="2e5d8-111">Требования</span><span class="sxs-lookup"><span data-stu-id="2e5d8-111">Requirements</span></span>



| <span data-ttu-id="2e5d8-112">Требование</span><span class="sxs-lookup"><span data-stu-id="2e5d8-112">Requirement</span></span> | <span data-ttu-id="2e5d8-113">Значение</span><span class="sxs-lookup"><span data-stu-id="2e5d8-113">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="2e5d8-114">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="2e5d8-114">Minimum supported client</span></span><br/> | <span data-ttu-id="2e5d8-115">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="2e5d8-115">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="2e5d8-116">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="2e5d8-116">Minimum supported server</span></span><br/> | <span data-ttu-id="2e5d8-117">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="2e5d8-117">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="2e5d8-118">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="2e5d8-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2e5d8-119">**IEventSubscription3**</span><span class="sxs-lookup"><span data-stu-id="2e5d8-119">**IEventSubscription3**</span></span>](ieventsubscription3.md)
</dt> </dl>

 

 




