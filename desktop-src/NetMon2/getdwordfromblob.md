---
description: Функция Жетдвордфромблоб получает именованное значение DWORD из большого двоичного объекта.
ms.assetid: edad74a7-b726-46d9-b49f-9984272d0a29
title: Функция Жетдвордфромблоб (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetDwordFromBlob
api_type:
- DllExport
api_location:
- Npptools.dll
ms.openlocfilehash: 064985f0f3b9a235dc1c00d683fe4b11371df87d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104143786"
---
# <a name="getdwordfromblob-function"></a><span data-ttu-id="6fbeb-103">Функция Жетдвордфромблоб</span><span class="sxs-lookup"><span data-stu-id="6fbeb-103">GetDwordFromBlob function</span></span>

<span data-ttu-id="6fbeb-104">Функция **жетдвордфромблоб** получает именованное значение **DWORD** из большого двоичного объекта.</span><span class="sxs-lookup"><span data-stu-id="6fbeb-104">The **GetDwordFromBlob** function retrieves the named **DWORD** value from a BLOB.</span></span>

## <a name="syntax"></a><span data-ttu-id="6fbeb-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="6fbeb-105">Syntax</span></span>


```C++
DWORD GetDwordFromBlob(
  _In_        HBLOB hBlob,
  _In_  const char  *pOwnerName,
  _In_  const char  *pCategoryName,
  _In_  const char  *pTagName,
  _Out_       DWORD *pDword
);
```



## <a name="parameters"></a><span data-ttu-id="6fbeb-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="6fbeb-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6fbeb-107">*хблоб* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="6fbeb-107">*hBlob* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6fbeb-108">Обработчик для большого двоичного объекта.</span><span class="sxs-lookup"><span data-stu-id="6fbeb-108">Handle to a BLOB.</span></span>

</dd> <dt>

<span data-ttu-id="6fbeb-109">*повнернаме* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="6fbeb-109">*pOwnerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6fbeb-110">Указатель на имя владельца большого двоичного объекта.</span><span class="sxs-lookup"><span data-stu-id="6fbeb-110">Pointer to the BLOB owner name.</span></span>

</dd> <dt>

<span data-ttu-id="6fbeb-111">*пкатегоринаме* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="6fbeb-111">*pCategoryName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6fbeb-112">Указатель на имя категории BLOB-объектов.</span><span class="sxs-lookup"><span data-stu-id="6fbeb-112">Pointer to the BLOB category name.</span></span>

</dd> <dt>

<span data-ttu-id="6fbeb-113">*птагнаме* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="6fbeb-113">*pTagName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6fbeb-114">Указатель на имя тега большого двоичного объекта.</span><span class="sxs-lookup"><span data-stu-id="6fbeb-114">Pointer to the BLOB tag name.</span></span>

</dd> <dt>

<span data-ttu-id="6fbeb-115">*пдворд* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="6fbeb-115">*pDword* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6fbeb-116">Указатель на значение **DWORD** большого двоичного объекта.</span><span class="sxs-lookup"><span data-stu-id="6fbeb-116">Pointer to the **DWORD** value of the BLOB.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6fbeb-117">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="6fbeb-117">Return value</span></span>

<span data-ttu-id="6fbeb-118">Если функция выполнена успешно, возвращается значение НМЕРР \_ Success.</span><span class="sxs-lookup"><span data-stu-id="6fbeb-118">If the function is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="6fbeb-119">Если функция завершается неудачно, возвращается значение НМЕРР, описывающее ошибку.</span><span class="sxs-lookup"><span data-stu-id="6fbeb-119">If the function is unsuccessful, the return value is a NMERR value that describes the error.</span></span>

## <a name="requirements"></a><span data-ttu-id="6fbeb-120">Требования</span><span class="sxs-lookup"><span data-stu-id="6fbeb-120">Requirements</span></span>



| <span data-ttu-id="6fbeb-121">Требование</span><span class="sxs-lookup"><span data-stu-id="6fbeb-121">Requirement</span></span> | <span data-ttu-id="6fbeb-122">Значение</span><span class="sxs-lookup"><span data-stu-id="6fbeb-122">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="6fbeb-123">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="6fbeb-123">Minimum supported client</span></span><br/> | <span data-ttu-id="6fbeb-124">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="6fbeb-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="6fbeb-125">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="6fbeb-125">Minimum supported server</span></span><br/> | <span data-ttu-id="6fbeb-126">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="6fbeb-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="6fbeb-127">Заголовок</span><span class="sxs-lookup"><span data-stu-id="6fbeb-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="6fbeb-128"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="6fbeb-128"><dt>Netmon.h</dt></span></span> </dl>     |
| <span data-ttu-id="6fbeb-129">Библиотека</span><span class="sxs-lookup"><span data-stu-id="6fbeb-129">Library</span></span><br/>                  | <dl> <span data-ttu-id="6fbeb-130"><dt>Нпптулс. lib</dt></span><span class="sxs-lookup"><span data-stu-id="6fbeb-130"><dt>Npptools.lib</dt></span></span> </dl> |
| <span data-ttu-id="6fbeb-131">DLL</span><span class="sxs-lookup"><span data-stu-id="6fbeb-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6fbeb-132"><dt>Npptools.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6fbeb-132"><dt>Npptools.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6fbeb-133">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="6fbeb-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6fbeb-134">сетдвординблоб</span><span class="sxs-lookup"><span data-stu-id="6fbeb-134">SetDwordInBlob</span></span>](setdwordinblob.md)
</dt> <dt>

