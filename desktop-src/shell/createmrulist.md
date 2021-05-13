---
description: Создает новый список последних использованных (MRU) списков.
title: Функция Креатемрулиств
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CreateMRUListW
- CreateMRUListW
api_type:
- DllExport
api_location:
- Comctl32.dll
ms.assetid: b2d9e3c7-8151-45ef-9658-bd33a87b4c9c
ms.openlocfilehash: 34cd3dd9e5b9e62bbdd13b31d95e7205e4427de6
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/12/2021
ms.locfileid: "109843385"
---
# <a name="createmrulistw-function"></a><span data-ttu-id="fb626-103">Функция Креатемрулиств</span><span class="sxs-lookup"><span data-stu-id="fb626-103">CreateMRUListW function</span></span>

<span data-ttu-id="fb626-104">Создает новый список последних использованных (MRU) списков.</span><span class="sxs-lookup"><span data-stu-id="fb626-104">Creates a new most recently used (MRU) list.</span></span>

## <a name="syntax"></a><span data-ttu-id="fb626-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="fb626-105">Syntax</span></span>


```C++
int CreateMRUListW(
  _In_ LPMRUINFO lpmi
);
```



## <a name="parameters"></a><span data-ttu-id="fb626-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="fb626-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fb626-107">*лпми* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="fb626-107">*lpmi* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fb626-108">Тип: **лпмруинфо**</span><span class="sxs-lookup"><span data-stu-id="fb626-108">Type: **LPMRUINFO**</span></span>

<span data-ttu-id="fb626-109">Указатель на структуру [**мруинфо**](mruinfo.md) , определяющую список MRU.</span><span class="sxs-lookup"><span data-stu-id="fb626-109">A pointer to an [**MRUINFO**](mruinfo.md) structure defining the MRU list.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fb626-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="fb626-110">Return value</span></span>

<span data-ttu-id="fb626-111">Тип: **int**</span><span class="sxs-lookup"><span data-stu-id="fb626-111">Type: **int**</span></span>

<span data-ttu-id="fb626-112">Возвращает маркер нового списка MRU или значение 0 в случае ошибки.</span><span class="sxs-lookup"><span data-stu-id="fb626-112">Returns a handle to the new MRU list, or 0 in case of an error.</span></span>

## <a name="remarks"></a><span data-ttu-id="fb626-113">Remarks</span><span class="sxs-lookup"><span data-stu-id="fb626-113">Remarks</span></span>

<span data-ttu-id="fb626-114">Эта функция не включена в общедоступный заголовок или библиотеку.</span><span class="sxs-lookup"><span data-stu-id="fb626-114">This function is not included in a public header or library.</span></span> <span data-ttu-id="fb626-115">Доступ к нему можно получить с помощью [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) или извлечь из comctl32.dll по порядковому номеру, 400 для **креатемрулиств**.</span><span class="sxs-lookup"><span data-stu-id="fb626-115">It can be accessed through [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) or extracted from comctl32.dll by its ordinal, which is 400 for **CreateMRUListW**.</span></span>

## <a name="requirements"></a><span data-ttu-id="fb626-116">Requirements (Требования)</span><span class="sxs-lookup"><span data-stu-id="fb626-116">Requirements</span></span>



| <span data-ttu-id="fb626-117">Требование</span><span class="sxs-lookup"><span data-stu-id="fb626-117">Requirement</span></span> | <span data-ttu-id="fb626-118">Значение</span><span class="sxs-lookup"><span data-stu-id="fb626-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fb626-119">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="fb626-119">Minimum supported client</span></span><br/> | <span data-ttu-id="fb626-120">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="fb626-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="fb626-121">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="fb626-121">Minimum supported server</span></span><br/> | <span data-ttu-id="fb626-122">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="fb626-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="fb626-123">DLL</span><span class="sxs-lookup"><span data-stu-id="fb626-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fb626-124"><dt>Comctl32.dll (версия 5,0 или более поздняя)</dt></span><span class="sxs-lookup"><span data-stu-id="fb626-124"><dt>Comctl32.dll (version 5.0 or later)</dt></span></span> </dl> |
| <span data-ttu-id="fb626-125">Имя в кодировке Юникод и ANSI</span><span class="sxs-lookup"><span data-stu-id="fb626-125">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="fb626-126">**Креатемрулиств** (Юникод)</span><span class="sxs-lookup"><span data-stu-id="fb626-126">**CreateMRUListW** (Unicode)</span></span><br/>                                                                        |



 

 
