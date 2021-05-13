---
description: Используется для определения наличия элемента в списке последних использованных элементов.
title: Функция обратного вызова МРУКМППРОК
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MRUCMPPROC
- MRUCMPPROCA
- MRUCMPPROCW
api_type:
- UserDefined
api_location: ''
ms.assetid: 00f31d6b-2a96-4abd-9647-24a6e66aa22f
ms.openlocfilehash: 83020fbcd0d4cfcfbc643d1360e3671595de6f32
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/12/2021
ms.locfileid: "109840785"
---
# <a name="mrucmpproc-callback-function"></a><span data-ttu-id="cb7aa-103">Функция обратного вызова МРУКМППРОК</span><span class="sxs-lookup"><span data-stu-id="cb7aa-103">MRUCMPPROC callback function</span></span>

<span data-ttu-id="cb7aa-104">Используется для определения наличия элемента в списке последних использованных элементов.</span><span class="sxs-lookup"><span data-stu-id="cb7aa-104">Used to determine whether an item is present in a most recently used (MRU) list.</span></span>

## <a name="syntax"></a><span data-ttu-id="cb7aa-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="cb7aa-105">Syntax</span></span>


```C++
int CALLBACK MRUCMPPROC(
   LPCTSTR pString1,
   LPCTSTR pString2
);
```



## <a name="parameters"></a><span data-ttu-id="cb7aa-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="cb7aa-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cb7aa-107">*pString1*</span><span class="sxs-lookup"><span data-stu-id="cb7aa-107">*pString1*</span></span> 
</dt> <dd>

<span data-ttu-id="cb7aa-108">Тип: **LPCTSTR**</span><span class="sxs-lookup"><span data-stu-id="cb7aa-108">Type: **LPCTSTR**</span></span>

<span data-ttu-id="cb7aa-109">Первая строка.</span><span class="sxs-lookup"><span data-stu-id="cb7aa-109">The first string.</span></span>

</dd> <dt>

<span data-ttu-id="cb7aa-110">*pString2*</span><span class="sxs-lookup"><span data-stu-id="cb7aa-110">*pString2*</span></span> 
</dt> <dd>

<span data-ttu-id="cb7aa-111">Тип: **LPCTSTR**</span><span class="sxs-lookup"><span data-stu-id="cb7aa-111">Type: **LPCTSTR**</span></span>

<span data-ttu-id="cb7aa-112">Вторая строка для сравнения с первой.</span><span class="sxs-lookup"><span data-stu-id="cb7aa-112">A second string to compare to the first.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cb7aa-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="cb7aa-113">Return value</span></span>

<span data-ttu-id="cb7aa-114">Тип: **int**</span><span class="sxs-lookup"><span data-stu-id="cb7aa-114">Type: **int**</span></span>

<span data-ttu-id="cb7aa-115">Возвращает 0, если элементы идентичны, в противном случае — ненулевое значение.</span><span class="sxs-lookup"><span data-stu-id="cb7aa-115">Returns 0 if the items are identical, a nonzero value otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="cb7aa-116">Remarks</span><span class="sxs-lookup"><span data-stu-id="cb7aa-116">Remarks</span></span>

<span data-ttu-id="cb7aa-117">Эту функцию можно дополнительно указать для использования в структуре [**мруинфо**](mruinfo.md) , передаваемой в [**креатемрулиств**](createmrulist.md).</span><span class="sxs-lookup"><span data-stu-id="cb7aa-117">This function can be optionally specified for use in the [**MRUINFO**](mruinfo.md) structure passed to [**CreateMRUListW**](createmrulist.md).</span></span> <span data-ttu-id="cb7aa-118">Это полезно, если список MRU был создан с помощью флага **\_ двоичного файла MRU** .</span><span class="sxs-lookup"><span data-stu-id="cb7aa-118">This is useful when the MRU list was created with the **MRU\_BINARY** flag.</span></span> <span data-ttu-id="cb7aa-119">Если эта функция не задана, используются стандартные функции сравнения строк.</span><span class="sxs-lookup"><span data-stu-id="cb7aa-119">When this function is not specified, standard string comparison functions are used.</span></span>

## <a name="requirements"></a><span data-ttu-id="cb7aa-120">Requirements (Требования)</span><span class="sxs-lookup"><span data-stu-id="cb7aa-120">Requirements</span></span>



| <span data-ttu-id="cb7aa-121">Требование</span><span class="sxs-lookup"><span data-stu-id="cb7aa-121">Requirement</span></span> | <span data-ttu-id="cb7aa-122">Значение</span><span class="sxs-lookup"><span data-stu-id="cb7aa-122">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------|
| <span data-ttu-id="cb7aa-123">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="cb7aa-123">Minimum supported client</span></span><br/> | <span data-ttu-id="cb7aa-124">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="cb7aa-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>      |
| <span data-ttu-id="cb7aa-125">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="cb7aa-125">Minimum supported server</span></span><br/> | <span data-ttu-id="cb7aa-126">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="cb7aa-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>            |
| <span data-ttu-id="cb7aa-127">Имя в кодировке Юникод и ANSI</span><span class="sxs-lookup"><span data-stu-id="cb7aa-127">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="cb7aa-128">**Мрукмппрокв** (Юникод) и **мрукмппрока** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="cb7aa-128">**MRUCMPPROCW** (Unicode) and **MRUCMPPROCA** (ANSI)</span></span><br/> |



 

 




