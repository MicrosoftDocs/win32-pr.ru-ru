---
description: Обратный вызов, уведомляющий основное приложение об ошибках, возвращенных связанным запросом.
MS-HAID: vspixengine.IPixErrorCallback\_ErrorListCallback\_DWORD\_Issue\_arr\_DWORD\_Issue\_arr
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'Метод Ипиксерроркаллбакк:: Еррорлисткаллбакк'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: B345846D-4853-4F6B-AB79-42265720451D
api_name:
- IPixErrorCallback.ErrorListCallback
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 91754cd7db13165efcb66e9bc87b8e4661842fce
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "105719249"
---
# <a name="span-idvspixengineipixerrorcallback_errorlistcallback_dword_issue_arr_dword_issue_arrspanipixerrorcallbackerrorlistcallback-method"></a><span data-ttu-id="895a5-103"><span id="vspixengine.ipixerrorcallback_errorlistcallback_dword_issue_arr_dword_issue_arr"></span>Метод Ипиксерроркаллбакк:: Еррорлисткаллбакк</span><span class="sxs-lookup"><span data-stu-id="895a5-103"><span id="vspixengine.ipixerrorcallback_errorlistcallback_dword_issue_arr_dword_issue_arr"></span>IPixErrorCallback::ErrorListCallback method</span></span>

<span data-ttu-id="895a5-104">Обратный вызов, уведомляющий основное приложение об ошибках, возвращенных связанным запросом.</span><span class="sxs-lookup"><span data-stu-id="895a5-104">A callback that notifies the host of errors returned by the associated request.</span></span>

## <a name="syntax"></a><span data-ttu-id="895a5-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="895a5-105">Syntax</span></span>


```C++
HRESULT ErrorListCallback(
   DWORD    count,
   Issue [] count0_errorList,
   DWORD    count,
   Issue [] count0_warningList
);
```

## <a name="parameters"></a><span data-ttu-id="895a5-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="895a5-106">Parameters</span></span>

<span data-ttu-id="895a5-107">*расчета* </span><span class="sxs-lookup"><span data-stu-id="895a5-107">*count* </span></span>  
<span data-ttu-id="895a5-108">Количество ошибок.</span><span class="sxs-lookup"><span data-stu-id="895a5-108">The number of errors.</span></span>

<span data-ttu-id="895a5-109">*count0 \_ сообщения* </span><span class="sxs-lookup"><span data-stu-id="895a5-109">*count0\_errorList* </span></span>  
<span data-ttu-id="895a5-110">Ошибки.</span><span class="sxs-lookup"><span data-stu-id="895a5-110">The errors.</span></span>

<span data-ttu-id="895a5-111">*расчета* </span><span class="sxs-lookup"><span data-stu-id="895a5-111">*count* </span></span>  
<span data-ttu-id="895a5-112">Число возникли.</span><span class="sxs-lookup"><span data-stu-id="895a5-112">The number of warningns.</span></span>

<span data-ttu-id="895a5-113">*count0 \_ варнинглист* </span><span class="sxs-lookup"><span data-stu-id="895a5-113">*count0\_warningList* </span></span>  
<span data-ttu-id="895a5-114">Предупреждения.</span><span class="sxs-lookup"><span data-stu-id="895a5-114">The warnings.</span></span>

## <a name="return-value"></a><span data-ttu-id="895a5-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="895a5-115">Return value</span></span>

<span data-ttu-id="895a5-116">Если этот метод завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="895a5-116">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="895a5-117">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="895a5-117">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="895a5-118">Требования</span><span class="sxs-lookup"><span data-stu-id="895a5-118">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="895a5-119">Header</span><span class="sxs-lookup"><span data-stu-id="895a5-119">Header</span></span></p></td><td><span data-ttu-id="895a5-120">Вспиксенгине. h</span><span class="sxs-lookup"><span data-stu-id="895a5-120">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="895a5-121"><span id="see_also"></span> См. также</span><span class="sxs-lookup"><span data-stu-id="895a5-121"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="895a5-122">**ипиксерроркаллбакк**</span><span class="sxs-lookup"><span data-stu-id="895a5-122">**IPixErrorCallback**</span></span>](/windows/desktop/direct3dtools/ipixerrorcallback)

 

 
