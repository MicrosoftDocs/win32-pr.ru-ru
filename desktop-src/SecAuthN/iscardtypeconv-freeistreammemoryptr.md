---
description: Освобождает указатель на байт, указывающий на блок памяти ХГЛОБАЛ, управляемый интерфейсом IStream COM.
ms.assetid: a76c97a9-d0e9-4eb0-9f97-15f22111187d
title: 'Метод Искардтипеконв:: Фриистреаммемориптр (Скарддат. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardTypeConv.FreeIStreamMemoryPtr
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 12912b8130ed6e1ccaa995f88069b59e96f57c09
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103814192"
---
# <a name="iscardtypeconvfreeistreammemoryptr-method"></a><span data-ttu-id="1718f-103">Метод Искардтипеконв:: Фриистреаммемориптр</span><span class="sxs-lookup"><span data-stu-id="1718f-103">ISCardTypeConv::FreeIStreamMemoryPtr method</span></span>

<span data-ttu-id="1718f-104">\[Метод **фриистреаммемориптр** доступен для использования в операционных системах, указанных в разделе требования.</span><span class="sxs-lookup"><span data-stu-id="1718f-104">\[The **FreeIStreamMemoryPtr** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="1718f-105">Он недоступен для использования в Windows Server 2003 с пакетом обновления 1 (SP1) и более поздней версии, Windows Vista, Windows Server 2008 и последующих версиях операционной системы.</span><span class="sxs-lookup"><span data-stu-id="1718f-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="1718f-106">[Модули смарт-карт](/previous-versions/windows/desktop/secsmart/smart-card-modules) предоставляют аналогичные функции.\]</span><span class="sxs-lookup"><span data-stu-id="1718f-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="1718f-107">Метод **фриистреаммемориптр** освобождает указатель на байт, указывающий на блок памяти хглобал, управляемый интерфейсом **IStream** com.</span><span class="sxs-lookup"><span data-stu-id="1718f-107">The **FreeIStreamMemoryPtr** method frees the byte pointer pointing to the HGLOBAL memory block managed by an **IStream** COM interface.</span></span>

## <a name="syntax"></a><span data-ttu-id="1718f-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="1718f-108">Syntax</span></span>


```C++
HRESULT FreeIStreamMemoryPtr(
  [in] LPSTREAM pStrm,
  [in] LPBYTE   pMem
);
```



## <a name="parameters"></a><span data-ttu-id="1718f-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="1718f-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1718f-110">*пстрм* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="1718f-110">*pStrm* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1718f-111">Указатель на интерфейс **IStream** , управляющий блоком памяти, на который указывает *pMem*.</span><span class="sxs-lookup"><span data-stu-id="1718f-111">Pointer to the **IStream** interface that manages the memory block pointed to by *pMem*.</span></span>

</dd> <dt>

<span data-ttu-id="1718f-112">*pMem* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="1718f-112">*pMem* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1718f-113">Указатель на блок памяти, управляемый интерфейсом **IStream** .</span><span class="sxs-lookup"><span data-stu-id="1718f-113">Pointer to the memory block managed by the **IStream** interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1718f-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="1718f-114">Return value</span></span>

<span data-ttu-id="1718f-115">Метод возвращает одно из следующих возможных значений:</span><span class="sxs-lookup"><span data-stu-id="1718f-115">The method returns one of the following possible values:</span></span>



| <span data-ttu-id="1718f-116">Код возврата</span><span class="sxs-lookup"><span data-stu-id="1718f-116">Return code</span></span>                                                                                   | <span data-ttu-id="1718f-117">Описание</span><span class="sxs-lookup"><span data-stu-id="1718f-117">Description</span></span>                                                                                      |
|-----------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="1718f-118"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="1718f-118"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="1718f-119">Выделенная память успешно распределена.</span><span class="sxs-lookup"><span data-stu-id="1718f-119">Memory allocated successfully.</span></span><br/>                                                        |
| <dl> <span data-ttu-id="1718f-120"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="1718f-120"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="1718f-121">Возникла проблема с одним или несколькими параметрами, передаваемыми в функцию.</span><span class="sxs-lookup"><span data-stu-id="1718f-121">There is something wrong with one or more of the parameters passed into the function.</span></span><br/> |
| <dl> <span data-ttu-id="1718f-122"><dt>**\_указатель E**</dt></span><span class="sxs-lookup"><span data-stu-id="1718f-122"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="1718f-123">Неверный параметр типа указателя.</span><span class="sxs-lookup"><span data-stu-id="1718f-123">A parameter of pointer type was incorrect.</span></span><br/>                                            |
| <dl> <span data-ttu-id="1718f-124"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="1718f-124"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="1718f-125">Недостаточно свободной памяти для удовлетворения запроса.</span><span class="sxs-lookup"><span data-stu-id="1718f-125">Not enough free memory to satisfy request.</span></span><br/>                                            |



 

## <a name="remarks"></a><span data-ttu-id="1718f-126">Комментарии</span><span class="sxs-lookup"><span data-stu-id="1718f-126">Remarks</span></span>

<span data-ttu-id="1718f-127">Эта функция полностью и четко освобождает указатель на байт, указывающий на блок памяти ХГЛОБАЛ, управляемый интерфейсом **IStream** .</span><span class="sxs-lookup"><span data-stu-id="1718f-127">This function completely and cleanly releases the byte pointer pointing to the HGLOBAL memory block managed by the **IStream** interface.</span></span> <span data-ttu-id="1718f-128">Указатель байтов запрашивается при вызове [**жетатистреаммемори**](iscardtypeconv-getatistreammemory.md).</span><span class="sxs-lookup"><span data-stu-id="1718f-128">The byte pointer is acquired by a call to [**GetAtIStreamMemory**](iscardtypeconv-getatistreammemory.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="1718f-129">Требования</span><span class="sxs-lookup"><span data-stu-id="1718f-129">Requirements</span></span>



| <span data-ttu-id="1718f-130">Требование</span><span class="sxs-lookup"><span data-stu-id="1718f-130">Requirement</span></span> | <span data-ttu-id="1718f-131">Значение</span><span class="sxs-lookup"><span data-stu-id="1718f-131">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="1718f-132">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="1718f-132">Minimum supported client</span></span><br/> | <span data-ttu-id="1718f-133">Только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="1718f-133">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="1718f-134">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="1718f-134">Minimum supported server</span></span><br/> | <span data-ttu-id="1718f-135">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="1718f-135">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="1718f-136">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="1718f-136">End of client support</span></span><br/>    | <span data-ttu-id="1718f-137">Windows XP</span><span class="sxs-lookup"><span data-stu-id="1718f-137">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="1718f-138">Поддержка конца сервера</span><span class="sxs-lookup"><span data-stu-id="1718f-138">End of server support</span></span><br/>    | <span data-ttu-id="1718f-139">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="1718f-139">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="1718f-140">Header</span><span class="sxs-lookup"><span data-stu-id="1718f-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="1718f-141"><dt>Скарддат. h</dt></span><span class="sxs-lookup"><span data-stu-id="1718f-141"><dt>Scarddat.h</dt></span></span> </dl>   |
| <span data-ttu-id="1718f-142">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="1718f-142">Type library</span></span><br/>             | <dl> <span data-ttu-id="1718f-143"><dt>Скарддат. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="1718f-143"><dt>Scarddat.tlb</dt></span></span> </dl> |
| <span data-ttu-id="1718f-144">DLL</span><span class="sxs-lookup"><span data-stu-id="1718f-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1718f-145"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1718f-145"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="1718f-146">IID</span><span class="sxs-lookup"><span data-stu-id="1718f-146">IID</span></span><br/>                      | <span data-ttu-id="1718f-147">IID \_ искардтипеконв определен как 53B6AA63-3F56-11D0-916B-00AA00C18068</span><span class="sxs-lookup"><span data-stu-id="1718f-147">IID\_ISCardTypeConv is defined as 53B6AA63-3F56-11D0-916B-00AA00C18068</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="1718f-148">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="1718f-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1718f-149">**искардтипеконв**</span><span class="sxs-lookup"><span data-stu-id="1718f-149">**ISCardTypeConv**</span></span>](iscardtypeconv.md)
</dt> <dt>

[<span data-ttu-id="1718f-150">Возвращаемые значения смарт-карты</span><span class="sxs-lookup"><span data-stu-id="1718f-150">Smart Card Return Values</span></span>](authentication-return-values.md)
</dt> <dt>

[<span data-ttu-id="1718f-151">**жетатистреаммемори**</span><span class="sxs-lookup"><span data-stu-id="1718f-151">**GetAtIStreamMemory**</span></span>](iscardtypeconv-getatistreammemory.md)
</dt> </dl>

 

 
