---
title: DXCoreAdapterMemoryBudget
description: Описывает бюджет памяти для адаптера.
ms.localizationpriority: low
ms.topic: reference
ms.date: 06/20/2019
ms.openlocfilehash: 2888b1480e3e394640a10bf0264403cd6c153e3b
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104488197"
---
# <a name="dxcoreadaptermemorybudget-structure"></a><span data-ttu-id="919da-103">Структура Дкскореадаптермеморибуджет</span><span class="sxs-lookup"><span data-stu-id="919da-103">DXCoreAdapterMemoryBudget structure</span></span>

<span data-ttu-id="919da-104">Указывает состояние адаптера <em>адаптермеморибуджет</em> , которое извлекает или запрашивает бюджет памяти адаптера на адаптере.</span><span class="sxs-lookup"><span data-stu-id="919da-104">Specifies the <em>AdapterMemoryBudget</em> adapter state, which retrieves or requests the adapter memory budget on the adapter.</span></span> <span data-ttu-id="919da-105">Установка (запрос) бюджета представляет минимальный объем физической памяти, необходимый для резервирования адаптера (в байтах).</span><span class="sxs-lookup"><span data-stu-id="919da-105">Setting (requesting) a budget represents the minimum required physical memory to reserve, in bytes, on the adapter.</span></span> <span data-ttu-id="919da-106">Рекомендуется настроить резервирование адаптера, чтобы обозначить объем физической памяти, которую приложение не может использовать.</span><span class="sxs-lookup"><span data-stu-id="919da-106">We recommend that you set an adapter reservation in order to denote the amount of physical memory that your application can't go without.</span></span> <span data-ttu-id="919da-107">Это значение помогает операционной системе (ОС) быстро уменьшить влияние больших случаев нехватки памяти.</span><span class="sxs-lookup"><span data-stu-id="919da-107">This value helps the operating system (OS) to quickly minimize the impact of large memory-pressure situations.</span></span>

<span data-ttu-id="919da-108">При вызове [куеристате](./nf-dxcore_interface-idxcoreadapter-querystate.md)состояние адаптера <em>Адаптермеморибуджет</em> имеет тип <a href="/windows/win32/dxcore/dxcore_interface/ns-dxcore_interface-dxcoreadaptermemorybudgetnodesegmentgroup">Дкскореадаптермеморибуджетнодесегментграуп</a> для *инпутстатедетаилс* и тип **DXCoreAdapterMemoryBudget** для *outputBuffer*.</span><span class="sxs-lookup"><span data-stu-id="919da-108">When calling [QueryState](./nf-dxcore_interface-idxcoreadapter-querystate.md), the <em>AdapterMemoryBudget</em> adapter state has type <a href="/windows/win32/dxcore/dxcore_interface/ns-dxcore_interface-dxcoreadaptermemorybudgetnodesegmentgroup">DXCoreAdapterMemoryBudgetNodeSegmentGroup</a> for *inputStateDetails*, and type **DXCoreAdapterMemoryBudget** for *outputBuffer*.</span></span>

<span data-ttu-id="919da-109">При вызове [SetState](./nf-dxcore_interface-idxcoreadapter-setstate.md)состояние адаптера <em>Адаптермеморибуджет</em> имеет тип <a href="/windows/win32/dxcore/dxcore_interface/ns-dxcore_interface-dxcoreadaptermemorybudgetnodesegmentgroup">дкскореадаптермеморибуджетнодесегментграуп</a> для *инпутстатедетаилс* и тип **uint64_t** для *inputData*.</span><span class="sxs-lookup"><span data-stu-id="919da-109">When calling [SetState](./nf-dxcore_interface-idxcoreadapter-setstate.md), the <em>AdapterMemoryBudget</em> adapter state has type <a href="/windows/win32/dxcore/dxcore_interface/ns-dxcore_interface-dxcoreadaptermemorybudgetnodesegmentgroup">DXCoreAdapterMemoryBudgetNodeSegmentGroup</a> for *inputStateDetails*, and type **uint64_t** for *inputData*.</span></span>

## <a name="syntax"></a><span data-ttu-id="919da-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="919da-110">Syntax</span></span>

```cpp
struct DXCoreAdapterMemoryBudget
{
  uint64_t budget;
  uint64_t currentUsage;
  uint64_t availableForReservation;
  uint64_t currentReservation;
};
```

## <a name="members"></a><span data-ttu-id="919da-111">Члены</span><span class="sxs-lookup"><span data-stu-id="919da-111">Members</span></span>

### <a name="budget"></a><span data-ttu-id="919da-112">составлен</span><span class="sxs-lookup"><span data-stu-id="919da-112">budget</span></span>

