---
description: Новый метод инициализирует команду для выполнения и возвращает новый объект Кдеферредкомманд.
ms.assetid: bdd80747-a15b-422a-b742-ebfa4076bdf7
title: Метод Ккмдкуеуе. New (Винутил. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CCmdQueue.New
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 58c3aee63005010b9ed7366cfb63a69fcc7348b9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105674864"
---
# <a name="ccmdqueuenew-method"></a><span data-ttu-id="8ae07-103">Ккмдкуеуе. New, метод</span><span class="sxs-lookup"><span data-stu-id="8ae07-103">CCmdQueue.New method</span></span>

<span data-ttu-id="8ae07-104">`New`Метод инициализирует команду для выполнения и возвращает новый объект [**кдеферредкомманд**](cdeferredcommand.md) .</span><span class="sxs-lookup"><span data-stu-id="8ae07-104">The `New` method initializes a command to be run and returns a new [**CDeferredCommand**](cdeferredcommand.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="8ae07-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="8ae07-105">Syntax</span></span>


```C++
virtual HRESULT New(
   CDeferredCommand **ppCmd,
   LPUNKNOWN        pUnk,
   REFTIME          time,
   GUID             *iid,
   long             dispidMethod,
   short            wFlags,
   long             cArgs,
   VARIANT          *pDispParams,
   VARIANT          *pvarResult,
   short            *puArgErr,
   BOOL             bStream
);
```



## <a name="parameters"></a><span data-ttu-id="8ae07-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="8ae07-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8ae07-107">*ppCmd*</span><span class="sxs-lookup"><span data-stu-id="8ae07-107">*ppCmd*</span></span> 
</dt> <dd>

<span data-ttu-id="8ae07-108">Адрес указателя на объект [**кдеферредкомманд**](cdeferredcommand.md) , по которому приложение может отменить команду, установить новое время презентации или получить сведения об оценке.</span><span class="sxs-lookup"><span data-stu-id="8ae07-108">Address of a pointer to a [**CDeferredCommand**](cdeferredcommand.md) object by which an application can cancel the command, set a new presentation time for it, or retrieve estimate information.</span></span>

</dd> <dt>

<span data-ttu-id="8ae07-109">*pUnk*</span><span class="sxs-lookup"><span data-stu-id="8ae07-109">*pUnk*</span></span> 
</dt> <dd>

<span data-ttu-id="8ae07-110">Указатель на объект, который будет выполнять команду.</span><span class="sxs-lookup"><span data-stu-id="8ae07-110">Pointer to the object that will run the command.</span></span>

</dd> <dt>

<span data-ttu-id="8ae07-111">*time*</span><span class="sxs-lookup"><span data-stu-id="8ae07-111">*time*</span></span> 
</dt> <dd>

<span data-ttu-id="8ae07-112">Время выполнения команды в очереди или команд.</span><span class="sxs-lookup"><span data-stu-id="8ae07-112">Time at which to run the queued command or commands.</span></span>

</dd> <dt>

<span data-ttu-id="8ae07-113">*IID*</span><span class="sxs-lookup"><span data-stu-id="8ae07-113">*iid*</span></span> 
</dt> <dd>

<span data-ttu-id="8ae07-114">Указатель на глобальный уникальный идентификатор (**GUID**) вызываемого интерфейса.</span><span class="sxs-lookup"><span data-stu-id="8ae07-114">Pointer to the globally unique identifier (**GUID**) of the interface to call.</span></span>

</dd> <dt>

<span data-ttu-id="8ae07-115">*диспидмесод*</span><span class="sxs-lookup"><span data-stu-id="8ae07-115">*dispidMethod*</span></span> 
</dt> <dd>

<span data-ttu-id="8ae07-116">Вызываемый метод интерфейса.</span><span class="sxs-lookup"><span data-stu-id="8ae07-116">Method on the interface to be called.</span></span>

</dd> <dt>

<span data-ttu-id="8ae07-117">*вфлагс*</span><span class="sxs-lookup"><span data-stu-id="8ae07-117">*wFlags*</span></span> 
</dt> <dd>

<span data-ttu-id="8ae07-118">Флаги, описывающие контекст вызова.</span><span class="sxs-lookup"><span data-stu-id="8ae07-118">Flags describing the context of the call.</span></span> <span data-ttu-id="8ae07-119">Этот параметр поддерживает те же флаги, что и метод **IDispatch:: Invoke** .</span><span class="sxs-lookup"><span data-stu-id="8ae07-119">This parameter supports the same flags as the **IDispatch::Invoke** method.</span></span>

</dd> <dt>

<span data-ttu-id="8ae07-120">*каргс*</span><span class="sxs-lookup"><span data-stu-id="8ae07-120">*cArgs*</span></span> 
</dt> <dd>

<span data-ttu-id="8ae07-121">Число переданных аргументов.</span><span class="sxs-lookup"><span data-stu-id="8ae07-121">Number of arguments passed.</span></span>

</dd> <dt>

<span data-ttu-id="8ae07-122">*пдисппарамс*</span><span class="sxs-lookup"><span data-stu-id="8ae07-122">*pDispParams*</span></span> 
</dt> <dd>

<span data-ttu-id="8ae07-123">Указатель на список типов Variant, связанных с параметрами диспетчеризации.</span><span class="sxs-lookup"><span data-stu-id="8ae07-123">Pointer to the list of variant types associated with the dispatch parameters.</span></span>

</dd> <dt>

<span data-ttu-id="8ae07-124">*пварресулт*</span><span class="sxs-lookup"><span data-stu-id="8ae07-124">*pvarResult*</span></span> 
</dt> <dd>

<span data-ttu-id="8ae07-125">Указатель на список, в котором будут возвращаться результаты (если они есть).</span><span class="sxs-lookup"><span data-stu-id="8ae07-125">Pointer to the list where results, if any, are to be returned.</span></span>

</dd> <dt>

<span data-ttu-id="8ae07-126">*puArgErr*</span><span class="sxs-lookup"><span data-stu-id="8ae07-126">*puArgErr*</span></span> 
</dt> <dd>

<span data-ttu-id="8ae07-127">Указатель на индекс в списке параметров *пдисппарамс* , где произошла последняя ошибка.</span><span class="sxs-lookup"><span data-stu-id="8ae07-127">Pointer to the index within the *pDispParams* parameter list where the last error occurred.</span></span>

</dd> <dt>

<span data-ttu-id="8ae07-128">*бстреам*</span><span class="sxs-lookup"><span data-stu-id="8ae07-128">*bStream*</span></span> 
</dt> <dd>

<span data-ttu-id="8ae07-129">Значение, указывающее, является ли параметр *времени* значением времени потока (**true**) или значением времени презентации (**false**).</span><span class="sxs-lookup"><span data-stu-id="8ae07-129">Value indicating whether the *time* parameter is a stream-time value (**TRUE**) or a presentation-time value (**FALSE**).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8ae07-130">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="8ae07-130">Return value</span></span>

<span data-ttu-id="8ae07-131">\_При успешном выполнении возвращает значение ОК.</span><span class="sxs-lookup"><span data-stu-id="8ae07-131">Returns S\_OK if successful.</span></span> <span data-ttu-id="8ae07-132">Возвращает E \_ OUTOFMEMORY, если *ппкмд* возвращает из создания нового объекта [**кдеферредкомманд**](cdeferredcommand.md) со значением **null**.</span><span class="sxs-lookup"><span data-stu-id="8ae07-132">Returns E\_OUTOFMEMORY if *ppCmd* returns from creating the new [**CDeferredCommand**](cdeferredcommand.md) object with a value of **NULL**.</span></span> <span data-ttu-id="8ae07-133">В противном случае возвращает **значение HRESULT** , указывающее на ошибку при попытке создать новый объект **кдеферредкомманд** .</span><span class="sxs-lookup"><span data-stu-id="8ae07-133">Otherwise, returns an **HRESULT** that indicates an error from attempting to create a new **CDeferredCommand** object.</span></span> <span data-ttu-id="8ae07-134">Если возникает ошибка, объект не помещается в очередь.</span><span class="sxs-lookup"><span data-stu-id="8ae07-134">If there is an error, no object has been queued.</span></span>

## <a name="remarks"></a><span data-ttu-id="8ae07-135">Комментарии</span><span class="sxs-lookup"><span data-stu-id="8ae07-135">Remarks</span></span>

<span data-ttu-id="8ae07-136">Новый объект [**кдеферредкомманд**](cdeferredcommand.md) будет инициализирован с параметрами и будет добавлен в очередь во время создания.</span><span class="sxs-lookup"><span data-stu-id="8ae07-136">The new [**CDeferredCommand**](cdeferredcommand.md) object will be initialized with the parameters and will be added to the queue during construction.</span></span> <span data-ttu-id="8ae07-137">Этот метод аналогичен методу **IDispatch:: Invoke** .</span><span class="sxs-lookup"><span data-stu-id="8ae07-137">This method is similar to the **IDispatch::Invoke** method.</span></span>

<span data-ttu-id="8ae07-138">Значения параметра *вфлагс* включают следующее:</span><span class="sxs-lookup"><span data-stu-id="8ae07-138">Values for the *wFlags* parameter include the following:</span></span>



| <span data-ttu-id="8ae07-139">Значение</span><span class="sxs-lookup"><span data-stu-id="8ae07-139">Value</span></span>                    | <span data-ttu-id="8ae07-140">Описание</span><span class="sxs-lookup"><span data-stu-id="8ae07-140">Description</span></span>                                                                                                                                                          |
|--------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8ae07-141">\_метод Dispatch</span><span class="sxs-lookup"><span data-stu-id="8ae07-141">DISPATCH\_METHOD</span></span>         | <span data-ttu-id="8ae07-142">Элемент выполняется как метод.</span><span class="sxs-lookup"><span data-stu-id="8ae07-142">The member is being run as a method.</span></span> <span data-ttu-id="8ae07-143">Если свойство имеет такое же имя, \_ можно задать и флаг диспетчеризации пропертижет.</span><span class="sxs-lookup"><span data-stu-id="8ae07-143">If a property has the same name, both this and the DISPATCH\_PROPERTYGET flag can be set.</span></span>                                       |
| <span data-ttu-id="8ae07-144">\_ПРОПЕРТИЖЕТ диспетчеризации</span><span class="sxs-lookup"><span data-stu-id="8ae07-144">DISPATCH\_PROPERTYGET</span></span>    | <span data-ttu-id="8ae07-145">Элемент извлекается как свойство или элемент данных.</span><span class="sxs-lookup"><span data-stu-id="8ae07-145">The member is being retrieved as a property or data member.</span></span>                                                                                                          |
| <span data-ttu-id="8ae07-146">\_ПРОПЕРТИПУТ диспетчеризации</span><span class="sxs-lookup"><span data-stu-id="8ae07-146">DISPATCH\_PROPERTYPUT</span></span>    | <span data-ttu-id="8ae07-147">Элемент изменяется как свойство или элемент данных.</span><span class="sxs-lookup"><span data-stu-id="8ae07-147">The member is being changed as a property or data member.</span></span>                                                                                                            |
| <span data-ttu-id="8ae07-148">\_ПРОПЕРТИПУТРЕФ диспетчеризации</span><span class="sxs-lookup"><span data-stu-id="8ae07-148">DISPATCH\_PROPERTYPUTREF</span></span> | <span data-ttu-id="8ae07-149">Элемент изменяется с помощью ссылочного назначения, а не назначения значения.</span><span class="sxs-lookup"><span data-stu-id="8ae07-149">The member is being changed via a reference assignment, rather than a value assignment.</span></span> <span data-ttu-id="8ae07-150">Это значение допустимо, только если свойство принимает ссылку на объект.</span><span class="sxs-lookup"><span data-stu-id="8ae07-150">This value is valid only when the property accepts a reference to an object.</span></span> |



 

## <a name="requirements"></a><span data-ttu-id="8ae07-151">Требования</span><span class="sxs-lookup"><span data-stu-id="8ae07-151">Requirements</span></span>



| <span data-ttu-id="8ae07-152">Требование</span><span class="sxs-lookup"><span data-stu-id="8ae07-152">Requirement</span></span> | <span data-ttu-id="8ae07-153">Значение</span><span class="sxs-lookup"><span data-stu-id="8ae07-153">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8ae07-154">Header</span><span class="sxs-lookup"><span data-stu-id="8ae07-154">Header</span></span><br/>  | <dl> <span data-ttu-id="8ae07-155"><dt>Винутил. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="8ae07-155"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="8ae07-156">Библиотека</span><span class="sxs-lookup"><span data-stu-id="8ae07-156">Library</span></span><br/> | <dl> <span data-ttu-id="8ae07-157"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="8ae07-157"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8ae07-158">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="8ae07-158">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8ae07-159">**Класс Ккмдкуеуе**</span><span class="sxs-lookup"><span data-stu-id="8ae07-159">**CCmdQueue Class**</span></span>](ccmdqueue.md)
</dt> </dl>

 

 




