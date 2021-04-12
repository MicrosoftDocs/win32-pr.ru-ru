---
title: DXCoreAdapterState
description: Определяет константы, указывающие виды состояний адаптера Дкскоре.
ms.localizationpriority: low
ms.topic: reference
ms.date: 06/20/2019
ms.openlocfilehash: e588b75360c141b52989aa14e88c886092af2647
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104338041"
---
# <a name="dxcoreadapterstate-enum"></a><span data-ttu-id="81a02-103">Перечисление Дкскореадаптерстате</span><span class="sxs-lookup"><span data-stu-id="81a02-103">DXCoreAdapterState enum</span></span>

<span data-ttu-id="81a02-104">Определяет константы, указывающие виды состояний адаптера Дкскоре.</span><span class="sxs-lookup"><span data-stu-id="81a02-104">Defines constants that specify kinds of DXCore adapter states.</span></span> <span data-ttu-id="81a02-105">Передайте одну из этих констант методу [идкскореадаптер:: куеристате](./nf-dxcore_interface-idxcoreadapter-querystate.md) , чтобы получить элемент состояния адаптера для типа состояния. Передайте константу в метод [идкскореадаптер:: setState](./nf-dxcore_interface-idxcoreadapter-setstate.md) , чтобы задать сведения о адаптере для элемента состояния.</span><span class="sxs-lookup"><span data-stu-id="81a02-105">Pass one of these constants to the [IDXCoreAdapter::QueryState](./nf-dxcore_interface-idxcoreadapter-querystate.md) method to retrieve the adapter state item for a state kind; pass a constant to the [IDXCoreAdapter::SetState](./nf-dxcore_interface-idxcoreadapter-setstate.md) method to set an adapter's info for a state item.</span></span>

## <a name="syntax"></a><span data-ttu-id="81a02-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="81a02-106">Syntax</span></span>

```cpp
enum class DXCoreAdapterState : uint32_t
{
  IsDriverUpdateInProgress = 0,
  AdapterMemoryBudget = 1
};
```

## <a name="constants"></a><span data-ttu-id="81a02-107">Константы</span><span class="sxs-lookup"><span data-stu-id="81a02-107">Constants</span></span>

### <a name="isdriverupdateinprogress"></a><span data-ttu-id="81a02-108">исдриверупдатеинпрогресс</span><span class="sxs-lookup"><span data-stu-id="81a02-108">IsDriverUpdateInProgress</span></span>

<span data-ttu-id="81a02-109">Указывает состояние адаптера <em>исдриверупдатеинпрогресс</em> , которое `true` указывает, что на адаптере было инициировано обновление драйвера, но оно еще не завершено.</span><span class="sxs-lookup"><span data-stu-id="81a02-109">Specifies the <em>IsDriverUpdateInProgress</em> adapter state, which when `true` indicates that a driver update has been initiated on the adapter but it has not yet completed.</span></span> <span data-ttu-id="81a02-110">Если обновление драйвера уже завершено, адаптер станет недействительным, и вызов [куеристате](./nf-dxcore_interface-idxcoreadapter-querystate.md) возвратит значение <b>HRESULT</b> <b>DXGI_ERROR_DEVICE_REMOVED</b>.</span><span class="sxs-lookup"><span data-stu-id="81a02-110">If the driver update has already completed, then the adapter will have been invalidated, and your [QueryState](./nf-dxcore_interface-idxcoreadapter-querystate.md) call will return a <b>HRESULT</b> of <b>DXGI_ERROR_DEVICE_REMOVED</b>.</span></span>

<span data-ttu-id="81a02-111">При вызове [куеристате](./nf-dxcore_interface-idxcoreadapter-querystate.md)элемент состояния <em>исдриверупдатеинпрогресс</em> имеет тип <b>uint8_t</b>, представляющий логическое значение.</span><span class="sxs-lookup"><span data-stu-id="81a02-111">When calling [QueryState](./nf-dxcore_interface-idxcoreadapter-querystate.md), the <em>IsDriverUpdateInProgress</em> state item has type <b>uint8_t</b>, representing a Boolean value.</span></span>

<span data-ttu-id="81a02-112"><b>Важное</b> —</span><span class="sxs-lookup"><span data-stu-id="81a02-112"><b>Important</b>.</span></span> <span data-ttu-id="81a02-113">Этот элемент состояния не поддерживается для [SetState](./nf-dxcore_interface-idxcoreadapter-setstate.md).</span><span class="sxs-lookup"><span data-stu-id="81a02-113">This state item is not supported for [SetState](./nf-dxcore_interface-idxcoreadapter-setstate.md).</span></span>

### <a name="adaptermemorybudget"></a><span data-ttu-id="81a02-114">адаптермеморибуджет</span><span class="sxs-lookup"><span data-stu-id="81a02-114">AdapterMemoryBudget</span></span>

<span data-ttu-id="81a02-115">Указывает состояние адаптера <em>адаптермеморибуджет</em> , которое извлекает или запрашивает бюджет памяти адаптера на адаптере.</span><span class="sxs-lookup"><span data-stu-id="81a02-115">Specifies the <em>AdapterMemoryBudget</em> adapter state, which retrieves or requests the adapter memory budget on the adapter.</span></span>

<span data-ttu-id="81a02-116">При вызове [куеристате](./nf-dxcore_interface-idxcoreadapter-querystate.md)состояние адаптера <em>Адаптермеморибуджет</em> имеет тип <a href="/windows/win32/dxcore/dxcore_interface/ns-dxcore_interface-dxcoreadaptermemorybudgetnodesegmentgroup">Дкскореадаптермеморибуджетнодесегментграуп</a> для *инпутстатедетаилс* и тип <a href="/windows/win32/dxcore/dxcore_interface/ns-dxcore_interface-dxcoreadaptermemorybudget">DXCoreAdapterMemoryBudget</a> для *outputBuffer*.</span><span class="sxs-lookup"><span data-stu-id="81a02-116">When calling [QueryState](./nf-dxcore_interface-idxcoreadapter-querystate.md), the <em>AdapterMemoryBudget</em> adapter state has type <a href="/windows/win32/dxcore/dxcore_interface/ns-dxcore_interface-dxcoreadaptermemorybudgetnodesegmentgroup">DXCoreAdapterMemoryBudgetNodeSegmentGroup</a> for *inputStateDetails*, and type <a href="/windows/win32/dxcore/dxcore_interface/ns-dxcore_interface-dxcoreadaptermemorybudget">DXCoreAdapterMemoryBudget</a> for *outputBuffer*.</span></span>

## <a name="see-also"></a><span data-ttu-id="81a02-117">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="81a02-117">See also</span></span>

<span data-ttu-id="81a02-118">[Идкскореадаптер:: куеристате](./nf-dxcore_interface-idxcoreadapter-querystate.md), [Идкскореадаптер:: setState](./nf-dxcore_interface-idxcoreadapter-setstate.md), [дкскоре Reference](../dxcore-reference.md), [Использование дкскоре для перечисления адаптеров](../dxcore-enum-adapters.md)</span><span class="sxs-lookup"><span data-stu-id="81a02-118">[IDXCoreAdapter::QueryState](./nf-dxcore_interface-idxcoreadapter-querystate.md), [IDXCoreAdapter::SetState](./nf-dxcore_interface-idxcoreadapter-setstate.md), [DXCore Reference](../dxcore-reference.md), [Using DXCore to enumerate adapters](../dxcore-enum-adapters.md)</span></span>