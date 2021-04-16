---
description: Задает фильтр соответствия шаблону большого двоичного объекта.
ms.assetid: 44e7c67a-f430-4d68-bc7f-f6bbd5b9e5a9
title: Функция Сетнпппаттернфилтеринблоб (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SetNPPPatternFilterInBlob
api_type:
- DllExport
api_location:
- Npptools.dll
ms.openlocfilehash: b2e8989264a042368b37926bbb502f48ab2fb04b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104542359"
---
# <a name="setnpppatternfilterinblob-function"></a><span data-ttu-id="e3f71-103">Функция Сетнпппаттернфилтеринблоб</span><span class="sxs-lookup"><span data-stu-id="e3f71-103">SetNPPPatternFilterInBlob function</span></span>

<span data-ttu-id="e3f71-104">Функция **сетнпппаттернфилтеринблоб** задает фильтр соответствия ШАБЛОНУ большого двоичного объекта.</span><span class="sxs-lookup"><span data-stu-id="e3f71-104">The **SetNPPPatternFilterInBlob** function sets the BLOB pattern match filter.</span></span>

## <a name="syntax"></a><span data-ttu-id="e3f71-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="e3f71-105">Syntax</span></span>


```C++
DWORD SetNPPPatternFilterInBlob(
  _In_  HBLOB        hBlob,
  _In_  LPEXPRESSION pExpression,
  _Out_ HBLOB        hErrorBlob
);
```



## <a name="parameters"></a><span data-ttu-id="e3f71-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="e3f71-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e3f71-107">*хблоб* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="e3f71-107">*hBlob* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e3f71-108">Маркер для большого двоичного объекта.</span><span class="sxs-lookup"><span data-stu-id="e3f71-108">The handle to the BLOB.</span></span>

</dd> <dt>

<span data-ttu-id="e3f71-109">*пекспрессион* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="e3f71-109">*pExpression* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e3f71-110">Указатель на структуру [выражения](expression.md) , определяющую устанавливаемое выражение фильтра.</span><span class="sxs-lookup"><span data-stu-id="e3f71-110">A pointer to an [EXPRESSION](expression.md) structure that defines the filter expression being set.</span></span>

</dd> <dt>

<span data-ttu-id="e3f71-111">*херрорблоб* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="e3f71-111">*hErrorBlob* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e3f71-112">Маркер для большого двоичного объекта ошибки, указывающий, где в исходном большом двоичном объекте произошла ошибка (если таковая имеется).</span><span class="sxs-lookup"><span data-stu-id="e3f71-112">The handle to an error BLOB that specifies where in the original BLOB the error (if any) occurred.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e3f71-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="e3f71-113">Return value</span></span>

<span data-ttu-id="e3f71-114">Если функция **сетнпппаттернфилтеринблоб** выполнена успешно, возвращается значение нмерр \_ Success.</span><span class="sxs-lookup"><span data-stu-id="e3f71-114">If the **SetNPPPatternFilterInBlob** function is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="e3f71-115">Если функция завершается неудачно, возвращается значение НМЕРР, указывающее на ошибку.</span><span class="sxs-lookup"><span data-stu-id="e3f71-115">If the function is unsuccessful, the return value is a NMERR value that indicates the error.</span></span>

## <a name="remarks"></a><span data-ttu-id="e3f71-116">Комментарии</span><span class="sxs-lookup"><span data-stu-id="e3f71-116">Remarks</span></span>

<span data-ttu-id="e3f71-117">Шаблон соответствует данным фильтра, хранящимся в категории **конфигурации** большого двоичного объекта.</span><span class="sxs-lookup"><span data-stu-id="e3f71-117">The pattern match filter data stored in the **Config** category of the BLOB.</span></span>

## <a name="requirements"></a><span data-ttu-id="e3f71-118">Требования</span><span class="sxs-lookup"><span data-stu-id="e3f71-118">Requirements</span></span>



| <span data-ttu-id="e3f71-119">Требование</span><span class="sxs-lookup"><span data-stu-id="e3f71-119">Requirement</span></span> | <span data-ttu-id="e3f71-120">Значение</span><span class="sxs-lookup"><span data-stu-id="e3f71-120">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e3f71-121">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="e3f71-121">Minimum supported client</span></span><br/> | <span data-ttu-id="e3f71-122">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="e3f71-122">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="e3f71-123">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="e3f71-123">Minimum supported server</span></span><br/> | <span data-ttu-id="e3f71-124">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="e3f71-124">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="e3f71-125">Заголовок</span><span class="sxs-lookup"><span data-stu-id="e3f71-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="e3f71-126"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="e3f71-126"><dt>Netmon.h</dt></span></span> </dl>     |
| <span data-ttu-id="e3f71-127">Библиотека</span><span class="sxs-lookup"><span data-stu-id="e3f71-127">Library</span></span><br/>                  | <dl> <span data-ttu-id="e3f71-128"><dt>Нпптулс. lib</dt></span><span class="sxs-lookup"><span data-stu-id="e3f71-128"><dt>Npptools.lib</dt></span></span> </dl> |
| <span data-ttu-id="e3f71-129">DLL</span><span class="sxs-lookup"><span data-stu-id="e3f71-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e3f71-130"><dt>Npptools.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e3f71-130"><dt>Npptools.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e3f71-131">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="e3f71-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e3f71-132">жетнппаддрессфилтерфромблоб</span><span class="sxs-lookup"><span data-stu-id="e3f71-132">GetNPPAddressFilterFromBlob</span></span>](getnppaddressfilterfromblob.md)
</dt> <dt>

[<span data-ttu-id="e3f71-133">сетбулинблоб</span><span class="sxs-lookup"><span data-stu-id="e3f71-133">SetBoolInBlob</span></span>](setboolinblob.md)
</dt> <dt>

[<span data-ttu-id="e3f71-134">сетклассидинблоб</span><span class="sxs-lookup"><span data-stu-id="e3f71-134">SetClassIDInBlob</span></span>](setclassidinblob.md)
</dt> <dt>

[<span data-ttu-id="e3f71-135">сетдвординблоб</span><span class="sxs-lookup"><span data-stu-id="e3f71-135">SetDwordInBlob</span></span>](setdwordinblob.md)
</dt> <dt>

[<span data-ttu-id="e3f71-136">сетмакаддрессинблоб</span><span class="sxs-lookup"><span data-stu-id="e3f71-136">SetMacAddressInBlob</span></span>](setmacaddressinblob.md)
</dt> <dt>

[<span data-ttu-id="e3f71-137">сетнетворкинфоинблоб</span><span class="sxs-lookup"><span data-stu-id="e3f71-137">SetNetworkInfoInBlob</span></span>](setnetworkinfoinblob.md)
</dt> <dt>

[<span data-ttu-id="e3f71-138">сетнппаддрессфилтеринблоб</span><span class="sxs-lookup"><span data-stu-id="e3f71-138">SetNPPAddressFilterInBlob</span></span>](setnppaddressfilterinblob.md)
</dt> <dt>

[<span data-ttu-id="e3f71-139">сетнпптригжеринблоб</span><span class="sxs-lookup"><span data-stu-id="e3f71-139">SetNPPTriggerInBlob</span></span>](setnpptriggerinblob.md)
</dt> <dt>

[<span data-ttu-id="e3f71-140">сетстрингинблоб</span><span class="sxs-lookup"><span data-stu-id="e3f71-140">SetStringInBlob</span></span>](setstringinblob.md)
</dt> </dl>

 

 




