---
description: Драйвер Unimodem, или универсальный модем, TSP (Унимдм. TSP) предоставляет доступ практически ко всем стандартным модемам.
ms.assetid: 1ea60477-f6c9-44ae-969c-515dfb0c607e
title: TSP Unimodem
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 115cc4fd159b2e62062171131f583bad19dc9b00
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105684224"
---
# <a name="unimodem-tsp"></a><span data-ttu-id="a7233-103">TSP Unimodem</span><span class="sxs-lookup"><span data-stu-id="a7233-103">Unimodem TSP</span></span>

<span data-ttu-id="a7233-104">Драйвер Unimodem, или универсальный модем, TSP (Унимдм. TSP) предоставляет доступ практически ко всем стандартным модемам.</span><span class="sxs-lookup"><span data-stu-id="a7233-104">The Unimodem, or Universal Modem Driver, TSP (Unimdm.tsp) provides access to nearly all standard modems.</span></span> <span data-ttu-id="a7233-105">Он поддерживает радиомодемы, поддерживающие двустороннюю потоковую передачу.</span><span class="sxs-lookup"><span data-stu-id="a7233-105">It supports voice modems that allow half-duplex streaming.</span></span> <span data-ttu-id="a7233-106">Поддерживаются звуковые MSP и управление потоком.</span><span class="sxs-lookup"><span data-stu-id="a7233-106">They are supported by the Wave MSP and stream control is possible.</span></span> <span data-ttu-id="a7233-107">(Обратите внимание, что Unimodem в Windows NT 4,0 или более ранней версии не поддерживает голосовые модемы, поэтому прямое управление потоком невозможно.)</span><span class="sxs-lookup"><span data-stu-id="a7233-107">(Note that Unimodem on Windows NT 4.0 or earlier does not support voice modems, so direct stream control is not possible.)</span></span>

<span data-ttu-id="a7233-108">Этот TSP поддерживает значение [**типа адреса**](./lineaddresstype--constants.md) линеаддресстипе \_ PHONENUMBER.</span><span class="sxs-lookup"><span data-stu-id="a7233-108">This TSP supports an [**address type**](./lineaddresstype--constants.md) value of LINEADDRESSTYPE\_PHONENUMBER.</span></span> <span data-ttu-id="a7233-109">Если программист хочет использовать правила набора номера, интерфейс TAPI 3 [**итаддресстранслатион**](/windows/win32/api/tapi3if/nn-tapi3if-itaddresstranslation) или функция [**линетранслатеаддресс**](/windows/win32/api/tapi/nf-tapi-linetranslateaddress) TAPI 2 должны использоваться для получения набора строк из номера телефона в каноническом формате.</span><span class="sxs-lookup"><span data-stu-id="a7233-109">If the programmer wants to use the dialing rules, the TAPI 3 [**ITAddressTranslation**](/windows/win32/api/tapi3if/nn-tapi3if-itaddresstranslation) interface or the TAPI 2 [**lineTranslateAddress**](/windows/win32/api/tapi/nf-tapi-linetranslateaddress) function must be used to obtain a dialable string from a phone number in canonical format.</span></span>

<span data-ttu-id="a7233-110">Unimodem TSP устанавливается вместе с операционными системами Windows Server 2003, Windows XP, Windows 2000, Windows NT, Windows Millennium Edition, Windows 98 и Windows 95.</span><span class="sxs-lookup"><span data-stu-id="a7233-110">The Unimodem TSP is installed with Windows Server 2003 operating systems, Windows XP, Windows 2000, Windows NT, Windows Millennium Edition, Windows 98, and Windows 95.</span></span>

 

 
