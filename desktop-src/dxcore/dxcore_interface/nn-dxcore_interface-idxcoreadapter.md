---
title: IDXCoreAdapter
description: Интерфейс **идкскореадаптер**   реализует методы для получения сведений об элементе адаптера.
ms.localizationpriority: low
ms.topic: reference
ms.date: 06/20/2019
ms.openlocfilehash: 0930ce76353d556f7839f476ec8979823eac3a6c
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104134427"
---
# <a name="idxcoreadapter-interface"></a><span data-ttu-id="f6f79-103">Интерфейс Идкскореадаптер</span><span class="sxs-lookup"><span data-stu-id="f6f79-103">IDXCoreAdapter interface</span></span>

<span data-ttu-id="f6f79-104">Интерфейс **идкскореадаптер**   реализует методы для получения сведений об элементе адаптера.</span><span class="sxs-lookup"><span data-stu-id="f6f79-104">The **IDXCoreAdapter** interface implements methods for retrieving details about an adapter item.</span></span> <span data-ttu-id="f6f79-105">**Идкскореадаптер** наследует от интерфейса [IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="f6f79-105">**IDXCoreAdapter** inherits from the [IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="f6f79-106">Инструкции по программированию и примеры кода см. [в разделе Использование дкскоре для перечисления адаптеров](../dxcore-enum-adapters.md).</span><span class="sxs-lookup"><span data-stu-id="f6f79-106">For programming guidance, and code examples, see [Using DXCore to enumerate adapters](../dxcore-enum-adapters.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="f6f79-107">Комментарии</span><span class="sxs-lookup"><span data-stu-id="f6f79-107">Remarks</span></span>

<span data-ttu-id="f6f79-108">Свойства адаптера устанавливаются во время запуска адаптера и становятся неизменяемыми в течение времени существования адаптера.</span><span class="sxs-lookup"><span data-stu-id="f6f79-108">An adapter's properties are established at the time the adapter starts, and they're immutable for the lifetime of the adapter.</span></span> <span data-ttu-id="f6f79-109">Это отличается от состояния адаптера, которое можно запрашивать или задавать, а значения, которые могут меняться со временем.</span><span class="sxs-lookup"><span data-stu-id="f6f79-109">This is in contrast to an adapter's state, which can be queried or set, and the values of which can change over time.</span></span>

## <a name="see-also"></a><span data-ttu-id="f6f79-110">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="f6f79-110">See also</span></span>

<span data-ttu-id="f6f79-111">[Дкскоре Reference](../dxcore-reference.md), [Использование дкскоре для перечисления адаптеров](../dxcore-enum-adapters.md)</span><span class="sxs-lookup"><span data-stu-id="f6f79-111">[DXCore Reference](../dxcore-reference.md), [Using DXCore to enumerate adapters](../dxcore-enum-adapters.md)</span></span>