---
description: Перечисляет содержимое списка недавно использовавшихся (MRU) списков. При необходимости извлекает элемент из перечисления.
title: Функция Енуммрулиств
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EnumMRUListW
- EnumMRUListW
api_type:
- DllExport
api_location:
- Comctl32.dll
ms.assetid: 630e5f27-96bf-4e88-b01a-127b301cc051
ms.openlocfilehash: 6b6e9588588e44a2c3b40f6ac012b11f21c875e3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103912367"
---
# <a name="enummrulistw-function"></a><span data-ttu-id="a3470-104">Функция Енуммрулиств</span><span class="sxs-lookup"><span data-stu-id="a3470-104">EnumMRUListW function</span></span>

<span data-ttu-id="a3470-105">\[Эта функция доступна в Windows XP с пакетом обновления 2 (SP2) и Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="a3470-105">\[This function is available through Windows XP with Service Pack 2 (SP2) and Windows Server 2003.</span></span> <span data-ttu-id="a3470-106">Он может быть изменен или недоступен в последующих версиях Windows.</span><span class="sxs-lookup"><span data-stu-id="a3470-106">It might be altered or unavailable in subsequent versions of Windows.</span></span> <span data-ttu-id="a3470-107">\]</span><span class="sxs-lookup"><span data-stu-id="a3470-107">\]</span></span>

<span data-ttu-id="a3470-108">Перечисляет содержимое списка недавно использовавшихся (MRU) списков.</span><span class="sxs-lookup"><span data-stu-id="a3470-108">Enumerates the contents of the most recently used (MRU) list.</span></span> <span data-ttu-id="a3470-109">При необходимости извлекает элемент из перечисления.</span><span class="sxs-lookup"><span data-stu-id="a3470-109">Optionally retrieves an item from the enumeration.</span></span>

## <a name="syntax"></a><span data-ttu-id="a3470-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="a3470-110">Syntax</span></span>


```C++
int EnumMRUListW(
  _In_  HANDLE hMRU,
  _In_  int    nItem,
  _Out_ void   *lpData,
  _In_  UINT   uLen
);
```



## <a name="parameters"></a><span data-ttu-id="a3470-111">Параметры</span><span class="sxs-lookup"><span data-stu-id="a3470-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a3470-112">*хмру* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="a3470-112">*hMRU* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a3470-113">Тип: **Handle**</span><span class="sxs-lookup"><span data-stu-id="a3470-113">Type: **HANDLE**</span></span>

<span data-ttu-id="a3470-114">Маркер списка MRU, полученный при создании списка.</span><span class="sxs-lookup"><span data-stu-id="a3470-114">The handle of the MRU list, obtained when the list was created.</span></span>

</dd> <dt>

<span data-ttu-id="a3470-115">*нитем* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="a3470-115">*nItem* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a3470-116">Тип: **int**</span><span class="sxs-lookup"><span data-stu-id="a3470-116">Type: **int**</span></span>

<span data-ttu-id="a3470-117">Возвращаемый элемент.</span><span class="sxs-lookup"><span data-stu-id="a3470-117">The item to return.</span></span> <span data-ttu-id="a3470-118">Если это значение меньше 0, функция возвращает количество элементов в списке MRU.</span><span class="sxs-lookup"><span data-stu-id="a3470-118">If this value is less than 0, the function returns the number of items in the MRU list.</span></span>

</dd> <dt>

<span data-ttu-id="a3470-119">*лпдата* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="a3470-119">*lpData* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a3470-120">Тип: \**void \** _</span><span class="sxs-lookup"><span data-stu-id="a3470-120">Type: \**void\** _</span></span>

<span data-ttu-id="a3470-121">Указатель на буфер, который получает элемент, запрошенный в _nItem \*.</span><span class="sxs-lookup"><span data-stu-id="a3470-121">A pointer to a buffer that receives the item requested in _nItem\*.</span></span> <span data-ttu-id="a3470-122">Если *нитем* меньше 0, содержимое этого буфера не изменяется.</span><span class="sxs-lookup"><span data-stu-id="a3470-122">If *nItem* is less than 0, the contents of this buffer are unchanged.</span></span>

</dd> <dt>

<span data-ttu-id="a3470-123">*Улен* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="a3470-123">*uLen* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a3470-124">Тип: **uint**</span><span class="sxs-lookup"><span data-stu-id="a3470-124">Type: **UINT**</span></span>

