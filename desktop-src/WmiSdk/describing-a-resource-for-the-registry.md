---
description: Системный реестр содержит данные, связанные с ресурсами.
ms.assetid: e66f1db8-a5f3-41d3-9835-34b81b9da5ed
ms.tgt_platform: multiple
title: Описание ресурса для реестра
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3ba175120b5abec238d1b9078010359effef8ba2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105702719"
---
# <a name="describing-a-resource-for-the-registry"></a><span data-ttu-id="50bfc-103">Описание ресурса для реестра</span><span class="sxs-lookup"><span data-stu-id="50bfc-103">Describing a Resource for the Registry</span></span>

<span data-ttu-id="50bfc-104">Системный реестр содержит данные, связанные с ресурсами.</span><span class="sxs-lookup"><span data-stu-id="50bfc-104">The system registry contains resource-related data.</span></span> <span data-ttu-id="50bfc-105">Эти данные находятся в следующем разделе реестра и хранятся в специальном типе данных реестра с именем **reg \_ Resource \_ List**.</span><span class="sxs-lookup"><span data-stu-id="50bfc-105">This data is located under the following registry key and is kept in a special registry data type named **REG\_RESOURCE\_LIST**.</span></span> <span data-ttu-id="50bfc-106">Приложения могут получать связанные с ресурсами данные через поставщик системного реестра.</span><span class="sxs-lookup"><span data-stu-id="50bfc-106">Applications can obtain the resource-related data through the System Registry provider.</span></span> <span data-ttu-id="50bfc-107">В реестр можно добавлять и изменять системные ресурсы.</span><span class="sxs-lookup"><span data-stu-id="50bfc-107">You can add and modify system resources in the registry.</span></span>

```
HKEY_LOCAL_MACHINE
   Hardware
      ResourceMap
```

<span data-ttu-id="50bfc-108">В следующей процедуре описывается хранение сведений о ресурсах в системном реестре.</span><span class="sxs-lookup"><span data-stu-id="50bfc-108">The following procedure describes how to store resource-related information in the system registry.</span></span>

<span data-ttu-id="50bfc-109">**Сохранение сведений, связанных с ресурсами, в системном реестре**</span><span class="sxs-lookup"><span data-stu-id="50bfc-109">**To store resource-related information in the system registry**</span></span>

