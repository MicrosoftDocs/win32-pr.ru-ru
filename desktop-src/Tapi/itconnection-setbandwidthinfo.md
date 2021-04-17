---
description: Метод Сетбандвидсинфо задает сведения о пропускной способности.
ms.assetid: bf5db456-ea67-4a65-a681-df0741f73fc9
title: 'Метод Итконнектион:: Сетбандвидсинфо (Сдпблб. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5c17054743f6d47775e994dbfe3b80c7afe1ab68
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105685314"
---
# <a name="itconnectionsetbandwidthinfo-method"></a><span data-ttu-id="df40b-103">Метод Итконнектион:: Сетбандвидсинфо</span><span class="sxs-lookup"><span data-stu-id="df40b-103">ITConnection::SetBandwidthInfo method</span></span>

<span data-ttu-id="df40b-104">\[ В Windows Vista, Windows Server 2008 и последующих версиях операционной системы нельзя использовать встречные средства и элементы управления Конференц-телефонией и интерфейсы.</span><span class="sxs-lookup"><span data-stu-id="df40b-104">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="df40b-105">API клиента RTC предоставляет аналогичные функциональные возможности.\]</span><span class="sxs-lookup"><span data-stu-id="df40b-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="df40b-106">Метод **сетбандвидсинфо** задает сведения о пропускной способности.</span><span class="sxs-lookup"><span data-stu-id="df40b-106">The **SetBandwidthInfo** method sets the bandwidth information.</span></span>

## <a name="syntax"></a><span data-ttu-id="df40b-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="df40b-107">Syntax</span></span>


```C++
HRESULT SetBandwidthInfo(
  [in] BSTR   pModifier,
  [in] DOUBLE Bandwidth
);
```



## <a name="parameters"></a><span data-ttu-id="df40b-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="df40b-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="df40b-109">*пмодифиер* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="df40b-109">*pModifier* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="df40b-110">Указатель на **BSTR** , указывающий область устанавливаемой пропускной способности.</span><span class="sxs-lookup"><span data-stu-id="df40b-110">Pointer to a **BSTR** indicating the scope of the bandwidth being set.</span></span> <span data-ttu-id="df40b-111">Дополнительные сведения см. в разделе "Примечания".</span><span class="sxs-lookup"><span data-stu-id="df40b-111">For more information, see the following Remarks section.</span></span>

</dd> <dt>

<span data-ttu-id="df40b-112">*Пропускная способность* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="df40b-112">*Bandwidth* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="df40b-113">Связи.</span><span class="sxs-lookup"><span data-stu-id="df40b-113">Bandwidth.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="df40b-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="df40b-114">Return value</span></span>

<span data-ttu-id="df40b-115">Этот метод может возвращать одно из этих значений.</span><span class="sxs-lookup"><span data-stu-id="df40b-115">This method can return one of these values.</span></span>



| <span data-ttu-id="df40b-116">Значение</span><span class="sxs-lookup"><span data-stu-id="df40b-116">Value</span></span>                                                                                         | <span data-ttu-id="df40b-117">Значение</span><span class="sxs-lookup"><span data-stu-id="df40b-117">Meaning</span></span>                                                           |
|-----------------------------------------------------------------------------------------------|-------------------------------------------------------------------|
| <dl> <span data-ttu-id="df40b-118"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="df40b-118"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="df40b-119">Метод успешно выполнен.</span><span class="sxs-lookup"><span data-stu-id="df40b-119">Method succeeded.</span></span><br/>                                      |
| <dl> <span data-ttu-id="df40b-120"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="df40b-120"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="df40b-121">Недопустимый параметр *пмодифиер* или *пропускной способности* .</span><span class="sxs-lookup"><span data-stu-id="df40b-121">The *pModifier* or *Bandwidth* parameter is not valid.</span></span><br/> |
| <dl> <span data-ttu-id="df40b-122"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="df40b-122"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="df40b-123">Недостаточно памяти для выполнения операции.</span><span class="sxs-lookup"><span data-stu-id="df40b-123">Insufficient memory exists to perform the operation.</span></span><br/>   |
| <dl> <span data-ttu-id="df40b-124"><dt>**\_Ошибка E**</dt></span><span class="sxs-lookup"><span data-stu-id="df40b-124"><dt>**E\_FAIL**</dt></span></span> </dl>        | <span data-ttu-id="df40b-125">Незаданная ошибка.</span><span class="sxs-lookup"><span data-stu-id="df40b-125">Unspecified error.</span></span><br/>                                     |
| <dl> <span data-ttu-id="df40b-126"><dt>**E \_ нотимпл**</dt></span><span class="sxs-lookup"><span data-stu-id="df40b-126"><dt>**E\_NOTIMPL**</dt></span></span> </dl>     | <span data-ttu-id="df40b-127">Этот метод еще не реализован.</span><span class="sxs-lookup"><span data-stu-id="df40b-127">This method is not yet implemented.</span></span><br/>                    |



 

## <a name="remarks"></a><span data-ttu-id="df40b-128">Комментарии</span><span class="sxs-lookup"><span data-stu-id="df40b-128">Remarks</span></span>

<span data-ttu-id="df40b-129">Приложение должно использовать [**сисаллокстринг**](/windows/win32/api/oleauto/nf-oleauto-sysallocstring) для выделения памяти для параметра *Пмодифиер* и использовать [**сисфристринг**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) для освобождения памяти, когда переменная больше не нужна.</span><span class="sxs-lookup"><span data-stu-id="df40b-129">The application must use [**SysAllocString**](/windows/win32/api/oleauto/nf-oleauto-sysallocstring) to allocate memory for the *pModifier* parameter and use [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) to free the memory when the variable is no longer needed.</span></span>

