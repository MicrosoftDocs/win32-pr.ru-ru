---
description: Идентификатор GUID приложения для объекта класса событий.
ms.assetid: 0d19183a-429c-4564-b6a5-f06481d27e00
title: 'Свойство IEventSubscription3:: Евентклассаппликатионид'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IEventSubscription3.EventClassApplicationID
- IEventSubscription3.get_EventClassApplicationID
- IEventSubscription3.put_EventClassApplicationID
api_type:
- COM
api_location: ''
ms.openlocfilehash: 3e80a8d8f557c80a1b2605328728260eb8ae7bd7
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104141821"
---
# <a name="ieventsubscription3eventclassapplicationid-property"></a><span data-ttu-id="4258c-103">Свойство IEventSubscription3:: Евентклассаппликатионид</span><span class="sxs-lookup"><span data-stu-id="4258c-103">IEventSubscription3::EventClassApplicationID property</span></span>

<span data-ttu-id="4258c-104">Идентификатор GUID приложения для объекта класса событий.</span><span class="sxs-lookup"><span data-stu-id="4258c-104">The application GUID of the event class object.</span></span>

<span data-ttu-id="4258c-105">Это свойство доступно для чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="4258c-105">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="4258c-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="4258c-106">Syntax</span></span>


```C++
HRESULT put_EventClassApplicationID(
  [in]          BSTR bstrEventClassApplicationID
);

HRESULT get_EventClassApplicationID(
  [out, retval] BSTR *pbstrEventClassApplicationID
);
```



## <a name="property-value"></a><span data-ttu-id="4258c-107">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="4258c-107">Property value</span></span>

<span data-ttu-id="4258c-108">Строка, содержащая идентификатор GUID приложения класса событий.</span><span class="sxs-lookup"><span data-stu-id="4258c-108">A string containing the GUID of the event class application.</span></span>

## <a name="error-codes"></a><span data-ttu-id="4258c-109">Коды ошибок</span><span class="sxs-lookup"><span data-stu-id="4258c-109">Error codes</span></span>

<span data-ttu-id="4258c-110">Этот метод может возвращать стандартные возвращаемые значения E \_ INVALIDARG, e \_ OUTOFMEMORY, e \_ непредвиденные, e \_ Fail и S \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="4258c-110">This method can return the standard return values E\_INVALIDARG, E\_OUTOFMEMORY, E\_UNEXPECTED, E\_FAIL, and S\_OK.</span></span>

## <a name="requirements"></a><span data-ttu-id="4258c-111">Требования</span><span class="sxs-lookup"><span data-stu-id="4258c-111">Requirements</span></span>



| <span data-ttu-id="4258c-112">Требование</span><span class="sxs-lookup"><span data-stu-id="4258c-112">Requirement</span></span> | <span data-ttu-id="4258c-113">Значение</span><span class="sxs-lookup"><span data-stu-id="4258c-113">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="4258c-114">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="4258c-114">Minimum supported client</span></span><br/> | <span data-ttu-id="4258c-115">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="4258c-115">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="4258c-116">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="4258c-116">Minimum supported server</span></span><br/> | <span data-ttu-id="4258c-117">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="4258c-117">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="4258c-118">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="4258c-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4258c-119">**IEventSubscription3**</span><span class="sxs-lookup"><span data-stu-id="4258c-119">**IEventSubscription3**</span></span>](ieventsubscription3.md)
</dt> </dl>

 

 




