---
description: Метод Get \_ енумератиониф получает указатель на интерфейс перечисления мультимедиа.
ms.assetid: d5f1e10f-e5ad-45e6-a5ec-024905603012
title: 'Метод Итмедиаколлектион:: get_EnumerationIf (Сдпблб. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 28a7e7d85c1f7a433a31360fabc8b5dac71e68ad
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105689047"
---
# <a name="itmediacollectionget_enumerationif-method"></a><span data-ttu-id="5d99c-103">Метод Итмедиаколлектион:: Get \_ енумератиониф</span><span class="sxs-lookup"><span data-stu-id="5d99c-103">ITMediaCollection::get\_EnumerationIf method</span></span>

<span data-ttu-id="5d99c-104">\[ В Windows Vista, Windows Server 2008 и последующих версиях операционной системы нельзя использовать встречные средства и элементы управления Конференц-телефонией и интерфейсы.</span><span class="sxs-lookup"><span data-stu-id="5d99c-104">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="5d99c-105">API клиента RTC предоставляет аналогичные функциональные возможности.\]</span><span class="sxs-lookup"><span data-stu-id="5d99c-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="5d99c-106">Метод **Get \_ енумератиониф** получает указатель на интерфейс перечисления мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="5d99c-106">The **get\_EnumerationIf** method gets a pointer to a media enumeration interface.</span></span>

## <a name="syntax"></a><span data-ttu-id="5d99c-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="5d99c-107">Syntax</span></span>


```C++
HRESULT get_EnumerationIf(
  [out] IEnumMedia **pVal
);
```



## <a name="parameters"></a><span data-ttu-id="5d99c-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="5d99c-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5d99c-109">*Pval* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="5d99c-109">*pVal* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="5d99c-110">Указатель на интерфейс [**иенуммедиа**](ienummedia.md) для требуемого элемента.</span><span class="sxs-lookup"><span data-stu-id="5d99c-110">Pointer to the [**IEnumMedia**](ienummedia.md) interface for the desired item.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5d99c-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="5d99c-111">Return value</span></span>

<span data-ttu-id="5d99c-112">Этот метод может возвращать одно из этих значений.</span><span class="sxs-lookup"><span data-stu-id="5d99c-112">This method can return one of these values.</span></span>



| <span data-ttu-id="5d99c-113">Значение</span><span class="sxs-lookup"><span data-stu-id="5d99c-113">Value</span></span>                                                                                         | <span data-ttu-id="5d99c-114">Значение</span><span class="sxs-lookup"><span data-stu-id="5d99c-114">Meaning</span></span>                                                         |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="5d99c-115"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="5d99c-115"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="5d99c-116">Метод успешно выполнен.</span><span class="sxs-lookup"><span data-stu-id="5d99c-116">Method succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="5d99c-117"><dt>**\_указатель E**</dt></span><span class="sxs-lookup"><span data-stu-id="5d99c-117"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="5d99c-118">Параметр *Pval* не является допустимым указателем.</span><span class="sxs-lookup"><span data-stu-id="5d99c-118">The *pVal* parameter is not a valid pointer.</span></span><br/>         |
| <dl> <span data-ttu-id="5d99c-119"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="5d99c-119"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="5d99c-120">Недостаточно памяти для выполнения операции.</span><span class="sxs-lookup"><span data-stu-id="5d99c-120">Insufficient memory exists to perform the operation.</span></span><br/> |
| <dl> <span data-ttu-id="5d99c-121"><dt>**\_Ошибка E**</dt></span><span class="sxs-lookup"><span data-stu-id="5d99c-121"><dt>**E\_FAIL**</dt></span></span> </dl>        | <span data-ttu-id="5d99c-122">Незаданная ошибка.</span><span class="sxs-lookup"><span data-stu-id="5d99c-122">Unspecified error.</span></span><br/>                                   |
| <dl> <span data-ttu-id="5d99c-123"><dt>**E \_ нотимпл**</dt></span><span class="sxs-lookup"><span data-stu-id="5d99c-123"><dt>**E\_NOTIMPL**</dt></span></span> </dl>     | <span data-ttu-id="5d99c-124">Этот метод еще не реализован.</span><span class="sxs-lookup"><span data-stu-id="5d99c-124">This method is not yet implemented.</span></span><br/>                  |



 

