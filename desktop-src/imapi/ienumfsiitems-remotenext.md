---
title: Иенумфсиитемс Ремотенекст, метод
description: Поддерживает удаленный клиент, который хочет получить указанное число элементов в последовательности перечисления. | Иенумфсиитемс Ремотенекст, метод
ms.assetid: a5ae59ed-08d7-4225-9aec-91049789e8fe
keywords:
- Метод Ремотенекст IMAPI
- Метод Ремотенекст IMAPI, интерфейс Иенумфсиитемс
- Интерфейс Иенумфсиитемс IMAPI, метод Ремотенекст
topic_type:
- apiref
api_name:
- IEnumFsiItems.RemoteNext
api_location:
- Imapi2fs.idl
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8e29d3f75cd8e2f83fcd21236661d0d1fa0dabef
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "104547642"
---
# <a name="ienumfsiitemsremotenext-method"></a><span data-ttu-id="b79ba-107">Метод Иенумфсиитемс:: Ремотенекст</span><span class="sxs-lookup"><span data-stu-id="b79ba-107">IEnumFsiItems::RemoteNext method</span></span>

<span data-ttu-id="b79ba-108">Поддерживает удаленный клиент, который хочет получить указанное число элементов в последовательности перечисления.</span><span class="sxs-lookup"><span data-stu-id="b79ba-108">Supports a remote client that wants to retrieve a specified number of items in the enumeration sequence.</span></span>

## <a name="syntax"></a><span data-ttu-id="b79ba-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="b79ba-109">Syntax</span></span>


```C++
HRESULT RemoteNext(
  [in]  ULONG    celt,
  [out] IFsiItem **rgelt,
  [out] ULONG    *pceltFetched
);
```



## <a name="parameters"></a><span data-ttu-id="b79ba-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="b79ba-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b79ba-111">*celt* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="b79ba-111">*celt* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b79ba-112">Число извлекаемых элементов.</span><span class="sxs-lookup"><span data-stu-id="b79ba-112">Number of items to retrieve.</span></span>

</dd> <dt>

<span data-ttu-id="b79ba-113">*rgelt* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="b79ba-113">*rgelt* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b79ba-114">Массив интерфейсов [**ифсиитем**](/windows/desktop/api/imapi2fs/nn-imapi2fs-ifsiitem) .</span><span class="sxs-lookup"><span data-stu-id="b79ba-114">Array of [**IFsiItem**](/windows/desktop/api/imapi2fs/nn-imapi2fs-ifsiitem) interfaces.</span></span> <span data-ttu-id="b79ba-115">По завершении необходимо освободить каждый интерфейс в rgelt.</span><span class="sxs-lookup"><span data-stu-id="b79ba-115">You must release each interface in rgelt when done.</span></span>

</dd> <dt>

<span data-ttu-id="b79ba-116">*пцелтфетчед* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="b79ba-116">*pceltFetched* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b79ba-117">Число элементов, возвращаемых в rgelt.</span><span class="sxs-lookup"><span data-stu-id="b79ba-117">Number of elements returned in rgelt.</span></span> <span data-ttu-id="b79ba-118">Если параметр *celt* равен 1, можно установить значение *Пцелтфетчед* равным **null** .</span><span class="sxs-lookup"><span data-stu-id="b79ba-118">You can set *pceltFetched* to **NULL** if *celt* is one.</span></span> <span data-ttu-id="b79ba-119">В противном случае инициализируйте значение *пцелтфетчед* значением 0 перед вызовом этого метода.</span><span class="sxs-lookup"><span data-stu-id="b79ba-119">Otherwise, initialize the value of *pceltFetched* to 0 before calling this method.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b79ba-120">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="b79ba-120">Return value</span></span>

<span data-ttu-id="b79ba-121">\_Если число запрошенных элементов (*celt*) возвращено успешно или число возвращаемых элементов (*пцелтфетчед*) меньше числа запрошенных элементов, то возвращается значение ОК.</span><span class="sxs-lookup"><span data-stu-id="b79ba-121">S\_OK is returned when the number of requested elements (*celt*) are returned successfully or the number of returned items (*pceltFetched*) is less than the number of requested elements.</span></span>

