---
description: Содержит сведения, определяющие новый список недавно использованных (MRU) списков. Используется Креатемрулиств.
title: Структура МРУИНФО
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- _MRUINFO
- MRUINFOA
- MRUINFOW
api_type:
- NA
api_location: ''
ms.assetid: 31d5831d-9a19-4bd9-8439-ce844966c414
ms.openlocfilehash: 652168e6a4e61ac754aac3202e0681ec6b7d9e66
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/12/2021
ms.locfileid: "109840765"
---
# <a name="mruinfo-structure"></a><span data-ttu-id="f82e7-104">Структура МРУИНФО</span><span class="sxs-lookup"><span data-stu-id="f82e7-104">MRUINFO structure</span></span>

<span data-ttu-id="f82e7-105">Содержит сведения, определяющие новый список недавно использованных (MRU) списков.</span><span class="sxs-lookup"><span data-stu-id="f82e7-105">Contains information that defines a new most recently used (MRU) list.</span></span> <span data-ttu-id="f82e7-106">Используется [**креатемрулиств**](createmrulist.md).</span><span class="sxs-lookup"><span data-stu-id="f82e7-106">Used by [**CreateMRUListW**](createmrulist.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="f82e7-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="f82e7-107">Syntax</span></span>


```C++
typedef struct {
  DWORD      cbSize;
  UINT       uMax;
  UINT       fFlags;
  HKEY       hKey;
  LPCTSTR    lpszSubKey;
  MRUCMPPROC lpfnCompare;
} _MRUINFO;
```



## <a name="members"></a><span data-ttu-id="f82e7-108">Члены</span><span class="sxs-lookup"><span data-stu-id="f82e7-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="f82e7-109">**кбсизе**</span><span class="sxs-lookup"><span data-stu-id="f82e7-109">**cbSize**</span></span>
</dt> <dd>

<span data-ttu-id="f82e7-110">Тип: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="f82e7-110">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="f82e7-111">Размер структуры.</span><span class="sxs-lookup"><span data-stu-id="f82e7-111">The size of the structure.</span></span>

</dd> <dt>

<span data-ttu-id="f82e7-112">**Компания**</span><span class="sxs-lookup"><span data-stu-id="f82e7-112">**uMax**</span></span>
</dt> <dd>

<span data-ttu-id="f82e7-113">Тип: **uint**</span><span class="sxs-lookup"><span data-stu-id="f82e7-113">Type: **UINT**</span></span>

</dd> <dd>

<span data-ttu-id="f82e7-114">Максимальное число записей в списке MRU.</span><span class="sxs-lookup"><span data-stu-id="f82e7-114">The maximum number of entries in the MRU list.</span></span>

</dd> <dt>

<span data-ttu-id="f82e7-115">**ффлагс**</span><span class="sxs-lookup"><span data-stu-id="f82e7-115">**fFlags**</span></span>
</dt> <dd>

<span data-ttu-id="f82e7-116">Тип: **uint**</span><span class="sxs-lookup"><span data-stu-id="f82e7-116">Type: **UINT**</span></span>

</dd> <dd>

<span data-ttu-id="f82e7-117">Один или несколько следующих флагов.</span><span class="sxs-lookup"><span data-stu-id="f82e7-117">One or more of the following flags.</span></span>

<dt>

<span id="MRU_BINARY"></span><span id="mru_binary"></span>

<span data-ttu-id="f82e7-118"><span id="MRU_BINARY"></span><span id="mru_binary"></span>**MRU \_ ДВОИЧный** (0x0001)</span><span class="sxs-lookup"><span data-stu-id="f82e7-118"><span id="MRU_BINARY"></span><span id="mru_binary"></span>**MRU\_BINARY** (0x0001)</span></span>


</dt> <dd>

<span data-ttu-id="f82e7-119">Данные хранятся в реестре в виде двоичных данных, а не строковых данных.</span><span class="sxs-lookup"><span data-stu-id="f82e7-119">Data is stored in the registry as binary data rather than string data.</span></span>

</dd> <dt>

<span id="MRU_CACHEWRITE"></span><span id="mru_cachewrite"></span>

<span data-ttu-id="f82e7-120"><span id="MRU_CACHEWRITE"></span><span id="mru_cachewrite"></span>**MRU \_ КАЧЕВРИТЕ** (0x0002)</span><span class="sxs-lookup"><span data-stu-id="f82e7-120"><span id="MRU_CACHEWRITE"></span><span id="mru_cachewrite"></span>**MRU\_CACHEWRITE** (0x0002)</span></span>


</dt> <dd>

<span data-ttu-id="f82e7-121">Запись изменений в версию MRU, сохраненную в реестре, только при добавлении нового элемента или освобождении ресурсов списка MRU из памяти.</span><span class="sxs-lookup"><span data-stu-id="f82e7-121">Write changes to the version of the MRU stored in the registry only when a new item is added or the MRU list's resources are freed from memory.</span></span> <span data-ttu-id="f82e7-122">Обратите внимание, что активная версия MRU в памяти обновляется немедленно в ответ на любые изменения в содержании или упорядочении.</span><span class="sxs-lookup"><span data-stu-id="f82e7-122">Note that the active version of the MRU in memory is updated immediately in response to any change in contents or ordering.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="f82e7-123">**hKey**</span><span class="sxs-lookup"><span data-stu-id="f82e7-123">**hKey**</span></span>
</dt> <dd>

<span data-ttu-id="f82e7-124">Тип: **hKey**</span><span class="sxs-lookup"><span data-stu-id="f82e7-124">Type: **HKEY**</span></span>

</dd> <dd>

<span data-ttu-id="f82e7-125">Обработчик текущего открытого ключа или одно из следующих предопределенных значений, по которым сохраняются данные MRU.</span><span class="sxs-lookup"><span data-stu-id="f82e7-125">A handle to the currently open key, or one of the following predefined values under which to store the MRU data.</span></span>

<dl><span id="HKEY_CURRENT_USER"></span><span id="hkey_current_user"></span><dt>

<span data-ttu-id="f82e7-126">**HKEY \_ текущего \_ пользователя**</span><span class="sxs-lookup"><span data-stu-id="f82e7-126">**HKEY\_CURRENT\_USER**</span></span>
</dt><span id="HKEY_LOCAL_MACHINE"></span><span id="hkey_local_machine"></span><dt>

<span data-ttu-id="f82e7-127">**HKEY \_ локальный \_ компьютер**</span><span class="sxs-lookup"><span data-stu-id="f82e7-127">**HKEY\_LOCAL\_MACHINE**</span></span>
</dt> </dl> </dd> <dt>

<span data-ttu-id="f82e7-128">**лпсзсубкэй**</span><span class="sxs-lookup"><span data-stu-id="f82e7-128">**lpszSubKey**</span></span>
</dt> <dd>

<span data-ttu-id="f82e7-129">Тип: **LPCTSTR**</span><span class="sxs-lookup"><span data-stu-id="f82e7-129">Type: **LPCTSTR**</span></span>

</dd> <dd>

<span data-ttu-id="f82e7-130">Подраздел, в котором сохраняются данные MRU.</span><span class="sxs-lookup"><span data-stu-id="f82e7-130">The subkey under which to store the MRU data.</span></span>

</dd> <dt>

<span data-ttu-id="f82e7-131">**лпфнкомпаре**</span><span class="sxs-lookup"><span data-stu-id="f82e7-131">**lpfnCompare**</span></span>
</dt> <dd>

<span data-ttu-id="f82e7-132">Тип: **[ **мрукмппрок**](mrucmpproc.md)**</span><span class="sxs-lookup"><span data-stu-id="f82e7-132">Type: **[**MRUCMPPROC**](mrucmpproc.md)**</span></span>

</dd> <dd>

<span data-ttu-id="f82e7-133">Указатель на необязательную функцию сравнения данных, которую можно использовать для определения наличия элемента в списке MRU.</span><span class="sxs-lookup"><span data-stu-id="f82e7-133">A pointer to an optional data comparison function that can be used to determine whether an item is present in the MRU list.</span></span> <span data-ttu-id="f82e7-134">Это полезно, если список MRU был создан с помощью флага **\_ двоичного файла MRU** .</span><span class="sxs-lookup"><span data-stu-id="f82e7-134">This is useful when the MRU list was created with the **MRU\_BINARY** flag.</span></span> <span data-ttu-id="f82e7-135">Если этот член имеет **значение NULL**, используются стандартные функции сравнения строк. для двоичных данных используется прямое сравнение памяти.</span><span class="sxs-lookup"><span data-stu-id="f82e7-135">If this member is **NULL**, standard string comparison functions are used; for binary data, a direct memory comparison is used.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="f82e7-136">Remarks</span><span class="sxs-lookup"><span data-stu-id="f82e7-136">Remarks</span></span>

<span data-ttu-id="f82e7-137">Эта структура не определена в файле заголовка.</span><span class="sxs-lookup"><span data-stu-id="f82e7-137">This structure is not defined in a header file.</span></span> <span data-ttu-id="f82e7-138">Его необходимо определить самостоятельно.</span><span class="sxs-lookup"><span data-stu-id="f82e7-138">You must define it yourself.</span></span>

## <a name="requirements"></a><span data-ttu-id="f82e7-139">Requirements (Требования)</span><span class="sxs-lookup"><span data-stu-id="f82e7-139">Requirements</span></span>



| <span data-ttu-id="f82e7-140">Требование</span><span class="sxs-lookup"><span data-stu-id="f82e7-140">Requirement</span></span> | <span data-ttu-id="f82e7-141">Значение</span><span class="sxs-lookup"><span data-stu-id="f82e7-141">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="f82e7-142">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="f82e7-142">Minimum supported client</span></span><br/> | <span data-ttu-id="f82e7-143">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="f82e7-143">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="f82e7-144">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="f82e7-144">Minimum supported server</span></span><br/> | <span data-ttu-id="f82e7-145">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="f82e7-145">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="f82e7-146">Имя в кодировке Юникод и ANSI</span><span class="sxs-lookup"><span data-stu-id="f82e7-146">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="f82e7-147">**Мруинфов** (Юникод) и **мруинфоа** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="f82e7-147">**MRUINFOW** (Unicode) and **MRUINFOA** (ANSI)</span></span><br/>  |



 

 




