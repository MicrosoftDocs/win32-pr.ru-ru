---
description: Функция Сетдвординблоб задает именованное значение DWORD большого двоичного объекта.
ms.assetid: 9174cd5c-4442-4fbe-8dc7-f8a74e1cc85d
title: Функция Сетдвординблоб (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SetDwordInBlob
api_type:
- DllExport
api_location:
- Npptools.dll
ms.openlocfilehash: 9bca0efe61824c6fb8dd41b0b241791b6303799d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105673544"
---
# <a name="setdwordinblob-function"></a><span data-ttu-id="3ce05-103">Функция Сетдвординблоб</span><span class="sxs-lookup"><span data-stu-id="3ce05-103">SetDwordInBlob function</span></span>

<span data-ttu-id="3ce05-104">Функция **сетдвординблоб** задает именованное значение **DWORD** большого двоичного объекта.</span><span class="sxs-lookup"><span data-stu-id="3ce05-104">The **SetDwordInBlob** function sets the named **DWORD** value of a BLOB.</span></span>

## <a name="syntax"></a><span data-ttu-id="3ce05-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="3ce05-105">Syntax</span></span>


```C++
DWORD SetDwordInBlob(
  _In_       HBLOB hBlob,
  _In_ const char  *pOwnerName,
  _In_ const char  *pCategoryName,
  _In_ const char  *pTagName,
  _In_       DWORD Dword
);
```



## <a name="parameters"></a><span data-ttu-id="3ce05-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="3ce05-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3ce05-107">*хблоб* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="3ce05-107">*hBlob* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3ce05-108">Обрабатываемый набор больших двоичных объектов.</span><span class="sxs-lookup"><span data-stu-id="3ce05-108">Handle to a BLOB being set.</span></span>

</dd> <dt>

<span data-ttu-id="3ce05-109">*повнернаме* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="3ce05-109">*pOwnerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3ce05-110">Указатель на устанавливаемое имя **владельца** большого двоичного объекта.</span><span class="sxs-lookup"><span data-stu-id="3ce05-110">Pointer to the BLOB **Owner** name being set.</span></span>

</dd> <dt>

<span data-ttu-id="3ce05-111">*пкатегоринаме* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="3ce05-111">*pCategoryName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3ce05-112">Указатель на устанавливаемое имя **категории** BLOB-объектов.</span><span class="sxs-lookup"><span data-stu-id="3ce05-112">Pointer to the BLOB **Category** name being set.</span></span>

</dd> <dt>

<span data-ttu-id="3ce05-113">*птагнаме* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="3ce05-113">*pTagName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3ce05-114">Указатель на заданный имя **тега** большого двоичного объекта.</span><span class="sxs-lookup"><span data-stu-id="3ce05-114">Pointer to the BLOB **Tag** name being set.</span></span>

</dd> <dt>

<span data-ttu-id="3ce05-115">*Параметр DWORD* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="3ce05-115">*Dword* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3ce05-116">Значение **DWORD** УСТАНАВЛИВАЕМОГО большого двоичного объекта.</span><span class="sxs-lookup"><span data-stu-id="3ce05-116">**DWORD** value of the BLOB being set.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3ce05-117">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="3ce05-117">Return value</span></span>

<span data-ttu-id="3ce05-118">Если функция выполнена успешно, возвращается значение НМЕРР \_ Success.</span><span class="sxs-lookup"><span data-stu-id="3ce05-118">If the function is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="3ce05-119">Если функция завершается неудачно, возвращается значение НМЕРР, указывающее на ошибку.</span><span class="sxs-lookup"><span data-stu-id="3ce05-119">If the function is unsuccessful, the return value is a NMERR value that indicates the error.</span></span>

## <a name="requirements"></a><span data-ttu-id="3ce05-120">Требования</span><span class="sxs-lookup"><span data-stu-id="3ce05-120">Requirements</span></span>



| <span data-ttu-id="3ce05-121">Требование</span><span class="sxs-lookup"><span data-stu-id="3ce05-121">Requirement</span></span> | <span data-ttu-id="3ce05-122">Значение</span><span class="sxs-lookup"><span data-stu-id="3ce05-122">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="3ce05-123">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="3ce05-123">Minimum supported client</span></span><br/> | <span data-ttu-id="3ce05-124">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="3ce05-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="3ce05-125">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="3ce05-125">Minimum supported server</span></span><br/> | <span data-ttu-id="3ce05-126">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="3ce05-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="3ce05-127">Заголовок</span><span class="sxs-lookup"><span data-stu-id="3ce05-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="3ce05-128"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="3ce05-128"><dt>Netmon.h</dt></span></span> </dl>     |
| <span data-ttu-id="3ce05-129">Библиотека</span><span class="sxs-lookup"><span data-stu-id="3ce05-129">Library</span></span><br/>                  | <dl> <span data-ttu-id="3ce05-130"><dt>Нпптулс. lib</dt></span><span class="sxs-lookup"><span data-stu-id="3ce05-130"><dt>Npptools.lib</dt></span></span> </dl> |
| <span data-ttu-id="3ce05-131">DLL</span><span class="sxs-lookup"><span data-stu-id="3ce05-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3ce05-132"><dt>Npptools.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3ce05-132"><dt>Npptools.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3ce05-133">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="3ce05-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3ce05-134">жетдвордфромблоб</span><span class="sxs-lookup"><span data-stu-id="3ce05-134">GetDwordFromBlob</span></span>](getdwordfromblob.md)
</dt> <dt>

[<span data-ttu-id="3ce05-135">сетбулинблоб</span><span class="sxs-lookup"><span data-stu-id="3ce05-135">SetBoolInBlob</span></span>](setboolinblob.md)
</dt> <dt>

[<span data-ttu-id="3ce05-136">сетклассидинблоб</span><span class="sxs-lookup"><span data-stu-id="3ce05-136">SetClassIDInBlob</span></span>](setclassidinblob.md)
</dt> <dt>

[<span data-ttu-id="3ce05-137">сетмакаддрессинблоб</span><span class="sxs-lookup"><span data-stu-id="3ce05-137">SetMacAddressInBlob</span></span>](setmacaddressinblob.md)
</dt> <dt>

[<span data-ttu-id="3ce05-138">сетнетворкинфоинблоб</span><span class="sxs-lookup"><span data-stu-id="3ce05-138">SetNetworkInfoInBlob</span></span>](setnetworkinfoinblob.md)
</dt> <dt>

[<span data-ttu-id="3ce05-139">сетнппаддрессфилтеринблоб</span><span class="sxs-lookup"><span data-stu-id="3ce05-139">SetNPPAddressFilterInBlob</span></span>](setnppaddressfilterinblob.md)
</dt> <dt>

[<span data-ttu-id="3ce05-140">сетнпппаттернфилтеринблоб</span><span class="sxs-lookup"><span data-stu-id="3ce05-140">SetNPPPatternFilterInBlob</span></span>](setnpppatternfilterinblob.md)
</dt> <dt>

[<span data-ttu-id="3ce05-141">сетнпптригжеринблоб</span><span class="sxs-lookup"><span data-stu-id="3ce05-141">SetNPPTriggerInBlob</span></span>](setnpptriggerinblob.md)
</dt> <dt>

[<span data-ttu-id="3ce05-142">сетстрингинблоб</span><span class="sxs-lookup"><span data-stu-id="3ce05-142">SetStringInBlob</span></span>](setstringinblob.md)
</dt> </dl>

 

 




