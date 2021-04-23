---
description: Добавляет строку в верхнюю часть списка недавно использовавшихся (MRU).
title: Функция Аддмрустрингв
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AddMRUStringW
- AddMRUStringW
api_type:
- DllExport
api_location:
- Comctl32.dll
ms.assetid: ad94a442-8492-412c-a4f2-ac6e7c5327d7
ms.openlocfilehash: 0d0d65187105f4ad844b349c6ac60b030c464716
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104072634"
---
# <a name="addmrustringw-function"></a><span data-ttu-id="b34fe-103">Функция Аддмрустрингв</span><span class="sxs-lookup"><span data-stu-id="b34fe-103">AddMRUStringW function</span></span>

<span data-ttu-id="b34fe-104">\[Эта функция доступна в Windows XP с пакетом обновления 2 (SP2) и Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="b34fe-104">\[This function is available through Windows XP with Service Pack 2 (SP2) and Windows Server 2003.</span></span> <span data-ttu-id="b34fe-105">Он может быть изменен или недоступен в последующих версиях Windows.</span><span class="sxs-lookup"><span data-stu-id="b34fe-105">It might be altered or unavailable in subsequent versions of Windows.</span></span> <span data-ttu-id="b34fe-106">\]</span><span class="sxs-lookup"><span data-stu-id="b34fe-106">\]</span></span>

<span data-ttu-id="b34fe-107">Добавляет строку в верхнюю часть списка недавно использовавшихся (MRU).</span><span class="sxs-lookup"><span data-stu-id="b34fe-107">Adds a string to the top of the most recently used (MRU) list.</span></span>

## <a name="syntax"></a><span data-ttu-id="b34fe-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="b34fe-108">Syntax</span></span>


```C++
int AddMRUStringW(
  _In_ HANDLE  hMRU,
  _In_ LPCTSTR szString
);
```



## <a name="parameters"></a><span data-ttu-id="b34fe-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="b34fe-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b34fe-110">*хмру* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="b34fe-110">*hMRU* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b34fe-111">Тип: **Handle**</span><span class="sxs-lookup"><span data-stu-id="b34fe-111">Type: **HANDLE**</span></span>

<span data-ttu-id="b34fe-112">Маркер списка MRU.</span><span class="sxs-lookup"><span data-stu-id="b34fe-112">The handle of the MRU list.</span></span>

</dd> <dt>

<span data-ttu-id="b34fe-113">*сзстринг* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="b34fe-113">*szString* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b34fe-114">Тип: **LPCTSTR**</span><span class="sxs-lookup"><span data-stu-id="b34fe-114">Type: **LPCTSTR**</span></span>

<span data-ttu-id="b34fe-115">Указатель на данные.</span><span class="sxs-lookup"><span data-stu-id="b34fe-115">A pointer to the data.</span></span> <span data-ttu-id="b34fe-116">Это может быть либо строка, либо, если список MRU был создан с помощью **\_ двоичного** флага MRU, двоичных данных.</span><span class="sxs-lookup"><span data-stu-id="b34fe-116">This can be either a string or, if the MRU list was created with the **MRU\_BINARY** flag, binary data.</span></span> <span data-ttu-id="b34fe-117">В случае двоичных данных первый **DWORD** указывает на его размер.</span><span class="sxs-lookup"><span data-stu-id="b34fe-117">In the case of binary data, the first **DWORD** indicates its size.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b34fe-118">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="b34fe-118">Return value</span></span>

<span data-ttu-id="b34fe-119">Тип: **int**</span><span class="sxs-lookup"><span data-stu-id="b34fe-119">Type: **int**</span></span>

<span data-ttu-id="b34fe-120">При успешном выполнении возвращает неотрицательное значение – 1 в противном случае.</span><span class="sxs-lookup"><span data-stu-id="b34fe-120">Returns a non-negative value if successful, -1 otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="b34fe-121">Примечания</span><span class="sxs-lookup"><span data-stu-id="b34fe-121">Remarks</span></span>

<span data-ttu-id="b34fe-122">Эта функция не включена в общедоступный заголовок или библиотеку.</span><span class="sxs-lookup"><span data-stu-id="b34fe-122">This function is not included in a public header or library.</span></span> <span data-ttu-id="b34fe-123">Доступ к нему можно получить с помощью [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) или извлечь из comctl32.dll по порядковому номеру, 401 для **аддмрустрингв**.</span><span class="sxs-lookup"><span data-stu-id="b34fe-123">It can be accessed through [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) or extracted from comctl32.dll by its ordinal, which is 401 for **AddMRUStringW**.</span></span>

## <a name="requirements"></a><span data-ttu-id="b34fe-124">Требования</span><span class="sxs-lookup"><span data-stu-id="b34fe-124">Requirements</span></span>



| <span data-ttu-id="b34fe-125">Требование</span><span class="sxs-lookup"><span data-stu-id="b34fe-125">Requirement</span></span> | <span data-ttu-id="b34fe-126">Значение</span><span class="sxs-lookup"><span data-stu-id="b34fe-126">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b34fe-127">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="b34fe-127">Minimum supported client</span></span><br/> | <span data-ttu-id="b34fe-128">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="b34fe-128">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="b34fe-129">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="b34fe-129">Minimum supported server</span></span><br/> | <span data-ttu-id="b34fe-130">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="b34fe-130">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="b34fe-131">DLL</span><span class="sxs-lookup"><span data-stu-id="b34fe-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b34fe-132"><dt>Comctl32.dll (версия 5,0 или более поздняя)</dt></span><span class="sxs-lookup"><span data-stu-id="b34fe-132"><dt>Comctl32.dll (version 5.0 or later)</dt></span></span> </dl> |
| <span data-ttu-id="b34fe-133">Имя в кодировке Юникод и ANSI</span><span class="sxs-lookup"><span data-stu-id="b34fe-133">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="b34fe-134">**Аддмрустрингв** (Юникод)</span><span class="sxs-lookup"><span data-stu-id="b34fe-134">**AddMRUStringW** (Unicode)</span></span><br/>                                                                         |



 

