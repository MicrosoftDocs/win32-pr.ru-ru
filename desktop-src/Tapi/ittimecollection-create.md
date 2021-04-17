---
description: Метод Create создает новый компонент Иттиме.
ms.assetid: dee50454-8358-4898-b098-2de51505b658
title: 'Метод Иттимеколлектион:: Create (Сдпблб. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: df62bbc8f1ad2a24a9b80a7f5d0a25bc01f713d8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105675277"
---
# <a name="ittimecollectioncreate-method"></a><span data-ttu-id="5a2f7-103">Метод Иттимеколлектион:: Create</span><span class="sxs-lookup"><span data-stu-id="5a2f7-103">ITTimeCollection::Create method</span></span>

<span data-ttu-id="5a2f7-104">\[ В Windows Vista, Windows Server 2008 и последующих версиях операционной системы нельзя использовать встречные средства и элементы управления Конференц-телефонией и интерфейсы.</span><span class="sxs-lookup"><span data-stu-id="5a2f7-104">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="5a2f7-105">API клиента RTC предоставляет аналогичные функциональные возможности.\]</span><span class="sxs-lookup"><span data-stu-id="5a2f7-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="5a2f7-106">Метод **CREATE** создает новый компонент [**иттиме**](ittime.md) .</span><span class="sxs-lookup"><span data-stu-id="5a2f7-106">The **Create** method creates a new [**ITTime**](ittime.md) component.</span></span>

## <a name="syntax"></a><span data-ttu-id="5a2f7-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="5a2f7-107">Syntax</span></span>


```C++
HRESULT Create(
  [in]  LONG   Index,
  [out] ITTime **ppTime
);
```



## <a name="parameters"></a><span data-ttu-id="5a2f7-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="5a2f7-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5a2f7-109">*Индекс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="5a2f7-109">*Index* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5a2f7-110">Индекс создаваемого элемента.</span><span class="sxs-lookup"><span data-stu-id="5a2f7-110">Index of the item to create.</span></span> <span data-ttu-id="5a2f7-111">(Индексный массив основан на единицах.)</span><span class="sxs-lookup"><span data-stu-id="5a2f7-111">(The index array is one-based.)</span></span>

</dd> <dt>

<span data-ttu-id="5a2f7-112">*пптиме* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="5a2f7-112">*ppTime* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="5a2f7-113">Указатель на созданный компонент b.</span><span class="sxs-lookup"><span data-stu-id="5a2f7-113">Pointer to the b component created.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5a2f7-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="5a2f7-114">Return value</span></span>

<span data-ttu-id="5a2f7-115">Этот метод может возвращать одно из этих значений.</span><span class="sxs-lookup"><span data-stu-id="5a2f7-115">This method can return one of these values.</span></span>



| <span data-ttu-id="5a2f7-116">Значение</span><span class="sxs-lookup"><span data-stu-id="5a2f7-116">Value</span></span>                                                                                         | <span data-ttu-id="5a2f7-117">Значение</span><span class="sxs-lookup"><span data-stu-id="5a2f7-117">Meaning</span></span>                                                         |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="5a2f7-118"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="5a2f7-118"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="5a2f7-119">Метод успешно выполнен.</span><span class="sxs-lookup"><span data-stu-id="5a2f7-119">Method succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="5a2f7-120"><dt>**\_указатель E**</dt></span><span class="sxs-lookup"><span data-stu-id="5a2f7-120"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="5a2f7-121">Параметр *пптиме* не является допустимым указателем.</span><span class="sxs-lookup"><span data-stu-id="5a2f7-121">The *ppTime* parameter is not a valid pointer.</span></span><br/>       |
| <dl> <span data-ttu-id="5a2f7-122"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="5a2f7-122"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="5a2f7-123">Недопустимый параметр *индекса* .</span><span class="sxs-lookup"><span data-stu-id="5a2f7-123">The *Index* parameter is not valid.</span></span><br/>                  |
| <dl> <span data-ttu-id="5a2f7-124"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="5a2f7-124"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="5a2f7-125">Недостаточно памяти для выполнения операции.</span><span class="sxs-lookup"><span data-stu-id="5a2f7-125">Insufficient memory exists to perform the operation.</span></span><br/> |
| <dl> <span data-ttu-id="5a2f7-126"><dt>**\_Ошибка E**</dt></span><span class="sxs-lookup"><span data-stu-id="5a2f7-126"><dt>**E\_FAIL**</dt></span></span> </dl>        | <span data-ttu-id="5a2f7-127">Незаданная ошибка.</span><span class="sxs-lookup"><span data-stu-id="5a2f7-127">Unspecified error.</span></span><br/>                                   |
| <dl> <span data-ttu-id="5a2f7-128"><dt>**E \_ нотимпл**</dt></span><span class="sxs-lookup"><span data-stu-id="5a2f7-128"><dt>**E\_NOTIMPL**</dt></span></span> </dl>     | <span data-ttu-id="5a2f7-129">Этот метод еще не реализован.</span><span class="sxs-lookup"><span data-stu-id="5a2f7-129">This method is not yet implemented.</span></span><br/>                  |



 

