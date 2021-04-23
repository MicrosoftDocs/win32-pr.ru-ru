---
description: Метод получения \_ символов возвращает дескриптор набора символов большого двоичного объекта \_ \_ , используемого в текущем большом двоичном объекте Конференции.
ms.assetid: 9783d18c-79f6-4faa-b12d-9504c13d54e3
title: 'Метод Итконференцеблоб:: get_CharacterSet (Сдпблб. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 681085672f49c75a8434c4b0311e75d2b9cea270
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105675521"
---
# <a name="itconferenceblobget_characterset-method"></a><span data-ttu-id="443e4-103">Метод Итконференцеблоб:: Get \_ character</span><span class="sxs-lookup"><span data-stu-id="443e4-103">ITConferenceBlob::get\_CharacterSet method</span></span>

<span data-ttu-id="443e4-104">\[ В Windows Vista, Windows Server 2008 и последующих версиях операционной системы нельзя использовать встречные средства и элементы управления Конференц-телефонией и интерфейсы.</span><span class="sxs-lookup"><span data-stu-id="443e4-104">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="443e4-105">API клиента RTC предоставляет аналогичные функциональные возможности.\]</span><span class="sxs-lookup"><span data-stu-id="443e4-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="443e4-106">Метод **получения \_ символов** возвращает дескриптор [**\_ \_ набора символов большого двоичного объекта**](blob-character-set.md) , используемого в текущем большом двоичном объекте Конференции.</span><span class="sxs-lookup"><span data-stu-id="443e4-106">The **get\_CharacterSet** method gets a [**BLOB\_CHARACTER\_SET**](blob-character-set.md) descriptor of the character set used in the current conference blob.</span></span>

## <a name="syntax"></a><span data-ttu-id="443e4-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="443e4-107">Syntax</span></span>


```C++
HRESULT get_CharacterSet(
  [out] BLOB_CHARACTER_SET *pCharacterSet
);
```



## <a name="parameters"></a><span data-ttu-id="443e4-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="443e4-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="443e4-109">*пчарактерсет* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="443e4-109">*pCharacterSet* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="443e4-110">Указатель на дескриптор [**\_ \_ набора символов большого двоичного объекта**](blob-character-set.md) в кодировке.</span><span class="sxs-lookup"><span data-stu-id="443e4-110">Pointer to a [**BLOB\_CHARACTER\_SET**](blob-character-set.md) descriptor of the character set.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="443e4-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="443e4-111">Return value</span></span>

<span data-ttu-id="443e4-112">Этот метод может возвращать одно из этих значений.</span><span class="sxs-lookup"><span data-stu-id="443e4-112">This method can return one of these values.</span></span>



