---
description: Терминал Каудиокаптуретерминал является производным от Ксинглефилтертерминал и реализует статический терминал аудио-захвата для звуковых устройств с помощью фильтра Wave. Большинству MSP не требуется переопределять реализацию этого терминала.
ms.assetid: 2860bf22-46ae-484a-a47b-0d7057b900a1
title: каудиокаптуретерминал
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 308af17ce7a7cb4d2d4cadebb43b06437ec14abc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105674023"
---
# <a name="caudiocaptureterminal"></a><span data-ttu-id="ce5a5-104">каудиокаптуретерминал</span><span class="sxs-lookup"><span data-stu-id="ce5a5-104">CAudioCaptureTerminal</span></span>

<span data-ttu-id="ce5a5-105">Терминал **каудиокаптуретерминал** является производным от [ксинглефилтертерминал](csinglefilterterminal.md) и реализует статический терминал аудио-захвата для звуковых устройств с помощью фильтра Wave.</span><span class="sxs-lookup"><span data-stu-id="ce5a5-105">The **CAudioCaptureTerminal** terminal is derived from [CSingleFilterTerminal](csinglefilterterminal.md) and implements a static audio capture terminal for wave devices using the DirectShow wavein filter.</span></span> <span data-ttu-id="ce5a5-106">Большинству MSP не требуется переопределять реализацию этого терминала.</span><span class="sxs-lookup"><span data-stu-id="ce5a5-106">Most MSPs will not need to override the implementation of this terminal.</span></span>

<span data-ttu-id="ce5a5-107">Определен в Мсптмак. h.</span><span class="sxs-lookup"><span data-stu-id="ce5a5-107">Defined in MSPtmac.h.</span></span>

## <a name="remarks"></a><span data-ttu-id="ce5a5-108">Комментарии</span><span class="sxs-lookup"><span data-stu-id="ce5a5-108">Remarks</span></span>

<span data-ttu-id="ce5a5-109">Методы [**помещения \_ баланса**](/windows/desktop/api/tapi3if/nf-tapi3if-itbasicaudioterminal-put_balance) и [**получения \_ баланса**](/windows/desktop/api/tapi3if/nf-tapi3if-itbasicaudioterminal-get_balance) **каудиокаптуретерминал** не реализованы и будут возвращать E \_ нотимпл.</span><span class="sxs-lookup"><span data-stu-id="ce5a5-109">The [**put\_Balance**](/windows/desktop/api/tapi3if/nf-tapi3if-itbasicaudioterminal-put_balance) and [**get\_Balance**](/windows/desktop/api/tapi3if/nf-tapi3if-itbasicaudioterminal-get_balance) methods of **CAudioCaptureTerminal** are not implemented and will return E\_NOTIMPL.</span></span>

 

 