## <a name="remarks"></a><span data-ttu-id="5d99c-125">Комментарии</span><span class="sxs-lookup"><span data-stu-id="5d99c-125">Remarks</span></span>

<span data-ttu-id="5d99c-126">Этот метод является взаимозаменяемым с [**Get \_ \_ NewEnum**](itmediacollection-get--newenum.md) , за исключением того, что он возвращает [**иенуммедиа**](ienummedia.md) вместо **IUnknown**.</span><span class="sxs-lookup"><span data-stu-id="5d99c-126">This method is interchangeable with [**get\_\_NewEnum**](itmediacollection-get--newenum.md) except that it returns [**IEnumMedia**](ienummedia.md) instead of **IUnknown**.</span></span>

<span data-ttu-id="5d99c-127">TAPI вызывает метод **AddRef** в интерфейсе [**иенуммедиа**](ienummedia.md) , возвращенном методом **итмедиаколлектион:: Get \_ енумератионлф**.</span><span class="sxs-lookup"><span data-stu-id="5d99c-127">TAPI calls the **AddRef** method on the [**IEnumMedia**](ienummedia.md) interface returned by **ITMediaCollection::get\_Enumerationlf**.</span></span> <span data-ttu-id="5d99c-128">Приложение должно вызвать **выпуск** в интерфейсе **иенуммедиа** , чтобы освободить ресурсы, связанные с ним.</span><span class="sxs-lookup"><span data-stu-id="5d99c-128">The application must call **Release** on the **IEnumMedia** interface to free resources associated with it.</span></span>

## <a name="requirements"></a><span data-ttu-id="5d99c-129">Требования</span><span class="sxs-lookup"><span data-stu-id="5d99c-129">Requirements</span></span>



| <span data-ttu-id="5d99c-130">Требование</span><span class="sxs-lookup"><span data-stu-id="5d99c-130">Requirement</span></span> | <span data-ttu-id="5d99c-131">Значение</span><span class="sxs-lookup"><span data-stu-id="5d99c-131">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="5d99c-132">Версия TAPI</span><span class="sxs-lookup"><span data-stu-id="5d99c-132">TAPI version</span></span><br/> | <span data-ttu-id="5d99c-133">Требуется TAPI 3,0 или более поздней версии</span><span class="sxs-lookup"><span data-stu-id="5d99c-133">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="5d99c-134">Header</span><span class="sxs-lookup"><span data-stu-id="5d99c-134">Header</span></span><br/>       | <dl> <span data-ttu-id="5d99c-135"><dt>Сдпблб. h</dt></span><span class="sxs-lookup"><span data-stu-id="5d99c-135"><dt>Sdpblb.h</dt></span></span> </dl>   |
| <span data-ttu-id="5d99c-136">Библиотека</span><span class="sxs-lookup"><span data-stu-id="5d99c-136">Library</span></span><br/>      | <dl> <span data-ttu-id="5d99c-137"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="5d99c-137"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="5d99c-138">DLL</span><span class="sxs-lookup"><span data-stu-id="5d99c-138">DLL</span></span><br/>          | <dl> <span data-ttu-id="5d99c-139"><dt>Sdpblb.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5d99c-139"><dt>Sdpblb.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5d99c-140">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="5d99c-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5d99c-141">**иенуммедиа**</span><span class="sxs-lookup"><span data-stu-id="5d99c-141">**IEnumMedia**</span></span>](ienummedia.md)
</dt> <dt>

[<span data-ttu-id="5d99c-142">**итмедиаколлектион**</span><span class="sxs-lookup"><span data-stu-id="5d99c-142">**ITMediaCollection**</span></span>](itmediacollection.md)
</dt> </dl>

 

 




