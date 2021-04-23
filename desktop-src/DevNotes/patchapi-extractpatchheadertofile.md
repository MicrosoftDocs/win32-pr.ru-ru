---
description: Извлекает сведения о заголовке из разностной области.
title: Функция Екстрактпатчхеадертофилеа/W
ms.topic: reference
ms.date: 04/17/2020
ms.keywords: ExtractPatchHeaderToFileA, ExtractPatchHeaderToFileW
req.header: patchapi.h
req.dll: mspatchc.dll
topic_type:
- APIRef
- kbSyntax
api_name:
- ExtractPatchHeaderToFileW
api_type:
- DllExport
api_location:
- mspatchc.dll
ms.openlocfilehash: 40835a0b88558046ff9086ffcd7ec4609d1ed863
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105721029"
---
# <a name="extractpatchheadertofileaw-function"></a><span data-ttu-id="14a35-103">Функция Екстрактпатчхеадертофилеа/W</span><span class="sxs-lookup"><span data-stu-id="14a35-103">ExtractPatchHeaderToFileA/W function</span></span>

<span data-ttu-id="14a35-104">Функции **екстрактпатчхеадертофилеа** и **екстрактпатчхеадертофилев** извлекают данные заголовка из разностной области.</span><span class="sxs-lookup"><span data-stu-id="14a35-104">The **ExtractPatchHeaderToFileA** and **ExtractPatchHeaderToFileW** functions extract the header information from a delta.</span></span> <span data-ttu-id="14a35-105">Дельта предоставляется в виде пути к файлу.</span><span class="sxs-lookup"><span data-stu-id="14a35-105">The delta is provided as a file path.</span></span> <span data-ttu-id="14a35-106">Выходной заголовок также записывается в указанный путь.</span><span class="sxs-lookup"><span data-stu-id="14a35-106">The output header is also written to a provided path.</span></span>

## <a name="syntax"></a><span data-ttu-id="14a35-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="14a35-107">Syntax</span></span>

```cpp
BOOL  PATCHAPI  ExtractPatchHeaderToFileA(
    LPCTSTR  PatchFileName,
    LPCTSTR  PatchHeaderFileName
    );

BOOL  PATCHAPI  ExtractPatchHeaderToFileW(
    LPCWSTR  PatchFileName,
    LPCWSTR  PatchHeaderFileName
    );
```

## <a name="parameters"></a><span data-ttu-id="14a35-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="14a35-108">Parameters</span></span>

<span data-ttu-id="14a35-109">*патчфиленаме*</span><span class="sxs-lookup"><span data-stu-id="14a35-109">*PatchFileName*</span></span>

<span data-ttu-id="14a35-110">Имя разностного файла, содержащего заголовок.</span><span class="sxs-lookup"><span data-stu-id="14a35-110">The name of the delta containing the header.</span></span>

<span data-ttu-id="14a35-111">*патчхеадерфиленаме*</span><span class="sxs-lookup"><span data-stu-id="14a35-111">*PatchHeaderFileName*</span></span>

<span data-ttu-id="14a35-112">Имя создаваемого файла заголовка.</span><span class="sxs-lookup"><span data-stu-id="14a35-112">The name of the header file that is to be created.</span></span>

## <a name="return-value"></a><span data-ttu-id="14a35-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="14a35-113">Return value</span></span>

<span data-ttu-id="14a35-114">Эта функция возвращает **значение true** , если она выполнена. в противном случае возвращается **значение false**.</span><span class="sxs-lookup"><span data-stu-id="14a35-114">This function returns **TRUE** if it succeeds; otherwise, it returns **FALSE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="14a35-115">Требования</span><span class="sxs-lookup"><span data-stu-id="14a35-115">Requirements</span></span>

| <span data-ttu-id="14a35-116">Требование</span><span class="sxs-lookup"><span data-stu-id="14a35-116">Requirement</span></span> | <span data-ttu-id="14a35-117">Значение</span><span class="sxs-lookup"><span data-stu-id="14a35-117">Value</span></span> |
|----------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="14a35-118">Header</span><span class="sxs-lookup"><span data-stu-id="14a35-118">Header</span></span> | <span data-ttu-id="14a35-119">патчапи. h</span><span class="sxs-lookup"><span data-stu-id="14a35-119">patchapi.h</span></span> |
| <span data-ttu-id="14a35-120">DLL</span><span class="sxs-lookup"><span data-stu-id="14a35-120">DLL</span></span> | <span data-ttu-id="14a35-121">mspatchc.dll</span><span class="sxs-lookup"><span data-stu-id="14a35-121">mspatchc.dll</span></span> |
| <span data-ttu-id="14a35-122">Юникод</span><span class="sxs-lookup"><span data-stu-id="14a35-122">Unicode</span></span> | <span data-ttu-id="14a35-123">Реализовано как Екстрактпатчхеадертофилев (Юникод) и Екстрактпатчхеадертофилеа (ANSI)</span><span class="sxs-lookup"><span data-stu-id="14a35-123">Implemented as ExtractPatchHeaderToFileW (Unicode) and ExtractPatchHeaderToFileA (ANSI)</span></span> |

## <a name="see-also"></a><span data-ttu-id="14a35-124">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="14a35-124">See also</span></span>

[<span data-ttu-id="14a35-125">патчапи</span><span class="sxs-lookup"><span data-stu-id="14a35-125">PatchAPI</span></span>](patchapi.md)
