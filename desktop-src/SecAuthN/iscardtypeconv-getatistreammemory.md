---
description: Получает указатель на байт для блока памяти ХГЛОБАЛ, управляемого интерфейсом IStream COM.
ms.assetid: ea25eb98-b841-4f5e-b428-3d9cb8176142
title: 'Метод Искардтипеконв:: Жетатистреаммемори (Скарддат. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardTypeConv.GetAtIStreamMemory
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: bdd828921f18c3d06edd2d41da189260a4ed4394
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103808675"
---
# <a name="iscardtypeconvgetatistreammemory-method"></a><span data-ttu-id="eec78-103">Метод Искардтипеконв:: Жетатистреаммемори</span><span class="sxs-lookup"><span data-stu-id="eec78-103">ISCardTypeConv::GetAtIStreamMemory method</span></span>

<span data-ttu-id="eec78-104">\[Метод **жетатистреаммемори** доступен для использования в операционных системах, указанных в разделе требования.</span><span class="sxs-lookup"><span data-stu-id="eec78-104">\[The **GetAtIStreamMemory** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="eec78-105">Он недоступен для использования в Windows Server 2003 с пакетом обновления 1 (SP1) и более поздней версии, Windows Vista, Windows Server 2008 и последующих версиях операционной системы.</span><span class="sxs-lookup"><span data-stu-id="eec78-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="eec78-106">[Модули смарт-карт](/previous-versions/windows/desktop/secsmart/smart-card-modules) предоставляют аналогичные функции.\]</span><span class="sxs-lookup"><span data-stu-id="eec78-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="eec78-107">Метод **жетатистреаммемори** получает указатель на байт для блока памяти хглобал, управляемого интерфейсом **IStream** com.</span><span class="sxs-lookup"><span data-stu-id="eec78-107">The **GetAtIStreamMemory** method acquires a byte pointer to the HGLOBAL memory block that is managed by the **IStream** COM interface.</span></span>

<span data-ttu-id="eec78-108">Это способ получить доступ к памяти в интерфейсе **IStream** без необходимости получения значения sizeof для блока памяти в байтах и считывания байтов во временный массив байтов с помощью интерфейса **IStream** .</span><span class="sxs-lookup"><span data-stu-id="eec78-108">This is a way to get at the memory under the **IStream** without having to get the sizeof value for the memory block in bytes and read the bytes into a temporary byte array using the **IStream** interface.</span></span>

## <a name="syntax"></a><span data-ttu-id="eec78-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="eec78-109">Syntax</span></span>


```C++
HRESULT GetAtIStreamMemory(
  [in]  LPSTREAM    pStrm,
  [out] LPBYTEARRAY *ppMem
);
```



## <a name="parameters"></a><span data-ttu-id="eec78-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="eec78-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="eec78-111">*пстрм* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="eec78-111">*pStrm* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="eec78-112">Указатель на интерфейс **IStream** com, который управляет блоком памяти хглобал.</span><span class="sxs-lookup"><span data-stu-id="eec78-112">A pointer to the **IStream** COM interface that manages the HGLOBAL memory block.</span></span>

</dd> <dt>

<span data-ttu-id="eec78-113">*ппмем* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="eec78-113">*ppMem* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="eec78-114">Указатель на первый байт блока памяти ХГЛОБАЛ в случае успешного выполнения; иначе, **значение NULL** , если операция завершается ошибкой.</span><span class="sxs-lookup"><span data-stu-id="eec78-114">A pointer to the first byte of the HGLOBAL memory block if successful; else, **NULL** if operation fails.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="eec78-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="eec78-115">Return value</span></span>

<span data-ttu-id="eec78-116">Метод возвращает одно из следующих возможных значений.</span><span class="sxs-lookup"><span data-stu-id="eec78-116">The method returns one of the following possible values.</span></span>



| <span data-ttu-id="eec78-117">Код возврата</span><span class="sxs-lookup"><span data-stu-id="eec78-117">Return code</span></span>                                                                                   | <span data-ttu-id="eec78-118">Описание</span><span class="sxs-lookup"><span data-stu-id="eec78-118">Description</span></span>                                                                                      |
|-----------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="eec78-119"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="eec78-119"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="eec78-120">Выделенная память успешно распределена.</span><span class="sxs-lookup"><span data-stu-id="eec78-120">Memory allocated successfully.</span></span><br/>                                                        |
| <dl> <span data-ttu-id="eec78-121"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="eec78-121"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="eec78-122">Возникла проблема с одним или несколькими параметрами, передаваемыми в функцию.</span><span class="sxs-lookup"><span data-stu-id="eec78-122">There is something wrong with one or more of the parameters passed into the function.</span></span><br/> |
| <dl> <span data-ttu-id="eec78-123"><dt>**\_указатель E**</dt></span><span class="sxs-lookup"><span data-stu-id="eec78-123"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="eec78-124">Неверный параметр типа указателя.</span><span class="sxs-lookup"><span data-stu-id="eec78-124">A parameter of pointer type was incorrect.</span></span><br/>                                            |
| <dl> <span data-ttu-id="eec78-125"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="eec78-125"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="eec78-126">Недостаточно свободной памяти для удовлетворения запроса.</span><span class="sxs-lookup"><span data-stu-id="eec78-126">Not enough free memory to satisfy request.</span></span><br/>                                            |



 

## <a name="remarks"></a><span data-ttu-id="eec78-127">Комментарии</span><span class="sxs-lookup"><span data-stu-id="eec78-127">Remarks</span></span>

<span data-ttu-id="eec78-128">Счетчик ссылок **IStream** будет увеличиваться для каждого полученного указателя *ппмем* .</span><span class="sxs-lookup"><span data-stu-id="eec78-128">The **IStream** reference count will be incremented for each *ppMem* pointer acquired.</span></span>

## <a name="requirements"></a><span data-ttu-id="eec78-129">Требования</span><span class="sxs-lookup"><span data-stu-id="eec78-129">Requirements</span></span>



| <span data-ttu-id="eec78-130">Требование</span><span class="sxs-lookup"><span data-stu-id="eec78-130">Requirement</span></span> | <span data-ttu-id="eec78-131">Значение</span><span class="sxs-lookup"><span data-stu-id="eec78-131">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="eec78-132">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="eec78-132">Minimum supported client</span></span><br/> | <span data-ttu-id="eec78-133">Только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="eec78-133">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="eec78-134">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="eec78-134">Minimum supported server</span></span><br/> | <span data-ttu-id="eec78-135">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="eec78-135">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="eec78-136">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="eec78-136">End of client support</span></span><br/>    | <span data-ttu-id="eec78-137">Windows XP</span><span class="sxs-lookup"><span data-stu-id="eec78-137">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="eec78-138">Поддержка конца сервера</span><span class="sxs-lookup"><span data-stu-id="eec78-138">End of server support</span></span><br/>    | <span data-ttu-id="eec78-139">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="eec78-139">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="eec78-140">Header</span><span class="sxs-lookup"><span data-stu-id="eec78-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="eec78-141"><dt>Скарддат. h</dt></span><span class="sxs-lookup"><span data-stu-id="eec78-141"><dt>Scarddat.h</dt></span></span> </dl>   |
| <span data-ttu-id="eec78-142">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="eec78-142">Type library</span></span><br/>             | <dl> <span data-ttu-id="eec78-143"><dt>Скарддат. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="eec78-143"><dt>Scarddat.tlb</dt></span></span> </dl> |
| <span data-ttu-id="eec78-144">DLL</span><span class="sxs-lookup"><span data-stu-id="eec78-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="eec78-145"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="eec78-145"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="eec78-146">IID</span><span class="sxs-lookup"><span data-stu-id="eec78-146">IID</span></span><br/>                      | <span data-ttu-id="eec78-147">IID \_ искардтипеконв определен как 53B6AA63-3F56-11D0-916B-00AA00C18068</span><span class="sxs-lookup"><span data-stu-id="eec78-147">IID\_ISCardTypeConv is defined as 53B6AA63-3F56-11D0-916B-00AA00C18068</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="eec78-148">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="eec78-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="eec78-149">**искардтипеконв**</span><span class="sxs-lookup"><span data-stu-id="eec78-149">**ISCardTypeConv**</span></span>](iscardtypeconv.md)
</dt> <dt>

[<span data-ttu-id="eec78-150">Возвращаемые значения смарт-карты</span><span class="sxs-lookup"><span data-stu-id="eec78-150">Smart Card Return Values</span></span>](authentication-return-values.md)
</dt> </dl>

 

 
