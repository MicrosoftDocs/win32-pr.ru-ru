---
description: Создает SAFEARRAY автоматизации для неподписанных символов (в байтах).
ms.assetid: 67cc8cd1-95be-4498-ac25-6c418089af27
title: 'Метод Искардтипеконв:: Креатесафеаррай (Скарддат. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardTypeConv.CreateSafeArray
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 6bc27a3f50f0740eca178787fd021f76c9b6729e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104143420"
---
# <a name="iscardtypeconvcreatesafearray-method"></a><span data-ttu-id="cf7c3-103">Метод Искардтипеконв:: Креатесафеаррай</span><span class="sxs-lookup"><span data-stu-id="cf7c3-103">ISCardTypeConv::CreateSafeArray method</span></span>

<span data-ttu-id="cf7c3-104">\[Метод **креатесафеаррай** доступен для использования в операционных системах, указанных в разделе требования.</span><span class="sxs-lookup"><span data-stu-id="cf7c3-104">\[The **CreateSafeArray** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="cf7c3-105">Он недоступен для использования в Windows Server 2003 с пакетом обновления 1 (SP1) и более поздней версии, Windows Vista, Windows Server 2008 и последующих версиях операционной системы.</span><span class="sxs-lookup"><span data-stu-id="cf7c3-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="cf7c3-106">[Модули смарт-карт](/previous-versions/windows/desktop/secsmart/smart-card-modules) предоставляют аналогичные функции.\]</span><span class="sxs-lookup"><span data-stu-id="cf7c3-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="cf7c3-107">Метод **креатесафеаррай** создает SAFEARRAY автоматизации для неподписанных символов (в байтах).</span><span class="sxs-lookup"><span data-stu-id="cf7c3-107">The **CreateSafeArray** method creates an Automation SAFEARRAY of unsigned characters (bytes).</span></span>

## <a name="syntax"></a><span data-ttu-id="cf7c3-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="cf7c3-108">Syntax</span></span>


```C++
HRESULT CreateSafeArray(
  [in]  UINT        nAllocSize,
  [out] LPSAFEARRAY *ppArray
);
```



## <a name="parameters"></a><span data-ttu-id="cf7c3-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="cf7c3-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cf7c3-110">*наллоксизе* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="cf7c3-110">*nAllocSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cf7c3-111">Размер в байтах памяти, выделяемой для массива.</span><span class="sxs-lookup"><span data-stu-id="cf7c3-111">Size in bytes of the memory to be allocated for the array.</span></span>

</dd> <dt>

<span data-ttu-id="cf7c3-112">*ппаррай* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="cf7c3-112">*ppArray* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="cf7c3-113">Указатель на возвращаемый объект SAFEARRAY.</span><span class="sxs-lookup"><span data-stu-id="cf7c3-113">Pointer to the SAFEARRAY object to be returned.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cf7c3-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="cf7c3-114">Return value</span></span>

<span data-ttu-id="cf7c3-115">Метод возвращает одно из следующих возможных значений:</span><span class="sxs-lookup"><span data-stu-id="cf7c3-115">The method returns one of the following possible values:</span></span>



| <span data-ttu-id="cf7c3-116">Код возврата</span><span class="sxs-lookup"><span data-stu-id="cf7c3-116">Return code</span></span>                                                                                   | <span data-ttu-id="cf7c3-117">Описание</span><span class="sxs-lookup"><span data-stu-id="cf7c3-117">Description</span></span>                                                                                      |
|-----------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="cf7c3-118"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="cf7c3-118"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="cf7c3-119">Выделенная память успешно распределена.</span><span class="sxs-lookup"><span data-stu-id="cf7c3-119">Memory allocated successfully.</span></span><br/>                                                        |
| <dl> <span data-ttu-id="cf7c3-120"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="cf7c3-120"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="cf7c3-121">Возникла проблема с одним или несколькими параметрами, передаваемыми в функцию.</span><span class="sxs-lookup"><span data-stu-id="cf7c3-121">There is something wrong with one or more of the parameters passed into the function.</span></span><br/> |
| <dl> <span data-ttu-id="cf7c3-122"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="cf7c3-122"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="cf7c3-123">Недостаточно свободной памяти для удовлетворения запроса.</span><span class="sxs-lookup"><span data-stu-id="cf7c3-123">Not enough free memory to satisfy request.</span></span><br/>                                            |



 

## <a name="remarks"></a><span data-ttu-id="cf7c3-124">Комментарии</span><span class="sxs-lookup"><span data-stu-id="cf7c3-124">Remarks</span></span>

<span data-ttu-id="cf7c3-125">Чтобы создать типичный массив байтов C/C++, вызовите [**креатебитеаррай**](iscardtypeconv-createbytearray.md).</span><span class="sxs-lookup"><span data-stu-id="cf7c3-125">To create a typical C/C++ byte array, call [**CreateByteArray**](iscardtypeconv-createbytearray.md).</span></span>

<span data-ttu-id="cf7c3-126">Чтобы создать универсальный буфер байтов, сопоставленный с объектом **IStream** ([**ибитебуффер**](ibytebuffer.md)), вызовите [**креатебитебуффер**](iscardtypeconv-createbytebuffer.md).</span><span class="sxs-lookup"><span data-stu-id="cf7c3-126">To create a universal buffer of bytes mapped into an **IStream** ([**IByteBuffer**](ibytebuffer.md)) object, call [**CreateByteBuffer**](iscardtypeconv-createbytebuffer.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="cf7c3-127">Требования</span><span class="sxs-lookup"><span data-stu-id="cf7c3-127">Requirements</span></span>



| <span data-ttu-id="cf7c3-128">Требование</span><span class="sxs-lookup"><span data-stu-id="cf7c3-128">Requirement</span></span> | <span data-ttu-id="cf7c3-129">Значение</span><span class="sxs-lookup"><span data-stu-id="cf7c3-129">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="cf7c3-130">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="cf7c3-130">Minimum supported client</span></span><br/> | <span data-ttu-id="cf7c3-131">Только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="cf7c3-131">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="cf7c3-132">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="cf7c3-132">Minimum supported server</span></span><br/> | <span data-ttu-id="cf7c3-133">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="cf7c3-133">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="cf7c3-134">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="cf7c3-134">End of client support</span></span><br/>    | <span data-ttu-id="cf7c3-135">Windows XP</span><span class="sxs-lookup"><span data-stu-id="cf7c3-135">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="cf7c3-136">Поддержка конца сервера</span><span class="sxs-lookup"><span data-stu-id="cf7c3-136">End of server support</span></span><br/>    | <span data-ttu-id="cf7c3-137">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="cf7c3-137">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="cf7c3-138">Header</span><span class="sxs-lookup"><span data-stu-id="cf7c3-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="cf7c3-139"><dt>Скарддат. h</dt></span><span class="sxs-lookup"><span data-stu-id="cf7c3-139"><dt>Scarddat.h</dt></span></span> </dl>   |
| <span data-ttu-id="cf7c3-140">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="cf7c3-140">Type library</span></span><br/>             | <dl> <span data-ttu-id="cf7c3-141"><dt>Скарддат. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="cf7c3-141"><dt>Scarddat.tlb</dt></span></span> </dl> |
| <span data-ttu-id="cf7c3-142">DLL</span><span class="sxs-lookup"><span data-stu-id="cf7c3-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="cf7c3-143"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="cf7c3-143"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="cf7c3-144">IID</span><span class="sxs-lookup"><span data-stu-id="cf7c3-144">IID</span></span><br/>                      | <span data-ttu-id="cf7c3-145">IID \_ искардтипеконв определен как 53B6AA63-3F56-11D0-916B-00AA00C18068</span><span class="sxs-lookup"><span data-stu-id="cf7c3-145">IID\_ISCardTypeConv is defined as 53B6AA63-3F56-11D0-916B-00AA00C18068</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="cf7c3-146">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="cf7c3-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cf7c3-147">**искардтипеконв**</span><span class="sxs-lookup"><span data-stu-id="cf7c3-147">**ISCardTypeConv**</span></span>](iscardtypeconv.md)
</dt> <dt>

[<span data-ttu-id="cf7c3-148">Возвращаемые значения смарт-карты</span><span class="sxs-lookup"><span data-stu-id="cf7c3-148">Smart Card Return Values</span></span>](authentication-return-values.md)
</dt> <dt>

[<span data-ttu-id="cf7c3-149">**креатебитеаррай**</span><span class="sxs-lookup"><span data-stu-id="cf7c3-149">**CreateByteArray**</span></span>](iscardtypeconv-createbytearray.md)
</dt> <dt>

[<span data-ttu-id="cf7c3-150">**креатебитебуффер**</span><span class="sxs-lookup"><span data-stu-id="cf7c3-150">**CreateByteBuffer**</span></span>](iscardtypeconv-createbytebuffer.md)
</dt> </dl>

 

 
