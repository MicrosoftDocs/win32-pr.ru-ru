---
title: Иенумпрогресситемс Ремотенекст, метод
description: Поддерживает удаленный клиент, который хочет получить указанное число элементов в последовательности перечисления. | Иенумпрогресситемс Ремотенекст, метод
ms.assetid: c5f85ca3-1bad-49fd-9e67-d41135cd837d
keywords:
- Метод Ремотенекст IMAPI
- Метод Ремотенекст IMAPI, интерфейс Иенумпрогресситемс
- Интерфейс Иенумпрогресситемс IMAPI, метод Ремотенекст
topic_type:
- apiref
api_name:
- IEnumProgressItems.RemoteNext
api_location:
- Imapi2fs.idl
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a088a1be640c6653a8a8ccd8b00cf21bd027ecd7
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "105703591"
---
# <a name="ienumprogressitemsremotenext-method"></a><span data-ttu-id="0d18e-107">Метод Иенумпрогресситемс:: Ремотенекст</span><span class="sxs-lookup"><span data-stu-id="0d18e-107">IEnumProgressItems::RemoteNext method</span></span>

<span data-ttu-id="0d18e-108">Поддерживает удаленный клиент, который хочет получить указанное число элементов в последовательности перечисления.</span><span class="sxs-lookup"><span data-stu-id="0d18e-108">Supports a remote client that wants to retrieve a specified number of items in the enumeration sequence</span></span>

## <a name="syntax"></a><span data-ttu-id="0d18e-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="0d18e-109">Syntax</span></span>


```C++
HRESULT RemoteNext(
  [in]  ULONG         celt,
  [out] IProgressItem **rgelt,
  [out] ULONG         *pceltFetched
);
```



## <a name="parameters"></a><span data-ttu-id="0d18e-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="0d18e-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0d18e-111">*celt* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="0d18e-111">*celt* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0d18e-112">Число извлекаемых элементов.</span><span class="sxs-lookup"><span data-stu-id="0d18e-112">Number of items to retrieve.</span></span>

</dd> <dt>

<span data-ttu-id="0d18e-113">*rgelt* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="0d18e-113">*rgelt* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="0d18e-114">Массив интерфейсов [**ипрогресситем**](/windows/desktop/api/imapi2fs/nn-imapi2fs-iprogressitem) .</span><span class="sxs-lookup"><span data-stu-id="0d18e-114">Array of [**IProgressItem**](/windows/desktop/api/imapi2fs/nn-imapi2fs-iprogressitem) interfaces.</span></span> <span data-ttu-id="0d18e-115">По завершении необходимо освободить каждый интерфейс в rgelt.</span><span class="sxs-lookup"><span data-stu-id="0d18e-115">You must release each interface in rgelt when done.</span></span>

</dd> <dt>

<span data-ttu-id="0d18e-116">*пцелтфетчед* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="0d18e-116">*pceltFetched* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="0d18e-117">Число элементов, возвращаемых в rgelt.</span><span class="sxs-lookup"><span data-stu-id="0d18e-117">Number of elements returned in rgelt.</span></span> <span data-ttu-id="0d18e-118">Если параметр *celt* равен 1, можно установить значение *Пцелтфетчед* равным **null** .</span><span class="sxs-lookup"><span data-stu-id="0d18e-118">You can set *pceltFetched* to **NULL** if *celt* is one.</span></span> <span data-ttu-id="0d18e-119">В противном случае инициализируйте значение *пцелтфетчед* значением 0 перед вызовом этого метода.</span><span class="sxs-lookup"><span data-stu-id="0d18e-119">Otherwise, initialize the value of *pceltFetched* to 0 before calling this method.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0d18e-120">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="0d18e-120">Return value</span></span>

<span data-ttu-id="0d18e-121">\_Если число запрошенных элементов (*celt*) возвращено успешно или число возвращаемых элементов (*пцелтфетчед*) меньше числа запрошенных элементов, то возвращается значение ОК.</span><span class="sxs-lookup"><span data-stu-id="0d18e-121">S\_OK is returned when the number of requested elements (*celt*) are returned successfully or the number of returned items (*pceltFetched*) is less than the number of requested elements.</span></span>

<span data-ttu-id="0d18e-122">Другие коды успеха могут возвращаться в результате реализации.</span><span class="sxs-lookup"><span data-stu-id="0d18e-122">Other success codes may be returned as a result of implementation.</span></span> <span data-ttu-id="0d18e-123">Следующие коды ошибок обычно возвращаются при сбое операции, но не представляют единственные возможные значения ошибок:</span><span class="sxs-lookup"><span data-stu-id="0d18e-123">The following error codes are commonly returned on operation failure, but do not represent the only possible error values:</span></span>



