---
description: Функция Жетнпппаттернфилтерфромблоб извлекает фильтр соответствия шаблонов из определенного большого двоичного объекта.
ms.assetid: b17cde55-8abb-4699-960f-676cbbb24326
title: Функция Жетнпппаттернфилтерфромблоб (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetNPPPatternFilterFromBlob
api_type:
- DllExport
api_location:
- Npptools.dll
ms.openlocfilehash: 5758c53fe21231d300058a9168e556e9f9ceaa43
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103808711"
---
# <a name="getnpppatternfilterfromblob-function"></a><span data-ttu-id="c77b3-103">Функция Жетнпппаттернфилтерфромблоб</span><span class="sxs-lookup"><span data-stu-id="c77b3-103">GetNPPPatternFilterFromBlob function</span></span>

<span data-ttu-id="c77b3-104">Функция **жетнпппаттернфилтерфромблоб** извлекает фильтр соответствия шаблонов из определенного большого двоичного объекта.</span><span class="sxs-lookup"><span data-stu-id="c77b3-104">The **GetNPPPatternFilterFromBlob** function retrieves the pattern match filter from a specific BLOB.</span></span>

## <a name="syntax"></a><span data-ttu-id="c77b3-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="c77b3-105">Syntax</span></span>


```C++
DWORD GetNPPPatternFilterFromBlob(
  _In_  HBLOB        hBlob,
  _In_  LPEXPRESSION pExpression,
  _Out_ HBLOB        hErrorBlob
);
```



## <a name="parameters"></a><span data-ttu-id="c77b3-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="c77b3-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c77b3-107">*хблоб* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="c77b3-107">*hBlob* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c77b3-108">Обработчик для большого двоичного объекта.</span><span class="sxs-lookup"><span data-stu-id="c77b3-108">Handle to the BLOB.</span></span>

</dd> <dt>

<span data-ttu-id="c77b3-109">*пекспрессион* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="c77b3-109">*pExpression* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c77b3-110">Указатель на критерий фильтра.</span><span class="sxs-lookup"><span data-stu-id="c77b3-110">Pointer to the filter expression.</span></span>

</dd> <dt>

<span data-ttu-id="c77b3-111">*херрорблоб* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="c77b3-111">*hErrorBlob* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c77b3-112">Обработайте с большим ДВОИЧным объектом ошибки, который указывает, где в исходном большом двоичном объекте произошла ошибка (если таковая имеется).</span><span class="sxs-lookup"><span data-stu-id="c77b3-112">Handle to an error BLOB that specifies where in the original BLOB the error (if any) occurred.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c77b3-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="c77b3-113">Return value</span></span>

<span data-ttu-id="c77b3-114">Если функция выполнена успешно, возвращается значение НМЕРР \_ Success.</span><span class="sxs-lookup"><span data-stu-id="c77b3-114">If the function is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="c77b3-115">Если функция завершается неудачно, возвращается значение НМЕРР, указывающее на ошибку.</span><span class="sxs-lookup"><span data-stu-id="c77b3-115">If the function is unsuccessful, the return value is a NMERR that indicates the error.</span></span>

## <a name="remarks"></a><span data-ttu-id="c77b3-116">Комментарии</span><span class="sxs-lookup"><span data-stu-id="c77b3-116">Remarks</span></span>

<span data-ttu-id="c77b3-117">Сведения о фильтре соответствия шаблону хранятся в категории **конфигурации** большого двоичного объекта.</span><span class="sxs-lookup"><span data-stu-id="c77b3-117">The pattern match filter information is stored in the **Config** category of the BLOB.</span></span>

## <a name="requirements"></a><span data-ttu-id="c77b3-118">Требования</span><span class="sxs-lookup"><span data-stu-id="c77b3-118">Requirements</span></span>



| <span data-ttu-id="c77b3-119">Требование</span><span class="sxs-lookup"><span data-stu-id="c77b3-119">Requirement</span></span> | <span data-ttu-id="c77b3-120">Значение</span><span class="sxs-lookup"><span data-stu-id="c77b3-120">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c77b3-121">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="c77b3-121">Minimum supported client</span></span><br/> | <span data-ttu-id="c77b3-122">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="c77b3-122">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="c77b3-123">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="c77b3-123">Minimum supported server</span></span><br/> | <span data-ttu-id="c77b3-124">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="c77b3-124">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="c77b3-125">Заголовок</span><span class="sxs-lookup"><span data-stu-id="c77b3-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="c77b3-126"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="c77b3-126"><dt>Netmon.h</dt></span></span> </dl>     |
| <span data-ttu-id="c77b3-127">Библиотека</span><span class="sxs-lookup"><span data-stu-id="c77b3-127">Library</span></span><br/>                  | <dl> <span data-ttu-id="c77b3-128"><dt>Нпптулс. lib</dt></span><span class="sxs-lookup"><span data-stu-id="c77b3-128"><dt>Npptools.lib</dt></span></span> </dl> |
| <span data-ttu-id="c77b3-129">DLL</span><span class="sxs-lookup"><span data-stu-id="c77b3-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c77b3-130"><dt>Npptools.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c77b3-130"><dt>Npptools.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c77b3-131">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="c77b3-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c77b3-132">сетнпппаттернфилтеринблоб</span><span class="sxs-lookup"><span data-stu-id="c77b3-132">SetNPPPatternFilterInBlob</span></span>](setnpppatternfilterinblob.md)
</dt> <dt>

[<span data-ttu-id="c77b3-133">жетбулфромблоб</span><span class="sxs-lookup"><span data-stu-id="c77b3-133">GetBoolFromBlob</span></span>](getboolfromblob.md)
</dt> <dt>

[<span data-ttu-id="c77b3-134">жетклассидфромблоб</span><span class="sxs-lookup"><span data-stu-id="c77b3-134">GetClassIDFromBlob</span></span>](getclassidfromblob.md)
</dt> <dt>

[<span data-ttu-id="c77b3-135">жетдвордфромблоб</span><span class="sxs-lookup"><span data-stu-id="c77b3-135">GetDwordFromBlob</span></span>](getdwordfromblob.md)
</dt> <dt>

[<span data-ttu-id="c77b3-136">жетмакаддрессфромблоб</span><span class="sxs-lookup"><span data-stu-id="c77b3-136">GetMacAddressFromBlob</span></span>](getmacaddressfromblob.md)
</dt> <dt>

[<span data-ttu-id="c77b3-137">жетнетворкинфофромблоб</span><span class="sxs-lookup"><span data-stu-id="c77b3-137">GetNetworkInfoFromBlob</span></span>](getnetworkinfofromblob.md)
</dt> <dt>

[<span data-ttu-id="c77b3-138">жетнппаддрессфилтерфромблоб</span><span class="sxs-lookup"><span data-stu-id="c77b3-138">GetNPPAddressFilterFromBlob</span></span>](getnppaddressfilterfromblob.md)
</dt> <dt>

[<span data-ttu-id="c77b3-139">жетнпптригжерфромблоб</span><span class="sxs-lookup"><span data-stu-id="c77b3-139">GetNPPTriggerFromBlob</span></span>](getnpptriggerfromblob.md)
</dt> <dt>

[<span data-ttu-id="c77b3-140">жетстрингфромблоб</span><span class="sxs-lookup"><span data-stu-id="c77b3-140">GetStringFromBlob</span></span>](getstringfromblob.md)
</dt> <dt>

[<span data-ttu-id="c77b3-141">жетстрингсфромблоб</span><span class="sxs-lookup"><span data-stu-id="c77b3-141">GetStringsFromBlob</span></span>](getstringsfromblob.md)
</dt> </dl>

 

 




