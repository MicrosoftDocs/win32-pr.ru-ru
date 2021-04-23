---
description: Реализует интерфейсы Иаксисервице и Иеаксисервицекаллбакк.
ms.assetid: 39f2ee3a-d4fd-4091-acd6-3d6b715bea75
title: Объект Циеаксиинсталлерсервице
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIeAxiInstallerService
api_type:
- COM
api_location: ''
ms.openlocfilehash: b5ae7ec2a2c904a523f3388fa08a3bf2e44fec9d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103991194"
---
# <a name="cieaxiinstallerservice-object"></a><span data-ttu-id="e41ef-103">Объект Циеаксиинсталлерсервице</span><span class="sxs-lookup"><span data-stu-id="e41ef-103">CIeAxiInstallerService object</span></span>

<span data-ttu-id="e41ef-104">Объект **Циеаксиинсталлерсервице** реализует интерфейсы [**иаксисервице**](ieaxiservice.md) и [**иеаксисервицекаллбакк**](ieaxiservicecallback.md) .</span><span class="sxs-lookup"><span data-stu-id="e41ef-104">The **CIeAxiInstallerService** object implements the [**IAxiService**](ieaxiservice.md) and [**IeAxiServiceCallback**](ieaxiservicecallback.md) interfaces.</span></span>

<span data-ttu-id="e41ef-105">Этот объект не объявлен в общедоступном заголовке.</span><span class="sxs-lookup"><span data-stu-id="e41ef-105">This object is not declared in a public header.</span></span> <span data-ttu-id="e41ef-106">Приложения должны самостоятельно определять его.</span><span class="sxs-lookup"><span data-stu-id="e41ef-106">Applications must define it themselves.</span></span> <span data-ttu-id="e41ef-107">Этот объект описан в следующем фрагменте языка определения интерфейса (IDL), включая его CLSID.</span><span class="sxs-lookup"><span data-stu-id="e41ef-107">The following Interface Definition Language (IDL) fragment describes this object, including its CLSID.</span></span>

``` syntax
[
        uuid(90F18417-F0F1-484E-9D3C-59DCEEE5DBD8)
]
    coclass CIeAxiInstallerService
    {
        [default] interface IeAxiService;
        interface IeAxiServiceCallback;
    }

```

## <a name="requirements"></a><span data-ttu-id="e41ef-108">Требования</span><span class="sxs-lookup"><span data-stu-id="e41ef-108">Requirements</span></span>



| <span data-ttu-id="e41ef-109">Требование</span><span class="sxs-lookup"><span data-stu-id="e41ef-109">Requirement</span></span> | <span data-ttu-id="e41ef-110">Значение</span><span class="sxs-lookup"><span data-stu-id="e41ef-110">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e41ef-111">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="e41ef-111">Minimum supported client</span></span><br/> | <span data-ttu-id="e41ef-112">Windows Vista Business, Windows Vista Корпоративная, только для \[ настольных приложений Windows Vista Ultimate\]</span><span class="sxs-lookup"><span data-stu-id="e41ef-112">Windows Vista Business, Windows Vista Enterprise, Windows Vista Ultimate \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="e41ef-113">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="e41ef-113">Minimum supported server</span></span><br/> | <span data-ttu-id="e41ef-114">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="e41ef-114">None supported</span></span><br/>                                                                                 |



## <a name="see-also"></a><span data-ttu-id="e41ef-115">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="e41ef-115">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e41ef-116">**иаксисервице**</span><span class="sxs-lookup"><span data-stu-id="e41ef-116">**IAxiService**</span></span>](ieaxiservice.md)
</dt> <dt>

[<span data-ttu-id="e41ef-117">**иеаксисервицекаллбакк**</span><span class="sxs-lookup"><span data-stu-id="e41ef-117">**IeAxiServiceCallback**</span></span>](ieaxiservicecallback.md)
</dt> </dl>

 

 




