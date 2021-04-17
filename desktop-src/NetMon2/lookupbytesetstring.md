---
description: Функция Лукупбитесетстринг возвращает строку, соответствующую указанному значению набора с меткой.
ms.assetid: 295891f9-dc8d-4dbe-aac9-7d0a96993cfa
title: Функция Лукупбитесетстринг (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LookupByteSetString
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 7a2b5bffbfcb30ed8ec00da42fbc9ad6008fd5ef
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105673317"
---
# <a name="lookupbytesetstring-function"></a><span data-ttu-id="96b6c-103">Функция Лукупбитесетстринг</span><span class="sxs-lookup"><span data-stu-id="96b6c-103">LookupByteSetString function</span></span>

<span data-ttu-id="96b6c-104">Функция **лукупбитесетстринг** возвращает строку, соответствующую указанному значению набора с меткой.</span><span class="sxs-lookup"><span data-stu-id="96b6c-104">The **LookupByteSetString** function returns the string corresponding to the specified value of a labeled set.</span></span>

## <a name="syntax"></a><span data-ttu-id="96b6c-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="96b6c-105">Syntax</span></span>


```C++
LPBYTE WINAPI LookupByteSetString(
   LPSET lpSet,
   BYTE  Value
);
```



## <a name="parameters"></a><span data-ttu-id="96b6c-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="96b6c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="96b6c-107">*лпсет*</span><span class="sxs-lookup"><span data-stu-id="96b6c-107">*lpSet*</span></span> 
</dt> <dd>

<span data-ttu-id="96b6c-108">Указатель на набор с меткой, из которого можно извлечь метку значения.</span><span class="sxs-lookup"><span data-stu-id="96b6c-108">Pointer to a labeled set, from which you can extract the value's label.</span></span>

</dd> <dt>

<span data-ttu-id="96b6c-109">*Значение*</span><span class="sxs-lookup"><span data-stu-id="96b6c-109">*Value*</span></span> 
</dt> <dd>

<span data-ttu-id="96b6c-110">Значение набора с меткой.</span><span class="sxs-lookup"><span data-stu-id="96b6c-110">Value of a labeled set.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="96b6c-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="96b6c-111">Return value</span></span>

<span data-ttu-id="96b6c-112">Если функция выполнена успешно, возвращаемое значение является строкой, соответствующей предоставленному значению.</span><span class="sxs-lookup"><span data-stu-id="96b6c-112">If the function is successful, the return value is a string corresponding to the value provided.</span></span>

<span data-ttu-id="96b6c-113">Если функция завершилась неудачно, возвращается значение **null**.</span><span class="sxs-lookup"><span data-stu-id="96b6c-113">If the function is unsuccessful, the return value is **NULL**.</span></span>

## <a name="requirements"></a><span data-ttu-id="96b6c-114">Требования</span><span class="sxs-lookup"><span data-stu-id="96b6c-114">Requirements</span></span>



| <span data-ttu-id="96b6c-115">Требование</span><span class="sxs-lookup"><span data-stu-id="96b6c-115">Requirement</span></span> | <span data-ttu-id="96b6c-116">Значение</span><span class="sxs-lookup"><span data-stu-id="96b6c-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="96b6c-117">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="96b6c-117">Minimum supported client</span></span><br/> | <span data-ttu-id="96b6c-118">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="96b6c-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="96b6c-119">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="96b6c-119">Minimum supported server</span></span><br/> | <span data-ttu-id="96b6c-120">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="96b6c-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="96b6c-121">Заголовок</span><span class="sxs-lookup"><span data-stu-id="96b6c-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="96b6c-122"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="96b6c-122"><dt>Netmon.h</dt></span></span> </dl>   |
| <span data-ttu-id="96b6c-123">Библиотека</span><span class="sxs-lookup"><span data-stu-id="96b6c-123">Library</span></span><br/>                  | <dl> <span data-ttu-id="96b6c-124"><dt>Parser. lib</dt></span><span class="sxs-lookup"><span data-stu-id="96b6c-124"><dt>Parser.lib</dt></span></span> </dl> |
| <span data-ttu-id="96b6c-125">DLL</span><span class="sxs-lookup"><span data-stu-id="96b6c-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="96b6c-126"><dt>Nmapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="96b6c-126"><dt>Nmapi.dll</dt></span></span> </dl>  |



 

 




