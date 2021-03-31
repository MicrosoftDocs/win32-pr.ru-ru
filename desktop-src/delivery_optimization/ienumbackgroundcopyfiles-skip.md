---
title: Метод Skip Иенумбаккграундкопифилес (Deliveryoptimization. h)
description: Пропускает следующее заданное число элементов в последовательности перечисления. Если в последовательности осталось меньше элементов, чем запрошенное число элементов для пропуска, он пропускается после последнего элемента последовательности.
ms.assetid: B01D4292-6BA5-4171-928B-AB2C555E2C2A
keywords:
- Skip - метод
- Метод Skip, интерфейс Иенумбаккграундкопифилес
- Интерфейс Иенумбаккграундкопифилес, метод Skip
topic_type:
- apiref
api_name:
- IEnumBackgroundCopyFiles.Skip
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 5d88a7d971ab93b90c844fc8d9d92d7f154c0ebf
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104071268"
---
# <a name="ienumbackgroundcopyfilesskip-method"></a><span data-ttu-id="b081e-107">Метод Иенумбаккграундкопифилес:: Skip</span><span class="sxs-lookup"><span data-stu-id="b081e-107">IEnumBackgroundCopyFiles::Skip method</span></span>

<span data-ttu-id="b081e-108">Пропускает следующее заданное число элементов в последовательности перечисления.</span><span class="sxs-lookup"><span data-stu-id="b081e-108">Skips the next specified number of elements in the enumeration sequence.</span></span> <span data-ttu-id="b081e-109">Если в последовательности осталось меньше элементов, чем запрошенное число элементов для пропуска, он пропускается после последнего элемента последовательности.</span><span class="sxs-lookup"><span data-stu-id="b081e-109">If there are fewer elements left in the sequence than the requested number of elements to skip, it skips past the last element in the sequence.</span></span>

## <a name="syntax"></a><span data-ttu-id="b081e-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="b081e-110">Syntax</span></span>


```C++
HRESULT Skip(
  [in] ULONG celt
);
```



## <a name="parameters"></a><span data-ttu-id="b081e-111">Параметры</span><span class="sxs-lookup"><span data-stu-id="b081e-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b081e-112">*celt* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="b081e-112">*celt* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b081e-113">Число пропускаемых элементов.</span><span class="sxs-lookup"><span data-stu-id="b081e-113">Number of elements to skip.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b081e-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="b081e-114">Return value</span></span>

<span data-ttu-id="b081e-115">Этот метод возвращает следующие значения **HRESULT** , а также другие.</span><span class="sxs-lookup"><span data-stu-id="b081e-115">This method returns the following **HRESULT** values, as well as others.</span></span>



| <span data-ttu-id="b081e-116">Код возврата</span><span class="sxs-lookup"><span data-stu-id="b081e-116">Return code</span></span>                                                                              | <span data-ttu-id="b081e-117">Описание</span><span class="sxs-lookup"><span data-stu-id="b081e-117">Description</span></span>                                                       |
|------------------------------------------------------------------------------------------|-------------------------------------------------------------------|
| <dl> <span data-ttu-id="b081e-118"><dt>S_OK \* \* \* \*</dt></span><span class="sxs-lookup"><span data-stu-id="b081e-118"><dt>\*\*\*\*S_OK\*\*\*\*</dt></span></span> </dl> | <span data-ttu-id="b081e-119">Число запрошенных элементов успешно пропущено.</span><span class="sxs-lookup"><span data-stu-id="b081e-119">Successfully skipped the number of requested elements.</span></span><br/> |
| <dl> <span data-ttu-id="b081e-120"><dt>**S_FALSE**</dt></span><span class="sxs-lookup"><span data-stu-id="b081e-120"><dt>**S_FALSE**</dt></span></span> </dl>  | <span data-ttu-id="b081e-121">Пропущено меньшее число запрошенных элементов.</span><span class="sxs-lookup"><span data-stu-id="b081e-121">Skipped less than the number of requested elements.</span></span><br/>    |



 

## <a name="requirements"></a><span data-ttu-id="b081e-122">Требования</span><span class="sxs-lookup"><span data-stu-id="b081e-122">Requirements</span></span>



| <span data-ttu-id="b081e-123">Требование</span><span class="sxs-lookup"><span data-stu-id="b081e-123">Requirement</span></span> | <span data-ttu-id="b081e-124">Значение</span><span class="sxs-lookup"><span data-stu-id="b081e-124">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b081e-125">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="b081e-125">Minimum supported client</span></span><br/> | <span data-ttu-id="b081e-126">\[Только для настольных приложений Windows 10 версии 1709\]</span><span class="sxs-lookup"><span data-stu-id="b081e-126">Windows 10, version 1709 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="b081e-127">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="b081e-127">Minimum supported server</span></span><br/> | <span data-ttu-id="b081e-128">\[Только для настольных приложений Windows Server версии 1709\]</span><span class="sxs-lookup"><span data-stu-id="b081e-128">Windows Server, version 1709 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="b081e-129">Header</span><span class="sxs-lookup"><span data-stu-id="b081e-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="b081e-130"><dt>Deliveryoptimization. h</dt></span><span class="sxs-lookup"><span data-stu-id="b081e-130"><dt>Deliveryoptimization.h</dt></span></span> </dl>   |
| <span data-ttu-id="b081e-131">IDL</span><span class="sxs-lookup"><span data-stu-id="b081e-131">IDL</span></span><br/>                      | <dl> <span data-ttu-id="b081e-132"><dt>DeliveryOptimization. idl</dt></span><span class="sxs-lookup"><span data-stu-id="b081e-132"><dt>DeliveryOptimization.idl</dt></span></span> </dl> |
| <span data-ttu-id="b081e-133">Библиотека</span><span class="sxs-lookup"><span data-stu-id="b081e-133">Library</span></span><br/>                  | <dl> <span data-ttu-id="b081e-134"><dt>Досвк. lib</dt></span><span class="sxs-lookup"><span data-stu-id="b081e-134"><dt>Dosvc.lib</dt></span></span> </dl>                |
| <span data-ttu-id="b081e-135">DLL</span><span class="sxs-lookup"><span data-stu-id="b081e-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b081e-136"><dt>Dosvc.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b081e-136"><dt>Dosvc.dll</dt></span></span> </dl>                |
| <span data-ttu-id="b081e-137">IID</span><span class="sxs-lookup"><span data-stu-id="b081e-137">IID</span></span><br/>                      | <span data-ttu-id="b081e-138">IID_IEnumBackgroundCopyFiles определен как CA51E165-C365-424C-8D41-24AAA4FF3C40</span><span class="sxs-lookup"><span data-stu-id="b081e-138">IID_IEnumBackgroundCopyFiles is defined as CA51E165-C365-424C-8D41-24AAA4FF3C40</span></span><br/>         |



## <a name="see-also"></a><span data-ttu-id="b081e-139">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="b081e-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b081e-140">**иенумбаккграундкопифилес**</span><span class="sxs-lookup"><span data-stu-id="b081e-140">**IEnumBackgroundCopyFiles**</span></span>](ienumbackgroundcopyfiles-.md)
</dt> </dl>

 

 