[<span data-ttu-id="6fbeb-135">жетбулфромблоб</span><span class="sxs-lookup"><span data-stu-id="6fbeb-135">GetBoolFromBlob</span></span>](getboolfromblob.md)
</dt> <dt>

[<span data-ttu-id="6fbeb-136">жетклассидфромблоб</span><span class="sxs-lookup"><span data-stu-id="6fbeb-136">GetClassIDFromBlob</span></span>](getclassidfromblob.md)
</dt> <dt>

[<span data-ttu-id="6fbeb-137">жетмакаддрессфромблоб</span><span class="sxs-lookup"><span data-stu-id="6fbeb-137">GetMacAddressFromBlob</span></span>](getmacaddressfromblob.md)
</dt> <dt>

[<span data-ttu-id="6fbeb-138">жетнетворкинфофромблоб</span><span class="sxs-lookup"><span data-stu-id="6fbeb-138">GetNetworkInfoFromBlob</span></span>](getnetworkinfofromblob.md)
</dt> <dt>

[<span data-ttu-id="6fbeb-139">жетнппаддрессфилтерфромблоб</span><span class="sxs-lookup"><span data-stu-id="6fbeb-139">GetNPPAddressFilterFromBlob</span></span>](getnppaddressfilterfromblob.md)
</dt> <dt>

[<span data-ttu-id="6fbeb-140">жетнпппаттернфилтерфромблоб</span><span class="sxs-lookup"><span data-stu-id="6fbeb-140">GetNPPPatternFilterFromBlob</span></span>](getnpppatternfilterfromblob.md)
</dt> <dt>

[<span data-ttu-id="6fbeb-141">жетнпптригжерфромблоб</span><span class="sxs-lookup"><span data-stu-id="6fbeb-141">GetNPPTriggerFromBlob</span></span>](getnpptriggerfromblob.md)
</dt> <dt>

[<span data-ttu-id="6fbeb-142">жетстрингфромблоб</span><span class="sxs-lookup"><span data-stu-id="6fbeb-142">GetStringFromBlob</span></span>](getstringfromblob.md)
</dt> <dt>

[<span data-ttu-id="6fbeb-143">жетстрингсфромблоб</span><span class="sxs-lookup"><span data-stu-id="6fbeb-143">GetStringsFromBlob</span></span>](getstringsfromblob.md)
</dt> </dl>

 

 




