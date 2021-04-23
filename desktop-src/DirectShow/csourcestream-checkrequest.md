---
description: Метод Чеккрекуест проверяет наличие запроса потока без блокировки.
ms.assetid: b4691dde-abec-4671-bea6-0f22cc4e7c61
title: Метод Ксаурцестреам. Чеккрекуест (Source. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceStream.CheckRequest
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 3100d449d2f29b2080541c5968cad6abc5643b26
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105688930"
---
# <a name="csourcestreamcheckrequest-method"></a><span data-ttu-id="e6fa6-103">Ксаурцестреам. Чеккрекуест, метод</span><span class="sxs-lookup"><span data-stu-id="e6fa6-103">CSourceStream.CheckRequest method</span></span>

<span data-ttu-id="e6fa6-104">`CheckRequest`Метод проверяет наличие запроса потока без блокировки.</span><span class="sxs-lookup"><span data-stu-id="e6fa6-104">The `CheckRequest` method checks if there is a thread request, without blocking.</span></span>

## <a name="syntax"></a><span data-ttu-id="e6fa6-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="e6fa6-105">Syntax</span></span>


```C++
BOOL CheckRequest(
   Command *pCom
);
```



## <a name="parameters"></a><span data-ttu-id="e6fa6-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="e6fa6-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e6fa6-107">*пком*</span><span class="sxs-lookup"><span data-stu-id="e6fa6-107">*pCom*</span></span> 
</dt> <dd>

<span data-ttu-id="e6fa6-108">Указатель на переменную, которая получает значение, переданное в последнем вызове метода [**камсреад:: каллворкер**](camthread-callworker.md) .</span><span class="sxs-lookup"><span data-stu-id="e6fa6-108">Pointer to a variable that receives the value passed in the last call to the [**CAMThread::CallWorker**](camthread-callworker.md) method.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e6fa6-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="e6fa6-109">Return value</span></span>

<span data-ttu-id="e6fa6-110">Возвращает **значение true** , если имеется ожидающий запрос, или **false** в противном случае.</span><span class="sxs-lookup"><span data-stu-id="e6fa6-110">Returns **TRUE** if there is a pending request, or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="e6fa6-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="e6fa6-111">Remarks</span></span>

<span data-ttu-id="e6fa6-112">Этот метод переопределяет метод [**камсреад:: чеккрекуест**](camthread-checkrequest.md) для выполнения проверки типа.</span><span class="sxs-lookup"><span data-stu-id="e6fa6-112">This method overrides the [**CAMThread::CheckRequest**](camthread-checkrequest.md) method to perform type-checking.</span></span> <span data-ttu-id="e6fa6-113">Класс **ксаурцестреам** определяет следующий перечислимый тип для параметра *пком* :</span><span class="sxs-lookup"><span data-stu-id="e6fa6-113">The **CSourceStream** class defines the following enumerated type for the *pCom* parameter:</span></span>


```C++
enum Command {CMD_INIT, CMD_PAUSE, CMD_RUN, CMD_STOP, CMD_EXIT};
```



## <a name="requirements"></a><span data-ttu-id="e6fa6-114">Требования</span><span class="sxs-lookup"><span data-stu-id="e6fa6-114">Requirements</span></span>



| <span data-ttu-id="e6fa6-115">Требование</span><span class="sxs-lookup"><span data-stu-id="e6fa6-115">Requirement</span></span> | <span data-ttu-id="e6fa6-116">Значение</span><span class="sxs-lookup"><span data-stu-id="e6fa6-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e6fa6-117">Header</span><span class="sxs-lookup"><span data-stu-id="e6fa6-117">Header</span></span><br/>  | <dl> <span data-ttu-id="e6fa6-118"><dt>Source. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="e6fa6-118"><dt>Source.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="e6fa6-119">Библиотека</span><span class="sxs-lookup"><span data-stu-id="e6fa6-119">Library</span></span><br/> | <dl> <span data-ttu-id="e6fa6-120"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="e6fa6-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e6fa6-121">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="e6fa6-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e6fa6-122">**Класс Ксаурцестреам**</span><span class="sxs-lookup"><span data-stu-id="e6fa6-122">**CSourceStream Class**</span></span>](csourcestream.md)
</dt> </dl>

 

 




