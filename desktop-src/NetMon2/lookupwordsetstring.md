---
description: Функция Лукупвордсетстринг возвращает строку, соответствующую запрошенному значению из набора с меткой.
ms.assetid: e8d158a1-8544-4c10-b8e8-46888c1097e4
title: Функция Лукупвордсетстринг (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LookupWordSetString
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 7487becb195571e1eb88044195293b2c0b226e8e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104542375"
---
# <a name="lookupwordsetstring-function"></a><span data-ttu-id="c3f52-103">Функция Лукупвордсетстринг</span><span class="sxs-lookup"><span data-stu-id="c3f52-103">LookupWordSetString function</span></span>

<span data-ttu-id="c3f52-104">Функция **лукупвордсетстринг** возвращает строку, соответствующую запрошенному значению из набора с меткой.</span><span class="sxs-lookup"><span data-stu-id="c3f52-104">The **LookupWordSetString** function returns the string corresponding to the requested value from a labeled set.</span></span>

## <a name="syntax"></a><span data-ttu-id="c3f52-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="c3f52-105">Syntax</span></span>


```C++
LPBYTE WINAPI LookupWordSetString(
   LPSET lpSet,
   WORD  Value
);
```



## <a name="parameters"></a><span data-ttu-id="c3f52-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="c3f52-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c3f52-107">*лпсет*</span><span class="sxs-lookup"><span data-stu-id="c3f52-107">*lpSet*</span></span> 
</dt> <dd>

<span data-ttu-id="c3f52-108">Набор с меткой, из которого извлекается метка значения.</span><span class="sxs-lookup"><span data-stu-id="c3f52-108">Labeled set from which you extract the value's label.</span></span>

</dd> <dt>

<span data-ttu-id="c3f52-109">*Значение*</span><span class="sxs-lookup"><span data-stu-id="c3f52-109">*Value*</span></span> 
</dt> <dd>

<span data-ttu-id="c3f52-110">Значение набора с меткой.</span><span class="sxs-lookup"><span data-stu-id="c3f52-110">Value of a labeled set.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c3f52-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="c3f52-111">Return value</span></span>

<span data-ttu-id="c3f52-112">Если функция выполнена успешно, возвращаемое значение является строкой, соответствующей запрошенному значению.</span><span class="sxs-lookup"><span data-stu-id="c3f52-112">If the function is successful, the return value is a string that corresponds to the requested value.</span></span>

<span data-ttu-id="c3f52-113">Если функция завершилась неудачно, указанное значение отсутствует в наборе, возвращаемое значение равно **null**.</span><span class="sxs-lookup"><span data-stu-id="c3f52-113">If the function is unsuccessful, the specified value is not in the set, the return value is **NULL**.</span></span>

## <a name="requirements"></a><span data-ttu-id="c3f52-114">Требования</span><span class="sxs-lookup"><span data-stu-id="c3f52-114">Requirements</span></span>



| <span data-ttu-id="c3f52-115">Требование</span><span class="sxs-lookup"><span data-stu-id="c3f52-115">Requirement</span></span> | <span data-ttu-id="c3f52-116">Значение</span><span class="sxs-lookup"><span data-stu-id="c3f52-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="c3f52-117">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="c3f52-117">Minimum supported client</span></span><br/> | <span data-ttu-id="c3f52-118">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="c3f52-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="c3f52-119">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="c3f52-119">Minimum supported server</span></span><br/> | <span data-ttu-id="c3f52-120">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="c3f52-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="c3f52-121">Заголовок</span><span class="sxs-lookup"><span data-stu-id="c3f52-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="c3f52-122"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="c3f52-122"><dt>Netmon.h</dt></span></span> </dl>   |
| <span data-ttu-id="c3f52-123">Библиотека</span><span class="sxs-lookup"><span data-stu-id="c3f52-123">Library</span></span><br/>                  | <dl> <span data-ttu-id="c3f52-124"><dt>Parser. lib</dt></span><span class="sxs-lookup"><span data-stu-id="c3f52-124"><dt>Parser.lib</dt></span></span> </dl> |
| <span data-ttu-id="c3f52-125">DLL</span><span class="sxs-lookup"><span data-stu-id="c3f52-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c3f52-126"><dt>Nmapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c3f52-126"><dt>Nmapi.dll</dt></span></span> </dl>  |



 

 




