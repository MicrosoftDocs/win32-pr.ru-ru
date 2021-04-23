---
description: Извлекает именованное логическое значение из большого двоичного объекта.
ms.assetid: 26acfd2a-5b17-47ad-8f7b-7793174a13c3
title: Функция Жетбулфромблоб (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetBoolFromBlob
api_type:
- DllExport
api_location:
- Npptools.dll
ms.openlocfilehash: e09a35f71181343cd401b3288c2b2c74a46f677b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105673190"
---
# <a name="getboolfromblob-function"></a><span data-ttu-id="4b6ea-103">Функция Жетбулфромблоб</span><span class="sxs-lookup"><span data-stu-id="4b6ea-103">GetBoolFromBlob function</span></span>

<span data-ttu-id="4b6ea-104">Функция **жетбулфромблоб** Извлекает именованное логическое значение из большого двоичного объекта.</span><span class="sxs-lookup"><span data-stu-id="4b6ea-104">The **GetBoolFromBlob** function retrieves a named Boolean value from a BLOB.</span></span>

## <a name="syntax"></a><span data-ttu-id="4b6ea-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="4b6ea-105">Syntax</span></span>


```C++
DWORD GetBoolFromBlob(
  _In_        HBLOB hBlob,
  _In_  const char  *pOwnerName,
  _In_  const char  *pCategoryName,
  _In_  const char  *pTagName,
  _Out_       BOOL  *pBool
);
```



## <a name="parameters"></a><span data-ttu-id="4b6ea-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="4b6ea-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4b6ea-107">*хблоб* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="4b6ea-107">*hBlob* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4b6ea-108">Маркер для большого двоичного объекта.</span><span class="sxs-lookup"><span data-stu-id="4b6ea-108">A handle to a BLOB.</span></span>

</dd> <dt>

<span data-ttu-id="4b6ea-109">*повнернаме* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="4b6ea-109">*pOwnerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4b6ea-110">Указатель на имя владельца большого двоичного объекта.</span><span class="sxs-lookup"><span data-stu-id="4b6ea-110">A pointer to the BLOB owner name.</span></span>

</dd> <dt>

<span data-ttu-id="4b6ea-111">*пкатегоринаме* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="4b6ea-111">*pCategoryName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4b6ea-112">Указатель на имя категории BLOB-объектов.</span><span class="sxs-lookup"><span data-stu-id="4b6ea-112">A pointer to the BLOB category name.</span></span>

</dd> <dt>

<span data-ttu-id="4b6ea-113">*птагнаме* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="4b6ea-113">*pTagName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4b6ea-114">Указатель на имя тега большого двоичного объекта.</span><span class="sxs-lookup"><span data-stu-id="4b6ea-114">A pointer to the BLOB tag name.</span></span>

</dd> <dt>

<span data-ttu-id="4b6ea-115">*пбул* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="4b6ea-115">*pBool* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="4b6ea-116">Указатель на логическое значение большого двоичного объекта.</span><span class="sxs-lookup"><span data-stu-id="4b6ea-116">Pointer to the Boolean value of the BLOB.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4b6ea-117">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="4b6ea-117">Return value</span></span>

<span data-ttu-id="4b6ea-118">Если функция выполнена успешно, возвращается значение НМЕРР \_ Success.</span><span class="sxs-lookup"><span data-stu-id="4b6ea-118">If the function is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="4b6ea-119">Если функция завершается неудачно, возвращается значение НМЕРР, описывающее ошибку.</span><span class="sxs-lookup"><span data-stu-id="4b6ea-119">If the function is unsuccessful, the return value is a NMERR value that describes the error.</span></span>

## <a name="requirements"></a><span data-ttu-id="4b6ea-120">Требования</span><span class="sxs-lookup"><span data-stu-id="4b6ea-120">Requirements</span></span>



| <span data-ttu-id="4b6ea-121">Требование</span><span class="sxs-lookup"><span data-stu-id="4b6ea-121">Requirement</span></span> | <span data-ttu-id="4b6ea-122">Значение</span><span class="sxs-lookup"><span data-stu-id="4b6ea-122">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="4b6ea-123">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="4b6ea-123">Minimum supported client</span></span><br/> | <span data-ttu-id="4b6ea-124">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="4b6ea-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="4b6ea-125">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="4b6ea-125">Minimum supported server</span></span><br/> | <span data-ttu-id="4b6ea-126">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="4b6ea-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="4b6ea-127">Заголовок</span><span class="sxs-lookup"><span data-stu-id="4b6ea-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="4b6ea-128"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="4b6ea-128"><dt>Netmon.h</dt></span></span> </dl>     |
| <span data-ttu-id="4b6ea-129">Библиотека</span><span class="sxs-lookup"><span data-stu-id="4b6ea-129">Library</span></span><br/>                  | <dl> <span data-ttu-id="4b6ea-130"><dt>Нпптулс. lib</dt></span><span class="sxs-lookup"><span data-stu-id="4b6ea-130"><dt>Npptools.lib</dt></span></span> </dl> |
| <span data-ttu-id="4b6ea-131">DLL</span><span class="sxs-lookup"><span data-stu-id="4b6ea-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4b6ea-132"><dt>Npptools.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4b6ea-132"><dt>Npptools.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4b6ea-133">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="4b6ea-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4b6ea-134">сетбулинблоб</span><span class="sxs-lookup"><span data-stu-id="4b6ea-134">SetBoolInBlob</span></span>](setboolinblob.md)
</dt> <dt>

