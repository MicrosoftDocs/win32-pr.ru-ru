---
description: Очищает состояние открываемого сеанса или текущего открытого сеанса.
ms.assetid: 8247AFA9-F471-4CCD-972D-D0C827E86880
title: Функция Вфддисплайсинкклосесессион (Вфдсинк. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WFDCloseDisplaySinkSession
api_type:
- DllExport
api_location:
- wifidisplay.dll
ms.openlocfilehash: 7697bc7ff1aa42569cf954b3f0b037f66ec67ded
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104544239"
---
# <a name="wfddisplaysinkclosesession-function"></a><span data-ttu-id="8c985-103">Функция Вфддисплайсинкклосесессион</span><span class="sxs-lookup"><span data-stu-id="8c985-103">WFDDisplaySinkCloseSession function</span></span>

<span data-ttu-id="8c985-104">Очищает состояние открываемого сеанса или текущего открытого сеанса.</span><span class="sxs-lookup"><span data-stu-id="8c985-104">Cleans up the state for the session being opened, or the currently open session.</span></span>

## <a name="syntax"></a><span data-ttu-id="8c985-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="8c985-105">Syntax</span></span>


```C++
DWORD WINAPI WFDCloseDisplaySinkSession(
  _In_ HANDLE hSessionHandle
);
```



## <a name="parameters"></a><span data-ttu-id="8c985-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="8c985-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8c985-107">*хсессионхандле* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="8c985-107">*hSessionHandle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8c985-108">Маркер, полученный по последнему вызову [**\_ \_ \_ \_ обратного вызова уведомления приемника WFD**](wfd-display-sink-notification-callback.md) , который включал в себя один.</span><span class="sxs-lookup"><span data-stu-id="8c985-108">The handle received via the most recent [**WFD\_DISPLAY\_SINK\_NOTIFICATION\_CALLBACK**](wfd-display-sink-notification-callback.md) invocation that included one.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8c985-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="8c985-109">Return value</span></span>

<span data-ttu-id="8c985-110">Если функция завершается успешно, возвращается значение ошибки \_ Success.</span><span class="sxs-lookup"><span data-stu-id="8c985-110">If the function succeeds, the return value is ERROR\_SUCCESS.</span></span>

## <a name="remarks"></a><span data-ttu-id="8c985-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="8c985-111">Remarks</span></span>

<span data-ttu-id="8c985-112">Приложение может вызвать эту функцию для завершения сеанса Miracast по любой причине.</span><span class="sxs-lookup"><span data-stu-id="8c985-112">Your app can call this function to terminate the Miracast session for any reason.</span></span> <span data-ttu-id="8c985-113">Приложению не требуется вызывать его при получении типа **дисконнектеднотификатион** в своем обратном вызове.</span><span class="sxs-lookup"><span data-stu-id="8c985-113">Your app is not required to call it when it receives the **DisconnectedNotification** type in its callback.</span></span>

## <a name="requirements"></a><span data-ttu-id="8c985-114">Требования</span><span class="sxs-lookup"><span data-stu-id="8c985-114">Requirements</span></span>



| <span data-ttu-id="8c985-115">Требование</span><span class="sxs-lookup"><span data-stu-id="8c985-115">Requirement</span></span> | <span data-ttu-id="8c985-116">Значение</span><span class="sxs-lookup"><span data-stu-id="8c985-116">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="8c985-117">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="8c985-117">Minimum supported client</span></span><br/> | <span data-ttu-id="8c985-118">\[Только Windows 8.1 Классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="8c985-118">Windows 8.1 \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="8c985-119">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="8c985-119">Minimum supported server</span></span><br/> | <span data-ttu-id="8c985-120">Только классические приложения Windows Server 2012 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="8c985-120">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="8c985-121">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="8c985-121">End of client support</span></span><br/>    | <span data-ttu-id="8c985-122">Windows 10</span><span class="sxs-lookup"><span data-stu-id="8c985-122">Windows 10</span></span><br/>                                                                      |
| <span data-ttu-id="8c985-123">Поддержка конца сервера</span><span class="sxs-lookup"><span data-stu-id="8c985-123">End of server support</span></span><br/>    | <span data-ttu-id="8c985-124">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="8c985-124">Windows Server 2016</span></span><br/>                                                             |
| <span data-ttu-id="8c985-125">Header</span><span class="sxs-lookup"><span data-stu-id="8c985-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="8c985-126"><dt>Вфдсинк. h</dt></span><span class="sxs-lookup"><span data-stu-id="8c985-126"><dt>Wfdsink.h</dt></span></span> </dl>       |
| <span data-ttu-id="8c985-127">Библиотека</span><span class="sxs-lookup"><span data-stu-id="8c985-127">Library</span></span><br/>                  | <dl> <span data-ttu-id="8c985-128"><dt>Вифидисплай. lib</dt></span><span class="sxs-lookup"><span data-stu-id="8c985-128"><dt>Wifidisplay.lib</dt></span></span> </dl> |
| <span data-ttu-id="8c985-129">DLL</span><span class="sxs-lookup"><span data-stu-id="8c985-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8c985-130"><dt>Wifidisplay.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8c985-130"><dt>Wifidisplay.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8c985-131">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="8c985-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8c985-132">**\_ \_ \_ обратный вызов уведомления приемника для дисплея WFD \_**</span><span class="sxs-lookup"><span data-stu-id="8c985-132">**WFD\_DISPLAY\_SINK\_NOTIFICATION\_CALLBACK**</span></span>](wfd-display-sink-notification-callback.md)
</dt> </dl>

 

 




