---
title: протокол PPP через Ethernet подключения
description: Операционные системы Windows Server 2003, Windows XP и более поздних версий обеспечивают поддержку протокол PPP over Ethernet (PPPoE). Для подключения PPPoE задайте следующие значения в структуре РАСЕНТРИ.
ms.assetid: abdbf22c-abeb-4363-bfa6-e0002d1637f4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eed66d3a694896bdec9e0f53215a782d5896cd38
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "103987810"
---
# <a name="point-to-point-protocol-over-ethernet-connections"></a><span data-ttu-id="24f92-104">протокол PPP через Ethernet подключения</span><span class="sxs-lookup"><span data-stu-id="24f92-104">Point-to-Point Protocol over Ethernet Connections</span></span>

<span data-ttu-id="24f92-105">Операционные системы Windows Server 2003, Windows XP и более поздних версий обеспечивают поддержку протокол PPP over Ethernet (PPPoE).</span><span class="sxs-lookup"><span data-stu-id="24f92-105">Windows Server 2003, Windows XP, and later operating systems provide support for Point-to-Point Protocol over Ethernet (PPPoE).</span></span> <span data-ttu-id="24f92-106">Для подключения PPPoE задайте следующие значения в структуре [**расентри**](/previous-versions/windows/desktop/legacy/aa377274(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="24f92-106">For a PPPoE connection, set the following values in the [**RASENTRY**](/previous-versions/windows/desktop/legacy/aa377274(v=vs.85)) structure.</span></span>



| <span data-ttu-id="24f92-107">Член</span><span class="sxs-lookup"><span data-stu-id="24f92-107">Member</span></span>                      | <span data-ttu-id="24f92-108">Значение</span><span class="sxs-lookup"><span data-stu-id="24f92-108">Value</span></span>             |
|-----------------------------|-------------------|
| <span data-ttu-id="24f92-109">РАСЕНТРИ. Двтипе</span><span class="sxs-lookup"><span data-stu-id="24f92-109">RASENTRY.dwType</span></span>             | <span data-ttu-id="24f92-110">РАСЕТ \_ широкополосный доступ</span><span class="sxs-lookup"><span data-stu-id="24f92-110">RASET\_Broadband</span></span>  |
| <span data-ttu-id="24f92-111">РАЕНТРИ. Сздевицетипе</span><span class="sxs-lookup"><span data-stu-id="24f92-111">RAENTRY.szDeviceType</span></span>        | <span data-ttu-id="24f92-112">РАСДТ \_ PPPoE</span><span class="sxs-lookup"><span data-stu-id="24f92-112">RASDT\_PPPoE</span></span>      |
| <span data-ttu-id="24f92-113">РАСЕНТРИ. Сзлокалфоненумбер</span><span class="sxs-lookup"><span data-stu-id="24f92-113">RASENTRY.szLocalPhoneNumber</span></span> | <span data-ttu-id="24f92-114">Имя службы.</span><span class="sxs-lookup"><span data-stu-id="24f92-114">The service name.</span></span> |



 

<span data-ttu-id="24f92-115">Чтобы задать эти значения, используйте функцию [**рассетентрипропертиес**](/windows/desktop/api/Ras/nf-ras-rassetentrypropertiesa) .</span><span class="sxs-lookup"><span data-stu-id="24f92-115">Use the [**RasSetEntryProperties**](/windows/desktop/api/Ras/nf-ras-rassetentrypropertiesa) function to set these values.</span></span>

<span data-ttu-id="24f92-116">Вы также можете использовать [**расентридлг**](/windows/desktop/api/Rasdlg/nf-rasdlg-rasentrydlga) и флаг раседфлаг \_ невброадбандентри для [**расентридлг**](/windows/desktop/api/Rasdlg/nf-rasdlg-rasentrydlga) , чтобы отобразить мастер для создания записи телефонной книги PPPoE.</span><span class="sxs-lookup"><span data-stu-id="24f92-116">You can also use [**RasEntryDlg**](/windows/desktop/api/Rasdlg/nf-rasdlg-rasentrydlga) and the RASEDFLAG\_NewBroadbandEntry flag for [**RASENTRYDLG**](/windows/desktop/api/Rasdlg/nf-rasdlg-rasentrydlga) to display a wizard for creating a PPPoE phonebook entry.</span></span>

 

 