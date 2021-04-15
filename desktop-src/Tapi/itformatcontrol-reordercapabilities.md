---
description: Метод Реордеркапабилитиес задает новый порядок для возможностей форматирования.
ms.assetid: 05785d64-a22f-411f-9fae-318828d30c52
title: 'Метод Итформатконтрол:: Реордеркапабилитиес (Ипмсп. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4d6f7800e4a04dbd70c5b270778cd7eb0ff540b4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105675778"
---
# <a name="itformatcontrolreordercapabilities-method"></a><span data-ttu-id="5a500-103">Метод Итформатконтрол:: Реордеркапабилитиес</span><span class="sxs-lookup"><span data-stu-id="5a500-103">ITFormatControl::ReOrderCapabilities method</span></span>

<span data-ttu-id="5a500-104">\[ Этот метод недоступен для использования в Windows Vista, Windows Server 2008 и последующих версиях операционной системы.</span><span class="sxs-lookup"><span data-stu-id="5a500-104">\[ This method is not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="5a500-105">API клиента RTC предоставляет аналогичные функциональные возможности.\]</span><span class="sxs-lookup"><span data-stu-id="5a500-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="5a500-106">Метод **реордеркапабилитиес** задает новый порядок для возможностей форматирования.</span><span class="sxs-lookup"><span data-stu-id="5a500-106">The **ReOrderCapabilities** method sets a new order for format capabilities.</span></span>

## <a name="syntax"></a><span data-ttu-id="5a500-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="5a500-107">Syntax</span></span>


```C++
HRESULT ReOrderCapabilities(
  [in] DWORD *pdwIndices,
  [in] BOOL  *pfEnabled,
  [in] BOOL  *pfPublicize,
  [in] DWORD dwNumIndices
);
```



## <a name="parameters"></a><span data-ttu-id="5a500-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="5a500-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5a500-109">*пдвиндицес* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="5a500-109">*pdwIndices* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5a500-110">Индекс формата, для которого выполняется изменение порядка.</span><span class="sxs-lookup"><span data-stu-id="5a500-110">Index of the format being reordered.</span></span>

</dd> <dt>

<span data-ttu-id="5a500-111">*пфенаблед* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="5a500-111">*pfEnabled* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5a500-112">Указывает, следует ли включать или отключать формат.</span><span class="sxs-lookup"><span data-stu-id="5a500-112">Indicates whether the format should be enabled or disabled.</span></span>

</dd> <dt>

<span data-ttu-id="5a500-113">*пфпублиЦизе* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="5a500-113">*pfPublicize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5a500-114">Указывает, следует ли сделать формат доступным.</span><span class="sxs-lookup"><span data-stu-id="5a500-114">Indicates whether the format should be made available.</span></span>

</dd> <dt>

<span data-ttu-id="5a500-115">*двнуминдицес* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="5a500-115">*dwNumIndices* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5a500-116">Новый номер индекса для формата.</span><span class="sxs-lookup"><span data-stu-id="5a500-116">New index number for the format.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5a500-117">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="5a500-117">Return value</span></span>

<span data-ttu-id="5a500-118">Этот метод может возвращать одно из этих значений.</span><span class="sxs-lookup"><span data-stu-id="5a500-118">This method can return one of these values.</span></span>



| <span data-ttu-id="5a500-119">Код возврата</span><span class="sxs-lookup"><span data-stu-id="5a500-119">Return code</span></span>                                                                                   | <span data-ttu-id="5a500-120">Описание</span><span class="sxs-lookup"><span data-stu-id="5a500-120">Description</span></span>                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="5a500-121"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="5a500-121"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="5a500-122">Метод успешно выполнен.</span><span class="sxs-lookup"><span data-stu-id="5a500-122">Method succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="5a500-123"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="5a500-123"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="5a500-124">Недостаточно памяти для выполнения операции.</span><span class="sxs-lookup"><span data-stu-id="5a500-124">Insufficient memory exists to perform the operation.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="5a500-125">Комментарии</span><span class="sxs-lookup"><span data-stu-id="5a500-125">Remarks</span></span>

<span data-ttu-id="5a500-126">Перед использованием этого метода необходимо вызвать метод [**жетнумберофкапабилитиес**](itformatcontrol-getnumberofcapabilities.md) .</span><span class="sxs-lookup"><span data-stu-id="5a500-126">The [**GetNumberOfCapabilities**](itformatcontrol-getnumberofcapabilities.md) method must be called prior to using this method.</span></span>

## <a name="requirements"></a><span data-ttu-id="5a500-127">Требования</span><span class="sxs-lookup"><span data-stu-id="5a500-127">Requirements</span></span>



| <span data-ttu-id="5a500-128">Требование</span><span class="sxs-lookup"><span data-stu-id="5a500-128">Requirement</span></span> | <span data-ttu-id="5a500-129">Значение</span><span class="sxs-lookup"><span data-stu-id="5a500-129">Value</span></span> |
|-------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="5a500-130">Версия TAPI</span><span class="sxs-lookup"><span data-stu-id="5a500-130">TAPI version</span></span><br/> | <span data-ttu-id="5a500-131">Требуется TAPI 3,1</span><span class="sxs-lookup"><span data-stu-id="5a500-131">Requires TAPI 3.1</span></span><br/>                                                         |
| <span data-ttu-id="5a500-132">Header</span><span class="sxs-lookup"><span data-stu-id="5a500-132">Header</span></span><br/>       | <dl> <span data-ttu-id="5a500-133"><dt>Ипмсп. h</dt></span><span class="sxs-lookup"><span data-stu-id="5a500-133"><dt>Ipmsp.h</dt></span></span> </dl>   |
| <span data-ttu-id="5a500-134">Библиотека</span><span class="sxs-lookup"><span data-stu-id="5a500-134">Library</span></span><br/>      | <dl> <span data-ttu-id="5a500-135"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="5a500-135"><dt>Uuid.lib</dt></span></span> </dl>  |
| <span data-ttu-id="5a500-136">DLL</span><span class="sxs-lookup"><span data-stu-id="5a500-136">DLL</span></span><br/>          | <dl> <span data-ttu-id="5a500-137"><dt>Tapi3.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5a500-137"><dt>Tapi3.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5a500-138">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="5a500-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5a500-139">**итформатконтрол**</span><span class="sxs-lookup"><span data-stu-id="5a500-139">**ITFormatControl**</span></span>](itformatcontrol.md)
</dt> <dt>

[<span data-ttu-id="5a500-140">**жетнумберофкапабилитиес**</span><span class="sxs-lookup"><span data-stu-id="5a500-140">**GetNumberOfCapabilities**</span></span>](itformatcontrol-getnumberofcapabilities.md)
</dt> </dl>

 

 




