---
description: Устанавливает объект ActiveX.
ms.assetid: 0eb725a9-ceb8-40e5-808d-ac2b286a48b6
title: Интерфейс Иеаксисистеминсталлер
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IeAxiSystemInstaller
api_type:
- COM
api_location: ''
ms.openlocfilehash: 391088a70aa845cd685511f10e4eb6e809dc7fcf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104081391"
---
# <a name="ieaxisysteminstaller-interface"></a><span data-ttu-id="62a2b-103">Интерфейс Иеаксисистеминсталлер</span><span class="sxs-lookup"><span data-stu-id="62a2b-103">IeAxiSystemInstaller interface</span></span>

<span data-ttu-id="62a2b-104">Интерфейс **иеаксисистеминсталлер** устанавливает объект ActiveX.</span><span class="sxs-lookup"><span data-stu-id="62a2b-104">The **IeAxiSystemInstaller** interface installs an ActiveX object.</span></span>

<span data-ttu-id="62a2b-105">Этот интерфейс не объявлен в общедоступном заголовке.</span><span class="sxs-lookup"><span data-stu-id="62a2b-105">This interface is not declared in a public header.</span></span> <span data-ttu-id="62a2b-106">Приложения должны самостоятельно определять его.</span><span class="sxs-lookup"><span data-stu-id="62a2b-106">Applications must define it themselves.</span></span> <span data-ttu-id="62a2b-107">Этот интерфейс описан в следующем фрагменте языка определения интерфейса (IDL), включая его IID.</span><span class="sxs-lookup"><span data-stu-id="62a2b-107">The following Interface Definition Language (IDL) fragment describes this interface, including its IID.</span></span>

``` syntax
[
    object,
    uuid(a50ea6f8-4764-4299-b309-022b2a8b4d8d),
    
]
interface IeAxiSystemInstaller : IUnknown
{
    
    HRESULT InitializeSystemInstaller(  [in] BSTR bstrUrl,
                                  [in] DWORD dwClientPID,
                                  [in] IUnknown* pCallback,
                                  [out] BSTR * pbstrNonce);
}

```

## <a name="members"></a><span data-ttu-id="62a2b-108">Элементы</span><span class="sxs-lookup"><span data-stu-id="62a2b-108">Members</span></span>

<span data-ttu-id="62a2b-109">Интерфейс **иеаксисистеминсталлер** наследует от интерфейса [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="62a2b-109">The **IeAxiSystemInstaller** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="62a2b-110">**Иеаксисистеминсталлер** также имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="62a2b-110">**IeAxiSystemInstaller** also has these types of members:</span></span>

-   [<span data-ttu-id="62a2b-111">Методы</span><span class="sxs-lookup"><span data-stu-id="62a2b-111">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="62a2b-112">Методы</span><span class="sxs-lookup"><span data-stu-id="62a2b-112">Methods</span></span>

<span data-ttu-id="62a2b-113">Интерфейс **иеаксисистеминсталлер** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="62a2b-113">The **IeAxiSystemInstaller** interface has these methods.</span></span>



| <span data-ttu-id="62a2b-114">Метод</span><span class="sxs-lookup"><span data-stu-id="62a2b-114">Method</span></span>                                                                              | <span data-ttu-id="62a2b-115">Описание</span><span class="sxs-lookup"><span data-stu-id="62a2b-115">Description</span></span>                                       |
|:------------------------------------------------------------------------------------|:--------------------------------------------------|
| [<span data-ttu-id="62a2b-116">**инитиализесистеминсталлер**</span><span class="sxs-lookup"><span data-stu-id="62a2b-116">**InitializeSystemInstaller**</span></span>](ieaxisysteminstaller-initializesysteminstaller.md) | <span data-ttu-id="62a2b-117">Устанавливает указанный объект ActiveX.</span><span class="sxs-lookup"><span data-stu-id="62a2b-117">Installs the specified ActiveX object.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="62a2b-118">Требования</span><span class="sxs-lookup"><span data-stu-id="62a2b-118">Requirements</span></span>



| <span data-ttu-id="62a2b-119">Требование</span><span class="sxs-lookup"><span data-stu-id="62a2b-119">Requirement</span></span> | <span data-ttu-id="62a2b-120">Значение</span><span class="sxs-lookup"><span data-stu-id="62a2b-120">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="62a2b-121">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="62a2b-121">Minimum supported client</span></span><br/> | <span data-ttu-id="62a2b-122">Windows Vista Business, Windows Vista Корпоративная, только для \[ настольных приложений Windows Vista Ultimate\]</span><span class="sxs-lookup"><span data-stu-id="62a2b-122">Windows Vista Business, Windows Vista Enterprise, Windows Vista Ultimate \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="62a2b-123">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="62a2b-123">Minimum supported server</span></span><br/> | <span data-ttu-id="62a2b-124">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="62a2b-124">None supported</span></span><br/>                                                                                 |
| <span data-ttu-id="62a2b-125">IID</span><span class="sxs-lookup"><span data-stu-id="62a2b-125">IID</span></span><br/>                      | <span data-ttu-id="62a2b-126">IID \_ иеаксисистеминсталлер определен как a50ea6f8-4764-4299-b309-022b2a8b4d8d</span><span class="sxs-lookup"><span data-stu-id="62a2b-126">IID\_IeAxiSystemInstaller is defined as a50ea6f8-4764-4299-b309-022b2a8b4d8d</span></span><br/>                   |



 

