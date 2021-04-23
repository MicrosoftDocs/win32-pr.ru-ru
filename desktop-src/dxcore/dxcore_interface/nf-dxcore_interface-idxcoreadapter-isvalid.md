---
title: IDXCoreAdapter::IsValid
description: Определяет, является ли этот объект адаптера Дкскоре допустимым.
ms.localizationpriority: low
ms.topic: reference
ms.date: 06/20/2019
ms.openlocfilehash: f58d8607b75253efda2e111eb358f576d36b65f0
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104070382"
---
# <a name="idxcoreadapterisvalid-method"></a><span data-ttu-id="8640d-103">Метод Идкскореадаптер:: IsValid</span><span class="sxs-lookup"><span data-stu-id="8640d-103">IDXCoreAdapter::IsValid method</span></span>

<span data-ttu-id="8640d-104">Определяет, является ли этот объект адаптера Дкскоре допустимым.</span><span class="sxs-lookup"><span data-stu-id="8640d-104">Determines whether this DXCore adapter object is still valid.</span></span> <span data-ttu-id="8640d-105">Инструкции по программированию и примеры кода см. [в разделе Использование дкскоре для перечисления адаптеров](../dxcore-enum-adapters.md).</span><span class="sxs-lookup"><span data-stu-id="8640d-105">For programming guidance, and code examples, see [Using DXCore to enumerate adapters](../dxcore-enum-adapters.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="8640d-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="8640d-106">Syntax</span></span>

```cpp
virtual bool STDMETHODCALLTYPE IsValid() = 0;
```

## <a name="returns"></a><span data-ttu-id="8640d-107">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="8640d-107">Returns</span></span>

<span data-ttu-id="8640d-108">Тип: **bool** .</span><span class="sxs-lookup"><span data-stu-id="8640d-108">Type: **bool**</span></span>

<span data-ttu-id="8640d-109">Возвращает значение  `true`   , если объект адаптера дкскоре по-прежнему является допустимым.</span><span class="sxs-lookup"><span data-stu-id="8640d-109">Returns `true` if this DXCore adapter object is still valid.</span></span> <span data-ttu-id="8640d-110">В противном случае возвращает  `false` .</span><span class="sxs-lookup"><span data-stu-id="8640d-110">Otherwise, returns `false`.</span></span>

## <a name="see-also"></a><span data-ttu-id="8640d-111">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="8640d-111">See also</span></span>

<span data-ttu-id="8640d-112">[Идкскореадаптер](./nn-dxcore_interface-idxcoreadapter.md), [дкскоре Reference](../dxcore-reference.md), [Использование дкскоре для перечисления адаптеров](../dxcore-enum-adapters.md)</span><span class="sxs-lookup"><span data-stu-id="8640d-112">[IDXCoreAdapter](./nn-dxcore_interface-idxcoreadapter.md), [DXCore Reference](../dxcore-reference.md), [Using DXCore to enumerate adapters](../dxcore-enum-adapters.md)</span></span>