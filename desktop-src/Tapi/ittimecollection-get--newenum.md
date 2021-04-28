---
description: 'Метод Иттимеколлектион:: get__NewEnum — метод Get \_ \_ NewEnum Возвращает перечислитель для коллекции.'
ms.assetid: 0c2d739d-736d-4773-9747-1107546a973c
title: 'Метод Иттимеколлектион:: get__NewEnum (Сдпблб. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: acfc9d616efb58c6173f2c9c6e5913d27776958c
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108088892"
---
# <a name="ittimecollectionget__newenum-method"></a><span data-ttu-id="82766-103">Метод Иттимеколлектион:: Get \_ \_ NewEnum</span><span class="sxs-lookup"><span data-stu-id="82766-103">ITTimeCollection::get\_\_NewEnum method</span></span>

<span data-ttu-id="82766-104">\[ В Windows Vista, Windows Server 2008 и последующих версиях операционной системы нельзя использовать встречные средства и элементы управления Конференц-телефонией и интерфейсы.</span><span class="sxs-lookup"><span data-stu-id="82766-104">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="82766-105">API клиента RTC предоставляет аналогичные функциональные возможности.\]</span><span class="sxs-lookup"><span data-stu-id="82766-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="82766-106">Метод **Get \_ \_ NewEnum** Возвращает перечислитель для коллекции.</span><span class="sxs-lookup"><span data-stu-id="82766-106">The **get\_\_NewEnum** method returns an enumerator for the collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="82766-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="82766-107">Syntax</span></span>


```C++
HRESULT get__NewEnum(
  [out] IUnknown **pVal
);
```



## <a name="parameters"></a><span data-ttu-id="82766-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="82766-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="82766-109">*Pval* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="82766-109">*pVal* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="82766-110">Указатель на интерфейс [IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown) в объекте перечислителя для коллекции.</span><span class="sxs-lookup"><span data-stu-id="82766-110">Pointer to an [IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface on an enumerator object for the collection.</span></span>

<span data-ttu-id="82766-111">Вызовите метод [QueryInterface](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) на возвращенном интерфейсе **IUnknown** , чтобы получить указатель на интерфейс перечисления [IEnumVARIANT](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) в коллекции.</span><span class="sxs-lookup"><span data-stu-id="82766-111">Call the [QueryInterface](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) method on the returned **IUnknown** interface to obtain a pointer to an [IEnumVARIANT](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) enumeration interface on the collection.</span></span> <span data-ttu-id="82766-112">**IEnumVARIANT** предоставляет ряд методов, которые можно использовать для итерации по коллекции.</span><span class="sxs-lookup"><span data-stu-id="82766-112">**IEnumVARIANT** provides a number of methods that you can use to iterate through the collection.</span></span>

<span data-ttu-id="82766-113">Дополнительные сведения см. в разделе "Примечания".</span><span class="sxs-lookup"><span data-stu-id="82766-113">For more information, see the following Remarks section.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="82766-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="82766-114">Return value</span></span>

<span data-ttu-id="82766-115">Этот метод может возвращать одно из этих значений.</span><span class="sxs-lookup"><span data-stu-id="82766-115">This method can return one of these values.</span></span>



