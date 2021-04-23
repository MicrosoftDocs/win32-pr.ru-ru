---
title: Подключение к компьютеру SDO
description: При помощи указателя интерфейса, возвращенного CoCreateInstance, вызовите метод Исдомачине Attach.
ms.assetid: b28691ef-4054-4cd1-92aa-72ad9902fba3
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1d35b9088fc1848dcf581bf69db036dce57cdd2b
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "103987585"
---
# <a name="attaching-to-the-sdo-computer"></a><span data-ttu-id="1a62d-103">Подключение к компьютеру SDO</span><span class="sxs-lookup"><span data-stu-id="1a62d-103">Attaching to the SDO Computer</span></span>

<span data-ttu-id="1a62d-104">При помощи указателя интерфейса, возвращенного [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance), вызовите метод [**Исдомачине:: Attach**](/windows/desktop/api/sdoias/nf-sdoias-isdomachine-attach) .</span><span class="sxs-lookup"><span data-stu-id="1a62d-104">With the interface pointer returned by [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance), call the [**ISdoMachine::Attach**](/windows/desktop/api/sdoias/nf-sdoias-isdomachine-attach) method.</span></span> <span data-ttu-id="1a62d-105">Передайте **значение NULL** в качестве параметра в метод **attach** .</span><span class="sxs-lookup"><span data-stu-id="1a62d-105">Pass **NULL** as the parameter to the **Attach** method.</span></span> <span data-ttu-id="1a62d-106">Значение **null** указывает, что **Присоединение** связывает объект компьютера с локальным компьютером.</span><span class="sxs-lookup"><span data-stu-id="1a62d-106">The value **NULL** specifies that **Attach** associate the machine object with the local computer.</span></span> <span data-ttu-id="1a62d-107">Присоединение к удаленному компьютеру не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="1a62d-107">Attaching to a remote computer is not supported.</span></span>

<span data-ttu-id="1a62d-108">Чтобы определить, присоединен ли локальный компьютер, вызовите метод [**исдомачине:: жетаттачедкомпутер**](/windows/desktop/api/sdoias/nf-sdoias-isdomachine-getattachedcomputer) .</span><span class="sxs-lookup"><span data-stu-id="1a62d-108">To determine if the local computer is already attached, call the [**ISdoMachine::GetAttachedComputer**](/windows/desktop/api/sdoias/nf-sdoias-isdomachine-getattachedcomputer) method.</span></span>

<span data-ttu-id="1a62d-109">Пример кода, демонстрирующий, как присоединиться к локальному компьютеру, см. [в разделе Присоединение к SDO-Enabled компьютеру](/windows/desktop/Nps/sdo-attaching-to-an-sdo-enabled-computer) .</span><span class="sxs-lookup"><span data-stu-id="1a62d-109">See [Attaching to an SDO-Enabled Computer](/windows/desktop/Nps/sdo-attaching-to-an-sdo-enabled-computer) for sample code that demonstrates how to attach to the local computer.</span></span>

 

 