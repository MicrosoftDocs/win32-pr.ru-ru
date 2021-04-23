---
title: Поддержка USB 3,0
description: Поддержка USB 3,0
ms.assetid: AACE4B57-A03F-40C7-AFDD-514D29F24521
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1c2f6fa342efa5e7b4fd95287a2061482fa0cbb9
ms.sourcegitcommit: ea4baf9953a78d2d6bd530b680601e39f3884541
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/01/2020
ms.locfileid: "103794220"
---
# <a name="support-for-usb-30"></a><span data-ttu-id="b8d4f-103">Поддержка USB 3,0</span><span class="sxs-lookup"><span data-stu-id="b8d4f-103">Support for USB 3.0</span></span>

## <a name="platforms"></a><span data-ttu-id="b8d4f-104">Платформы</span><span class="sxs-lookup"><span data-stu-id="b8d4f-104">Platforms</span></span>

<span data-ttu-id="b8d4f-105">**Клиенты** — Windows 8</span><span class="sxs-lookup"><span data-stu-id="b8d4f-105">**Clients** – Windows 8</span></span>  
<span data-ttu-id="b8d4f-106">**Серверы** — Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="b8d4f-106">**Servers** – Windows Server 2012</span></span>  


## <a name="description"></a><span data-ttu-id="b8d4f-107">Описание</span><span class="sxs-lookup"><span data-stu-id="b8d4f-107">Description</span></span>

<span data-ttu-id="b8d4f-108">В Windows 8 и Windows Server 2012 Добавлена поддержка USB 3,0.</span><span class="sxs-lookup"><span data-stu-id="b8d4f-108">In Windows 8 and Windows Server 2012, we added support for USB 3.0.</span></span> <span data-ttu-id="b8d4f-109">Мы сделали это, добавив новый стек программного обеспечения для питания контроллера узла USB 3,0, который называется расширяемым хост-контроллером (КСХК).</span><span class="sxs-lookup"><span data-stu-id="b8d4f-109">We did this by adding a new software stack to power the USB 3.0 host controller, called an eXtensible Host Controller (XHC).</span></span> <span data-ttu-id="b8d4f-110">Мы поддерживаем четность интерфейса, уровень IRQL, контекст вызывающего объекта, состояние ошибки, периодичность повтора и т. д.</span><span class="sxs-lookup"><span data-stu-id="b8d4f-110">We maintained interface parity, IRQL level, caller context, error status, retry frequency, and so on.</span></span> <span data-ttu-id="b8d4f-111">При взаимодействии с устройством, подключенным через USB 2,0 по сравнению с USB 3,0, не должно быть разницы.</span><span class="sxs-lookup"><span data-stu-id="b8d4f-111">There should be no difference for you when interacting with a device connected over USB 2.0 versus USB 3.0.</span></span>

<span data-ttu-id="b8d4f-112">Однако при написании драйвера для нового USB-устройства 3,0, определенно, следует использовать новые возможности USB 3,0.</span><span class="sxs-lookup"><span data-stu-id="b8d4f-112">However, if you are writing a driver for a new, USB 3.0 device, definitely opt for new USB 3.0 capabilities.</span></span>

## <a name="manifestation"></a><span data-ttu-id="b8d4f-113">Проявление</span><span class="sxs-lookup"><span data-stu-id="b8d4f-113">Manifestation</span></span>

<span data-ttu-id="b8d4f-114">Передача устройств выполняется быстрее, и снижается энергопотребление с компьютера на USB-устройствах в целом.</span><span class="sxs-lookup"><span data-stu-id="b8d4f-114">Device transfers are faster and less power is consumed from a PC by USB devices overall.</span></span> <span data-ttu-id="b8d4f-115">Существует риск того, что существующие USB-устройства могут работать неправильно при подключении к порту USB 3,0.</span><span class="sxs-lookup"><span data-stu-id="b8d4f-115">There is a risk that existing USB devices may not function correctly when connected to a USB 3.0 port.</span></span> <span data-ttu-id="b8d4f-116">Это не должно происходить и не ожидалось, но, поскольку программное обеспечение, обеспечивающее USB 3,0, является новым, это является риском.</span><span class="sxs-lookup"><span data-stu-id="b8d4f-116">This should not happen, and is not expected, but, because the software that powers USB 3.0 is new, it is a risk.</span></span>

 

 




