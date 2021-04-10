---
description: Функция Жетклассидфромблоб извлекает значение идентификатора именованного класса из большого двоичного объекта.
ms.assetid: fef29a42-ccd3-4655-958c-d150e5bcd0d7
title: Функция Жетклассидфромблоб (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetClassIDFromBlob
api_type:
- DllExport
api_location:
- Npptools.dll
ms.openlocfilehash: 70122422c47a986058322ca8d17082093e02a4b6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104143792"
---
# <a name="getclassidfromblob-function"></a><span data-ttu-id="4adcb-103">Функция Жетклассидфромблоб</span><span class="sxs-lookup"><span data-stu-id="4adcb-103">GetClassIDFromBlob function</span></span>

<span data-ttu-id="4adcb-104">Функция **жетклассидфромблоб** извлекает значение идентификатора именованного класса из большого двоичного объекта.</span><span class="sxs-lookup"><span data-stu-id="4adcb-104">The **GetClassIDFromBlob** function retrieves a named class identifier value from a BLOB.</span></span>

## <a name="syntax"></a><span data-ttu-id="4adcb-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="4adcb-105">Syntax</span></span>


```C++
DWORD GetClassIDFromBlob(
  _In_        HBLOB hBlob,
  _In_  const char  *pOwnerName,
  _In_  const char  *pCategoryName,
  _In_  const char  *pTagName,
  _Out_       CLSID *pClsID
);
```



## <a name="parameters"></a><span data-ttu-id="4adcb-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="4adcb-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4adcb-107">*хблоб* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="4adcb-107">*hBlob* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4adcb-108">Обработчик для большого двоичного объекта.</span><span class="sxs-lookup"><span data-stu-id="4adcb-108">Handle to a BLOB.</span></span>

</dd> <dt>

<span data-ttu-id="4adcb-109">*повнернаме* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="4adcb-109">*pOwnerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4adcb-110">Указатель на имя владельца большого двоичного объекта.</span><span class="sxs-lookup"><span data-stu-id="4adcb-110">Pointer to the BLOB owner name.</span></span>

</dd> <dt>

<span data-ttu-id="4adcb-111">*пкатегоринаме* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="4adcb-111">*pCategoryName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4adcb-112">Указатель на имя категории BLOB-объектов.</span><span class="sxs-lookup"><span data-stu-id="4adcb-112">Pointer to the BLOB category name.</span></span>

</dd> <dt>

<span data-ttu-id="4adcb-113">*птагнаме* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="4adcb-113">*pTagName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4adcb-114">Указатель на имя тега большого двоичного объекта.</span><span class="sxs-lookup"><span data-stu-id="4adcb-114">Pointer to the BLOB tag name.</span></span>

</dd> <dt>

<span data-ttu-id="4adcb-115">*пклсид* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="4adcb-115">*pClsID* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="4adcb-116">Указатель на идентификатор класса BLOB-объекта.</span><span class="sxs-lookup"><span data-stu-id="4adcb-116">Pointer to the BLOB class identifier.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4adcb-117">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="4adcb-117">Return value</span></span>

<span data-ttu-id="4adcb-118">Если функция выполнена успешно, возвращается значение НМЕРР \_ Success.</span><span class="sxs-lookup"><span data-stu-id="4adcb-118">If the function is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="4adcb-119">Если функция завершается неудачно, возвращается значение НМЕРР, описывающее ошибку.</span><span class="sxs-lookup"><span data-stu-id="4adcb-119">If the function is unsuccessful, the return value is a NMERR value that describes the error.</span></span>

## <a name="requirements"></a><span data-ttu-id="4adcb-120">Требования</span><span class="sxs-lookup"><span data-stu-id="4adcb-120">Requirements</span></span>



| <span data-ttu-id="4adcb-121">Требование</span><span class="sxs-lookup"><span data-stu-id="4adcb-121">Requirement</span></span> | <span data-ttu-id="4adcb-122">Значение</span><span class="sxs-lookup"><span data-stu-id="4adcb-122">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="4adcb-123">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="4adcb-123">Minimum supported client</span></span><br/> | <span data-ttu-id="4adcb-124">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="4adcb-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="4adcb-125">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="4adcb-125">Minimum supported server</span></span><br/> | <span data-ttu-id="4adcb-126">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="4adcb-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="4adcb-127">Заголовок</span><span class="sxs-lookup"><span data-stu-id="4adcb-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="4adcb-128"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="4adcb-128"><dt>Netmon.h</dt></span></span> </dl>     |
| <span data-ttu-id="4adcb-129">Библиотека</span><span class="sxs-lookup"><span data-stu-id="4adcb-129">Library</span></span><br/>                  | <dl> <span data-ttu-id="4adcb-130"><dt>Нпптулс. lib</dt></span><span class="sxs-lookup"><span data-stu-id="4adcb-130"><dt>Npptools.lib</dt></span></span> </dl> |
| <span data-ttu-id="4adcb-131">DLL</span><span class="sxs-lookup"><span data-stu-id="4adcb-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4adcb-132"><dt>Npptools.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4adcb-132"><dt>Npptools.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4adcb-133">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="4adcb-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4adcb-134">сетклассидинблоб</span><span class="sxs-lookup"><span data-stu-id="4adcb-134">SetClassIDInBlob</span></span>](setclassidinblob.md)
</dt> <dt>

[<span data-ttu-id="4adcb-135">жетбулфромблоб</span><span class="sxs-lookup"><span data-stu-id="4adcb-135">GetBoolFromBlob</span></span>](getboolfromblob.md)
</dt> <dt>

[<span data-ttu-id="4adcb-136">жетдвордфромблоб</span><span class="sxs-lookup"><span data-stu-id="4adcb-136">GetDwordFromBlob</span></span>](getdwordfromblob.md)
</dt> <dt>

[<span data-ttu-id="4adcb-137">жетмакаддрессфромблоб</span><span class="sxs-lookup"><span data-stu-id="4adcb-137">GetMacAddressFromBlob</span></span>](getmacaddressfromblob.md)
</dt> <dt>

[<span data-ttu-id="4adcb-138">жетнетворкинфофромблоб</span><span class="sxs-lookup"><span data-stu-id="4adcb-138">GetNetworkInfoFromBlob</span></span>](getnetworkinfofromblob.md)
</dt> <dt>

[<span data-ttu-id="4adcb-139">жетнппаддрессфилтерфромблоб</span><span class="sxs-lookup"><span data-stu-id="4adcb-139">GetNPPAddressFilterFromBlob</span></span>](getnppaddressfilterfromblob.md)
</dt> <dt>

[<span data-ttu-id="4adcb-140">жетнпппаттернфилтерфромблоб</span><span class="sxs-lookup"><span data-stu-id="4adcb-140">GetNPPPatternFilterFromBlob</span></span>](getnpppatternfilterfromblob.md)
</dt> <dt>

[<span data-ttu-id="4adcb-141">жетнпптригжерфромблоб</span><span class="sxs-lookup"><span data-stu-id="4adcb-141">GetNPPTriggerFromBlob</span></span>](getnpptriggerfromblob.md)
</dt> <dt>

[<span data-ttu-id="4adcb-142">жетстрингфромблоб</span><span class="sxs-lookup"><span data-stu-id="4adcb-142">GetStringFromBlob</span></span>](getstringfromblob.md)
</dt> <dt>

[<span data-ttu-id="4adcb-143">жетстрингсфромблоб</span><span class="sxs-lookup"><span data-stu-id="4adcb-143">GetStringsFromBlob</span></span>](getstringsfromblob.md)
</dt> </dl>

 

 




