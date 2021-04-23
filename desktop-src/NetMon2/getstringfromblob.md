---
description: Возвращает строку, расположенную в заданной позиции в большом двоичном объекте.
ms.assetid: 5930a30b-f0ed-4d5b-a0ba-6cead55c2fcd
title: Функция Жетстрингфромблоб (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetStringFromBlob
api_type:
- DllExport
api_location:
- Npptools.dll
ms.openlocfilehash: 475600fb6128b5dbbaf9333f8c550351831f0a0f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104496995"
---
# <a name="getstringfromblob-function"></a><span data-ttu-id="14a63-103">Функция Жетстрингфромблоб</span><span class="sxs-lookup"><span data-stu-id="14a63-103">GetStringFromBlob function</span></span>

<span data-ttu-id="14a63-104">Функция **жетстрингфромблоб** возвращает строку, расположенную в заданной позиции в большом двоичном объекте.</span><span class="sxs-lookup"><span data-stu-id="14a63-104">The **GetStringFromBlob** function returns a string located at a given position within a BLOB.</span></span>

## <a name="syntax"></a><span data-ttu-id="14a63-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="14a63-105">Syntax</span></span>


```C++
DWORD GetStringFromBlob(
  _In_        HBLOB hBlob,
  _In_  const char  *pOwnerName,
  _In_  const char  *pCategoryName,
  _In_  const char  *pTagName,
  _Out_ const char  **ppString
);
```



## <a name="parameters"></a><span data-ttu-id="14a63-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="14a63-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="14a63-107">*хблоб* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="14a63-107">*hBlob* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="14a63-108">Маркер для большого двоичного объекта.</span><span class="sxs-lookup"><span data-stu-id="14a63-108">A handle to the BLOB.</span></span>

</dd> <dt>

<span data-ttu-id="14a63-109">*повнернаме* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="14a63-109">*pOwnerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="14a63-110">Раздел **владельца** большого двоичного объекта, где находится строка.</span><span class="sxs-lookup"><span data-stu-id="14a63-110">A BLOB **Owner** section where the string is located.</span></span>

</dd> <dt>

<span data-ttu-id="14a63-111">*пкатегоринаме* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="14a63-111">*pCategoryName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="14a63-112">Раздел **категории** BLOB-объектов, в котором находится строка.</span><span class="sxs-lookup"><span data-stu-id="14a63-112">A BLOB **Category** section where the string is located.</span></span>

</dd> <dt>

<span data-ttu-id="14a63-113">*птагнаме* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="14a63-113">*pTagName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="14a63-114">**Тег** запрошенной строки.</span><span class="sxs-lookup"><span data-stu-id="14a63-114">The **Tag** of the requested string.</span></span>

</dd> <dt>

<span data-ttu-id="14a63-115">*ппстринг* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="14a63-115">*ppString* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="14a63-116">Указатель на переменную, указывающую на возвращаемую строку.</span><span class="sxs-lookup"><span data-stu-id="14a63-116">A pointer to a variable that points to the returned string.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="14a63-117">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="14a63-117">Return value</span></span>

<span data-ttu-id="14a63-118">Если функция выполнена успешно, возвращается значение НМЕРР \_ Success.</span><span class="sxs-lookup"><span data-stu-id="14a63-118">If the function is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="14a63-119">Если функция завершается неудачно, возвращается значение НМЕРР, указывающее на ошибку.</span><span class="sxs-lookup"><span data-stu-id="14a63-119">If the function is unsuccessful, the return value is a NMERR value that indicates the error.</span></span>

<span data-ttu-id="14a63-120">Если указанный **владелец**, **Категория** или данные **тега** не существуют, функция возвращает **\_ запись BLOB-объекта нмерр \_ \_ \_ не \_ существует**.</span><span class="sxs-lookup"><span data-stu-id="14a63-120">If the specified **Owner**, **Category**, or **Tag** data does not exist, the function returns **NMERR\_BLOB\_ENTRY\_DOES\_NOT\_EXIST**.</span></span>

## <a name="requirements"></a><span data-ttu-id="14a63-121">Требования</span><span class="sxs-lookup"><span data-stu-id="14a63-121">Requirements</span></span>



| <span data-ttu-id="14a63-122">Требование</span><span class="sxs-lookup"><span data-stu-id="14a63-122">Requirement</span></span> | <span data-ttu-id="14a63-123">Значение</span><span class="sxs-lookup"><span data-stu-id="14a63-123">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="14a63-124">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="14a63-124">Minimum supported client</span></span><br/> | <span data-ttu-id="14a63-125">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="14a63-125">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="14a63-126">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="14a63-126">Minimum supported server</span></span><br/> | <span data-ttu-id="14a63-127">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="14a63-127">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="14a63-128">Заголовок</span><span class="sxs-lookup"><span data-stu-id="14a63-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="14a63-129"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="14a63-129"><dt>Netmon.h</dt></span></span> </dl>     |
| <span data-ttu-id="14a63-130">Библиотека</span><span class="sxs-lookup"><span data-stu-id="14a63-130">Library</span></span><br/>                  | <dl> <span data-ttu-id="14a63-131"><dt>Нпптулс. lib</dt></span><span class="sxs-lookup"><span data-stu-id="14a63-131"><dt>Npptools.lib</dt></span></span> </dl> |
| <span data-ttu-id="14a63-132">DLL</span><span class="sxs-lookup"><span data-stu-id="14a63-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="14a63-133"><dt>Npptools.dll</dt></span><span class="sxs-lookup"><span data-stu-id="14a63-133"><dt>Npptools.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="14a63-134">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="14a63-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="14a63-135">сетстрингинблоб</span><span class="sxs-lookup"><span data-stu-id="14a63-135">SetStringInBlob</span></span>](setstringinblob.md)
</dt> <dt>

