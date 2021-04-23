---
description: Вызывает метод, который вызывается, когда заданная асинхронная операция сообщает о ходе выполнения.
ms.assetid: FB60DDC0-7521-4999-8DD8-175556004198
title: 'Иасинкоператионвиспрогресскомплетедхандлер<TResult, TProgress>:: Invoke метод'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAsyncOperationWithProgressCompletedHandler<TResult,TProgress>.Invoke
api_type:
- COM
api_location: ''
ms.openlocfilehash: 469686cbd96dedc7f816fdd1f482d3474362688e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104145130"
---
# <a name="iasyncoperationwithprogresscompletedhandlertresulttprogressinvoke-method"></a><span data-ttu-id="cd137-103">Иасинкоператионвиспрогресскомплетедхандлер<TResult, TProgress>:: Invoke метод</span><span class="sxs-lookup"><span data-stu-id="cd137-103">IAsyncOperationWithProgressCompletedHandler<TResult,TProgress>::Invoke method</span></span>

<span data-ttu-id="cd137-104">Вызывает метод, который вызывается, когда заданная асинхронная операция сообщает о ходе выполнения.</span><span class="sxs-lookup"><span data-stu-id="cd137-104">Invokes the method that is called when the specified asynchronous operation reports progress.</span></span>

## <a name="syntax"></a><span data-ttu-id="cd137-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="cd137-105">Syntax</span></span>


```C++
HRESULT Invoke(
  [in] IAsyncOperationWithProgress<TResult,TProgress> *asyncInfo
);
```



## <a name="parameters"></a><span data-ttu-id="cd137-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="cd137-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cd137-107">*асинЦинфо* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="cd137-107">*asyncInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cd137-108">Введите: \**[**IAsyncOperationWithProgress<TResult, TProgress>**](/previous-versions//br205807(v=vs.85)) \** _</span><span class="sxs-lookup"><span data-stu-id="cd137-108">Type: \**[**IAsyncOperationWithProgress<TResult,TProgress>**](/previous-versions//br205807(v=vs.85))\** _</span></span>

<span data-ttu-id="cd137-109">Асинхронное действие, которое сообщает о завершении.</span><span class="sxs-lookup"><span data-stu-id="cd137-109">The asynchronous action that reports completion.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cd137-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="cd137-110">Return value</span></span>

<span data-ttu-id="cd137-111">Тип: _ *HRESULT*\*</span><span class="sxs-lookup"><span data-stu-id="cd137-111">Type: _ *HRESULT*\*</span></span>

<span data-ttu-id="cd137-112">Если этот метод завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="cd137-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="cd137-113">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="cd137-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="cd137-114">Требования</span><span class="sxs-lookup"><span data-stu-id="cd137-114">Requirements</span></span>



| <span data-ttu-id="cd137-115">Требование</span><span class="sxs-lookup"><span data-stu-id="cd137-115">Requirement</span></span> | <span data-ttu-id="cd137-116">Значение</span><span class="sxs-lookup"><span data-stu-id="cd137-116">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="cd137-117">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="cd137-117">Minimum supported client</span></span><br/> | <span data-ttu-id="cd137-118">Windows 8</span><span class="sxs-lookup"><span data-stu-id="cd137-118">Windows 8</span></span><br/>           |
| <span data-ttu-id="cd137-119">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="cd137-119">Minimum supported server</span></span><br/> | <span data-ttu-id="cd137-120">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="cd137-120">Windows Server 2012</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="cd137-121">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="cd137-121">See also</span></span>

<dl> <dt>

<span data-ttu-id="cd137-122">[**Иасинкоператионвиспрогресскомплетедхандлер<TResult, TProgress>**](/previous-versions//br205808(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="cd137-122">[**IAsyncOperationWithProgressCompletedHandler<TResult,TProgress>**](/previous-versions//br205808(v=vs.85))</span></span>
</dt> </dl>

 

 
