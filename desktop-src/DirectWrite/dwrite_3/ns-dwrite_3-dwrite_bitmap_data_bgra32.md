---
UID: NS:dwrite_3.DWRITE_BITMAP_DATA_BGRA32
title: DWRITE_BITMAP_DATA_BGRA32 (dwrite_3.h)
description: Представляет данные точечного рисунка в формате BGRA32.
tech.root: DirectWrite
ms.date: 11/11/2020
ms.topic: reference
req.header: dwrite_3.h
req.include-header: dwrite_core.h
req.target-type: Windows
req.target-min-winverclnt: ''
req.target-min-winversvr: ''
req.kmdf-ver: ''
req.umdf-ver: ''
req.ddi-compliance: ''
req.unicode-ansi: ''
req.idl: ''
req.max-support: ''
req.namespace: ''
req.assembly: ''
req.type-library: ''
req.lib: ''
req.dll: ''
req.irql: ''
targetos: Windows
req.typenames: ''
req.redist: ''
f1_keywords:
- DWRITE_BITMAP_DATA_BGRA32
- dwrite_3/DWRITE_BITMAP_DATA_BGRA32
dev_langs:
- c++
topic_type:
- APIRef
- kbSyntax
api_type:
- HeaderDef
api_location:
- dwrite_3.h
api_name:
- DWRITE_BITMAP_DATA_BGRA32
ms.openlocfilehash: 813f3601cac03dcf477fa40f6db5105e075029ab
ms.sourcegitcommit: f848119a8faa29b27585f4df53f6e50ee9666684
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/27/2021
ms.locfileid: "110548929"
---
# <a name="dwrite_bitmap_data_bgra32-structure-dwrite_3h"></a><span data-ttu-id="30d6a-103">Структура DWRITE_BITMAP_DATA_BGRA32 (dwrite_3. h)</span><span class="sxs-lookup"><span data-stu-id="30d6a-103">DWRITE_BITMAP_DATA_BGRA32 structure (dwrite_3.h)</span></span>

<span data-ttu-id="30d6a-104">Представляет данные точечного рисунка в формате BGRA32.</span><span class="sxs-lookup"><span data-stu-id="30d6a-104">Represents bitmap data in BGRA32 format.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="30d6a-105">Этот API доступен как часть реализации Двритекоре класса [DirectWrite](../direct-write-portal.md).</span><span class="sxs-lookup"><span data-stu-id="30d6a-105">This API is available as part of the DWriteCore implementation of [DirectWrite](../direct-write-portal.md).</span></span> <span data-ttu-id="30d6a-106">DWriteCore — это один из видов DirectWrite, который работает с версиями Windows вплоть до Windows 8 и позволяет использовать его на разных платформах.</span><span class="sxs-lookup"><span data-stu-id="30d6a-106">DWriteCore is a form of DirectWrite that runs on versions of Windows down to Windows 8, and opens the door for you to use it cross-platform.</span></span> <span data-ttu-id="30d6a-107">Дополнительные сведения и примеры кода см. в разделе [двритекоре Overview](../dwritecore-overview.md).</span><span class="sxs-lookup"><span data-stu-id="30d6a-107">For more info, and code examples, see [DWriteCore overview](../dwritecore-overview.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="30d6a-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="30d6a-108">Syntax</span></span>

```cpp
struct DWRITE_BITMAP_DATA_BGRA32
{
  UINT32 width;
  UINT32 height;
  _Field_size_(width * height) UINT32* pixels;
};
```

## <a name="members"></a><span data-ttu-id="30d6a-109">Участники</span><span class="sxs-lookup"><span data-stu-id="30d6a-109">Members</span></span>

`width`

<span data-ttu-id="30d6a-110">Тип: **[UINT32](../../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="30d6a-110">Type: **[UINT32](../../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="30d6a-111">Ширина точечного рисунка в пикселях.</span><span class="sxs-lookup"><span data-stu-id="30d6a-111">The width, in pixels, of the bitmap.</span></span>


`height`

<span data-ttu-id="30d6a-112">Тип: **[UINT32](../../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="30d6a-112">Type: **[UINT32](../../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="30d6a-113">Высота точечного рисунка (в пикселях).</span><span class="sxs-lookup"><span data-stu-id="30d6a-113">The height, in pixels, of the bitmap.</span></span>


`pixels`

<span data-ttu-id="30d6a-114">Тип: \_ \_ Размер поля \_ (ширина \* высота)**[UINT32](../../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="30d6a-114">Type: \_Field\_size\_(width \* height)**[UINT32](../../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="30d6a-115">Указатель на расположение битовых значений для точечного рисунка.</span><span class="sxs-lookup"><span data-stu-id="30d6a-115">A pointer to the location of the bit values for the bitmap.</span></span>


## <a name="examples"></a><span data-ttu-id="30d6a-116">Примеры</span><span class="sxs-lookup"><span data-stu-id="30d6a-116">Examples</span></span>

<span data-ttu-id="30d6a-117">См. раздел [Обзор двритекоре](../dwritecore-overview.md) и пример приложения [двритекорегаллери](https://github.com/microsoft/Project-Reunion-Samples/tree/main/DWriteCore/DWriteCoreGallery) .</span><span class="sxs-lookup"><span data-stu-id="30d6a-117">See the [DWriteCore overview](../dwritecore-overview.md) topic, and the [DWriteCoreGallery](https://github.com/microsoft/Project-Reunion-Samples/tree/main/DWriteCore/DWriteCoreGallery) sample app.</span></span>

## <a name="requirements"></a><span data-ttu-id="30d6a-118">Требования</span><span class="sxs-lookup"><span data-stu-id="30d6a-118">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="30d6a-119">**Минимальная версия клиента**</span><span class="sxs-lookup"><span data-stu-id="30d6a-119">**Minimum supported client**</span></span> | <span data-ttu-id="30d6a-120">Windows 10, переобъединение проектов [приложения Win32]</span><span class="sxs-lookup"><span data-stu-id="30d6a-120">Windows 10, Project Reunion [Win32 apps]</span></span> |
| <span data-ttu-id="30d6a-121">**Header**</span><span class="sxs-lookup"><span data-stu-id="30d6a-121">**Header**</span></span> | <span data-ttu-id="30d6a-122">dwrite_3. h (включает dwrite_core. h)</span><span class="sxs-lookup"><span data-stu-id="30d6a-122">dwrite_3.h (include dwrite_core.h)</span></span> |