---
title: Метод Reset Иенумбаккграундкопифилес (Deliveryoptimization. h)
description: Сбрасывает последовательность перечисления в начало.
ms.assetid: 6A303069-105C-4053-A8C5-2ECF60E789DE
keywords:
- Reset - метод
- Метод Reset, интерфейс Иенумбаккграундкопифилес
- Интерфейс Иенумбаккграундкопифилес, метод Reset
topic_type:
- apiref
api_name:
- IEnumBackgroundCopyFiles.Reset
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 314c7cae44ae48402642c202a624b9a60590e55b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103891737"
---
# <a name="ienumbackgroundcopyfilesreset-method"></a><span data-ttu-id="b167f-106">Метод Иенумбаккграундкопифилес:: Reset</span><span class="sxs-lookup"><span data-stu-id="b167f-106">IEnumBackgroundCopyFiles::Reset method</span></span>

<span data-ttu-id="b167f-107">Сбрасывает последовательность перечисления в начало.</span><span class="sxs-lookup"><span data-stu-id="b167f-107">Resets the enumeration sequence to the beginning.</span></span>

## <a name="syntax"></a><span data-ttu-id="b167f-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="b167f-108">Syntax</span></span>


```C++
HRESULT Reset();
```



## <a name="parameters"></a><span data-ttu-id="b167f-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="b167f-109">Parameters</span></span>

<span data-ttu-id="b167f-110">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="b167f-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="b167f-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="b167f-111">Return value</span></span>

<span data-ttu-id="b167f-112">Этот метод возвращает **S_OK** при успешном или одном из стандартных значений **HRESULT** com при ошибке.</span><span class="sxs-lookup"><span data-stu-id="b167f-112">This method returns **S_OK** on success or one of the standard COM **HRESULT** values on error.</span></span>

## <a name="requirements"></a><span data-ttu-id="b167f-113">Требования</span><span class="sxs-lookup"><span data-stu-id="b167f-113">Requirements</span></span>



| <span data-ttu-id="b167f-114">Требование</span><span class="sxs-lookup"><span data-stu-id="b167f-114">Requirement</span></span> | <span data-ttu-id="b167f-115">Значение</span><span class="sxs-lookup"><span data-stu-id="b167f-115">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b167f-116">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="b167f-116">Minimum supported client</span></span><br/> | <span data-ttu-id="b167f-117">\[Только для настольных приложений Windows 10 версии 1709\]</span><span class="sxs-lookup"><span data-stu-id="b167f-117">Windows 10, version 1709 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="b167f-118">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="b167f-118">Minimum supported server</span></span><br/> | <span data-ttu-id="b167f-119">\[Только для настольных приложений Windows Server версии 1709\]</span><span class="sxs-lookup"><span data-stu-id="b167f-119">Windows Server, version 1709 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="b167f-120">Header</span><span class="sxs-lookup"><span data-stu-id="b167f-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="b167f-121"><dt>Deliveryoptimization. h</dt></span><span class="sxs-lookup"><span data-stu-id="b167f-121"><dt>Deliveryoptimization.h</dt></span></span> </dl>   |
| <span data-ttu-id="b167f-122">IDL</span><span class="sxs-lookup"><span data-stu-id="b167f-122">IDL</span></span><br/>                      | <dl> <span data-ttu-id="b167f-123"><dt>DeliveryOptimization. idl</dt></span><span class="sxs-lookup"><span data-stu-id="b167f-123"><dt>DeliveryOptimization.idl</dt></span></span> </dl> |
| <span data-ttu-id="b167f-124">Библиотека</span><span class="sxs-lookup"><span data-stu-id="b167f-124">Library</span></span><br/>                  | <dl> <span data-ttu-id="b167f-125"><dt>Досвк. lib</dt></span><span class="sxs-lookup"><span data-stu-id="b167f-125"><dt>Dosvc.lib</dt></span></span> </dl>                |
| <span data-ttu-id="b167f-126">DLL</span><span class="sxs-lookup"><span data-stu-id="b167f-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b167f-127"><dt>Dosvc.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b167f-127"><dt>Dosvc.dll</dt></span></span> </dl>                |
| <span data-ttu-id="b167f-128">IID</span><span class="sxs-lookup"><span data-stu-id="b167f-128">IID</span></span><br/>                      | <span data-ttu-id="b167f-129">IID_IEnumBackgroundCopyFiles определен как CA51E165-C365-424C-8D41-24AAA4FF3C40</span><span class="sxs-lookup"><span data-stu-id="b167f-129">IID_IEnumBackgroundCopyFiles is defined as CA51E165-C365-424C-8D41-24AAA4FF3C40</span></span><br/>         |



## <a name="see-also"></a><span data-ttu-id="b167f-130">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="b167f-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b167f-131">**иенумбаккграундкопифилес**</span><span class="sxs-lookup"><span data-stu-id="b167f-131">**IEnumBackgroundCopyFiles**</span></span>](ienumbackgroundcopyfiles-.md)
</dt> </dl>

 

 





