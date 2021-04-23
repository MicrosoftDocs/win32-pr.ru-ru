---
description: Методического HResult извлекает значение HRESULT из вызванной команды.
ms.assetid: 7e88a2bd-6b1b-4e59-b185-5dfd501fc37a
title: Кдеферредкомманд. метод HResult (Ктлутил. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDeferredCommand.GetHResult
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 5b09049bc443991dabe07a7626ffc42097feceee
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105669439"
---
# <a name="cdeferredcommandgethresult-method"></a><span data-ttu-id="a92ec-103">Кдеферредкомманд. метод HResult</span><span class="sxs-lookup"><span data-stu-id="a92ec-103">CDeferredCommand.GetHResult method</span></span>

<span data-ttu-id="a92ec-104">`GetHResult`Метод получает значение **HRESULT** из вызванной команды.</span><span class="sxs-lookup"><span data-stu-id="a92ec-104">The `GetHResult` method retrieves the **HRESULT** value from the invoked command.</span></span>

## <a name="syntax"></a><span data-ttu-id="a92ec-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="a92ec-105">Syntax</span></span>


```C++
HRESULT GetHResult(
   HRESULT *phrResult
);
```



## <a name="parameters"></a><span data-ttu-id="a92ec-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="a92ec-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a92ec-107">*фрресулт*</span><span class="sxs-lookup"><span data-stu-id="a92ec-107">*phrResult*</span></span> 
</dt> <dd>

<span data-ttu-id="a92ec-108">Указатель на значение **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="a92ec-108">Pointer to the **HRESULT** value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a92ec-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="a92ec-109">Return value</span></span>

<span data-ttu-id="a92ec-110">Возвращает "E \_ Abort", если **m \_ Пкуеуе** имеет **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="a92ec-110">Returns E\_ABORT if **m\_pQueue** is **NULL**.</span></span> <span data-ttu-id="a92ec-111">В противном случае возвращается значение S \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="a92ec-111">Otherwise, returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="a92ec-112">Комментарии</span><span class="sxs-lookup"><span data-stu-id="a92ec-112">Remarks</span></span>

<span data-ttu-id="a92ec-113">Эта функция члена реализует метод [**идеферредкомманд:: и HRESULT**](/windows/desktop/api/Control/nf-control-ideferredcommand-gethresult) .</span><span class="sxs-lookup"><span data-stu-id="a92ec-113">This member function implements the [**IDeferredCommand::GetHResult**](/windows/desktop/api/Control/nf-control-ideferredcommand-gethresult) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="a92ec-114">Требования</span><span class="sxs-lookup"><span data-stu-id="a92ec-114">Requirements</span></span>



| <span data-ttu-id="a92ec-115">Требование</span><span class="sxs-lookup"><span data-stu-id="a92ec-115">Requirement</span></span> | <span data-ttu-id="a92ec-116">Значение</span><span class="sxs-lookup"><span data-stu-id="a92ec-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a92ec-117">Header</span><span class="sxs-lookup"><span data-stu-id="a92ec-117">Header</span></span><br/>  | <dl> <span data-ttu-id="a92ec-118"><dt>Ктлутил. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="a92ec-118"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="a92ec-119">Библиотека</span><span class="sxs-lookup"><span data-stu-id="a92ec-119">Library</span></span><br/> | <dl> <span data-ttu-id="a92ec-120"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="a92ec-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a92ec-121">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="a92ec-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a92ec-122">**Класс Кдеферредкомманд**</span><span class="sxs-lookup"><span data-stu-id="a92ec-122">**CDeferredCommand Class**</span></span>](cdeferredcommand.md)
</dt> </dl>

 

 




