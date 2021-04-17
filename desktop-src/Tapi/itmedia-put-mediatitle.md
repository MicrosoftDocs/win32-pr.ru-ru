---
description: Метод размещения \_ медиатитле задает текстовый заголовок для носителя, который приложение может использовать для информационных и экранных целей. Это должна быть Преобразуемая строка в кодировке ASCII, если кодировка — ASCII. В противном случае это может быть любая строка BSTR.
ms.assetid: bbab033b-bd37-4ef6-9e84-1d0b17ecbd4e
title: 'Итмедиа: метод ut_MediaTitle:p (Сдпблб. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c1d1abee91b08555f79437e5e26710761429e4f1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105685292"
---
# <a name="itmediaput_mediatitle-method"></a><span data-ttu-id="68757-105">Итмедиа::p UT \_ медиатитле метод</span><span class="sxs-lookup"><span data-stu-id="68757-105">ITMedia::put\_MediaTitle method</span></span>

<span data-ttu-id="68757-106">\[ В Windows Vista, Windows Server 2008 и последующих версиях операционной системы нельзя использовать встречные средства и элементы управления Конференц-телефонией и интерфейсы.</span><span class="sxs-lookup"><span data-stu-id="68757-106">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="68757-107">API клиента RTC предоставляет аналогичные функциональные возможности.\]</span><span class="sxs-lookup"><span data-stu-id="68757-107">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="68757-108">Метод **размещения \_ медиатитле** задает текстовый заголовок для носителя, который приложение может использовать для информационных и экранных целей.</span><span class="sxs-lookup"><span data-stu-id="68757-108">The **put\_MediaTitle** method sets a textual title for the media that the application can use for informational or display purposes.</span></span> <span data-ttu-id="68757-109">Это должна быть Преобразуемая строка в кодировке ASCII, если кодировка — ASCII.</span><span class="sxs-lookup"><span data-stu-id="68757-109">This must be an ASCII convertible string if the character set is ASCII.</span></span> <span data-ttu-id="68757-110">В противном случае это может быть любая строка **BSTR** .</span><span class="sxs-lookup"><span data-stu-id="68757-110">Otherwise, it can be any **BSTR** string.</span></span>

## <a name="syntax"></a><span data-ttu-id="68757-111">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="68757-111">Syntax</span></span>


```C++
HRESULT put_MediaTitle(
  [in] BSTR pMediaTitle
);
```



## <a name="parameters"></a><span data-ttu-id="68757-112">Параметры</span><span class="sxs-lookup"><span data-stu-id="68757-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="68757-113">*пмедиатитле* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="68757-113">*pMediaTitle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="68757-114">Указатель на **строку BSTR** , содержащую заголовок носителя.</span><span class="sxs-lookup"><span data-stu-id="68757-114">Pointer to a **BSTR** containing the title of the media.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="68757-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="68757-115">Return value</span></span>

<span data-ttu-id="68757-116">Этот метод может возвращать одно из этих значений.</span><span class="sxs-lookup"><span data-stu-id="68757-116">This method can return one of these values.</span></span>



| <span data-ttu-id="68757-117">Код возврата</span><span class="sxs-lookup"><span data-stu-id="68757-117">Return code</span></span>                                                                                   | <span data-ttu-id="68757-118">Описание</span><span class="sxs-lookup"><span data-stu-id="68757-118">Description</span></span>                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="68757-119"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="68757-119"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="68757-120">Метод успешно выполнен.</span><span class="sxs-lookup"><span data-stu-id="68757-120">Method succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="68757-121"><dt>**\_указатель E**</dt></span><span class="sxs-lookup"><span data-stu-id="68757-121"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="68757-122">Параметр *пмедиатитле* не является допустимым указателем.</span><span class="sxs-lookup"><span data-stu-id="68757-122">The *pMediaTitle* parameter is not a valid pointer.</span></span><br/>  |
| <dl> <span data-ttu-id="68757-123"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="68757-123"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="68757-124">Недопустимый параметр *пмедиатитле* .</span><span class="sxs-lookup"><span data-stu-id="68757-124">The *pMediaTitle* parameter is not valid.</span></span><br/>            |
| <dl> <span data-ttu-id="68757-125"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="68757-125"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="68757-126">Недостаточно памяти для выполнения операции.</span><span class="sxs-lookup"><span data-stu-id="68757-126">Insufficient memory exists to perform the operation.</span></span><br/> |
| <dl> <span data-ttu-id="68757-127"><dt>**\_Ошибка E**</dt></span><span class="sxs-lookup"><span data-stu-id="68757-127"><dt>**E\_FAIL**</dt></span></span> </dl>        | <span data-ttu-id="68757-128">Незаданная ошибка.</span><span class="sxs-lookup"><span data-stu-id="68757-128">Unspecified error.</span></span><br/>                                   |
| <dl> <span data-ttu-id="68757-129"><dt>**E \_ нотимпл**</dt></span><span class="sxs-lookup"><span data-stu-id="68757-129"><dt>**E\_NOTIMPL**</dt></span></span> </dl>     | <span data-ttu-id="68757-130">Этот метод еще не реализован.</span><span class="sxs-lookup"><span data-stu-id="68757-130">This method is not yet implemented.</span></span><br/>                  |



 

