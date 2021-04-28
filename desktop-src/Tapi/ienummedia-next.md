---
description: 'Метод Иенуммедиа:: Next — Следующий метод получает указанное число следующих элементов в последовательности перечисления.'
ms.assetid: 39c6d082-415f-4375-8cad-6d4c734d277f
title: 'Метод Иенуммедиа:: Next (Сдпблб. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 711e9c844c46aab6ca90988d4e456e926716b201
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108113442"
---
# <a name="ienummedianext-method"></a><span data-ttu-id="eb0cd-103">Метод Иенуммедиа:: Next</span><span class="sxs-lookup"><span data-stu-id="eb0cd-103">IEnumMedia::Next method</span></span>

<span data-ttu-id="eb0cd-104">\[ В Windows Vista, Windows Server 2008 и последующих версиях операционной системы нельзя использовать встречные средства и элементы управления Конференц-телефонией и интерфейсы.</span><span class="sxs-lookup"><span data-stu-id="eb0cd-104">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="eb0cd-105">API клиента RTC предоставляет аналогичные функциональные возможности.\]</span><span class="sxs-lookup"><span data-stu-id="eb0cd-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="eb0cd-106">**Следующий** метод получает указанное число следующих элементов в последовательности перечисления.</span><span class="sxs-lookup"><span data-stu-id="eb0cd-106">The **Next** method gets the next specified number of elements in the enumeration sequence.</span></span>

## <a name="syntax"></a><span data-ttu-id="eb0cd-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="eb0cd-107">Syntax</span></span>


```C++
HRESULT Next(
  [in]  ULONG   celt,
  [out] ITMedia **pVal,
  [out] ULONG   *pceltFetched
);
```



## <a name="parameters"></a><span data-ttu-id="eb0cd-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="eb0cd-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="eb0cd-109">*celt* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="eb0cd-109">*celt* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="eb0cd-110">Число запрошенных элементов.</span><span class="sxs-lookup"><span data-stu-id="eb0cd-110">Number of elements requested.</span></span>

</dd> <dt>

<span data-ttu-id="eb0cd-111">*Pval* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="eb0cd-111">*pVal* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="eb0cd-112">Указатель на интерфейс [**итмедиа**](itmedia.md) .</span><span class="sxs-lookup"><span data-stu-id="eb0cd-112">Pointer to the [**ITMedia**](itmedia.md) interface.</span></span>

</dd> <dt>

<span data-ttu-id="eb0cd-113">*пцелтфетчед* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="eb0cd-113">*pceltFetched* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="eb0cd-114">Указатель на число фактически предоставляемых элементов.</span><span class="sxs-lookup"><span data-stu-id="eb0cd-114">Pointer to the number of elements actually supplied.</span></span> <span data-ttu-id="eb0cd-115">Может иметь **значение NULL** , если значение *celt* равно единице.</span><span class="sxs-lookup"><span data-stu-id="eb0cd-115">May be **NULL** if *celt* is one.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="eb0cd-116">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="eb0cd-116">Return value</span></span>

<span data-ttu-id="eb0cd-117">Этот метод может возвращать одно из этих значений.</span><span class="sxs-lookup"><span data-stu-id="eb0cd-117">This method can return one of these values.</span></span>



