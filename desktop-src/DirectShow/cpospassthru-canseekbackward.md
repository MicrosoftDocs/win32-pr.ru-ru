---
description: 'Метод Кансикбакквард определяет, возможен ли обратный поиск в потоке. Этот метод реализует метод Имедиапоситион:: Кансикбакквард.'
ms.assetid: 6443980f-6863-4941-b2dd-4a31257b5810
title: Кпоспасссру. Кансикбакквард, метод (Ктлутил. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPosPassThru.CanSeekBackward
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a6a016f5cfeea7ca1e63bb4d0e603784b8f95a85
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105675076"
---
# <a name="cpospassthrucanseekbackward-method"></a><span data-ttu-id="47026-104">Кпоспасссру. Кансикбакквард, метод</span><span class="sxs-lookup"><span data-stu-id="47026-104">CPosPassThru.CanSeekBackward method</span></span>

<span data-ttu-id="47026-105">`CanSeekBackward`Метод определяет, можно ли выполнить поиск в потоке обратно.</span><span class="sxs-lookup"><span data-stu-id="47026-105">The `CanSeekBackward` method determines whether the stream can be seeked backward.</span></span> <span data-ttu-id="47026-106">Этот метод реализует метод [**имедиапоситион:: кансикбакквард**](/windows/desktop/api/Control/nf-control-imediaposition-canseekbackward) .</span><span class="sxs-lookup"><span data-stu-id="47026-106">This method implements the [**IMediaPosition::CanSeekBackward**](/windows/desktop/api/Control/nf-control-imediaposition-canseekbackward) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="47026-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="47026-107">Syntax</span></span>


```C++
HRESULT CanSeekBackward(
   LONG *pCanSeekBackward
);
```



## <a name="parameters"></a><span data-ttu-id="47026-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="47026-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="47026-109">*пкансикбакквард*</span><span class="sxs-lookup"><span data-stu-id="47026-109">*pCanSeekBackward*</span></span> 
</dt> <dd>

<span data-ttu-id="47026-110">Указатель на переменную, которая получает значение ОАТРУЕ, если фильтр может искать назад, или ОАФАЛСЕ в противном случае.</span><span class="sxs-lookup"><span data-stu-id="47026-110">Pointer to a variable that receives the value OATRUE if the filter can seek backward, or OAFALSE otherwise.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="47026-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="47026-111">Return value</span></span>

<span data-ttu-id="47026-112">Возвращает значение **HRESULT** из подключенного ПИН-кода.</span><span class="sxs-lookup"><span data-stu-id="47026-112">Returns the **HRESULT** value from the connected pin.</span></span>

## <a name="requirements"></a><span data-ttu-id="47026-113">Требования</span><span class="sxs-lookup"><span data-stu-id="47026-113">Requirements</span></span>



| <span data-ttu-id="47026-114">Требование</span><span class="sxs-lookup"><span data-stu-id="47026-114">Requirement</span></span> | <span data-ttu-id="47026-115">Значение</span><span class="sxs-lookup"><span data-stu-id="47026-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="47026-116">Header</span><span class="sxs-lookup"><span data-stu-id="47026-116">Header</span></span><br/>  | <dl> <span data-ttu-id="47026-117"><dt>Ктлутил. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="47026-117"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="47026-118">Библиотека</span><span class="sxs-lookup"><span data-stu-id="47026-118">Library</span></span><br/> | <dl> <span data-ttu-id="47026-119"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="47026-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="47026-120">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="47026-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="47026-121">**Класс Кпоспасссру**</span><span class="sxs-lookup"><span data-stu-id="47026-121">**CPosPassThru Class**</span></span>](cpospassthru.md)
</dt> </dl>

 

 




