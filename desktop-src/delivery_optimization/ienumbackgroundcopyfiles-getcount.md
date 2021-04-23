---
title: Метод Иенумбаккграундкопифилес-Count (Deliveryoptimization. h)
description: Извлекает количество файлов в перечислении.
ms.assetid: EE27679D-3AC0-49DA-992F-8DEA10C21646
keywords:
- GetCount - метод
- Метод NOCOUNT, интерфейс Иенумбаккграундкопифилес
- Интерфейс Иенумбаккграундкопифилес, метод NOCOUNT
topic_type:
- apiref
api_name:
- IEnumBackgroundCopyFiles.GetCount
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 05e2672f0cda3c572024a0865b2fb534dddb6598
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103802254"
---
# <a name="ienumbackgroundcopyfilesgetcount-method"></a><span data-ttu-id="6cd1b-106">Метод Иенумбаккграундкопифилес:: NOCOUNT</span><span class="sxs-lookup"><span data-stu-id="6cd1b-106">IEnumBackgroundCopyFiles::GetCount method</span></span>

<span data-ttu-id="6cd1b-107">Извлекает количество файлов в перечислении.</span><span class="sxs-lookup"><span data-stu-id="6cd1b-107">Retrieves a count of the number of files in the enumeration.</span></span>

## <a name="syntax"></a><span data-ttu-id="6cd1b-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="6cd1b-108">Syntax</span></span>


```C++
HRESULT GetCount(
  [out] ULONG *pCount
);
```



## <a name="parameters"></a><span data-ttu-id="6cd1b-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="6cd1b-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6cd1b-110">*pCount* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="6cd1b-110">*pCount* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6cd1b-111">Число файлов в перечислении.</span><span class="sxs-lookup"><span data-stu-id="6cd1b-111">Number of files in the enumeration.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6cd1b-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="6cd1b-112">Return value</span></span>

<span data-ttu-id="6cd1b-113">Этот метод возвращает **S_OK** при успешном или одном из стандартных значений **HRESULT** com при ошибке.</span><span class="sxs-lookup"><span data-stu-id="6cd1b-113">This method returns **S_OK** on success or one of the standard COM **HRESULT** values on error.</span></span>

## <a name="requirements"></a><span data-ttu-id="6cd1b-114">Требования</span><span class="sxs-lookup"><span data-stu-id="6cd1b-114">Requirements</span></span>



| <span data-ttu-id="6cd1b-115">Требование</span><span class="sxs-lookup"><span data-stu-id="6cd1b-115">Requirement</span></span> | <span data-ttu-id="6cd1b-116">Значение</span><span class="sxs-lookup"><span data-stu-id="6cd1b-116">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6cd1b-117">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="6cd1b-117">Minimum supported client</span></span><br/> | <span data-ttu-id="6cd1b-118">\[Только для настольных приложений Windows 10 версии 1709\]</span><span class="sxs-lookup"><span data-stu-id="6cd1b-118">Windows 10, version 1709 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="6cd1b-119">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="6cd1b-119">Minimum supported server</span></span><br/> | <span data-ttu-id="6cd1b-120">\[Только для настольных приложений Windows Server версии 1709\]</span><span class="sxs-lookup"><span data-stu-id="6cd1b-120">Windows Server, version 1709 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="6cd1b-121">Header</span><span class="sxs-lookup"><span data-stu-id="6cd1b-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="6cd1b-122"><dt>Deliveryoptimization. h</dt></span><span class="sxs-lookup"><span data-stu-id="6cd1b-122"><dt>Deliveryoptimization.h</dt></span></span> </dl>   |
| <span data-ttu-id="6cd1b-123">IDL</span><span class="sxs-lookup"><span data-stu-id="6cd1b-123">IDL</span></span><br/>                      | <dl> <span data-ttu-id="6cd1b-124"><dt>DeliveryOptimization. idl</dt></span><span class="sxs-lookup"><span data-stu-id="6cd1b-124"><dt>DeliveryOptimization.idl</dt></span></span> </dl> |
| <span data-ttu-id="6cd1b-125">Библиотека</span><span class="sxs-lookup"><span data-stu-id="6cd1b-125">Library</span></span><br/>                  | <dl> <span data-ttu-id="6cd1b-126"><dt>Досвк. lib</dt></span><span class="sxs-lookup"><span data-stu-id="6cd1b-126"><dt>Dosvc.lib</dt></span></span> </dl>                |
| <span data-ttu-id="6cd1b-127">DLL</span><span class="sxs-lookup"><span data-stu-id="6cd1b-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6cd1b-128"><dt>Dosvc.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6cd1b-128"><dt>Dosvc.dll</dt></span></span> </dl>                |
| <span data-ttu-id="6cd1b-129">IID</span><span class="sxs-lookup"><span data-stu-id="6cd1b-129">IID</span></span><br/>                      | <span data-ttu-id="6cd1b-130">IID_IEnumBackgroundCopyFiles определен как CA51E165-C365-424C-8D41-24AAA4FF3C40</span><span class="sxs-lookup"><span data-stu-id="6cd1b-130">IID_IEnumBackgroundCopyFiles is defined as CA51E165-C365-424C-8D41-24AAA4FF3C40</span></span><br/>         |



## <a name="see-also"></a><span data-ttu-id="6cd1b-131">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="6cd1b-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6cd1b-132">**иенумбаккграундкопифилес**</span><span class="sxs-lookup"><span data-stu-id="6cd1b-132">**IEnumBackgroundCopyFiles**</span></span>](ienumbackgroundcopyfiles-.md)
</dt> </dl>

 

 





