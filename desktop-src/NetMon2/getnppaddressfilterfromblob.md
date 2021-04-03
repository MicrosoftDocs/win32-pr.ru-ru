---
description: Функция Жетнппаддрессфилтерфромблоб заполняет заданный фильтр адресов данными, хранящимися в большом двоичном объекте.
ms.assetid: b34e0e52-1b2a-4d61-b60c-f1b19ff8ff38
title: Функция Жетнппаддрессфилтерфромблоб (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetNPPAddressFilterFromBlob
api_type:
- DllExport
api_location:
- Npptools.dll
ms.openlocfilehash: 944821620123d63f654e286a77018232c79981e8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103999397"
---
# <a name="getnppaddressfilterfromblob-function"></a><span data-ttu-id="82dea-103">Функция Жетнппаддрессфилтерфромблоб</span><span class="sxs-lookup"><span data-stu-id="82dea-103">GetNPPAddressFilterFromBlob function</span></span>

<span data-ttu-id="82dea-104">Функция **жетнппаддрессфилтерфромблоб** заполняет заданный фильтр адресов данными, хранящимися в большом двоичном объекте.</span><span class="sxs-lookup"><span data-stu-id="82dea-104">The **GetNPPAddressFilterFromBlob** function fills in the given address filter with information stored in the BLOB.</span></span>

## <a name="syntax"></a><span data-ttu-id="82dea-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="82dea-105">Syntax</span></span>


```C++
DWORD GetNPPAddressFilterFromBlob(
  _In_    HBLOB          hBlob,
  _Inout_ LPADDRESSTABLE pAddressTable,
  _Out_   HBLOB          hErrorBlob
);
```



## <a name="parameters"></a><span data-ttu-id="82dea-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="82dea-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="82dea-107">*хблоб* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="82dea-107">*hBlob* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="82dea-108">Обработчик для большого двоичного объекта.</span><span class="sxs-lookup"><span data-stu-id="82dea-108">Handle to a BLOB.</span></span>

</dd> <dt>

<span data-ttu-id="82dea-109">*паддресстабле* \[ в, out\]</span><span class="sxs-lookup"><span data-stu-id="82dea-109">*pAddressTable* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="82dea-110">Указатель на выделенную пользователем таблицу адресов.</span><span class="sxs-lookup"><span data-stu-id="82dea-110">Pointer to the user-allocated address table.</span></span>

</dd> <dt>

<span data-ttu-id="82dea-111">*херрорблоб* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="82dea-111">*hErrorBlob* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="82dea-112">Обработайте с большим ДВОИЧным объектом ошибки, который указывает, где в исходном большом двоичном объекте произошла ошибка (если таковая имеется).</span><span class="sxs-lookup"><span data-stu-id="82dea-112">Handle to an error BLOB that specifies where in the original BLOB the error (if any) occurred.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="82dea-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="82dea-113">Return value</span></span>

<span data-ttu-id="82dea-114">Если функция выполнена успешно, возвращается значение НМЕРР \_ Success.</span><span class="sxs-lookup"><span data-stu-id="82dea-114">If the function is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="82dea-115">Если функция завершается неудачно, возвращается значение НМЕРР, описывающее ошибку.</span><span class="sxs-lookup"><span data-stu-id="82dea-115">If the function is unsuccessful, the return value is a NMERR value that describes the error.</span></span>

## <a name="remarks"></a><span data-ttu-id="82dea-116">Комментарии</span><span class="sxs-lookup"><span data-stu-id="82dea-116">Remarks</span></span>

<span data-ttu-id="82dea-117">Сведения об адресе хранятся в разделе **config** категории **владельца** BLOB-объекта НПП.</span><span class="sxs-lookup"><span data-stu-id="82dea-117">The address information is stored in the **Config** section of the BLOB NPP **Owner** category.</span></span>

## <a name="requirements"></a><span data-ttu-id="82dea-118">Требования</span><span class="sxs-lookup"><span data-stu-id="82dea-118">Requirements</span></span>



| <span data-ttu-id="82dea-119">Требование</span><span class="sxs-lookup"><span data-stu-id="82dea-119">Requirement</span></span> | <span data-ttu-id="82dea-120">Значение</span><span class="sxs-lookup"><span data-stu-id="82dea-120">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="82dea-121">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="82dea-121">Minimum supported client</span></span><br/> | <span data-ttu-id="82dea-122">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="82dea-122">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="82dea-123">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="82dea-123">Minimum supported server</span></span><br/> | <span data-ttu-id="82dea-124">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="82dea-124">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="82dea-125">Заголовок</span><span class="sxs-lookup"><span data-stu-id="82dea-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="82dea-126"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="82dea-126"><dt>Netmon.h</dt></span></span> </dl>     |
| <span data-ttu-id="82dea-127">Библиотека</span><span class="sxs-lookup"><span data-stu-id="82dea-127">Library</span></span><br/>                  | <dl> <span data-ttu-id="82dea-128"><dt>Нпптулс. lib</dt></span><span class="sxs-lookup"><span data-stu-id="82dea-128"><dt>Npptools.lib</dt></span></span> </dl> |
| <span data-ttu-id="82dea-129">DLL</span><span class="sxs-lookup"><span data-stu-id="82dea-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="82dea-130"><dt>Npptools.dll</dt></span><span class="sxs-lookup"><span data-stu-id="82dea-130"><dt>Npptools.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="82dea-131">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="82dea-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="82dea-132">сетнппаддрессфилтеринблоб</span><span class="sxs-lookup"><span data-stu-id="82dea-132">SetNPPAddressFilterInBlob</span></span>](setnppaddressfilterinblob.md)
</dt> <dt>

