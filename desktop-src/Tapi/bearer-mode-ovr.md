---
description: Режим носителя соответствует качеству передачи, запрошенному из сети для установления вызова.
ms.assetid: 5276e1e7-7a91-4b74-b8c2-c0c7cebb203f
title: Режим носителя
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1780bee44254e6da754584f838785452ee728f18
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104263836"
---
# <a name="bearer-mode"></a><span data-ttu-id="e3519-103">Режим носителя</span><span class="sxs-lookup"><span data-stu-id="e3519-103">Bearer Mode</span></span>

<span data-ttu-id="e3519-104">[**Режим носителя**](./linebearermode--constants.md) соответствует качеству передачи, запрошенному из сети для установления вызова.</span><span class="sxs-lookup"><span data-stu-id="e3519-104">The [**bearer mode**](./linebearermode--constants.md) corresponds to the quality of transmission requested from the network for establishing a call.</span></span> <span data-ttu-id="e3519-105">Важно помнить, что понятие режима носителя не отличается от [**типа носителя**](tapimediatype--constants.md).</span><span class="sxs-lookup"><span data-stu-id="e3519-105">It is important to keep the concept of bearer mode separate from that of [**media type**](tapimediatype--constants.md).</span></span> <span data-ttu-id="e3519-106">Например, аналоговая телефонная сеть (PSTN) обеспечивает только режим носителя в 3,1 кГц, но вызов с его помощью может поддерживать такие типы носителей, как голосовой, Факс или модем данных.</span><span class="sxs-lookup"><span data-stu-id="e3519-106">As an example, the analog telephone network (PSTN) provides only a 3.1 kHz voice-grade bearer mode but calls using it can support media types such as voice, fax, or data modem.</span></span>

<span data-ttu-id="e3519-107">Режим носителя вызова указывается, когда вызов настраивается или предоставляется при вызове метода.</span><span class="sxs-lookup"><span data-stu-id="e3519-107">The bearer mode of a call is specified when the call is set up, or is provided when the call is offered.</span></span> <span data-ttu-id="e3519-108">Если линейные устройства могут представлять пулы каналов, поставщик услуг может разрешить вызовы с более широкой пропускной способностью.</span><span class="sxs-lookup"><span data-stu-id="e3519-108">With line devices able to represent channel pools, it is possible for a service provider to allow calls to be established with wider bandwidth.</span></span>

<span data-ttu-id="e3519-109">Не все поставщики служб поддерживают использование этих сведений.</span><span class="sxs-lookup"><span data-stu-id="e3519-109">Not all service providers support use of this information.</span></span>

<span data-ttu-id="e3519-110">**Интерфейс TAPI 2. x:** См. раздел [**линесеткаллпарамс**](/windows/win32/api/tapi/nf-tapi-linesetcallparams), [**линежеткаллинфо**](/windows/win32/api/tapi/nf-tapi-linegetcallinfo), **двбеарермоде** член [**линекаллинфо**](/windows/win32/api/tapi/ns-tapi-linecallinfo).</span><span class="sxs-lookup"><span data-stu-id="e3519-110">**TAPI 2.x:** See [**lineSetCallParams**](/windows/win32/api/tapi/nf-tapi-linesetcallparams), [**lineGetCallInfo**](/windows/win32/api/tapi/nf-tapi-linegetcallinfo), **dwBearerMode** member of [**LINECALLINFO**](/windows/win32/api/tapi/ns-tapi-linecallinfo).</span></span>

<span data-ttu-id="e3519-111">**Интерфейс TAPI 3. x:** См. раздел [**иткаллинфо:: Get \_ каллинфолонг**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-get_callinfolong), [**иткаллинфо::p UT \_ каллинфолонг**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-put_callinfolong), **CIL \_ беарермоде** [**каллинфо \_**](/windows/desktop/api/Tapi3if/ne-tapi3if-callinfo_long).</span><span class="sxs-lookup"><span data-stu-id="e3519-111">**TAPI 3.x:** See [**ITCallInfo::get\_CallInfoLong**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-get_callinfolong), [**ITCallInfo::put\_CallInfoLong**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-put_callinfolong), **CIL\_BEARERMODE** member of [**CALLINFO\_LONG**](/windows/desktop/api/Tapi3if/ne-tapi3if-callinfo_long).</span></span>

<span data-ttu-id="e3519-112">**Тспи:** См. [**строку \_ каллинфо**](/previous-versions/windows/desktop/legacy/ms725218(v=vs.85)) Message, где для *DWPARAM1* задано значение линекаллинфостате \_ беарермоде.</span><span class="sxs-lookup"><span data-stu-id="e3519-112">**TSPI:** See [**LINE\_CALLINFO**](/previous-versions/windows/desktop/legacy/ms725218(v=vs.85)) message, with *dwParam1* set to LINECALLINFOSTATE\_BEARERMODE.</span></span>

 

 
