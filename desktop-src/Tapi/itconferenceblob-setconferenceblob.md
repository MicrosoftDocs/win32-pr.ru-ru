---
description: Метод Сетконференцеблоб фиксирует изменения в большом двоичном объекте Конференции. Чтобы в первый раз инициализировать объект Conference, используйте метод init.
ms.assetid: 4a65edb9-77de-42d9-85a1-1e3c41706417
title: 'Метод Итконференцеблоб:: Сетконференцеблоб (Сдпблб. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 47779807e5bde6a070b4600aec903309c7679dc8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105675518"
---
# <a name="itconferenceblobsetconferenceblob-method"></a><span data-ttu-id="f19f2-104">Метод Итконференцеблоб:: Сетконференцеблоб</span><span class="sxs-lookup"><span data-stu-id="f19f2-104">ITConferenceBlob::SetConferenceBlob method</span></span>

<span data-ttu-id="f19f2-105">\[ В Windows Vista, Windows Server 2008 и последующих версиях операционной системы нельзя использовать встречные средства и элементы управления Конференц-телефонией и интерфейсы.</span><span class="sxs-lookup"><span data-stu-id="f19f2-105">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="f19f2-106">API клиента RTC предоставляет аналогичные функциональные возможности.\]</span><span class="sxs-lookup"><span data-stu-id="f19f2-106">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="f19f2-107">Метод **сетконференцеблоб** фиксирует изменения в большом двоичном объекте Конференции.</span><span class="sxs-lookup"><span data-stu-id="f19f2-107">The **SetConferenceBlob** method commits changes to the conference blob.</span></span> <span data-ttu-id="f19f2-108">Чтобы в первый раз инициализировать объект Conference, используйте метод [**init**](itconferenceblob-init.md) .</span><span class="sxs-lookup"><span data-stu-id="f19f2-108">To initialize the conference blob for the first time, use the [**Init**](itconferenceblob-init.md) method instead.</span></span>

## <a name="syntax"></a><span data-ttu-id="f19f2-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="f19f2-109">Syntax</span></span>


```C++
HRESULT SetConferenceBlob(
  [in] BLOB_CHARACTER_SET CharacterSet,
  [in] BSTR               pBlob
);
```



## <a name="parameters"></a><span data-ttu-id="f19f2-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="f19f2-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f19f2-111">*Кодировка* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="f19f2-111">*CharacterSet* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f19f2-112">[**Большой двоичный объект \_ Дескриптор \_ кодировки набора символов для**](blob-character-set.md) объекта Conference.</span><span class="sxs-lookup"><span data-stu-id="f19f2-112">[**BLOB\_CHARACTER\_SET**](blob-character-set.md) descriptor of the conference blob's character set.</span></span>

</dd> <dt>

<span data-ttu-id="f19f2-113">*пблоб* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="f19f2-113">*pBlob* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f19f2-114">Указатель на **строку BSTR** , содержащую большой двоичный объект конференции.</span><span class="sxs-lookup"><span data-stu-id="f19f2-114">Pointer to a **BSTR** containing the conference blob.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f19f2-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="f19f2-115">Return value</span></span>

<span data-ttu-id="f19f2-116">Этот метод может возвращать одно из этих значений.</span><span class="sxs-lookup"><span data-stu-id="f19f2-116">This method can return one of these values.</span></span>



