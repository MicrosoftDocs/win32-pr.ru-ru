---
description: Функция Сетклассидинблоб задает значение идентификатора именованного класса для большого двоичного объекта.
ms.assetid: d17dd48b-2e35-4c57-ba33-688180910b63
title: Функция Сетклассидинблоб (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SetClassIDInBlob
api_type:
- DllExport
api_location:
- Npptools.dll
ms.openlocfilehash: b617c39767038bac51d749a640ebcf2301e0c63f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105673543"
---
# <a name="setclassidinblob-function"></a><span data-ttu-id="456c5-103">Функция Сетклассидинблоб</span><span class="sxs-lookup"><span data-stu-id="456c5-103">SetClassIDInBlob function</span></span>

<span data-ttu-id="456c5-104">Функция **сетклассидинблоб** задает значение идентификатора именованного класса для большого двоичного объекта.</span><span class="sxs-lookup"><span data-stu-id="456c5-104">The **SetClassIDInBlob** function sets the named class identifier value of a BLOB.</span></span>

## <a name="syntax"></a><span data-ttu-id="456c5-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="456c5-105">Syntax</span></span>


```C++
DWORD SetClassIDInBlob(
  _In_       HBLOB hBlob,
  _In_ const char  *pOwnerName,
  _In_ const char  *pCategoryName,
  _In_ const char  *pTagName,
  _In_ const CLSID *pClsID
);
```



## <a name="parameters"></a><span data-ttu-id="456c5-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="456c5-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="456c5-107">*хблоб* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="456c5-107">*hBlob* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="456c5-108">Обработчик для большого двоичного объекта.</span><span class="sxs-lookup"><span data-stu-id="456c5-108">Handle to a BLOB.</span></span>

</dd> <dt>

<span data-ttu-id="456c5-109">*повнернаме* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="456c5-109">*pOwnerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="456c5-110">Указатель на заданное имя **владельца** большого двоичного объекта.</span><span class="sxs-lookup"><span data-stu-id="456c5-110">Pointer to the BLOB **Owner** name that is set.</span></span>

</dd> <dt>

<span data-ttu-id="456c5-111">*пкатегоринаме* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="456c5-111">*pCategoryName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="456c5-112">Указатель на заданное имя **категории** BLOB-объектов.</span><span class="sxs-lookup"><span data-stu-id="456c5-112">Pointer to the BLOB **Category** name that is set.</span></span>

</dd> <dt>

<span data-ttu-id="456c5-113">*птагнаме* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="456c5-113">*pTagName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="456c5-114">Указатель на заданное имя **ТЕГА** BLOB-объекта.</span><span class="sxs-lookup"><span data-stu-id="456c5-114">Pointer to the BLOB **Tag** name that is set.</span></span>

</dd> <dt>

<span data-ttu-id="456c5-115">*пклсид* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="456c5-115">*pClsID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="456c5-116">Указатель на идентификатор класса заданного большого двоичного объекта.</span><span class="sxs-lookup"><span data-stu-id="456c5-116">Pointer to the class identifier of the BLOB that is set.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="456c5-117">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="456c5-117">Return value</span></span>

<span data-ttu-id="456c5-118">Если функция выполнена успешно, возвращается значение НМЕРР \_ Success.</span><span class="sxs-lookup"><span data-stu-id="456c5-118">If the function is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="456c5-119">Если функция завершается неудачно, возвращается значение НМЕРР, указывающее на ошибку.</span><span class="sxs-lookup"><span data-stu-id="456c5-119">If the function is unsuccessful, the return value is a NMERR value that indicates the error.</span></span>

## <a name="requirements"></a><span data-ttu-id="456c5-120">Требования</span><span class="sxs-lookup"><span data-stu-id="456c5-120">Requirements</span></span>



| <span data-ttu-id="456c5-121">Требование</span><span class="sxs-lookup"><span data-stu-id="456c5-121">Requirement</span></span> | <span data-ttu-id="456c5-122">Значение</span><span class="sxs-lookup"><span data-stu-id="456c5-122">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="456c5-123">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="456c5-123">Minimum supported client</span></span><br/> | <span data-ttu-id="456c5-124">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="456c5-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="456c5-125">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="456c5-125">Minimum supported server</span></span><br/> | <span data-ttu-id="456c5-126">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="456c5-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="456c5-127">Заголовок</span><span class="sxs-lookup"><span data-stu-id="456c5-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="456c5-128"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="456c5-128"><dt>Netmon.h</dt></span></span> </dl>     |
| <span data-ttu-id="456c5-129">Библиотека</span><span class="sxs-lookup"><span data-stu-id="456c5-129">Library</span></span><br/>                  | <dl> <span data-ttu-id="456c5-130"><dt>Нпптулс. lib</dt></span><span class="sxs-lookup"><span data-stu-id="456c5-130"><dt>Npptools.lib</dt></span></span> </dl> |
| <span data-ttu-id="456c5-131">DLL</span><span class="sxs-lookup"><span data-stu-id="456c5-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="456c5-132"><dt>Npptools.dll</dt></span><span class="sxs-lookup"><span data-stu-id="456c5-132"><dt>Npptools.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="456c5-133">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="456c5-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="456c5-134">жетклассидфромблоб</span><span class="sxs-lookup"><span data-stu-id="456c5-134">GetClassIDFromBlob</span></span>](getclassidfromblob.md)
</dt> <dt>

[<span data-ttu-id="456c5-135">сетбулинблоб</span><span class="sxs-lookup"><span data-stu-id="456c5-135">SetBoolInBlob</span></span>](setboolinblob.md)
</dt> <dt>

[<span data-ttu-id="456c5-136">сетдвординблоб</span><span class="sxs-lookup"><span data-stu-id="456c5-136">SetDwordInBlob</span></span>](setdwordinblob.md)
</dt> <dt>

[<span data-ttu-id="456c5-137">сетмакаддрессинблоб</span><span class="sxs-lookup"><span data-stu-id="456c5-137">SetMacAddressInBlob</span></span>](setmacaddressinblob.md)
</dt> <dt>

[<span data-ttu-id="456c5-138">сетнетворкинфоинблоб</span><span class="sxs-lookup"><span data-stu-id="456c5-138">SetNetworkInfoInBlob</span></span>](setnetworkinfoinblob.md)
</dt> <dt>

[<span data-ttu-id="456c5-139">сетнппаддрессфилтеринблоб</span><span class="sxs-lookup"><span data-stu-id="456c5-139">SetNPPAddressFilterInBlob</span></span>](setnppaddressfilterinblob.md)
</dt> <dt>

[<span data-ttu-id="456c5-140">сетнпппаттернфилтеринблоб</span><span class="sxs-lookup"><span data-stu-id="456c5-140">SetNPPPatternFilterInBlob</span></span>](setnpppatternfilterinblob.md)
</dt> <dt>

[<span data-ttu-id="456c5-141">сетнпптригжеринблоб</span><span class="sxs-lookup"><span data-stu-id="456c5-141">SetNPPTriggerInBlob</span></span>](setnpptriggerinblob.md)
</dt> <dt>

[<span data-ttu-id="456c5-142">сетстрингинблоб</span><span class="sxs-lookup"><span data-stu-id="456c5-142">SetStringInBlob</span></span>](setstringinblob.md)
</dt> </dl>

 

 




