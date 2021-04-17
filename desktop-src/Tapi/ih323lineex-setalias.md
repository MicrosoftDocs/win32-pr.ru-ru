---
description: Метод Сеталиас настраивает псевдоним H. 323 по умолчанию для адреса. Этот псевдоним будет использоваться в обмене настройками для настройки вызова H. 323, чтобы другая сторона знала имя этой стороны.
ms.assetid: 09608214-7346-4ee8-bbfd-0877d3ad0766
title: 'Метод IH323LineEx:: Сеталиас (H323priv. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7341d177297cf95f46d07e503244f06b2c4dea71
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105685285"
---
# <a name="ih323lineexsetalias-method"></a><span data-ttu-id="640c4-104">Метод IH323LineEx:: Сеталиас</span><span class="sxs-lookup"><span data-stu-id="640c4-104">IH323LineEx::SetAlias method</span></span>

<span data-ttu-id="640c4-105">\[**Сеталиас** недоступен для использования в Windows Vista, windows Server 2008 и последующих версиях операционной системы.</span><span class="sxs-lookup"><span data-stu-id="640c4-105">\[**SetAlias** is not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="640c4-106">API клиента RTC предоставляет аналогичные функциональные возможности.\]</span><span class="sxs-lookup"><span data-stu-id="640c4-106">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="640c4-107">Метод **сеталиас** настраивает псевдоним H. 323 по умолчанию для адреса.</span><span class="sxs-lookup"><span data-stu-id="640c4-107">The **SetAlias** method configures a default H.323 alias for the address.</span></span> <span data-ttu-id="640c4-108">Этот псевдоним будет использоваться в обмене настройками для настройки вызова H. 323, чтобы другая сторона знала имя этой стороны.</span><span class="sxs-lookup"><span data-stu-id="640c4-108">This alias will be used in the H.323 call setup exchange so that the other party knows the name of this party.</span></span>

<span data-ttu-id="640c4-109">При повторном вызове этого метода предыдущий псевдоним будет перезаписан.</span><span class="sxs-lookup"><span data-stu-id="640c4-109">Calling this method a second time will overwrite the previous alias.</span></span>

<span data-ttu-id="640c4-110">Псевдоним, заданный для этого интерфейса, будет использоваться только в том случае, если для TSP не существует другого способа найти правильный псевдоним.</span><span class="sxs-lookup"><span data-stu-id="640c4-110">The alias set on this interface will be used only when there is no other way for the TSP to find a proper alias.</span></span> <span data-ttu-id="640c4-111">В будущем, когда в TSP добавляется поддержка привратника, псевдоним, зарегистрированный в привратнике или назначенный привратником, будет переопределять все, что задается этим методом.</span><span class="sxs-lookup"><span data-stu-id="640c4-111">In the future, when gatekeeper support is added into the TSP, the alias registered to the gatekeeper or assigned by the gatekeeper will override whatever is set through this method.</span></span>

## <a name="syntax"></a><span data-ttu-id="640c4-112">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="640c4-112">Syntax</span></span>


```C++
HRESULT SetAlias(
  [in] WCHAR *strAlias,
  [in] DWORD dwLength
);
```



## <a name="parameters"></a><span data-ttu-id="640c4-113">Параметры</span><span class="sxs-lookup"><span data-stu-id="640c4-113">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="640c4-114">*стралиас* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="640c4-114">*strAlias* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="640c4-115">Псевдоним, используемый в Юникоде.</span><span class="sxs-lookup"><span data-stu-id="640c4-115">The alias to be used, in Unicode.</span></span> <span data-ttu-id="640c4-116">Завершение **null** не требуется.</span><span class="sxs-lookup"><span data-stu-id="640c4-116">**Null** termination is not required.</span></span>

</dd> <dt>

<span data-ttu-id="640c4-117">*двленгс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="640c4-117">*dwLength* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="640c4-118">Длина имени псевдонима в количестве символов, включая знак завершения **null** .</span><span class="sxs-lookup"><span data-stu-id="640c4-118">The length of the alias name in number of characters, including the **null** terminator.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="640c4-119">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="640c4-119">Return value</span></span>

<span data-ttu-id="640c4-120">Этот метод может возвращать одно из этих значений.</span><span class="sxs-lookup"><span data-stu-id="640c4-120">This method can return one of these values.</span></span>



| <span data-ttu-id="640c4-121">Код возврата</span><span class="sxs-lookup"><span data-stu-id="640c4-121">Return code</span></span>                                                                               | <span data-ttu-id="640c4-122">Описание</span><span class="sxs-lookup"><span data-stu-id="640c4-122">Description</span></span>                                                                                                                      |
|-------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="640c4-123"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="640c4-123"><dt>**S\_OK**</dt></span></span> </dl>      | <span data-ttu-id="640c4-124">Метод успешно выполнен.</span><span class="sxs-lookup"><span data-stu-id="640c4-124">Method succeeded.</span></span><br/>                                                                                                     |
| <dl> <span data-ttu-id="640c4-125"><dt>**\_указатель E**</dt></span><span class="sxs-lookup"><span data-stu-id="640c4-125"><dt>**E\_POINTER**</dt></span></span> </dl> | <span data-ttu-id="640c4-126">Число символов, указанных в *двленгс* , превышает фактическое число символов в параметре *стралиас* .</span><span class="sxs-lookup"><span data-stu-id="640c4-126">The number of characters indicated in *dwLength* exceeds the actual number of characters in the *strAlias* parameter.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="640c4-127">Требования</span><span class="sxs-lookup"><span data-stu-id="640c4-127">Requirements</span></span>



| <span data-ttu-id="640c4-128">Требование</span><span class="sxs-lookup"><span data-stu-id="640c4-128">Requirement</span></span> | <span data-ttu-id="640c4-129">Значение</span><span class="sxs-lookup"><span data-stu-id="640c4-129">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="640c4-130">Версия TAPI</span><span class="sxs-lookup"><span data-stu-id="640c4-130">TAPI version</span></span><br/> | <span data-ttu-id="640c4-131">Требуется TAPI 3,0 или более поздней версии</span><span class="sxs-lookup"><span data-stu-id="640c4-131">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="640c4-132">Header</span><span class="sxs-lookup"><span data-stu-id="640c4-132">Header</span></span><br/>       | <dl> <span data-ttu-id="640c4-133"><dt>H323priv. h</dt></span><span class="sxs-lookup"><span data-stu-id="640c4-133"><dt>H323priv.h</dt></span></span> </dl> |
| <span data-ttu-id="640c4-134">Библиотека</span><span class="sxs-lookup"><span data-stu-id="640c4-134">Library</span></span><br/>      | <dl> <span data-ttu-id="640c4-135"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="640c4-135"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="640c4-136">DLL</span><span class="sxs-lookup"><span data-stu-id="640c4-136">DLL</span></span><br/>          | <dl> <span data-ttu-id="640c4-137"><dt>Tapi3.dll</dt></span><span class="sxs-lookup"><span data-stu-id="640c4-137"><dt>Tapi3.dll</dt></span></span> </dl>  |



 

 




