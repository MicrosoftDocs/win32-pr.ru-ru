---
description: Метод init инициализирует конференцный BLOB-объект на основе текстовой строки. Если Пблоб имеет значение NULL, используются значения по умолчанию.
ms.assetid: ba492503-90ff-45dd-a39f-6d4451e57339
title: 'Метод Итконференцеблоб:: init (Сдпблб. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 81bdd512ffeb4b380da04e59deb17315d00b7285
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105688863"
---
# <a name="itconferenceblobinit-method"></a><span data-ttu-id="8371a-104">Метод Итконференцеблоб:: init</span><span class="sxs-lookup"><span data-stu-id="8371a-104">ITConferenceBlob::Init method</span></span>

<span data-ttu-id="8371a-105">\[ В Windows Vista, Windows Server 2008 и последующих версиях операционной системы нельзя использовать встречные средства и элементы управления Конференц-телефонией и интерфейсы.</span><span class="sxs-lookup"><span data-stu-id="8371a-105">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="8371a-106">API клиента RTC предоставляет аналогичные функциональные возможности.\]</span><span class="sxs-lookup"><span data-stu-id="8371a-106">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="8371a-107">Метод **init** инициализирует конференцный BLOB-объект на основе текстовой строки.</span><span class="sxs-lookup"><span data-stu-id="8371a-107">The **Init** method initializes the conference blob based on a textual string.</span></span> <span data-ttu-id="8371a-108">Если *пблоб* имеет **значение NULL**, используются значения по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="8371a-108">If *pBlob* is **NULL**, default values are used.</span></span>

## <a name="syntax"></a><span data-ttu-id="8371a-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="8371a-109">Syntax</span></span>


```C++
HRESULT Init(
  [in] BSTR               pName,
  [in] BLOB_CHARACTER_SET CharacterSet,
  [in] BSTR               pBlob
);
```



## <a name="parameters"></a><span data-ttu-id="8371a-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="8371a-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8371a-111">*pName* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="8371a-111">*pName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8371a-112">Указатель на представление имени Конференции в формате **BSTR** .</span><span class="sxs-lookup"><span data-stu-id="8371a-112">Pointer to a **BSTR** representation of the conference name.</span></span>

</dd> <dt>

<span data-ttu-id="8371a-113">*Кодировка* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="8371a-113">*CharacterSet* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8371a-114">[**Большой двоичный объект \_ Дескриптор \_ кодировки набора символов**](blob-character-set.md) .</span><span class="sxs-lookup"><span data-stu-id="8371a-114">[**BLOB\_CHARACTER\_SET**](blob-character-set.md) descriptor of the character set.</span></span>

</dd> <dt>

<span data-ttu-id="8371a-115">*пблоб* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="8371a-115">*pBlob* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8371a-116">Указатель на **строку BSTR** , содержащую большой двоичный объект конференции.</span><span class="sxs-lookup"><span data-stu-id="8371a-116">Pointer to a **BSTR** containing the conference blob.</span></span> <span data-ttu-id="8371a-117">Если **значение равно NULL**, то объект Conference BLOB инициализируется со значениями по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="8371a-117">If **NULL**, the conference blob is initialized with default values.</span></span> <span data-ttu-id="8371a-118">В настоящее время значения конференций по умолчанию доступны, только если для параметра " *Кодировка* " задано значение " \_ ASCII".</span><span class="sxs-lookup"><span data-stu-id="8371a-118">Currently, default conference values are available only if the *CharacterSet* parameter is set to BCS\_ASCII.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8371a-119">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="8371a-119">Return value</span></span>

<span data-ttu-id="8371a-120">Этот метод может возвращать одно из этих значений.</span><span class="sxs-lookup"><span data-stu-id="8371a-120">This method can return one of these values.</span></span>



