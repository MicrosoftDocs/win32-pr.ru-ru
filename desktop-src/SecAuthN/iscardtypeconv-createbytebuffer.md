---
description: Создает универсальный буфер байтов, сопоставленный с объектом IStream (Ибитебуффер).
ms.assetid: 8015c7e8-2cbb-4ba8-9bd0-2f84751840f1
title: 'Метод Искардтипеконв:: Креатебитебуффер (Скарддат. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardTypeConv.CreateByteBuffer
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: ab69c8061d2e2740e652e29b2fe6407574fe7076
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104080851"
---
# <a name="iscardtypeconvcreatebytebuffer-method"></a><span data-ttu-id="b2ad7-103">Метод Искардтипеконв:: Креатебитебуффер</span><span class="sxs-lookup"><span data-stu-id="b2ad7-103">ISCardTypeConv::CreateByteBuffer method</span></span>

<span data-ttu-id="b2ad7-104">\[Метод **креатебитебуффер** доступен для использования в операционных системах, указанных в разделе требования.</span><span class="sxs-lookup"><span data-stu-id="b2ad7-104">\[The **CreateByteBuffer** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="b2ad7-105">Он недоступен для использования в Windows Server 2003 с пакетом обновления 1 (SP1) и более поздней версии, Windows Vista, Windows Server 2008 и последующих версиях операционной системы.</span><span class="sxs-lookup"><span data-stu-id="b2ad7-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="b2ad7-106">[Модули смарт-карт](/previous-versions/windows/desktop/secsmart/smart-card-modules) предоставляют аналогичные функции.\]</span><span class="sxs-lookup"><span data-stu-id="b2ad7-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="b2ad7-107">Метод **креатебитебуффер** создает универсальный буфер байтов, сопоставленный с объектом **IStream** ([**ибитебуффер**](ibytebuffer.md)).</span><span class="sxs-lookup"><span data-stu-id="b2ad7-107">The **CreateByteBuffer** method creates a universal buffer of bytes mapped into an **IStream** ([**IByteBuffer**](ibytebuffer.md)) object.</span></span>

<span data-ttu-id="b2ad7-108">Созданный буфер байтов — это поток, сопоставленный с блоком памяти.</span><span class="sxs-lookup"><span data-stu-id="b2ad7-108">The byte buffer created is a stream mapped over a memory block.</span></span> <span data-ttu-id="b2ad7-109">Чтобы получить доступ к буферу или управлять им, используйте методы, предоставляемые интерфейсом **IStream** .</span><span class="sxs-lookup"><span data-stu-id="b2ad7-109">To access or manage the buffer, use the methods provided by the **IStream** interface.</span></span> <span data-ttu-id="b2ad7-110">Уникальная функция, связанная с реализацией массива, заключается в том, что при вызове метода **IStream:: Release** базовая память будет освобождена.</span><span class="sxs-lookup"><span data-stu-id="b2ad7-110">A unique feature about this array implementation is that when you call the **IStream::Release** method, the underlying memory will be released for you.</span></span>

## <a name="syntax"></a><span data-ttu-id="b2ad7-111">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="b2ad7-111">Syntax</span></span>


```C++
HRESULT CreateByteBuffer(
  [in]  DWORD        dwAllocSize,
  [out] LPBYTEBUFFER *ppbyBuff
);
```



## <a name="parameters"></a><span data-ttu-id="b2ad7-112">Параметры</span><span class="sxs-lookup"><span data-stu-id="b2ad7-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b2ad7-113">*дваллоксизе* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="b2ad7-113">*dwAllocSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b2ad7-114">Размер в байтах памяти, выделяемой для массива.</span><span class="sxs-lookup"><span data-stu-id="b2ad7-114">Size in bytes of the memory to be allocated for the array.</span></span>

</dd> <dt>

<span data-ttu-id="b2ad7-115">*ппбибуфф* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="b2ad7-115">*ppbyBuff* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b2ad7-116">Указатель на возвращаемый объект IStream.</span><span class="sxs-lookup"><span data-stu-id="b2ad7-116">Pointer to the IStream object to be returned.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b2ad7-117">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="b2ad7-117">Return value</span></span>

<span data-ttu-id="b2ad7-118">Возможны следующие возвращаемые значения:</span><span class="sxs-lookup"><span data-stu-id="b2ad7-118">The possible return values are the following:</span></span>



| <span data-ttu-id="b2ad7-119">Код возврата</span><span class="sxs-lookup"><span data-stu-id="b2ad7-119">Return code</span></span>                                                                                   | <span data-ttu-id="b2ad7-120">Описание</span><span class="sxs-lookup"><span data-stu-id="b2ad7-120">Description</span></span>                                                                                      |
|-----------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="b2ad7-121"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="b2ad7-121"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="b2ad7-122">Выделенная память успешно распределена.</span><span class="sxs-lookup"><span data-stu-id="b2ad7-122">Memory allocated successfully.</span></span><br/>                                                        |
| <dl> <span data-ttu-id="b2ad7-123"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="b2ad7-123"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="b2ad7-124">Возникла проблема с одним или несколькими параметрами, передаваемыми в функцию.</span><span class="sxs-lookup"><span data-stu-id="b2ad7-124">There is something wrong with one or more of the parameters passed into the function.</span></span><br/> |
| <dl> <span data-ttu-id="b2ad7-125"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="b2ad7-125"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="b2ad7-126">Недостаточно свободной памяти для удовлетворения запроса.</span><span class="sxs-lookup"><span data-stu-id="b2ad7-126">Not enough free memory to satisfy request.</span></span><br/>                                            |



 

## <a name="remarks"></a><span data-ttu-id="b2ad7-127">Комментарии</span><span class="sxs-lookup"><span data-stu-id="b2ad7-127">Remarks</span></span>

<span data-ttu-id="b2ad7-128">Выделенная память является перемещаемой.</span><span class="sxs-lookup"><span data-stu-id="b2ad7-128">Memory allocated is movable.</span></span> <span data-ttu-id="b2ad7-129">Чтобы освободить память, используйте метод **IStream:: Release** .</span><span class="sxs-lookup"><span data-stu-id="b2ad7-129">Use the **IStream::Release** method to free the memory.</span></span>

<span data-ttu-id="b2ad7-130">Чтобы создать типичный массив байтов C/C++, вызовите [**креатебитеаррай**](iscardtypeconv-createbytearray.md).</span><span class="sxs-lookup"><span data-stu-id="b2ad7-130">To create a typical C/C++ byte array, call [**CreateByteArray**](iscardtypeconv-createbytearray.md).</span></span>

<span data-ttu-id="b2ad7-131">Чтобы создать набор SAFEARRAY автоматизации для неподписанных символов (байт), вызовите [**креатесафеаррай**](iscardtypeconv-createsafearray.md).</span><span class="sxs-lookup"><span data-stu-id="b2ad7-131">To create an Automation SAFEARRAY of unsigned characters (bytes), call [**CreateSafeArray**](iscardtypeconv-createsafearray.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="b2ad7-132">Требования</span><span class="sxs-lookup"><span data-stu-id="b2ad7-132">Requirements</span></span>



| <span data-ttu-id="b2ad7-133">Требование</span><span class="sxs-lookup"><span data-stu-id="b2ad7-133">Requirement</span></span> | <span data-ttu-id="b2ad7-134">Значение</span><span class="sxs-lookup"><span data-stu-id="b2ad7-134">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b2ad7-135">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="b2ad7-135">Minimum supported client</span></span><br/> | <span data-ttu-id="b2ad7-136">Только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="b2ad7-136">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="b2ad7-137">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="b2ad7-137">Minimum supported server</span></span><br/> | <span data-ttu-id="b2ad7-138">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="b2ad7-138">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="b2ad7-139">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="b2ad7-139">End of client support</span></span><br/>    | <span data-ttu-id="b2ad7-140">Windows XP</span><span class="sxs-lookup"><span data-stu-id="b2ad7-140">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="b2ad7-141">Поддержка конца сервера</span><span class="sxs-lookup"><span data-stu-id="b2ad7-141">End of server support</span></span><br/>    | <span data-ttu-id="b2ad7-142">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="b2ad7-142">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="b2ad7-143">Header</span><span class="sxs-lookup"><span data-stu-id="b2ad7-143">Header</span></span><br/>                   | <dl> <span data-ttu-id="b2ad7-144"><dt>Скарддат. h</dt></span><span class="sxs-lookup"><span data-stu-id="b2ad7-144"><dt>Scarddat.h</dt></span></span> </dl>   |
| <span data-ttu-id="b2ad7-145">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="b2ad7-145">Type library</span></span><br/>             | <dl> <span data-ttu-id="b2ad7-146"><dt>Скарддат. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="b2ad7-146"><dt>Scarddat.tlb</dt></span></span> </dl> |
| <span data-ttu-id="b2ad7-147">DLL</span><span class="sxs-lookup"><span data-stu-id="b2ad7-147">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b2ad7-148"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b2ad7-148"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="b2ad7-149">IID</span><span class="sxs-lookup"><span data-stu-id="b2ad7-149">IID</span></span><br/>                      | <span data-ttu-id="b2ad7-150">IID \_ искардтипеконв определен как 53B6AA63-3F56-11D0-916B-00AA00C18068</span><span class="sxs-lookup"><span data-stu-id="b2ad7-150">IID\_ISCardTypeConv is defined as 53B6AA63-3F56-11D0-916B-00AA00C18068</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="b2ad7-151">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="b2ad7-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b2ad7-152">**искардтипеконв**</span><span class="sxs-lookup"><span data-stu-id="b2ad7-152">**ISCardTypeConv**</span></span>](iscardtypeconv.md)
</dt> <dt>

[<span data-ttu-id="b2ad7-153">Возвращаемые значения смарт-карты</span><span class="sxs-lookup"><span data-stu-id="b2ad7-153">Smart Card Return Values</span></span>](authentication-return-values.md)
</dt> <dt>

[<span data-ttu-id="b2ad7-154">**креатебитеаррай**</span><span class="sxs-lookup"><span data-stu-id="b2ad7-154">**CreateByteArray**</span></span>](iscardtypeconv-createbytearray.md)
</dt> <dt>

[<span data-ttu-id="b2ad7-155">**креатесафеаррай**</span><span class="sxs-lookup"><span data-stu-id="b2ad7-155">**CreateSafeArray**</span></span>](iscardtypeconv-createsafearray.md)
</dt> </dl>

 

 
