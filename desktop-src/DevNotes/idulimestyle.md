---
description: Определяет, имеет ли заданный нецветный стиль подчеркивание.
ms.assetid: 72056bf7-0a18-4ad3-a8c4-d2335a7218ae
title: Функция Идулиместиле
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IdUlIMEStyle
api_type:
- DllExport
api_location:
- Imeshare.dll
ms.openlocfilehash: 262f726e8b2201b809a9416a67c2af860acee65e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105648915"
---
# <a name="idulimestyle-function"></a><span data-ttu-id="6c84d-103">Функция Идулиместиле</span><span class="sxs-lookup"><span data-stu-id="6c84d-103">IdUlIMEStyle function</span></span>

<span data-ttu-id="6c84d-104">Определяет, имеет ли заданный нецветный стиль подчеркивание.</span><span class="sxs-lookup"><span data-stu-id="6c84d-104">Identifies whether the specified non-color style has underline.</span></span>

## <a name="syntax"></a><span data-ttu-id="6c84d-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="6c84d-105">Syntax</span></span>


```C++
UINT __cdecl IdUlIMEStyle(
  _In_ const IMESTYLE *pimestyle
);
```



## <a name="parameters"></a><span data-ttu-id="6c84d-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="6c84d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6c84d-107">*пиместиле* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="6c84d-107">*pimestyle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6c84d-108">Структура **иместиле** , возвращаемая из функции [**пиместилефроматтр**](pimestylefromattr.md) .</span><span class="sxs-lookup"><span data-stu-id="6c84d-108">An **IMESTYLE** structure returned from [**PIMEStyleFromAttr**](pimestylefromattr.md) function.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6c84d-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="6c84d-109">Return value</span></span>

<span data-ttu-id="6c84d-110">Эта функция может возвращать одно из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="6c84d-110">This function can returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="6c84d-111">**Имести \_ \_Min UL** (2002)</span><span class="sxs-lookup"><span data-stu-id="6c84d-111">**IMESTY\_UL\_MIN** (2002)</span></span>
</dt> <dt>

<span data-ttu-id="6c84d-112">**Имести \_ UL \_ None** (2002)</span><span class="sxs-lookup"><span data-stu-id="6c84d-112">**IMESTY\_UL\_NONE** (2002)</span></span>
</dt> <dt>

<span data-ttu-id="6c84d-113">**Имести \_ UL, \_ один** (2003)</span><span class="sxs-lookup"><span data-stu-id="6c84d-113">**IMESTY\_UL\_SINGLE** (2003)</span></span>
</dt> <dt>

<span data-ttu-id="6c84d-114">**Имести \_ UL, \_ пунктир** (2005)</span><span class="sxs-lookup"><span data-stu-id="6c84d-114">**IMESTY\_UL\_DOTTED** (2005)</span></span>
</dt> <dt>

<span data-ttu-id="6c84d-115">**Имести \_ UL- \_ толстая** (2006)</span><span class="sxs-lookup"><span data-stu-id="6c84d-115">**IMESTY\_UL\_THICK** (2006)</span></span>
</dt> <dt>

<span data-ttu-id="6c84d-116">**Имести \_ UL \_** (2011)</span><span class="sxs-lookup"><span data-stu-id="6c84d-116">**IMESTY\_UL\_LOWER** (2011)</span></span>
</dt> <dt>

<span data-ttu-id="6c84d-117">**Имести \_ UL \_ сиккловер** (2012)</span><span class="sxs-lookup"><span data-stu-id="6c84d-117">**IMESTY\_UL\_THICKLOWER** (2012)</span></span>
</dt> <dt>

<span data-ttu-id="6c84d-118">**Имести \_ UL \_ сиккдисловер** (2013)</span><span class="sxs-lookup"><span data-stu-id="6c84d-118">**IMESTY\_UL\_THICKDITHLOWER** (2013)</span></span>
</dt> <dt>

<span data-ttu-id="6c84d-119">**Имести \_ UL \_ дисловер** (2014)</span><span class="sxs-lookup"><span data-stu-id="6c84d-119">**IMESTY\_UL\_DITHLOWER** (2014)</span></span>
</dt> <dt>

<span data-ttu-id="6c84d-120">**Имести \_ UL \_ Max** (2014)</span><span class="sxs-lookup"><span data-stu-id="6c84d-120">**IMESTY\_UL\_MAX** (2014)</span></span>
</dt> </dl>

## <a name="remarks"></a><span data-ttu-id="6c84d-121">Комментарии</span><span class="sxs-lookup"><span data-stu-id="6c84d-121">Remarks</span></span>

<span data-ttu-id="6c84d-122">Эта функция не имеет связанной библиотеки импорта или файла заголовка. его необходимо вызвать с помощью функций [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) и [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .</span><span class="sxs-lookup"><span data-stu-id="6c84d-122">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="6c84d-123">Требования</span><span class="sxs-lookup"><span data-stu-id="6c84d-123">Requirements</span></span>



| <span data-ttu-id="6c84d-124">Требование</span><span class="sxs-lookup"><span data-stu-id="6c84d-124">Requirement</span></span> | <span data-ttu-id="6c84d-125">Значение</span><span class="sxs-lookup"><span data-stu-id="6c84d-125">Value</span></span> |
|----------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="6c84d-126">DLL</span><span class="sxs-lookup"><span data-stu-id="6c84d-126">DLL</span></span><br/> | <dl> <span data-ttu-id="6c84d-127"><dt>Imeshare.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6c84d-127"><dt>Imeshare.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6c84d-128">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="6c84d-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6c84d-129">**пиместилефроматтр**</span><span class="sxs-lookup"><span data-stu-id="6c84d-129">**PIMEStyleFromAttr**</span></span>](pimestylefromattr.md)
</dt> </dl>

 

 
