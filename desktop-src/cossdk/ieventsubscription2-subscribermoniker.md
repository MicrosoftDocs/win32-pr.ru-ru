---
description: Моникер подписчиков.
ms.assetid: d33d8c80-3251-4ec7-9cf3-d0b60d91ed5a
title: IEventSubscription2SubscriberMoniker, свойство
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IEventSubscription2.SubscriberMoniker
- IEventSubscription2.get_SubscriberMoniker
- IEventSubscription2.put_SubscriberMoniker
api_type:
- COM
api_location: ''
ms.openlocfilehash: 9496a3046b4bb0e99a88322892e557588a92aab8
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103807378"
---
# <a name="ieventsubscription2subscribermoniker-property"></a><span data-ttu-id="89d55-103">Свойство IEventSubscription2:: Субскрибермоникер</span><span class="sxs-lookup"><span data-stu-id="89d55-103">IEventSubscription2::SubscriberMoniker property</span></span>

<span data-ttu-id="89d55-104">Моникер подписчика.</span><span class="sxs-lookup"><span data-stu-id="89d55-104">The subscriber's moniker.</span></span>

<span data-ttu-id="89d55-105">Это свойство доступно для чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="89d55-105">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="89d55-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="89d55-106">Syntax</span></span>


```C++
HRESULT put_SubscriberMoniker(
  [in]          BSTR bstrMoniker
);

HRESULT get_SubscriberMoniker(
  [out, retval] BSTR *pbstrMoniker
);
```



## <a name="property-value"></a><span data-ttu-id="89d55-107">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="89d55-107">Property value</span></span>

<span data-ttu-id="89d55-108">Строка моникера, указывающая подписчика.</span><span class="sxs-lookup"><span data-stu-id="89d55-108">A moniker string specifying the subscriber.</span></span>

## <a name="error-codes"></a><span data-ttu-id="89d55-109">Коды ошибок</span><span class="sxs-lookup"><span data-stu-id="89d55-109">Error codes</span></span>

<span data-ttu-id="89d55-110">Этот метод может возвращать стандартные возвращаемые значения E \_ INVALIDARG, e \_ OUTOFMEMORY, e \_ непредвиденные, e \_ Fail и S \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="89d55-110">This method can return the standard return values E\_INVALIDARG, E\_OUTOFMEMORY, E\_UNEXPECTED, E\_FAIL, and S\_OK.</span></span>

## <a name="requirements"></a><span data-ttu-id="89d55-111">Требования</span><span class="sxs-lookup"><span data-stu-id="89d55-111">Requirements</span></span>



| <span data-ttu-id="89d55-112">Требование</span><span class="sxs-lookup"><span data-stu-id="89d55-112">Requirement</span></span> | <span data-ttu-id="89d55-113">Значение</span><span class="sxs-lookup"><span data-stu-id="89d55-113">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="89d55-114">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="89d55-114">Minimum supported client</span></span><br/> | <span data-ttu-id="89d55-115">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="89d55-115">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="89d55-116">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="89d55-116">Minimum supported server</span></span><br/> | <span data-ttu-id="89d55-117">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="89d55-117">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="89d55-118">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="89d55-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="89d55-119">**IEventSubscription2**</span><span class="sxs-lookup"><span data-stu-id="89d55-119">**IEventSubscription2**</span></span>](ieventsubscription2.md)
</dt> </dl>

 

 




