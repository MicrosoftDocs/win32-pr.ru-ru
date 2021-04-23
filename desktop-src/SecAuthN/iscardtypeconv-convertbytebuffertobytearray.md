---
description: Преобразует универсальный буфер байтов (объект IStream) в типичный массив байтов C/C++.
ms.assetid: f5b14096-d848-4de9-a5c3-bb60af9044a2
title: 'Метод Искардтипеконв:: Конвертбитебуффертобитеаррай (Скарддат. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardTypeConv.ConvertByteBufferToByteArray
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 7eed6758373aebf08863669b5b81909fca1c0840
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104265939"
---
# <a name="iscardtypeconvconvertbytebuffertobytearray-method"></a><span data-ttu-id="fdbda-103">Метод Искардтипеконв:: Конвертбитебуффертобитеаррай</span><span class="sxs-lookup"><span data-stu-id="fdbda-103">ISCardTypeConv::ConvertByteBufferToByteArray method</span></span>

<span data-ttu-id="fdbda-104">\[Метод **конвертбитебуффертобитеаррай** доступен для использования в операционных системах, указанных в разделе требования.</span><span class="sxs-lookup"><span data-stu-id="fdbda-104">\[The **ConvertByteBufferToByteArray** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="fdbda-105">Он недоступен для использования в Windows Server 2003 с пакетом обновления 1 (SP1) и более поздней версии, Windows Vista, Windows Server 2008 и последующих версиях операционной системы.</span><span class="sxs-lookup"><span data-stu-id="fdbda-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="fdbda-106">[Модули смарт-карт](/previous-versions/windows/desktop/secsmart/smart-card-modules) предоставляют аналогичные функции.\]</span><span class="sxs-lookup"><span data-stu-id="fdbda-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="fdbda-107">Метод **конвертбитебуффертобитеаррай** преобразует универсальный буфер байтов (объект **IStream** ) в типичный массив байтов C/C++.</span><span class="sxs-lookup"><span data-stu-id="fdbda-107">The **ConvertByteBufferToByteArray** method converts a universal buffer of bytes (**IStream** object) into a typical C/C++ byte array.</span></span>

## <a name="syntax"></a><span data-ttu-id="fdbda-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="fdbda-108">Syntax</span></span>


```C++
HRESULT ConvertByteBufferToByteArray(
  [in]  LPBYTEBUFFER pbyBuffer,
  [out] LPBYTEARRAY  *ppArray
);
```



## <a name="parameters"></a><span data-ttu-id="fdbda-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="fdbda-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fdbda-110">*пбибуффер* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="fdbda-110">*pbyBuffer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fdbda-111">Указатель на объект **IStream** для преобразования.</span><span class="sxs-lookup"><span data-stu-id="fdbda-111">Pointer to the **IStream** object to be converted.</span></span>

</dd> <dt>

<span data-ttu-id="fdbda-112">*ппаррай* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="fdbda-112">*ppArray* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="fdbda-113">Указатель на массив байтов, который необходимо вернуть.</span><span class="sxs-lookup"><span data-stu-id="fdbda-113">Pointer to the array of bytes to be returned.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fdbda-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="fdbda-114">Return value</span></span>

<span data-ttu-id="fdbda-115">Метод возвращает одно из следующих возможных значений:</span><span class="sxs-lookup"><span data-stu-id="fdbda-115">The method returns one of the following possible values:</span></span>



| <span data-ttu-id="fdbda-116">Код возврата</span><span class="sxs-lookup"><span data-stu-id="fdbda-116">Return code</span></span>                                                                                   | <span data-ttu-id="fdbda-117">Описание</span><span class="sxs-lookup"><span data-stu-id="fdbda-117">Description</span></span>                                                                                      |
|-----------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="fdbda-118"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="fdbda-118"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="fdbda-119">Выделенная память успешно распределена.</span><span class="sxs-lookup"><span data-stu-id="fdbda-119">Memory allocated successfully.</span></span><br/>                                                        |
| <dl> <span data-ttu-id="fdbda-120"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="fdbda-120"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="fdbda-121">Возникла проблема с одним или несколькими параметрами, передаваемыми в функцию.</span><span class="sxs-lookup"><span data-stu-id="fdbda-121">There is something wrong with one or more of the parameters passed into the function.</span></span><br/> |
| <dl> <span data-ttu-id="fdbda-122"><dt>**\_указатель E**</dt></span><span class="sxs-lookup"><span data-stu-id="fdbda-122"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="fdbda-123">Неверный параметр типа указателя.</span><span class="sxs-lookup"><span data-stu-id="fdbda-123">A parameter of pointer type was incorrect.</span></span><br/>                                            |
| <dl> <span data-ttu-id="fdbda-124"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="fdbda-124"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="fdbda-125">Недостаточно свободной памяти для удовлетворения запроса.</span><span class="sxs-lookup"><span data-stu-id="fdbda-125">Not enough free memory to satisfy request.</span></span><br/>                                            |



 

## <a name="requirements"></a><span data-ttu-id="fdbda-126">Требования</span><span class="sxs-lookup"><span data-stu-id="fdbda-126">Requirements</span></span>



| <span data-ttu-id="fdbda-127">Требование</span><span class="sxs-lookup"><span data-stu-id="fdbda-127">Requirement</span></span> | <span data-ttu-id="fdbda-128">Значение</span><span class="sxs-lookup"><span data-stu-id="fdbda-128">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="fdbda-129">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="fdbda-129">Minimum supported client</span></span><br/> | <span data-ttu-id="fdbda-130">Только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="fdbda-130">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="fdbda-131">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="fdbda-131">Minimum supported server</span></span><br/> | <span data-ttu-id="fdbda-132">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="fdbda-132">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="fdbda-133">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="fdbda-133">End of client support</span></span><br/>    | <span data-ttu-id="fdbda-134">Windows XP</span><span class="sxs-lookup"><span data-stu-id="fdbda-134">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="fdbda-135">Поддержка конца сервера</span><span class="sxs-lookup"><span data-stu-id="fdbda-135">End of server support</span></span><br/>    | <span data-ttu-id="fdbda-136">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="fdbda-136">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="fdbda-137">Header</span><span class="sxs-lookup"><span data-stu-id="fdbda-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="fdbda-138"><dt>Скарддат. h</dt></span><span class="sxs-lookup"><span data-stu-id="fdbda-138"><dt>Scarddat.h</dt></span></span> </dl>   |
| <span data-ttu-id="fdbda-139">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="fdbda-139">Type library</span></span><br/>             | <dl> <span data-ttu-id="fdbda-140"><dt>Скарддат. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="fdbda-140"><dt>Scarddat.tlb</dt></span></span> </dl> |
| <span data-ttu-id="fdbda-141">DLL</span><span class="sxs-lookup"><span data-stu-id="fdbda-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fdbda-142"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fdbda-142"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="fdbda-143">IID</span><span class="sxs-lookup"><span data-stu-id="fdbda-143">IID</span></span><br/>                      | <span data-ttu-id="fdbda-144">IID \_ искардтипеконв определен как 53B6AA63-3F56-11D0-916B-00AA00C18068</span><span class="sxs-lookup"><span data-stu-id="fdbda-144">IID\_ISCardTypeConv is defined as 53B6AA63-3F56-11D0-916B-00AA00C18068</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="fdbda-145">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="fdbda-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fdbda-146">**искардтипеконв**</span><span class="sxs-lookup"><span data-stu-id="fdbda-146">**ISCardTypeConv**</span></span>](iscardtypeconv.md)
</dt> <dt>

[<span data-ttu-id="fdbda-147">Возвращаемые значения смарт-карты</span><span class="sxs-lookup"><span data-stu-id="fdbda-147">Smart Card Return Values</span></span>](authentication-return-values.md)
</dt> </dl>

 

 
