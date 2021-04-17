---
description: Поиск расположения на ленте
ms.assetid: 17fb4eba-4b2c-41c2-94e2-e58586f92e53
title: Поиск расположения на ленте
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 33d1fb719f3b43374e5aa86f34c60e5b8f14d536
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105684116"
---
# <a name="tape-location-search"></a><span data-ttu-id="c814c-103">Поиск расположения на ленте</span><span class="sxs-lookup"><span data-stu-id="c814c-103">Tape Location Search</span></span>

<span data-ttu-id="c814c-104">Хотя DV-устройства поддерживают команду для поиска по коду времени или по номеру абсолютной записи (АТН), драйвер МСДВ не имеет стандартного, независимого от устройства способа доступа к этим функциям.</span><span class="sxs-lookup"><span data-stu-id="c814c-104">Although DV devices support a command to search by time code or by absolute track number (ATN), the MSDV driver does not have a standard, device-independent way to access these functions.</span></span> <span data-ttu-id="c814c-105">Единственным вариантом является отправка необработанной команды AV/C драйверу, как описано в разделе, [поставляющем необработанные команды AV/c](issuing-raw-av-c-commands.md).</span><span class="sxs-lookup"><span data-stu-id="c814c-105">The only option is to send a raw AV/C command to the driver as described in the topic [Issuing Raw AV/C Commands](issuing-raw-av-c-commands.md).</span></span>

<span data-ttu-id="c814c-106">Драйвер УВК поддерживает набор свойств для поиска по расположению ленты.</span><span class="sxs-lookup"><span data-stu-id="c814c-106">The UVC driver supports a property set for tape location searches.</span></span> <span data-ttu-id="c814c-107">Чтобы отправить команду поиска, используйте интерфейс **иксконтрол** и задайте \_ свойство пропсетид ext \_ Transport.</span><span class="sxs-lookup"><span data-stu-id="c814c-107">To send a search command, use the **IKsControl** interface and set the PROPSETID\_EXT\_TRANSPORT property.</span></span> <span data-ttu-id="c814c-108">Использование набора свойств является более безопасным, чем отправка необработанных команд AV/C на устройство, так как команды AV/C обходят фильтр и непосредственно переходят к драйверу устройства.</span><span class="sxs-lookup"><span data-stu-id="c814c-108">Using a property set is safer than sending raw AV/C commands to the device, because AV/C commands bypass the filter and go directly to the device driver.</span></span>

## <a name="related-topics"></a><span data-ttu-id="c814c-109">См. также</span><span class="sxs-lookup"><span data-stu-id="c814c-109">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c814c-110">Управление видеокамерой</span><span class="sxs-lookup"><span data-stu-id="c814c-110">Controlling a DV Camcorder</span></span>](controlling-a-dv-camcorder.md)
</dt> <dt>

[<span data-ttu-id="c814c-111">Набор свойств транспорта внешнего устройства</span><span class="sxs-lookup"><span data-stu-id="c814c-111">External Device Transport Property Set</span></span>](external-device-transport-property-set.md)
</dt> </dl>

 

 