| <span data-ttu-id="0d18e-124">Код возврата</span><span class="sxs-lookup"><span data-stu-id="0d18e-124">Return code</span></span>                                                                                   | <span data-ttu-id="0d18e-125">Описание</span><span class="sxs-lookup"><span data-stu-id="0d18e-125">Description</span></span>                                                                     |
|-----------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="0d18e-126"><dt>**\_указатель E**</dt></span><span class="sxs-lookup"><span data-stu-id="0d18e-126"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="0d18e-127">Недопустимый указатель.</span><span class="sxs-lookup"><span data-stu-id="0d18e-127">Pointer is not valid.</span></span><br/> <span data-ttu-id="0d18e-128">Значение: 0x80004003</span><span class="sxs-lookup"><span data-stu-id="0d18e-128">Value: 0x80004003</span></span><br/>                   |
| <dl> <span data-ttu-id="0d18e-129"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="0d18e-129"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="0d18e-130">Не удалось выделить требуемую память.</span><span class="sxs-lookup"><span data-stu-id="0d18e-130">Failed to allocate the required memory.</span></span><br/> <span data-ttu-id="0d18e-131">Значение: 0x8007000E</span><span class="sxs-lookup"><span data-stu-id="0d18e-131">Value: 0x8007000E</span></span><br/> |
| <dl> <span data-ttu-id="0d18e-132"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="0d18e-132"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="0d18e-133">Один или несколько аргументов недопустимы.</span><span class="sxs-lookup"><span data-stu-id="0d18e-133">One or more arguments are not valid.</span></span><br/> <span data-ttu-id="0d18e-134">Значение: 0x80070057</span><span class="sxs-lookup"><span data-stu-id="0d18e-134">Value: 0x80070057</span></span><br/>    |
| <dl> <span data-ttu-id="0d18e-135"><dt>**Д \_ НЕПРЕДВИДЕНные**</dt></span><span class="sxs-lookup"><span data-stu-id="0d18e-135"><dt> **E\_UNEXPECTED**</dt></span></span> </dl> | <span data-ttu-id="0d18e-136">Произошла непредвиденная ошибка.</span><span class="sxs-lookup"><span data-stu-id="0d18e-136">An unexpected failure occurred.</span></span><br/> <span data-ttu-id="0d18e-137">Значение: 0x8000FFFF</span><span class="sxs-lookup"><span data-stu-id="0d18e-137">Value: 0x8000FFFF</span></span><br/>         |



 

## <a name="remarks"></a><span data-ttu-id="0d18e-138">Комментарии</span><span class="sxs-lookup"><span data-stu-id="0d18e-138">Remarks</span></span>

<span data-ttu-id="0d18e-139">Если в последовательности осталось меньше запрошенного числа элементов, то он извлекает оставшиеся элементы.</span><span class="sxs-lookup"><span data-stu-id="0d18e-139">If there are fewer than the requested number of elements left in the sequence, it retrieves the remaining elements.</span></span>

## <a name="requirements"></a><span data-ttu-id="0d18e-140">Требования</span><span class="sxs-lookup"><span data-stu-id="0d18e-140">Requirements</span></span>



| <span data-ttu-id="0d18e-141">Требование</span><span class="sxs-lookup"><span data-stu-id="0d18e-141">Requirement</span></span> | <span data-ttu-id="0d18e-142">Значение</span><span class="sxs-lookup"><span data-stu-id="0d18e-142">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="0d18e-143">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="0d18e-143">Minimum supported client</span></span><br/> | <span data-ttu-id="0d18e-144">Windows Vista, Windows XP с пакетом обновления 2 (SP2), \[ только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="0d18e-144">Windows Vista, Windows XP with SP2 \[desktop apps only\]</span></span><br/>                     |
| <span data-ttu-id="0d18e-145">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="0d18e-145">Minimum supported server</span></span><br/> | <span data-ttu-id="0d18e-146">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="0d18e-146">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="0d18e-147">IDL</span><span class="sxs-lookup"><span data-stu-id="0d18e-147">IDL</span></span><br/>                      | <dl> <span data-ttu-id="0d18e-148"><dt>Imapi2fs. idl</dt></span><span class="sxs-lookup"><span data-stu-id="0d18e-148"><dt>Imapi2fs.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0d18e-149">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="0d18e-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0d18e-150">**иенумпрогресситемс**</span><span class="sxs-lookup"><span data-stu-id="0d18e-150">**IEnumProgressItems**</span></span>](/windows/desktop/api/imapi2fs/nn-imapi2fs-ienumprogressitems)
</dt> <dt>

[<span data-ttu-id="0d18e-151">Иенумпрогресситемс:: Next</span><span class="sxs-lookup"><span data-stu-id="0d18e-151">IEnumProgressItems::Next</span></span>](/windows/desktop/api/imapi2fs/nf-imapi2fs-ienumprogressitems-next)
</dt> </dl>

 

 