<span data-ttu-id="a3470-125">Размер буфера, включая завершающий нуль символ.</span><span class="sxs-lookup"><span data-stu-id="a3470-125">The size of the buffer, including the terminating null character.</span></span> <span data-ttu-id="a3470-126">Если список MRU был создан с флагом **\_ двоичный файл MRU** , это размер в байтах.</span><span class="sxs-lookup"><span data-stu-id="a3470-126">If the MRU list was created with the **MRU\_BINARY** flag, this is the size in bytes.</span></span> <span data-ttu-id="a3470-127">В противном случае это размер в символах.</span><span class="sxs-lookup"><span data-stu-id="a3470-127">Otherwise, it is the size in characters.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a3470-128">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="a3470-128">Return value</span></span>

<span data-ttu-id="a3470-129">Тип: **int**</span><span class="sxs-lookup"><span data-stu-id="a3470-129">Type: **int**</span></span>

<span data-ttu-id="a3470-130">Возвращает одно из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="a3470-130">Returns one of the following values.</span></span>

-   <span data-ttu-id="a3470-131">Возвращает количество элементов в перечислении, если *нитем* меньше 0.</span><span class="sxs-lookup"><span data-stu-id="a3470-131">Returns the number of items in the enumeration, if *nItem* is less than 0.</span></span>
-   <span data-ttu-id="a3470-132">Возвращает значение-1, если произошла ошибка.</span><span class="sxs-lookup"><span data-stu-id="a3470-132">Returns -1 if an error occurred.</span></span>
-   <span data-ttu-id="a3470-133">В противном случае возвращает размер строки, возвращаемой в *лпдата*, включая завершающий символ null.</span><span class="sxs-lookup"><span data-stu-id="a3470-133">Otherwise, returns the size of the string returned in *lpData*, including the terminating null character.</span></span> <span data-ttu-id="a3470-134">Если список MRU был создан с флагом **\_ двоичный файл MRU** , это размер в байтах.</span><span class="sxs-lookup"><span data-stu-id="a3470-134">If the MRU list was created with the **MRU\_BINARY** flag, this is the size in bytes.</span></span> <span data-ttu-id="a3470-135">В противном случае это размер в символах.</span><span class="sxs-lookup"><span data-stu-id="a3470-135">Otherwise, it is the size in characters.</span></span>

## <a name="remarks"></a><span data-ttu-id="a3470-136">Примечания</span><span class="sxs-lookup"><span data-stu-id="a3470-136">Remarks</span></span>

<span data-ttu-id="a3470-137">Эта функция не включена в общедоступный заголовок или библиотеку.</span><span class="sxs-lookup"><span data-stu-id="a3470-137">This function is not included in a public header or library.</span></span> <span data-ttu-id="a3470-138">Доступ к нему можно получить с помощью [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) или извлечь из comctl32.dll по порядковому номеру, 403 для **енуммрулиств**.</span><span class="sxs-lookup"><span data-stu-id="a3470-138">It can be accessed through [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) or extracted from comctl32.dll by its ordinal, which is 403 for **EnumMRUListW**.</span></span>

## <a name="requirements"></a><span data-ttu-id="a3470-139">Требования</span><span class="sxs-lookup"><span data-stu-id="a3470-139">Requirements</span></span>



| <span data-ttu-id="a3470-140">Требование</span><span class="sxs-lookup"><span data-stu-id="a3470-140">Requirement</span></span> | <span data-ttu-id="a3470-141">Значение</span><span class="sxs-lookup"><span data-stu-id="a3470-141">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a3470-142">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="a3470-142">Minimum supported client</span></span><br/> | <span data-ttu-id="a3470-143">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="a3470-143">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="a3470-144">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="a3470-144">Minimum supported server</span></span><br/> | <span data-ttu-id="a3470-145">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="a3470-145">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="a3470-146">DLL</span><span class="sxs-lookup"><span data-stu-id="a3470-146">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a3470-147"><dt>Comctl32.dll (версия 5,0 или более поздняя)</dt></span><span class="sxs-lookup"><span data-stu-id="a3470-147"><dt>Comctl32.dll (version 5.0 or later)</dt></span></span> </dl> |
| <span data-ttu-id="a3470-148">Имя в кодировке Юникод и ANSI</span><span class="sxs-lookup"><span data-stu-id="a3470-148">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="a3470-149">**Енуммрулиств** (Юникод)</span><span class="sxs-lookup"><span data-stu-id="a3470-149">**EnumMRUListW** (Unicode)</span></span><br/>                                                                          |



## <a name="see-also"></a><span data-ttu-id="a3470-150">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="a3470-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a3470-151">**креатемрулиств**</span><span class="sxs-lookup"><span data-stu-id="a3470-151">**CreateMRUListW**</span></span>](createmrulist.md)
</dt> <dt>

[<span data-ttu-id="a3470-152">**мруинфо**</span><span class="sxs-lookup"><span data-stu-id="a3470-152">**MRUINFO**</span></span>](mruinfo.md)
</dt> </dl>

 

 
