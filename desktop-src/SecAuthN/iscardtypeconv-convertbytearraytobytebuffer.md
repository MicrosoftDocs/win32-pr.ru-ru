---
description: Преобразует стандартный массив байтов C/C++ в универсальный буфер байтов (объект IStream).
ms.assetid: 512c561a-63f1-463e-9bae-9bec1ebdbe9b
title: 'Метод Искардтипеконв:: Конвертбитеаррайтобитебуффер (Скарддат. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardTypeConv.ConvertByteArrayToByteBuffer
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 406e7aecb7e86802ad67c07669ca199b158ad954
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103912456"
---
# <a name="iscardtypeconvconvertbytearraytobytebuffer-method"></a><span data-ttu-id="cf83f-103">Метод Искардтипеконв:: Конвертбитеаррайтобитебуффер</span><span class="sxs-lookup"><span data-stu-id="cf83f-103">ISCardTypeConv::ConvertByteArrayToByteBuffer method</span></span>

<span data-ttu-id="cf83f-104">\[Метод **конвертбитеаррайтобитебуффер** доступен для использования в операционных системах, указанных в разделе требования.</span><span class="sxs-lookup"><span data-stu-id="cf83f-104">\[The **ConvertByteArrayToByteBuffer** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="cf83f-105">Он недоступен для использования в Windows Server 2003 с пакетом обновления 1 (SP1) и более поздней версии, Windows Vista, Windows Server 2008 и последующих версиях операционной системы.</span><span class="sxs-lookup"><span data-stu-id="cf83f-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="cf83f-106">[Модули смарт-карт](/previous-versions/windows/desktop/secsmart/smart-card-modules) предоставляют аналогичные функции.\]</span><span class="sxs-lookup"><span data-stu-id="cf83f-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="cf83f-107">Метод **конвертбитеаррайтобитебуффер** преобразует стандартный массив байтов C/C++ в универсальный буфер байтов (объект **IStream** ).</span><span class="sxs-lookup"><span data-stu-id="cf83f-107">The **ConvertByteArrayToByteBuffer** method converts a typical C/C++ byte array into a universal buffer of bytes (**IStream** object).</span></span>

<span data-ttu-id="cf83f-108">Созданный буфер байтов — это поток, сопоставленный с блоком памяти.</span><span class="sxs-lookup"><span data-stu-id="cf83f-108">The byte buffer created is a stream mapped over a memory block.</span></span> <span data-ttu-id="cf83f-109">Чтобы получить доступ к буферу или управлять им, используйте методы, предоставляемые интерфейсом **IStream** .</span><span class="sxs-lookup"><span data-stu-id="cf83f-109">To access or manage the buffer, use the methods provided by the **IStream** interface.</span></span> <span data-ttu-id="cf83f-110">Уникальная функция, связанная с реализацией массива, заключается в том, что при вызове метода **IStream:: Release** базовая память будет освобождена.</span><span class="sxs-lookup"><span data-stu-id="cf83f-110">A unique feature about this array implementation is that when you call the **IStream::Release** method, the underlying memory will be released for you.</span></span>

## <a name="syntax"></a><span data-ttu-id="cf83f-111">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="cf83f-111">Syntax</span></span>


```C++
HRESULT ConvertByteArrayToByteBuffer(
  [in]  LPBYTE       pbyArray,
  [in]  DWORD        dwArraySize,
  [out] LPBYTEBUFFER *ppbyBuffer
);
```



## <a name="parameters"></a><span data-ttu-id="cf83f-112">Параметры</span><span class="sxs-lookup"><span data-stu-id="cf83f-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cf83f-113">*пбяррай* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="cf83f-113">*pbyArray* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cf83f-114">Указатель на массив байтов для преобразования.</span><span class="sxs-lookup"><span data-stu-id="cf83f-114">Pointer to the array of bytes to be converted.</span></span>

</dd> <dt>

<span data-ttu-id="cf83f-115">*дваррайсизе* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="cf83f-115">*dwArraySize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cf83f-116">Размер преобразуемого массива байтов.</span><span class="sxs-lookup"><span data-stu-id="cf83f-116">Size of the byte array to be converted.</span></span>

</dd> <dt>

<span data-ttu-id="cf83f-117">*ппбибуффер* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="cf83f-117">*ppbyBuffer* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="cf83f-118">Указатель на возвращаемый объект **IStream** .</span><span class="sxs-lookup"><span data-stu-id="cf83f-118">Pointer to the **IStream** object to be returned.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cf83f-119">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="cf83f-119">Return value</span></span>

<span data-ttu-id="cf83f-120">Метод возвращает одно из следующих возможных значений:</span><span class="sxs-lookup"><span data-stu-id="cf83f-120">The method returns one of the following possible values:</span></span>



| <span data-ttu-id="cf83f-121">Код возврата</span><span class="sxs-lookup"><span data-stu-id="cf83f-121">Return code</span></span>                                                                                   | <span data-ttu-id="cf83f-122">Описание</span><span class="sxs-lookup"><span data-stu-id="cf83f-122">Description</span></span>                                                                                      |
|-----------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="cf83f-123"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="cf83f-123"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="cf83f-124">Выделенная память успешно распределена.</span><span class="sxs-lookup"><span data-stu-id="cf83f-124">Memory allocated successfully.</span></span><br/>                                                        |
| <dl> <span data-ttu-id="cf83f-125"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="cf83f-125"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="cf83f-126">Возникла проблема с одним или несколькими параметрами, передаваемыми в функцию.</span><span class="sxs-lookup"><span data-stu-id="cf83f-126">There is something wrong with one or more of the parameters passed into the function.</span></span><br/> |
| <dl> <span data-ttu-id="cf83f-127"><dt>**\_указатель E**</dt></span><span class="sxs-lookup"><span data-stu-id="cf83f-127"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="cf83f-128">Неверный параметр типа указателя.</span><span class="sxs-lookup"><span data-stu-id="cf83f-128">A parameter of pointer type was incorrect.</span></span><br/>                                            |
| <dl> <span data-ttu-id="cf83f-129"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="cf83f-129"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="cf83f-130">Недостаточно свободной памяти для удовлетворения запроса.</span><span class="sxs-lookup"><span data-stu-id="cf83f-130">Not enough free memory to satisfy request.</span></span><br/>                                            |



 

## <a name="remarks"></a><span data-ttu-id="cf83f-131">Комментарии</span><span class="sxs-lookup"><span data-stu-id="cf83f-131">Remarks</span></span>

<span data-ttu-id="cf83f-132">Выделенная память является перемещаемой.</span><span class="sxs-lookup"><span data-stu-id="cf83f-132">Memory allocated is movable.</span></span> <span data-ttu-id="cf83f-133">Чтобы освободить память, используйте метод **IStream:: Release** .</span><span class="sxs-lookup"><span data-stu-id="cf83f-133">Use the **IStream::Release** method to free the memory.</span></span>

## <a name="requirements"></a><span data-ttu-id="cf83f-134">Требования</span><span class="sxs-lookup"><span data-stu-id="cf83f-134">Requirements</span></span>



| <span data-ttu-id="cf83f-135">Требование</span><span class="sxs-lookup"><span data-stu-id="cf83f-135">Requirement</span></span> | <span data-ttu-id="cf83f-136">Значение</span><span class="sxs-lookup"><span data-stu-id="cf83f-136">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="cf83f-137">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="cf83f-137">Minimum supported client</span></span><br/> | <span data-ttu-id="cf83f-138">Только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="cf83f-138">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="cf83f-139">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="cf83f-139">Minimum supported server</span></span><br/> | <span data-ttu-id="cf83f-140">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="cf83f-140">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="cf83f-141">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="cf83f-141">End of client support</span></span><br/>    | <span data-ttu-id="cf83f-142">Windows XP</span><span class="sxs-lookup"><span data-stu-id="cf83f-142">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="cf83f-143">Поддержка конца сервера</span><span class="sxs-lookup"><span data-stu-id="cf83f-143">End of server support</span></span><br/>    | <span data-ttu-id="cf83f-144">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="cf83f-144">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="cf83f-145">Header</span><span class="sxs-lookup"><span data-stu-id="cf83f-145">Header</span></span><br/>                   | <dl> <span data-ttu-id="cf83f-146"><dt>Скарддат. h</dt></span><span class="sxs-lookup"><span data-stu-id="cf83f-146"><dt>Scarddat.h</dt></span></span> </dl>   |
| <span data-ttu-id="cf83f-147">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="cf83f-147">Type library</span></span><br/>             | <dl> <span data-ttu-id="cf83f-148"><dt>Скарддат. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="cf83f-148"><dt>Scarddat.tlb</dt></span></span> </dl> |
| <span data-ttu-id="cf83f-149">DLL</span><span class="sxs-lookup"><span data-stu-id="cf83f-149">DLL</span></span><br/>                      | <dl> <span data-ttu-id="cf83f-150"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="cf83f-150"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="cf83f-151">IID</span><span class="sxs-lookup"><span data-stu-id="cf83f-151">IID</span></span><br/>                      | <span data-ttu-id="cf83f-152">IID \_ искардтипеконв определен как 53B6AA63-3F56-11D0-916B-00AA00C18068</span><span class="sxs-lookup"><span data-stu-id="cf83f-152">IID\_ISCardTypeConv is defined as 53B6AA63-3F56-11D0-916B-00AA00C18068</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="cf83f-153">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="cf83f-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cf83f-154">**искардтипеконв**</span><span class="sxs-lookup"><span data-stu-id="cf83f-154">**ISCardTypeConv**</span></span>](iscardtypeconv.md)
</dt> <dt>

[<span data-ttu-id="cf83f-155">Возвращаемые значения смарт-карты</span><span class="sxs-lookup"><span data-stu-id="cf83f-155">Smart Card Return Values</span></span>](authentication-return-values.md)
</dt> </dl>

 

 