[<span data-ttu-id="4b6ea-135">жетклассидфромблоб</span><span class="sxs-lookup"><span data-stu-id="4b6ea-135">GetClassIDFromBlob</span></span>](getclassidfromblob.md)
</dt> <dt>

[<span data-ttu-id="4b6ea-136">жетдвордфромблоб</span><span class="sxs-lookup"><span data-stu-id="4b6ea-136">GetDwordFromBlob</span></span>](getdwordfromblob.md)
</dt> <dt>

[<span data-ttu-id="4b6ea-137">жетмакаддрессфромблоб</span><span class="sxs-lookup"><span data-stu-id="4b6ea-137">GetMacAddressFromBlob</span></span>](getmacaddressfromblob.md)
</dt> <dt>

[<span data-ttu-id="4b6ea-138">жетнетворкинфофромблоб</span><span class="sxs-lookup"><span data-stu-id="4b6ea-138">GetNetworkInfoFromBlob</span></span>](getnetworkinfofromblob.md)
</dt> <dt>

[<span data-ttu-id="4b6ea-139">жетнппаддрессфилтерфромблоб</span><span class="sxs-lookup"><span data-stu-id="4b6ea-139">GetNPPAddressFilterFromBlob</span></span>](getnppaddressfilterfromblob.md)
</dt> <dt>

[<span data-ttu-id="4b6ea-140">жетнпппаттернфилтерфромблоб</span><span class="sxs-lookup"><span data-stu-id="4b6ea-140">GetNPPPatternFilterFromBlob</span></span>](getnpppatternfilterfromblob.md)
</dt> <dt>

[<span data-ttu-id="4b6ea-141">жетнпптригжерфромблоб</span><span class="sxs-lookup"><span data-stu-id="4b6ea-141">GetNPPTriggerFromBlob</span></span>](getnpptriggerfromblob.md)
</dt> <dt>

[<span data-ttu-id="4b6ea-142">жетстрингфромблоб</span><span class="sxs-lookup"><span data-stu-id="4b6ea-142">GetStringFromBlob</span></span>](getstringfromblob.md)
</dt> <dt>

[<span data-ttu-id="4b6ea-143">жетстрингсфромблоб</span><span class="sxs-lookup"><span data-stu-id="4b6ea-143">GetStringsFromBlob</span></span>](getstringsfromblob.md)
</dt> </dl>

 

 