## <a name="remarks"></a><span data-ttu-id="5a2f7-130">Комментарии</span><span class="sxs-lookup"><span data-stu-id="5a2f7-130">Remarks</span></span>

<span data-ttu-id="5a2f7-131">TAPI вызывает метод **AddRef** в интерфейсе [**иттиме**](ittime.md) , возвращенном методом **иттимеколлектион:: Create**.</span><span class="sxs-lookup"><span data-stu-id="5a2f7-131">TAPI calls the **AddRef** method on the [**ITTime**](ittime.md) interface returned by **ITTimeCollection::Create**.</span></span> <span data-ttu-id="5a2f7-132">Приложение должно вызвать **выпуск** в интерфейсе v, чтобы освободить ресурсы, связанные с ним.</span><span class="sxs-lookup"><span data-stu-id="5a2f7-132">The application must call **Release** on the v interface to free resources associated with it.</span></span>

<span data-ttu-id="5a2f7-133">Эта функция может передавать данные по сети в незашифрованном виде; Таким образом, кто-то, кто прослушивает сеть, может прочитать данные.</span><span class="sxs-lookup"><span data-stu-id="5a2f7-133">This function may send data over the wire in unencrypted form; therefore, someone eavesdropping on the network may be able to read the data.</span></span> <span data-ttu-id="5a2f7-134">Прежде чем использовать этот метод, следует учесть угрозу безопасности при отправке данных в виде открытого текста.</span><span class="sxs-lookup"><span data-stu-id="5a2f7-134">The security risk of sending the data in clear text should be considered before using this method.</span></span>

## <a name="requirements"></a><span data-ttu-id="5a2f7-135">Требования</span><span class="sxs-lookup"><span data-stu-id="5a2f7-135">Requirements</span></span>



| <span data-ttu-id="5a2f7-136">Требование</span><span class="sxs-lookup"><span data-stu-id="5a2f7-136">Requirement</span></span> | <span data-ttu-id="5a2f7-137">Значение</span><span class="sxs-lookup"><span data-stu-id="5a2f7-137">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="5a2f7-138">Версия TAPI</span><span class="sxs-lookup"><span data-stu-id="5a2f7-138">TAPI version</span></span><br/> | <span data-ttu-id="5a2f7-139">Требуется TAPI 3,0 или более поздней версии</span><span class="sxs-lookup"><span data-stu-id="5a2f7-139">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="5a2f7-140">Header</span><span class="sxs-lookup"><span data-stu-id="5a2f7-140">Header</span></span><br/>       | <dl> <span data-ttu-id="5a2f7-141"><dt>Сдпблб. h</dt></span><span class="sxs-lookup"><span data-stu-id="5a2f7-141"><dt>Sdpblb.h</dt></span></span> </dl>   |
| <span data-ttu-id="5a2f7-142">Библиотека</span><span class="sxs-lookup"><span data-stu-id="5a2f7-142">Library</span></span><br/>      | <dl> <span data-ttu-id="5a2f7-143"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="5a2f7-143"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="5a2f7-144">DLL</span><span class="sxs-lookup"><span data-stu-id="5a2f7-144">DLL</span></span><br/>          | <dl> <span data-ttu-id="5a2f7-145"><dt>Sdpblb.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5a2f7-145"><dt>Sdpblb.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5a2f7-146">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="5a2f7-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5a2f7-147">**иттимеколлектион**</span><span class="sxs-lookup"><span data-stu-id="5a2f7-147">**ITTimeCollection**</span></span>](ittimecollection.md)
</dt> <dt>

[<span data-ttu-id="5a2f7-148">**иттиме**</span><span class="sxs-lookup"><span data-stu-id="5a2f7-148">**ITTime**</span></span>](ittime.md)
</dt> </dl>

 

 




