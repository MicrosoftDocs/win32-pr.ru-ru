---
description: Метод Get \_ \_ NewEnum Возвращает перечислитель для коллекции.
ms.assetid: 22b1eb48-e1ef-4694-a1dc-b2de326989c8
title: 'Метод Итмедиаколлектион:: get__NewEnum (Сдпблб. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bfa5655d70026fe2c481aedad0e76923f4caa646
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105688992"
---
# <a name="itmediacollectionget__newenum-method"></a><span data-ttu-id="2a6fe-103">Метод Итмедиаколлектион:: Get \_ \_ NewEnum</span><span class="sxs-lookup"><span data-stu-id="2a6fe-103">ITMediaCollection::get\_\_NewEnum method</span></span>

<span data-ttu-id="2a6fe-104">\[ В Windows Vista, Windows Server 2008 и последующих версиях операционной системы нельзя использовать встречные средства и элементы управления Конференц-телефонией и интерфейсы.</span><span class="sxs-lookup"><span data-stu-id="2a6fe-104">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="2a6fe-105">API клиента RTC предоставляет аналогичные функциональные возможности.\]</span><span class="sxs-lookup"><span data-stu-id="2a6fe-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="2a6fe-106">Метод **Get \_ \_ NewEnum** Возвращает перечислитель для коллекции.</span><span class="sxs-lookup"><span data-stu-id="2a6fe-106">The **get\_\_NewEnum** method returns an enumerator for the collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="2a6fe-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="2a6fe-107">Syntax</span></span>


```C++
HRESULT get__NewEnum(
  [out] IUnknown **pVal
);
```



## <a name="parameters"></a><span data-ttu-id="2a6fe-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="2a6fe-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2a6fe-109">*Pval* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="2a6fe-109">*pVal* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="2a6fe-110">Указатель на интерфейс [IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown) в объекте перечислителя для коллекции.</span><span class="sxs-lookup"><span data-stu-id="2a6fe-110">Pointer to an [IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface on an enumerator object for the collection.</span></span>

<span data-ttu-id="2a6fe-111">Вызовите метод [QueryInterface](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) на возвращенном интерфейсе **IUnknown** , чтобы получить указатель на интерфейс перечисления [IEnumVARIANT](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) в коллекции.</span><span class="sxs-lookup"><span data-stu-id="2a6fe-111">Call the [QueryInterface](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) method on the returned **IUnknown** interface to obtain a pointer to an [IEnumVARIANT](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) enumeration interface on the collection.</span></span> <span data-ttu-id="2a6fe-112">**IEnumVARIANT** предоставляет ряд методов, которые можно использовать для итерации по коллекции.</span><span class="sxs-lookup"><span data-stu-id="2a6fe-112">**IEnumVARIANT** provides a number of methods that you can use to iterate through the collection.</span></span>

<span data-ttu-id="2a6fe-113">Дополнительные сведения см. в разделе "Примечания".</span><span class="sxs-lookup"><span data-stu-id="2a6fe-113">For more information, see the following Remarks section.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2a6fe-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="2a6fe-114">Return value</span></span>

<span data-ttu-id="2a6fe-115">Этот метод может возвращать одно из этих значений.</span><span class="sxs-lookup"><span data-stu-id="2a6fe-115">This method can return one of these values.</span></span>



