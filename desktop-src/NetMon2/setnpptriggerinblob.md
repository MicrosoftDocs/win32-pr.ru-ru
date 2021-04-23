---
description: Задает триггер большого двоичного объекта.
ms.assetid: 88bfd5cd-f563-4d0c-81a3-54a846805b87
title: Функция Сетнпптригжеринблоб (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SetNPPTriggerInBlob
api_type:
- DllExport
api_location:
- Npptools.dll
ms.openlocfilehash: 05b8bb3f7f95dc3246ef10f3945b9ab0868550cb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104263222"
---
# <a name="setnpptriggerinblob-function"></a><span data-ttu-id="dbc96-103">Функция Сетнпптригжеринблоб</span><span class="sxs-lookup"><span data-stu-id="dbc96-103">SetNPPTriggerInBlob function</span></span>

<span data-ttu-id="dbc96-104">Функция **сетнпптригжеринблоб** задает триггер большого двоичного объекта.</span><span class="sxs-lookup"><span data-stu-id="dbc96-104">The **SetNPPTriggerInBlob** function sets the BLOB trigger.</span></span>

## <a name="syntax"></a><span data-ttu-id="dbc96-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="dbc96-105">Syntax</span></span>


```C++
DWORD SetNPPTriggerInBlob(
  _In_  HBLOB     hBlob,
  _In_  LPTRIGGER pTrigger,
  _Out_ HBLOB     hErrorBlob
);
```



## <a name="parameters"></a><span data-ttu-id="dbc96-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="dbc96-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dbc96-107">*хблоб* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="dbc96-107">*hBlob* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dbc96-108">Маркер для большого двоичного объекта.</span><span class="sxs-lookup"><span data-stu-id="dbc96-108">The handle to the BLOB.</span></span>

</dd> <dt>

<span data-ttu-id="dbc96-109">*птригжер* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="dbc96-109">*pTrigger* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dbc96-110">Указатель на значение триггера.</span><span class="sxs-lookup"><span data-stu-id="dbc96-110">A pointer to the trigger value.</span></span>

</dd> <dt>

<span data-ttu-id="dbc96-111">*херрорблоб* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="dbc96-111">*hErrorBlob* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="dbc96-112">Маркер для большого двоичного объекта ошибки, указывающий, где в исходном большом двоичном объекте произошла ошибка (если таковая имеется).</span><span class="sxs-lookup"><span data-stu-id="dbc96-112">The handle to an error BLOB that specifies where in the original BLOB the error (if any) occurred.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dbc96-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="dbc96-113">Return value</span></span>

<span data-ttu-id="dbc96-114">Если функция выполнена успешно, возвращается значение НМЕРР \_ Success.</span><span class="sxs-lookup"><span data-stu-id="dbc96-114">If the function is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="dbc96-115">Если функция завершается неудачно, возвращается значение НМЕРР, указывающее на ошибку.</span><span class="sxs-lookup"><span data-stu-id="dbc96-115">If the function is unsuccessful, the return value is a NMERR value that indicates the error.</span></span>

## <a name="remarks"></a><span data-ttu-id="dbc96-116">Комментарии</span><span class="sxs-lookup"><span data-stu-id="dbc96-116">Remarks</span></span>

<span data-ttu-id="dbc96-117">Данные триггера хранятся в категории **триггеров** большого двоичного объекта.</span><span class="sxs-lookup"><span data-stu-id="dbc96-117">This trigger data is stored in the **Trigger** category of the BLOB.</span></span>

## <a name="requirements"></a><span data-ttu-id="dbc96-118">Требования</span><span class="sxs-lookup"><span data-stu-id="dbc96-118">Requirements</span></span>



| <span data-ttu-id="dbc96-119">Требование</span><span class="sxs-lookup"><span data-stu-id="dbc96-119">Requirement</span></span> | <span data-ttu-id="dbc96-120">Значение</span><span class="sxs-lookup"><span data-stu-id="dbc96-120">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="dbc96-121">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="dbc96-121">Minimum supported client</span></span><br/> | <span data-ttu-id="dbc96-122">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="dbc96-122">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="dbc96-123">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="dbc96-123">Minimum supported server</span></span><br/> | <span data-ttu-id="dbc96-124">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="dbc96-124">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="dbc96-125">Заголовок</span><span class="sxs-lookup"><span data-stu-id="dbc96-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="dbc96-126"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="dbc96-126"><dt>Netmon.h</dt></span></span> </dl>     |
| <span data-ttu-id="dbc96-127">Библиотека</span><span class="sxs-lookup"><span data-stu-id="dbc96-127">Library</span></span><br/>                  | <dl> <span data-ttu-id="dbc96-128"><dt>Нпптулс. lib</dt></span><span class="sxs-lookup"><span data-stu-id="dbc96-128"><dt>Npptools.lib</dt></span></span> </dl> |
| <span data-ttu-id="dbc96-129">DLL</span><span class="sxs-lookup"><span data-stu-id="dbc96-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="dbc96-130"><dt>Npptools.dll</dt></span><span class="sxs-lookup"><span data-stu-id="dbc96-130"><dt>Npptools.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dbc96-131">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="dbc96-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dbc96-132">жетнпптригжерфромблоб</span><span class="sxs-lookup"><span data-stu-id="dbc96-132">GetNPPTriggerFromBlob</span></span>](getnpptriggerfromblob.md)
</dt> <dt>

[<span data-ttu-id="dbc96-133">сетбулинблоб</span><span class="sxs-lookup"><span data-stu-id="dbc96-133">SetBoolInBlob</span></span>](setboolinblob.md)
</dt> <dt>

[<span data-ttu-id="dbc96-134">сетклассидинблоб</span><span class="sxs-lookup"><span data-stu-id="dbc96-134">SetClassIDInBlob</span></span>](setclassidinblob.md)
</dt> <dt>

[<span data-ttu-id="dbc96-135">сетдвординблоб</span><span class="sxs-lookup"><span data-stu-id="dbc96-135">SetDwordInBlob</span></span>](setdwordinblob.md)
</dt> <dt>

[<span data-ttu-id="dbc96-136">сетмакаддрессинблоб</span><span class="sxs-lookup"><span data-stu-id="dbc96-136">SetMacAddressInBlob</span></span>](setmacaddressinblob.md)
</dt> <dt>

[<span data-ttu-id="dbc96-137">сетнетворкинфоинблоб</span><span class="sxs-lookup"><span data-stu-id="dbc96-137">SetNetworkInfoInBlob</span></span>](setnetworkinfoinblob.md)
</dt> <dt>

[<span data-ttu-id="dbc96-138">сетнппаддрессфилтеринблоб</span><span class="sxs-lookup"><span data-stu-id="dbc96-138">SetNPPAddressFilterInBlob</span></span>](setnppaddressfilterinblob.md)
</dt> <dt>

[<span data-ttu-id="dbc96-139">сетнпппаттернфилтеринблоб</span><span class="sxs-lookup"><span data-stu-id="dbc96-139">SetNPPPatternFilterInBlob</span></span>](setnpppatternfilterinblob.md)
</dt> <dt>

[<span data-ttu-id="dbc96-140">сетстрингинблоб</span><span class="sxs-lookup"><span data-stu-id="dbc96-140">SetStringInBlob</span></span>](setstringinblob.md)
</dt> </dl>

 

 




