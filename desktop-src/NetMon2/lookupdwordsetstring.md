---
description: Функция Лукупдвордсетстринг возвращает строку, соответствующую указанному значению набора с меткой.
ms.assetid: ee2b1b7a-6b64-4c8c-a71d-de970b66d46e
title: Функция Лукупдвордсетстринг (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LookupDwordSetString
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 57688edab7421f939e03322b8b244219b00d31fb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103810289"
---
# <a name="lookupdwordsetstring-function"></a><span data-ttu-id="f9623-103">Функция Лукупдвордсетстринг</span><span class="sxs-lookup"><span data-stu-id="f9623-103">LookupDwordSetString function</span></span>

<span data-ttu-id="f9623-104">Функция **лукупдвордсетстринг** возвращает строку, соответствующую указанному значению набора с меткой.</span><span class="sxs-lookup"><span data-stu-id="f9623-104">The **LookupDwordSetString** function returns the string corresponding to the specified value of a labeled set.</span></span>

## <a name="syntax"></a><span data-ttu-id="f9623-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="f9623-105">Syntax</span></span>


```C++
LPBYTE WINAPI LookupDwordSetString(
   LPSET lpSet,
   DWORD Value
);
```



## <a name="parameters"></a><span data-ttu-id="f9623-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="f9623-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f9623-107">*лпсет*</span><span class="sxs-lookup"><span data-stu-id="f9623-107">*lpSet*</span></span> 
</dt> <dd>

<span data-ttu-id="f9623-108">Набор с метками, из которого можно извлечь метку значения.</span><span class="sxs-lookup"><span data-stu-id="f9623-108">Labeled set, from which you can extract the value's label.</span></span>

</dd> <dt>

<span data-ttu-id="f9623-109">*Значение*</span><span class="sxs-lookup"><span data-stu-id="f9623-109">*Value*</span></span> 
</dt> <dd>

<span data-ttu-id="f9623-110">Значение набора с меткой.</span><span class="sxs-lookup"><span data-stu-id="f9623-110">Value of a labeled set.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f9623-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="f9623-111">Return value</span></span>

<span data-ttu-id="f9623-112">Если функция выполнена успешно, возвращаемое значение является строкой, соответствующей указанному значению.</span><span class="sxs-lookup"><span data-stu-id="f9623-112">If the function is successful, the return value is the string that corresponds to the specified value.</span></span>

<span data-ttu-id="f9623-113">Если функция завершилась неудачно, указанное значение отсутствует в наборе, возвращаемое значение равно **null**.</span><span class="sxs-lookup"><span data-stu-id="f9623-113">If the function is unsuccessful, the specified value is not in the set, the return value is **NULL**.</span></span>

## <a name="requirements"></a><span data-ttu-id="f9623-114">Требования</span><span class="sxs-lookup"><span data-stu-id="f9623-114">Requirements</span></span>



| <span data-ttu-id="f9623-115">Требование</span><span class="sxs-lookup"><span data-stu-id="f9623-115">Requirement</span></span> | <span data-ttu-id="f9623-116">Значение</span><span class="sxs-lookup"><span data-stu-id="f9623-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="f9623-117">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="f9623-117">Minimum supported client</span></span><br/> | <span data-ttu-id="f9623-118">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="f9623-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="f9623-119">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="f9623-119">Minimum supported server</span></span><br/> | <span data-ttu-id="f9623-120">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="f9623-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="f9623-121">Заголовок</span><span class="sxs-lookup"><span data-stu-id="f9623-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="f9623-122"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="f9623-122"><dt>Netmon.h</dt></span></span> </dl>   |
| <span data-ttu-id="f9623-123">Библиотека</span><span class="sxs-lookup"><span data-stu-id="f9623-123">Library</span></span><br/>                  | <dl> <span data-ttu-id="f9623-124"><dt>Parser. lib</dt></span><span class="sxs-lookup"><span data-stu-id="f9623-124"><dt>Parser.lib</dt></span></span> </dl> |
| <span data-ttu-id="f9623-125">DLL</span><span class="sxs-lookup"><span data-stu-id="f9623-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f9623-126"><dt>Nmapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f9623-126"><dt>Nmapi.dll</dt></span></span> </dl>  |



 

 




