---
description: 'Метод Кансикфорвард определяет, можно ли выполнить поиск в потоке вперед. Этот метод реализует метод Имедиапоситион:: Кансикфорвард.'
ms.assetid: ccb2db8d-b52e-4e3d-b49b-9689197a974a
title: Кпоспасссру. Кансикфорвард, метод (Ктлутил. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPosPassThru.CanSeekForward
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 701bfdff1d3a3a37dc0e3935aa82bfca2e01cfcb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105675788"
---
# <a name="cpospassthrucanseekforward-method"></a><span data-ttu-id="11fc0-104">Кпоспасссру. Кансикфорвард, метод</span><span class="sxs-lookup"><span data-stu-id="11fc0-104">CPosPassThru.CanSeekForward method</span></span>

<span data-ttu-id="11fc0-105">`CanSeekForward`Метод определяет, можно ли выполнить поиск в потоке вперед.</span><span class="sxs-lookup"><span data-stu-id="11fc0-105">The `CanSeekForward` method determines whether the stream can be seeked forward.</span></span> <span data-ttu-id="11fc0-106">Этот метод реализует метод [**имедиапоситион:: кансикфорвард**](/windows/desktop/api/Control/nf-control-imediaposition-canseekforward) .</span><span class="sxs-lookup"><span data-stu-id="11fc0-106">This method implements the [**IMediaPosition::CanSeekForward**](/windows/desktop/api/Control/nf-control-imediaposition-canseekforward) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="11fc0-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="11fc0-107">Syntax</span></span>


```C++
HRESULT CanSeekForward(
   LONG *pCanSeekForward
);
```



## <a name="parameters"></a><span data-ttu-id="11fc0-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="11fc0-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="11fc0-109">*пкансикфорвард*</span><span class="sxs-lookup"><span data-stu-id="11fc0-109">*pCanSeekForward*</span></span> 
</dt> <dd>

<span data-ttu-id="11fc0-110">Указатель на переменную, которая получает значение ОАТРУЕ, если фильтр может искать вперед или ОАФАЛСЕ в противном случае.</span><span class="sxs-lookup"><span data-stu-id="11fc0-110">Pointer to a variable that receives the value OATRUE if the filter can seek forward, or OAFALSE otherwise.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="11fc0-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="11fc0-111">Return value</span></span>

<span data-ttu-id="11fc0-112">Возвращает значение **HRESULT** из подключенного ПИН-кода.</span><span class="sxs-lookup"><span data-stu-id="11fc0-112">Returns the **HRESULT** value from the connected pin.</span></span>

## <a name="requirements"></a><span data-ttu-id="11fc0-113">Требования</span><span class="sxs-lookup"><span data-stu-id="11fc0-113">Requirements</span></span>



| <span data-ttu-id="11fc0-114">Требование</span><span class="sxs-lookup"><span data-stu-id="11fc0-114">Requirement</span></span> | <span data-ttu-id="11fc0-115">Значение</span><span class="sxs-lookup"><span data-stu-id="11fc0-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="11fc0-116">Header</span><span class="sxs-lookup"><span data-stu-id="11fc0-116">Header</span></span><br/>  | <dl> <span data-ttu-id="11fc0-117"><dt>Ктлутил. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="11fc0-117"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="11fc0-118">Библиотека</span><span class="sxs-lookup"><span data-stu-id="11fc0-118">Library</span></span><br/> | <dl> <span data-ttu-id="11fc0-119"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="11fc0-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="11fc0-120">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="11fc0-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="11fc0-121">**Класс Кпоспасссру**</span><span class="sxs-lookup"><span data-stu-id="11fc0-121">**CPosPassThru Class**</span></span>](cpospassthru.md)
</dt> </dl>

 

 




