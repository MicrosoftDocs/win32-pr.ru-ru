---
description: Вызывается интерфейсом Иеаксисистеминсталлер для проверки возможности установки объекта ActiveX.
ms.assetid: d5cd6263-d07e-4261-9463-b9a06e883f16
title: Интерфейс Иеаксисервицекаллбакк
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IeAxiServiceCallback
api_type:
- COM
api_location: ''
ms.openlocfilehash: 3ad276126548ac6d5fdc2c828f722c90b43ad679
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103913643"
---
# <a name="ieaxiservicecallback-interface"></a><span data-ttu-id="89a21-103">Интерфейс Иеаксисервицекаллбакк</span><span class="sxs-lookup"><span data-stu-id="89a21-103">IeAxiServiceCallback interface</span></span>

<span data-ttu-id="89a21-104">Интерфейс **иеаксисервицекаллбакк** вызывается интерфейсом [**иеаксисистеминсталлер**](ieaxisysteminstaller.md) , чтобы проверить возможность установки объекта ActiveX.</span><span class="sxs-lookup"><span data-stu-id="89a21-104">The **IeAxiServiceCallback** interface is called by the [**IeAxiSystemInstaller**](ieaxisysteminstaller.md) interface to verify that an ActiveX object can be installed.</span></span>

<span data-ttu-id="89a21-105">Класс [**Циеаксиинсталлерсервице**](cieaxiinstallerservice.md) реализует этот интерфейс.</span><span class="sxs-lookup"><span data-stu-id="89a21-105">The [**CIeAxiInstallerService**](cieaxiinstallerservice.md) class implements this interface.</span></span>

<span data-ttu-id="89a21-106">Этот интерфейс не объявлен в общедоступном заголовке.</span><span class="sxs-lookup"><span data-stu-id="89a21-106">This interface is not declared in a public header.</span></span> <span data-ttu-id="89a21-107">Приложения должны самостоятельно определять его.</span><span class="sxs-lookup"><span data-stu-id="89a21-107">Applications must define it themselves.</span></span> <span data-ttu-id="89a21-108">Этот интерфейс описан в следующем фрагменте языка определения интерфейса (IDL), включая его IID.</span><span class="sxs-lookup"><span data-stu-id="89a21-108">The following Interface Definition Language (IDL) fragment describes this interface, including its IID.</span></span>

``` syntax
[
    object,
    uuid(1823E7BA-EC36-447a-9B2E-B4912E15AFE7),
    dual,
    nonextensible,
    pointer_default(unique)
]

interface IeAxiServiceCallback : IUnknown
{
    HRESULT VerifyFile(
                       [in] BSTR bstrFileUrl,
                       [out] BSTR * bstrApprovedFileName);
}

```

## <a name="members"></a><span data-ttu-id="89a21-109">Элементы</span><span class="sxs-lookup"><span data-stu-id="89a21-109">Members</span></span>

<span data-ttu-id="89a21-110">Интерфейс **иеаксисервицекаллбакк** наследует от интерфейса [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="89a21-110">The **IeAxiServiceCallback** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="89a21-111">**Иеаксисервицекаллбакк** также имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="89a21-111">**IeAxiServiceCallback** also has these types of members:</span></span>

-   [<span data-ttu-id="89a21-112">Методы</span><span class="sxs-lookup"><span data-stu-id="89a21-112">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="89a21-113">Методы</span><span class="sxs-lookup"><span data-stu-id="89a21-113">Methods</span></span>

<span data-ttu-id="89a21-114">Интерфейс **иеаксисервицекаллбакк** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="89a21-114">The **IeAxiServiceCallback** interface has these methods.</span></span>



| <span data-ttu-id="89a21-115">Метод</span><span class="sxs-lookup"><span data-stu-id="89a21-115">Method</span></span>                                                | <span data-ttu-id="89a21-116">Описание</span><span class="sxs-lookup"><span data-stu-id="89a21-116">Description</span></span>                                                                                                                                    |
|:------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="89a21-117">**верифифиле**</span><span class="sxs-lookup"><span data-stu-id="89a21-117">**VerifyFile**</span></span>](ieaxiservicecallback-verifyfile.md) | <span data-ttu-id="89a21-118">Выполняет проверки безопасности для указанного объекта ActiveX и возвращает расположение, в которое был скачан соответствующий CAB-файл.</span><span class="sxs-lookup"><span data-stu-id="89a21-118">Performs security checks on the specified ActiveX object and returns the location where the corresponding .cab file was downloaded.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="89a21-119">Требования</span><span class="sxs-lookup"><span data-stu-id="89a21-119">Requirements</span></span>



| <span data-ttu-id="89a21-120">Требование</span><span class="sxs-lookup"><span data-stu-id="89a21-120">Requirement</span></span> | <span data-ttu-id="89a21-121">Значение</span><span class="sxs-lookup"><span data-stu-id="89a21-121">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="89a21-122">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="89a21-122">Minimum supported client</span></span><br/> | <span data-ttu-id="89a21-123">Windows Vista Business, Windows Vista Корпоративная, только для \[ настольных приложений Windows Vista Ultimate\]</span><span class="sxs-lookup"><span data-stu-id="89a21-123">Windows Vista Business, Windows Vista Enterprise, Windows Vista Ultimate \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="89a21-124">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="89a21-124">Minimum supported server</span></span><br/> | <span data-ttu-id="89a21-125">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="89a21-125">None supported</span></span><br/>                                                                                 |
| <span data-ttu-id="89a21-126">IID</span><span class="sxs-lookup"><span data-stu-id="89a21-126">IID</span></span><br/>                      | <span data-ttu-id="89a21-127">IID \_ иеаксисервицекаллбакк определен как 1823E7BA-EC36-447a-9B2E-B4912E15AFE7</span><span class="sxs-lookup"><span data-stu-id="89a21-127">IID\_IeAxiServiceCallback is defined as 1823E7BA-EC36-447a-9B2E-B4912E15AFE7</span></span><br/>                   |



 