<span data-ttu-id="919da-113">Тип: **uint64_t**</span><span class="sxs-lookup"><span data-stu-id="919da-113">Type: **uint64_t**</span></span>

<span data-ttu-id="919da-114">Указывает предоставляемый ОС бюджет памяти (в байтах), который должно быть целевое приложение.</span><span class="sxs-lookup"><span data-stu-id="919da-114">Specifies the OS-provided adapter memory budget, in bytes, that your application should target.</span></span> <span data-ttu-id="919da-115">Если *куррентусаже* больше, чем *бюджет*, приложение может повлечь за собой "дергания" или снижения производительности из-за фоновых действий операционной системы, которая предназначена для предоставления другим приложениям достаточного использования памяти адаптера.</span><span class="sxs-lookup"><span data-stu-id="919da-115">If *currentUsage* is greater than *budget*, then your application may incur stuttering or performance penalties due to background activity by the OS, which is intended to provide other applications with a fair usage of adapter memory.</span></span>

### <a name="currentusage"></a><span data-ttu-id="919da-116">куррентусаже</span><span class="sxs-lookup"><span data-stu-id="919da-116">currentUsage</span></span>

<span data-ttu-id="919da-117">Тип: **uint64_t**</span><span class="sxs-lookup"><span data-stu-id="919da-117">Type: **uint64_t**</span></span>

<span data-ttu-id="919da-118">Указывает текущее использование памяти адаптера приложения отменено в байтах.</span><span class="sxs-lookup"><span data-stu-id="919da-118">Specifies your applicaton's current adapter memory usage, in bytes.</span></span>

### <a name="availableforreservation"></a><span data-ttu-id="919da-119">аваилаблефорресерватион</span><span class="sxs-lookup"><span data-stu-id="919da-119">availableForReservation</span></span>

<span data-ttu-id="919da-120">Тип: **uint64_t**</span><span class="sxs-lookup"><span data-stu-id="919da-120">Type: **uint64_t**</span></span>

<span data-ttu-id="919da-121">Указывает объем памяти адаптера в байтах, доступный для резервирования приложением.</span><span class="sxs-lookup"><span data-stu-id="919da-121">Specifies the amount of adapter memory, in bytes, that your application has available for reservation.</span></span> <span data-ttu-id="919da-122">Чтобы зарезервировать эту память адаптера, приложение должно вызвать [идкскореадаптер:: setState](./nf-dxcore_interface-idxcoreadapter-setstate.md) с *состоянием* , установленным в [дкскореадаптерстате:: адаптермеморибуджет](./ne-dxcore_interface-dxcoreadapterstate.md).</span><span class="sxs-lookup"><span data-stu-id="919da-122">To reserve this adapter memory, your application should call [IDXCoreAdapter::SetState](./nf-dxcore_interface-idxcoreadapter-setstate.md) with *state* set to [DXCoreAdapterState::AdapterMemoryBudget](./ne-dxcore_interface-dxcoreadapterstate.md).</span></span>

### <a name="currentreservation"></a><span data-ttu-id="919da-123">куррентресерватион</span><span class="sxs-lookup"><span data-stu-id="919da-123">currentReservation</span></span>

<span data-ttu-id="919da-124">Тип: **uint64_t**</span><span class="sxs-lookup"><span data-stu-id="919da-124">Type: **uint64_t**</span></span>

<span data-ttu-id="919da-125">Указывает объем памяти адаптера в байтах, зарезервированный приложением.</span><span class="sxs-lookup"><span data-stu-id="919da-125">Specifies the amount of adapter memory, in bytes, that is reserved by your application.</span></span> <span data-ttu-id="919da-126">ОС использует резервирование в качестве подсказки для определения минимального рабочего набора приложения.</span><span class="sxs-lookup"><span data-stu-id="919da-126">The OS uses the reservation as a hint to determine your application's minimum working set.</span></span> <span data-ttu-id="919da-127">Приложение должно попытаться отрезать использование памяти адаптера в соответствии с этим требованием.</span><span class="sxs-lookup"><span data-stu-id="919da-127">Your application should attempt to ensure that its adapter memory usage can be trimmed to meet this requirement.</span></span>

## <a name="see-also"></a><span data-ttu-id="919da-128">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="919da-128">See also</span></span>

<span data-ttu-id="919da-129">[Дкскоре Reference](../dxcore-reference.md), [Использование дкскоре для перечисления адаптеров](../dxcore-enum-adapters.md)</span><span class="sxs-lookup"><span data-stu-id="919da-129">[DXCore Reference](../dxcore-reference.md), [Using DXCore to enumerate adapters](../dxcore-enum-adapters.md)</span></span>