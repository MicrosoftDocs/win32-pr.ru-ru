---
UID: NN:dwrite_3.IDWriteBitmapRenderTarget2
title: IDWriteBitmapRenderTarget2 (dwrite_3.h)
description: 32 инкапсулирует независимое от устройства битовое изображение и контекст устройства, которые можно использовать для отрисовки глифов.
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
req.lib: Dwrite.lib
req.dll: Dwrite.dll
req.irql: ''
targetos: Windows
req.typenames: ''
req.redist: ''
f1_keywords:
- IDWriteBitmapRenderTarget2
- dwrite_3/IDWriteBitmapRenderTarget2
dev_langs:
- c++
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- dwrite.dll
api_name:
- IDWriteBitmapRenderTarget2
ms.openlocfilehash: 346b2e9c7510010abb50f421489b67f7d327512f
ms.sourcegitcommit: f848119a8faa29b27585f4df53f6e50ee9666684
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/27/2021
ms.locfileid: "110548949"
---
# <a name="idwritebitmaprendertarget2-interface-dwrite_3h"></a><span data-ttu-id="f9dc3-103">Интерфейс IDWriteBitmapRenderTarget2 (dwrite_3. h)</span><span class="sxs-lookup"><span data-stu-id="f9dc3-103">IDWriteBitmapRenderTarget2 interface (dwrite_3.h)</span></span>

<span data-ttu-id="f9dc3-104">32 инкапсулирует независимое от устройства битовое изображение и контекст устройства, которые можно использовать для отрисовки глифов.</span><span class="sxs-lookup"><span data-stu-id="f9dc3-104">Encapsulates a 32-bit device independent bitmap and device context, which can be used for rendering glyphs.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="f9dc3-105">Этот API доступен как часть реализации Двритекоре класса [DirectWrite](../direct-write-portal.md).</span><span class="sxs-lookup"><span data-stu-id="f9dc3-105">This API is available as part of the DWriteCore implementation of [DirectWrite](../direct-write-portal.md).</span></span> <span data-ttu-id="f9dc3-106">DWriteCore — это один из видов DirectWrite, который работает с версиями Windows вплоть до Windows 8 и позволяет использовать его на разных платформах.</span><span class="sxs-lookup"><span data-stu-id="f9dc3-106">DWriteCore is a form of DirectWrite that runs on versions of Windows down to Windows 8, and opens the door for you to use it cross-platform.</span></span> <span data-ttu-id="f9dc3-107">Дополнительные сведения и примеры кода см. в разделе [двритекоре Overview](../dwritecore-overview.md).</span><span class="sxs-lookup"><span data-stu-id="f9dc3-107">For more info, and code examples, see [DWriteCore overview](../dwritecore-overview.md).</span></span>

## <a name="inheritance"></a><span data-ttu-id="f9dc3-108">Наследование</span><span class="sxs-lookup"><span data-stu-id="f9dc3-108">Inheritance</span></span>

<span data-ttu-id="f9dc3-109">Интерфейс **IDWriteBitmapRenderTarget2** наследует от [IDWriteBitmapRenderTarget1](/windows/win32/api/dwrite_1/nn-dwrite_1-idwritebitmaprendertarget1).</span><span class="sxs-lookup"><span data-stu-id="f9dc3-109">The **IDWriteBitmapRenderTarget2** interface inherits from [IDWriteBitmapRenderTarget1](/windows/win32/api/dwrite_1/nn-dwrite_1-idwritebitmaprendertarget1).</span></span>

## <a name="methods"></a><span data-ttu-id="f9dc3-110">Методы</span><span class="sxs-lookup"><span data-stu-id="f9dc3-110">Methods</span></span>

<span data-ttu-id="f9dc3-111">Интерфейс **IDWriteBitmapRenderTarget2** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="f9dc3-111">The **IDWriteBitmapRenderTarget2** interface has these methods.</span></span>

| <span data-ttu-id="f9dc3-112">Метод</span><span class="sxs-lookup"><span data-stu-id="f9dc3-112">Method</span></span> | <span data-ttu-id="f9dc3-113">Описание</span><span class="sxs-lookup"><span data-stu-id="f9dc3-113">Description</span></span> |
| ---- |:---- |
| [<span data-ttu-id="f9dc3-114">IDWriteBitmapRenderTarget2:: "BitmapData"</span><span class="sxs-lookup"><span data-stu-id="f9dc3-114">IDWriteBitmapRenderTarget2::GetBitmapData</span></span>](./nf-dwrite_3-idwritebitmaprendertarget2-getbitmapdata.md) | <span data-ttu-id="f9dc3-115">Извлекает данные пикселя из целевого объекта прорисовки растрового изображения.</span><span class="sxs-lookup"><span data-stu-id="f9dc3-115">Retrieves the pixel data from a bitmap render target.</span></span> |

## <a name="requirements"></a><span data-ttu-id="f9dc3-116">Требования</span><span class="sxs-lookup"><span data-stu-id="f9dc3-116">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="f9dc3-117">**Минимальная версия клиента**</span><span class="sxs-lookup"><span data-stu-id="f9dc3-117">**Minimum supported client**</span></span> | <span data-ttu-id="f9dc3-118">Windows 10, переобъединение проектов [приложения Win32]</span><span class="sxs-lookup"><span data-stu-id="f9dc3-118">Windows 10, Project Reunion [Win32 apps]</span></span> |
| <span data-ttu-id="f9dc3-119">**Header**</span><span class="sxs-lookup"><span data-stu-id="f9dc3-119">**Header**</span></span> | <span data-ttu-id="f9dc3-120">dwrite_3. h (включает dwrite_core. h)</span><span class="sxs-lookup"><span data-stu-id="f9dc3-120">dwrite_3.h (include dwrite_core.h)</span></span> |