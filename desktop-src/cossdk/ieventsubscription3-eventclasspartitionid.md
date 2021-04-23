---
description: Идентификатор GUID раздела объекта класса событий.
ms.assetid: 154849ac-350c-4b2f-bb51-ac6973f0a8fa
title: 'Свойство IEventSubscription3:: Евенткласспартитионид'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IEventSubscription3.EventClassPartitionID
- IEventSubscription3.get_EventClassPartitionID
- IEventSubscription3.put_EventClassPartitionID
api_type:
- COM
api_location: ''
ms.openlocfilehash: d41d3e2a170deffb73f1f533226421d88f150c01
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104539305"
---
# <a name="ieventsubscription3eventclasspartitionid-property"></a><span data-ttu-id="e6e53-103">Свойство IEventSubscription3:: Евенткласспартитионид</span><span class="sxs-lookup"><span data-stu-id="e6e53-103">IEventSubscription3::EventClassPartitionID property</span></span>

<span data-ttu-id="e6e53-104">Идентификатор GUID раздела объекта класса событий.</span><span class="sxs-lookup"><span data-stu-id="e6e53-104">The partition GUID of the event class object.</span></span>

<span data-ttu-id="e6e53-105">Это свойство доступно для чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="e6e53-105">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="e6e53-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="e6e53-106">Syntax</span></span>


```C++
HRESULT put_EventClassPartitionID(
  [in]          BSTR bstrEventClassPartitionID
);

HRESULT get_EventClassPartitionID(
  [out, retval] BSTR *pbstrEventClassPartitionID
);
```



## <a name="property-value"></a><span data-ttu-id="e6e53-107">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="e6e53-107">Property value</span></span>

<span data-ttu-id="e6e53-108">Строка, содержащая идентификатор GUID Секции класса событий.</span><span class="sxs-lookup"><span data-stu-id="e6e53-108">A string containing the GUID of the event class partition.</span></span>

## <a name="error-codes"></a><span data-ttu-id="e6e53-109">Коды ошибок</span><span class="sxs-lookup"><span data-stu-id="e6e53-109">Error codes</span></span>

<span data-ttu-id="e6e53-110">Этот метод может возвращать стандартные возвращаемые значения E \_ INVALIDARG, e \_ OUTOFMEMORY, e \_ непредвиденные, e \_ Fail и S \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="e6e53-110">This method can return the standard return values E\_INVALIDARG, E\_OUTOFMEMORY, E\_UNEXPECTED, E\_FAIL, and S\_OK.</span></span>

## <a name="requirements"></a><span data-ttu-id="e6e53-111">Требования</span><span class="sxs-lookup"><span data-stu-id="e6e53-111">Requirements</span></span>



| <span data-ttu-id="e6e53-112">Требование</span><span class="sxs-lookup"><span data-stu-id="e6e53-112">Requirement</span></span> | <span data-ttu-id="e6e53-113">Значение</span><span class="sxs-lookup"><span data-stu-id="e6e53-113">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="e6e53-114">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="e6e53-114">Minimum supported client</span></span><br/> | <span data-ttu-id="e6e53-115">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="e6e53-115">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="e6e53-116">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="e6e53-116">Minimum supported server</span></span><br/> | <span data-ttu-id="e6e53-117">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="e6e53-117">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="e6e53-118">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="e6e53-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e6e53-119">**IEventSubscription3**</span><span class="sxs-lookup"><span data-stu-id="e6e53-119">**IEventSubscription3**</span></span>](ieventsubscription3.md)
</dt> </dl>

 

 




