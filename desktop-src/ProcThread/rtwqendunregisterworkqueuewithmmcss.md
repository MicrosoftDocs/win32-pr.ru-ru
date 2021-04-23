---
description: Завершает асинхронный запрос на отмену регистрации рабочей очереди с помощью задачи службы планировщика классов мультимедиа (MMCSS).
ms.assetid: 0E8F9BF6-AC1E-4FC0-BFAE-F292C4859F1F
title: Функция Ртвкендунрегистерворккуеуевисммксс
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- RtwqEndUnregisterWorkQueueWithMMCSS
api_type:
- DllExport
api_location:
- RTWorkQ.dll
ms.openlocfilehash: b55386b2a018b0e311a1d4dbb2084b136d49c2f6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103910355"
---
# <a name="rtwqendunregisterworkqueuewithmmcss-function"></a><span data-ttu-id="58517-103">Функция Ртвкендунрегистерворккуеуевисммксс</span><span class="sxs-lookup"><span data-stu-id="58517-103">RtwqEndUnregisterWorkQueueWithMMCSS function</span></span>

<span data-ttu-id="58517-104">Завершает асинхронный запрос на отмену регистрации рабочей очереди с помощью задачи службы планировщика классов мультимедиа (MMCSS).</span><span class="sxs-lookup"><span data-stu-id="58517-104">Completes an asynchronous request to unregister a work queue with a Multimedia Class Scheduler Service (MMCSS) task.</span></span>

## <a name="syntax"></a><span data-ttu-id="58517-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="58517-105">Syntax</span></span>


```C++
HRESULT WINAPI RtwqEndUnregisterWorkQueueWithMMCSS(
    IMFAsyncResult  *pResult 
);
```



## <a name="parameters"></a><span data-ttu-id="58517-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="58517-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="58517-107">*пресулт*</span><span class="sxs-lookup"><span data-stu-id="58517-107">*pResult*</span></span> 
</dt> <dd>

<span data-ttu-id="58517-108">Указатель на интерфейс [**имфасинкресулт**](/windows/win32/api/mfobjects/nn-mfobjects-imfasyncresult) .</span><span class="sxs-lookup"><span data-stu-id="58517-108">Pointer to the [**IMFAsyncResult**](/windows/win32/api/mfobjects/nn-mfobjects-imfasyncresult) interface.</span></span> <span data-ttu-id="58517-109">Передайте тот же указатель, который был получен объектом обратного вызова в методе [**иртвкасинккаллбакк:: Invoke**](/windows/win32/api/rtworkq/nf-rtworkq-irtwqasynccallback-invoke) .</span><span class="sxs-lookup"><span data-stu-id="58517-109">Pass in the same pointer that your callback object received in the [**IRtwqAsyncCallback::Invoke**](/windows/win32/api/rtworkq/nf-rtworkq-irtwqasynccallback-invoke) method.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="58517-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="58517-110">Return value</span></span>

<span data-ttu-id="58517-111">Если эта функция завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="58517-111">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="58517-112">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="58517-112">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="58517-113">Требования</span><span class="sxs-lookup"><span data-stu-id="58517-113">Requirements</span></span>



| <span data-ttu-id="58517-114">Требование</span><span class="sxs-lookup"><span data-stu-id="58517-114">Requirement</span></span> | <span data-ttu-id="58517-115">Значение</span><span class="sxs-lookup"><span data-stu-id="58517-115">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="58517-116">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="58517-116">Minimum supported client</span></span><br/> | <span data-ttu-id="58517-117">\[Только Windows 8.1 Классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="58517-117">Windows 8.1 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="58517-118">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="58517-118">Minimum supported server</span></span><br/> | <span data-ttu-id="58517-119">Только классические приложения Windows Server 2012 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="58517-119">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="58517-120">Header</span><span class="sxs-lookup"><span data-stu-id="58517-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="58517-121"><dt>Нет</dt></span><span class="sxs-lookup"><span data-stu-id="58517-121"><dt>None</dt></span></span> </dl>        |
| <span data-ttu-id="58517-122">Библиотека</span><span class="sxs-lookup"><span data-stu-id="58517-122">Library</span></span><br/>                  | <dl> <span data-ttu-id="58517-123"><dt>Ртворкк. lib</dt></span><span class="sxs-lookup"><span data-stu-id="58517-123"><dt>Rtworkq.lib</dt></span></span> </dl> |
| <span data-ttu-id="58517-124">DLL</span><span class="sxs-lookup"><span data-stu-id="58517-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="58517-125"><dt>RTWorkQ.dll</dt></span><span class="sxs-lookup"><span data-stu-id="58517-125"><dt>RTWorkQ.dll</dt></span></span> </dl> |



 

 
