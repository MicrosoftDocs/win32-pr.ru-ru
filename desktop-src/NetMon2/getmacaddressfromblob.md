---
description: Функция Жетмакаддрессфромблоб Извлекает именованный MAC-адрес из большого двоичного объекта.
ms.assetid: 1769c92c-0946-447c-885a-fcf175fa1bf3
title: Функция Жетмакаддрессфромблоб (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetMacAddressFromBlob
api_type:
- DllExport
api_location:
- Npptools.dll
ms.openlocfilehash: 022d4f618c09652c368f6664b194b4ebafc81717
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105684352"
---
# <a name="getmacaddressfromblob-function"></a><span data-ttu-id="bc3a4-103">Функция Жетмакаддрессфромблоб</span><span class="sxs-lookup"><span data-stu-id="bc3a4-103">GetMacAddressFromBlob function</span></span>

<span data-ttu-id="bc3a4-104">Функция **жетмакаддрессфромблоб** извлекает ИМЕНОВАННЫЙ Mac-адрес из большого двоичного объекта.</span><span class="sxs-lookup"><span data-stu-id="bc3a4-104">The **GetMacAddressFromBlob** function retrieves the named MAC address from a BLOB.</span></span>

## <a name="syntax"></a><span data-ttu-id="bc3a4-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="bc3a4-105">Syntax</span></span>


```C++
DWORD GetMacAddressFromBlob(
  _In_        HBLOB hBlob,
  _In_  const char  *pOwnerName,
  _In_  const char  *pCategoryName,
  _In_  const char  *pTagName,
  _Out_       BYTE  *pMacAddress
);
```



## <a name="parameters"></a><span data-ttu-id="bc3a4-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="bc3a4-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bc3a4-107">*хблоб* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="bc3a4-107">*hBlob* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bc3a4-108">Обработчик для большого двоичного объекта.</span><span class="sxs-lookup"><span data-stu-id="bc3a4-108">Handle to a BLOB.</span></span>

</dd> <dt>

<span data-ttu-id="bc3a4-109">*повнернаме* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="bc3a4-109">*pOwnerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bc3a4-110">Указатель на имя владельца большого двоичного объекта.</span><span class="sxs-lookup"><span data-stu-id="bc3a4-110">Pointer to the BLOB owner name.</span></span>

</dd> <dt>

<span data-ttu-id="bc3a4-111">*пкатегоринаме* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="bc3a4-111">*pCategoryName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bc3a4-112">Указатель на имя категории BLOB-объектов.</span><span class="sxs-lookup"><span data-stu-id="bc3a4-112">Pointer to the BLOB category name.</span></span>

</dd> <dt>

<span data-ttu-id="bc3a4-113">*птагнаме* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="bc3a4-113">*pTagName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bc3a4-114">Указатель на имя тега большого двоичного объекта.</span><span class="sxs-lookup"><span data-stu-id="bc3a4-114">Pointer to the BLOB tag name.</span></span>

</dd> <dt>

<span data-ttu-id="bc3a4-115">*пмакаддресс* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="bc3a4-115">*pMacAddress* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="bc3a4-116">Указатель на MAC-адрес большого двоичного объекта.</span><span class="sxs-lookup"><span data-stu-id="bc3a4-116">Pointer to the MAC address of the BLOB.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bc3a4-117">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="bc3a4-117">Return value</span></span>

<span data-ttu-id="bc3a4-118">Если функция выполнена успешно, возвращается значение НМЕРР \_ Success.</span><span class="sxs-lookup"><span data-stu-id="bc3a4-118">If the function is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="bc3a4-119">Если функция завершается неудачно, возвращается значение НМЕРР, описывающее ошибку.</span><span class="sxs-lookup"><span data-stu-id="bc3a4-119">If the function is unsuccessful, the return value is a NMERR value that describes the error.</span></span>

## <a name="requirements"></a><span data-ttu-id="bc3a4-120">Требования</span><span class="sxs-lookup"><span data-stu-id="bc3a4-120">Requirements</span></span>



| <span data-ttu-id="bc3a4-121">Требование</span><span class="sxs-lookup"><span data-stu-id="bc3a4-121">Requirement</span></span> | <span data-ttu-id="bc3a4-122">Значение</span><span class="sxs-lookup"><span data-stu-id="bc3a4-122">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="bc3a4-123">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="bc3a4-123">Minimum supported client</span></span><br/> | <span data-ttu-id="bc3a4-124">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="bc3a4-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="bc3a4-125">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="bc3a4-125">Minimum supported server</span></span><br/> | <span data-ttu-id="bc3a4-126">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="bc3a4-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="bc3a4-127">Заголовок</span><span class="sxs-lookup"><span data-stu-id="bc3a4-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="bc3a4-128"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="bc3a4-128"><dt>Netmon.h</dt></span></span> </dl>     |
| <span data-ttu-id="bc3a4-129">Библиотека</span><span class="sxs-lookup"><span data-stu-id="bc3a4-129">Library</span></span><br/>                  | <dl> <span data-ttu-id="bc3a4-130"><dt>Нпптулс. lib</dt></span><span class="sxs-lookup"><span data-stu-id="bc3a4-130"><dt>Npptools.lib</dt></span></span> </dl> |
| <span data-ttu-id="bc3a4-131">DLL</span><span class="sxs-lookup"><span data-stu-id="bc3a4-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="bc3a4-132"><dt>Npptools.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bc3a4-132"><dt>Npptools.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bc3a4-133">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="bc3a4-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bc3a4-134">сетмакаддрессинблоб</span><span class="sxs-lookup"><span data-stu-id="bc3a4-134">SetMacAddressInBlob</span></span>](setmacaddressinblob.md)
</dt> <dt>

[<span data-ttu-id="bc3a4-135">жетбулфромблоб</span><span class="sxs-lookup"><span data-stu-id="bc3a4-135">GetBoolFromBlob</span></span>](getboolfromblob.md)
</dt> <dt>

[<span data-ttu-id="bc3a4-136">жетклассидфромблоб</span><span class="sxs-lookup"><span data-stu-id="bc3a4-136">GetClassIDFromBlob</span></span>](getclassidfromblob.md)
</dt> <dt>

[<span data-ttu-id="bc3a4-137">жетдвордфромблоб</span><span class="sxs-lookup"><span data-stu-id="bc3a4-137">GetDwordFromBlob</span></span>](getdwordfromblob.md)
</dt> <dt>

[<span data-ttu-id="bc3a4-138">жетнетворкинфофромблоб</span><span class="sxs-lookup"><span data-stu-id="bc3a4-138">GetNetworkInfoFromBlob</span></span>](getnetworkinfofromblob.md)
</dt> <dt>

[<span data-ttu-id="bc3a4-139">жетнппаддрессфилтерфромблоб</span><span class="sxs-lookup"><span data-stu-id="bc3a4-139">GetNPPAddressFilterFromBlob</span></span>](getnppaddressfilterfromblob.md)
</dt> <dt>

[<span data-ttu-id="bc3a4-140">жетнпппаттернфилтерфромблоб</span><span class="sxs-lookup"><span data-stu-id="bc3a4-140">GetNPPPatternFilterFromBlob</span></span>](getnpppatternfilterfromblob.md)
</dt> <dt>

[<span data-ttu-id="bc3a4-141">жетнпптригжерфромблоб</span><span class="sxs-lookup"><span data-stu-id="bc3a4-141">GetNPPTriggerFromBlob</span></span>](getnpptriggerfromblob.md)
</dt> <dt>

[<span data-ttu-id="bc3a4-142">жетстрингфромблоб</span><span class="sxs-lookup"><span data-stu-id="bc3a4-142">GetStringFromBlob</span></span>](getstringfromblob.md)
</dt> <dt>

[<span data-ttu-id="bc3a4-143">жетстрингсфромблоб</span><span class="sxs-lookup"><span data-stu-id="bc3a4-143">GetStringsFromBlob</span></span>](getstringsfromblob.md)
</dt> </dl>

 

 




