---
description: Функция Лоадстрингаддр преобразует строку (например, &\# 0034; 157.54.32.45&\# 0034;) и создает адрес DWORD.
ms.assetid: 305e0072-b597-4cd5-975e-94103a1680aa
title: Функция Лоадстрингаддр (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LoadStringAddr
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 3317c8e842c23daa08f260063a8310404c92aed5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105673320"
---
# <a name="loadstringaddr-function"></a><span data-ttu-id="472c3-103">Функция Лоадстрингаддр</span><span class="sxs-lookup"><span data-stu-id="472c3-103">LoadStringAddr function</span></span>

<span data-ttu-id="472c3-104">Функция **лоадстрингаддр** преобразует строку (например, "157.54.32.45") и создает адрес **DWORD** .</span><span class="sxs-lookup"><span data-stu-id="472c3-104">The **LoadStringAddr** function transforms a string (such as "157.54.32.45") and creates a **DWORD** address.</span></span>

## <a name="syntax"></a><span data-ttu-id="472c3-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="472c3-105">Syntax</span></span>


```C++
BOOL LoadStringAddr(
         DWORD *pAddress,
   const char  *str
);
```



## <a name="parameters"></a><span data-ttu-id="472c3-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="472c3-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="472c3-107">*паддресс*</span><span class="sxs-lookup"><span data-stu-id="472c3-107">*pAddress*</span></span> 
</dt> <dd>

<span data-ttu-id="472c3-108">Указатель на **DWORD**.</span><span class="sxs-lookup"><span data-stu-id="472c3-108">Pointer to a **DWORD**.</span></span>

</dd> <dt>

<span data-ttu-id="472c3-109">*str*</span><span class="sxs-lookup"><span data-stu-id="472c3-109">*str*</span></span> 
</dt> <dd>

<span data-ttu-id="472c3-110">Указатель на строку символов с представлением IP-адреса x. x. x. x (например, 127.0.0.1).</span><span class="sxs-lookup"><span data-stu-id="472c3-110">Pointer to a character string with x.x.x.x representation of an IP address (for example,127.0.0.1).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="472c3-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="472c3-111">Return value</span></span>

<span data-ttu-id="472c3-112">Значение, если функция выполнена успешно (обнаружено имя адреса); Возвращаемое значение равно **true**.</span><span class="sxs-lookup"><span data-stu-id="472c3-112">If the function is successful (the address name was found); the return value is **TRUE**.</span></span>

<span data-ttu-id="472c3-113">Если функция завершается неудачно, возвращается значение **false**.</span><span class="sxs-lookup"><span data-stu-id="472c3-113">If the function is unsuccessful, the return value is **FALSE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="472c3-114">Требования</span><span class="sxs-lookup"><span data-stu-id="472c3-114">Requirements</span></span>



| <span data-ttu-id="472c3-115">Требование</span><span class="sxs-lookup"><span data-stu-id="472c3-115">Requirement</span></span> | <span data-ttu-id="472c3-116">Значение</span><span class="sxs-lookup"><span data-stu-id="472c3-116">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="472c3-117">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="472c3-117">Minimum supported client</span></span><br/> | <span data-ttu-id="472c3-118">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="472c3-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="472c3-119">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="472c3-119">Minimum supported server</span></span><br/> | <span data-ttu-id="472c3-120">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="472c3-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="472c3-121">Заголовок</span><span class="sxs-lookup"><span data-stu-id="472c3-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="472c3-122"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="472c3-122"><dt>Netmon.h</dt></span></span> </dl>  |
| <span data-ttu-id="472c3-123">Библиотека</span><span class="sxs-lookup"><span data-stu-id="472c3-123">Library</span></span><br/>                  | <dl> <span data-ttu-id="472c3-124"><dt>Нмапи. lib</dt></span><span class="sxs-lookup"><span data-stu-id="472c3-124"><dt>Nmapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="472c3-125">DLL</span><span class="sxs-lookup"><span data-stu-id="472c3-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="472c3-126"><dt>Nmapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="472c3-126"><dt>Nmapi.dll</dt></span></span> </dl> |



 

 




