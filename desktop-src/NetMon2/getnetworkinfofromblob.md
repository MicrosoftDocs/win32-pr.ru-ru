---
description: Функция Жетнетворкинфофромблоб извлекает сведения о сети из заданного большого двоичного объекта.
ms.assetid: 217c33f4-e548-4072-9edd-ded61e6cd743
title: Функция Жетнетворкинфофромблоб (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetNetworkInfoFromBlob
api_type:
- DllExport
api_location:
- Npptools.dll
ms.openlocfilehash: 2f8b15dce010febdc952c2527a9f4ad31054fa3b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105674490"
---
# <a name="getnetworkinfofromblob-function"></a><span data-ttu-id="b136e-103">Функция Жетнетворкинфофромблоб</span><span class="sxs-lookup"><span data-stu-id="b136e-103">GetNetworkInfoFromBlob function</span></span>

<span data-ttu-id="b136e-104">Функция **жетнетворкинфофромблоб** извлекает сведения о сети из заданного большого двоичного объекта.</span><span class="sxs-lookup"><span data-stu-id="b136e-104">The **GetNetworkInfoFromBlob** function retrieves network information from a given BLOB.</span></span>

## <a name="syntax"></a><span data-ttu-id="b136e-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="b136e-105">Syntax</span></span>


```C++
DWORD GetNetworkInfoFromBlob(
  _In_    HBLOB         hBlob,
  _Inout_ LPNETWORKINFO lpNetworkInfo
);
```



## <a name="parameters"></a><span data-ttu-id="b136e-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="b136e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b136e-107">*хблоб* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="b136e-107">*hBlob* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b136e-108">Обработчик для большого двоичного объекта.</span><span class="sxs-lookup"><span data-stu-id="b136e-108">Handle to a BLOB.</span></span>

</dd> <dt>

<span data-ttu-id="b136e-109">*лпнетворкинфо* \[ в, out\]</span><span class="sxs-lookup"><span data-stu-id="b136e-109">*lpNetworkInfo* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="b136e-110">Указатель на выделенную пользователем структуру [нетворкинфо](networkinfo.md) , которая заполняется.</span><span class="sxs-lookup"><span data-stu-id="b136e-110">A pointer to the user-allocated [NETWORKINFO](networkinfo.md) structure that is filled in.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b136e-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="b136e-111">Return value</span></span>

<span data-ttu-id="b136e-112">Если функция **жетнетворкинфофромблоб** выполнена успешно, возвращается значение нмерр \_ Success.</span><span class="sxs-lookup"><span data-stu-id="b136e-112">If the **GetNetworkInfoFromBlob** function is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="b136e-113">Если функция завершается неудачно, возвращается значение НМЕРР, описывающее ошибку.</span><span class="sxs-lookup"><span data-stu-id="b136e-113">If the function is unsuccessful, the return value is a NMERR value that describes the error.</span></span>

## <a name="remarks"></a><span data-ttu-id="b136e-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="b136e-114">Remarks</span></span>

<span data-ttu-id="b136e-115">Сведения о сети хранятся в разделе **нетворкинфо** большого двоичного объекта категории **владельца** BLOB-объекта НПП.</span><span class="sxs-lookup"><span data-stu-id="b136e-115">The network information is stored in the BLOB **NetworkInfo** section of the BLOB NPP **Owner** category.</span></span>

## <a name="requirements"></a><span data-ttu-id="b136e-116">Требования</span><span class="sxs-lookup"><span data-stu-id="b136e-116">Requirements</span></span>



| <span data-ttu-id="b136e-117">Требование</span><span class="sxs-lookup"><span data-stu-id="b136e-117">Requirement</span></span> | <span data-ttu-id="b136e-118">Значение</span><span class="sxs-lookup"><span data-stu-id="b136e-118">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b136e-119">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="b136e-119">Minimum supported client</span></span><br/> | <span data-ttu-id="b136e-120">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="b136e-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="b136e-121">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="b136e-121">Minimum supported server</span></span><br/> | <span data-ttu-id="b136e-122">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="b136e-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="b136e-123">Заголовок</span><span class="sxs-lookup"><span data-stu-id="b136e-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="b136e-124"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="b136e-124"><dt>Netmon.h</dt></span></span> </dl>     |
| <span data-ttu-id="b136e-125">Библиотека</span><span class="sxs-lookup"><span data-stu-id="b136e-125">Library</span></span><br/>                  | <dl> <span data-ttu-id="b136e-126"><dt>Нпптулс. lib</dt></span><span class="sxs-lookup"><span data-stu-id="b136e-126"><dt>Npptools.lib</dt></span></span> </dl> |
| <span data-ttu-id="b136e-127">DLL</span><span class="sxs-lookup"><span data-stu-id="b136e-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b136e-128"><dt>Npptools.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b136e-128"><dt>Npptools.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b136e-129">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="b136e-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b136e-130">сетнетворкинфоинблоб</span><span class="sxs-lookup"><span data-stu-id="b136e-130">SetNetworkInfoInBlob</span></span>](setnetworkinfoinblob.md)
</dt> <dt>

[<span data-ttu-id="b136e-131">жетбулфромблоб</span><span class="sxs-lookup"><span data-stu-id="b136e-131">GetBoolFromBlob</span></span>](getboolfromblob.md)
</dt> <dt>

[<span data-ttu-id="b136e-132">жетклассидфромблоб</span><span class="sxs-lookup"><span data-stu-id="b136e-132">GetClassIDFromBlob</span></span>](getclassidfromblob.md)
</dt> <dt>

[<span data-ttu-id="b136e-133">жетдвордфромблоб</span><span class="sxs-lookup"><span data-stu-id="b136e-133">GetDwordFromBlob</span></span>](getdwordfromblob.md)
</dt> <dt>

[<span data-ttu-id="b136e-134">жетмакаддрессфромблоб</span><span class="sxs-lookup"><span data-stu-id="b136e-134">GetMacAddressFromBlob</span></span>](getmacaddressfromblob.md)
</dt> <dt>

[<span data-ttu-id="b136e-135">жетнппаддрессфилтерфромблоб</span><span class="sxs-lookup"><span data-stu-id="b136e-135">GetNPPAddressFilterFromBlob</span></span>](getnppaddressfilterfromblob.md)
</dt> <dt>

[<span data-ttu-id="b136e-136">жетнпппаттернфилтерфромблоб</span><span class="sxs-lookup"><span data-stu-id="b136e-136">GetNPPPatternFilterFromBlob</span></span>](getnpppatternfilterfromblob.md)
</dt> <dt>

[<span data-ttu-id="b136e-137">жетнпптригжерфромблоб</span><span class="sxs-lookup"><span data-stu-id="b136e-137">GetNPPTriggerFromBlob</span></span>](getnpptriggerfromblob.md)
</dt> <dt>

[<span data-ttu-id="b136e-138">жетстрингфромблоб</span><span class="sxs-lookup"><span data-stu-id="b136e-138">GetStringFromBlob</span></span>](getstringfromblob.md)
</dt> <dt>

[<span data-ttu-id="b136e-139">жетстрингсфромблоб</span><span class="sxs-lookup"><span data-stu-id="b136e-139">GetStringsFromBlob</span></span>](getstringsfromblob.md)
</dt> </dl>

 

 




