---
description: Метод INSERT добавляет объект Кдеферредкомманд в очередь.
ms.assetid: 41f9c30c-6267-435a-9089-eb34ae606896
title: Метод Ккмдкуеуе. Insert (Винутил. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CCmdQueue.Insert
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 6bad004641258e29ed42d7142a5b0ab2c0ceb78d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105656891"
---
# <a name="ccmdqueueinsert-method"></a><span data-ttu-id="67425-103">Ккмдкуеуе. INSERT, метод</span><span class="sxs-lookup"><span data-stu-id="67425-103">CCmdQueue.Insert method</span></span>

<span data-ttu-id="67425-104">`Insert`Метод добавляет объект [**кдеферредкомманд**](cdeferredcommand.md) в очередь.</span><span class="sxs-lookup"><span data-stu-id="67425-104">The `Insert` method adds a [**CDeferredCommand**](cdeferredcommand.md) object to the queue.</span></span>

## <a name="syntax"></a><span data-ttu-id="67425-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="67425-105">Syntax</span></span>


```C++
virtual HRESULT Insert(
   CDeferredCommand *pCmd
);
```



## <a name="parameters"></a><span data-ttu-id="67425-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="67425-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="67425-107">*pCmd*</span><span class="sxs-lookup"><span data-stu-id="67425-107">*pCmd*</span></span> 
</dt> <dd>

<span data-ttu-id="67425-108">Указатель на объект **кдеферредкомманд** для добавления в очередь.</span><span class="sxs-lookup"><span data-stu-id="67425-108">Pointer to the **CDeferredCommand** object to add to the queue.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="67425-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="67425-109">Return value</span></span>

<span data-ttu-id="67425-110">Возвращает \_ ОК в реализации по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="67425-110">Returns S\_OK in the default implementation.</span></span>

## <a name="requirements"></a><span data-ttu-id="67425-111">Требования</span><span class="sxs-lookup"><span data-stu-id="67425-111">Requirements</span></span>



| <span data-ttu-id="67425-112">Требование</span><span class="sxs-lookup"><span data-stu-id="67425-112">Requirement</span></span> | <span data-ttu-id="67425-113">Значение</span><span class="sxs-lookup"><span data-stu-id="67425-113">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="67425-114">Header</span><span class="sxs-lookup"><span data-stu-id="67425-114">Header</span></span><br/>  | <dl> <span data-ttu-id="67425-115"><dt>Винутил. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="67425-115"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="67425-116">Библиотека</span><span class="sxs-lookup"><span data-stu-id="67425-116">Library</span></span><br/> | <dl> <span data-ttu-id="67425-117"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="67425-117"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="67425-118">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="67425-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="67425-119">**Класс Ккмдкуеуе**</span><span class="sxs-lookup"><span data-stu-id="67425-119">**CCmdQueue Class**</span></span>](ccmdqueue.md)
</dt> </dl>

 

 




