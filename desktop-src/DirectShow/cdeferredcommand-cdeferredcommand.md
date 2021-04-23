---
description: Метод конструктора.
ms.assetid: 0b372fa2-78a9-4e38-813c-f18123716c6d
title: Конструктор Кдеферредкомманд. Кдеферредкомманд (Ктлутил. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDeferredCommand.CDeferredCommand
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 4e92a2ffc5129ee38fc5061b28ea7ffef49da0f1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105680013"
---
# <a name="cdeferredcommandcdeferredcommand-constructor"></a><span data-ttu-id="cec38-103">Кдеферредкомманд. Кдеферредкомманд, конструктор</span><span class="sxs-lookup"><span data-stu-id="cec38-103">CDeferredCommand.CDeferredCommand constructor</span></span>

<span data-ttu-id="cec38-104">Метод конструктора.</span><span class="sxs-lookup"><span data-stu-id="cec38-104">Constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="cec38-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="cec38-105">Syntax</span></span>


```C++
CDeferredCommand(
   CCmdQueue *pQ,
   LPUNKNOWN pUnk,
   HRESULT   *phr,
   LPUNKNOWN pUnkExecutor,
   REFTIME   time,
   GUID      *iid,
   long      dispidMethod,
   short     wFlags,
   long      cArgs,
   VARIANT   *pDispParams,
   VARIANT   *pvarResult,
   short     *puArgErr,
   BOOL      bStream
);
```



## <a name="parameters"></a><span data-ttu-id="cec38-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="cec38-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cec38-107">*pQ*</span><span class="sxs-lookup"><span data-stu-id="cec38-107">*pQ*</span></span> 
</dt> <dd>

<span data-ttu-id="cec38-108">Указатель на объект, который предоставляет интерфейс [**икуеуекомманд**](/windows/desktop/api/Control/nn-control-iqueuecommand) .</span><span class="sxs-lookup"><span data-stu-id="cec38-108">Pointer to an object that exposes the [**IQueueCommand**](/windows/desktop/api/Control/nn-control-iqueuecommand) interface.</span></span>

</dd> <dt>

<span data-ttu-id="cec38-109">*pUnk*</span><span class="sxs-lookup"><span data-stu-id="cec38-109">*pUnk*</span></span> 
</dt> <dd>

<span data-ttu-id="cec38-110">Указатель на внешний интерфейс **IUnknown** для агрегирования.</span><span class="sxs-lookup"><span data-stu-id="cec38-110">Pointer to the outer **IUnknown** interface for aggregation.</span></span>

</dd> <dt>

<span data-ttu-id="cec38-111">*фр*</span><span class="sxs-lookup"><span data-stu-id="cec38-111">*phr*</span></span> 
</dt> <dd>

<span data-ttu-id="cec38-112">Указатель на возвращаемое значение **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="cec38-112">Pointer to a returned **HRESULT** value.</span></span>

</dd> <dt>

<span data-ttu-id="cec38-113">*пункексекутор*</span><span class="sxs-lookup"><span data-stu-id="cec38-113">*pUnkExecutor*</span></span> 
</dt> <dd>

<span data-ttu-id="cec38-114">Указатель на объект, который будет выполнять эту команду.</span><span class="sxs-lookup"><span data-stu-id="cec38-114">Pointer to the object that will carry out this command.</span></span>

</dd> <dt>

<span data-ttu-id="cec38-115">*time*</span><span class="sxs-lookup"><span data-stu-id="cec38-115">*time*</span></span> 
</dt> <dd>

<span data-ttu-id="cec38-116">Время, когда будет выполняться команда.</span><span class="sxs-lookup"><span data-stu-id="cec38-116">Time at which the command will be run.</span></span>

</dd> <dt>

<span data-ttu-id="cec38-117">*IID*</span><span class="sxs-lookup"><span data-stu-id="cec38-117">*iid*</span></span> 
</dt> <dd>

<span data-ttu-id="cec38-118">Указатель на глобальный уникальный идентификатор (**GUID**) интерфейса, содержащего метод.</span><span class="sxs-lookup"><span data-stu-id="cec38-118">Pointer to the globally unique identifier (**GUID**) of the interface that contains the method.</span></span>

</dd> <dt>

<span data-ttu-id="cec38-119">*диспидмесод*</span><span class="sxs-lookup"><span data-stu-id="cec38-119">*dispidMethod*</span></span> 
</dt> <dd>

<span data-ttu-id="cec38-120">Вызываемый метод интерфейса.</span><span class="sxs-lookup"><span data-stu-id="cec38-120">Method on the interface to call.</span></span>

</dd> <dt>

<span data-ttu-id="cec38-121">*вфлагс*</span><span class="sxs-lookup"><span data-stu-id="cec38-121">*wFlags*</span></span> 
</dt> <dd>

<span data-ttu-id="cec38-122">Контекст вызова.</span><span class="sxs-lookup"><span data-stu-id="cec38-122">Context of the invocation.</span></span>

</dd> <dt>

<span data-ttu-id="cec38-123">*каргс*</span><span class="sxs-lookup"><span data-stu-id="cec38-123">*cArgs*</span></span> 
</dt> <dd>

<span data-ttu-id="cec38-124">Число переданных аргументов.</span><span class="sxs-lookup"><span data-stu-id="cec38-124">Number of arguments passed.</span></span>

</dd> <dt>

<span data-ttu-id="cec38-125">*пдисппарамс*</span><span class="sxs-lookup"><span data-stu-id="cec38-125">*pDispParams*</span></span> 
</dt> <dd>

<span data-ttu-id="cec38-126">Указатель на список типов Variant аргументов.</span><span class="sxs-lookup"><span data-stu-id="cec38-126">Pointer to a list of argument variant types.</span></span>

</dd> <dt>

<span data-ttu-id="cec38-127">*пварресулт*</span><span class="sxs-lookup"><span data-stu-id="cec38-127">*pvarResult*</span></span> 
</dt> <dd>

<span data-ttu-id="cec38-128">Указатель на возвращаемый список типов Variant, если таковой имеется.</span><span class="sxs-lookup"><span data-stu-id="cec38-128">Pointer to a returned variant type list, if any.</span></span>

</dd> <dt>

<span data-ttu-id="cec38-129">*puArgErr*</span><span class="sxs-lookup"><span data-stu-id="cec38-129">*puArgErr*</span></span> 
</dt> <dd>

<span data-ttu-id="cec38-130">Указатель на последний аргумент в списке параметров *пдисппарамс* с ошибкой.</span><span class="sxs-lookup"><span data-stu-id="cec38-130">Pointer to the last argument in the *pDispParams* parameter list with an error.</span></span>

</dd> <dt>

<span data-ttu-id="cec38-131">*бстреам*</span><span class="sxs-lookup"><span data-stu-id="cec38-131">*bStream*</span></span> 
</dt> <dd>

<span data-ttu-id="cec38-132">Значение, указывающее, находится ли время отложенной команды во время потока (**true**) или во время презентации (**false**).</span><span class="sxs-lookup"><span data-stu-id="cec38-132">Value indicating whether the deferred command time is in stream time (**TRUE**) or presentation time (**FALSE**).</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="cec38-133">Требования</span><span class="sxs-lookup"><span data-stu-id="cec38-133">Requirements</span></span>



| <span data-ttu-id="cec38-134">Требование</span><span class="sxs-lookup"><span data-stu-id="cec38-134">Requirement</span></span> | <span data-ttu-id="cec38-135">Значение</span><span class="sxs-lookup"><span data-stu-id="cec38-135">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cec38-136">Header</span><span class="sxs-lookup"><span data-stu-id="cec38-136">Header</span></span><br/>  | <dl> <span data-ttu-id="cec38-137"><dt>Ктлутил. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="cec38-137"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="cec38-138">Библиотека</span><span class="sxs-lookup"><span data-stu-id="cec38-138">Library</span></span><br/> | <dl> <span data-ttu-id="cec38-139"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="cec38-139"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cec38-140">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="cec38-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cec38-141">**Класс Кдеферредкомманд**</span><span class="sxs-lookup"><span data-stu-id="cec38-141">**CDeferredCommand Class**</span></span>](cdeferredcommand.md)
</dt> </dl>

 

 




