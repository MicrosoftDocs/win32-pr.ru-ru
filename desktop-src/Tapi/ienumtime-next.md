---
description: 'Метод Иенумтиме:: Next — Следующий метод получает указанное число следующих элементов в последовательности перечисления.'
ms.assetid: e8ca77b8-0322-43b4-9996-26f584cf878a
title: 'Метод Иенумтиме:: Next (Сдпблб. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1487136b0e3e41ba11a23ba92500d2aa0758df79
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108118392"
---
# <a name="ienumtimenext-method"></a><span data-ttu-id="446ea-103">Метод Иенумтиме:: Next</span><span class="sxs-lookup"><span data-stu-id="446ea-103">IEnumTime::Next method</span></span>

<span data-ttu-id="446ea-104">\[ В Windows Vista, Windows Server 2008 и последующих версиях операционной системы нельзя использовать встречные средства и элементы управления Конференц-телефонией и интерфейсы.</span><span class="sxs-lookup"><span data-stu-id="446ea-104">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="446ea-105">API клиента RTC предоставляет аналогичные функциональные возможности.\]</span><span class="sxs-lookup"><span data-stu-id="446ea-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="446ea-106">**Следующий** метод получает указанное число следующих элементов в последовательности перечисления.</span><span class="sxs-lookup"><span data-stu-id="446ea-106">The **Next** method gets the next specified number of elements in the enumeration sequence.</span></span>

## <a name="syntax"></a><span data-ttu-id="446ea-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="446ea-107">Syntax</span></span>


```C++
HRESULT Next(
  [in]  ULONG  celt,
  [out] ITTime **pVal,
  [out] ULONG  *pceltFetched
);
```



## <a name="parameters"></a><span data-ttu-id="446ea-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="446ea-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="446ea-109">*celt* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="446ea-109">*celt* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="446ea-110">Число запрошенных элементов.</span><span class="sxs-lookup"><span data-stu-id="446ea-110">Number of elements requested.</span></span>

</dd> <dt>

<span data-ttu-id="446ea-111">*Pval* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="446ea-111">*pVal* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="446ea-112">Указатель на интерфейс [**иттиме**](ittime.md) .</span><span class="sxs-lookup"><span data-stu-id="446ea-112">Pointer to the [**ITTime**](ittime.md) interface.</span></span>

</dd> <dt>

<span data-ttu-id="446ea-113">*пцелтфетчед* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="446ea-113">*pceltFetched* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="446ea-114">Указатель на число фактически предоставляемых элементов.</span><span class="sxs-lookup"><span data-stu-id="446ea-114">Pointer to the number of elements actually supplied.</span></span> <span data-ttu-id="446ea-115">Может иметь **значение NULL** , если значение *celt* равно 1.</span><span class="sxs-lookup"><span data-stu-id="446ea-115">May be **NULL** if *celt* is 1.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="446ea-116">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="446ea-116">Return value</span></span>

<span data-ttu-id="446ea-117">Этот метод может возвращать одно из этих значений.</span><span class="sxs-lookup"><span data-stu-id="446ea-117">This method can return one of these values.</span></span>



| <span data-ttu-id="446ea-118">Значение</span><span class="sxs-lookup"><span data-stu-id="446ea-118">Value</span></span>                                                                                     | <span data-ttu-id="446ea-119">Значение</span><span class="sxs-lookup"><span data-stu-id="446ea-119">Meaning</span></span>                                                       |
|-------------------------------------------------------------------------------------------|---------------------------------------------------------------|
| <dl> <span data-ttu-id="446ea-120"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="446ea-120"><dt>**S\_OK**</dt></span></span> </dl>      | <span data-ttu-id="446ea-121">Метод возвратил *celt* число элементов.</span><span class="sxs-lookup"><span data-stu-id="446ea-121">Method returned *celt* number of elements.</span></span><br/>         |
| <dl> <span data-ttu-id="446ea-122"><dt>**S \_ false**</dt></span><span class="sxs-lookup"><span data-stu-id="446ea-122"><dt>**S\_FALSE**</dt></span></span> </dl>   | <span data-ttu-id="446ea-123">Количество оставшихся элементов меньше значения *celt*.</span><span class="sxs-lookup"><span data-stu-id="446ea-123">Number of elements remaining was less than *celt*.</span></span><br/> |
| <dl> <span data-ttu-id="446ea-124"><dt>**\_указатель E**</dt></span><span class="sxs-lookup"><span data-stu-id="446ea-124"><dt>**E\_POINTER**</dt></span></span> </dl> | <span data-ttu-id="446ea-125">Параметр *Pval* не является допустимым указателем.</span><span class="sxs-lookup"><span data-stu-id="446ea-125">The *pVal* parameter is not a valid pointer.</span></span><br/>       |



 

## <a name="remarks"></a><span data-ttu-id="446ea-126">Remarks</span><span class="sxs-lookup"><span data-stu-id="446ea-126">Remarks</span></span>

<span data-ttu-id="446ea-127">TAPI вызывает метод **AddRef** в интерфейсе [**иттиме**](ittime.md) , возвращенном методом **иенумтиме:: Next**.</span><span class="sxs-lookup"><span data-stu-id="446ea-127">TAPI calls the **AddRef** method on the [**ITTime**](ittime.md) interface returned by **IEnumTime::Next**.</span></span> <span data-ttu-id="446ea-128">Приложение должно вызвать **выпуск** в интерфейсе **иттиме** , чтобы освободить ресурсы, связанные с ним.</span><span class="sxs-lookup"><span data-stu-id="446ea-128">The application must call **Release** on the **ITTime** interface to free resources associated with it.</span></span>

## <a name="requirements"></a><span data-ttu-id="446ea-129">Требования</span><span class="sxs-lookup"><span data-stu-id="446ea-129">Requirements</span></span>



| <span data-ttu-id="446ea-130">Требование</span><span class="sxs-lookup"><span data-stu-id="446ea-130">Requirement</span></span> | <span data-ttu-id="446ea-131">Значение</span><span class="sxs-lookup"><span data-stu-id="446ea-131">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="446ea-132">Версия TAPI</span><span class="sxs-lookup"><span data-stu-id="446ea-132">TAPI version</span></span><br/> | <span data-ttu-id="446ea-133">Требуется TAPI 3,0 или более поздней версии</span><span class="sxs-lookup"><span data-stu-id="446ea-133">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="446ea-134">Header</span><span class="sxs-lookup"><span data-stu-id="446ea-134">Header</span></span><br/>       | <dl> <span data-ttu-id="446ea-135"><dt>Сдпблб. h</dt></span><span class="sxs-lookup"><span data-stu-id="446ea-135"><dt>Sdpblb.h</dt></span></span> </dl>   |
| <span data-ttu-id="446ea-136">Библиотека</span><span class="sxs-lookup"><span data-stu-id="446ea-136">Library</span></span><br/>      | <dl> <span data-ttu-id="446ea-137"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="446ea-137"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="446ea-138">DLL</span><span class="sxs-lookup"><span data-stu-id="446ea-138">DLL</span></span><br/>          | <dl> <span data-ttu-id="446ea-139"><dt>Sdpblb.dll</dt></span><span class="sxs-lookup"><span data-stu-id="446ea-139"><dt>Sdpblb.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="446ea-140">См. также</span><span class="sxs-lookup"><span data-stu-id="446ea-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="446ea-141">**иенумтиме**</span><span class="sxs-lookup"><span data-stu-id="446ea-141">**IEnumTime**</span></span>](ienumtime.md)
</dt> </dl>

 

 




