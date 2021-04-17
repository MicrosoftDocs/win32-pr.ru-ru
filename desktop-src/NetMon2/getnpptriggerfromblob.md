---
description: Функция Жетнпптригжерфромблоб извлекает триггер из заданного большого двоичного объекта.
ms.assetid: 48a27cf3-57b0-4241-a925-4209e0d384e2
title: Функция Жетнпптригжерфромблоб (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetNPPTriggerFromBlob
api_type:
- DllExport
api_location:
- Npptools.dll
ms.openlocfilehash: 11622078354012de4796ddd43a698ac812951742
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105673184"
---
# <a name="getnpptriggerfromblob-function"></a><span data-ttu-id="899d2-103">Функция Жетнпптригжерфромблоб</span><span class="sxs-lookup"><span data-stu-id="899d2-103">GetNPPTriggerFromBlob function</span></span>

<span data-ttu-id="899d2-104">Функция **жетнпптригжерфромблоб** извлекает триггер из заданного большого двоичного объекта.</span><span class="sxs-lookup"><span data-stu-id="899d2-104">The **GetNPPTriggerFromBlob** function retrieves the trigger from the given BLOB.</span></span>

## <a name="syntax"></a><span data-ttu-id="899d2-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="899d2-105">Syntax</span></span>


```C++
DWORD GetNPPTriggerFromBlob(
  _In_  HBLOB     hBlob,
  _Out_ LPTRIGGER pTrigger,
  _Out_ HBLOB     hErrorBlob
);
```



## <a name="parameters"></a><span data-ttu-id="899d2-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="899d2-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="899d2-107">*хблоб* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="899d2-107">*hBlob* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="899d2-108">Обработчик для большого двоичного объекта.</span><span class="sxs-lookup"><span data-stu-id="899d2-108">Handle to the BLOB.</span></span>

</dd> <dt>

<span data-ttu-id="899d2-109">*птригжер* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="899d2-109">*pTrigger* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="899d2-110">Указатель на значение триггера.</span><span class="sxs-lookup"><span data-stu-id="899d2-110">Pointer to the trigger value.</span></span>

</dd> <dt>

<span data-ttu-id="899d2-111">*херрорблоб* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="899d2-111">*hErrorBlob* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="899d2-112">Обработайте с большим ДВОИЧным объектом ошибки, который указывает, где в исходном большом двоичном объекте произошла ошибка (если таковая имеется).</span><span class="sxs-lookup"><span data-stu-id="899d2-112">Handle to an error BLOB that specifies where in the original BLOB the error (if any) occurred.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="899d2-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="899d2-113">Return value</span></span>

<span data-ttu-id="899d2-114">Если функция выполнена успешно, возвращается значение НМЕРР \_ Success.</span><span class="sxs-lookup"><span data-stu-id="899d2-114">If the function is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="899d2-115">Если функция завершается неудачно, возвращается значение НМЕРР, указывающее на ошибку.</span><span class="sxs-lookup"><span data-stu-id="899d2-115">If the function is unsuccessful, the return value is a NMERR value that indicates the error.</span></span>

## <a name="remarks"></a><span data-ttu-id="899d2-116">Комментарии</span><span class="sxs-lookup"><span data-stu-id="899d2-116">Remarks</span></span>

<span data-ttu-id="899d2-117">Сведения о триггере хранятся в категории **триггеров** большого двоичного объекта.</span><span class="sxs-lookup"><span data-stu-id="899d2-117">The trigger information is stored in the **Trigger** category of the BLOB.</span></span>

## <a name="requirements"></a><span data-ttu-id="899d2-118">Требования</span><span class="sxs-lookup"><span data-stu-id="899d2-118">Requirements</span></span>



| <span data-ttu-id="899d2-119">Требование</span><span class="sxs-lookup"><span data-stu-id="899d2-119">Requirement</span></span> | <span data-ttu-id="899d2-120">Значение</span><span class="sxs-lookup"><span data-stu-id="899d2-120">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="899d2-121">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="899d2-121">Minimum supported client</span></span><br/> | <span data-ttu-id="899d2-122">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="899d2-122">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="899d2-123">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="899d2-123">Minimum supported server</span></span><br/> | <span data-ttu-id="899d2-124">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="899d2-124">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="899d2-125">Заголовок</span><span class="sxs-lookup"><span data-stu-id="899d2-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="899d2-126"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="899d2-126"><dt>Netmon.h</dt></span></span> </dl>     |
| <span data-ttu-id="899d2-127">Библиотека</span><span class="sxs-lookup"><span data-stu-id="899d2-127">Library</span></span><br/>                  | <dl> <span data-ttu-id="899d2-128"><dt>Нпптулс. lib</dt></span><span class="sxs-lookup"><span data-stu-id="899d2-128"><dt>Npptools.lib</dt></span></span> </dl> |
| <span data-ttu-id="899d2-129">DLL</span><span class="sxs-lookup"><span data-stu-id="899d2-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="899d2-130"><dt>Npptools.dll</dt></span><span class="sxs-lookup"><span data-stu-id="899d2-130"><dt>Npptools.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="899d2-131">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="899d2-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="899d2-132">жетбулфромблоб</span><span class="sxs-lookup"><span data-stu-id="899d2-132">GetBoolFromBlob</span></span>](getboolfromblob.md)
</dt> <dt>

[<span data-ttu-id="899d2-133">жетклассидфромблоб</span><span class="sxs-lookup"><span data-stu-id="899d2-133">GetClassIDFromBlob</span></span>](getclassidfromblob.md)
</dt> <dt>

[<span data-ttu-id="899d2-134">жетдвордфромблоб</span><span class="sxs-lookup"><span data-stu-id="899d2-134">GetDwordFromBlob</span></span>](getdwordfromblob.md)
</dt> <dt>

[<span data-ttu-id="899d2-135">жетмакаддрессфромблоб</span><span class="sxs-lookup"><span data-stu-id="899d2-135">GetMacAddressFromBlob</span></span>](getmacaddressfromblob.md)
</dt> <dt>

[<span data-ttu-id="899d2-136">жетнетворкинфофромблоб</span><span class="sxs-lookup"><span data-stu-id="899d2-136">GetNetworkInfoFromBlob</span></span>](getnetworkinfofromblob.md)
</dt> <dt>

[<span data-ttu-id="899d2-137">жетнппаддрессфилтерфромблоб</span><span class="sxs-lookup"><span data-stu-id="899d2-137">GetNPPAddressFilterFromBlob</span></span>](getnppaddressfilterfromblob.md)
</dt> <dt>

[<span data-ttu-id="899d2-138">жетнпппаттернфилтерфромблоб</span><span class="sxs-lookup"><span data-stu-id="899d2-138">GetNPPPatternFilterFromBlob</span></span>](getnpppatternfilterfromblob.md)
</dt> <dt>

[<span data-ttu-id="899d2-139">жетстрингфромблоб</span><span class="sxs-lookup"><span data-stu-id="899d2-139">GetStringFromBlob</span></span>](getstringfromblob.md)
</dt> <dt>

[<span data-ttu-id="899d2-140">жетстрингсфромблоб</span><span class="sxs-lookup"><span data-stu-id="899d2-140">GetStringsFromBlob</span></span>](getstringsfromblob.md)
</dt> </dl>

 

 




