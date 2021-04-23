---
description: Функция Сетбулинблоб задает логическое значение в указанном месте в большом двоичном объекте.
ms.assetid: 354d22be-b8c4-4068-8356-19b30ac188d0
title: Функция Сетбулинблоб (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SetBoolInBlob
api_type:
- DllExport
api_location:
- Npptools.dll
ms.openlocfilehash: 5cfbb9a3410d511ab143f1d77584a0144435c230
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104544879"
---
# <a name="setboolinblob-function"></a><span data-ttu-id="0d619-103">Функция Сетбулинблоб</span><span class="sxs-lookup"><span data-stu-id="0d619-103">SetBoolInBlob function</span></span>

<span data-ttu-id="0d619-104">Функция **сетбулинблоб** задает логическое значение в указанном месте в большом двоичном объекте.</span><span class="sxs-lookup"><span data-stu-id="0d619-104">The **SetBoolInBlob** function sets a Boolean value at a given location within a BLOB.</span></span>

## <a name="syntax"></a><span data-ttu-id="0d619-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="0d619-105">Syntax</span></span>


```C++
DWORD SetBoolInBlob(
  _In_       HBLOB hBlob,
  _In_ const char  *pOwnerName,
  _In_ const char  *pCategoryName,
  _In_ const char  *pTagName,
  _In_       BOOL  Bool
);
```



## <a name="parameters"></a><span data-ttu-id="0d619-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="0d619-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0d619-107">*хблоб* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="0d619-107">*hBlob* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0d619-108">Обработчик для большого двоичного объекта.</span><span class="sxs-lookup"><span data-stu-id="0d619-108">Handle to a BLOB.</span></span>

</dd> <dt>

<span data-ttu-id="0d619-109">*повнернаме* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="0d619-109">*pOwnerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0d619-110">Указатель на имя **владельца** большого двоичного объекта.</span><span class="sxs-lookup"><span data-stu-id="0d619-110">Pointer to the BLOB **Owner** name.</span></span>

</dd> <dt>

<span data-ttu-id="0d619-111">*пкатегоринаме* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="0d619-111">*pCategoryName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0d619-112">Указатель на имя **категории** BLOB-объектов.</span><span class="sxs-lookup"><span data-stu-id="0d619-112">Pointer to the BLOB **Category** name.</span></span>

</dd> <dt>

<span data-ttu-id="0d619-113">*птагнаме* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="0d619-113">*pTagName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0d619-114">Указатель на имя **тега** большого двоичного объекта.</span><span class="sxs-lookup"><span data-stu-id="0d619-114">Pointer to the BLOB **Tag** name.</span></span>

</dd> <dt>

<span data-ttu-id="0d619-115">*Bool (логическое* \[ ) окне\]</span><span class="sxs-lookup"><span data-stu-id="0d619-115">*Bool* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0d619-116">Логическое значение, заданное в заданном месте.</span><span class="sxs-lookup"><span data-stu-id="0d619-116">Boolean value that is set at the given location.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0d619-117">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="0d619-117">Return value</span></span>

<span data-ttu-id="0d619-118">Если функция выполнена успешно, возвращается значение НМЕРР \_ Success.</span><span class="sxs-lookup"><span data-stu-id="0d619-118">If the function is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="0d619-119">Если функция завершается неудачно, возвращается значение НМЕРР, указывающее на ошибку.</span><span class="sxs-lookup"><span data-stu-id="0d619-119">If the function is unsuccessful, the return value is a NMERR value that indicates the error.</span></span>

## <a name="requirements"></a><span data-ttu-id="0d619-120">Требования</span><span class="sxs-lookup"><span data-stu-id="0d619-120">Requirements</span></span>



| <span data-ttu-id="0d619-121">Требование</span><span class="sxs-lookup"><span data-stu-id="0d619-121">Requirement</span></span> | <span data-ttu-id="0d619-122">Значение</span><span class="sxs-lookup"><span data-stu-id="0d619-122">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="0d619-123">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="0d619-123">Minimum supported client</span></span><br/> | <span data-ttu-id="0d619-124">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="0d619-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="0d619-125">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="0d619-125">Minimum supported server</span></span><br/> | <span data-ttu-id="0d619-126">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="0d619-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="0d619-127">Заголовок</span><span class="sxs-lookup"><span data-stu-id="0d619-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="0d619-128"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="0d619-128"><dt>Netmon.h</dt></span></span> </dl>     |
| <span data-ttu-id="0d619-129">Библиотека</span><span class="sxs-lookup"><span data-stu-id="0d619-129">Library</span></span><br/>                  | <dl> <span data-ttu-id="0d619-130"><dt>Нпптулс. lib</dt></span><span class="sxs-lookup"><span data-stu-id="0d619-130"><dt>Npptools.lib</dt></span></span> </dl> |
| <span data-ttu-id="0d619-131">DLL</span><span class="sxs-lookup"><span data-stu-id="0d619-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0d619-132"><dt>Npptools.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0d619-132"><dt>Npptools.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0d619-133">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="0d619-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0d619-134">жетбулфромблоб</span><span class="sxs-lookup"><span data-stu-id="0d619-134">GetBoolFromBlob</span></span>](getboolfromblob.md)
</dt> <dt>

[<span data-ttu-id="0d619-135">сетклассидинблоб</span><span class="sxs-lookup"><span data-stu-id="0d619-135">SetClassIDInBlob</span></span>](setclassidinblob.md)
</dt> <dt>

[<span data-ttu-id="0d619-136">сетдвординблоб</span><span class="sxs-lookup"><span data-stu-id="0d619-136">SetDwordInBlob</span></span>](setdwordinblob.md)
</dt> <dt>

[<span data-ttu-id="0d619-137">сетмакаддрессинблоб</span><span class="sxs-lookup"><span data-stu-id="0d619-137">SetMacAddressInBlob</span></span>](setmacaddressinblob.md)
</dt> <dt>

[<span data-ttu-id="0d619-138">сетнетворкинфоинблоб</span><span class="sxs-lookup"><span data-stu-id="0d619-138">SetNetworkInfoInBlob</span></span>](setnetworkinfoinblob.md)
</dt> <dt>

[<span data-ttu-id="0d619-139">сетнппаддрессфилтеринблоб</span><span class="sxs-lookup"><span data-stu-id="0d619-139">SetNPPAddressFilterInBlob</span></span>](setnppaddressfilterinblob.md)
</dt> <dt>

[<span data-ttu-id="0d619-140">сетнпппаттернфилтеринблоб</span><span class="sxs-lookup"><span data-stu-id="0d619-140">SetNPPPatternFilterInBlob</span></span>](setnpppatternfilterinblob.md)
</dt> <dt>

[<span data-ttu-id="0d619-141">сетнпптригжеринблоб</span><span class="sxs-lookup"><span data-stu-id="0d619-141">SetNPPTriggerInBlob</span></span>](setnpptriggerinblob.md)
</dt> <dt>

[<span data-ttu-id="0d619-142">сетстрингинблоб</span><span class="sxs-lookup"><span data-stu-id="0d619-142">SetStringInBlob</span></span>](setstringinblob.md)
</dt> </dl>

 

 




