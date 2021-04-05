---
description: Функция Сетмакаддрессинблоб задает запрошенный MAC-адрес большого двоичного объекта.
ms.assetid: f44d0cec-ced7-4d2a-a58e-aeb476bfe800
title: Функция Сетмакаддрессинблоб (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SetMacAddressInBlob
api_type:
- DllExport
api_location:
- Npptools.dll
ms.openlocfilehash: 2183f5635dcdb15362a86a77ae2b3c109c71dbd5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103911316"
---
# <a name="setmacaddressinblob-function"></a><span data-ttu-id="49191-103">Функция Сетмакаддрессинблоб</span><span class="sxs-lookup"><span data-stu-id="49191-103">SetMacAddressInBlob function</span></span>

<span data-ttu-id="49191-104">Функция **сетмакаддрессинблоб** задает ЗАПРОШЕННЫЙ Mac-адрес большого двоичного объекта.</span><span class="sxs-lookup"><span data-stu-id="49191-104">The **SetMacAddressInBlob** function sets the requested MAC address of a BLOB.</span></span>

## <a name="syntax"></a><span data-ttu-id="49191-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="49191-105">Syntax</span></span>


```C++
DWORD SetMacAddressInBlob(
  _In_       HBLOB hBlob,
  _In_ const char  *pOwnerName,
  _In_ const char  *pCategoryName,
  _In_ const char  *pTagName,
  _In_ const BYTE  *pMacAddress
);
```



## <a name="parameters"></a><span data-ttu-id="49191-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="49191-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="49191-107">*хблоб* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="49191-107">*hBlob* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="49191-108">Обрабатываемый набор больших двоичных объектов.</span><span class="sxs-lookup"><span data-stu-id="49191-108">Handle to the BLOB being set.</span></span>

</dd> <dt>

<span data-ttu-id="49191-109">*повнернаме* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="49191-109">*pOwnerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="49191-110">Указатель на устанавливаемое имя **владельца** большого двоичного объекта.</span><span class="sxs-lookup"><span data-stu-id="49191-110">Pointer to the BLOB **Owner** name being set.</span></span>

</dd> <dt>

<span data-ttu-id="49191-111">*пкатегоринаме* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="49191-111">*pCategoryName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="49191-112">Указатель на устанавливаемое имя **категории** BLOB-объектов.</span><span class="sxs-lookup"><span data-stu-id="49191-112">Pointer to the BLOB **Category** name being set.</span></span>

</dd> <dt>

<span data-ttu-id="49191-113">*птагнаме* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="49191-113">*pTagName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="49191-114">Указатель на заданный имя **тега** большого двоичного объекта.</span><span class="sxs-lookup"><span data-stu-id="49191-114">Pointer to the BLOB **Tag** name being set.</span></span>

</dd> <dt>

<span data-ttu-id="49191-115">*пмакаддресс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="49191-115">*pMacAddress* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="49191-116">Указатель на MAC-адрес устанавливаемого большого двоичного объекта.</span><span class="sxs-lookup"><span data-stu-id="49191-116">Pointer to the MAC address of the BLOB being set.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="49191-117">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="49191-117">Return value</span></span>

<span data-ttu-id="49191-118">Если функция выполнена успешно, возвращается значение НМЕРР \_ Success.</span><span class="sxs-lookup"><span data-stu-id="49191-118">If the function is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="49191-119">Если функция завершается неудачно, возвращается значение НМЕРР, указывающее на ошибку.</span><span class="sxs-lookup"><span data-stu-id="49191-119">If the function is unsuccessful, the return value is a NMERR value that indicates the error.</span></span>

## <a name="requirements"></a><span data-ttu-id="49191-120">Требования</span><span class="sxs-lookup"><span data-stu-id="49191-120">Requirements</span></span>



| <span data-ttu-id="49191-121">Требование</span><span class="sxs-lookup"><span data-stu-id="49191-121">Requirement</span></span> | <span data-ttu-id="49191-122">Значение</span><span class="sxs-lookup"><span data-stu-id="49191-122">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="49191-123">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="49191-123">Minimum supported client</span></span><br/> | <span data-ttu-id="49191-124">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="49191-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="49191-125">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="49191-125">Minimum supported server</span></span><br/> | <span data-ttu-id="49191-126">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="49191-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="49191-127">Заголовок</span><span class="sxs-lookup"><span data-stu-id="49191-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="49191-128"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="49191-128"><dt>Netmon.h</dt></span></span> </dl>     |
| <span data-ttu-id="49191-129">Библиотека</span><span class="sxs-lookup"><span data-stu-id="49191-129">Library</span></span><br/>                  | <dl> <span data-ttu-id="49191-130"><dt>Нпптулс. lib</dt></span><span class="sxs-lookup"><span data-stu-id="49191-130"><dt>Npptools.lib</dt></span></span> </dl> |
| <span data-ttu-id="49191-131">DLL</span><span class="sxs-lookup"><span data-stu-id="49191-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="49191-132"><dt>Npptools.dll</dt></span><span class="sxs-lookup"><span data-stu-id="49191-132"><dt>Npptools.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="49191-133">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="49191-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="49191-134">жетмакаддрессфромблоб</span><span class="sxs-lookup"><span data-stu-id="49191-134">GetMacAddressFromBlob</span></span>](getmacaddressfromblob.md)
</dt> <dt>

[<span data-ttu-id="49191-135">сетбулинблоб</span><span class="sxs-lookup"><span data-stu-id="49191-135">SetBoolInBlob</span></span>](setboolinblob.md)
</dt> <dt>

[<span data-ttu-id="49191-136">сетклассидинблоб</span><span class="sxs-lookup"><span data-stu-id="49191-136">SetClassIDInBlob</span></span>](setclassidinblob.md)
</dt> <dt>

[<span data-ttu-id="49191-137">сетдвординблоб</span><span class="sxs-lookup"><span data-stu-id="49191-137">SetDwordInBlob</span></span>](setdwordinblob.md)
</dt> <dt>

[<span data-ttu-id="49191-138">сетнетворкинфоинблоб</span><span class="sxs-lookup"><span data-stu-id="49191-138">SetNetworkInfoInBlob</span></span>](setnetworkinfoinblob.md)
</dt> <dt>

[<span data-ttu-id="49191-139">сетнппаддрессфилтеринблоб</span><span class="sxs-lookup"><span data-stu-id="49191-139">SetNPPAddressFilterInBlob</span></span>](setnppaddressfilterinblob.md)
</dt> <dt>

[<span data-ttu-id="49191-140">сетнпппаттернфилтеринблоб</span><span class="sxs-lookup"><span data-stu-id="49191-140">SetNPPPatternFilterInBlob</span></span>](setnpppatternfilterinblob.md)
</dt> <dt>

[<span data-ttu-id="49191-141">сетнпптригжеринблоб</span><span class="sxs-lookup"><span data-stu-id="49191-141">SetNPPTriggerInBlob</span></span>](setnpptriggerinblob.md)
</dt> <dt>

[<span data-ttu-id="49191-142">сетстрингинблоб</span><span class="sxs-lookup"><span data-stu-id="49191-142">SetStringInBlob</span></span>](setstringinblob.md)
</dt> </dl>

 

 




