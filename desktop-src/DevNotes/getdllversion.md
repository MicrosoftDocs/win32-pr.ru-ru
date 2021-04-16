---
description: Функция Жетдллверсион получает номер версии Cabinet.dll.
ms.assetid: b324d5cd-1ede-473e-a10f-249c95eda057
title: Функция Жетдллверсион
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetDllVersion
api_type:
- DllExport
api_location:
- Cabinet.dll
ms.openlocfilehash: 1b1142bd2ece965a3f2fc58b6bb2f90586a8b391
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105657130"
---
# <a name="getdllversion-function"></a><span data-ttu-id="9bc63-103">Функция Жетдллверсион</span><span class="sxs-lookup"><span data-stu-id="9bc63-103">GetDllVersion function</span></span>

<span data-ttu-id="9bc63-104">\[Эта функция больше не поддерживается, поэтому ее поведение не гарантируется.</span><span class="sxs-lookup"><span data-stu-id="9bc63-104">\[This function is no longer supported, so its behavior cannot be guaranteed.</span></span> <span data-ttu-id="9bc63-105">\]</span><span class="sxs-lookup"><span data-stu-id="9bc63-105">\]</span></span>

<span data-ttu-id="9bc63-106">Функция **жетдллверсион** получает номер версии Cabinet.dll.</span><span class="sxs-lookup"><span data-stu-id="9bc63-106">The **GetDllVersion** function retrieves the version number of Cabinet.dll.</span></span>

## <a name="syntax"></a><span data-ttu-id="9bc63-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="9bc63-107">Syntax</span></span>


```C++
LPCSTR WINAPI GetDllVersion(void);
```



## <a name="parameters"></a><span data-ttu-id="9bc63-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="9bc63-108">Parameters</span></span>

<span data-ttu-id="9bc63-109">У этой функции нет параметров.</span><span class="sxs-lookup"><span data-stu-id="9bc63-109">This function has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="9bc63-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="9bc63-110">Return value</span></span>

<span data-ttu-id="9bc63-111">Номер версии файла (см. [ресурс versionInfo](../menurc/versioninfo-resource.md)).</span><span class="sxs-lookup"><span data-stu-id="9bc63-111">The version number of the file (see [VERSIONINFO Resource](../menurc/versioninfo-resource.md)).</span></span>

## <a name="remarks"></a><span data-ttu-id="9bc63-112">Комментарии</span><span class="sxs-lookup"><span data-stu-id="9bc63-112">Remarks</span></span>

<span data-ttu-id="9bc63-113">Эта функция не имеет связанной библиотеки импорта или файла заголовка. его необходимо вызвать с помощью функций [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) и [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .</span><span class="sxs-lookup"><span data-stu-id="9bc63-113">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="9bc63-114">Требования</span><span class="sxs-lookup"><span data-stu-id="9bc63-114">Requirements</span></span>



| <span data-ttu-id="9bc63-115">Требование</span><span class="sxs-lookup"><span data-stu-id="9bc63-115">Requirement</span></span> | <span data-ttu-id="9bc63-116">Значение</span><span class="sxs-lookup"><span data-stu-id="9bc63-116">Value</span></span> |
|----------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="9bc63-117">DLL</span><span class="sxs-lookup"><span data-stu-id="9bc63-117">DLL</span></span><br/> | <dl> <span data-ttu-id="9bc63-118"><dt>Cabinet.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9bc63-118"><dt>Cabinet.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9bc63-119">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="9bc63-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9bc63-120">**дллжетверсион**</span><span class="sxs-lookup"><span data-stu-id="9bc63-120">**DllGetVersion**</span></span>](dllgetversion.md)
</dt> </dl>

 

 
