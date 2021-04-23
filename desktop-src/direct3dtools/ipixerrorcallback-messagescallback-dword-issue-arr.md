---
description: Обратный вызов, уведомляющий узел о сообщениях, возвращенных связанным запросом.
MS-HAID: vspixengine.IPixErrorCallback\_MessagesCallback\_DWORD\_Issue\_arr
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'Метод Ипиксерроркаллбакк:: Мессажескаллбакк'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 55343F63-BB58-4F57-884D-CEFE8AB57A27
api_name:
- IPixErrorCallback.MessagesCallback
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 2b95a95a6ef472f2603bfa6b21c85659634074a1
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "105719244"
---
# <a name="span-idvspixengineipixerrorcallback_messagescallback_dword_issue_arrspanipixerrorcallbackmessagescallback-method"></a><span data-ttu-id="fe726-103"><span id="vspixengine.ipixerrorcallback_messagescallback_dword_issue_arr"></span>Метод Ипиксерроркаллбакк:: Мессажескаллбакк</span><span class="sxs-lookup"><span data-stu-id="fe726-103"><span id="vspixengine.ipixerrorcallback_messagescallback_dword_issue_arr"></span>IPixErrorCallback::MessagesCallback method</span></span>

<span data-ttu-id="fe726-104">Обратный вызов, уведомляющий узел о сообщениях, возвращенных связанным запросом.</span><span class="sxs-lookup"><span data-stu-id="fe726-104">A callback that notifies the host of messages returned by the associated request.</span></span>

## <a name="syntax"></a><span data-ttu-id="fe726-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="fe726-105">Syntax</span></span>


```C++
HRESULT MessagesCallback(
   DWORD    count,
   Issue [] count0_messages
);
```

## <a name="parameters"></a><span data-ttu-id="fe726-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="fe726-106">Parameters</span></span>

<span data-ttu-id="fe726-107">*расчета* </span><span class="sxs-lookup"><span data-stu-id="fe726-107">*count* </span></span>  
<span data-ttu-id="fe726-108">Число сообщений.</span><span class="sxs-lookup"><span data-stu-id="fe726-108">The number of messages.</span></span>

<span data-ttu-id="fe726-109">*\_сообщения count0* </span><span class="sxs-lookup"><span data-stu-id="fe726-109">*count0\_messages* </span></span>  
<span data-ttu-id="fe726-110">Сообщения.</span><span class="sxs-lookup"><span data-stu-id="fe726-110">The messages.</span></span>

## <a name="return-value"></a><span data-ttu-id="fe726-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="fe726-111">Return value</span></span>

<span data-ttu-id="fe726-112">Если этот метод завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="fe726-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="fe726-113">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="fe726-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="fe726-114">Требования</span><span class="sxs-lookup"><span data-stu-id="fe726-114">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="fe726-115">Header</span><span class="sxs-lookup"><span data-stu-id="fe726-115">Header</span></span></p></td><td><span data-ttu-id="fe726-116">Вспиксенгине. h</span><span class="sxs-lookup"><span data-stu-id="fe726-116">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="fe726-117"><span id="see_also"></span> См. также</span><span class="sxs-lookup"><span data-stu-id="fe726-117"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="fe726-118">**ипиксерроркаллбакк**</span><span class="sxs-lookup"><span data-stu-id="fe726-118">**IPixErrorCallback**</span></span>](/windows/desktop/direct3dtools/ipixerrorcallback)

 

 
