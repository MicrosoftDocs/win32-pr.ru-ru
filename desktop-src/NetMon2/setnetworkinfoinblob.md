---
description: Функция Сетнетворкинфоинблоб заполняет структуру НЕТВОРКИНФО в большом двоичном объекте.
ms.assetid: 1a511c26-2fa7-4fe4-a5a9-23188c59bc34
title: Функция Сетнетворкинфоинблоб (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SetNetworkInfoInBlob
api_type:
- DllExport
api_location:
- Npptools.dll
ms.openlocfilehash: a0019bfaf802b5d4dc80d73e75affa3c50d95de1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105674036"
---
# <a name="setnetworkinfoinblob-function"></a><span data-ttu-id="af60b-103">Функция Сетнетворкинфоинблоб</span><span class="sxs-lookup"><span data-stu-id="af60b-103">SetNetworkInfoInBlob function</span></span>

<span data-ttu-id="af60b-104">Функция **сетнетворкинфоинблоб** заполняет структуру **нетворкинфо** в большом двоичном объекте.</span><span class="sxs-lookup"><span data-stu-id="af60b-104">The **SetNetworkInfoInBlob** function fills in the **NETWORKINFO** structure in the BLOB.</span></span>

## <a name="syntax"></a><span data-ttu-id="af60b-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="af60b-105">Syntax</span></span>


```C++
DWORD SetNetworkInfoInBlob(
  _In_ HBLOB         hBlob,
  _In_ LPNETWORKINFO lpNetworkInfo
);
```



## <a name="parameters"></a><span data-ttu-id="af60b-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="af60b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="af60b-107">*хблоб* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="af60b-107">*hBlob* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="af60b-108">Обработчик для большого двоичного объекта.</span><span class="sxs-lookup"><span data-stu-id="af60b-108">Handle to a BLOB.</span></span>

</dd> <dt>

<span data-ttu-id="af60b-109">*лпнетворкинфо* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="af60b-109">*lpNetworkInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="af60b-110">Указатель на выделенную пользователем структуру [нетворкинфо](networkinfo.md) , которую заполняет функция.</span><span class="sxs-lookup"><span data-stu-id="af60b-110">Pointer to the user-allocated [NETWORKINFO](networkinfo.md) structure that the function fills in.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="af60b-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="af60b-111">Return value</span></span>

<span data-ttu-id="af60b-112">Если функция выполнена успешно, возвращается значение НМЕРР \_ Success.</span><span class="sxs-lookup"><span data-stu-id="af60b-112">If the function is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="af60b-113">Если функция завершается неудачно, возвращается значение НМЕРР, указывающее на ошибку.</span><span class="sxs-lookup"><span data-stu-id="af60b-113">If the function is unsuccessful, the return value is a NMERR value that indicates the error.</span></span>

## <a name="requirements"></a><span data-ttu-id="af60b-114">Требования</span><span class="sxs-lookup"><span data-stu-id="af60b-114">Requirements</span></span>



| <span data-ttu-id="af60b-115">Требование</span><span class="sxs-lookup"><span data-stu-id="af60b-115">Requirement</span></span> | <span data-ttu-id="af60b-116">Значение</span><span class="sxs-lookup"><span data-stu-id="af60b-116">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="af60b-117">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="af60b-117">Minimum supported client</span></span><br/> | <span data-ttu-id="af60b-118">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="af60b-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="af60b-119">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="af60b-119">Minimum supported server</span></span><br/> | <span data-ttu-id="af60b-120">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="af60b-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="af60b-121">Заголовок</span><span class="sxs-lookup"><span data-stu-id="af60b-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="af60b-122"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="af60b-122"><dt>Netmon.h</dt></span></span> </dl>     |
| <span data-ttu-id="af60b-123">Библиотека</span><span class="sxs-lookup"><span data-stu-id="af60b-123">Library</span></span><br/>                  | <dl> <span data-ttu-id="af60b-124"><dt>Нпптулс. lib</dt></span><span class="sxs-lookup"><span data-stu-id="af60b-124"><dt>Npptools.lib</dt></span></span> </dl> |
| <span data-ttu-id="af60b-125">DLL</span><span class="sxs-lookup"><span data-stu-id="af60b-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="af60b-126"><dt>Npptools.dll</dt></span><span class="sxs-lookup"><span data-stu-id="af60b-126"><dt>Npptools.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="af60b-127">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="af60b-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="af60b-128">жетнетворкинфофромблоб</span><span class="sxs-lookup"><span data-stu-id="af60b-128">GetNetworkInfoFromBlob</span></span>](getnetworkinfofromblob.md)
</dt> <dt>

[<span data-ttu-id="af60b-129">сетбулинблоб</span><span class="sxs-lookup"><span data-stu-id="af60b-129">SetBoolInBlob</span></span>](setboolinblob.md)
</dt> <dt>

[<span data-ttu-id="af60b-130">сетклассидинблоб</span><span class="sxs-lookup"><span data-stu-id="af60b-130">SetClassIDInBlob</span></span>](setclassidinblob.md)
</dt> <dt>

[<span data-ttu-id="af60b-131">сетдвординблоб</span><span class="sxs-lookup"><span data-stu-id="af60b-131">SetDwordInBlob</span></span>](setdwordinblob.md)
</dt> <dt>

[<span data-ttu-id="af60b-132">сетмакаддрессинблоб</span><span class="sxs-lookup"><span data-stu-id="af60b-132">SetMacAddressInBlob</span></span>](setmacaddressinblob.md)
</dt> <dt>

[<span data-ttu-id="af60b-133">сетнппаддрессфилтеринблоб</span><span class="sxs-lookup"><span data-stu-id="af60b-133">SetNPPAddressFilterInBlob</span></span>](setnppaddressfilterinblob.md)
</dt> <dt>

[<span data-ttu-id="af60b-134">сетнпппаттернфилтеринблоб</span><span class="sxs-lookup"><span data-stu-id="af60b-134">SetNPPPatternFilterInBlob</span></span>](setnpppatternfilterinblob.md)
</dt> <dt>

[<span data-ttu-id="af60b-135">сетнпптригжеринблоб</span><span class="sxs-lookup"><span data-stu-id="af60b-135">SetNPPTriggerInBlob</span></span>](setnpptriggerinblob.md)
</dt> <dt>

[<span data-ttu-id="af60b-136">сетстрингинблоб</span><span class="sxs-lookup"><span data-stu-id="af60b-136">SetStringInBlob</span></span>](setstringinblob.md)
</dt> </dl>

 

 




