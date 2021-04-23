---
description: Задает строку в указанном месте в большом двоичном объекте.
ms.assetid: 645e6b8b-aaaf-429f-ad2f-bf4364ef4e80
title: Функция Сетстрингинблоб (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SetStringInBlob
api_type:
- DllExport
api_location:
- Npptools.dll
ms.openlocfilehash: 37278b9111818957e6d5fb3032f1bf33ad3a6ec3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104263221"
---
# <a name="setstringinblob-function"></a><span data-ttu-id="810f5-103">Функция Сетстрингинблоб</span><span class="sxs-lookup"><span data-stu-id="810f5-103">SetStringInBlob function</span></span>

<span data-ttu-id="810f5-104">Функция **сетстрингинблоб** задает строку в заданном месте в большом двоичном объекте.</span><span class="sxs-lookup"><span data-stu-id="810f5-104">The **SetStringInBlob** function sets a string at a given location within a BLOB.</span></span>

## <a name="syntax"></a><span data-ttu-id="810f5-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="810f5-105">Syntax</span></span>


```C++
DWORD SetStringInBlob(
  _In_       HBLOB hBlob,
  _In_ const char  *pOwnerName,
  _In_ const char  *pCategoryName,
  _In_ const char  *pTagName,
  _In_ const char  *pString
);
```



## <a name="parameters"></a><span data-ttu-id="810f5-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="810f5-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="810f5-107">*хблоб* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="810f5-107">*hBlob* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="810f5-108">Маркер для большого двоичного объекта.</span><span class="sxs-lookup"><span data-stu-id="810f5-108">A handle to the BLOB.</span></span>

</dd> <dt>

<span data-ttu-id="810f5-109">*повнернаме* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="810f5-109">*pOwnerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="810f5-110">Указатель на раздел **owner** большого двоичного объекта, где задана строка.</span><span class="sxs-lookup"><span data-stu-id="810f5-110">A pointer to the **Owner** section of the BLOB, where the string is set.</span></span>

</dd> <dt>

<span data-ttu-id="810f5-111">*пкатегоринаме* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="810f5-111">*pCategoryName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="810f5-112">Указатель на раздел **категории** большого двоичного объекта, где задана строка.</span><span class="sxs-lookup"><span data-stu-id="810f5-112">A pointer to the **Category** section of the BLOB, where the string is set.</span></span>

</dd> <dt>

<span data-ttu-id="810f5-113">*птагнаме* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="810f5-113">*pTagName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="810f5-114">Указатель на **тег** запрошенной строки.</span><span class="sxs-lookup"><span data-stu-id="810f5-114">A pointer to the **Tag** of the requested string.</span></span>

</dd> <dt>

<span data-ttu-id="810f5-115">*пстринг* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="810f5-115">*pString* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="810f5-116">Указатель на переменную, в которой будет возвращен указатель на строку.</span><span class="sxs-lookup"><span data-stu-id="810f5-116">A pointer to the variable where a pointer to the string will be returned.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="810f5-117">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="810f5-117">Return value</span></span>

<span data-ttu-id="810f5-118">Если функция выполнена успешно, возвращается значение НМЕРР \_ Success.</span><span class="sxs-lookup"><span data-stu-id="810f5-118">If the function is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="810f5-119">Если функция завершается неудачно, возвращается значение НМЕРР, указывающее на проблему.</span><span class="sxs-lookup"><span data-stu-id="810f5-119">If the function is unsuccessful, the return value is a NMERR value that indicates the problem.</span></span>

<span data-ttu-id="810f5-120">Если указанные сведения о **владельце**, **категории** или **теге** не существуют, возвращаемое значение является \_ записью большого двоичного объекта нмерр \_ \_ \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="810f5-120">If the specified **Owner**, **Category**, or **Tag** information does not exist, the return value is NMERR\_BLOB\_ENTRY\_DOES\_NOT\_EXIST.</span></span>

## <a name="requirements"></a><span data-ttu-id="810f5-121">Требования</span><span class="sxs-lookup"><span data-stu-id="810f5-121">Requirements</span></span>



| <span data-ttu-id="810f5-122">Требование</span><span class="sxs-lookup"><span data-stu-id="810f5-122">Requirement</span></span> | <span data-ttu-id="810f5-123">Значение</span><span class="sxs-lookup"><span data-stu-id="810f5-123">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="810f5-124">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="810f5-124">Minimum supported client</span></span><br/> | <span data-ttu-id="810f5-125">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="810f5-125">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="810f5-126">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="810f5-126">Minimum supported server</span></span><br/> | <span data-ttu-id="810f5-127">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="810f5-127">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="810f5-128">Заголовок</span><span class="sxs-lookup"><span data-stu-id="810f5-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="810f5-129"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="810f5-129"><dt>Netmon.h</dt></span></span> </dl>     |
| <span data-ttu-id="810f5-130">Библиотека</span><span class="sxs-lookup"><span data-stu-id="810f5-130">Library</span></span><br/>                  | <dl> <span data-ttu-id="810f5-131"><dt>Нпптулс. lib</dt></span><span class="sxs-lookup"><span data-stu-id="810f5-131"><dt>Npptools.lib</dt></span></span> </dl> |
| <span data-ttu-id="810f5-132">DLL</span><span class="sxs-lookup"><span data-stu-id="810f5-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="810f5-133"><dt>Npptools.dll</dt></span><span class="sxs-lookup"><span data-stu-id="810f5-133"><dt>Npptools.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="810f5-134">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="810f5-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="810f5-135">жетстрингфромблоб</span><span class="sxs-lookup"><span data-stu-id="810f5-135">GetStringFromBlob</span></span>](getstringfromblob.md)
</dt> <dt>

[<span data-ttu-id="810f5-136">сетбулинблоб</span><span class="sxs-lookup"><span data-stu-id="810f5-136">SetBoolInBlob</span></span>](setboolinblob.md)
</dt> <dt>

[<span data-ttu-id="810f5-137">сетклассидинблоб</span><span class="sxs-lookup"><span data-stu-id="810f5-137">SetClassIDInBlob</span></span>](setclassidinblob.md)
</dt> <dt>

[<span data-ttu-id="810f5-138">сетдвординблоб</span><span class="sxs-lookup"><span data-stu-id="810f5-138">SetDwordInBlob</span></span>](setdwordinblob.md)
</dt> <dt>

[<span data-ttu-id="810f5-139">сетмакаддрессинблоб</span><span class="sxs-lookup"><span data-stu-id="810f5-139">SetMacAddressInBlob</span></span>](setmacaddressinblob.md)
</dt> <dt>

[<span data-ttu-id="810f5-140">сетнетворкинфоинблоб</span><span class="sxs-lookup"><span data-stu-id="810f5-140">SetNetworkInfoInBlob</span></span>](setnetworkinfoinblob.md)
</dt> <dt>

[<span data-ttu-id="810f5-141">сетнппаддрессфилтеринблоб</span><span class="sxs-lookup"><span data-stu-id="810f5-141">SetNPPAddressFilterInBlob</span></span>](setnppaddressfilterinblob.md)
</dt> <dt>

[<span data-ttu-id="810f5-142">сетнпппаттернфилтеринблоб</span><span class="sxs-lookup"><span data-stu-id="810f5-142">SetNPPPatternFilterInBlob</span></span>](setnpppatternfilterinblob.md)
</dt> <dt>

[<span data-ttu-id="810f5-143">сетнпптригжеринблоб</span><span class="sxs-lookup"><span data-stu-id="810f5-143">SetNPPTriggerInBlob</span></span>](setnpptriggerinblob.md)
</dt> </dl>

 

 