| <span data-ttu-id="f19f2-117">Код возврата</span><span class="sxs-lookup"><span data-stu-id="f19f2-117">Return code</span></span>                                                                                   | <span data-ttu-id="f19f2-118">Описание</span><span class="sxs-lookup"><span data-stu-id="f19f2-118">Description</span></span>                                                      |
|-----------------------------------------------------------------------------------------------|------------------------------------------------------------------|
| <dl> <span data-ttu-id="f19f2-119"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="f19f2-119"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="f19f2-120">Метод успешно выполнен.</span><span class="sxs-lookup"><span data-stu-id="f19f2-120">Method succeeded.</span></span><br/>                                     |
| <dl> <span data-ttu-id="f19f2-121"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="f19f2-121"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="f19f2-122">Недопустимый параметр *character* или *пблоб* .</span><span class="sxs-lookup"><span data-stu-id="f19f2-122">The *CharacterSet* or *pBlob* parameter is not valid.</span></span><br/> |
| <dl> <span data-ttu-id="f19f2-123"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="f19f2-123"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="f19f2-124">Недостаточно памяти для выполнения операции.</span><span class="sxs-lookup"><span data-stu-id="f19f2-124">Insufficient memory exists to perform the operation.</span></span><br/>  |
| <dl> <span data-ttu-id="f19f2-125"><dt>**\_Ошибка E**</dt></span><span class="sxs-lookup"><span data-stu-id="f19f2-125"><dt>**E\_FAIL**</dt></span></span> </dl>        | <span data-ttu-id="f19f2-126">Незаданная ошибка.</span><span class="sxs-lookup"><span data-stu-id="f19f2-126">Unspecified error.</span></span><br/>                                    |
| <dl> <span data-ttu-id="f19f2-127"><dt>**E \_ нотимпл**</dt></span><span class="sxs-lookup"><span data-stu-id="f19f2-127"><dt>**E\_NOTIMPL**</dt></span></span> </dl>     | <span data-ttu-id="f19f2-128">Этот метод еще не реализован.</span><span class="sxs-lookup"><span data-stu-id="f19f2-128">This method is not yet implemented.</span></span><br/>                   |



 

## <a name="remarks"></a><span data-ttu-id="f19f2-129">Комментарии</span><span class="sxs-lookup"><span data-stu-id="f19f2-129">Remarks</span></span>

<span data-ttu-id="f19f2-130">Приложение должно использовать [**сисаллокстринг**](/windows/win32/api/oleauto/nf-oleauto-sysallocstring) для выделения памяти для параметра *Пблоб* и использовать [**сисфристринг**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) для освобождения памяти, когда переменная больше не нужна.</span><span class="sxs-lookup"><span data-stu-id="f19f2-130">The application must use [**SysAllocString**](/windows/win32/api/oleauto/nf-oleauto-sysallocstring) to allocate memory for the *pBlob* parameter and use [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) to free the memory when the variable is no longer needed.</span></span>

## <a name="requirements"></a><span data-ttu-id="f19f2-131">Требования</span><span class="sxs-lookup"><span data-stu-id="f19f2-131">Requirements</span></span>



| <span data-ttu-id="f19f2-132">Требование</span><span class="sxs-lookup"><span data-stu-id="f19f2-132">Requirement</span></span> | <span data-ttu-id="f19f2-133">Значение</span><span class="sxs-lookup"><span data-stu-id="f19f2-133">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="f19f2-134">Версия TAPI</span><span class="sxs-lookup"><span data-stu-id="f19f2-134">TAPI version</span></span><br/> | <span data-ttu-id="f19f2-135">Требуется TAPI 3,0 или более поздней версии</span><span class="sxs-lookup"><span data-stu-id="f19f2-135">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="f19f2-136">Header</span><span class="sxs-lookup"><span data-stu-id="f19f2-136">Header</span></span><br/>       | <dl> <span data-ttu-id="f19f2-137"><dt>Сдпблб. h</dt></span><span class="sxs-lookup"><span data-stu-id="f19f2-137"><dt>Sdpblb.h</dt></span></span> </dl>   |
| <span data-ttu-id="f19f2-138">Библиотека</span><span class="sxs-lookup"><span data-stu-id="f19f2-138">Library</span></span><br/>      | <dl> <span data-ttu-id="f19f2-139"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="f19f2-139"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="f19f2-140">DLL</span><span class="sxs-lookup"><span data-stu-id="f19f2-140">DLL</span></span><br/>          | <dl> <span data-ttu-id="f19f2-141"><dt>Sdpblb.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f19f2-141"><dt>Sdpblb.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f19f2-142">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="f19f2-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f19f2-143">**итконференцеблоб**</span><span class="sxs-lookup"><span data-stu-id="f19f2-143">**ITConferenceBlob**</span></span>](itconferenceblob.md)
</dt> <dt>

[<span data-ttu-id="f19f2-144">**\_набор символов BLOB-объектов \_**</span><span class="sxs-lookup"><span data-stu-id="f19f2-144">**BLOB\_CHARACTER\_SET**</span></span>](blob-character-set.md)
</dt> </dl>

 