## <a name="remarks"></a><span data-ttu-id="68757-131">Комментарии</span><span class="sxs-lookup"><span data-stu-id="68757-131">Remarks</span></span>

<span data-ttu-id="68757-132">Приложение должно использовать [**сисаллокстринг**](/windows/win32/api/oleauto/nf-oleauto-sysallocstring) для выделения памяти для параметра *Пмедиатитле* и использовать [**сисфристринг**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) для освобождения памяти, когда переменная больше не нужна.</span><span class="sxs-lookup"><span data-stu-id="68757-132">The application must use [**SysAllocString**](/windows/win32/api/oleauto/nf-oleauto-sysallocstring) to allocate memory for the *pMediaTitle* parameter and use [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) to free the memory when the variable is no longer needed.</span></span>

<span data-ttu-id="68757-133">Эта функция может передавать данные по сети в незашифрованном виде; Таким образом, кто-то, кто прослушивает сеть, может прочитать данные.</span><span class="sxs-lookup"><span data-stu-id="68757-133">This function may send data over the wire in unencrypted form; therefore, someone eavesdropping on the network may be able to read the data.</span></span> <span data-ttu-id="68757-134">Прежде чем использовать этот метод, следует учесть угрозу безопасности при отправке данных в виде открытого текста.</span><span class="sxs-lookup"><span data-stu-id="68757-134">The security risk of sending the data in clear text should be considered before using this method.</span></span>

## <a name="requirements"></a><span data-ttu-id="68757-135">Требования</span><span class="sxs-lookup"><span data-stu-id="68757-135">Requirements</span></span>



| <span data-ttu-id="68757-136">Требование</span><span class="sxs-lookup"><span data-stu-id="68757-136">Requirement</span></span> | <span data-ttu-id="68757-137">Значение</span><span class="sxs-lookup"><span data-stu-id="68757-137">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="68757-138">Версия TAPI</span><span class="sxs-lookup"><span data-stu-id="68757-138">TAPI version</span></span><br/> | <span data-ttu-id="68757-139">Требуется TAPI 3,0 или более поздней версии</span><span class="sxs-lookup"><span data-stu-id="68757-139">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="68757-140">Header</span><span class="sxs-lookup"><span data-stu-id="68757-140">Header</span></span><br/>       | <dl> <span data-ttu-id="68757-141"><dt>Сдпблб. h</dt></span><span class="sxs-lookup"><span data-stu-id="68757-141"><dt>Sdpblb.h</dt></span></span> </dl>   |
| <span data-ttu-id="68757-142">Библиотека</span><span class="sxs-lookup"><span data-stu-id="68757-142">Library</span></span><br/>      | <dl> <span data-ttu-id="68757-143"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="68757-143"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="68757-144">DLL</span><span class="sxs-lookup"><span data-stu-id="68757-144">DLL</span></span><br/>          | <dl> <span data-ttu-id="68757-145"><dt>Sdpblb.dll</dt></span><span class="sxs-lookup"><span data-stu-id="68757-145"><dt>Sdpblb.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="68757-146">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="68757-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="68757-147">**итмедиа**</span><span class="sxs-lookup"><span data-stu-id="68757-147">**ITMedia**</span></span>](itmedia.md)
</dt> <dt>

[<span data-ttu-id="68757-148">**Итмедиа:: Get \_ медиатитле**</span><span class="sxs-lookup"><span data-stu-id="68757-148">**ITMedia::get\_MediaTitle**</span></span>](itmedia-get-mediatitle.md)
</dt> </dl>

 

