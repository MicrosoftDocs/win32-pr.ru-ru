---
description: Преобразует универсальный буфер байтов (объект IStream) в массив SAFEARRAY неподписанного char (Byte).
ms.assetid: b8d052e8-2f36-42cf-b88c-ace215a2fc68
title: 'Метод Искардтипеконв:: Конвертбитебуффертосафеаррай (Скарддат. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardTypeConv.ConvertByteBufferToSafeArray
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: eb6f646df60ab505c41c45bea34fd2d59aa3bb4f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103814736"
---
# <a name="iscardtypeconvconvertbytebuffertosafearray-method"></a><span data-ttu-id="dfa41-103">Метод Искардтипеконв:: Конвертбитебуффертосафеаррай</span><span class="sxs-lookup"><span data-stu-id="dfa41-103">ISCardTypeConv::ConvertByteBufferToSafeArray method</span></span>

<span data-ttu-id="dfa41-104">\[Метод **конвертбитебуффертосафеаррай** доступен для использования в операционных системах, указанных в разделе требования.</span><span class="sxs-lookup"><span data-stu-id="dfa41-104">\[The **ConvertByteBufferToSafeArray** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="dfa41-105">Он недоступен для использования в Windows Server 2003 с пакетом обновления 1 (SP1) и более поздней версии, Windows Vista, Windows Server 2008 и последующих версиях операционной системы.</span><span class="sxs-lookup"><span data-stu-id="dfa41-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="dfa41-106">[Модули смарт-карт](/previous-versions/windows/desktop/secsmart/smart-card-modules) предоставляют аналогичные функции.\]</span><span class="sxs-lookup"><span data-stu-id="dfa41-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="dfa41-107">Метод **конвертбитебуффертосафеаррай** преобразует универсальный буфер байтов (объект **ISTREAM** ) в массив SafeArray неподписанного char (Byte).</span><span class="sxs-lookup"><span data-stu-id="dfa41-107">The **ConvertByteBufferToSafeArray** method converts a universal buffer of bytes (**IStream** object) into a SAFEARRAY of unsigned char (byte).</span></span>

## <a name="syntax"></a><span data-ttu-id="dfa41-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="dfa41-108">Syntax</span></span>


```C++
HRESULT ConvertByteBufferToSafeArray(
  [in]  LPBYTEBUFFER pbyBuffer,
  [out] LPSAFEARRAY  *ppbyArray
);
```



## <a name="parameters"></a><span data-ttu-id="dfa41-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="dfa41-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dfa41-110">*пбибуффер* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="dfa41-110">*pbyBuffer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dfa41-111">Указатель на объект **IStream** для преобразования.</span><span class="sxs-lookup"><span data-stu-id="dfa41-111">Pointer to the **IStream** object to be converted.</span></span>

</dd> <dt>

<span data-ttu-id="dfa41-112">*ппбяррай* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="dfa41-112">*ppbyArray* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="dfa41-113">Указатель на массив SAFEARRAY, который должен быть возвращен.</span><span class="sxs-lookup"><span data-stu-id="dfa41-113">Pointer to the SAFEARRAY to be returned.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dfa41-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="dfa41-114">Return value</span></span>

<span data-ttu-id="dfa41-115">Метод возвращает одно из следующих возможных значений:</span><span class="sxs-lookup"><span data-stu-id="dfa41-115">The method returns one of the following possible values:</span></span>



| <span data-ttu-id="dfa41-116">Код возврата</span><span class="sxs-lookup"><span data-stu-id="dfa41-116">Return code</span></span>                                                                                   | <span data-ttu-id="dfa41-117">Описание</span><span class="sxs-lookup"><span data-stu-id="dfa41-117">Description</span></span>                                                                                      |
|-----------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="dfa41-118"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="dfa41-118"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="dfa41-119">Выделенная память успешно распределена.</span><span class="sxs-lookup"><span data-stu-id="dfa41-119">Memory allocated successfully.</span></span><br/>                                                        |
| <dl> <span data-ttu-id="dfa41-120"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="dfa41-120"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="dfa41-121">Возникла проблема с одним или несколькими параметрами, передаваемыми в функцию.</span><span class="sxs-lookup"><span data-stu-id="dfa41-121">There is something wrong with one or more of the parameters passed into the function.</span></span><br/> |
| <dl> <span data-ttu-id="dfa41-122"><dt>**\_указатель E**</dt></span><span class="sxs-lookup"><span data-stu-id="dfa41-122"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="dfa41-123">Неверный параметр типа указателя.</span><span class="sxs-lookup"><span data-stu-id="dfa41-123">A parameter of pointer type was incorrect.</span></span><br/>                                            |
| <dl> <span data-ttu-id="dfa41-124"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="dfa41-124"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="dfa41-125">Недостаточно свободной памяти для удовлетворения запроса.</span><span class="sxs-lookup"><span data-stu-id="dfa41-125">Not enough free memory to satisfy request.</span></span><br/>                                            |



 

## <a name="requirements"></a><span data-ttu-id="dfa41-126">Требования</span><span class="sxs-lookup"><span data-stu-id="dfa41-126">Requirements</span></span>



| <span data-ttu-id="dfa41-127">Требование</span><span class="sxs-lookup"><span data-stu-id="dfa41-127">Requirement</span></span> | <span data-ttu-id="dfa41-128">Значение</span><span class="sxs-lookup"><span data-stu-id="dfa41-128">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="dfa41-129">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="dfa41-129">Minimum supported client</span></span><br/> | <span data-ttu-id="dfa41-130">Только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="dfa41-130">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="dfa41-131">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="dfa41-131">Minimum supported server</span></span><br/> | <span data-ttu-id="dfa41-132">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="dfa41-132">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="dfa41-133">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="dfa41-133">End of client support</span></span><br/>    | <span data-ttu-id="dfa41-134">Windows XP</span><span class="sxs-lookup"><span data-stu-id="dfa41-134">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="dfa41-135">Поддержка конца сервера</span><span class="sxs-lookup"><span data-stu-id="dfa41-135">End of server support</span></span><br/>    | <span data-ttu-id="dfa41-136">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="dfa41-136">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="dfa41-137">Header</span><span class="sxs-lookup"><span data-stu-id="dfa41-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="dfa41-138"><dt>Скарддат. h</dt></span><span class="sxs-lookup"><span data-stu-id="dfa41-138"><dt>Scarddat.h</dt></span></span> </dl>   |
| <span data-ttu-id="dfa41-139">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="dfa41-139">Type library</span></span><br/>             | <dl> <span data-ttu-id="dfa41-140"><dt>Скарддат. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="dfa41-140"><dt>Scarddat.tlb</dt></span></span> </dl> |
| <span data-ttu-id="dfa41-141">DLL</span><span class="sxs-lookup"><span data-stu-id="dfa41-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="dfa41-142"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="dfa41-142"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="dfa41-143">IID</span><span class="sxs-lookup"><span data-stu-id="dfa41-143">IID</span></span><br/>                      | <span data-ttu-id="dfa41-144">IID \_ искардтипеконв определен как 53B6AA63-3F56-11D0-916B-00AA00C18068</span><span class="sxs-lookup"><span data-stu-id="dfa41-144">IID\_ISCardTypeConv is defined as 53B6AA63-3F56-11D0-916B-00AA00C18068</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="dfa41-145">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="dfa41-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dfa41-146">**искардтипеконв**</span><span class="sxs-lookup"><span data-stu-id="dfa41-146">**ISCardTypeConv**</span></span>](iscardtypeconv.md)
</dt> <dt>

[<span data-ttu-id="dfa41-147">Возвращаемые значения смарт-карты</span><span class="sxs-lookup"><span data-stu-id="dfa41-147">Smart Card Return Values</span></span>](authentication-return-values.md)
</dt> </dl>

 

 
