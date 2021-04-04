---
title: Метод Иенумбаккграундкопифилес Next (Deliveryoptimization. h)
description: Возвращает заданное число элементов последовательности перечисления. Если в последовательности осталось меньше запрошенного числа элементов, то он извлекает оставшиеся элементы.
ms.assetid: 31E603EC-2684-487D-AB37-4C6A6F661298
keywords:
- Метод Next
- Метод Next, интерфейс Иенумбаккграундкопифилес
- Интерфейс Иенумбаккграундкопифилес, метод Next
topic_type:
- apiref
api_name:
- IEnumBackgroundCopyFiles.Next
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 504b9083f4bdb1651496b4ab2d3b937740596243
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103989132"
---
# <a name="ienumbackgroundcopyfilesnext-method"></a><span data-ttu-id="9e017-107">Метод Иенумбаккграундкопифилес:: Next</span><span class="sxs-lookup"><span data-stu-id="9e017-107">IEnumBackgroundCopyFiles::Next method</span></span>

<span data-ttu-id="9e017-108">Возвращает заданное число элементов последовательности перечисления.</span><span class="sxs-lookup"><span data-stu-id="9e017-108">Retrieves a specified number of items in the enumeration sequence.</span></span> <span data-ttu-id="9e017-109">Если в последовательности осталось меньше запрошенного числа элементов, то он извлекает оставшиеся элементы.</span><span class="sxs-lookup"><span data-stu-id="9e017-109">If there are fewer than the requested number of elements left in the sequence, it retrieves the remaining elements.</span></span>

## <a name="syntax"></a><span data-ttu-id="9e017-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="9e017-110">Syntax</span></span>


```C++
HRESULT Next(
  [in]  ULONG               celt,
  [out] IBackgroundCopyFile **rgelt,
  [out] ULONG               *pceltFetched
);
```



## <a name="parameters"></a><span data-ttu-id="9e017-111">Параметры</span><span class="sxs-lookup"><span data-stu-id="9e017-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9e017-112">*celt* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="9e017-112">*celt* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9e017-113">Число запрошенных элементов.</span><span class="sxs-lookup"><span data-stu-id="9e017-113">Number of elements requested.</span></span>

</dd> <dt>

<span data-ttu-id="9e017-114">*rgelt* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="9e017-114">*rgelt* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="9e017-115">Массив объектов [**ибаккграундкопифиле**](ibackgroundcopyfile.md) .</span><span class="sxs-lookup"><span data-stu-id="9e017-115">Array of [**IBackgroundCopyFile**](ibackgroundcopyfile.md) objects.</span></span> <span data-ttu-id="9e017-116">По завершении необходимо освободить каждый объект в *rgelt* .</span><span class="sxs-lookup"><span data-stu-id="9e017-116">You must release each object in *rgelt* when done.</span></span>

</dd> <dt>

<span data-ttu-id="9e017-117">*пцелтфетчед* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="9e017-117">*pceltFetched* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="9e017-118">Число элементов, возвращаемых в *rgelt*.</span><span class="sxs-lookup"><span data-stu-id="9e017-118">Number of elements returned in *rgelt*.</span></span> <span data-ttu-id="9e017-119">Если параметр *celt* равен 1, можно установить значение *Пцелтфетчед* равным **null** .</span><span class="sxs-lookup"><span data-stu-id="9e017-119">You can set *pceltFetched* to **NULL** if *celt* is one.</span></span> <span data-ttu-id="9e017-120">В противном случае инициализируйте значение *пцелтфетчед* значением 0 перед вызовом этого метода.</span><span class="sxs-lookup"><span data-stu-id="9e017-120">Otherwise, initialize the value of *pceltFetched* to 0 before calling this method.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9e017-121">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="9e017-121">Return value</span></span>

<span data-ttu-id="9e017-122">Этот метод возвращает следующие значения **HRESULT** , а также другие.</span><span class="sxs-lookup"><span data-stu-id="9e017-122">This method returns the following **HRESULT** values, as well as others.</span></span>



