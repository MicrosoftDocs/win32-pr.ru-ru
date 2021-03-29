---
description: Преобразует массив байтов, определенный как SAFEARRAY, в универсальный буфер байтов (объект IStream).
ms.assetid: faa07bb5-cfdb-4181-b86a-f82a9c6b251a
title: 'Метод Искардтипеконв:: Конвертсафеаррайтобитебуффер (Скарддат. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardTypeConv.ConvertSafeArrayToByteBuffer
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: aa6503f474d96e3c25da3f2780ac43976b6507a4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103991062"
---
# <a name="iscardtypeconvconvertsafearraytobytebuffer-method"></a><span data-ttu-id="af7b2-103">Метод Искардтипеконв:: Конвертсафеаррайтобитебуффер</span><span class="sxs-lookup"><span data-stu-id="af7b2-103">ISCardTypeConv::ConvertSafeArrayToByteBuffer method</span></span>

<span data-ttu-id="af7b2-104">\[Метод **конвертсафеаррайтобитебуффер** доступен для использования в операционных системах, указанных в разделе требования.</span><span class="sxs-lookup"><span data-stu-id="af7b2-104">\[The **ConvertSafeArrayToByteBuffer** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="af7b2-105">Он недоступен для использования в Windows Server 2003 с пакетом обновления 1 (SP1) и более поздней версии, Windows Vista, Windows Server 2008 и последующих версиях операционной системы.</span><span class="sxs-lookup"><span data-stu-id="af7b2-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="af7b2-106">[Модули смарт-карт](/previous-versions/windows/desktop/secsmart/smart-card-modules) предоставляют аналогичные функции.\]</span><span class="sxs-lookup"><span data-stu-id="af7b2-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="af7b2-107">Метод **конвертсафеаррайтобитебуффер** преобразует массив байтов, определенный как SAFEARRAY, в универсальный буфер байтов (объект **IStream** ).</span><span class="sxs-lookup"><span data-stu-id="af7b2-107">The **ConvertSafeArrayToByteBuffer** method converts a byte array defined as a SAFEARRAY into a universal buffer of bytes (**IStream** object).</span></span>

<span data-ttu-id="af7b2-108">Созданный буфер байтов — это поток, сопоставленный с блоком памяти.</span><span class="sxs-lookup"><span data-stu-id="af7b2-108">The byte buffer created is a stream mapped over a memory block.</span></span> <span data-ttu-id="af7b2-109">Чтобы получить доступ к буферу или управлять им, используйте методы, предоставляемые интерфейсом **IStream** .</span><span class="sxs-lookup"><span data-stu-id="af7b2-109">To access or manage the buffer, use the methods provided by the **IStream** interface.</span></span> <span data-ttu-id="af7b2-110">Уникальная функция, связанная с реализацией массива, заключается в том, что при вызове метода **IStream:: Release** базовая память будет освобождена.</span><span class="sxs-lookup"><span data-stu-id="af7b2-110">A unique feature about this array implementation is that when you call the **IStream::Release** method, the underlying memory will be released for you.</span></span>

## <a name="syntax"></a><span data-ttu-id="af7b2-111">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="af7b2-111">Syntax</span></span>


```C++
HRESULT ConvertSafeArrayToByteBuffer(
  [in]  LPSAFEARRAY  pbyArray,
  [out] LPBYTEBUFFER *ppbyBuff
);
```



## <a name="parameters"></a><span data-ttu-id="af7b2-112">Параметры</span><span class="sxs-lookup"><span data-stu-id="af7b2-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="af7b2-113">*пбяррай* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="af7b2-113">*pbyArray* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="af7b2-114">Указатель на SAFEARRAY для преобразования.</span><span class="sxs-lookup"><span data-stu-id="af7b2-114">Pointer to the SAFEARRAY to be converted.</span></span>

</dd> <dt>

<span data-ttu-id="af7b2-115">*ппбибуфф* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="af7b2-115">*ppbyBuff* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="af7b2-116">Указатель на возвращаемый объект **IStream** .</span><span class="sxs-lookup"><span data-stu-id="af7b2-116">Pointer to the **IStream** object to be returned.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="af7b2-117">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="af7b2-117">Return value</span></span>

<span data-ttu-id="af7b2-118">Метод возвращает одно из следующих возможных значений:</span><span class="sxs-lookup"><span data-stu-id="af7b2-118">The method returns one of the following possible values:</span></span>



| <span data-ttu-id="af7b2-119">Код возврата</span><span class="sxs-lookup"><span data-stu-id="af7b2-119">Return code</span></span>                                                                                   | <span data-ttu-id="af7b2-120">Описание</span><span class="sxs-lookup"><span data-stu-id="af7b2-120">Description</span></span>                                                                                      |
|-----------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="af7b2-121"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="af7b2-121"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="af7b2-122">Выделенная память успешно распределена.</span><span class="sxs-lookup"><span data-stu-id="af7b2-122">Memory allocated successfully.</span></span><br/>                                                        |
| <dl> <span data-ttu-id="af7b2-123"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="af7b2-123"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="af7b2-124">Возникла проблема с одним или несколькими параметрами, передаваемыми в функцию.</span><span class="sxs-lookup"><span data-stu-id="af7b2-124">There is something wrong with one or more of the parameters passed into the function.</span></span><br/> |
| <dl> <span data-ttu-id="af7b2-125"><dt>**\_указатель E**</dt></span><span class="sxs-lookup"><span data-stu-id="af7b2-125"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="af7b2-126">Неверный параметр типа указателя.</span><span class="sxs-lookup"><span data-stu-id="af7b2-126">A parameter of pointer type was incorrect.</span></span><br/>                                            |
| <dl> <span data-ttu-id="af7b2-127"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="af7b2-127"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="af7b2-128">Недостаточно свободной памяти для удовлетворения запроса.</span><span class="sxs-lookup"><span data-stu-id="af7b2-128">Not enough free memory to satisfy request.</span></span><br/>                                            |



 

## <a name="remarks"></a><span data-ttu-id="af7b2-129">Комментарии</span><span class="sxs-lookup"><span data-stu-id="af7b2-129">Remarks</span></span>

<span data-ttu-id="af7b2-130">Выделенная память является перемещаемой.</span><span class="sxs-lookup"><span data-stu-id="af7b2-130">Memory allocated is moveable.</span></span> <span data-ttu-id="af7b2-131">Чтобы освободить память, используйте метод **IStream:: Release** .</span><span class="sxs-lookup"><span data-stu-id="af7b2-131">Use the **IStream::Release** method to free the memory.</span></span>

## <a name="requirements"></a><span data-ttu-id="af7b2-132">Требования</span><span class="sxs-lookup"><span data-stu-id="af7b2-132">Requirements</span></span>



| <span data-ttu-id="af7b2-133">Требование</span><span class="sxs-lookup"><span data-stu-id="af7b2-133">Requirement</span></span> | <span data-ttu-id="af7b2-134">Значение</span><span class="sxs-lookup"><span data-stu-id="af7b2-134">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="af7b2-135">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="af7b2-135">Minimum supported client</span></span><br/> | <span data-ttu-id="af7b2-136">Только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="af7b2-136">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="af7b2-137">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="af7b2-137">Minimum supported server</span></span><br/> | <span data-ttu-id="af7b2-138">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="af7b2-138">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="af7b2-139">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="af7b2-139">End of client support</span></span><br/>    | <span data-ttu-id="af7b2-140">Windows XP</span><span class="sxs-lookup"><span data-stu-id="af7b2-140">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="af7b2-141">Поддержка конца сервера</span><span class="sxs-lookup"><span data-stu-id="af7b2-141">End of server support</span></span><br/>    | <span data-ttu-id="af7b2-142">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="af7b2-142">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="af7b2-143">Header</span><span class="sxs-lookup"><span data-stu-id="af7b2-143">Header</span></span><br/>                   | <dl> <span data-ttu-id="af7b2-144"><dt>Скарддат. h</dt></span><span class="sxs-lookup"><span data-stu-id="af7b2-144"><dt>Scarddat.h</dt></span></span> </dl>   |
| <span data-ttu-id="af7b2-145">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="af7b2-145">Type library</span></span><br/>             | <dl> <span data-ttu-id="af7b2-146"><dt>Скарддат. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="af7b2-146"><dt>Scarddat.tlb</dt></span></span> </dl> |
| <span data-ttu-id="af7b2-147">DLL</span><span class="sxs-lookup"><span data-stu-id="af7b2-147">DLL</span></span><br/>                      | <dl> <span data-ttu-id="af7b2-148"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="af7b2-148"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="af7b2-149">IID</span><span class="sxs-lookup"><span data-stu-id="af7b2-149">IID</span></span><br/>                      | <span data-ttu-id="af7b2-150">IID \_ искардтипеконв определен как 53B6AA63-3F56-11D0-916B-00AA00C18068</span><span class="sxs-lookup"><span data-stu-id="af7b2-150">IID\_ISCardTypeConv is defined as 53B6AA63-3F56-11D0-916B-00AA00C18068</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="af7b2-151">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="af7b2-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="af7b2-152">**искардтипеконв**</span><span class="sxs-lookup"><span data-stu-id="af7b2-152">**ISCardTypeConv**</span></span>](iscardtypeconv.md)
</dt> <dt>

[<span data-ttu-id="af7b2-153">Возвращаемые значения смарт-карты</span><span class="sxs-lookup"><span data-stu-id="af7b2-153">Smart Card Return Values</span></span>](authentication-return-values.md)
</dt> </dl>

 

 
