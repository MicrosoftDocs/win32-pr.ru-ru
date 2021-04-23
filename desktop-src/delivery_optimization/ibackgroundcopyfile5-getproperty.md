---
title: Метод IBackgroundCopyFile5-Property (Deliveryoptimization. h)
description: Возвращает универсальное свойство передачи файла оптимизации доставки (DO).
ms.assetid: E2E96A0F-5670-4DE7-9DF8-A215AFAD0E8A
keywords:
- Метод GetProperty
- Метод Property, интерфейс IBackgroundCopyFile5
- Интерфейс IBackgroundCopyFile5, метод метода Property
topic_type:
- apiref
api_name:
- IBackgroundCopyFile5.GetProperty
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 84c6a9f96fc332bda940573bde78d7dd05efeeb1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104135742"
---
# <a name="ibackgroundcopyfile5getproperty-method"></a><span data-ttu-id="1b359-106">IBackgroundCopyFile5:: метод Property</span><span class="sxs-lookup"><span data-stu-id="1b359-106">IBackgroundCopyFile5::GetProperty method</span></span>

<span data-ttu-id="1b359-107">Возвращает универсальное свойство передачи файла оптимизации доставки (DO).</span><span class="sxs-lookup"><span data-stu-id="1b359-107">Gets a generic property of a Delivery Optimization (DO) file transfer.</span></span>

## <a name="syntax"></a><span data-ttu-id="1b359-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="1b359-108">Syntax</span></span>


```C++
HRESULT GetProperty(
  [in]  BITS_FILE_PROPERTY_ID    PropertyId,
  [out] BITS_FILE_PROPERTY_VALUE *PropertyValue
);
```



## <a name="parameters"></a><span data-ttu-id="1b359-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="1b359-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1b359-110">*PropertyId* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="1b359-110">*PropertyId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1b359-111">Указывает свойство файла, значение которого необходимо извлечь.</span><span class="sxs-lookup"><span data-stu-id="1b359-111">Specifies the file property whose value is to be retrieved.</span></span>

</dd> <dt>

<span data-ttu-id="1b359-112">*Propertyvalue* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="1b359-112">*PropertyValue* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="1b359-113">Значение свойства, возвращаемое как указатель на BITS_FILE_PROPERTY_VALUEное объединение.</span><span class="sxs-lookup"><span data-stu-id="1b359-113">The property value, returned as a pointer to a BITS_FILE_PROPERTY_VALUE union.</span></span> <span data-ttu-id="1b359-114">Используйте поле Union, подходящее для значения идентификатора свойства, переданного в.</span><span class="sxs-lookup"><span data-stu-id="1b359-114">Use the union field appropriate for the property ID value passed in.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1b359-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="1b359-115">Return value</span></span>

<span data-ttu-id="1b359-116">Если этот метод завершается с ошибкой, возвращается **S_OK**.</span><span class="sxs-lookup"><span data-stu-id="1b359-116">If this method succeeds, it returns **S_OK**.</span></span> <span data-ttu-id="1b359-117">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="1b359-117">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="1b359-118">Требования</span><span class="sxs-lookup"><span data-stu-id="1b359-118">Requirements</span></span>



| <span data-ttu-id="1b359-119">Требование</span><span class="sxs-lookup"><span data-stu-id="1b359-119">Requirement</span></span> | <span data-ttu-id="1b359-120">Значение</span><span class="sxs-lookup"><span data-stu-id="1b359-120">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1b359-121">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="1b359-121">Minimum supported client</span></span><br/> | <span data-ttu-id="1b359-122">\[Только для настольных приложений Windows 10 версии 1709\]</span><span class="sxs-lookup"><span data-stu-id="1b359-122">Windows 10, version 1709 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="1b359-123">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="1b359-123">Minimum supported server</span></span><br/> | <span data-ttu-id="1b359-124">\[Только для настольных приложений Windows Server версии 1709\]</span><span class="sxs-lookup"><span data-stu-id="1b359-124">Windows Server, version 1709 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="1b359-125">Header</span><span class="sxs-lookup"><span data-stu-id="1b359-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="1b359-126"><dt>Deliveryoptimization. h</dt></span><span class="sxs-lookup"><span data-stu-id="1b359-126"><dt>Deliveryoptimization.h</dt></span></span> </dl>   |
| <span data-ttu-id="1b359-127">IDL</span><span class="sxs-lookup"><span data-stu-id="1b359-127">IDL</span></span><br/>                      | <dl> <span data-ttu-id="1b359-128"><dt>DeliveryOptimization. idl</dt></span><span class="sxs-lookup"><span data-stu-id="1b359-128"><dt>DeliveryOptimization.idl</dt></span></span> </dl> |
| <span data-ttu-id="1b359-129">Библиотека</span><span class="sxs-lookup"><span data-stu-id="1b359-129">Library</span></span><br/>                  | <dl> <span data-ttu-id="1b359-130"><dt>Досвк. lib</dt></span><span class="sxs-lookup"><span data-stu-id="1b359-130"><dt>Dosvc.lib</dt></span></span> </dl>                |
| <span data-ttu-id="1b359-131">DLL</span><span class="sxs-lookup"><span data-stu-id="1b359-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1b359-132"><dt>Dosvc.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1b359-132"><dt>Dosvc.dll</dt></span></span> </dl>                |
| <span data-ttu-id="1b359-133">IID</span><span class="sxs-lookup"><span data-stu-id="1b359-133">IID</span></span><br/>                      | <span data-ttu-id="1b359-134">IID_IBackgroundCopyFile5 определен как 85C1657F-DAFC-40E8-8834-DF18EA25717E</span><span class="sxs-lookup"><span data-stu-id="1b359-134">IID_IBackgroundCopyFile5 is defined as 85C1657F-DAFC-40E8-8834-DF18EA25717E</span></span><br/>             |



## <a name="see-also"></a><span data-ttu-id="1b359-135">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="1b359-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1b359-136">**IBackgroundCopyFile5**</span><span class="sxs-lookup"><span data-stu-id="1b359-136">**IBackgroundCopyFile5**</span></span>](ibackgroundcopyfile5.md)
</dt> <dt>

[<span data-ttu-id="1b359-137">**IBackgroundCopyFile5. SetProperty**</span><span class="sxs-lookup"><span data-stu-id="1b359-137">**IBackgroundCopyFile5.SetProperty**</span></span>](ibackgroundcopyfile5-setproperty.md)
</dt> </dl>

 

 





