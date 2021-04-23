---
description: Функция Аддресстостринг преобразует адрес в строку.
ms.assetid: 999a6142-1423-4006-a489-63895dd19ce3
title: Функция Аддресстостринг (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AddressToString
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 0c7c659a05167055b18c36e5c6c36465538af483
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104156842"
---
# <a name="addresstostring-function"></a><span data-ttu-id="2dc93-103">Функция Аддресстостринг</span><span class="sxs-lookup"><span data-stu-id="2dc93-103">AddressToString function</span></span>

<span data-ttu-id="2dc93-104">Функция **аддресстостринг** преобразует адрес в строку.</span><span class="sxs-lookup"><span data-stu-id="2dc93-104">The **AddressToString** function converts an address into a string.</span></span>

## <a name="syntax"></a><span data-ttu-id="2dc93-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="2dc93-105">Syntax</span></span>


```C++
LPSTR WINAPI AddressToString(
  _Out_ LPSTR string,
  _In_  BYTE  *lpAddress
);
```



## <a name="parameters"></a><span data-ttu-id="2dc93-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="2dc93-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2dc93-107">*строка* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="2dc93-107">*string* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="2dc93-108">Строка, в которую преобразуется адрес.</span><span class="sxs-lookup"><span data-stu-id="2dc93-108">String that the address is converted to.</span></span>

</dd> <dt>

<span data-ttu-id="2dc93-109">*лпаддресс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="2dc93-109">*lpAddress* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2dc93-110">Выводимый адрес.</span><span class="sxs-lookup"><span data-stu-id="2dc93-110">The address that is printed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2dc93-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="2dc93-111">Return value</span></span>

<span data-ttu-id="2dc93-112">Возвращаемое значение является указателем на преобразованную строку.</span><span class="sxs-lookup"><span data-stu-id="2dc93-112">The return value is a pointer to the converted string.</span></span>

## <a name="requirements"></a><span data-ttu-id="2dc93-113">Требования</span><span class="sxs-lookup"><span data-stu-id="2dc93-113">Requirements</span></span>



| <span data-ttu-id="2dc93-114">Требование</span><span class="sxs-lookup"><span data-stu-id="2dc93-114">Requirement</span></span> | <span data-ttu-id="2dc93-115">Значение</span><span class="sxs-lookup"><span data-stu-id="2dc93-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="2dc93-116">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="2dc93-116">Minimum supported client</span></span><br/> | <span data-ttu-id="2dc93-117">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="2dc93-117">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="2dc93-118">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="2dc93-118">Minimum supported server</span></span><br/> | <span data-ttu-id="2dc93-119">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="2dc93-119">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="2dc93-120">Заголовок</span><span class="sxs-lookup"><span data-stu-id="2dc93-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="2dc93-121"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="2dc93-121"><dt>Netmon.h</dt></span></span> </dl>   |
| <span data-ttu-id="2dc93-122">Библиотека</span><span class="sxs-lookup"><span data-stu-id="2dc93-122">Library</span></span><br/>                  | <dl> <span data-ttu-id="2dc93-123"><dt>Parser. lib</dt></span><span class="sxs-lookup"><span data-stu-id="2dc93-123"><dt>Parser.lib</dt></span></span> </dl> |
| <span data-ttu-id="2dc93-124">DLL</span><span class="sxs-lookup"><span data-stu-id="2dc93-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2dc93-125"><dt>Nmapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2dc93-125"><dt>Nmapi.dll</dt></span></span> </dl>  |



 

 




