---
description: Пользовательские устройства ввода представлены этими классами. Виртуальная машина всегда имеет по одному экземпляру каждого класса, связанного с ним.
ms.assetid: FFCA890D-6102-47BB-B499-4B9D77D75E9B
title: Входные классы
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b2955cadfb00dcc39fed490a9c706b12bb1a8993
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105683102"
---
# <a name="input-classes"></a><span data-ttu-id="7b470-104">Входные классы</span><span class="sxs-lookup"><span data-stu-id="7b470-104">Input classes</span></span>

<span data-ttu-id="7b470-105">Пользовательские устройства ввода представлены этими классами.</span><span class="sxs-lookup"><span data-stu-id="7b470-105">The user input devices are represented by these classes.</span></span> <span data-ttu-id="7b470-106">Виртуальная машина всегда имеет по одному экземпляру каждого класса, связанного с ним.</span><span class="sxs-lookup"><span data-stu-id="7b470-106">A virtual machine always has one instance of each class associated with it.</span></span> <span data-ttu-id="7b470-107">Эти устройства не могут быть добавлены или удалены с виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="7b470-107">These devices may not be added or removed from the virtual machine.</span></span> <span data-ttu-id="7b470-108">Таким образом, не существует экземпляров пула ресурсов для устройств клавиатуры или мыши.</span><span class="sxs-lookup"><span data-stu-id="7b470-108">Therefore, there are no resource pool instances for keyboard or mouse devices.</span></span>

<span data-ttu-id="7b470-109">Устройства с клавиатурой и мышью связаны с виртуальной машиной с помощью ассоциации [**мсвм \_ системдевице**](msvm-systemdevice.md) .</span><span class="sxs-lookup"><span data-stu-id="7b470-109">The keyboard and mouse devices are linked to the virtual machine through the [**Msvm\_SystemDevice**](msvm-systemdevice.md) association.</span></span> <span data-ttu-id="7b470-110">Виртуальная машина содержит как PS2, так и искусственное устройство мыши.</span><span class="sxs-lookup"><span data-stu-id="7b470-110">A virtual machine contains both a PS2 and a synthetic mouse device.</span></span> <span data-ttu-id="7b470-111">В каждый момент времени активно только одно указывающее устройство.</span><span class="sxs-lookup"><span data-stu-id="7b470-111">Only one pointing device is active at a time.</span></span>

<span data-ttu-id="7b470-112">Ниже перечислены классы WMI виртуализации, связанные с входными данными.</span><span class="sxs-lookup"><span data-stu-id="7b470-112">The following are virtualization WMI classes related to input.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="7b470-113">В этом разделе</span><span class="sxs-lookup"><span data-stu-id="7b470-113">In this section</span></span>



| <span data-ttu-id="7b470-114">Раздел</span><span class="sxs-lookup"><span data-stu-id="7b470-114">Topic</span></span>                                                          | <span data-ttu-id="7b470-115">Описание</span><span class="sxs-lookup"><span data-stu-id="7b470-115">Description</span></span>                                     |
|----------------------------------------------------------------|-------------------------------------------------|
| [<span data-ttu-id="7b470-116">**Мсвм \_ клавиатура**</span><span class="sxs-lookup"><span data-stu-id="7b470-116">**Msvm\_Keyboard**</span></span>](msvm-keyboard.md)<br/>             | <span data-ttu-id="7b470-117">Представляет устройство клавиатуры.</span><span class="sxs-lookup"><span data-stu-id="7b470-117">Represents a keyboard device.</span></span><br/>        |
| [<span data-ttu-id="7b470-118">**Мсвм \_ Ps2Mouse**</span><span class="sxs-lookup"><span data-stu-id="7b470-118">**Msvm\_Ps2Mouse**</span></span>](msvm-ps2mouse.md)<br/>             | <span data-ttu-id="7b470-119">Представляет устройство мыши PS2.</span><span class="sxs-lookup"><span data-stu-id="7b470-119">Represents a PS2 mouse device.</span></span><br/>       |
| [<span data-ttu-id="7b470-120">**Мсвм \_ синсетикмаусе**</span><span class="sxs-lookup"><span data-stu-id="7b470-120">**Msvm\_SyntheticMouse**</span></span>](msvm-syntheticmouse.md)<br/> | <span data-ttu-id="7b470-121">Представляет устройство искусственного мыши.</span><span class="sxs-lookup"><span data-stu-id="7b470-121">Represents a synthetic mouse device.</span></span><br/> |



 

 

 




