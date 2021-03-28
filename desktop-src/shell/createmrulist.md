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
ms.openlocfilehash: 572e52f1461e3d48ab9eba1aa903c7fb690636d1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103808836"
---
# <a name="createmrulistw-function"></a><span data-ttu-id="e32a1-103">Функция Креатемрулиств</span><span class="sxs-lookup"><span data-stu-id="e32a1-103">CreateMRUListW function</span></span>

<span data-ttu-id="e32a1-104">Создает новый список последних использованных (MRU) списков.</span><span class="sxs-lookup"><span data-stu-id="e32a1-104">Creates a new most recently used (MRU) list.</span></span>

## <a name="syntax"></a><span data-ttu-id="e32a1-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="e32a1-105">Syntax</span></span>


```C++
int CreateMRUListW(
  _In_ LPMRUINFO lpmi
);
```



## <a name="parameters"></a><span data-ttu-id="e32a1-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="e32a1-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e32a1-107">*лпми* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="e32a1-107">*lpmi* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e32a1-108">Тип: **лпмруинфо**</span><span class="sxs-lookup"><span data-stu-id="e32a1-108">Type: **LPMRUINFO**</span></span>

<span data-ttu-id="e32a1-109">Указатель на структуру [**мруинфо**](mruinfo.md) , определяющую список MRU.</span><span class="sxs-lookup"><span data-stu-id="e32a1-109">A pointer to an [**MRUINFO**](mruinfo.md) structure defining the MRU list.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e32a1-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="e32a1-110">Return value</span></span>

<span data-ttu-id="e32a1-111">Тип: **int**</span><span class="sxs-lookup"><span data-stu-id="e32a1-111">Type: **int**</span></span>

<span data-ttu-id="e32a1-112">Возвращает маркер нового списка MRU или значение 0 в случае ошибки.</span><span class="sxs-lookup"><span data-stu-id="e32a1-112">Returns a handle to the new MRU list, or 0 in case of an error.</span></span>

## <a name="remarks"></a><span data-ttu-id="e32a1-113">Примечания</span><span class="sxs-lookup"><span data-stu-id="e32a1-113">Remarks</span></span>

<span data-ttu-id="e32a1-114">Эта функция не включена в общедоступный заголовок или библиотеку.</span><span class="sxs-lookup"><span data-stu-id="e32a1-114">This function is not included in a public header or library.</span></span> <span data-ttu-id="e32a1-115">Доступ к нему можно получить с помощью [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) или извлечь из comctl32.dll по порядковому номеру, 400 для **креатемрулиств**.</span><span class="sxs-lookup"><span data-stu-id="e32a1-115">It can be accessed through [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) or extracted from comctl32.dll by its ordinal, which is 400 for **CreateMRUListW**.</span></span>

## <a name="requirements"></a><span data-ttu-id="e32a1-116">Требования</span><span class="sxs-lookup"><span data-stu-id="e32a1-116">Requirements</span></span>



| <span data-ttu-id="e32a1-117">Требование</span><span class="sxs-lookup"><span data-stu-id="e32a1-117">Requirement</span></span> | <span data-ttu-id="e32a1-118">Значение</span><span class="sxs-lookup"><span data-stu-id="e32a1-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e32a1-119">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="e32a1-119">Minimum supported client</span></span><br/> | <span data-ttu-id="e32a1-120">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="e32a1-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="e32a1-121">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="e32a1-121">Minimum supported server</span></span><br/> | <span data-ttu-id="e32a1-122">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="e32a1-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="e32a1-123">DLL</span><span class="sxs-lookup"><span data-stu-id="e32a1-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e32a1-124"><dt>Comctl32.dll (версия 5,0 или более поздняя)</dt></span><span class="sxs-lookup"><span data-stu-id="e32a1-124"><dt>Comctl32.dll (version 5.0 or later)</dt></span></span> </dl> |
| <span data-ttu-id="e32a1-125">Имя в кодировке Юникод и ANSI</span><span class="sxs-lookup"><span data-stu-id="e32a1-125">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="e32a1-126">**Креатемрулиств** (Юникод)</span><span class="sxs-lookup"><span data-stu-id="e32a1-126">**CreateMRUListW** (Unicode)</span></span><br/>                                                                        |



 

 
