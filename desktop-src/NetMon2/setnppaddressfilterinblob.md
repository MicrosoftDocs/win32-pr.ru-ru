---
description: Функция Сетнппаддрессфилтеринблоб задает указанный фильтр адресов в большом двоичном объекте.
ms.assetid: bdd1482d-8be0-4999-9a7a-16b0400412fb
title: Функция Сетнппаддрессфилтеринблоб (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SetNPPAddressFilterInBlob
api_type:
- DllExport
api_location:
- Npptools.dll
ms.openlocfilehash: 39e8a85599fa63b1320d707f648731a195dbb48e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105674333"
---
# <a name="setnppaddressfilterinblob-function"></a><span data-ttu-id="9192f-103">Функция Сетнппаддрессфилтеринблоб</span><span class="sxs-lookup"><span data-stu-id="9192f-103">SetNPPAddressFilterInBlob function</span></span>

<span data-ttu-id="9192f-104">Функция **сетнппаддрессфилтеринблоб** задает указанный фильтр адресов в большом двоичном объекте.</span><span class="sxs-lookup"><span data-stu-id="9192f-104">The **SetNPPAddressFilterInBlob** function sets the given address filter in the BLOB.</span></span>

## <a name="syntax"></a><span data-ttu-id="9192f-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="9192f-105">Syntax</span></span>


```C++
DWORD SetNPPAddressFilterInBlob(
  _In_ HBLOB          hBlob,
  _In_ LPADDRESSTABLE pAddressTable
);
```



## <a name="parameters"></a><span data-ttu-id="9192f-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="9192f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9192f-107">*хблоб* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="9192f-107">*hBlob* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9192f-108">Обработчик для большого двоичного объекта.</span><span class="sxs-lookup"><span data-stu-id="9192f-108">Handle to a BLOB.</span></span>

</dd> <dt>

<span data-ttu-id="9192f-109">*паддресстабле* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="9192f-109">*pAddressTable* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9192f-110">Указатель на структуру [**аддресстабле**](addresstable.md) , которая определяет выделенную пользователем таблицу адресов.</span><span class="sxs-lookup"><span data-stu-id="9192f-110">Pointer to an [**ADDRESSTABLE**](addresstable.md) structure that defines the user-allocated address table.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9192f-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="9192f-111">Return value</span></span>

<span data-ttu-id="9192f-112">Если функция выполнена успешно, возвращается значение НМЕРР \_ Success.</span><span class="sxs-lookup"><span data-stu-id="9192f-112">If the function is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="9192f-113">Если функция завершается неудачно, возвращается значение НМЕРР, указывающее на ошибку.</span><span class="sxs-lookup"><span data-stu-id="9192f-113">If the function is unsuccessful, the return value is a NMERR value that indicates the error.</span></span>

## <a name="requirements"></a><span data-ttu-id="9192f-114">Требования</span><span class="sxs-lookup"><span data-stu-id="9192f-114">Requirements</span></span>



| <span data-ttu-id="9192f-115">Требование</span><span class="sxs-lookup"><span data-stu-id="9192f-115">Requirement</span></span> | <span data-ttu-id="9192f-116">Значение</span><span class="sxs-lookup"><span data-stu-id="9192f-116">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="9192f-117">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="9192f-117">Minimum supported client</span></span><br/> | <span data-ttu-id="9192f-118">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="9192f-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="9192f-119">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="9192f-119">Minimum supported server</span></span><br/> | <span data-ttu-id="9192f-120">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="9192f-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="9192f-121">Заголовок</span><span class="sxs-lookup"><span data-stu-id="9192f-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="9192f-122"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="9192f-122"><dt>Netmon.h</dt></span></span> </dl>     |
| <span data-ttu-id="9192f-123">Библиотека</span><span class="sxs-lookup"><span data-stu-id="9192f-123">Library</span></span><br/>                  | <dl> <span data-ttu-id="9192f-124"><dt>Нпптулс. lib</dt></span><span class="sxs-lookup"><span data-stu-id="9192f-124"><dt>Npptools.lib</dt></span></span> </dl> |
| <span data-ttu-id="9192f-125">DLL</span><span class="sxs-lookup"><span data-stu-id="9192f-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9192f-126"><dt>Npptools.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9192f-126"><dt>Npptools.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9192f-127">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="9192f-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9192f-128">жетнппаддрессфилтерфромблоб</span><span class="sxs-lookup"><span data-stu-id="9192f-128">GetNPPAddressFilterFromBlob</span></span>](getnppaddressfilterfromblob.md)
</dt> <dt>

[<span data-ttu-id="9192f-129">сетбулинблоб</span><span class="sxs-lookup"><span data-stu-id="9192f-129">SetBoolInBlob</span></span>](setboolinblob.md)
</dt> <dt>

[<span data-ttu-id="9192f-130">сетклассидинблоб</span><span class="sxs-lookup"><span data-stu-id="9192f-130">SetClassIDInBlob</span></span>](setclassidinblob.md)
</dt> <dt>

[<span data-ttu-id="9192f-131">сетдвординблоб</span><span class="sxs-lookup"><span data-stu-id="9192f-131">SetDwordInBlob</span></span>](setdwordinblob.md)
</dt> <dt>

[<span data-ttu-id="9192f-132">сетмакаддрессинблоб</span><span class="sxs-lookup"><span data-stu-id="9192f-132">SetMacAddressInBlob</span></span>](setmacaddressinblob.md)
</dt> <dt>

[<span data-ttu-id="9192f-133">сетнетворкинфоинблоб</span><span class="sxs-lookup"><span data-stu-id="9192f-133">SetNetworkInfoInBlob</span></span>](setnetworkinfoinblob.md)
</dt> <dt>

[<span data-ttu-id="9192f-134">сетнпппаттернфилтеринблоб</span><span class="sxs-lookup"><span data-stu-id="9192f-134">SetNPPPatternFilterInBlob</span></span>](setnpppatternfilterinblob.md)
</dt> <dt>

[<span data-ttu-id="9192f-135">сетнпптригжеринблоб</span><span class="sxs-lookup"><span data-stu-id="9192f-135">SetNPPTriggerInBlob</span></span>](setnpptriggerinblob.md)
</dt> <dt>

[<span data-ttu-id="9192f-136">сетстрингинблоб</span><span class="sxs-lookup"><span data-stu-id="9192f-136">SetStringInBlob</span></span>](setstringinblob.md)
</dt> </dl>

 

 