| <span data-ttu-id="2a6fe-116">Код возврата</span><span class="sxs-lookup"><span data-stu-id="2a6fe-116">Return code</span></span>                                                                                   | <span data-ttu-id="2a6fe-117">Описание</span><span class="sxs-lookup"><span data-stu-id="2a6fe-117">Description</span></span>                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="2a6fe-118"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="2a6fe-118"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="2a6fe-119">Метод успешно выполнен.</span><span class="sxs-lookup"><span data-stu-id="2a6fe-119">Method succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="2a6fe-120"><dt>**\_указатель E**</dt></span><span class="sxs-lookup"><span data-stu-id="2a6fe-120"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="2a6fe-121">Параметр *Pval* не является допустимым указателем.</span><span class="sxs-lookup"><span data-stu-id="2a6fe-121">The *pVal* parameter is not a valid pointer.</span></span><br/>         |
| <dl> <span data-ttu-id="2a6fe-122"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="2a6fe-122"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="2a6fe-123">Недостаточно памяти для выполнения операции.</span><span class="sxs-lookup"><span data-stu-id="2a6fe-123">Insufficient memory exists to perform the operation.</span></span><br/> |
| <dl> <span data-ttu-id="2a6fe-124"><dt>**\_Ошибка E**</dt></span><span class="sxs-lookup"><span data-stu-id="2a6fe-124"><dt>**E\_FAIL**</dt></span></span> </dl>        | <span data-ttu-id="2a6fe-125">Незаданная ошибка.</span><span class="sxs-lookup"><span data-stu-id="2a6fe-125">Unspecified error.</span></span><br/>                                   |
| <dl> <span data-ttu-id="2a6fe-126"><dt>**E \_ нотимпл**</dt></span><span class="sxs-lookup"><span data-stu-id="2a6fe-126"><dt>**E\_NOTIMPL**</dt></span></span> </dl>     | <span data-ttu-id="2a6fe-127">Этот метод еще не реализован.</span><span class="sxs-lookup"><span data-stu-id="2a6fe-127">This method is not yet implemented.</span></span><br/>                  |



 

## <a name="remarks"></a><span data-ttu-id="2a6fe-128">Комментарии</span><span class="sxs-lookup"><span data-stu-id="2a6fe-128">Remarks</span></span>

<span data-ttu-id="2a6fe-129">Этот метод является взаимозаменяемым с [**Get \_ енумератиониф**](itmediacollection-get-enumerationif.md) , за исключением того, что он возвращает **IUnknown** вместо [**иенуммедиа**](ienummedia.md).</span><span class="sxs-lookup"><span data-stu-id="2a6fe-129">This method is interchangeable with [**get\_EnumerationIf**](itmediacollection-get-enumerationif.md) except that it returns **IUnknown** instead of [**IEnumMedia**](ienummedia.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="2a6fe-130">Требования</span><span class="sxs-lookup"><span data-stu-id="2a6fe-130">Requirements</span></span>



| <span data-ttu-id="2a6fe-131">Требование</span><span class="sxs-lookup"><span data-stu-id="2a6fe-131">Requirement</span></span> | <span data-ttu-id="2a6fe-132">Значение</span><span class="sxs-lookup"><span data-stu-id="2a6fe-132">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="2a6fe-133">Версия TAPI</span><span class="sxs-lookup"><span data-stu-id="2a6fe-133">TAPI version</span></span><br/> | <span data-ttu-id="2a6fe-134">Требуется TAPI 3,0 или более поздней версии</span><span class="sxs-lookup"><span data-stu-id="2a6fe-134">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="2a6fe-135">Header</span><span class="sxs-lookup"><span data-stu-id="2a6fe-135">Header</span></span><br/>       | <dl> <span data-ttu-id="2a6fe-136"><dt>Сдпблб. h</dt></span><span class="sxs-lookup"><span data-stu-id="2a6fe-136"><dt>Sdpblb.h</dt></span></span> </dl>   |
| <span data-ttu-id="2a6fe-137">Библиотека</span><span class="sxs-lookup"><span data-stu-id="2a6fe-137">Library</span></span><br/>      | <dl> <span data-ttu-id="2a6fe-138"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="2a6fe-138"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="2a6fe-139">DLL</span><span class="sxs-lookup"><span data-stu-id="2a6fe-139">DLL</span></span><br/>          | <dl> <span data-ttu-id="2a6fe-140"><dt>Sdpblb.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2a6fe-140"><dt>Sdpblb.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2a6fe-141">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="2a6fe-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2a6fe-142">**итмедиаколлектион**</span><span class="sxs-lookup"><span data-stu-id="2a6fe-142">**ITMediaCollection**</span></span>](itmediacollection.md)
</dt> </dl>

 

