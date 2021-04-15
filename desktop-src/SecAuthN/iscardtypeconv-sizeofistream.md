---
description: Определяет размер (в байтах) интерфейса IStream COM.
ms.assetid: 8c2f081d-cc41-409e-a868-bcf834e1f128
title: 'Метод Искардтипеконв:: Сизеофистреам (Скарддат. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardTypeConv.SizeOfIStream
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 603a01dc6cb4727d59a7fb82c3270c08a495f021
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105647405"
---
# <a name="iscardtypeconvsizeofistream-method"></a><span data-ttu-id="6b294-103">Метод Искардтипеконв:: Сизеофистреам</span><span class="sxs-lookup"><span data-stu-id="6b294-103">ISCardTypeConv::SizeOfIStream method</span></span>

<span data-ttu-id="6b294-104">\[Метод **сизеофистреам** доступен для использования в операционных системах, указанных в разделе требования.</span><span class="sxs-lookup"><span data-stu-id="6b294-104">\[The **SizeOfIStream** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="6b294-105">Он недоступен для использования в Windows Server 2003 с пакетом обновления 1 (SP1) и более поздней версии, Windows Vista, Windows Server 2008 и последующих версиях операционной системы.</span><span class="sxs-lookup"><span data-stu-id="6b294-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="6b294-106">[Модули смарт-карт](/previous-versions/windows/desktop/secsmart/smart-card-modules) предоставляют аналогичные функции.\]</span><span class="sxs-lookup"><span data-stu-id="6b294-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="6b294-107">Метод **сизеофистреам** определяет размер (в байтах) интерфейса **IStream** com.</span><span class="sxs-lookup"><span data-stu-id="6b294-107">The **SizeOfIStream** method determines the size, in bytes, of the **IStream** COM interface.</span></span>

## <a name="syntax"></a><span data-ttu-id="6b294-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="6b294-108">Syntax</span></span>


```C++
HRESULT SizeOfIStream(
  [in]  LPSTREAM       pStrm,
  [out] ULARGE_INTEGER *puliSize
);
```



## <a name="parameters"></a><span data-ttu-id="6b294-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="6b294-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6b294-110">*пстрм* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="6b294-110">*pStrm* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6b294-111">Указатель на интерфейс COM **IStream** .</span><span class="sxs-lookup"><span data-stu-id="6b294-111">A pointer to the **IStream** COM interface.</span></span>

</dd> <dt>

<span data-ttu-id="6b294-112">*пулисизе* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="6b294-112">*puliSize* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6b294-113">Указатель на большое целое число без знака, которое может содержать все 64-битное значение sizeof интерфейса **IStream** com.</span><span class="sxs-lookup"><span data-stu-id="6b294-113">A pointer to the unsigned large integer that can hold the entire 64-bit sizeof value of the **IStream** COM interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6b294-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="6b294-114">Return value</span></span>

<span data-ttu-id="6b294-115">Метод возвращает одно из следующих возможных значений.</span><span class="sxs-lookup"><span data-stu-id="6b294-115">The method returns one of the following possible values.</span></span>



| <span data-ttu-id="6b294-116">Код возврата</span><span class="sxs-lookup"><span data-stu-id="6b294-116">Return code</span></span>                                                                                  | <span data-ttu-id="6b294-117">Описание</span><span class="sxs-lookup"><span data-stu-id="6b294-117">Description</span></span>                                                                                             |
|----------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="6b294-118"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="6b294-118"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="6b294-119">Функция прошла удачно, а *\* пулисизе* — размер (в байтах) интерфейса IStream COM.</span><span class="sxs-lookup"><span data-stu-id="6b294-119">The function succeeded and *\*puliSize* is the size, in bytes, of the IStream COM interface.</span></span><br/> |
| <dl> <span data-ttu-id="6b294-120"><dt>**\_Ошибка E**</dt></span><span class="sxs-lookup"><span data-stu-id="6b294-120"><dt>**E\_FAIL**</dt></span></span> </dl>       | <span data-ttu-id="6b294-121">Произошла неопределенная ошибка.</span><span class="sxs-lookup"><span data-stu-id="6b294-121">Unspecified failure occurred.</span></span><br/>                                                                |
| <dl> <span data-ttu-id="6b294-122"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="6b294-122"><dt>**E\_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="6b294-123">Неверный параметр *пулисизе* .</span><span class="sxs-lookup"><span data-stu-id="6b294-123">The *puliSize* parameter is incorrect.</span></span><br/>                                                       |
| <dl> <span data-ttu-id="6b294-124"><dt>**\_указатель E**</dt></span><span class="sxs-lookup"><span data-stu-id="6b294-124"><dt>**E\_POINTER**</dt></span></span> </dl>    | <span data-ttu-id="6b294-125">Неверный параметр *пстрм* .</span><span class="sxs-lookup"><span data-stu-id="6b294-125">The *pStrm* parameter is incorrect.</span></span><br/>                                                          |
| <dl> <span data-ttu-id="6b294-126"><dt>**\_непредвиденная E**</dt></span><span class="sxs-lookup"><span data-stu-id="6b294-126"><dt>**E\_UNEXPECTED**</dt></span></span> </dl> | <span data-ttu-id="6b294-127">Произошла непредвиденная ошибка.</span><span class="sxs-lookup"><span data-stu-id="6b294-127">Unexpected error occurred.</span></span><br/>                                                                   |



 

## <a name="requirements"></a><span data-ttu-id="6b294-128">Требования</span><span class="sxs-lookup"><span data-stu-id="6b294-128">Requirements</span></span>



| <span data-ttu-id="6b294-129">Требование</span><span class="sxs-lookup"><span data-stu-id="6b294-129">Requirement</span></span> | <span data-ttu-id="6b294-130">Значение</span><span class="sxs-lookup"><span data-stu-id="6b294-130">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="6b294-131">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="6b294-131">Minimum supported client</span></span><br/> | <span data-ttu-id="6b294-132">Только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="6b294-132">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="6b294-133">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="6b294-133">Minimum supported server</span></span><br/> | <span data-ttu-id="6b294-134">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="6b294-134">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="6b294-135">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="6b294-135">End of client support</span></span><br/>    | <span data-ttu-id="6b294-136">Windows XP</span><span class="sxs-lookup"><span data-stu-id="6b294-136">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="6b294-137">Поддержка конца сервера</span><span class="sxs-lookup"><span data-stu-id="6b294-137">End of server support</span></span><br/>    | <span data-ttu-id="6b294-138">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="6b294-138">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="6b294-139">Header</span><span class="sxs-lookup"><span data-stu-id="6b294-139">Header</span></span><br/>                   | <dl> <span data-ttu-id="6b294-140"><dt>Скарддат. h</dt></span><span class="sxs-lookup"><span data-stu-id="6b294-140"><dt>Scarddat.h</dt></span></span> </dl>   |
| <span data-ttu-id="6b294-141">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="6b294-141">Type library</span></span><br/>             | <dl> <span data-ttu-id="6b294-142"><dt>Скарддат. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="6b294-142"><dt>Scarddat.tlb</dt></span></span> </dl> |
| <span data-ttu-id="6b294-143">DLL</span><span class="sxs-lookup"><span data-stu-id="6b294-143">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6b294-144"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6b294-144"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="6b294-145">IID</span><span class="sxs-lookup"><span data-stu-id="6b294-145">IID</span></span><br/>                      | <span data-ttu-id="6b294-146">IID \_ искардтипеконв определен как 53B6AA63-3F56-11D0-916B-00AA00C18068</span><span class="sxs-lookup"><span data-stu-id="6b294-146">IID\_ISCardTypeConv is defined as 53B6AA63-3F56-11D0-916B-00AA00C18068</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="6b294-147">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="6b294-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6b294-148">**искардтипеконв**</span><span class="sxs-lookup"><span data-stu-id="6b294-148">**ISCardTypeConv**</span></span>](iscardtypeconv.md)
</dt> <dt>

[<span data-ttu-id="6b294-149">Возвращаемые значения смарт-карты</span><span class="sxs-lookup"><span data-stu-id="6b294-149">Smart Card Return Values</span></span>](authentication-return-values.md)
</dt> </dl>

 

 
