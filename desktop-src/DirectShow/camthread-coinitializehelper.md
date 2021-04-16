---
description: Метод Коинитиализехелпер вызывает функцию CoInitializeEx в начале потока.
ms.assetid: 1a981e1e-c059-4e51-81d8-33bcb39ee580
title: Камсреад. Коинитиализехелпер, метод (Вксутил. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAMThread.CoInitializeHelper
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a6c3eb7fbcb9e4abada43098339a29d208ded0d4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105657159"
---
# <a name="camthreadcoinitializehelper-method"></a><span data-ttu-id="a61a4-103">Камсреад. Коинитиализехелпер, метод</span><span class="sxs-lookup"><span data-stu-id="a61a4-103">CAMThread.CoInitializeHelper method</span></span>

<span data-ttu-id="a61a4-104">`CoInitializeHelper`Метод вызывает функцию CoInitializeEx в начале потока.</span><span class="sxs-lookup"><span data-stu-id="a61a4-104">The `CoInitializeHelper` method calls the CoInitializeEx function at the start of the thread.</span></span>

## <a name="syntax"></a><span data-ttu-id="a61a4-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="a61a4-105">Syntax</span></span>


```C++
static HRESULT CoInitializeHelper();
```



## <a name="parameters"></a><span data-ttu-id="a61a4-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="a61a4-106">Parameters</span></span>

<span data-ttu-id="a61a4-107">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="a61a4-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="a61a4-108">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="a61a4-108">Return value</span></span>

<span data-ttu-id="a61a4-109">Возвращает значение **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="a61a4-109">Returns an **HRESULT** value.</span></span> <span data-ttu-id="a61a4-110">Ниже приведены возможные значения.</span><span class="sxs-lookup"><span data-stu-id="a61a4-110">The following are possible values.</span></span>



| <span data-ttu-id="a61a4-111">Код возврата</span><span class="sxs-lookup"><span data-stu-id="a61a4-111">Return code</span></span>                                                                             | <span data-ttu-id="a61a4-112">Описание</span><span class="sxs-lookup"><span data-stu-id="a61a4-112">Description</span></span>                                              |
|-----------------------------------------------------------------------------------------|----------------------------------------------------------|
| <dl> <span data-ttu-id="a61a4-113"><dt>**S \_ false**</dt></span><span class="sxs-lookup"><span data-stu-id="a61a4-113"><dt>**S\_FALSE**</dt></span></span> </dl> | <span data-ttu-id="a61a4-114">Функция CoInitializeEx недоступна.</span><span class="sxs-lookup"><span data-stu-id="a61a4-114">The CoInitializeEx function is not available.</span></span><br/> |
| <dl> <span data-ttu-id="a61a4-115"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="a61a4-115"><dt>**S\_OK**</dt></span></span> </dl>    | <span data-ttu-id="a61a4-116">Успешно.</span><span class="sxs-lookup"><span data-stu-id="a61a4-116">Success.</span></span><br/>                                      |
| <dl> <span data-ttu-id="a61a4-117"><dt>**\_Ошибка E**</dt></span><span class="sxs-lookup"><span data-stu-id="a61a4-117"><dt>**E\_FAIL**</dt></span></span> </dl>  | <span data-ttu-id="a61a4-118">Ошибка.</span><span class="sxs-lookup"><span data-stu-id="a61a4-118">Failure.</span></span><br/>                                      |



 

## <a name="remarks"></a><span data-ttu-id="a61a4-119">Комментарии</span><span class="sxs-lookup"><span data-stu-id="a61a4-119">Remarks</span></span>

<span data-ttu-id="a61a4-120">Метод [**камсреад:: инитиалсреадпрок**](camthread-initialthreadproc.md) вызывает этот вспомогательный метод, который вызывает функцию CoInitializeEx.</span><span class="sxs-lookup"><span data-stu-id="a61a4-120">The [**CAMThread::InitialThreadProc**](camthread-initialthreadproc.md) method calls this helper method, which calls the CoInitializeEx function.</span></span> <span data-ttu-id="a61a4-121">\_ \_ Для отключения платформа динамических данных Exchange (DDE) используется флаг деinit Disable OLE1DDE.</span><span class="sxs-lookup"><span data-stu-id="a61a4-121">It uses the COINIT\_DISABLE\_OLE1DDE flag, to disable Dynamic Data Exchange (DDE).</span></span> <span data-ttu-id="a61a4-122">Дополнительные сведения см. в разделе пакет SDK для платформы.</span><span class="sxs-lookup"><span data-stu-id="a61a4-122">For more information, see the Platform SDK.</span></span>

## <a name="requirements"></a><span data-ttu-id="a61a4-123">Требования</span><span class="sxs-lookup"><span data-stu-id="a61a4-123">Requirements</span></span>



| <span data-ttu-id="a61a4-124">Требование</span><span class="sxs-lookup"><span data-stu-id="a61a4-124">Requirement</span></span> | <span data-ttu-id="a61a4-125">Значение</span><span class="sxs-lookup"><span data-stu-id="a61a4-125">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a61a4-126">Header</span><span class="sxs-lookup"><span data-stu-id="a61a4-126">Header</span></span><br/>  | <dl> <span data-ttu-id="a61a4-127"><dt>Вксутил. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="a61a4-127"><dt>Wxutil.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="a61a4-128">Библиотека</span><span class="sxs-lookup"><span data-stu-id="a61a4-128">Library</span></span><br/> | <dl> <span data-ttu-id="a61a4-129"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="a61a4-129"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a61a4-130">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="a61a4-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a61a4-131">**Класс Камсреад**</span><span class="sxs-lookup"><span data-stu-id="a61a4-131">**CAMThread Class**</span></span>](camthread.md)
</dt> </dl>

 

 