| <span data-ttu-id="eb0cd-118">Значение</span><span class="sxs-lookup"><span data-stu-id="eb0cd-118">Value</span></span>                                                                                     | <span data-ttu-id="eb0cd-119">Значение</span><span class="sxs-lookup"><span data-stu-id="eb0cd-119">Meaning</span></span>                                                       |
|-------------------------------------------------------------------------------------------|---------------------------------------------------------------|
| <dl> <span data-ttu-id="eb0cd-120"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="eb0cd-120"><dt>**S\_OK**</dt></span></span> </dl>      | <span data-ttu-id="eb0cd-121">Метод возвратил *celt* число элементов.</span><span class="sxs-lookup"><span data-stu-id="eb0cd-121">Method returned *celt* number of elements.</span></span><br/>         |
| <dl> <span data-ttu-id="eb0cd-122"><dt>**S \_ false**</dt></span><span class="sxs-lookup"><span data-stu-id="eb0cd-122"><dt>**S\_FALSE**</dt></span></span> </dl>   | <span data-ttu-id="eb0cd-123">Количество оставшихся элементов меньше значения *celt*.</span><span class="sxs-lookup"><span data-stu-id="eb0cd-123">Number of elements remaining was less than *celt*.</span></span><br/> |
| <dl> <span data-ttu-id="eb0cd-124"><dt>**\_указатель E**</dt></span><span class="sxs-lookup"><span data-stu-id="eb0cd-124"><dt>**E\_POINTER**</dt></span></span> </dl> | <span data-ttu-id="eb0cd-125">Параметр *Pval* не является допустимым указателем.</span><span class="sxs-lookup"><span data-stu-id="eb0cd-125">The *pVal* parameter is not a valid pointer.</span></span><br/>       |



 

## <a name="remarks"></a><span data-ttu-id="eb0cd-126">Remarks</span><span class="sxs-lookup"><span data-stu-id="eb0cd-126">Remarks</span></span>

<span data-ttu-id="eb0cd-127">TAPI вызывает метод **AddRef** в интерфейсе [**итмедиа**](itmedia.md) , возвращенном методом **иенуммедиа:: Next**.</span><span class="sxs-lookup"><span data-stu-id="eb0cd-127">TAPI calls the **AddRef** method on the [**ITMedia**](itmedia.md) interface returned by **IEnumMedia::Next**.</span></span> <span data-ttu-id="eb0cd-128">Приложение должно вызвать **выпуск** в интерфейсе **итмедиа** , чтобы освободить ресурсы, связанные с ним.</span><span class="sxs-lookup"><span data-stu-id="eb0cd-128">The application must call **Release** on the **ITMedia** interface to free resources associated with it.</span></span>

## <a name="requirements"></a><span data-ttu-id="eb0cd-129">Требования</span><span class="sxs-lookup"><span data-stu-id="eb0cd-129">Requirements</span></span>



| <span data-ttu-id="eb0cd-130">Требование</span><span class="sxs-lookup"><span data-stu-id="eb0cd-130">Requirement</span></span> | <span data-ttu-id="eb0cd-131">Значение</span><span class="sxs-lookup"><span data-stu-id="eb0cd-131">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="eb0cd-132">Версия TAPI</span><span class="sxs-lookup"><span data-stu-id="eb0cd-132">TAPI version</span></span><br/> | <span data-ttu-id="eb0cd-133">Требуется TAPI 3,0 или более поздней версии</span><span class="sxs-lookup"><span data-stu-id="eb0cd-133">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="eb0cd-134">Header</span><span class="sxs-lookup"><span data-stu-id="eb0cd-134">Header</span></span><br/>       | <dl> <span data-ttu-id="eb0cd-135"><dt>Сдпблб. h</dt></span><span class="sxs-lookup"><span data-stu-id="eb0cd-135"><dt>Sdpblb.h</dt></span></span> </dl>   |
| <span data-ttu-id="eb0cd-136">Библиотека</span><span class="sxs-lookup"><span data-stu-id="eb0cd-136">Library</span></span><br/>      | <dl> <span data-ttu-id="eb0cd-137"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="eb0cd-137"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="eb0cd-138">DLL</span><span class="sxs-lookup"><span data-stu-id="eb0cd-138">DLL</span></span><br/>          | <dl> <span data-ttu-id="eb0cd-139"><dt>Sdpblb.dll</dt></span><span class="sxs-lookup"><span data-stu-id="eb0cd-139"><dt>Sdpblb.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="eb0cd-140">См. также</span><span class="sxs-lookup"><span data-stu-id="eb0cd-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="eb0cd-141">**иенуммедиа**</span><span class="sxs-lookup"><span data-stu-id="eb0cd-141">**IEnumMedia**</span></span>](ienummedia.md)
</dt> </dl>

 

 