| <span data-ttu-id="9e017-123">Код возврата</span><span class="sxs-lookup"><span data-stu-id="9e017-123">Return code</span></span>                                                                              | <span data-ttu-id="9e017-124">Описание</span><span class="sxs-lookup"><span data-stu-id="9e017-124">Description</span></span>                                                        |
|------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="9e017-125"><dt>S_OK \* \* \* \*</dt></span><span class="sxs-lookup"><span data-stu-id="9e017-125"><dt>\*\*\*\*S_OK\*\*\*\*</dt></span></span> </dl> | <span data-ttu-id="9e017-126">Число запрошенных элементов успешно возвращено.</span><span class="sxs-lookup"><span data-stu-id="9e017-126">Successfully returned the number of requested elements.</span></span><br/> |
| <dl> <span data-ttu-id="9e017-127"><dt>**S_FALSE**</dt></span><span class="sxs-lookup"><span data-stu-id="9e017-127"><dt>**S_FALSE**</dt></span></span> </dl>  | <span data-ttu-id="9e017-128">Возвращаемое значение меньше числа запрошенных элементов.</span><span class="sxs-lookup"><span data-stu-id="9e017-128">Returned less than the number of requested elements.</span></span><br/>    |



 

## <a name="requirements"></a><span data-ttu-id="9e017-129">Требования</span><span class="sxs-lookup"><span data-stu-id="9e017-129">Requirements</span></span>



| <span data-ttu-id="9e017-130">Требование</span><span class="sxs-lookup"><span data-stu-id="9e017-130">Requirement</span></span> | <span data-ttu-id="9e017-131">Значение</span><span class="sxs-lookup"><span data-stu-id="9e017-131">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9e017-132">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="9e017-132">Minimum supported client</span></span><br/> | <span data-ttu-id="9e017-133">\[Только для настольных приложений Windows 10 версии 1709\]</span><span class="sxs-lookup"><span data-stu-id="9e017-133">Windows 10, version 1709 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="9e017-134">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="9e017-134">Minimum supported server</span></span><br/> | <span data-ttu-id="9e017-135">\[Только для настольных приложений Windows Server версии 1709\]</span><span class="sxs-lookup"><span data-stu-id="9e017-135">Windows Server, version 1709 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="9e017-136">Header</span><span class="sxs-lookup"><span data-stu-id="9e017-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="9e017-137"><dt>Deliveryoptimization. h</dt></span><span class="sxs-lookup"><span data-stu-id="9e017-137"><dt>Deliveryoptimization.h</dt></span></span> </dl>   |
| <span data-ttu-id="9e017-138">IDL</span><span class="sxs-lookup"><span data-stu-id="9e017-138">IDL</span></span><br/>                      | <dl> <span data-ttu-id="9e017-139"><dt>DeliveryOptimization. idl</dt></span><span class="sxs-lookup"><span data-stu-id="9e017-139"><dt>DeliveryOptimization.idl</dt></span></span> </dl> |
| <span data-ttu-id="9e017-140">Библиотека</span><span class="sxs-lookup"><span data-stu-id="9e017-140">Library</span></span><br/>                  | <dl> <span data-ttu-id="9e017-141"><dt>Досвк. lib</dt></span><span class="sxs-lookup"><span data-stu-id="9e017-141"><dt>Dosvc.lib</dt></span></span> </dl>                |
| <span data-ttu-id="9e017-142">DLL</span><span class="sxs-lookup"><span data-stu-id="9e017-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9e017-143"><dt>Dosvc.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9e017-143"><dt>Dosvc.dll</dt></span></span> </dl>                |
| <span data-ttu-id="9e017-144">IID</span><span class="sxs-lookup"><span data-stu-id="9e017-144">IID</span></span><br/>                      | <span data-ttu-id="9e017-145">IID_IEnumBackgroundCopyFiles определен как CA51E165-C365-424C-8D41-24AAA4FF3C40</span><span class="sxs-lookup"><span data-stu-id="9e017-145">IID_IEnumBackgroundCopyFiles is defined as CA51E165-C365-424C-8D41-24AAA4FF3C40</span></span><br/>         |



## <a name="see-also"></a><span data-ttu-id="9e017-146">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="9e017-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9e017-147">**иенумбаккграундкопифилес**</span><span class="sxs-lookup"><span data-stu-id="9e017-147">**IEnumBackgroundCopyFiles**</span></span>](ienumbackgroundcopyfiles-.md)
</dt> </dl>

 

 





