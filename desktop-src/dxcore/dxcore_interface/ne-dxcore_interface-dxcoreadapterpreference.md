---
title: DXCoreAdapterPreference
description: Определяет константы, указывающие параметры адаптера Дкскоре для использования в качестве критерия сортировки списка.
ms.localizationpriority: low
ms.topic: reference
ms.date: 09/03/2019
ms.openlocfilehash: 4301bdc1fe0ece8d9594ec3287e2ea8ddcce8f0a
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104413390"
---
# <a name="dxcoreadapterpreference-enum"></a><span data-ttu-id="9e7dd-103">Перечисление Дкскореадаптерпреференце</span><span class="sxs-lookup"><span data-stu-id="9e7dd-103">DXCoreAdapterPreference enum</span></span>

## <a name="description"></a><span data-ttu-id="9e7dd-104">Описание</span><span class="sxs-lookup"><span data-stu-id="9e7dd-104">Description</span></span>

<span data-ttu-id="9e7dd-105">Определяет константы, указывающие параметры адаптера Дкскоре для использования в качестве критерия сортировки списка.</span><span class="sxs-lookup"><span data-stu-id="9e7dd-105">Defines constants that specify DXCore adapter preferences to be used as list-sorting criteria.</span></span> <span data-ttu-id="9e7dd-106">Список адаптеров Дкскоре можно отсортировать, передав массив **дкскореадаптерпреференце** в [Идкскореадаптерлист:: Sort](./nf-dxcore_interface-idxcoreadapterlist-sort.md).</span><span class="sxs-lookup"><span data-stu-id="9e7dd-106">You can sort a DXCore adapter list by passing an array of **DXCoreAdapterPreference** to [IDXCoreAdapterList::Sort](./nf-dxcore_interface-idxcoreadapterlist-sort.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="9e7dd-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="9e7dd-107">Syntax</span></span>

```cpp
enum class DXCoreAdapterPreference : uint32_t
{
  Hardware = 0,
  MinimumPower = 1,
  HighPerformance = 2
};
```

## <a name="enum-fields"></a><span data-ttu-id="9e7dd-108">Поля перечислений</span><span class="sxs-lookup"><span data-stu-id="9e7dd-108">Enum fields</span></span>

### <a name="hardware"></a><span data-ttu-id="9e7dd-109">Оборудование</span><span class="sxs-lookup"><span data-stu-id="9e7dd-109">Hardware</span></span>

<span data-ttu-id="9e7dd-110">Задает предпочтения для аппаратных адаптеров (в отличие от программных адаптеров).</span><span class="sxs-lookup"><span data-stu-id="9e7dd-110">Specifies a preference for hardware adapters (as opposed to software adapters).</span></span>

### <a name="minimumpower"></a><span data-ttu-id="9e7dd-111">минимумповер</span><span class="sxs-lookup"><span data-stu-id="9e7dd-111">MinimumPower</span></span>

<span data-ttu-id="9e7dd-112">Указывает предпочитаемый для него графический процессор (например, встроенный графический процессор или ИГПУ).</span><span class="sxs-lookup"><span data-stu-id="9e7dd-112">Specifies a preference for the minimum-powered GPU (such as an integrated graphics processor, or iGPU).</span></span>

### <a name="highperformance"></a><span data-ttu-id="9e7dd-113">HighPerformance.</span><span class="sxs-lookup"><span data-stu-id="9e7dd-113">HighPerformance</span></span>

<span data-ttu-id="9e7dd-114">Задает предпочитаемый для высокопроизводительного графического процессора, например внешний графический процессор (Ксгпу), если он доступен, или дискретный графический процессор (ДГПУ), если он доступен.</span><span class="sxs-lookup"><span data-stu-id="9e7dd-114">Specifies a preference for the highest-performance GPU, such as an external graphics processor (xGPU), if available, or discrete graphics processor (dGPU) if available.</span></span>

## <a name="see-also"></a><span data-ttu-id="9e7dd-115">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="9e7dd-115">See also</span></span>

<span data-ttu-id="9e7dd-116">[Идкскореадаптерлист:: Sort](./nf-dxcore_interface-idxcoreadapterlist-sort.md), [дкскоре Reference](../dxcore-reference.md), [Использование дкскоре для перечисления адаптеров](../dxcore-enum-adapters.md)</span><span class="sxs-lookup"><span data-stu-id="9e7dd-116">[IDXCoreAdapterList::Sort](./nf-dxcore_interface-idxcoreadapterlist-sort.md), [DXCore Reference](../dxcore-reference.md), [Using DXCore to enumerate adapters](../dxcore-enum-adapters.md)</span></span>