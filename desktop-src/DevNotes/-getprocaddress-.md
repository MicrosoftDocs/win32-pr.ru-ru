---
description: Возвращает адрес функции из библиотеки DLL.
ms.assetid: e425948c-5588-4a4f-994c-4e608af18439
title: Функция _GetProcAddress_
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- _GetProcAddress_
api_type:
- DllExport
api_location:
- Msmdun80.dll
- Sqlunirl.dll
ms.openlocfilehash: 0d717036b92e79056fd3b1bf69f1fd17784db713
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105657880"
---
# <a name="_getprocaddress_-function"></a><span data-ttu-id="c1ae9-103">\_\_Функция GetProcAddress</span><span class="sxs-lookup"><span data-stu-id="c1ae9-103">\_GetProcAddress\_ function</span></span>

<span data-ttu-id="c1ae9-104">\[Эта функция является оболочкой для функции **GetProcAddress** .</span><span class="sxs-lookup"><span data-stu-id="c1ae9-104">\[This function is a wrapper over the **GetProcAddress** function.</span></span> <span data-ttu-id="c1ae9-105">Эта функция может быть изменена или недоступна в будущем.</span><span class="sxs-lookup"><span data-stu-id="c1ae9-105">This function may be altered or unavailable in the future.</span></span> <span data-ttu-id="c1ae9-106">Приложения должны вызывать функцию **GetProcAddress** напрямую.\]</span><span class="sxs-lookup"><span data-stu-id="c1ae9-106">Applications should call **GetProcAddress** directly.\]</span></span>

<span data-ttu-id="c1ae9-107">Возвращает адрес функции из библиотеки DLL.</span><span class="sxs-lookup"><span data-stu-id="c1ae9-107">Gets the address of a function from a DLL.</span></span> <span data-ttu-id="c1ae9-108">См. раздел [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress).</span><span class="sxs-lookup"><span data-stu-id="c1ae9-108">See [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress).</span></span>

## <a name="syntax"></a><span data-ttu-id="c1ae9-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="c1ae9-109">Syntax</span></span>


```C++
FARPROC _GetProcAddress_(
    ...
);
```



## <a name="parameters"></a><span data-ttu-id="c1ae9-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="c1ae9-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c1ae9-111">*...*</span><span class="sxs-lookup"><span data-stu-id="c1ae9-111">*...*</span></span> 
<span data-ttu-id="c1ae9-112"></dt> <dd></dd> </dl></span><span class="sxs-lookup"><span data-stu-id="c1ae9-112"></dt> <dd></dd> </dl></span></span>

## <a name="requirements"></a><span data-ttu-id="c1ae9-113">Требования</span><span class="sxs-lookup"><span data-stu-id="c1ae9-113">Requirements</span></span>



| <span data-ttu-id="c1ae9-114">Требование</span><span class="sxs-lookup"><span data-stu-id="c1ae9-114">Requirement</span></span> | <span data-ttu-id="c1ae9-115">Значение</span><span class="sxs-lookup"><span data-stu-id="c1ae9-115">Value</span></span> |
|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c1ae9-116">DLL</span><span class="sxs-lookup"><span data-stu-id="c1ae9-116">DLL</span></span><br/> | <dl> <span data-ttu-id="c1ae9-117"><dt>Msmdun80.dll; </dt> <dt>Sqlunirl.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c1ae9-117"><dt>Msmdun80.dll; </dt> <dt>Sqlunirl.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c1ae9-118">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="c1ae9-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c1ae9-119">**GetProcAddress**</span><span class="sxs-lookup"><span data-stu-id="c1ae9-119">**GetProcAddress**</span></span>](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress)
</dt> </dl>

 

 
