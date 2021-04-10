---
title: DXCoreHardwareID
description: Представляет компоненты идентификатора оборудования PnP для адаптера.
ms.localizationpriority: low
ms.topic: reference
ms.date: 06/20/2019
ms.openlocfilehash: 6882d9aa16bf72fb33f9a254a6434becb37f9cb8
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104134006"
---
# <a name="dxcorehardwareid-structure"></a><span data-ttu-id="ee200-103">Структура Дкскорехардвареид</span><span class="sxs-lookup"><span data-stu-id="ee200-103">DXCoreHardwareID structure</span></span>

<span data-ttu-id="ee200-104">Представляет компоненты идентификатора оборудования PnP для адаптера.</span><span class="sxs-lookup"><span data-stu-id="ee200-104">Represents the PnP hardware ID parts for an adapter.</span></span>

## <a name="syntax"></a><span data-ttu-id="ee200-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="ee200-105">Syntax</span></span>

```cpp
struct DXCoreHardwareID
{
  uint32_t vendorID;
  uint32_t deviceID;
  uint32_t subSysID;
  uint32_t revision;
};
```

## <a name="members"></a><span data-ttu-id="ee200-106">Члены</span><span class="sxs-lookup"><span data-stu-id="ee200-106">Members</span></span>

### <a name="vendorid"></a><span data-ttu-id="ee200-107">Поставщика</span><span class="sxs-lookup"><span data-stu-id="ee200-107">vendorId</span></span>

<span data-ttu-id="ee200-108">Тип: **uint32_t \***</span><span class="sxs-lookup"><span data-stu-id="ee200-108">Type: **uint32_t\***</span></span>

<span data-ttu-id="ee200-109">Идентификатор PCI поставщика оборудования адаптера.</span><span class="sxs-lookup"><span data-stu-id="ee200-109">The PCI ID of the adapter's hardware vendor.</span></span>

### <a name="deviceid"></a><span data-ttu-id="ee200-110">deviceId</span><span class="sxs-lookup"><span data-stu-id="ee200-110">deviceId</span></span>

<span data-ttu-id="ee200-111">Тип: **uint32_t \***</span><span class="sxs-lookup"><span data-stu-id="ee200-111">Type: **uint32_t\***</span></span>

<span data-ttu-id="ee200-112">Идентификатор PCI аппаратного устройства адаптера.</span><span class="sxs-lookup"><span data-stu-id="ee200-112">The PCI ID of the adapter's hardware device.</span></span>

### <a name="subsysid"></a><span data-ttu-id="ee200-113">субсисид</span><span class="sxs-lookup"><span data-stu-id="ee200-113">subSysId</span></span>

<span data-ttu-id="ee200-114">Тип: **uint32_t \***</span><span class="sxs-lookup"><span data-stu-id="ee200-114">Type: **uint32_t\***</span></span>

<span data-ttu-id="ee200-115">Идентификатор PCI аппаратной подсистемы адаптера.</span><span class="sxs-lookup"><span data-stu-id="ee200-115">The PCI ID of the adapter's hardware subsystem.</span></span>

### <a name="revision"></a><span data-ttu-id="ee200-116">revision</span><span class="sxs-lookup"><span data-stu-id="ee200-116">revision</span></span>

<span data-ttu-id="ee200-117">Тип: **uint32_t \***</span><span class="sxs-lookup"><span data-stu-id="ee200-117">Type: **uint32_t\***</span></span>

<span data-ttu-id="ee200-118">Идентификатор PCI для номера редакции адаптера.</span><span class="sxs-lookup"><span data-stu-id="ee200-118">The PCI ID of the adapter's revision number.</span></span>

## <a name="see-also"></a><span data-ttu-id="ee200-119">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="ee200-119">See also</span></span>

<span data-ttu-id="ee200-120">[Дкскоре Reference](../dxcore-reference.md), [Использование дкскоре для перечисления адаптеров](../dxcore-enum-adapters.md)</span><span class="sxs-lookup"><span data-stu-id="ee200-120">[DXCore Reference](../dxcore-reference.md), [Using DXCore to enumerate adapters](../dxcore-enum-adapters.md)</span></span>