| <span data-ttu-id="443e4-113">Код возврата</span><span class="sxs-lookup"><span data-stu-id="443e4-113">Return code</span></span>                                                                                                   | <span data-ttu-id="443e4-114">Описание</span><span class="sxs-lookup"><span data-stu-id="443e4-114">Description</span></span>                                                      |
|---------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------|
| <dl> <span data-ttu-id="443e4-115"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="443e4-115"><dt>**S\_OK**</dt></span></span> </dl>                          | <span data-ttu-id="443e4-116">Метод успешно выполнен.</span><span class="sxs-lookup"><span data-stu-id="443e4-116">Method succeeded.</span></span><br/>                                     |
| <dl> <span data-ttu-id="443e4-117"><dt>**\_указатель E**</dt></span><span class="sxs-lookup"><span data-stu-id="443e4-117"><dt>**E\_POINTER**</dt></span></span> </dl>                     | <span data-ttu-id="443e4-118">Параметр *пчарактерсет* не является допустимым указателем.</span><span class="sxs-lookup"><span data-stu-id="443e4-118">The *pCharacterSet* parameter is not a valid pointer.</span></span><br/> |
| <dl> <span data-ttu-id="443e4-119"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="443e4-119"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl>                 | <span data-ttu-id="443e4-120">Недостаточно памяти для выполнения операции.</span><span class="sxs-lookup"><span data-stu-id="443e4-120">Insufficient memory exists to perform the operation.</span></span><br/>  |
| <dl> <span data-ttu-id="443e4-121"><dt>**\_Ошибка E**</dt></span><span class="sxs-lookup"><span data-stu-id="443e4-121"><dt>**E\_FAIL**</dt></span></span> </dl>                        | <span data-ttu-id="443e4-122">Незаданная ошибка.</span><span class="sxs-lookup"><span data-stu-id="443e4-122">Unspecified error.</span></span><br/>                                    |
| <dl> <span data-ttu-id="443e4-123"><dt>**E \_ нотимпл**</dt></span><span class="sxs-lookup"><span data-stu-id="443e4-123"><dt>**E\_NOTIMPL**</dt></span></span> </dl>                     | <span data-ttu-id="443e4-124">Этот метод еще не реализован.</span><span class="sxs-lookup"><span data-stu-id="443e4-124">This method is not yet implemented.</span></span><br/>                   |
| <dl> <span data-ttu-id="443e4-125"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="443e4-125"><dt>**E\_INVALIDARG**</dt></span></span> </dl>                  | <span data-ttu-id="443e4-126">*пчарактерсет* имеет **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="443e4-126">*pCharacterSet* is **NULL**.</span></span><br/>                          |
| <dl> <span data-ttu-id="443e4-127"><dt>**СОСТАВ Ошибка при \_ недопустимых \_ данных**</dt></span><span class="sxs-lookup"><span data-stu-id="443e4-127"><dt>**(HRESULT) ERROR\_INVALID\_DATA**</dt></span></span> </dl> | <span data-ttu-id="443e4-128">Текущий набор символов недопустим или недоступен.</span><span class="sxs-lookup"><span data-stu-id="443e4-128">The current character set is invalid or unavailable.</span></span><br/>  |



 

## <a name="requirements"></a><span data-ttu-id="443e4-129">Требования</span><span class="sxs-lookup"><span data-stu-id="443e4-129">Requirements</span></span>



| <span data-ttu-id="443e4-130">Требование</span><span class="sxs-lookup"><span data-stu-id="443e4-130">Requirement</span></span> | <span data-ttu-id="443e4-131">Значение</span><span class="sxs-lookup"><span data-stu-id="443e4-131">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="443e4-132">Версия TAPI</span><span class="sxs-lookup"><span data-stu-id="443e4-132">TAPI version</span></span><br/> | <span data-ttu-id="443e4-133">Требуется TAPI 3,0 или более поздней версии</span><span class="sxs-lookup"><span data-stu-id="443e4-133">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="443e4-134">Header</span><span class="sxs-lookup"><span data-stu-id="443e4-134">Header</span></span><br/>       | <dl> <span data-ttu-id="443e4-135"><dt>Сдпблб. h</dt></span><span class="sxs-lookup"><span data-stu-id="443e4-135"><dt>Sdpblb.h</dt></span></span> </dl>   |
| <span data-ttu-id="443e4-136">Библиотека</span><span class="sxs-lookup"><span data-stu-id="443e4-136">Library</span></span><br/>      | <dl> <span data-ttu-id="443e4-137"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="443e4-137"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="443e4-138">DLL</span><span class="sxs-lookup"><span data-stu-id="443e4-138">DLL</span></span><br/>          | <dl> <span data-ttu-id="443e4-139"><dt>Sdpblb.dll</dt></span><span class="sxs-lookup"><span data-stu-id="443e4-139"><dt>Sdpblb.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="443e4-140">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="443e4-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="443e4-141">**итконференцеблоб**</span><span class="sxs-lookup"><span data-stu-id="443e4-141">**ITConferenceBlob**</span></span>](itconferenceblob.md)
</dt> <dt>

[<span data-ttu-id="443e4-142">**\_набор символов BLOB-объектов \_**</span><span class="sxs-lookup"><span data-stu-id="443e4-142">**BLOB\_CHARACTER\_SET**</span></span>](blob-character-set.md)
</dt> </dl>

 

 




