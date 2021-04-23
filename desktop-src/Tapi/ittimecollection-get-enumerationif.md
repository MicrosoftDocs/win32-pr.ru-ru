---
description: Метод Get \_ енумератиониф возвращает интерфейс перечисления иенумтиме, который перечисляет иттиме.
ms.assetid: 31f6fa94-d047-4c53-96ae-8dd7e66a4e33
title: 'Метод Иттимеколлектион:: get_EnumerationIf (Сдпблб. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a698fca73e923597b2dff5b82e3258dd79306f05
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105685351"
---
# <a name="ittimecollectionget_enumerationif-method"></a><span data-ttu-id="ed158-103">Метод Иттимеколлектион:: Get \_ енумератиониф</span><span class="sxs-lookup"><span data-stu-id="ed158-103">ITTimeCollection::get\_EnumerationIf method</span></span>

<span data-ttu-id="ed158-104">\[ В Windows Vista, Windows Server 2008 и последующих версиях операционной системы нельзя использовать встречные средства и элементы управления Конференц-телефонией и интерфейсы.</span><span class="sxs-lookup"><span data-stu-id="ed158-104">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="ed158-105">API клиента RTC предоставляет аналогичные функциональные возможности.\]</span><span class="sxs-lookup"><span data-stu-id="ed158-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="ed158-106">Метод **Get \_ енумератиониф** возвращает интерфейс перечисления [**Иенумтиме**](ienumtime.md) , который перечисляет [**иттиме**](ittime.md).</span><span class="sxs-lookup"><span data-stu-id="ed158-106">The **get\_EnumerationIf** method returns the [**IEnumTime**](ienumtime.md) enumeration interface that enumerates [**ITTime**](ittime.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="ed158-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="ed158-107">Syntax</span></span>


```C++
HRESULT get_EnumerationIf(
  [out] IEnumTime **pVal
);
```



## <a name="parameters"></a><span data-ttu-id="ed158-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="ed158-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ed158-109">*Pval* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="ed158-109">*pVal* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ed158-110">Указатель на интерфейс [**иенумтиме**](ienumtime.md) .</span><span class="sxs-lookup"><span data-stu-id="ed158-110">Pointer to the [**IEnumTime**](ienumtime.md) interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ed158-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="ed158-111">Return value</span></span>

<span data-ttu-id="ed158-112">Этот метод может возвращать одно из этих значений.</span><span class="sxs-lookup"><span data-stu-id="ed158-112">This method can return one of these values.</span></span>



| <span data-ttu-id="ed158-113">Значение</span><span class="sxs-lookup"><span data-stu-id="ed158-113">Value</span></span>                                                                                         | <span data-ttu-id="ed158-114">Значение</span><span class="sxs-lookup"><span data-stu-id="ed158-114">Meaning</span></span>                                                         |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="ed158-115"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="ed158-115"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="ed158-116">Метод успешно выполнен.</span><span class="sxs-lookup"><span data-stu-id="ed158-116">Method succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="ed158-117"><dt>**\_указатель E**</dt></span><span class="sxs-lookup"><span data-stu-id="ed158-117"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="ed158-118">Параметр *Pval* не является допустимым указателем.</span><span class="sxs-lookup"><span data-stu-id="ed158-118">The *pVal* parameter is not a valid pointer.</span></span><br/>         |
| <dl> <span data-ttu-id="ed158-119"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="ed158-119"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="ed158-120">Недостаточно памяти для выполнения операции.</span><span class="sxs-lookup"><span data-stu-id="ed158-120">Insufficient memory exists to perform the operation.</span></span><br/> |
| <dl> <span data-ttu-id="ed158-121"><dt>**\_Ошибка E**</dt></span><span class="sxs-lookup"><span data-stu-id="ed158-121"><dt>**E\_FAIL**</dt></span></span> </dl>        | <span data-ttu-id="ed158-122">Незаданная ошибка.</span><span class="sxs-lookup"><span data-stu-id="ed158-122">Unspecified error.</span></span><br/>                                   |
| <dl> <span data-ttu-id="ed158-123"><dt>**E \_ нотимпл**</dt></span><span class="sxs-lookup"><span data-stu-id="ed158-123"><dt>**E\_NOTIMPL**</dt></span></span> </dl>     | <span data-ttu-id="ed158-124">Этот метод еще не реализован.</span><span class="sxs-lookup"><span data-stu-id="ed158-124">This method is not yet implemented.</span></span><br/>                  |



 

