---
title: IDXCoreAdapter::IsAttributeSupported
description: Определяет, поддерживает ли этот объект адаптера Дкскоре указанный атрибут адаптера.
ms.localizationpriority: low
ms.topic: reference
ms.date: 06/20/2019
ms.openlocfilehash: 9824595326f9e81bfa21ab198a3f5b2e6eae74bc
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104413106"
---
# <a name="idxcoreadapterisattributesupported-method"></a><span data-ttu-id="e96ef-103">Метод Идкскореадаптер:: Исаттрибутесуппортед</span><span class="sxs-lookup"><span data-stu-id="e96ef-103">IDXCoreAdapter::IsAttributeSupported method</span></span>

<span data-ttu-id="e96ef-104">Определяет, поддерживает ли этот объект адаптера Дкскоре указанный атрибут адаптера.</span><span class="sxs-lookup"><span data-stu-id="e96ef-104">Determines whether this DXCore adapter object supports the specified adapter attribute.</span></span>

## <a name="syntax"></a><span data-ttu-id="e96ef-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="e96ef-105">Syntax</span></span>

```cpp
virtual bool STDMETHODCALLTYPE IsAttributeSupported( 
  REFGUID attributeGUID) = 0;
```

## <a name="parameters"></a><span data-ttu-id="e96ef-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="e96ef-106">Parameters</span></span>

### <a name="attributeguid"></a><span data-ttu-id="e96ef-107">аттрибутегуид</span><span class="sxs-lookup"><span data-stu-id="e96ef-107">attributeGUID</span></span>

<span data-ttu-id="e96ef-108">Тип: **рефгуид**</span><span class="sxs-lookup"><span data-stu-id="e96ef-108">Type: **REFGUID**</span></span>

<span data-ttu-id="e96ef-109">Ссылка на GUID атрибута адаптера.</span><span class="sxs-lookup"><span data-stu-id="e96ef-109">A reference to an adapter attribute GUID.</span></span> <span data-ttu-id="e96ef-110">Список идентификаторов GUID атрибутов см. в разделе [идентификаторы GUID атрибута адаптера дкскоре](../dxcore-adapter-attribute-guids.md).</span><span class="sxs-lookup"><span data-stu-id="e96ef-110">For a list of attribute GUIDs, see [DXCore adapter attribute GUIDs](../dxcore-adapter-attribute-guids.md).</span></span>

## <a name="returns"></a><span data-ttu-id="e96ef-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="e96ef-111">Returns</span></span>

<span data-ttu-id="e96ef-112">Тип: **bool** .</span><span class="sxs-lookup"><span data-stu-id="e96ef-112">Type: **bool**</span></span>

<span data-ttu-id="e96ef-113">Возвращает  `true`   , если этот объект адаптера дкскоре поддерживает указанный атрибут адаптера.</span><span class="sxs-lookup"><span data-stu-id="e96ef-113">Returns `true` if this DXCore adapter object supports the specified adapter attribute.</span></span> <span data-ttu-id="e96ef-114">В противном случае возвращает  `false` .</span><span class="sxs-lookup"><span data-stu-id="e96ef-114">Otherwise, returns `false`.</span></span>

## <a name="see-also"></a><span data-ttu-id="e96ef-115">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="e96ef-115">See also</span></span>

<span data-ttu-id="e96ef-116">[Идкскореадаптер](./nn-dxcore_interface-idxcoreadapter.md), [ДКСКОРЕ Reference](../dxcore-reference.md), [GUID атрибутов адаптера дкскоре](../dxcore-adapter-attribute-guids.md), [Использование дкскоре для перечисления адаптеров](../dxcore-enum-adapters.md)</span><span class="sxs-lookup"><span data-stu-id="e96ef-116">[IDXCoreAdapter](./nn-dxcore_interface-idxcoreadapter.md), [DXCore Reference](../dxcore-reference.md), [DXCore adapter attribute GUIDs](../dxcore-adapter-attribute-guids.md), [Using DXCore to enumerate adapters](../dxcore-enum-adapters.md)</span></span>