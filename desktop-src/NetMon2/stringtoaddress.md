---
description: Функция Стрингтоаддресс преобразует строку в адрес.
ms.assetid: b1ada88d-04bb-4869-87c6-99f5046356c5
title: Функция Стрингтоаддресс (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- StringToAddress
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 70a9e6b42359a2f73fba55194c9b6e6e21ffa9a4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105683224"
---
# <a name="stringtoaddress-function"></a><span data-ttu-id="8d0c3-103">Функция Стрингтоаддресс</span><span class="sxs-lookup"><span data-stu-id="8d0c3-103">StringToAddress function</span></span>

<span data-ttu-id="8d0c3-104">Функция **стрингтоаддресс** преобразует строку в адрес.</span><span class="sxs-lookup"><span data-stu-id="8d0c3-104">The **StringToAddress** function converts a string to an address.</span></span>

## <a name="syntax"></a><span data-ttu-id="8d0c3-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="8d0c3-105">Syntax</span></span>


```C++
LPBYTE WINAPI StringToAddress(
  _Out_ BYTE  *lpAddress,
  _In_  LPSTR string
);
```



## <a name="parameters"></a><span data-ttu-id="8d0c3-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="8d0c3-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8d0c3-107">*лпаддресс* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="8d0c3-107">*lpAddress* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8d0c3-108">Указатель на адрес, в который преобразуется строка.</span><span class="sxs-lookup"><span data-stu-id="8d0c3-108">Pointer to the address the string is converted to.</span></span>

</dd> <dt>

<span data-ttu-id="8d0c3-109">*строка* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="8d0c3-109">*string* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8d0c3-110">Строка, которая преобразуется в адрес.</span><span class="sxs-lookup"><span data-stu-id="8d0c3-110">String that is converted to an address.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8d0c3-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="8d0c3-111">Return value</span></span>

<span data-ttu-id="8d0c3-112">Возвращаемое значение является указателем на преобразованную строку.</span><span class="sxs-lookup"><span data-stu-id="8d0c3-112">The return value is a pointer to the converted string.</span></span>

## <a name="requirements"></a><span data-ttu-id="8d0c3-113">Требования</span><span class="sxs-lookup"><span data-stu-id="8d0c3-113">Requirements</span></span>



| <span data-ttu-id="8d0c3-114">Требование</span><span class="sxs-lookup"><span data-stu-id="8d0c3-114">Requirement</span></span> | <span data-ttu-id="8d0c3-115">Значение</span><span class="sxs-lookup"><span data-stu-id="8d0c3-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="8d0c3-116">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="8d0c3-116">Minimum supported client</span></span><br/> | <span data-ttu-id="8d0c3-117">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="8d0c3-117">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="8d0c3-118">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="8d0c3-118">Minimum supported server</span></span><br/> | <span data-ttu-id="8d0c3-119">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="8d0c3-119">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="8d0c3-120">Заголовок</span><span class="sxs-lookup"><span data-stu-id="8d0c3-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="8d0c3-121"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="8d0c3-121"><dt>Netmon.h</dt></span></span> </dl>   |
| <span data-ttu-id="8d0c3-122">Библиотека</span><span class="sxs-lookup"><span data-stu-id="8d0c3-122">Library</span></span><br/>                  | <dl> <span data-ttu-id="8d0c3-123"><dt>Parser. lib</dt></span><span class="sxs-lookup"><span data-stu-id="8d0c3-123"><dt>Parser.lib</dt></span></span> </dl> |
| <span data-ttu-id="8d0c3-124">DLL</span><span class="sxs-lookup"><span data-stu-id="8d0c3-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8d0c3-125"><dt>Nmapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8d0c3-125"><dt>Nmapi.dll</dt></span></span> </dl>  |



 

 




