---
description: Очищает кэш базы данных оболочки совместимости. Эту функцию следует вызывать после установки новой базы данных оболочек совместимости.
ms.assetid: 7e5bbdca-7b58-4c51-9cd1-105b05ee7fbe
title: Функция Шимфлушкаче
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ShimFlushCache
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: 35e279c5036142ec87c5bad6d7c512388033bc94
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104072338"
---
# <a name="shimflushcache-function"></a><span data-ttu-id="6abb1-104">Функция Шимфлушкаче</span><span class="sxs-lookup"><span data-stu-id="6abb1-104">ShimFlushCache function</span></span>

<span data-ttu-id="6abb1-105">Очищает кэш базы данных оболочки совместимости.</span><span class="sxs-lookup"><span data-stu-id="6abb1-105">Flushes the shim database cache.</span></span> <span data-ttu-id="6abb1-106">Эту функцию следует вызывать после установки новой базы данных оболочек совместимости.</span><span class="sxs-lookup"><span data-stu-id="6abb1-106">This function should be called after installing a new shim database.</span></span>

## <a name="syntax"></a><span data-ttu-id="6abb1-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="6abb1-107">Syntax</span></span>


```C++
BOOL WINAPI ShimFlushCache(
  _In_opt_ HWND      hwnd,
  _In_opt_ HINSTANCE hInstance,
  _In_opt_ LPCSTR    lpszCmdLine,
  _In_     int       nCmdShow
);
```



## <a name="parameters"></a><span data-ttu-id="6abb1-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="6abb1-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6abb1-109">*HWND* \[ в необязательное\]</span><span class="sxs-lookup"><span data-stu-id="6abb1-109">*hwnd* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="6abb1-110">Использующ значение должно быть равно 0.</span><span class="sxs-lookup"><span data-stu-id="6abb1-110">Unused; must be 0.</span></span>

</dd> <dt>

<span data-ttu-id="6abb1-111">*HINSTANCE* \[ в необязательное\]</span><span class="sxs-lookup"><span data-stu-id="6abb1-111">*hInstance* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="6abb1-112">Использующ значение должно быть равно 0.</span><span class="sxs-lookup"><span data-stu-id="6abb1-112">Unused; must be 0.</span></span>

</dd> <dt>

<span data-ttu-id="6abb1-113">*лпсзкмдлине* \[ в необязательное\]</span><span class="sxs-lookup"><span data-stu-id="6abb1-113">*lpszCmdLine* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="6abb1-114">Использующ значение должно быть равно 0.</span><span class="sxs-lookup"><span data-stu-id="6abb1-114">Unused; must be 0.</span></span>

</dd> <dt>

<span data-ttu-id="6abb1-115">*нкмдшов* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="6abb1-115">*nCmdShow* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6abb1-116">Использующ значение должно быть равно 0.</span><span class="sxs-lookup"><span data-stu-id="6abb1-116">Unused; must be 0.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6abb1-117">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="6abb1-117">Return value</span></span>

<span data-ttu-id="6abb1-118">Функция возвращает **true** при успешном выполнении или **false** в случае сбоя.</span><span class="sxs-lookup"><span data-stu-id="6abb1-118">The function returns **TRUE** on success or **FALSE** on failure.</span></span>

## <a name="remarks"></a><span data-ttu-id="6abb1-119">Комментарии</span><span class="sxs-lookup"><span data-stu-id="6abb1-119">Remarks</span></span>

<span data-ttu-id="6abb1-120">Вызывающий объект должен быть администратором.</span><span class="sxs-lookup"><span data-stu-id="6abb1-120">The caller must be an administrator.</span></span>

## <a name="requirements"></a><span data-ttu-id="6abb1-121">Требования</span><span class="sxs-lookup"><span data-stu-id="6abb1-121">Requirements</span></span>



| <span data-ttu-id="6abb1-122">Требование</span><span class="sxs-lookup"><span data-stu-id="6abb1-122">Requirement</span></span> | <span data-ttu-id="6abb1-123">Значение</span><span class="sxs-lookup"><span data-stu-id="6abb1-123">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="6abb1-124">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="6abb1-124">Minimum supported client</span></span><br/> | <span data-ttu-id="6abb1-125">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="6abb1-125">Windows Vista \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="6abb1-126">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="6abb1-126">Minimum supported server</span></span><br/> | <span data-ttu-id="6abb1-127">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="6abb1-127">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="6abb1-128">DLL</span><span class="sxs-lookup"><span data-stu-id="6abb1-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6abb1-129"><dt>Apphelp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6abb1-129"><dt>Apphelp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6abb1-130">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="6abb1-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6abb1-131">**басефлушаппкомпаткаче**</span><span class="sxs-lookup"><span data-stu-id="6abb1-131">**BaseFlushAppcompatCache**</span></span>](baseflushappcompatcache.md)
</dt> </dl>

 

 




