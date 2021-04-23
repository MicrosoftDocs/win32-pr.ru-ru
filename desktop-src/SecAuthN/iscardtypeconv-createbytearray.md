---
description: Создает типичный массив байтов C/C++.
ms.assetid: 915e8cca-2a0f-409e-a6df-54fa73bdc305
title: 'Метод Искардтипеконв:: Креатебитеаррай (Скарддат. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardTypeConv.CreateByteArray
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: ae253af1b24433987baf66364519a3761f7e0365
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104156574"
---
# <a name="iscardtypeconvcreatebytearray-method"></a><span data-ttu-id="523f7-103">Метод Искардтипеконв:: Креатебитеаррай</span><span class="sxs-lookup"><span data-stu-id="523f7-103">ISCardTypeConv::CreateByteArray method</span></span>

<span data-ttu-id="523f7-104">\[Метод **креатебитеаррай** доступен для использования в операционных системах, указанных в разделе требования.</span><span class="sxs-lookup"><span data-stu-id="523f7-104">\[The **CreateByteArray** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="523f7-105">Он недоступен для использования в Windows Server 2003 с пакетом обновления 1 (SP1) и более поздней версии, Windows Vista, Windows Server 2008 и последующих версиях операционной системы.</span><span class="sxs-lookup"><span data-stu-id="523f7-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="523f7-106">[Модули смарт-карт](/previous-versions/windows/desktop/secsmart/smart-card-modules) предоставляют аналогичные функции.\]</span><span class="sxs-lookup"><span data-stu-id="523f7-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="523f7-107">Метод **креатебитеаррай** создает типичный массив байтов C/C++.</span><span class="sxs-lookup"><span data-stu-id="523f7-107">The **CreateByteArray** method creates a typical C/C++ byte array.</span></span>

## <a name="syntax"></a><span data-ttu-id="523f7-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="523f7-108">Syntax</span></span>


```C++
HRESULT CreateByteArray(
  [in]  DWORD  dwAllocSize,
  [out] LPBYTE *ppbyArray
);
```



## <a name="parameters"></a><span data-ttu-id="523f7-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="523f7-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="523f7-110">*дваллоксизе* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="523f7-110">*dwAllocSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="523f7-111">Размер (в байтах) памяти, выделяемой для массива.</span><span class="sxs-lookup"><span data-stu-id="523f7-111">Size (in bytes) of the memory to be allocated for the array.</span></span>

</dd> <dt>

<span data-ttu-id="523f7-112">*ппбяррай* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="523f7-112">*ppbyArray* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="523f7-113">Указатель на массив байтов, который необходимо вернуть.</span><span class="sxs-lookup"><span data-stu-id="523f7-113">Pointer to the byte array to be returned.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="523f7-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="523f7-114">Return value</span></span>

<span data-ttu-id="523f7-115">Метод возвращает одно из следующих возможных значений:</span><span class="sxs-lookup"><span data-stu-id="523f7-115">The method returns one of the following possible values:</span></span>



| <span data-ttu-id="523f7-116">Код возврата</span><span class="sxs-lookup"><span data-stu-id="523f7-116">Return code</span></span>                                                                                   | <span data-ttu-id="523f7-117">Описание</span><span class="sxs-lookup"><span data-stu-id="523f7-117">Description</span></span>                                                                                      |
|-----------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="523f7-118"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="523f7-118"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="523f7-119">Выделенная память успешно распределена.</span><span class="sxs-lookup"><span data-stu-id="523f7-119">Memory allocated successfully.</span></span><br/>                                                        |
| <dl> <span data-ttu-id="523f7-120"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="523f7-120"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="523f7-121">Возникла проблема с одним или несколькими параметрами, передаваемыми в функцию.</span><span class="sxs-lookup"><span data-stu-id="523f7-121">There is something wrong with one or more of the parameters passed into the function.</span></span><br/> |
| <dl> <span data-ttu-id="523f7-122"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="523f7-122"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="523f7-123">Недостаточно свободной памяти для удовлетворения запроса.</span><span class="sxs-lookup"><span data-stu-id="523f7-123">Not enough free memory to satisfy request.</span></span><br/>                                            |



 

## <a name="remarks"></a><span data-ttu-id="523f7-124">Комментарии</span><span class="sxs-lookup"><span data-stu-id="523f7-124">Remarks</span></span>

<span data-ttu-id="523f7-125">Чтобы создать универсальный буфер байтов, сопоставленный с объектом **IStream** ([**ибитебуффер**](ibytebuffer.md)), вызовите [**креатебитебуффер**](iscardtypeconv-createbytebuffer.md).</span><span class="sxs-lookup"><span data-stu-id="523f7-125">To create a universal buffer of bytes mapped into an **IStream** ([**IByteBuffer**](ibytebuffer.md)) object, call [**CreateByteBuffer**](iscardtypeconv-createbytebuffer.md).</span></span>

<span data-ttu-id="523f7-126">Чтобы создать набор SAFEARRAY автоматизации для неподписанных символов (байт), вызовите [**креатесафеаррай**](iscardtypeconv-createsafearray.md).</span><span class="sxs-lookup"><span data-stu-id="523f7-126">To create an Automation SAFEARRAY of unsigned characters (bytes), call [**CreateSafeArray**](iscardtypeconv-createsafearray.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="523f7-127">Требования</span><span class="sxs-lookup"><span data-stu-id="523f7-127">Requirements</span></span>



| <span data-ttu-id="523f7-128">Требование</span><span class="sxs-lookup"><span data-stu-id="523f7-128">Requirement</span></span> | <span data-ttu-id="523f7-129">Значение</span><span class="sxs-lookup"><span data-stu-id="523f7-129">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="523f7-130">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="523f7-130">Minimum supported client</span></span><br/> | <span data-ttu-id="523f7-131">Только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="523f7-131">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="523f7-132">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="523f7-132">Minimum supported server</span></span><br/> | <span data-ttu-id="523f7-133">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="523f7-133">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="523f7-134">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="523f7-134">End of client support</span></span><br/>    | <span data-ttu-id="523f7-135">Windows XP</span><span class="sxs-lookup"><span data-stu-id="523f7-135">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="523f7-136">Поддержка конца сервера</span><span class="sxs-lookup"><span data-stu-id="523f7-136">End of server support</span></span><br/>    | <span data-ttu-id="523f7-137">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="523f7-137">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="523f7-138">Header</span><span class="sxs-lookup"><span data-stu-id="523f7-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="523f7-139"><dt>Скарддат. h</dt></span><span class="sxs-lookup"><span data-stu-id="523f7-139"><dt>Scarddat.h</dt></span></span> </dl>   |
| <span data-ttu-id="523f7-140">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="523f7-140">Type library</span></span><br/>             | <dl> <span data-ttu-id="523f7-141"><dt>Скарддат. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="523f7-141"><dt>Scarddat.tlb</dt></span></span> </dl> |
| <span data-ttu-id="523f7-142">DLL</span><span class="sxs-lookup"><span data-stu-id="523f7-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="523f7-143"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="523f7-143"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="523f7-144">IID</span><span class="sxs-lookup"><span data-stu-id="523f7-144">IID</span></span><br/>                      | <span data-ttu-id="523f7-145">IID \_ искардтипеконв определен как 53B6AA63-3F56-11D0-916B-00AA00C18068</span><span class="sxs-lookup"><span data-stu-id="523f7-145">IID\_ISCardTypeConv is defined as 53B6AA63-3F56-11D0-916B-00AA00C18068</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="523f7-146">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="523f7-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="523f7-147">**искардтипеконв**</span><span class="sxs-lookup"><span data-stu-id="523f7-147">**ISCardTypeConv**</span></span>](iscardtypeconv.md)
</dt> <dt>

[<span data-ttu-id="523f7-148">Возвращаемые значения смарт-карты</span><span class="sxs-lookup"><span data-stu-id="523f7-148">Smart Card Return Values</span></span>](authentication-return-values.md)
</dt> <dt>

[<span data-ttu-id="523f7-149">**креатебитебуффер**</span><span class="sxs-lookup"><span data-stu-id="523f7-149">**CreateByteBuffer**</span></span>](iscardtypeconv-createbytebuffer.md)
</dt> <dt>

[<span data-ttu-id="523f7-150">**креатесафеаррай**</span><span class="sxs-lookup"><span data-stu-id="523f7-150">**CreateSafeArray**</span></span>](iscardtypeconv-createsafearray.md)
</dt> </dl>

 

 