[<span data-ttu-id="14a63-136">жетбулфромблоб</span><span class="sxs-lookup"><span data-stu-id="14a63-136">GetBoolFromBlob</span></span>](getboolfromblob.md)
</dt> <dt>

[<span data-ttu-id="14a63-137">жетклассидфромблоб</span><span class="sxs-lookup"><span data-stu-id="14a63-137">GetClassIDFromBlob</span></span>](getclassidfromblob.md)
</dt> <dt>

[<span data-ttu-id="14a63-138">жетдвордфромблоб</span><span class="sxs-lookup"><span data-stu-id="14a63-138">GetDwordFromBlob</span></span>](getdwordfromblob.md)
</dt> <dt>

[<span data-ttu-id="14a63-139">жетмакаддрессфромблоб</span><span class="sxs-lookup"><span data-stu-id="14a63-139">GetMacAddressFromBlob</span></span>](getmacaddressfromblob.md)
</dt> <dt>

[<span data-ttu-id="14a63-140">жетнетворкинфофромблоб</span><span class="sxs-lookup"><span data-stu-id="14a63-140">GetNetworkInfoFromBlob</span></span>](getnetworkinfofromblob.md)
</dt> <dt>

[<span data-ttu-id="14a63-141">жетнппаддрессфилтерфромблоб</span><span class="sxs-lookup"><span data-stu-id="14a63-141">GetNPPAddressFilterFromBlob</span></span>](getnppaddressfilterfromblob.md)
</dt> <dt>

[<span data-ttu-id="14a63-142">жетнпппаттернфилтерфромблоб</span><span class="sxs-lookup"><span data-stu-id="14a63-142">GetNPPPatternFilterFromBlob</span></span>](getnpppatternfilterfromblob.md)
</dt> <dt>

[<span data-ttu-id="14a63-143">жетнпптригжерфромблоб</span><span class="sxs-lookup"><span data-stu-id="14a63-143">GetNPPTriggerFromBlob</span></span>](getnpptriggerfromblob.md)
</dt> <dt>

[<span data-ttu-id="14a63-144">жетстрингсфромблоб</span><span class="sxs-lookup"><span data-stu-id="14a63-144">GetStringsFromBlob</span></span>](getstringsfromblob.md)
</dt> </dl>

 

 




