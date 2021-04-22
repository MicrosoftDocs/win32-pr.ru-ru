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
ms.openlocfilehash: 3d5b2168e5154f2e55b6f5acb83897f68d4a029c
ms.sourcegitcommit: d7e9a20168111fb608f5fefb092b30f8e093d816
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/22/2021
ms.locfileid: "107881833"
---
# <a name="dwrite_bitmap_data_bgra32-structure-dwrite_3h"></a><span data-ttu-id="79447-103">Структура DWRITE_BITMAP_DATA_BGRA32 (dwrite_3. h)</span><span class="sxs-lookup"><span data-stu-id="79447-103">DWRITE_BITMAP_DATA_BGRA32 structure (dwrite_3.h)</span></span>

<span data-ttu-id="79447-104">Представляет данные точечного рисунка в формате BGRA32.</span><span class="sxs-lookup"><span data-stu-id="79447-104">Represents bitmap data in BGRA32 format.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="79447-105">Этот API доступен как часть реализации Двритекоре класса [DirectWrite](../direct-write-portal.md).</span><span class="sxs-lookup"><span data-stu-id="79447-105">This API is available as part of the DWriteCore implementation of [DirectWrite](../direct-write-portal.md).</span></span> <span data-ttu-id="79447-106">DWriteCore — это один из видов DirectWrite, который работает с версиями Windows вплоть до Windows 8 и позволяет использовать его на разных платформах.</span><span class="sxs-lookup"><span data-stu-id="79447-106">DWriteCore is a form of DirectWrite that runs on versions of Windows down to Windows 8, and opens the door for you to use it cross-platform.</span></span> <span data-ttu-id="79447-107">Дополнительные сведения и примеры кода см. в разделе [двритекоре Overview](/windows/win32/DirectWrite/dwrite/dwritecore-overview).</span><span class="sxs-lookup"><span data-stu-id="79447-107">For more info, and code examples, see [DWriteCore overview](/windows/win32/DirectWrite/dwrite/dwritecore-overview).</span></span>

## <a name="syntax"></a><span data-ttu-id="79447-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="79447-108">Syntax</span></span>

```cpp
struct DWRITE_BITMAP_DATA_BGRA32
{
  UINT32 width;
  UINT32 height;
  _Field_size_(width * height) UINT32* pixels;
};
```

## <a name="members"></a><span data-ttu-id="79447-109">Члены</span><span class="sxs-lookup"><span data-stu-id="79447-109">Members</span></span>

`width`

<span data-ttu-id="79447-110">Тип: **[UINT32](../../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="79447-110">Type: **[UINT32](../../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="79447-111">Ширина точечного рисунка в пикселях.</span><span class="sxs-lookup"><span data-stu-id="79447-111">The width, in pixels, of the bitmap.</span></span>


`height`

<span data-ttu-id="79447-112">Тип: **[UINT32](../../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="79447-112">Type: **[UINT32](../../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="79447-113">Высота точечного рисунка (в пикселях).</span><span class="sxs-lookup"><span data-stu-id="79447-113">The height, in pixels, of the bitmap.</span></span>


`pixels`

<span data-ttu-id="79447-114">Тип: \_ \_ Размер поля \_ (ширина \* высота)**[UINT32](../../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="79447-114">Type: \_Field\_size\_(width \* height)**[UINT32](../../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="79447-115">Указатель на расположение битовых значений для точечного рисунка.</span><span class="sxs-lookup"><span data-stu-id="79447-115">A pointer to the location of the bit values for the bitmap.</span></span>


## <a name="examples"></a><span data-ttu-id="79447-116">Примеры</span><span class="sxs-lookup"><span data-stu-id="79447-116">Examples</span></span>

<span data-ttu-id="79447-117">См. раздел [Обзор двритекоре](/windows/win32/DirectWrite/dwrite/dwritecore-overview) и пример приложения [двритекорегаллери](https://github.com/microsoft/Project-Reunion-Samples/tree/main/DWriteCore/DWriteCoreGallery) .</span><span class="sxs-lookup"><span data-stu-id="79447-117">See the [DWriteCore overview](/windows/win32/DirectWrite/dwrite/dwritecore-overview) topic, and the [DWriteCoreGallery](https://github.com/microsoft/Project-Reunion-Samples/tree/main/DWriteCore/DWriteCoreGallery) sample app.</span></span>

## <a name="requirements"></a><span data-ttu-id="79447-118">Требования</span><span class="sxs-lookup"><span data-stu-id="79447-118">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="79447-119">**Минимальная версия клиента**</span><span class="sxs-lookup"><span data-stu-id="79447-119">**Minimum supported client**</span></span> | <span data-ttu-id="79447-120">Windows 10, переобъединение проектов [приложения Win32]</span><span class="sxs-lookup"><span data-stu-id="79447-120">Windows 10, Project Reunion [Win32 apps]</span></span> |
| <span data-ttu-id="79447-121">**Header**</span><span class="sxs-lookup"><span data-stu-id="79447-121">**Header**</span></span> | <span data-ttu-id="79447-122">dwrite_3. h (включает dwrite_core. h)</span><span class="sxs-lookup"><span data-stu-id="79447-122">dwrite_3.h (include dwrite_core.h)</span></span> |