---
title: Метод SetProperty IBackgroundCopyFile5 (Deliveryoptimization. h)
description: Задает универсальное свойство для передачи файла оптимизации доставки (DO).
ms.assetid: 63B6806E-47D6-49B0-9867-628C110540D0
keywords:
- SetProperty — метод
- Метод SetProperty, интерфейс IBackgroundCopyFile5
- Интерфейс IBackgroundCopyFile5, метод SetProperty
topic_type:
- apiref
api_name:
- IBackgroundCopyFile5.SetProperty
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 7f519ee77af0ae6e0c3d1d036aeeb6a8ad712870
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103988562"
---
# <a name="ibackgroundcopyfile5setproperty-method"></a><span data-ttu-id="70a47-106">Метод IBackgroundCopyFile5:: SetProperty</span><span class="sxs-lookup"><span data-stu-id="70a47-106">IBackgroundCopyFile5::SetProperty method</span></span>

<span data-ttu-id="70a47-107">Задает универсальное свойство для передачи файла оптимизации доставки (DO).</span><span class="sxs-lookup"><span data-stu-id="70a47-107">Sets a generic property of a Delivery Optimization (DO) file transfer.</span></span>

## <a name="syntax"></a><span data-ttu-id="70a47-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="70a47-108">Syntax</span></span>


```C++
HRESULT SetProperty(
  [in]  BITS_FILE_PROPERTY_ID    PropertyId,
  [out] BITS_FILE_PROPERTY_VALUE *ProertyValue
);
```



## <a name="parameters"></a><span data-ttu-id="70a47-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="70a47-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="70a47-110">*PropertyId* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="70a47-110">*PropertyId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="70a47-111">Указывает свойство, которое необходимо задать.</span><span class="sxs-lookup"><span data-stu-id="70a47-111">Specifies the property to be set.</span></span>

</dd> <dt>

<span data-ttu-id="70a47-112">*Проертивалуе* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="70a47-112">*ProertyValue* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="70a47-113">Указатель на объединение, указывающее значение, которое необходимо задать.</span><span class="sxs-lookup"><span data-stu-id="70a47-113">A pointer to a union that specifies the value to be set.</span></span> <span data-ttu-id="70a47-114">Используется элемент объединения, соответствующий ИДЕНТИФИКАТОРу свойства.</span><span class="sxs-lookup"><span data-stu-id="70a47-114">The union member appropriate for the property ID is used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="70a47-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="70a47-115">Return value</span></span>

<span data-ttu-id="70a47-116">Если этот метод завершается с ошибкой, возвращается **S_OK**.</span><span class="sxs-lookup"><span data-stu-id="70a47-116">If this method succeeds, it returns **S_OK**.</span></span> <span data-ttu-id="70a47-117">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="70a47-117">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="70a47-118">Требования</span><span class="sxs-lookup"><span data-stu-id="70a47-118">Requirements</span></span>



| <span data-ttu-id="70a47-119">Требование</span><span class="sxs-lookup"><span data-stu-id="70a47-119">Requirement</span></span> | <span data-ttu-id="70a47-120">Значение</span><span class="sxs-lookup"><span data-stu-id="70a47-120">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="70a47-121">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="70a47-121">Minimum supported client</span></span><br/> | <span data-ttu-id="70a47-122">\[Только для настольных приложений Windows 10 версии 1709\]</span><span class="sxs-lookup"><span data-stu-id="70a47-122">Windows 10, version 1709 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="70a47-123">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="70a47-123">Minimum supported server</span></span><br/> | <span data-ttu-id="70a47-124">\[Только для настольных приложений Windows Server версии 1709\]</span><span class="sxs-lookup"><span data-stu-id="70a47-124">Windows Server, version 1709 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="70a47-125">Header</span><span class="sxs-lookup"><span data-stu-id="70a47-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="70a47-126"><dt>Deliveryoptimization. h</dt></span><span class="sxs-lookup"><span data-stu-id="70a47-126"><dt>Deliveryoptimization.h</dt></span></span> </dl>   |
| <span data-ttu-id="70a47-127">IDL</span><span class="sxs-lookup"><span data-stu-id="70a47-127">IDL</span></span><br/>                      | <dl> <span data-ttu-id="70a47-128"><dt>DeliveryOptimization. idl</dt></span><span class="sxs-lookup"><span data-stu-id="70a47-128"><dt>DeliveryOptimization.idl</dt></span></span> </dl> |
| <span data-ttu-id="70a47-129">Библиотека</span><span class="sxs-lookup"><span data-stu-id="70a47-129">Library</span></span><br/>                  | <dl> <span data-ttu-id="70a47-130"><dt>Досвк. lib</dt></span><span class="sxs-lookup"><span data-stu-id="70a47-130"><dt>Dosvc.lib</dt></span></span> </dl>                |
| <span data-ttu-id="70a47-131">DLL</span><span class="sxs-lookup"><span data-stu-id="70a47-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="70a47-132"><dt>Dosvc.dll</dt></span><span class="sxs-lookup"><span data-stu-id="70a47-132"><dt>Dosvc.dll</dt></span></span> </dl>                |
| <span data-ttu-id="70a47-133">IID</span><span class="sxs-lookup"><span data-stu-id="70a47-133">IID</span></span><br/>                      | <span data-ttu-id="70a47-134">IID_IBackgroundCopyFile5 определен как 85C1657F-DAFC-40E8-8834-DF18EA25717E</span><span class="sxs-lookup"><span data-stu-id="70a47-134">IID_IBackgroundCopyFile5 is defined as 85C1657F-DAFC-40E8-8834-DF18EA25717E</span></span><br/>             |



## <a name="see-also"></a><span data-ttu-id="70a47-135">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="70a47-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="70a47-136">**IBackgroundCopyFile5**</span><span class="sxs-lookup"><span data-stu-id="70a47-136">**IBackgroundCopyFile5**</span></span>](ibackgroundcopyfile5.md)
</dt> <dt>

[<span data-ttu-id="70a47-137">**IBackgroundCopyFile5., свойство**</span><span class="sxs-lookup"><span data-stu-id="70a47-137">**IBackgroundCopyFile5.GetProperty**</span></span>](ibackgroundcopyfile5-getproperty.md)
</dt> </dl>

 

 





