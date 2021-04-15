---
description: Изменяет флаг «грязных» для текущего потока.
ms.assetid: 65fa7fbe-4fa7-45a3-91a4-4a3547b035b9
title: Кперсистстреам. Сетдирти, метод (Пстреам. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPersistStream.SetDirty
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 382b74f6314beb586b1e51c02a257cad8904c188
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105675686"
---
# <a name="cpersiststreamsetdirty-method"></a><span data-ttu-id="8522c-103">Кперсистстреам. Сетдирти, метод</span><span class="sxs-lookup"><span data-stu-id="8522c-103">CPersistStream.SetDirty method</span></span>

<span data-ttu-id="8522c-104">Изменяет флаг «грязных» для текущего потока.</span><span class="sxs-lookup"><span data-stu-id="8522c-104">Changes the dirty flag for the current stream.</span></span>

## <a name="syntax"></a><span data-ttu-id="8522c-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="8522c-105">Syntax</span></span>


```C++
HRESULT SetDirty(
   BOOL fDirty
);
```



## <a name="parameters"></a><span data-ttu-id="8522c-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="8522c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8522c-107">*фдирти*</span><span class="sxs-lookup"><span data-stu-id="8522c-107">*fDirty*</span></span> 
</dt> <dd>

<span data-ttu-id="8522c-108">Новый "грязный" флаг для этого потока.</span><span class="sxs-lookup"><span data-stu-id="8522c-108">New dirty flag for this stream.</span></span> <span data-ttu-id="8522c-109">**Значение true** означает, что данные не были сохранены.</span><span class="sxs-lookup"><span data-stu-id="8522c-109">**TRUE** means that the data has not been saved.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8522c-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="8522c-110">Return value</span></span>

<span data-ttu-id="8522c-111">Возвращает значение **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="8522c-111">Returns an **HRESULT** value.</span></span>

## <a name="requirements"></a><span data-ttu-id="8522c-112">Требования</span><span class="sxs-lookup"><span data-stu-id="8522c-112">Requirements</span></span>



| <span data-ttu-id="8522c-113">Требование</span><span class="sxs-lookup"><span data-stu-id="8522c-113">Requirement</span></span> | <span data-ttu-id="8522c-114">Значение</span><span class="sxs-lookup"><span data-stu-id="8522c-114">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8522c-115">Header</span><span class="sxs-lookup"><span data-stu-id="8522c-115">Header</span></span><br/>  | <dl> <span data-ttu-id="8522c-116"><dt>Пстреам. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="8522c-116"><dt>Pstream.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="8522c-117">Библиотека</span><span class="sxs-lookup"><span data-stu-id="8522c-117">Library</span></span><br/> | <dl> <span data-ttu-id="8522c-118"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="8522c-118"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8522c-119">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="8522c-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8522c-120">**Класс Кперсистстреам**</span><span class="sxs-lookup"><span data-stu-id="8522c-120">**CPersistStream Class**</span></span>](cpersiststream.md)
</dt> </dl>

 

 