1.  <span data-ttu-id="50bfc-110">Создайте строку, содержащую следующие поля.</span><span class="sxs-lookup"><span data-stu-id="50bfc-110">Create a string that contains the following fields.</span></span>

    

    <table>
    <thead>
    <tr class="header">
    <th><span data-ttu-id="50bfc-111">Поле</span><span class="sxs-lookup"><span data-stu-id="50bfc-111">Field</span></span></th>
    <th><span data-ttu-id="50bfc-112">Содержит</span><span class="sxs-lookup"><span data-stu-id="50bfc-112">Contains</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td><span data-ttu-id="50bfc-113">Тип интерфейса</span><span class="sxs-lookup"><span data-stu-id="50bfc-113">Interface type</span></span></td>
    <td><span data-ttu-id="50bfc-114">Одно из следующих значений:</span><span class="sxs-lookup"><span data-stu-id="50bfc-114">One of the following values:</span></span><br/> <dl> <span data-ttu-id="50bfc-115">Внутренние</span><span class="sxs-lookup"><span data-stu-id="50bfc-115">Internal</span></span><br />
    <span data-ttu-id="50bfc-116">Диспетчера</span><span class="sxs-lookup"><span data-stu-id="50bfc-116">Isa</span></span><br />
    <span data-ttu-id="50bfc-117">Использует</span><span class="sxs-lookup"><span data-stu-id="50bfc-117">Eisa</span></span><br />
    <span data-ttu-id="50bfc-118">Микроканал</span><span class="sxs-lookup"><span data-stu-id="50bfc-118">MicroChannel</span></span><br />
    <span data-ttu-id="50bfc-119">турбочаннел</span><span class="sxs-lookup"><span data-stu-id="50bfc-119">TurboChannel</span></span><br />
    <span data-ttu-id="50bfc-120">пЦибус</span><span class="sxs-lookup"><span data-stu-id="50bfc-120">PCIBus</span></span><br />
    <span data-ttu-id="50bfc-121">вмебус</span><span class="sxs-lookup"><span data-stu-id="50bfc-121">VMEBus</span></span><br />
    <span data-ttu-id="50bfc-122">нубус</span><span class="sxs-lookup"><span data-stu-id="50bfc-122">NuBus</span></span><br />
    <span data-ttu-id="50bfc-123">пкмЦиабус</span><span class="sxs-lookup"><span data-stu-id="50bfc-123">PCMCIABus</span></span><br />
    <span data-ttu-id="50bfc-124">кбус</span><span class="sxs-lookup"><span data-stu-id="50bfc-124">CBus</span></span><br />
    <span data-ttu-id="50bfc-125">мпибус</span><span class="sxs-lookup"><span data-stu-id="50bfc-125">MPIBus</span></span><br />
    <span data-ttu-id="50bfc-126">мпсабус</span><span class="sxs-lookup"><span data-stu-id="50bfc-126">MPSABus</span></span><br />
    </dl></td>
    </tr>
    <tr class="even">
    <td><span data-ttu-id="50bfc-127">Номер шины</span><span class="sxs-lookup"><span data-stu-id="50bfc-127">Bus number</span></span></td>
    <td><span data-ttu-id="50bfc-128">Целое число, указывающее номер шины.</span><span class="sxs-lookup"><span data-stu-id="50bfc-128">Integer specifying the bus number.</span></span></td>
    </tr>
    <tr class="odd">
    <td><span data-ttu-id="50bfc-129">Частичный номер дескриптора</span><span class="sxs-lookup"><span data-stu-id="50bfc-129">Partial descriptor number</span></span></td>
    <td><span data-ttu-id="50bfc-130">Целое число, указывающее номер дескриптора.</span><span class="sxs-lookup"><span data-stu-id="50bfc-130">Integer specifying the descriptor number.</span></span></td>
    </tr>
    <tr class="even">
    <td><span data-ttu-id="50bfc-131">Тип смещения или объединения</span><span class="sxs-lookup"><span data-stu-id="50bfc-131">Offset or union type</span></span></td>
    <td><span data-ttu-id="50bfc-132">Одно из следующих значений:</span><span class="sxs-lookup"><span data-stu-id="50bfc-132">One of the following values:</span></span><br/> <dl> <span data-ttu-id="50bfc-133">Порт. Запуск</span><span class="sxs-lookup"><span data-stu-id="50bfc-133">Port.Start</span></span><br />
    <span data-ttu-id="50bfc-134">Порт. PhysicalAddress</span><span class="sxs-lookup"><span data-stu-id="50bfc-134">Port.PhysicalAddress</span></span><br />
    <span data-ttu-id="50bfc-135">Порт. Длина</span><span class="sxs-lookup"><span data-stu-id="50bfc-135">Port.Length</span></span><br />
    <span data-ttu-id="50bfc-136">Прервать. уровень</span><span class="sxs-lookup"><span data-stu-id="50bfc-136">Interrupt.Level</span></span><br />
    <span data-ttu-id="50bfc-137">Interrupt. Vector</span><span class="sxs-lookup"><span data-stu-id="50bfc-137">Interrupt.Vector</span></span><br />
    <span data-ttu-id="50bfc-138">Прерывание. сходство</span><span class="sxs-lookup"><span data-stu-id="50bfc-138">Interrupt.Affinity</span></span><br />
    <span data-ttu-id="50bfc-139">Память. Запуск</span><span class="sxs-lookup"><span data-stu-id="50bfc-139">Memory.Start</span></span><br />
    <span data-ttu-id="50bfc-140">Memory. PhysicalAddress</span><span class="sxs-lookup"><span data-stu-id="50bfc-140">Memory.PhysicalAddress</span></span><br />
    <span data-ttu-id="50bfc-141">Память. Длина</span><span class="sxs-lookup"><span data-stu-id="50bfc-141">Memory.Length</span></span><br />
    <span data-ttu-id="50bfc-142">Канал DMA.</span><span class="sxs-lookup"><span data-stu-id="50bfc-142">Dma.Channel</span></span><br />
    <span data-ttu-id="50bfc-143">DMA. Port</span><span class="sxs-lookup"><span data-stu-id="50bfc-143">Dma.Port</span></span><br />
    <span data-ttu-id="50bfc-144">DMA. Reserved1</span><span class="sxs-lookup"><span data-stu-id="50bfc-144">Dma.Reserved1</span></span><br />
    <span data-ttu-id="50bfc-145">ДевицеспеЦификдата. DataSize</span><span class="sxs-lookup"><span data-stu-id="50bfc-145">DeviceSpecificData.DataSize</span></span><br />
    <span data-ttu-id="50bfc-146">ДевицеспеЦификдата. Reserved1</span><span class="sxs-lookup"><span data-stu-id="50bfc-146">DeviceSpecificData.Reserved1</span></span><br />
    <span data-ttu-id="50bfc-147">ДевицеспеЦификдата. Reserved2</span><span class="sxs-lookup"><span data-stu-id="50bfc-147">DeviceSpecificData.Reserved2</span></span><br />
    </dl></td>
    </tr>
    </tbody>
    </table>

    

     

2.  <span data-ttu-id="50bfc-148">Поместите строку в соответствующий раздел раздела реестра.</span><span class="sxs-lookup"><span data-stu-id="50bfc-148">Place the string in the appropriate key under the registry key.</span></span>

    ```
    HKEY_LOCAL_MACHINE
       Hardware
          ResourceMap
    ```

<span data-ttu-id="50bfc-149">В следующем примере кода описывается допустимый дескриптор ресурса.</span><span class="sxs-lookup"><span data-stu-id="50bfc-149">The following code example describes a valid resource descriptor.</span></span>

``` syntax
local|hkey_local_machine\hardware\resourcemap\
  hardware abstraction layer\
  pc compatible eisa/isa HAL|.raw("eisa",0,0,"interrupt.affinity")
```

<span data-ttu-id="50bfc-150">В следующем примере кода показан допустимый синтаксис MOF для получения дескриптора ресурса.</span><span class="sxs-lookup"><span data-stu-id="50bfc-150">The following code example shows valid MOF syntax for retrieving a resource descriptor.</span></span>

``` syntax
[DYNPROPS] 
class MyRegProp
{    
   [KEY]  
   STRING MyKey; 
   STRING MyReservedTranslated;
};

[DYNPROPS] 
instance of MyRegProp
{
   MyKey = "1";
   [PropertyContext("local|hkey_local_Machine\\hardware\\ResourceMap\\
                   System Resources\\Reserved|.Translated
                   (\"Internal\")(0)(1)(\"Memory.PhysicalAddress\")"),
   Dynamic, Provider("RegPropProv")] 
   MyReservedTranslated;
};
```

 

 




