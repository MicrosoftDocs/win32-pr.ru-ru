---
description: Отменяет подписывание уведомлений об изменении состояния службы.
ms.assetid: 8c04ebf7-4d61-4617-b120-dbe26b2f9ad2
title: Функция Унсубскрибесервицечанженотификатионс (Винсвкп. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- UnsubscribeServiceChangeNotifications
api_type:
- DllExport
api_location:
- SecHost.dll
- API-MS-Win-Service-Private-L1-1-0.dll
- API-MS-Win-Service-Private-L1-1-1.dll
- Advapi32.dll
- API-MS-Win-Service-Private-L1-1-2.dll
ms.openlocfilehash: ebecfb133172c9c7a56ed6d28f7ad6b395d8afce
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103911244"
---
# <a name="unsubscribeservicechangenotifications-function"></a><span data-ttu-id="ea1db-103">Функция Унсубскрибесервицечанженотификатионс</span><span class="sxs-lookup"><span data-stu-id="ea1db-103">UnsubscribeServiceChangeNotifications function</span></span>

<span data-ttu-id="ea1db-104">Отменяет подписывание уведомлений об изменении состояния службы.</span><span class="sxs-lookup"><span data-stu-id="ea1db-104">Unsubscribes from service status change notifications.</span></span> <span data-ttu-id="ea1db-105">Эта функция использует подписки, возвращаемые функцией [**субскрибесервицечанженотификатионс**](subscribeservicechangenotifications.md).</span><span class="sxs-lookup"><span data-stu-id="ea1db-105">This function uses subscriptions returned by [**SubscribeServiceChangeNotifications**](subscribeservicechangenotifications.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="ea1db-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="ea1db-106">Syntax</span></span>


```C++
 VOID WINAPI UnsubscribeServiceChangeNotifications(
  _In_ PSC_NOTIFICATION_REGISTRATION pSubscription
);
```



## <a name="parameters"></a><span data-ttu-id="ea1db-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="ea1db-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ea1db-108">*псубскриптион* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="ea1db-108">*pSubscription* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ea1db-109">Указатель на подписку, для которой необходимо отменить подписку.</span><span class="sxs-lookup"><span data-stu-id="ea1db-109">A pointer to the subscription to be unsubscribed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ea1db-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="ea1db-110">Return value</span></span>

<span data-ttu-id="ea1db-111">Эта функция не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="ea1db-111">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="ea1db-112">Комментарии</span><span class="sxs-lookup"><span data-stu-id="ea1db-112">Remarks</span></span>

<span data-ttu-id="ea1db-113">**Унсубскрибесервицечанженотификатионс** не возвращает, пока не будут завершены необработанные Обратные вызовы в процессе.</span><span class="sxs-lookup"><span data-stu-id="ea1db-113">**UnsubscribeServiceChangeNotifications** does not return until outstanding in-process callbacks are complete.</span></span> <span data-ttu-id="ea1db-114">Поэтому нельзя вызвать **унсубскрибесервицечанженотификатионс** в обратном вызове, не вызывая взаимоблокировки.</span><span class="sxs-lookup"><span data-stu-id="ea1db-114">So, you cannot call **UnsubscribeServiceChangeNotifications** within the callback without causing a deadlock.</span></span>

## <a name="requirements"></a><span data-ttu-id="ea1db-115">Требования</span><span class="sxs-lookup"><span data-stu-id="ea1db-115">Requirements</span></span>



| <span data-ttu-id="ea1db-116">Требование</span><span class="sxs-lookup"><span data-stu-id="ea1db-116">Requirement</span></span> | <span data-ttu-id="ea1db-117">Значение</span><span class="sxs-lookup"><span data-stu-id="ea1db-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="ea1db-118">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="ea1db-118">Minimum supported client</span></span><br/> | <span data-ttu-id="ea1db-119">\[Только классические приложения Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="ea1db-119">Windows 8 \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="ea1db-120">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="ea1db-120">Minimum supported server</span></span><br/> | <span data-ttu-id="ea1db-121">\[Только для настольных приложений Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="ea1db-121">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="ea1db-122">Header</span><span class="sxs-lookup"><span data-stu-id="ea1db-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="ea1db-123"><dt>Винсвкп. h</dt></span><span class="sxs-lookup"><span data-stu-id="ea1db-123"><dt>Winsvcp.h</dt></span></span> </dl>   |
| <span data-ttu-id="ea1db-124">DLL</span><span class="sxs-lookup"><span data-stu-id="ea1db-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ea1db-125"><dt>SecHost.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ea1db-125"><dt>SecHost.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ea1db-126">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="ea1db-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ea1db-127">**CreateService**</span><span class="sxs-lookup"><span data-stu-id="ea1db-127">**CreateService**</span></span>](/windows/desktop/api/Winsvc/nf-winsvc-createservicea)
</dt> <dt>

[<span data-ttu-id="ea1db-128">**OpenService**</span><span class="sxs-lookup"><span data-stu-id="ea1db-128">**OpenService**</span></span>](/windows/desktop/api/Winsvc/nf-winsvc-openservicea)
</dt> <dt>

[<span data-ttu-id="ea1db-129">**OpenSCManager**</span><span class="sxs-lookup"><span data-stu-id="ea1db-129">**OpenSCManager**</span></span>](/windows/desktop/api/Winsvc/nf-winsvc-openscmanagera)
</dt> <dt>

[<span data-ttu-id="ea1db-130">**субскрибесервицечанженотификатионс**</span><span class="sxs-lookup"><span data-stu-id="ea1db-130">**SubscribeServiceChangeNotifications**</span></span>](subscribeservicechangenotifications.md)
</dt> <dt>

[<span data-ttu-id="ea1db-131">**куерисервицединамиЦинформатион**</span><span class="sxs-lookup"><span data-stu-id="ea1db-131">**QueryServiceDynamicInformation**</span></span>](/windows/desktop/api/Winsvc/nf-winsvc-queryservicedynamicinformation)
</dt> </dl>

 

 




