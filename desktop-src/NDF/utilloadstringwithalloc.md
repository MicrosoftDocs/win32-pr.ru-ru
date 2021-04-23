---
title: Функция Утиллоадстрингвисаллок (Ндаттрибутилс. h)
description: Выделяет и загружает строку из таблицы ресурсов.
ms.assetid: 34bf0b93-2bec-49c3-9441-c83686c4abdb
keywords:
- Утиллоадстрингвисаллок функция NDF
topic_type:
- apiref
api_name:
- UtilLoadStringWithAlloc
api_location:
- ndattributils.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 72e13930fe9bb11ae9c9456152c823491eabc462
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104137779"
---
# <a name="utilloadstringwithalloc-function"></a><span data-ttu-id="9b9d1-104">Функция Утиллоадстрингвисаллок</span><span class="sxs-lookup"><span data-stu-id="9b9d1-104">UtilLoadStringWithAlloc function</span></span>

<span data-ttu-id="9b9d1-105">Функция **утиллоадстрингвисаллок** выделяет и загружает строку из таблицы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="9b9d1-105">The **UtilLoadStringWithAlloc** function allocates and loads a string out of the resource table.</span></span>

## <a name="syntax"></a><span data-ttu-id="9b9d1-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="9b9d1-106">Syntax</span></span>


```C++
HRESULT UtilLoadStringWithAlloc(
  _In_  UINT   uID,
  _Out_ LPWSTR *ppwzBuffer,
  _In_  UINT   cchBufferMax
);
```



## <a name="parameters"></a><span data-ttu-id="9b9d1-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="9b9d1-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9b9d1-108">*UID* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="9b9d1-108">*uID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9b9d1-109">Тип: **uint**</span><span class="sxs-lookup"><span data-stu-id="9b9d1-109">Type: **UINT**</span></span>

<span data-ttu-id="9b9d1-110">Идентификатор загружаемой строки.</span><span class="sxs-lookup"><span data-stu-id="9b9d1-110">Identifier of of the string to be loaded.</span></span>

</dd> <dt>

<span data-ttu-id="9b9d1-111">*ппвзбуффер* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="9b9d1-111">*ppwzBuffer* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="9b9d1-112">Введите: \**LPWSTR \** _</span><span class="sxs-lookup"><span data-stu-id="9b9d1-112">Type: \**LPWSTR\** _</span></span>

<span data-ttu-id="9b9d1-113">Расположение, в которое будет помещена вновь выделенная строка.</span><span class="sxs-lookup"><span data-stu-id="9b9d1-113">The location where the newly allocated string will be placed.</span></span> <span data-ttu-id="9b9d1-114">Строка должна быть освобождена с помощью [_ *CoTaskMemFree* \*](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree) , если она больше не нужна.</span><span class="sxs-lookup"><span data-stu-id="9b9d1-114">The string must be freed using [_ *CoTaskMemFree*\*](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree) when it is no longer needed.</span></span>

</dd> <dt>

<span data-ttu-id="9b9d1-115">*кчбуффермакс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="9b9d1-115">*cchBufferMax* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9b9d1-116">Тип: **uint**</span><span class="sxs-lookup"><span data-stu-id="9b9d1-116">Type: **UINT**</span></span>

<span data-ttu-id="9b9d1-117">Максимальное число символов, загружаемых из таблицы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="9b9d1-117">The maximum number of characters to load from the resource table.</span></span> <span data-ttu-id="9b9d1-118">Если длина строки ресурса превышает указанное число символов, она усекается и завершается нулем.</span><span class="sxs-lookup"><span data-stu-id="9b9d1-118">If the resource string is longer than the number of characters specified, it is truncated and null-terminated.</span></span>

> [!Note]  
> <span data-ttu-id="9b9d1-119">Этот параметр не может иметь значение 0.</span><span class="sxs-lookup"><span data-stu-id="9b9d1-119">This parameter may not be set to zero.</span></span>

 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9b9d1-120">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="9b9d1-120">Return value</span></span>

<span data-ttu-id="9b9d1-121">Тип: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="9b9d1-121">Type: **HRESULT**</span></span>

<span data-ttu-id="9b9d1-122">Возможные возвращаемые значения включают, но не ограничиваются следующим.</span><span class="sxs-lookup"><span data-stu-id="9b9d1-122">Possible return values include, but are not limited to, the following.</span></span>



| <span data-ttu-id="9b9d1-123">Код возврата</span><span class="sxs-lookup"><span data-stu-id="9b9d1-123">Return code</span></span>                                                                                  | <span data-ttu-id="9b9d1-124">Описание</span><span class="sxs-lookup"><span data-stu-id="9b9d1-124">Description</span></span>                                                        |
|----------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="9b9d1-125"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="9b9d1-125"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="9b9d1-126">Операция успешно выполнена.</span><span class="sxs-lookup"><span data-stu-id="9b9d1-126">The operation succeeded.</span></span><br/>                                |
| <dl> <span data-ttu-id="9b9d1-127"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="9b9d1-127"><dt>**E\_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="9b9d1-128">Один или несколько параметров указаны неправильно.</span><span class="sxs-lookup"><span data-stu-id="9b9d1-128">One or more parameters has not been provided correctly.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="9b9d1-129">Требования</span><span class="sxs-lookup"><span data-stu-id="9b9d1-129">Requirements</span></span>



| <span data-ttu-id="9b9d1-130">Требование</span><span class="sxs-lookup"><span data-stu-id="9b9d1-130">Requirement</span></span> | <span data-ttu-id="9b9d1-131">Значение</span><span class="sxs-lookup"><span data-stu-id="9b9d1-131">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="9b9d1-132">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="9b9d1-132">Minimum supported client</span></span><br/> | <span data-ttu-id="9b9d1-133">\[Только классические приложения Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="9b9d1-133">Windows 8 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="9b9d1-134">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="9b9d1-134">Minimum supported server</span></span><br/> | <span data-ttu-id="9b9d1-135">\[Только для настольных приложений Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="9b9d1-135">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="9b9d1-136">Header</span><span class="sxs-lookup"><span data-stu-id="9b9d1-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="9b9d1-137"><dt>Ндаттрибутилс. h</dt></span><span class="sxs-lookup"><span data-stu-id="9b9d1-137"><dt>Ndattributils.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9b9d1-138">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="9b9d1-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9b9d1-139">**утилстрингкопивисаллок**</span><span class="sxs-lookup"><span data-stu-id="9b9d1-139">**UtilStringCopyWithAlloc**</span></span>](utilstringcopywithalloc.md)
</dt> <dt>

[<span data-ttu-id="9b9d1-140">**утилассемблестрингсвисаллок**</span><span class="sxs-lookup"><span data-stu-id="9b9d1-140">**UtilAssembleStringsWithAlloc**</span></span>](utilassemblestringswithalloc.md)
</dt> <dt>

[<span data-ttu-id="9b9d1-141">**CoTaskMemFree**</span><span class="sxs-lookup"><span data-stu-id="9b9d1-141">**CoTaskMemFree**</span></span>](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree)
</dt> </dl>

 

