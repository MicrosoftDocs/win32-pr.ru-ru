---
title: IDXCoreAdapter::IsPropertySupported
description: Определяет, поддерживает ли этот объект адаптера Дкскоре и текущую операционную систему (ОС) указанное свойство адаптера.
ms.localizationpriority: low
ms.topic: reference
ms.date: 06/20/2019
ms.openlocfilehash: b960d96515d4aee85520a6def70a8f0e9349e131
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "105719140"
---
# <a name="idxcoreadapterispropertysupported-method"></a><span data-ttu-id="ce117-103">Метод Идкскореадаптер:: Испропертисуппортед</span><span class="sxs-lookup"><span data-stu-id="ce117-103">IDXCoreAdapter::IsPropertySupported method</span></span>

<span data-ttu-id="ce117-104">Определяет, поддерживает ли этот объект адаптера Дкскоре и текущую операционную систему (ОС) указанное свойство адаптера.</span><span class="sxs-lookup"><span data-stu-id="ce117-104">Determines whether this DXCore adapter object and the current operating system (OS) support the specified adapter property.</span></span>

## <a name="syntax"></a><span data-ttu-id="ce117-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="ce117-105">Syntax</span></span>

```cpp
virtual bool STDMETHODCALLTYPE IsPropertySupported( 
  DXCoreAdapterProperty property) = 0;
```

## <a name="parameters"></a><span data-ttu-id="ce117-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="ce117-106">Parameters</span></span>

### <a name="property"></a><span data-ttu-id="ce117-107">свойство;</span><span class="sxs-lookup"><span data-stu-id="ce117-107">property</span></span>

<span data-ttu-id="ce117-108">Тип: **[дкскореадаптерпроперти](./ne-dxcore_interface-dxcoreadapterproperty.md)**</span><span class="sxs-lookup"><span data-stu-id="ce117-108">Type: **[DXCoreAdapterProperty](./ne-dxcore_interface-dxcoreadapterproperty.md)**</span></span>

<span data-ttu-id="ce117-109">Тип свойства, для которого запрашиваются сведения о поддержке.</span><span class="sxs-lookup"><span data-stu-id="ce117-109">The type of property that you're querying about support for.</span></span> <span data-ttu-id="ce117-110">Дополнительные сведения о каждом свойстве адаптера см. в таблице в [дкскореадаптерпроперти](./ne-dxcore_interface-dxcoreadapterproperty.md) .</span><span class="sxs-lookup"><span data-stu-id="ce117-110">See the table in [DXCoreAdapterProperty](./ne-dxcore_interface-dxcoreadapterproperty.md) for more info about each adapter property.</span></span>

## <a name="returns"></a><span data-ttu-id="ce117-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="ce117-111">Returns</span></span>

<span data-ttu-id="ce117-112">Тип: **bool** .</span><span class="sxs-lookup"><span data-stu-id="ce117-112">Type: **bool**</span></span>

<span data-ttu-id="ce117-113">Возвращает значение  `true`   , если этот объект адаптера дкскоре и текущая операционная система (ОС) поддерживают указанное свойство адаптера.</span><span class="sxs-lookup"><span data-stu-id="ce117-113">Returns `true` if this DXCore adapter object and the current operating system (OS) support the specified adapter property.</span></span> <span data-ttu-id="ce117-114">В противном случае возвращает  `false` .</span><span class="sxs-lookup"><span data-stu-id="ce117-114">Otherwise, returns `false`.</span></span>

## <a name="see-also"></a><span data-ttu-id="ce117-115">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="ce117-115">See also</span></span>

<span data-ttu-id="ce117-116">[Идкскореадаптер](./nn-dxcore_interface-idxcoreadapter.md), [ДКСКОРЕ Reference](../dxcore-reference.md), [GUID атрибутов адаптера дкскоре](../dxcore-adapter-attribute-guids.md), [Использование дкскоре для перечисления адаптеров](../dxcore-enum-adapters.md)</span><span class="sxs-lookup"><span data-stu-id="ce117-116">[IDXCoreAdapter](./nn-dxcore_interface-idxcoreadapter.md), [DXCore Reference](../dxcore-reference.md), [DXCore adapter attribute GUIDs](../dxcore-adapter-attribute-guids.md), [Using DXCore to enumerate adapters](../dxcore-enum-adapters.md)</span></span>