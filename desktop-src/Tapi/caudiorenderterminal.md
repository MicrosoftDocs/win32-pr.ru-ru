---
description: Терминал Каудиорендертерминал является производным от Ксинглефилтертерминал и реализует статический терминал воспроизведения звука для звуковых устройств с помощью фильтра звука DirectShow. Большинству MSP не требуется переопределять реализацию этого терминала.
ms.assetid: 58cd0765-9430-4333-ae96-4d8ca73727b5
title: каудиорендертерминал
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ad9915ef03a210f4ca440cb7a7b66448228b41df
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105683797"
---
# <a name="caudiorenderterminal"></a><span data-ttu-id="aa52f-104">каудиорендертерминал</span><span class="sxs-lookup"><span data-stu-id="aa52f-104">CAudioRenderTerminal</span></span>

<span data-ttu-id="aa52f-105">Терминал **каудиорендертерминал** является производным от [ксинглефилтертерминал](csinglefilterterminal.md) и реализует статический терминал воспроизведения звука для звуковых устройств с помощью фильтра звука DirectShow.</span><span class="sxs-lookup"><span data-stu-id="aa52f-105">The **CAudioRenderTerminal** terminal is derived from [CSingleFilterTerminal](csinglefilterterminal.md) and implements a static audio render terminal for wave devices using the DirectShow waveout filter.</span></span> <span data-ttu-id="aa52f-106">Большинству MSP не требуется переопределять реализацию этого терминала.</span><span class="sxs-lookup"><span data-stu-id="aa52f-106">Most MSPs will not need to override the implementation of this terminal.</span></span>

<span data-ttu-id="aa52f-107">Определен в Мсптрмар. h.</span><span class="sxs-lookup"><span data-stu-id="aa52f-107">Defined in MSPtrmar.h.</span></span>

## <a name="remarks"></a><span data-ttu-id="aa52f-108">Комментарии</span><span class="sxs-lookup"><span data-stu-id="aa52f-108">Remarks</span></span>

<span data-ttu-id="aa52f-109">Методы [**помещения \_ баланса**](/windows/desktop/api/tapi3if/nf-tapi3if-itbasicaudioterminal-put_balance) и [**получения \_ баланса**](/windows/desktop/api/tapi3if/nf-tapi3if-itbasicaudioterminal-get_balance) **каудиорендертерминал** не реализованы и будут возвращать E \_ нотимпл.</span><span class="sxs-lookup"><span data-stu-id="aa52f-109">The [**put\_Balance**](/windows/desktop/api/tapi3if/nf-tapi3if-itbasicaudioterminal-put_balance) and [**get\_Balance**](/windows/desktop/api/tapi3if/nf-tapi3if-itbasicaudioterminal-get_balance) methods of **CAudioRenderTerminal** are not implemented and will return E\_NOTIMPL.</span></span>

 

 



