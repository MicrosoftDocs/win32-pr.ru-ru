---
description: Метод Жетнумберофкапабилитиес извлекает количество возможностей, связанных с текущим форматом.
ms.assetid: 26e51c0d-c1cb-410f-ab19-eb884afa8431
title: 'Метод Итформатконтрол:: Жетнумберофкапабилитиес (Ипмсп. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e29153f5ee9ce8c5e12b93a1d219905c40f80418
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105688958"
---
# <a name="itformatcontrolgetnumberofcapabilities-method"></a><span data-ttu-id="41399-103">Метод Итформатконтрол:: Жетнумберофкапабилитиес</span><span class="sxs-lookup"><span data-stu-id="41399-103">ITFormatControl::GetNumberOfCapabilities method</span></span>

<span data-ttu-id="41399-104">\[ Этот метод недоступен для использования в Windows Vista, Windows Server 2008 и последующих версиях операционной системы.</span><span class="sxs-lookup"><span data-stu-id="41399-104">\[ This method is not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="41399-105">API клиента RTC предоставляет аналогичные функциональные возможности.\]</span><span class="sxs-lookup"><span data-stu-id="41399-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="41399-106">Метод **жетнумберофкапабилитиес** извлекает количество возможностей, связанных с текущим форматом.</span><span class="sxs-lookup"><span data-stu-id="41399-106">The **GetNumberOfCapabilities** method retrieves the number of capabilities associated with the current format.</span></span>

## <a name="syntax"></a><span data-ttu-id="41399-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="41399-107">Syntax</span></span>


```C++
HRESULT GetNumberOfCapabilities(
  [out] DWORD *pdwCount
);
```



## <a name="parameters"></a><span data-ttu-id="41399-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="41399-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="41399-109">*пдвкаунт* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="41399-109">*pdwCount* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="41399-110">Число возможностей.</span><span class="sxs-lookup"><span data-stu-id="41399-110">Count of the capabilities.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="41399-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="41399-111">Return value</span></span>

<span data-ttu-id="41399-112">Этот метод может возвращать одно из этих значений.</span><span class="sxs-lookup"><span data-stu-id="41399-112">This method can return one of these values.</span></span>



| <span data-ttu-id="41399-113">Код возврата</span><span class="sxs-lookup"><span data-stu-id="41399-113">Return code</span></span>                                                                                   | <span data-ttu-id="41399-114">Описание</span><span class="sxs-lookup"><span data-stu-id="41399-114">Description</span></span>                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="41399-115"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="41399-115"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="41399-116">Метод успешно выполнен.</span><span class="sxs-lookup"><span data-stu-id="41399-116">Method succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="41399-117"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="41399-117"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="41399-118">Недостаточно памяти для выполнения операции.</span><span class="sxs-lookup"><span data-stu-id="41399-118">Insufficient memory exists to perform the operation.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="41399-119">Требования</span><span class="sxs-lookup"><span data-stu-id="41399-119">Requirements</span></span>



| <span data-ttu-id="41399-120">Требование</span><span class="sxs-lookup"><span data-stu-id="41399-120">Requirement</span></span> | <span data-ttu-id="41399-121">Значение</span><span class="sxs-lookup"><span data-stu-id="41399-121">Value</span></span> |
|-------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="41399-122">Версия TAPI</span><span class="sxs-lookup"><span data-stu-id="41399-122">TAPI version</span></span><br/> | <span data-ttu-id="41399-123">Требуется TAPI 3,1</span><span class="sxs-lookup"><span data-stu-id="41399-123">Requires TAPI 3.1</span></span><br/>                                                         |
| <span data-ttu-id="41399-124">Header</span><span class="sxs-lookup"><span data-stu-id="41399-124">Header</span></span><br/>       | <dl> <span data-ttu-id="41399-125"><dt>Ипмсп. h</dt></span><span class="sxs-lookup"><span data-stu-id="41399-125"><dt>Ipmsp.h</dt></span></span> </dl>   |
| <span data-ttu-id="41399-126">Библиотека</span><span class="sxs-lookup"><span data-stu-id="41399-126">Library</span></span><br/>      | <dl> <span data-ttu-id="41399-127"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="41399-127"><dt>Uuid.lib</dt></span></span> </dl>  |
| <span data-ttu-id="41399-128">DLL</span><span class="sxs-lookup"><span data-stu-id="41399-128">DLL</span></span><br/>          | <dl> <span data-ttu-id="41399-129"><dt>Tapi3.dll</dt></span><span class="sxs-lookup"><span data-stu-id="41399-129"><dt>Tapi3.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="41399-130">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="41399-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="41399-131">**итформатконтрол**</span><span class="sxs-lookup"><span data-stu-id="41399-131">**ITFormatControl**</span></span>](itformatcontrol.md)
</dt> </dl>

 

 




