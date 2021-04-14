---
description: Функция ThunkConnect32 используется 16-разрядными драйверами устройств (для MS-DOS), которые вызывают 32-разрядный ядро.
ms.assetid: 3376ca67-04ea-4765-a2f4-15a84d5c84d4
title: Функция ThunkConnect32
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ThunkConnect32
api_type:
- DllExport
api_location:
- Kernel32.dll
ms.openlocfilehash: 7f22d7ceb59732e986c23c873133b11f358364cd
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105647965"
---
# <a name="thunkconnect32-function"></a><span data-ttu-id="b4549-103">Функция ThunkConnect32</span><span class="sxs-lookup"><span data-stu-id="b4549-103">ThunkConnect32 function</span></span>

<span data-ttu-id="b4549-104">\[Эта функция поддерживалась для обеспечения обратной совместимости, но отсутствует в текущих версиях Windows.</span><span class="sxs-lookup"><span data-stu-id="b4549-104">\[This function was supported for backward compatibility, but is not present in current versions of Windows.</span></span> <span data-ttu-id="b4549-105">Новые драйверы устройств должны быть 32 или 64-бит и не нуждаются в этой функции.\]</span><span class="sxs-lookup"><span data-stu-id="b4549-105">New device drivers should be 32- or 64-bit and do not need this function.\]</span></span>

<span data-ttu-id="b4549-106">Функция **ThunkConnect32** используется 16-разрядными драйверами устройств (для MS-DOS), которые вызывают 32-разрядный ядро.</span><span class="sxs-lookup"><span data-stu-id="b4549-106">The **ThunkConnect32** function is used by 16-bit device drivers (for MS-DOS) that call into the 32-bit kernel.</span></span>

## <a name="syntax"></a><span data-ttu-id="b4549-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="b4549-107">Syntax</span></span>


```C++
BOOL ThunkConnect32(
   LPVOID lpThunkData32,
   LPSTR  pszThunkData16Name,
   LPSTR  pszDll16,
   LPSTR  pszDll32,
   HANDLE hInstance,
   DWORD  dwReason
);
```



## <a name="parameters"></a><span data-ttu-id="b4549-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="b4549-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b4549-109">*lpThunkData32*</span><span class="sxs-lookup"><span data-stu-id="b4549-109">*lpThunkData32*</span></span> 
</dt> <dd>

<span data-ttu-id="b4549-110">Не обрабатывается.</span><span class="sxs-lookup"><span data-stu-id="b4549-110">Ignored.</span></span>

</dd> <dt>

<span data-ttu-id="b4549-111">*pszThunkData16Name*</span><span class="sxs-lookup"><span data-stu-id="b4549-111">*pszThunkData16Name*</span></span> 
</dt> <dd>

<span data-ttu-id="b4549-112">Не обрабатывается.</span><span class="sxs-lookup"><span data-stu-id="b4549-112">Ignored.</span></span>

</dd> <dt>

<span data-ttu-id="b4549-113">*pszDll16*</span><span class="sxs-lookup"><span data-stu-id="b4549-113">*pszDll16*</span></span> 
</dt> <dd>

<span data-ttu-id="b4549-114">Не обрабатывается.</span><span class="sxs-lookup"><span data-stu-id="b4549-114">Ignored.</span></span>

</dd> <dt>

<span data-ttu-id="b4549-115">*pszDll32*</span><span class="sxs-lookup"><span data-stu-id="b4549-115">*pszDll32*</span></span> 
</dt> <dd>

<span data-ttu-id="b4549-116">Не обрабатывается.</span><span class="sxs-lookup"><span data-stu-id="b4549-116">Ignored.</span></span>

</dd> <dt>

<span data-ttu-id="b4549-117">*hInstance*</span><span class="sxs-lookup"><span data-stu-id="b4549-117">*hInstance*</span></span> 
</dt> <dd>

<span data-ttu-id="b4549-118">Не обрабатывается.</span><span class="sxs-lookup"><span data-stu-id="b4549-118">Ignored.</span></span>

</dd> <dt>

<span data-ttu-id="b4549-119">*Параметр dwReason*</span><span class="sxs-lookup"><span data-stu-id="b4549-119">*dwReason*</span></span> 
</dt> <dd>

<span data-ttu-id="b4549-120">Не обрабатывается.</span><span class="sxs-lookup"><span data-stu-id="b4549-120">Ignored.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b4549-121">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="b4549-121">Return value</span></span>

<span data-ttu-id="b4549-122">Всегда возвращает **значение false**.</span><span class="sxs-lookup"><span data-stu-id="b4549-122">Always returns **FALSE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="b4549-123">Требования</span><span class="sxs-lookup"><span data-stu-id="b4549-123">Requirements</span></span>



| <span data-ttu-id="b4549-124">Требование</span><span class="sxs-lookup"><span data-stu-id="b4549-124">Requirement</span></span> | <span data-ttu-id="b4549-125">Значение</span><span class="sxs-lookup"><span data-stu-id="b4549-125">Value</span></span> |
|----------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b4549-126">DLL</span><span class="sxs-lookup"><span data-stu-id="b4549-126">DLL</span></span><br/> | <dl> <span data-ttu-id="b4549-127"><dt>Kernel32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b4549-127"><dt>Kernel32.dll</dt></span></span> </dl> |



 

 