<span data-ttu-id="b79ba-122">Другие коды успеха могут возвращаться в результате реализации.</span><span class="sxs-lookup"><span data-stu-id="b79ba-122">Other success codes may be returned as a result of implementation.</span></span> <span data-ttu-id="b79ba-123">Следующие коды ошибок обычно возвращаются при сбое операции, но не представляют единственные возможные значения ошибок:</span><span class="sxs-lookup"><span data-stu-id="b79ba-123">The following error codes are commonly returned on operation failure, but do not represent the only possible error values:</span></span>



| <span data-ttu-id="b79ba-124">Код возврата</span><span class="sxs-lookup"><span data-stu-id="b79ba-124">Return code</span></span>                                                                                   | <span data-ttu-id="b79ba-125">Описание</span><span class="sxs-lookup"><span data-stu-id="b79ba-125">Description</span></span>                                                                     |
|-----------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="b79ba-126"><dt>**\_указатель E**</dt></span><span class="sxs-lookup"><span data-stu-id="b79ba-126"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="b79ba-127">Недопустимый указатель.</span><span class="sxs-lookup"><span data-stu-id="b79ba-127">Pointer is not valid.</span></span><br/> <span data-ttu-id="b79ba-128">Значение: 0x80004003</span><span class="sxs-lookup"><span data-stu-id="b79ba-128">Value: 0x80004003</span></span><br/>                   |
| <dl> <span data-ttu-id="b79ba-129"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="b79ba-129"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="b79ba-130">Не удалось выделить требуемую память.</span><span class="sxs-lookup"><span data-stu-id="b79ba-130">Failed to allocate the required memory.</span></span><br/> <span data-ttu-id="b79ba-131">Значение: 0x8007000E</span><span class="sxs-lookup"><span data-stu-id="b79ba-131">Value: 0x8007000E</span></span><br/> |
| <dl> <span data-ttu-id="b79ba-132"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="b79ba-132"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="b79ba-133">Один или несколько аргументов недопустимы.</span><span class="sxs-lookup"><span data-stu-id="b79ba-133">One or more arguments are not valid.</span></span><br/> <span data-ttu-id="b79ba-134">Значение: 0x80070057</span><span class="sxs-lookup"><span data-stu-id="b79ba-134">Value: 0x80070057</span></span><br/>    |



 

## <a name="requirements"></a><span data-ttu-id="b79ba-135">Требования</span><span class="sxs-lookup"><span data-stu-id="b79ba-135">Requirements</span></span>



| <span data-ttu-id="b79ba-136">Требование</span><span class="sxs-lookup"><span data-stu-id="b79ba-136">Requirement</span></span> | <span data-ttu-id="b79ba-137">Значение</span><span class="sxs-lookup"><span data-stu-id="b79ba-137">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b79ba-138">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="b79ba-138">Minimum supported client</span></span><br/> | <span data-ttu-id="b79ba-139">Windows Vista, Windows XP с пакетом обновления 2 (SP2), \[ только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="b79ba-139">Windows Vista, Windows XP with SP2 \[desktop apps only\]</span></span><br/>                     |
| <span data-ttu-id="b79ba-140">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="b79ba-140">Minimum supported server</span></span><br/> | <span data-ttu-id="b79ba-141">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="b79ba-141">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="b79ba-142">IDL</span><span class="sxs-lookup"><span data-stu-id="b79ba-142">IDL</span></span><br/>                      | <dl> <span data-ttu-id="b79ba-143"><dt>Imapi2fs. idl</dt></span><span class="sxs-lookup"><span data-stu-id="b79ba-143"><dt>Imapi2fs.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b79ba-144">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="b79ba-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b79ba-145">**иенумфсиитемс**</span><span class="sxs-lookup"><span data-stu-id="b79ba-145">**IEnumFsiItems**</span></span>](/windows/desktop/api/imapi2fs/nn-imapi2fs-ienumfsiitems)
</dt> <dt>

[<span data-ttu-id="b79ba-146">Иенумфсиитемс:: Next</span><span class="sxs-lookup"><span data-stu-id="b79ba-146">IEnumFsiItems::Next</span></span>](/windows/desktop/api/imapi2fs/nf-imapi2fs-ienumfsiitems-next)
</dt> </dl>

 

 