## <a name="remarks"></a><span data-ttu-id="ed158-125">Комментарии</span><span class="sxs-lookup"><span data-stu-id="ed158-125">Remarks</span></span>

<span data-ttu-id="ed158-126">Этот метод является взаимозаменяемым с [**Get \_ \_ NewEnum**](ittimecollection-get--newenum.md) , за исключением того, что он возвращает [**иенумтиме**](ienumtime.md) вместо **IUnknown**.</span><span class="sxs-lookup"><span data-stu-id="ed158-126">This method is interchangeable with [**get\_\_NewEnum**](ittimecollection-get--newenum.md) except that it returns [**IEnumTime**](ienumtime.md) instead of **IUnknown**.</span></span>

<span data-ttu-id="ed158-127">TAPI вызывает метод **AddRef** в интерфейсе [**иенумтиме**](ienumtime.md) , возвращенном методом **иттимеколлектион:: Get \_ енумератиониф**.</span><span class="sxs-lookup"><span data-stu-id="ed158-127">TAPI calls the **AddRef** method on the [**IEnumTime**](ienumtime.md) interface returned by **ITTimeCollection::get\_EnumerationIf**.</span></span> <span data-ttu-id="ed158-128">Приложение должно вызвать **выпуск** в интерфейсе [**иенумтиме**](ienumtime.md) , чтобы освободить ресурсы, связанные с ним.</span><span class="sxs-lookup"><span data-stu-id="ed158-128">The application must call **Release** on the [**IEnumTime**](ienumtime.md) interface to free resources associated with it.</span></span>

## <a name="requirements"></a><span data-ttu-id="ed158-129">Требования</span><span class="sxs-lookup"><span data-stu-id="ed158-129">Requirements</span></span>



| <span data-ttu-id="ed158-130">Требование</span><span class="sxs-lookup"><span data-stu-id="ed158-130">Requirement</span></span> | <span data-ttu-id="ed158-131">Значение</span><span class="sxs-lookup"><span data-stu-id="ed158-131">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="ed158-132">Версия TAPI</span><span class="sxs-lookup"><span data-stu-id="ed158-132">TAPI version</span></span><br/> | <span data-ttu-id="ed158-133">Требуется TAPI 3,0 или более поздней версии</span><span class="sxs-lookup"><span data-stu-id="ed158-133">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="ed158-134">Header</span><span class="sxs-lookup"><span data-stu-id="ed158-134">Header</span></span><br/>       | <dl> <span data-ttu-id="ed158-135"><dt>Сдпблб. h</dt></span><span class="sxs-lookup"><span data-stu-id="ed158-135"><dt>Sdpblb.h</dt></span></span> </dl>   |
| <span data-ttu-id="ed158-136">Библиотека</span><span class="sxs-lookup"><span data-stu-id="ed158-136">Library</span></span><br/>      | <dl> <span data-ttu-id="ed158-137"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="ed158-137"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="ed158-138">DLL</span><span class="sxs-lookup"><span data-stu-id="ed158-138">DLL</span></span><br/>          | <dl> <span data-ttu-id="ed158-139"><dt>Sdpblb.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ed158-139"><dt>Sdpblb.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ed158-140">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="ed158-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ed158-141">**иенумтиме**</span><span class="sxs-lookup"><span data-stu-id="ed158-141">**IEnumTime**</span></span>](ienumtime.md)
</dt> <dt>

[<span data-ttu-id="ed158-142">**иттимеколлектион**</span><span class="sxs-lookup"><span data-stu-id="ed158-142">**ITTimeCollection**</span></span>](ittimecollection.md)
</dt> <dt>

[<span data-ttu-id="ed158-143">**иттиме**</span><span class="sxs-lookup"><span data-stu-id="ed158-143">**ITTime**</span></span>](ittime.md)
</dt> </dl>

 

 