[<span data-ttu-id="82dea-133">жетбулфромблоб</span><span class="sxs-lookup"><span data-stu-id="82dea-133">GetBoolFromBlob</span></span>](getboolfromblob.md)
</dt> <dt>

[<span data-ttu-id="82dea-134">жетклассидфромблоб</span><span class="sxs-lookup"><span data-stu-id="82dea-134">GetClassIDFromBlob</span></span>](getclassidfromblob.md)
</dt> <dt>

[<span data-ttu-id="82dea-135">жетдвордфромблоб</span><span class="sxs-lookup"><span data-stu-id="82dea-135">GetDwordFromBlob</span></span>](getdwordfromblob.md)
</dt> <dt>

[<span data-ttu-id="82dea-136">жетмакаддрессфромблоб</span><span class="sxs-lookup"><span data-stu-id="82dea-136">GetMacAddressFromBlob</span></span>](getmacaddressfromblob.md)
</dt> <dt>

[<span data-ttu-id="82dea-137">жетнетворкинфофромблоб</span><span class="sxs-lookup"><span data-stu-id="82dea-137">GetNetworkInfoFromBlob</span></span>](getnetworkinfofromblob.md)
</dt> <dt>

[<span data-ttu-id="82dea-138">жетнпппаттернфилтерфромблоб</span><span class="sxs-lookup"><span data-stu-id="82dea-138">GetNPPPatternFilterFromBlob</span></span>](getnpppatternfilterfromblob.md)
</dt> <dt>

[<span data-ttu-id="82dea-139">жетнпптригжерфромблоб</span><span class="sxs-lookup"><span data-stu-id="82dea-139">GetNPPTriggerFromBlob</span></span>](getnpptriggerfromblob.md)
</dt> <dt>

[<span data-ttu-id="82dea-140">жетстрингфромблоб</span><span class="sxs-lookup"><span data-stu-id="82dea-140">GetStringFromBlob</span></span>](getstringfromblob.md)
</dt> <dt>

[<span data-ttu-id="82dea-141">жетстрингсфромблоб</span><span class="sxs-lookup"><span data-stu-id="82dea-141">GetStringsFromBlob</span></span>](getstringsfromblob.md)
</dt> </dl>

 

 




