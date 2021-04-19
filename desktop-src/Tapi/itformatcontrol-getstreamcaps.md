---
description: Метод Жетстреамкапс извлекает возможности, связанные с данным индексом формата.
ms.assetid: 4c375369-51d9-44ac-a8f0-c2a96fc10805
title: 'Метод Итформатконтрол:: Жетстреамкапс (Ипмсп. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8a1ccaf825912e53eafb5112f14ed369f999959a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105688957"
---
# <a name="itformatcontrolgetstreamcaps-method"></a><span data-ttu-id="e5731-103">Метод Итформатконтрол:: Жетстреамкапс</span><span class="sxs-lookup"><span data-stu-id="e5731-103">ITFormatControl::GetStreamCaps method</span></span>

<span data-ttu-id="e5731-104">\[ Этот метод недоступен для использования в Windows Vista, Windows Server 2008 и последующих версиях операционной системы.</span><span class="sxs-lookup"><span data-stu-id="e5731-104">\[ This method is not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="e5731-105">API клиента RTC предоставляет аналогичные функциональные возможности.\]</span><span class="sxs-lookup"><span data-stu-id="e5731-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="e5731-106">Метод **жетстреамкапс** извлекает возможности, связанные с данным индексом формата.</span><span class="sxs-lookup"><span data-stu-id="e5731-106">The **GetStreamCaps** method retrieves the capabilities associated with a given format index.</span></span>

## <a name="syntax"></a><span data-ttu-id="e5731-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="e5731-107">Syntax</span></span>


```C++
HRESULT GetStreamCaps(
  [in]  DWORD                   dwIndex,
  [out] AM_MEDIA_TYPE           **ppMediaType,
  [out] TAPI_STREAM_CONFIG_CAPS *pStreamConfigCaps,
  [out] BOOL                    *pfEnabled
);
```



## <a name="parameters"></a><span data-ttu-id="e5731-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="e5731-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e5731-109">*двиндекс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="e5731-109">*dwIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e5731-110">Индекс проверяемого формата.</span><span class="sxs-lookup"><span data-stu-id="e5731-110">Index of the format being probed.</span></span>

</dd> <dt>

<span data-ttu-id="e5731-111">*ппмедиатипе* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="e5731-111">*ppMediaType* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e5731-112">Указатель на дескриптор **\_ \_ типа носителя AM** в формате терминала.</span><span class="sxs-lookup"><span data-stu-id="e5731-112">Pointer to an **AM\_MEDIA\_TYPE** descriptor of the terminal format.</span></span> <span data-ttu-id="e5731-113">Дополнительные сведения о **\_ \_ типе носителя** см. в документации DirectX.</span><span class="sxs-lookup"><span data-stu-id="e5731-113">For more information on **AM\_MEDIA\_TYPE**, see the DirectX documentation.</span></span>

</dd> <dt>

<span data-ttu-id="e5731-114">*пстреамконфигкапс* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="e5731-114">*pStreamConfigCaps* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e5731-115">Структура [**\_ \_ \_ Caps конфигурации потока TAPI**](tapi-stream-config-caps.md) , которая предоставляет подробные сведения о возможностях потока.</span><span class="sxs-lookup"><span data-stu-id="e5731-115">A [**TAPI\_STREAM\_CONFIG\_CAPS**](tapi-stream-config-caps.md) structure that gives detailed information concerning stream capabilities.</span></span>

</dd> <dt>

<span data-ttu-id="e5731-116">*пфенаблед* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="e5731-116">*pfEnabled* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e5731-117">Указывает, включен ли формат, связанный с текущим индексом.</span><span class="sxs-lookup"><span data-stu-id="e5731-117">Indicates whether the format associated with the current index is enabled.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e5731-118">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="e5731-118">Return value</span></span>

<span data-ttu-id="e5731-119">Этот метод может возвращать одно из этих значений.</span><span class="sxs-lookup"><span data-stu-id="e5731-119">This method can return one of these values.</span></span>



| <span data-ttu-id="e5731-120">Код возврата</span><span class="sxs-lookup"><span data-stu-id="e5731-120">Return code</span></span>                                                                                   | <span data-ttu-id="e5731-121">Описание</span><span class="sxs-lookup"><span data-stu-id="e5731-121">Description</span></span>                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="e5731-122"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="e5731-122"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="e5731-123">Метод успешно выполнен.</span><span class="sxs-lookup"><span data-stu-id="e5731-123">Method succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="e5731-124"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="e5731-124"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="e5731-125">Недостаточно памяти для выполнения операции.</span><span class="sxs-lookup"><span data-stu-id="e5731-125">Insufficient memory exists to perform the operation.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="e5731-126">Требования</span><span class="sxs-lookup"><span data-stu-id="e5731-126">Requirements</span></span>



| <span data-ttu-id="e5731-127">Требование</span><span class="sxs-lookup"><span data-stu-id="e5731-127">Requirement</span></span> | <span data-ttu-id="e5731-128">Значение</span><span class="sxs-lookup"><span data-stu-id="e5731-128">Value</span></span> |
|-------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="e5731-129">Версия TAPI</span><span class="sxs-lookup"><span data-stu-id="e5731-129">TAPI version</span></span><br/> | <span data-ttu-id="e5731-130">Требуется TAPI 3,1</span><span class="sxs-lookup"><span data-stu-id="e5731-130">Requires TAPI 3.1</span></span><br/>                                                         |
| <span data-ttu-id="e5731-131">Header</span><span class="sxs-lookup"><span data-stu-id="e5731-131">Header</span></span><br/>       | <dl> <span data-ttu-id="e5731-132"><dt>Ипмсп. h</dt></span><span class="sxs-lookup"><span data-stu-id="e5731-132"><dt>Ipmsp.h</dt></span></span> </dl>   |
| <span data-ttu-id="e5731-133">Библиотека</span><span class="sxs-lookup"><span data-stu-id="e5731-133">Library</span></span><br/>      | <dl> <span data-ttu-id="e5731-134"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="e5731-134"><dt>Uuid.lib</dt></span></span> </dl>  |
| <span data-ttu-id="e5731-135">DLL</span><span class="sxs-lookup"><span data-stu-id="e5731-135">DLL</span></span><br/>          | <dl> <span data-ttu-id="e5731-136"><dt>Tapi3.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e5731-136"><dt>Tapi3.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e5731-137">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="e5731-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e5731-138">**итформатконтрол**</span><span class="sxs-lookup"><span data-stu-id="e5731-138">**ITFormatControl**</span></span>](itformatcontrol.md)
</dt> <dt>

[<span data-ttu-id="e5731-139">**\_ \_ ограничения конфигурации потока \_ TAPI**</span><span class="sxs-lookup"><span data-stu-id="e5731-139">**TAPI\_STREAM\_CONFIG\_CAPS**</span></span>](tapi-stream-config-caps.md)
</dt> </dl>

 

 




