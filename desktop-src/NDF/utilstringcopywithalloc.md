---
title: Функция Утилстрингкопивисаллок (Ндаттрибутилс. h)
description: Выделяет и копирует исходную строку.
ms.assetid: e1400ae1-0edd-4b59-af03-3da1b9d7073b
keywords:
- Утилстрингкопивисаллок функция NDF
topic_type:
- apiref
api_name:
- UtilStringCopyWithAlloc
api_location:
- ndattributils.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b68bd1815ff09473f0431dde19a12a87603a9dec
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105672597"
---
# <a name="utilstringcopywithalloc-function"></a><span data-ttu-id="3438b-104">Функция Утилстрингкопивисаллок</span><span class="sxs-lookup"><span data-stu-id="3438b-104">UtilStringCopyWithAlloc function</span></span>

<span data-ttu-id="3438b-105">Функция **утилстрингкопивисаллок** выделяет и копирует исходную строку.</span><span class="sxs-lookup"><span data-stu-id="3438b-105">The **UtilStringCopyWithAlloc** function allocates and copies a source string.</span></span>

## <a name="syntax"></a><span data-ttu-id="3438b-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="3438b-106">Syntax</span></span>


```C++
HRESULT UtilStringCopyWithAlloc(
  _Out_ LPWSTR  *Buffer,
  _In_  UINT    BufferMax,
  _In_  LPCWSTR Source
);
```



## <a name="parameters"></a><span data-ttu-id="3438b-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="3438b-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3438b-108">*Буфер* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="3438b-108">*Buffer* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="3438b-109">Введите: \**LPWSTR \** _</span><span class="sxs-lookup"><span data-stu-id="3438b-109">Type: \**LPWSTR\** _</span></span>

<span data-ttu-id="3438b-110">Расположение, в котором хранится указатель на выделенную память.</span><span class="sxs-lookup"><span data-stu-id="3438b-110">The location where the pointer to the allocated memory is stored.</span></span> <span data-ttu-id="3438b-111">Если он больше не нужен, он должен быть освобожден с помощью [_ *CoTaskMemFree* \*](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree).</span><span class="sxs-lookup"><span data-stu-id="3438b-111">When no longer needed, it must be released with [_ *CoTaskMemFree*\*](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree).</span></span> <span data-ttu-id="3438b-112">Этот буфер всегда завершается нулем.</span><span class="sxs-lookup"><span data-stu-id="3438b-112">This buffer is always null-terminated.</span></span>

</dd> <dt>

<span data-ttu-id="3438b-113">*Буффермакс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="3438b-113">*BufferMax* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3438b-114">Тип: **uint**</span><span class="sxs-lookup"><span data-stu-id="3438b-114">Type: **UINT**</span></span>

<span data-ttu-id="3438b-115">Максимальное число символов для чтения из *источника*.</span><span class="sxs-lookup"><span data-stu-id="3438b-115">The maximum number of characters to read from *Source*.</span></span>

</dd> <dt>

<span data-ttu-id="3438b-116">*Исходный код* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="3438b-116">*Source* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3438b-117">Тип: **лпквстр**</span><span class="sxs-lookup"><span data-stu-id="3438b-117">Type: **LPCWSTR**</span></span>

<span data-ttu-id="3438b-118">Копируемая строка.</span><span class="sxs-lookup"><span data-stu-id="3438b-118">The string to be copied.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3438b-119">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="3438b-119">Return value</span></span>

<span data-ttu-id="3438b-120">Тип: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="3438b-120">Type: **HRESULT**</span></span>

<span data-ttu-id="3438b-121">Возможные возвращаемые значения включают, но не ограничиваются следующим.</span><span class="sxs-lookup"><span data-stu-id="3438b-121">Possible return values include, but are not limited to, the following.</span></span>



| <span data-ttu-id="3438b-122">Код возврата</span><span class="sxs-lookup"><span data-stu-id="3438b-122">Return code</span></span>                                                                                  | <span data-ttu-id="3438b-123">Описание</span><span class="sxs-lookup"><span data-stu-id="3438b-123">Description</span></span>                                                        |
|----------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="3438b-124"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="3438b-124"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="3438b-125">Операция успешно выполнена.</span><span class="sxs-lookup"><span data-stu-id="3438b-125">The operation succeeded.</span></span><br/>                                |
| <dl> <span data-ttu-id="3438b-126"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="3438b-126"><dt>**E\_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="3438b-127">Один или несколько параметров указаны неправильно.</span><span class="sxs-lookup"><span data-stu-id="3438b-127">One or more parameters has not been provided correctly.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="3438b-128">Требования</span><span class="sxs-lookup"><span data-stu-id="3438b-128">Requirements</span></span>



| <span data-ttu-id="3438b-129">Требование</span><span class="sxs-lookup"><span data-stu-id="3438b-129">Requirement</span></span> | <span data-ttu-id="3438b-130">Значение</span><span class="sxs-lookup"><span data-stu-id="3438b-130">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="3438b-131">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="3438b-131">Minimum supported client</span></span><br/> | <span data-ttu-id="3438b-132">\[Только классические приложения Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="3438b-132">Windows 8 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="3438b-133">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="3438b-133">Minimum supported server</span></span><br/> | <span data-ttu-id="3438b-134">\[Только для настольных приложений Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="3438b-134">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="3438b-135">Header</span><span class="sxs-lookup"><span data-stu-id="3438b-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="3438b-136"><dt>Ндаттрибутилс. h</dt></span><span class="sxs-lookup"><span data-stu-id="3438b-136"><dt>Ndattributils.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3438b-137">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="3438b-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3438b-138">**CoTaskMemFree**</span><span class="sxs-lookup"><span data-stu-id="3438b-138">**CoTaskMemFree**</span></span>](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree)
</dt> <dt>

[<span data-ttu-id="3438b-139">**утилассемблестрингсвисаллок**</span><span class="sxs-lookup"><span data-stu-id="3438b-139">**UtilAssembleStringsWithAlloc**</span></span>](utilassemblestringswithalloc.md)
</dt> <dt>

[<span data-ttu-id="3438b-140">**утиллоадстрингвисаллок**</span><span class="sxs-lookup"><span data-stu-id="3438b-140">**UtilLoadStringWithAlloc**</span></span>](utilloadstringwithalloc.md)
</dt> </dl>

 

