---
description: Инициализирует объект системной службы для установки объекта ActiveX, если текущий пользователь не имеет разрешения на установку объекта.
ms.assetid: 42f7cf83-789b-42ea-bb1a-4b79137188ea
title: Интерфейс Иеаксисервице
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IeAxiService
api_type:
- COM
api_location: ''
ms.openlocfilehash: 34c4743327b2539616dee6b09c34d9f479aa3303
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105663959"
---
# <a name="ieaxiservice-interface"></a><span data-ttu-id="abd25-103">Интерфейс Иеаксисервице</span><span class="sxs-lookup"><span data-stu-id="abd25-103">IeAxiService interface</span></span>

<span data-ttu-id="abd25-104">Интерфейс **иаксисервице** Инициализирует объект системной службы для установки объекта ActiveX, если у текущего пользователя нет разрешения на установку объекта.</span><span class="sxs-lookup"><span data-stu-id="abd25-104">The **IAxiService** interface initializes a system service object to install an ActiveX object when the current user does not have permission to install the object.</span></span>

<span data-ttu-id="abd25-105">Класс [**Циеаксиинсталлерсервице**](cieaxiinstallerservice.md) реализует этот интерфейс.</span><span class="sxs-lookup"><span data-stu-id="abd25-105">The [**CIeAxiInstallerService**](cieaxiinstallerservice.md) class implements this interface.</span></span>

<span data-ttu-id="abd25-106">Этот интерфейс не объявлен в общедоступном заголовке.</span><span class="sxs-lookup"><span data-stu-id="abd25-106">This interface is not declared in a public header.</span></span> <span data-ttu-id="abd25-107">Приложения должны самостоятельно определять его.</span><span class="sxs-lookup"><span data-stu-id="abd25-107">Applications must define it themselves.</span></span> <span data-ttu-id="abd25-108">Этот интерфейс описан в следующем фрагменте языка определения интерфейса (IDL), включая его IID.</span><span class="sxs-lookup"><span data-stu-id="abd25-108">The following Interface Definition Language (IDL) fragment describes this interface, including its IID.</span></span>

``` syntax
[
    object,
    uuid(E9E92380-9ECD-4982-A0EB-6815A56CCF27),
    pointer_default(unique)
]

interface IeAxiService : IUnknown{

    
    HRESULT Initialize(
            [in]        HWND            hwndParent,
            [in]        DWORD           dwClientPID,
            [in]        BSTR            bstrDesktop,
            [in]        BSTR            bstrClsID,              
            [in]        BSTR            bstrURL,                
            [out]       BSTR *          pbstrNonce,            
            [out]       IUnknown**      ppISyncBrokerInterface  
            );  
 
    HRESULT Cleanup();
};
```

## <a name="members"></a><span data-ttu-id="abd25-109">Элементы</span><span class="sxs-lookup"><span data-stu-id="abd25-109">Members</span></span>

<span data-ttu-id="abd25-110">Интерфейс **иеаксисервице** наследует от интерфейса [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="abd25-110">The **IeAxiService** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="abd25-111">**Иеаксисервице** также имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="abd25-111">**IeAxiService** also has these types of members:</span></span>

-   [<span data-ttu-id="abd25-112">Методы</span><span class="sxs-lookup"><span data-stu-id="abd25-112">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="abd25-113">Методы</span><span class="sxs-lookup"><span data-stu-id="abd25-113">Methods</span></span>

<span data-ttu-id="abd25-114">Интерфейс **иеаксисервице** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="abd25-114">The **IeAxiService** interface has these methods.</span></span>



| <span data-ttu-id="abd25-115">Метод</span><span class="sxs-lookup"><span data-stu-id="abd25-115">Method</span></span>                                        | <span data-ttu-id="abd25-116">Описание</span><span class="sxs-lookup"><span data-stu-id="abd25-116">Description</span></span>                                                        |
|:----------------------------------------------|:-------------------------------------------------------------------|
| [<span data-ttu-id="abd25-117">**Очистка**</span><span class="sxs-lookup"><span data-stu-id="abd25-117">**Cleanup**</span></span>](ieaxiservice-cleanup.md)       | <span data-ttu-id="abd25-118">Освобождает ресурсы, используемые интерфейсом **иеаксисервице** .</span><span class="sxs-lookup"><span data-stu-id="abd25-118">Frees resources used by the **IeAxiService** interface.</span></span><br/> |
| [<span data-ttu-id="abd25-119">**Инициализация**</span><span class="sxs-lookup"><span data-stu-id="abd25-119">**Initialize**</span></span>](ieaxiservice-initialize.md) | <span data-ttu-id="abd25-120">Проверяет и скачивает объект ActiveX.</span><span class="sxs-lookup"><span data-stu-id="abd25-120">Checks and downloads an ActiveX object.</span></span><br/>                 |



 

## <a name="requirements"></a><span data-ttu-id="abd25-121">Требования</span><span class="sxs-lookup"><span data-stu-id="abd25-121">Requirements</span></span>



| <span data-ttu-id="abd25-122">Требование</span><span class="sxs-lookup"><span data-stu-id="abd25-122">Requirement</span></span> | <span data-ttu-id="abd25-123">Значение</span><span class="sxs-lookup"><span data-stu-id="abd25-123">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="abd25-124">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="abd25-124">Minimum supported client</span></span><br/> | <span data-ttu-id="abd25-125">Windows Vista Business, Windows Vista Корпоративная, только для \[ настольных приложений Windows Vista Ultimate\]</span><span class="sxs-lookup"><span data-stu-id="abd25-125">Windows Vista Business, Windows Vista Enterprise, Windows Vista Ultimate \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="abd25-126">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="abd25-126">Minimum supported server</span></span><br/> | <span data-ttu-id="abd25-127">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="abd25-127">None supported</span></span><br/>                                                                                 |
| <span data-ttu-id="abd25-128">IID</span><span class="sxs-lookup"><span data-stu-id="abd25-128">IID</span></span><br/>                      | <span data-ttu-id="abd25-129">IID \_ иеаксисервице определен как E9E92380-9ECD-4982-A0EB-6815A56CCF27</span><span class="sxs-lookup"><span data-stu-id="abd25-129">IID\_IeAxiService is defined as E9E92380-9ECD-4982-A0EB-6815A56CCF27</span></span><br/>                           |



 

