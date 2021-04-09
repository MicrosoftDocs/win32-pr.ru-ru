---
title: IDXCoreAdapter::IsQueryStateSupported
description: Определяет, будет ли этот объект адаптера Дкскоре и текущая поддержка операционной системы (ОС) запрашивать значение указанного состояния адаптера.
ms.localizationpriority: low
ms.topic: reference
ms.date: 06/20/2019
ms.openlocfilehash: d154597f9b3ddbec24cff230317d881b9595bcde
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104134275"
---
# <a name="idxcoreadapterisquerystatesupported-method"></a><span data-ttu-id="f125f-103">Метод Идкскореадаптер:: Искуеристатесуппортед</span><span class="sxs-lookup"><span data-stu-id="f125f-103">IDXCoreAdapter::IsQueryStateSupported method</span></span>

<span data-ttu-id="f125f-104">Определяет, будет ли этот объект адаптера Дкскоре и текущая поддержка операционной системы (ОС) запрашивать значение указанного состояния адаптера.</span><span class="sxs-lookup"><span data-stu-id="f125f-104">Determines whether this DXCore adapter object and the current operating system (OS) support querying the value of the specified adapter state.</span></span>

## <a name="syntax"></a><span data-ttu-id="f125f-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="f125f-105">Syntax</span></span>

```cpp
virtual bool STDMETHODCALLTYPE IsQueryStateSupported( 
  DXCoreAdapterState property) = 0;
```

## <a name="parameters"></a><span data-ttu-id="f125f-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="f125f-106">Parameters</span></span>

### <a name="state"></a><span data-ttu-id="f125f-107">state</span><span class="sxs-lookup"><span data-stu-id="f125f-107">state</span></span>

<span data-ttu-id="f125f-108">Тип: **[дкскореадаптерстате](./ne-dxcore_interface-dxcoreadapterstate.md)**</span><span class="sxs-lookup"><span data-stu-id="f125f-108">Type: **[DXCoreAdapterState](./ne-dxcore_interface-dxcoreadapterstate.md)**</span></span>

<span data-ttu-id="f125f-109">Тип элемента состояния, для которого запрашиваются сведения о поддержке.</span><span class="sxs-lookup"><span data-stu-id="f125f-109">The kind of state item that you're querying about support for.</span></span> <span data-ttu-id="f125f-110">Дополнительные сведения о каждом типе состояния адаптера см. в таблице в [дкскореадаптерстате](./ne-dxcore_interface-dxcoreadapterstate.md) .</span><span class="sxs-lookup"><span data-stu-id="f125f-110">See the table in [DXCoreAdapterState](./ne-dxcore_interface-dxcoreadapterstate.md) for more info about each adapter state kind.</span></span>

## <a name="returns"></a><span data-ttu-id="f125f-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="f125f-111">Returns</span></span>

<span data-ttu-id="f125f-112">Тип: **bool** .</span><span class="sxs-lookup"><span data-stu-id="f125f-112">Type: **bool**</span></span>

<span data-ttu-id="f125f-113">Возвращает значение,  `true`   Если данный объект адаптера дкскоре и текущая поддержка операционной системы (ОС) запрашивают заданное состояние адаптера.</span><span class="sxs-lookup"><span data-stu-id="f125f-113">Returns `true` if this DXCore adapter object and the current operating system (OS) support querying the specified adapter state.</span></span> <span data-ttu-id="f125f-114">В противном случае возвращает  `false` .</span><span class="sxs-lookup"><span data-stu-id="f125f-114">Otherwise, returns `false`.</span></span>

## <a name="see-also"></a><span data-ttu-id="f125f-115">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="f125f-115">See also</span></span>

<span data-ttu-id="f125f-116">[Идкскореадаптер](./nn-dxcore_interface-idxcoreadapter.md), [ДКСКОРЕ Reference](../dxcore-reference.md), [GUID атрибутов адаптера дкскоре](../dxcore-adapter-attribute-guids.md), [Использование дкскоре для перечисления адаптеров](../dxcore-enum-adapters.md)</span><span class="sxs-lookup"><span data-stu-id="f125f-116">[IDXCoreAdapter](./nn-dxcore_interface-idxcoreadapter.md), [DXCore Reference](../dxcore-reference.md), [DXCore adapter attribute GUIDs](../dxcore-adapter-attribute-guids.md), [Using DXCore to enumerate adapters](../dxcore-enum-adapters.md)</span></span>