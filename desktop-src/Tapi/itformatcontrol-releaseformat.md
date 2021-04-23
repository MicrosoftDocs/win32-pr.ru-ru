---
description: Метод Релеасеформат освобождает структуру, связанную с форматом.
ms.assetid: 67181773-5a04-4e20-9814-b004d3b549f5
title: 'Метод Итформатконтрол:: Релеасеформат (Ипмсп. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c91b3eb2a84149054d7ff364cf05290946bca975
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105688956"
---
# <a name="itformatcontrolreleaseformat-method"></a><span data-ttu-id="15cdc-103">Метод Итформатконтрол:: Релеасеформат</span><span class="sxs-lookup"><span data-stu-id="15cdc-103">ITFormatControl::ReleaseFormat method</span></span>

<span data-ttu-id="15cdc-104">\[ Этот метод недоступен для использования в Windows Vista, Windows Server 2008 и последующих версиях операционной системы.</span><span class="sxs-lookup"><span data-stu-id="15cdc-104">\[ This method is not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="15cdc-105">API клиента RTC предоставляет аналогичные функциональные возможности.\]</span><span class="sxs-lookup"><span data-stu-id="15cdc-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="15cdc-106">Метод **релеасеформат** освобождает структуру, связанную с форматом.</span><span class="sxs-lookup"><span data-stu-id="15cdc-106">The **ReleaseFormat** method releases the structure associated with the format.</span></span>

## <a name="syntax"></a><span data-ttu-id="15cdc-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="15cdc-107">Syntax</span></span>


```C++
HRESULT ReleaseFormat(
  [in] AM_MEDIA_TYPE *pMediaType
);
```



## <a name="parameters"></a><span data-ttu-id="15cdc-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="15cdc-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="15cdc-109">*пмедиатипе* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="15cdc-109">*pMediaType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="15cdc-110">Указатель на дескриптор **\_ \_ типа носителя AM** в формате терминала.</span><span class="sxs-lookup"><span data-stu-id="15cdc-110">Pointer to an **AM\_MEDIA\_TYPE** descriptor of the terminal format.</span></span> <span data-ttu-id="15cdc-111">Дополнительные сведения о **\_ \_ типе носителя** см. в документации DirectX.</span><span class="sxs-lookup"><span data-stu-id="15cdc-111">For more information on **AM\_MEDIA\_TYPE**, see the DirectX documentation.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="15cdc-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="15cdc-112">Return value</span></span>

<span data-ttu-id="15cdc-113">Этот метод может возвращать одно из этих значений.</span><span class="sxs-lookup"><span data-stu-id="15cdc-113">This method can return one of these values.</span></span>



| <span data-ttu-id="15cdc-114">Код возврата</span><span class="sxs-lookup"><span data-stu-id="15cdc-114">Return code</span></span>                                                                                   | <span data-ttu-id="15cdc-115">Описание</span><span class="sxs-lookup"><span data-stu-id="15cdc-115">Description</span></span>                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="15cdc-116"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="15cdc-116"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="15cdc-117">Метод успешно выполнен.</span><span class="sxs-lookup"><span data-stu-id="15cdc-117">Method succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="15cdc-118"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="15cdc-118"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="15cdc-119">Недостаточно памяти для выполнения операции.</span><span class="sxs-lookup"><span data-stu-id="15cdc-119">Insufficient memory exists to perform the operation.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="15cdc-120">Требования</span><span class="sxs-lookup"><span data-stu-id="15cdc-120">Requirements</span></span>



| <span data-ttu-id="15cdc-121">Требование</span><span class="sxs-lookup"><span data-stu-id="15cdc-121">Requirement</span></span> | <span data-ttu-id="15cdc-122">Значение</span><span class="sxs-lookup"><span data-stu-id="15cdc-122">Value</span></span> |
|-------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="15cdc-123">Версия TAPI</span><span class="sxs-lookup"><span data-stu-id="15cdc-123">TAPI version</span></span><br/> | <span data-ttu-id="15cdc-124">Требуется TAPI 3,1</span><span class="sxs-lookup"><span data-stu-id="15cdc-124">Requires TAPI 3.1</span></span><br/>                                                         |
| <span data-ttu-id="15cdc-125">Header</span><span class="sxs-lookup"><span data-stu-id="15cdc-125">Header</span></span><br/>       | <dl> <span data-ttu-id="15cdc-126"><dt>Ипмсп. h</dt></span><span class="sxs-lookup"><span data-stu-id="15cdc-126"><dt>Ipmsp.h</dt></span></span> </dl>   |
| <span data-ttu-id="15cdc-127">Библиотека</span><span class="sxs-lookup"><span data-stu-id="15cdc-127">Library</span></span><br/>      | <dl> <span data-ttu-id="15cdc-128"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="15cdc-128"><dt>Uuid.lib</dt></span></span> </dl>  |
| <span data-ttu-id="15cdc-129">DLL</span><span class="sxs-lookup"><span data-stu-id="15cdc-129">DLL</span></span><br/>          | <dl> <span data-ttu-id="15cdc-130"><dt>Tapi3.dll</dt></span><span class="sxs-lookup"><span data-stu-id="15cdc-130"><dt>Tapi3.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="15cdc-131">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="15cdc-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="15cdc-132">**итформатконтрол**</span><span class="sxs-lookup"><span data-stu-id="15cdc-132">**ITFormatControl**</span></span>](itformatcontrol.md)
</dt> </dl>

 

 




