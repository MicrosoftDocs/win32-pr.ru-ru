---
description: Метод Жеткуррентформат извлекает формат носителя текущего потока.
ms.assetid: 02d1b3b5-3639-4864-9b72-623bf94acf69
title: 'Метод Итформатконтрол:: Жеткуррентформат (Ипмсп. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b1b711b539ea9a92af6bd345c5a1f48b212b640b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105688959"
---
# <a name="itformatcontrolgetcurrentformat-method"></a><span data-ttu-id="96e36-103">Метод Итформатконтрол:: Жеткуррентформат</span><span class="sxs-lookup"><span data-stu-id="96e36-103">ITFormatControl::GetCurrentFormat method</span></span>

<span data-ttu-id="96e36-104">\[ Этот метод недоступен для использования в Windows Vista, Windows Server 2008 и последующих версиях операционной системы.</span><span class="sxs-lookup"><span data-stu-id="96e36-104">\[ This method is not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="96e36-105">API клиента RTC предоставляет аналогичные функциональные возможности.\]</span><span class="sxs-lookup"><span data-stu-id="96e36-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="96e36-106">Метод **жеткуррентформат** извлекает формат носителя текущего потока.</span><span class="sxs-lookup"><span data-stu-id="96e36-106">The **GetCurrentFormat** method retrieves the media format of the current stream.</span></span>

## <a name="syntax"></a><span data-ttu-id="96e36-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="96e36-107">Syntax</span></span>


```C++
HRESULT GetCurrentFormat(
  [out] AM_MEDIA_TYPE **ppMediaType
);
```



## <a name="parameters"></a><span data-ttu-id="96e36-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="96e36-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="96e36-109">*ппмедиатипе* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="96e36-109">*ppMediaType* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="96e36-110">Указатель на дескриптор **\_ \_ типа носителя AM** в формате терминала.</span><span class="sxs-lookup"><span data-stu-id="96e36-110">Pointer to an **AM\_MEDIA\_TYPE** descriptor of the terminal format.</span></span> <span data-ttu-id="96e36-111">Дополнительные сведения о **\_ \_ типе носителя** см. в документации DirectX.</span><span class="sxs-lookup"><span data-stu-id="96e36-111">For more information on **AM\_MEDIA\_TYPE**, see the DirectX documentation.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="96e36-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="96e36-112">Return value</span></span>

<span data-ttu-id="96e36-113">Этот метод может возвращать одно из этих значений.</span><span class="sxs-lookup"><span data-stu-id="96e36-113">This method can return one of these values.</span></span>



| <span data-ttu-id="96e36-114">Код возврата</span><span class="sxs-lookup"><span data-stu-id="96e36-114">Return code</span></span>                                                                                   | <span data-ttu-id="96e36-115">Описание</span><span class="sxs-lookup"><span data-stu-id="96e36-115">Description</span></span>                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="96e36-116"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="96e36-116"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="96e36-117">Метод успешно выполнен.</span><span class="sxs-lookup"><span data-stu-id="96e36-117">Method succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="96e36-118"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="96e36-118"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="96e36-119">Недостаточно памяти для выполнения операции.</span><span class="sxs-lookup"><span data-stu-id="96e36-119">Insufficient memory exists to perform the operation.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="96e36-120">Требования</span><span class="sxs-lookup"><span data-stu-id="96e36-120">Requirements</span></span>



| <span data-ttu-id="96e36-121">Требование</span><span class="sxs-lookup"><span data-stu-id="96e36-121">Requirement</span></span> | <span data-ttu-id="96e36-122">Значение</span><span class="sxs-lookup"><span data-stu-id="96e36-122">Value</span></span> |
|-------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="96e36-123">Версия TAPI</span><span class="sxs-lookup"><span data-stu-id="96e36-123">TAPI version</span></span><br/> | <span data-ttu-id="96e36-124">Требуется TAPI 3,1</span><span class="sxs-lookup"><span data-stu-id="96e36-124">Requires TAPI 3.1</span></span><br/>                                                         |
| <span data-ttu-id="96e36-125">Header</span><span class="sxs-lookup"><span data-stu-id="96e36-125">Header</span></span><br/>       | <dl> <span data-ttu-id="96e36-126"><dt>Ипмсп. h</dt></span><span class="sxs-lookup"><span data-stu-id="96e36-126"><dt>Ipmsp.h</dt></span></span> </dl>   |
| <span data-ttu-id="96e36-127">Библиотека</span><span class="sxs-lookup"><span data-stu-id="96e36-127">Library</span></span><br/>      | <dl> <span data-ttu-id="96e36-128"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="96e36-128"><dt>Uuid.lib</dt></span></span> </dl>  |
| <span data-ttu-id="96e36-129">DLL</span><span class="sxs-lookup"><span data-stu-id="96e36-129">DLL</span></span><br/>          | <dl> <span data-ttu-id="96e36-130"><dt>Tapi3.dll</dt></span><span class="sxs-lookup"><span data-stu-id="96e36-130"><dt>Tapi3.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="96e36-131">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="96e36-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="96e36-132">**итформатконтрол**</span><span class="sxs-lookup"><span data-stu-id="96e36-132">**ITFormatControl**</span></span>](itformatcontrol.md)
</dt> </dl>

 

 