| <span data-ttu-id="8371a-121">Значение</span><span class="sxs-lookup"><span data-stu-id="8371a-121">Value</span></span>                                                                                         | <span data-ttu-id="8371a-122">Значение</span><span class="sxs-lookup"><span data-stu-id="8371a-122">Meaning</span></span>                                                                    |
|-----------------------------------------------------------------------------------------------|----------------------------------------------------------------------------|
| <dl> <span data-ttu-id="8371a-123"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="8371a-123"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="8371a-124">Метод успешно выполнен.</span><span class="sxs-lookup"><span data-stu-id="8371a-124">Method succeeded.</span></span><br/>                                               |
| <dl> <span data-ttu-id="8371a-125"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="8371a-125"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="8371a-126">Недопустимый параметр *pName*, *character* или *пблоб* .</span><span class="sxs-lookup"><span data-stu-id="8371a-126">The *pName*, *CharacterSet*, or *pBlob* parameter is not valid.</span></span><br/> |
| <dl> <span data-ttu-id="8371a-127"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="8371a-127"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="8371a-128">Недостаточно памяти для выполнения операции.</span><span class="sxs-lookup"><span data-stu-id="8371a-128">Insufficient memory exists to perform the operation.</span></span><br/>            |
| <dl> <span data-ttu-id="8371a-129"><dt>**\_Ошибка E**</dt></span><span class="sxs-lookup"><span data-stu-id="8371a-129"><dt>**E\_FAIL**</dt></span></span> </dl>        | <span data-ttu-id="8371a-130">Незаданная ошибка.</span><span class="sxs-lookup"><span data-stu-id="8371a-130">Unspecified error.</span></span><br/>                                              |
| <dl> <span data-ttu-id="8371a-131"><dt>**E \_ нотимпл**</dt></span><span class="sxs-lookup"><span data-stu-id="8371a-131"><dt>**E\_NOTIMPL**</dt></span></span> </dl>     | <span data-ttu-id="8371a-132">Этот метод еще не реализован.</span><span class="sxs-lookup"><span data-stu-id="8371a-132">This method is not yet implemented.</span></span><br/>                             |



 

## <a name="remarks"></a><span data-ttu-id="8371a-133">Комментарии</span><span class="sxs-lookup"><span data-stu-id="8371a-133">Remarks</span></span>

<span data-ttu-id="8371a-134">**Итконференцеблоб:: init** вернет ошибку, если большой двоичный объект уже инициализирован.</span><span class="sxs-lookup"><span data-stu-id="8371a-134">**ITConferenceBlob::Init** will return a failure if the blob has already been initialized.</span></span>

<span data-ttu-id="8371a-135">Приложение должно использовать [**сисаллокстринг**](/windows/win32/api/oleauto/nf-oleauto-sysallocstring) для выделения памяти для параметров *pName* и *пблоб* .</span><span class="sxs-lookup"><span data-stu-id="8371a-135">The application must use [**SysAllocString**](/windows/win32/api/oleauto/nf-oleauto-sysallocstring) to allocate memory for the *pName* and *pBlob* parameters.</span></span> <span data-ttu-id="8371a-136">Приложение должно использовать [**сисфристринг**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) для освобождения памяти, когда переменные больше не нужны.</span><span class="sxs-lookup"><span data-stu-id="8371a-136">The application must use [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) to free the memory when the variables are no longer needed.</span></span>

## <a name="requirements"></a><span data-ttu-id="8371a-137">Требования</span><span class="sxs-lookup"><span data-stu-id="8371a-137">Requirements</span></span>



| <span data-ttu-id="8371a-138">Требование</span><span class="sxs-lookup"><span data-stu-id="8371a-138">Requirement</span></span> | <span data-ttu-id="8371a-139">Значение</span><span class="sxs-lookup"><span data-stu-id="8371a-139">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="8371a-140">Версия TAPI</span><span class="sxs-lookup"><span data-stu-id="8371a-140">TAPI version</span></span><br/> | <span data-ttu-id="8371a-141">Требуется TAPI 3,0 или более поздней версии</span><span class="sxs-lookup"><span data-stu-id="8371a-141">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="8371a-142">Header</span><span class="sxs-lookup"><span data-stu-id="8371a-142">Header</span></span><br/>       | <dl> <span data-ttu-id="8371a-143"><dt>Сдпблб. h</dt></span><span class="sxs-lookup"><span data-stu-id="8371a-143"><dt>Sdpblb.h</dt></span></span> </dl>   |
| <span data-ttu-id="8371a-144">Библиотека</span><span class="sxs-lookup"><span data-stu-id="8371a-144">Library</span></span><br/>      | <dl> <span data-ttu-id="8371a-145"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="8371a-145"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="8371a-146">DLL</span><span class="sxs-lookup"><span data-stu-id="8371a-146">DLL</span></span><br/>          | <dl> <span data-ttu-id="8371a-147"><dt>Sdpblb.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8371a-147"><dt>Sdpblb.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8371a-148">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="8371a-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8371a-149">**итконференцеблоб**</span><span class="sxs-lookup"><span data-stu-id="8371a-149">**ITConferenceBlob**</span></span>](itconferenceblob.md)
</dt> <dt>

[<span data-ttu-id="8371a-150">**\_набор символов BLOB-объектов \_**</span><span class="sxs-lookup"><span data-stu-id="8371a-150">**BLOB\_CHARACTER\_SET**</span></span>](blob-character-set.md)
</dt> </dl>

 

