---
description: Эта функция принудительно завершает вызывающую программу, если она вызывается внутри выноски загрузчика. В противном случае он не действует.
ms.assetid: 5C10BF04-B7C7-4481-A184-FDD418FE5F52
title: Функция Лдрфастфаилинлоадеркаллаут
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LdrFastFailInLoaderCallout
api_type:
- DllExport
api_location:
- NTDll.dll
ms.openlocfilehash: f74b9cdc0aec666242a8267fab8d6255c75dc94b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105665156"
---
# <a name="ldrfastfailinloadercallout-function"></a><span data-ttu-id="bc5a3-104">Функция Лдрфастфаилинлоадеркаллаут</span><span class="sxs-lookup"><span data-stu-id="bc5a3-104">LdrFastFailInLoaderCallout function</span></span>

<span data-ttu-id="bc5a3-105">\[Некоторые сведения относятся к предварительно выпущенному продукту, который может быть значительно изменен перед коммерческой выпуском.</span><span class="sxs-lookup"><span data-stu-id="bc5a3-105">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="bc5a3-106">Майкрософт не дает никаких гарантий, явных или подразумеваемых, в отношении предоставленной здесь информации.\]</span><span class="sxs-lookup"><span data-stu-id="bc5a3-106">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="bc5a3-107">Эта функция принудительно завершает вызывающую программу, если она вызывается внутри выноски загрузчика.</span><span class="sxs-lookup"><span data-stu-id="bc5a3-107">This function forcefully terminates the calling program if it is invoked inside a loader callout.</span></span> <span data-ttu-id="bc5a3-108">В противном случае он не действует.</span><span class="sxs-lookup"><span data-stu-id="bc5a3-108">Otherwise, it has no effect.</span></span>

## <a name="syntax"></a><span data-ttu-id="bc5a3-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="bc5a3-109">Syntax</span></span>


```C++
VOID NTAPI LdrFastFailInLoaderCallout(void);
```



## <a name="parameters"></a><span data-ttu-id="bc5a3-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="bc5a3-110">Parameters</span></span>

<span data-ttu-id="bc5a3-111">У этой функции нет параметров.</span><span class="sxs-lookup"><span data-stu-id="bc5a3-111">This function has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="bc5a3-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="bc5a3-112">Return value</span></span>

<span data-ttu-id="bc5a3-113">Эта функция не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="bc5a3-113">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="bc5a3-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="bc5a3-114">Remarks</span></span>

<span data-ttu-id="bc5a3-115">Эта подпрограммы не перехватывает все возможные ситуации взаимоблокировки. поток внутри вызываемого загрузчика может получить блокировку, в то время как некоторый поток за пределами вызова загрузчика содержит одну и ту же блокировку и вызывает загрузчик.</span><span class="sxs-lookup"><span data-stu-id="bc5a3-115">This routine does not catch all potential deadlock cases; it is possible for a thread inside a loader callout to acquire a lock while some thread outside a loader callout holds the same lock and makes a call into the loader.</span></span> <span data-ttu-id="bc5a3-116">Иными словами, между блокировкой загрузчика и блокировкой клиента может быть инверсия порядка блокировок.</span><span class="sxs-lookup"><span data-stu-id="bc5a3-116">In other words, there can be a lock order inversion between the loader lock and a client lock.</span></span>

## <a name="requirements"></a><span data-ttu-id="bc5a3-117">Требования</span><span class="sxs-lookup"><span data-stu-id="bc5a3-117">Requirements</span></span>



| <span data-ttu-id="bc5a3-118">Требование</span><span class="sxs-lookup"><span data-stu-id="bc5a3-118">Requirement</span></span> | <span data-ttu-id="bc5a3-119">Значение</span><span class="sxs-lookup"><span data-stu-id="bc5a3-119">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="bc5a3-120">Библиотека</span><span class="sxs-lookup"><span data-stu-id="bc5a3-120">Library</span></span><br/> | <dl> <span data-ttu-id="bc5a3-121"><dt>NTDll. lib</dt></span><span class="sxs-lookup"><span data-stu-id="bc5a3-121"><dt>NTDll.lib</dt></span></span> </dl> |
| <span data-ttu-id="bc5a3-122">DLL</span><span class="sxs-lookup"><span data-stu-id="bc5a3-122">DLL</span></span><br/>     | <dl> <span data-ttu-id="bc5a3-123"><dt>NTDll.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bc5a3-123"><dt>NTDll.dll</dt></span></span> </dl> |



 

 




