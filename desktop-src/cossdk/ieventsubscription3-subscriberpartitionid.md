---
description: Идентификатор GUID раздела подписчика.
ms.assetid: 0b2411d3-cdc1-492c-a54f-ca3d3bd8b953
title: 'Свойство IEventSubscription3:: Субскриберпартитионид'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IEventSubscription3.SubscriberPartitionID
- IEventSubscription3.get_SubscriberPartitionID
- IEventSubscription3.put_SubscriberPartitionID
api_type:
- COM
api_location: ''
ms.openlocfilehash: b09c41ac1b3a90c3275daf7afa0cd90fe2bb905c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104262763"
---
# <a name="ieventsubscription3subscriberpartitionid-property"></a><span data-ttu-id="5593f-103">Свойство IEventSubscription3:: Субскриберпартитионид</span><span class="sxs-lookup"><span data-stu-id="5593f-103">IEventSubscription3::SubscriberPartitionID property</span></span>

<span data-ttu-id="5593f-104">Идентификатор GUID раздела подписчика.</span><span class="sxs-lookup"><span data-stu-id="5593f-104">The partition GUID of the subscriber.</span></span>

<span data-ttu-id="5593f-105">Это свойство доступно для чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="5593f-105">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="5593f-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="5593f-106">Syntax</span></span>


```C++
HRESULT put_SubscriberPartitionID(
  [in]          BSTR bstrSubscriberPartitionID
);

HRESULT get_SubscriberPartitionID(
  [out, retval] BSTR *pbstrSubscriberPartitionID
);
```



## <a name="property-value"></a><span data-ttu-id="5593f-107">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="5593f-107">Property value</span></span>

<span data-ttu-id="5593f-108">Строка, содержащая идентификатор GUID секции подписчика.</span><span class="sxs-lookup"><span data-stu-id="5593f-108">A string containing the GUID of the subscriber partition.</span></span>

## <a name="error-codes"></a><span data-ttu-id="5593f-109">Коды ошибок</span><span class="sxs-lookup"><span data-stu-id="5593f-109">Error codes</span></span>

<span data-ttu-id="5593f-110">Этот метод может возвращать стандартные возвращаемые значения E \_ INVALIDARG, e \_ OUTOFMEMORY, e \_ непредвиденные, e \_ Fail и S \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="5593f-110">This method can return the standard return values E\_INVALIDARG, E\_OUTOFMEMORY, E\_UNEXPECTED, E\_FAIL, and S\_OK.</span></span>

## <a name="requirements"></a><span data-ttu-id="5593f-111">Требования</span><span class="sxs-lookup"><span data-stu-id="5593f-111">Requirements</span></span>



| <span data-ttu-id="5593f-112">Требование</span><span class="sxs-lookup"><span data-stu-id="5593f-112">Requirement</span></span> | <span data-ttu-id="5593f-113">Значение</span><span class="sxs-lookup"><span data-stu-id="5593f-113">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="5593f-114">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="5593f-114">Minimum supported client</span></span><br/> | <span data-ttu-id="5593f-115">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="5593f-115">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="5593f-116">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="5593f-116">Minimum supported server</span></span><br/> | <span data-ttu-id="5593f-117">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="5593f-117">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="5593f-118">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="5593f-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5593f-119">**IEventSubscription3**</span><span class="sxs-lookup"><span data-stu-id="5593f-119">**IEventSubscription3**</span></span>](ieventsubscription3.md)
</dt> </dl>

 

 




