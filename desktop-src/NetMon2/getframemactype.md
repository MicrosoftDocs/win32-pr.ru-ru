---
description: Функция Жетфрамемактипе Возвращает тип MAC фрейма.
ms.assetid: 8d3da770-1392-4638-a267-32c2dae289b0
title: Функция Жетфрамемактипе (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetFrameMacType
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: b85accc64a6e29424e3f65d070bafcf29bb3ec0f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103990904"
---
# <a name="getframemactype-function"></a><span data-ttu-id="28f2c-103">Функция Жетфрамемактипе</span><span class="sxs-lookup"><span data-stu-id="28f2c-103">GetFrameMacType function</span></span>

<span data-ttu-id="28f2c-104">Функция **жетфрамемактипе** ВОЗВРАЩАЕТ тип Mac фрейма.</span><span class="sxs-lookup"><span data-stu-id="28f2c-104">The **GetFrameMacType** function returns the MAC type of the frame.</span></span>

## <a name="syntax"></a><span data-ttu-id="28f2c-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="28f2c-105">Syntax</span></span>


```C++
DWORD WINAPI GetFrameMacType(
  _In_ HFRAME hFrame
);
```



## <a name="parameters"></a><span data-ttu-id="28f2c-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="28f2c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="28f2c-107">*хфраме* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="28f2c-107">*hFrame* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="28f2c-108">Обработчик для фрейма.</span><span class="sxs-lookup"><span data-stu-id="28f2c-108">Handle to the frame.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="28f2c-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="28f2c-109">Return value</span></span>

<span data-ttu-id="28f2c-110">Функция возвращает тип MAC фрейма, который может иметь одно из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="28f2c-110">The function returns the MAC type of the frame, which can have one of the following values.</span></span>

-   <span data-ttu-id="28f2c-111">\_неизвестный тип Mac \_</span><span class="sxs-lookup"><span data-stu-id="28f2c-111">MAC\_TYPE\_UNKNOWN</span></span>
-   <span data-ttu-id="28f2c-112">\_тип Mac \_ Ethernet</span><span class="sxs-lookup"><span data-stu-id="28f2c-112">MAC\_TYPE\_ETHERNET</span></span>
-   <span data-ttu-id="28f2c-113">\_тип Mac \_ токенринг</span><span class="sxs-lookup"><span data-stu-id="28f2c-113">MAC\_TYPE\_TOKENRING</span></span>
-   <span data-ttu-id="28f2c-114">\_тип Mac \_ FDDI</span><span class="sxs-lookup"><span data-stu-id="28f2c-114">MAC\_TYPE\_FDDI</span></span>

## <a name="remarks"></a><span data-ttu-id="28f2c-115">Комментарии</span><span class="sxs-lookup"><span data-stu-id="28f2c-115">Remarks</span></span>

<span data-ttu-id="28f2c-116">[*Эксперты*](e.md) и [*средства синтаксического анализа*](p.md) могут вызывать функцию **жетфрамемактипе** .</span><span class="sxs-lookup"><span data-stu-id="28f2c-116">[*Experts*](e.md) and [*parsers*](p.md) can call the **GetFrameMacType** function.</span></span>

## <a name="requirements"></a><span data-ttu-id="28f2c-117">Требования</span><span class="sxs-lookup"><span data-stu-id="28f2c-117">Requirements</span></span>



| <span data-ttu-id="28f2c-118">Требование</span><span class="sxs-lookup"><span data-stu-id="28f2c-118">Requirement</span></span> | <span data-ttu-id="28f2c-119">Значение</span><span class="sxs-lookup"><span data-stu-id="28f2c-119">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="28f2c-120">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="28f2c-120">Minimum supported client</span></span><br/> | <span data-ttu-id="28f2c-121">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="28f2c-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="28f2c-122">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="28f2c-122">Minimum supported server</span></span><br/> | <span data-ttu-id="28f2c-123">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="28f2c-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="28f2c-124">Заголовок</span><span class="sxs-lookup"><span data-stu-id="28f2c-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="28f2c-125"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="28f2c-125"><dt>Netmon.h</dt></span></span> </dl>  |
| <span data-ttu-id="28f2c-126">Библиотека</span><span class="sxs-lookup"><span data-stu-id="28f2c-126">Library</span></span><br/>                  | <dl> <span data-ttu-id="28f2c-127"><dt>Нмапи. lib</dt></span><span class="sxs-lookup"><span data-stu-id="28f2c-127"><dt>Nmapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="28f2c-128">DLL</span><span class="sxs-lookup"><span data-stu-id="28f2c-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="28f2c-129"><dt>Nmapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="28f2c-129"><dt>Nmapi.dll</dt></span></span> </dl> |



 

 