<span data-ttu-id="df40b-130">Справочник: RFC 2327.</span><span class="sxs-lookup"><span data-stu-id="df40b-130">Reference: RFC 2327.</span></span>

<span data-ttu-id="df40b-131">В качестве модификатора пропускной способности обычно будет использоваться либо CT, либо как:</span><span class="sxs-lookup"><span data-stu-id="df40b-131">The bandwidth modifier will normally be either CT or AS:</span></span>

<span data-ttu-id="df40b-132">**Общая Конференция по CT:** Неявная максимальная пропускная способность связана [*с каждым сроком жизни (*](t-tapgloss.md) TTL) мбоне или в определенном регионе многоадресной административной области (в разделе часто задаваемых вопросов по мбоне указаны ограничения пропускной способности МБОНЕ и TTL).</span><span class="sxs-lookup"><span data-stu-id="df40b-132">**CT Conference Total:** An implicit maximum bandwidth is associated with each [*time to live*](t-tapgloss.md) (TTL) on the Mbone or within a particular multicast administrative scope region (the Mbone bandwidth versus TTL limits are given in the MBone FAQ).</span></span> <span data-ttu-id="df40b-133">Если пропускная способность сеанса или мультимедиа в сеансе отличается от пропускной способности, неявной от области, a \` b = CT:... ' для сеанса необходимо указать строку, которая предоставляет предложенный верхний предел для используемой пропускной способности.</span><span class="sxs-lookup"><span data-stu-id="df40b-133">If the bandwidth of a session or media in a session is different from the bandwidth implicit from the scope, a \`b=CT:...' line should be supplied for the session giving the proposed upper limit to the bandwidth used.</span></span> <span data-ttu-id="df40b-134">Основная цель этого — дать приблизительное представление о том, могут ли две или несколько конференций одновременно сосуществовать.</span><span class="sxs-lookup"><span data-stu-id="df40b-134">The primary purpose of this is to give an approximate idea as to whether two or more conferences can coexist simultaneously.</span></span>

<span data-ttu-id="df40b-135">**Максимально Application-Specific:** Пропускная способность интерпретируется как зависящая от приложения, т. е. будет понятием максимальной пропускной способности приложения.</span><span class="sxs-lookup"><span data-stu-id="df40b-135">**AS Application-Specific Maximum:** The bandwidth is interpreted to be application-specific, i.e., will be the application's concept of maximum bandwidth.</span></span> <span data-ttu-id="df40b-136">Обычно это будет совпадать с тем, что задано для элемента управления "максимальная пропускная способность" приложения, если это применимо.</span><span class="sxs-lookup"><span data-stu-id="df40b-136">Normally this will coincide with what is set on the application's "maximum bandwidth" control, if applicable.</span></span>

<span data-ttu-id="df40b-137">Обратите внимание, что CT предоставляет общую пропускную способность для всех носителей на всех сайтах.</span><span class="sxs-lookup"><span data-stu-id="df40b-137">Note that CT gives a total bandwidth figure for all the media at all sites.</span></span> <span data-ttu-id="df40b-138">КАК дает цифровую пропускную способность для одного носителя на одном сайте, хотя может одновременно отправляться множество сайтов.</span><span class="sxs-lookup"><span data-stu-id="df40b-138">AS gives a bandwidth figure for a single media at a single site, although there may be many sites sending simultaneously.</span></span>

<span data-ttu-id="df40b-139">**Механизм расширения:** Средства записи инструментов могут определять экспериментальные модификаторы пропускной способности путем добавления префиксов "X-" к их модификаторам.</span><span class="sxs-lookup"><span data-stu-id="df40b-139">**Extension Mechanism:** Tool writers can define experimental bandwidth modifiers by prefixing their modifiers with "X-".</span></span>

## <a name="requirements"></a><span data-ttu-id="df40b-140">Требования</span><span class="sxs-lookup"><span data-stu-id="df40b-140">Requirements</span></span>



| <span data-ttu-id="df40b-141">Требование</span><span class="sxs-lookup"><span data-stu-id="df40b-141">Requirement</span></span> | <span data-ttu-id="df40b-142">Значение</span><span class="sxs-lookup"><span data-stu-id="df40b-142">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="df40b-143">Версия TAPI</span><span class="sxs-lookup"><span data-stu-id="df40b-143">TAPI version</span></span><br/> | <span data-ttu-id="df40b-144">Требуется TAPI 3,0 или более поздней версии</span><span class="sxs-lookup"><span data-stu-id="df40b-144">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="df40b-145">Header</span><span class="sxs-lookup"><span data-stu-id="df40b-145">Header</span></span><br/>       | <dl> <span data-ttu-id="df40b-146"><dt>Сдпблб. h</dt></span><span class="sxs-lookup"><span data-stu-id="df40b-146"><dt>Sdpblb.h</dt></span></span> </dl>   |
| <span data-ttu-id="df40b-147">Библиотека</span><span class="sxs-lookup"><span data-stu-id="df40b-147">Library</span></span><br/>      | <dl> <span data-ttu-id="df40b-148"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="df40b-148"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="df40b-149">DLL</span><span class="sxs-lookup"><span data-stu-id="df40b-149">DLL</span></span><br/>          | <dl> <span data-ttu-id="df40b-150"><dt>Sdpblb.dll</dt></span><span class="sxs-lookup"><span data-stu-id="df40b-150"><dt>Sdpblb.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="df40b-151">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="df40b-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="df40b-152">**итконнектион**</span><span class="sxs-lookup"><span data-stu-id="df40b-152">**ITConnection**</span></span>](itconnection.md)
</dt> </dl>

 

