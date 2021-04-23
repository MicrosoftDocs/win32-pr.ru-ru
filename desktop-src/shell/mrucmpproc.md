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
ms.openlocfilehash: f95856f6508ad728a15b3df3d6f5eafa4f5bd2ff
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103991311"
---
# <a name="mrucmpproc-callback-function"></a><span data-ttu-id="03e86-103">Функция обратного вызова МРУКМППРОК</span><span class="sxs-lookup"><span data-stu-id="03e86-103">MRUCMPPROC callback function</span></span>

<span data-ttu-id="03e86-104">Используется для определения наличия элемента в списке последних использованных элементов.</span><span class="sxs-lookup"><span data-stu-id="03e86-104">Used to determine whether an item is present in a most recently used (MRU) list.</span></span>

## <a name="syntax"></a><span data-ttu-id="03e86-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="03e86-105">Syntax</span></span>


```C++
int CALLBACK MRUCMPPROC(
   LPCTSTR pString1,
   LPCTSTR pString2
);
```



## <a name="parameters"></a><span data-ttu-id="03e86-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="03e86-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="03e86-107">*pString1*</span><span class="sxs-lookup"><span data-stu-id="03e86-107">*pString1*</span></span> 
</dt> <dd>

<span data-ttu-id="03e86-108">Тип: **LPCTSTR**</span><span class="sxs-lookup"><span data-stu-id="03e86-108">Type: **LPCTSTR**</span></span>

<span data-ttu-id="03e86-109">Первая строка.</span><span class="sxs-lookup"><span data-stu-id="03e86-109">The first string.</span></span>

</dd> <dt>

<span data-ttu-id="03e86-110">*pString2*</span><span class="sxs-lookup"><span data-stu-id="03e86-110">*pString2*</span></span> 
</dt> <dd>

<span data-ttu-id="03e86-111">Тип: **LPCTSTR**</span><span class="sxs-lookup"><span data-stu-id="03e86-111">Type: **LPCTSTR**</span></span>

<span data-ttu-id="03e86-112">Вторая строка для сравнения с первой.</span><span class="sxs-lookup"><span data-stu-id="03e86-112">A second string to compare to the first.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="03e86-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="03e86-113">Return value</span></span>

<span data-ttu-id="03e86-114">Тип: **int**</span><span class="sxs-lookup"><span data-stu-id="03e86-114">Type: **int**</span></span>

<span data-ttu-id="03e86-115">Возвращает 0, если элементы идентичны, в противном случае — ненулевое значение.</span><span class="sxs-lookup"><span data-stu-id="03e86-115">Returns 0 if the items are identical, a nonzero value otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="03e86-116">Примечания</span><span class="sxs-lookup"><span data-stu-id="03e86-116">Remarks</span></span>

<span data-ttu-id="03e86-117">Эту функцию можно дополнительно указать для использования в структуре [**мруинфо**](mruinfo.md) , передаваемой в [**креатемрулиств**](createmrulist.md).</span><span class="sxs-lookup"><span data-stu-id="03e86-117">This function can be optionally specified for use in the [**MRUINFO**](mruinfo.md) structure passed to [**CreateMRUListW**](createmrulist.md).</span></span> <span data-ttu-id="03e86-118">Это полезно, если список MRU был создан с помощью флага **\_ двоичного файла MRU** .</span><span class="sxs-lookup"><span data-stu-id="03e86-118">This is useful when the MRU list was created with the **MRU\_BINARY** flag.</span></span> <span data-ttu-id="03e86-119">Если эта функция не задана, используются стандартные функции сравнения строк.</span><span class="sxs-lookup"><span data-stu-id="03e86-119">When this function is not specified, standard string comparison functions are used.</span></span>

## <a name="requirements"></a><span data-ttu-id="03e86-120">Требования</span><span class="sxs-lookup"><span data-stu-id="03e86-120">Requirements</span></span>



| <span data-ttu-id="03e86-121">Требование</span><span class="sxs-lookup"><span data-stu-id="03e86-121">Requirement</span></span> | <span data-ttu-id="03e86-122">Значение</span><span class="sxs-lookup"><span data-stu-id="03e86-122">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------|
| <span data-ttu-id="03e86-123">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="03e86-123">Minimum supported client</span></span><br/> | <span data-ttu-id="03e86-124">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="03e86-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>      |
| <span data-ttu-id="03e86-125">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="03e86-125">Minimum supported server</span></span><br/> | <span data-ttu-id="03e86-126">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="03e86-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>            |
| <span data-ttu-id="03e86-127">Имя в кодировке Юникод и ANSI</span><span class="sxs-lookup"><span data-stu-id="03e86-127">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="03e86-128">**Мрукмппрокв** (Юникод) и **мрукмппрока** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="03e86-128">**MRUCMPPROCW** (Unicode) and **MRUCMPPROCA** (ANSI)</span></span><br/> |



 

 




