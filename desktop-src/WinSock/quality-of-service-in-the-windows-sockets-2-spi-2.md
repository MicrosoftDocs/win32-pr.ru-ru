---
description: Качество обслуживания (QoS) реализовано в Windows с помощью различных компонентов QoS, поддерживаемых в Windows Server 2003, Windows XP и Windows 2000.
ms.assetid: e55b085f-6f72-4aa4-a8b0-b7609b9010dc
title: Качество обслуживания в списке SPI для Windows Sockets 2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e87d37f2e30e0a4fb296fc340353e2f4d85b5b8d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105702105"
---
# <a name="quality-of-service-in-the-windows-sockets-2-spi"></a><span data-ttu-id="689ab-103">Качество обслуживания в списке SPI для Windows Sockets 2</span><span class="sxs-lookup"><span data-stu-id="689ab-103">Quality of Service in the Windows Sockets 2 SPI</span></span>

<span data-ttu-id="689ab-104">Качество обслуживания (QoS) реализовано в Windows с помощью различных компонентов QoS, поддерживаемых в Windows Server 2003, Windows XP и Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="689ab-104">Quality of Service (QoS) is implemented in Windows through various QoS components supported on Windows Server 2003, Windows XP, and Windows 2000.</span></span> <span data-ttu-id="689ab-105">Подробное описание качества обслуживания и его компонентов можно найти в разделе, посвященном качеству обслуживания, который находится в пакете средств разработки программного обеспечения (SDK) для Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="689ab-105">A detailed explanation of QoS and its components is located in a section dedicated to Quality of Service, located in the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="689ab-106">Каждый компонент QoS и роль, которую он играет в реализации QoS, описаны в этом разделе, в котором содержатся дополнительные рекомендации по реализации приложений и служб, поддерживающих QoS.</span><span class="sxs-lookup"><span data-stu-id="689ab-106">Each QoS component, and the role it plays in the QoS implementation, is explained in this QoS section, with additional guidance provided for the implementation of QoS-enabled applications and services.</span></span> <span data-ttu-id="689ab-107">Более подробные сведения см. в разделе [качество обслуживания (QoS)](/previous-versions/windows/desktop/qos/qos-start-page) Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="689ab-107">Please see the [Quality of Service (QoS)](/previous-versions/windows/desktop/qos/qos-start-page) section of the Windows SDK for more detailed information.</span></span>

<span data-ttu-id="689ab-108">В этом разделе описываются возможности качества обслуживания, доступные для разработчиков Winsock.</span><span class="sxs-lookup"><span data-stu-id="689ab-108">This section describes Quality of Service capabilities available to Winsock developers.</span></span> <span data-ttu-id="689ab-109">В следующем списке перечислены подразделы этого раздела.</span><span class="sxs-lookup"><span data-stu-id="689ab-109">The following list describes the topics in this section:</span></span>

-   [<span data-ttu-id="689ab-110">Модель использования</span><span class="sxs-lookup"><span data-stu-id="689ab-110">Usage Model</span></span>](usage-model-2.md)
-   [<span data-ttu-id="689ab-111">Обновления QoS</span><span class="sxs-lookup"><span data-stu-id="689ab-111">QoS Updates</span></span>](qos-updates-2.md)
-   [<span data-ttu-id="689ab-112">Значения по умолчанию в SPI</span><span class="sxs-lookup"><span data-stu-id="689ab-112">Default Values in the SPI</span></span>](default-values-in-the-spi-2.md)
-   [<span data-ttu-id="689ab-113">Шаблоны качества обслуживания в SPI</span><span class="sxs-lookup"><span data-stu-id="689ab-113">QoS Templates in the SPI</span></span>](qos-templates-in-the-spi-2.md)

## <a name="related-topics"></a><span data-ttu-id="689ab-114">См. также</span><span class="sxs-lookup"><span data-stu-id="689ab-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="689ab-115">Качество обслуживания (QoS)</span><span class="sxs-lookup"><span data-stu-id="689ab-115">Quality of Service (QoS)</span></span>](/previous-versions/windows/desktop/qos/qos-start-page)
</dt> <dt>

<span data-ttu-id="689ab-116">[Что такое качество обслуживания?](/previous-versions/windows/it-pro/windows-server-2003/cc757120(v=ws.10))</span><span class="sxs-lookup"><span data-stu-id="689ab-116">[What Is QoS?](/previous-versions/windows/it-pro/windows-server-2003/cc757120(v=ws.10))</span></span>
</dt> <dt>

[<span data-ttu-id="689ab-117">Расширение службы Winsock ATM</span><span class="sxs-lookup"><span data-stu-id="689ab-117">Winsock ATM QoS Extension</span></span>](winsock-atm-qos-extension.md)
</dt> <dt>

[<span data-ttu-id="689ab-118">**Winsock IOCTL**</span><span class="sxs-lookup"><span data-stu-id="689ab-118">**Winsock IOCTLs**</span></span>](winsock-ioctls.md)
</dt> </dl>

 

 
