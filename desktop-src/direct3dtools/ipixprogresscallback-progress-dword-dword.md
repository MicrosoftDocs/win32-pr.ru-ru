---
description: Обратный вызов, уведомляющий узел о ходе выполнения связанного запроса.
MS-HAID: vspixengine.IPixProgressCallback\_Progress\_DWORD\_DWORD
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'Ипикспрогресскаллбакк: метод:P рогресс'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: BE74599B-C98F-4BDB-ACDF-641F77A35EEB
api_name:
- IPixProgressCallback.Progress
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 0379ad6fcb5f97825469c97af38453e55585d005
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "104422929"
---
# <a name="span-idvspixengineipixprogresscallback_progress_dword_dwordspanipixprogresscallbackprogress-method"></a><span data-ttu-id="e4954-103"><span id="vspixengine.ipixprogresscallback_progress_dword_dword"></span>Ипикспрогресскаллбакк: метод:P рогресс</span><span class="sxs-lookup"><span data-stu-id="e4954-103"><span id="vspixengine.ipixprogresscallback_progress_dword_dword"></span>IPixProgressCallback::Progress method</span></span>

<span data-ttu-id="e4954-104">Обратный вызов, уведомляющий узел о ходе выполнения связанного запроса.</span><span class="sxs-lookup"><span data-stu-id="e4954-104">A callback that notifies the host of the progress of an associated request.</span></span>

## <a name="syntax"></a><span data-ttu-id="e4954-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="e4954-105">Syntax</span></span>


```C++
HRESULT Progress(
   DWORD current,
   DWORD maxSize
);
```

## <a name="parameters"></a><span data-ttu-id="e4954-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="e4954-106">Parameters</span></span>

<span data-ttu-id="e4954-107">*данном* </span><span class="sxs-lookup"><span data-stu-id="e4954-107">*current* </span></span>  
<span data-ttu-id="e4954-108">Часть запроса завершена в виде количества завершенных шагов.</span><span class="sxs-lookup"><span data-stu-id="e4954-108">The portion of a request completed, as a count of the number of steps completed.</span></span>

<span data-ttu-id="e4954-109">*maxSize* </span><span class="sxs-lookup"><span data-stu-id="e4954-109">*maxSize* </span></span>  
<span data-ttu-id="e4954-110">Общее число шагов для выполнения запроса.</span><span class="sxs-lookup"><span data-stu-id="e4954-110">The total number of steps to complete the request.</span></span>

## <a name="return-value"></a><span data-ttu-id="e4954-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="e4954-111">Return value</span></span>

<span data-ttu-id="e4954-112">Если этот метод завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="e4954-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="e4954-113">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="e4954-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="e4954-114">Требования</span><span class="sxs-lookup"><span data-stu-id="e4954-114">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="e4954-115">Header</span><span class="sxs-lookup"><span data-stu-id="e4954-115">Header</span></span></p></td><td><span data-ttu-id="e4954-116">Вспиксенгине. h</span><span class="sxs-lookup"><span data-stu-id="e4954-116">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="e4954-117"><span id="see_also"></span> См. также</span><span class="sxs-lookup"><span data-stu-id="e4954-117"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="e4954-118">**ипикспрогресскаллбакк**</span><span class="sxs-lookup"><span data-stu-id="e4954-118">**IPixProgressCallback**</span></span>](/windows/desktop/direct3dtools/ipixprogresscallback)

 

 