| <span data-ttu-id="82766-116">Код возврата</span><span class="sxs-lookup"><span data-stu-id="82766-116">Return code</span></span>                                                                                   | <span data-ttu-id="82766-117">Описание</span><span class="sxs-lookup"><span data-stu-id="82766-117">Description</span></span>                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="82766-118"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="82766-118"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="82766-119">Метод успешно выполнен.</span><span class="sxs-lookup"><span data-stu-id="82766-119">Method succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="82766-120"><dt>**\_указатель E**</dt></span><span class="sxs-lookup"><span data-stu-id="82766-120"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="82766-121">Параметр *Pval* не является допустимым указателем.</span><span class="sxs-lookup"><span data-stu-id="82766-121">The *pVal* parameter is not a valid pointer.</span></span><br/>         |
| <dl> <span data-ttu-id="82766-122"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="82766-122"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="82766-123">Недостаточно памяти для выполнения операции.</span><span class="sxs-lookup"><span data-stu-id="82766-123">Insufficient memory exists to perform the operation.</span></span><br/> |
| <dl> <span data-ttu-id="82766-124"><dt>**\_Ошибка E**</dt></span><span class="sxs-lookup"><span data-stu-id="82766-124"><dt>**E\_FAIL**</dt></span></span> </dl>        | <span data-ttu-id="82766-125">Незаданная ошибка.</span><span class="sxs-lookup"><span data-stu-id="82766-125">Unspecified error.</span></span><br/>                                   |
| <dl> <span data-ttu-id="82766-126"><dt>**E \_ нотимпл**</dt></span><span class="sxs-lookup"><span data-stu-id="82766-126"><dt>**E\_NOTIMPL**</dt></span></span> </dl>     | <span data-ttu-id="82766-127">Этот метод еще не реализован.</span><span class="sxs-lookup"><span data-stu-id="82766-127">This method is not yet implemented.</span></span><br/>                  |



 

## <a name="remarks"></a><span data-ttu-id="82766-128">Remarks</span><span class="sxs-lookup"><span data-stu-id="82766-128">Remarks</span></span>

<span data-ttu-id="82766-129">Этот метод является взаимозаменяемым с [**Get \_ енумератиониф**](ittimecollection-get-enumerationif.md) , за исключением того, что он возвращает **IUnknown** вместо [**иенумтиме**](ienumtime.md).</span><span class="sxs-lookup"><span data-stu-id="82766-129">This method is interchangeable with [**get\_EnumerationIf**](ittimecollection-get-enumerationif.md) except that it returns **IUnknown** instead of [**IEnumTime**](ienumtime.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="82766-130">Требования</span><span class="sxs-lookup"><span data-stu-id="82766-130">Requirements</span></span>



| <span data-ttu-id="82766-131">Требование</span><span class="sxs-lookup"><span data-stu-id="82766-131">Requirement</span></span> | <span data-ttu-id="82766-132">Значение</span><span class="sxs-lookup"><span data-stu-id="82766-132">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="82766-133">Версия TAPI</span><span class="sxs-lookup"><span data-stu-id="82766-133">TAPI version</span></span><br/> | <span data-ttu-id="82766-134">Требуется TAPI 3,0 или более поздней версии</span><span class="sxs-lookup"><span data-stu-id="82766-134">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="82766-135">Header</span><span class="sxs-lookup"><span data-stu-id="82766-135">Header</span></span><br/>       | <dl> <span data-ttu-id="82766-136"><dt>Сдпблб. h</dt></span><span class="sxs-lookup"><span data-stu-id="82766-136"><dt>Sdpblb.h</dt></span></span> </dl>   |
| <span data-ttu-id="82766-137">Библиотека</span><span class="sxs-lookup"><span data-stu-id="82766-137">Library</span></span><br/>      | <dl> <span data-ttu-id="82766-138"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="82766-138"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="82766-139">DLL</span><span class="sxs-lookup"><span data-stu-id="82766-139">DLL</span></span><br/>          | <dl> <span data-ttu-id="82766-140"><dt>Sdpblb.dll</dt></span><span class="sxs-lookup"><span data-stu-id="82766-140"><dt>Sdpblb.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="82766-141">См. также</span><span class="sxs-lookup"><span data-stu-id="82766-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="82766-142">**иттимеколлектион**</span><span class="sxs-lookup"><span data-stu-id="82766-142">**ITTimeCollection**</span></span>](ittimecollection.md)
</dt> <dt>

[<span data-ttu-id="82766-143">**иттиме**</span><span class="sxs-lookup"><span data-stu-id="82766-143">**ITTime**</span></span>](ittime.md)
</dt> </dl>

 

