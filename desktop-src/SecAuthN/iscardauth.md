---
description: Определение интерфейса Искардаус предоставляется в качестве стандарта, который может быть выполнен при разработке поставщика услуг смарт-карты. Интерфейс Искардаус можно использовать для предоставления служб проверки подлинности, поддерживаемых смарт-картой.
ms.assetid: 6b8a5b90-49ad-48fd-813c-c3c3337ec8f1
title: Интерфейс Искардаус
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardAuth
api_type:
- COM
api_location: ''
ms.openlocfilehash: bf8df3702aceb2ac8bbf5ad090802be2dc07e45a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104497295"
---
# <a name="iscardauth-interface"></a><span data-ttu-id="b837a-103">Интерфейс Искардаус</span><span class="sxs-lookup"><span data-stu-id="b837a-103">ISCardAuth interface</span></span>

<span data-ttu-id="b837a-104">\[Интерфейс **искардаус** доступен для использования в операционных системах, указанных в разделе требования.</span><span class="sxs-lookup"><span data-stu-id="b837a-104">\[The **ISCardAuth** interface is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="b837a-105">Он недоступен для использования в Windows Server 2003 с пакетом обновления 1 (SP1) и более поздней версии, Windows Vista, Windows Server 2008 и последующих версиях операционной системы.</span><span class="sxs-lookup"><span data-stu-id="b837a-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="b837a-106">[Модули смарт-карт](/previous-versions/windows/desktop/secsmart/smart-card-modules) предоставляют аналогичные функции.\]</span><span class="sxs-lookup"><span data-stu-id="b837a-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="b837a-107">Определение интерфейса **искардаус** предоставляется в качестве стандарта, который может быть выполнен при разработке [*поставщика услуг*](../secgloss/c-gly.md) [*смарт-карты*](../secgloss/s-gly.md) .</span><span class="sxs-lookup"><span data-stu-id="b837a-107">The **ISCardAuth** interface definition is provided as a standard that can be followed when developing a [*smart card*](../secgloss/s-gly.md) [*service provider*](../secgloss/c-gly.md).</span></span>

<span data-ttu-id="b837a-108">Интерфейс **искардаус** можно использовать для предоставления служб проверки подлинности, поддерживаемых смарт-картой.</span><span class="sxs-lookup"><span data-stu-id="b837a-108">The **ISCardAuth** interface can be used to expose authentication services supported by a smart card.</span></span> <span data-ttu-id="b837a-109">Эти службы включают проверку подлинности приложений, проверку подлинности смарт-карты и проверку подлинности пользователей.</span><span class="sxs-lookup"><span data-stu-id="b837a-109">These services include application authentication, smart card authentication, and user authentication.</span></span>

<span data-ttu-id="b837a-110">В следующем примере показано типичное использование интерфейса **искардаус** .</span><span class="sxs-lookup"><span data-stu-id="b837a-110">The following example shows a typical use of the **ISCardAuth** interface.</span></span>

<span data-ttu-id="b837a-111">**Использование Искардаус**</span><span class="sxs-lookup"><span data-stu-id="b837a-111">**To use ISCardAuth**</span></span>

1.  <span data-ttu-id="b837a-112">Создайте интерфейс **искардаус** (с помощью соответствующего метода интерфейса [**искардманаже**](iscardmanage.md) ).</span><span class="sxs-lookup"><span data-stu-id="b837a-112">Create an **ISCardAuth** interface (through the corresponding [**ISCardManage**](iscardmanage.md) interface method).</span></span>
2.  <span data-ttu-id="b837a-113">Вызовите соответствующий метод **искардаус** ([**\_ Проверка подлинности приложения**](iscardauth-app-auth.md), [**вызов**](iscardauth-getchallenge.md)функции, ICC- [**\_ Аутентификация**](iscardauth-icc-auth.md)или [**\_ Проверка**](iscardauth-user-auth.md)подлинности пользователя).</span><span class="sxs-lookup"><span data-stu-id="b837a-113">Call the appropriate **ISCardAuth** method ([**APP\_Auth**](iscardauth-app-auth.md), [**GetChallenge**](iscardauth-getchallenge.md), [**ICC\_Auth**](iscardauth-icc-auth.md), or [**User\_Auth**](iscardauth-user-auth.md)).</span></span>
3.  <span data-ttu-id="b837a-114">Освободите интерфейс **искардаус** .</span><span class="sxs-lookup"><span data-stu-id="b837a-114">Release the **ISCardAuth** interface.</span></span>

## <a name="members"></a><span data-ttu-id="b837a-115">Элементы</span><span class="sxs-lookup"><span data-stu-id="b837a-115">Members</span></span>

<span data-ttu-id="b837a-116">Интерфейс **искардаус** наследует от интерфейса [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) .</span><span class="sxs-lookup"><span data-stu-id="b837a-116">The **ISCardAuth** interface inherits from the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface.</span></span> <span data-ttu-id="b837a-117">**Искардаус** также имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="b837a-117">**ISCardAuth** also has these types of members:</span></span>

-   [<span data-ttu-id="b837a-118">Методы</span><span class="sxs-lookup"><span data-stu-id="b837a-118">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="b837a-119">Методы</span><span class="sxs-lookup"><span data-stu-id="b837a-119">Methods</span></span>

<span data-ttu-id="b837a-120">Интерфейс **искардаус** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="b837a-120">The **ISCardAuth** interface has these methods.</span></span>



| <span data-ttu-id="b837a-121">Метод</span><span class="sxs-lookup"><span data-stu-id="b837a-121">Method</span></span>                                          | <span data-ttu-id="b837a-122">Описание</span><span class="sxs-lookup"><span data-stu-id="b837a-122">Description</span></span>                                                                                    |
|:------------------------------------------------|:-----------------------------------------------------------------------------------------------|
| [<span data-ttu-id="b837a-123">**\_Проверка подлинности приложения**</span><span class="sxs-lookup"><span data-stu-id="b837a-123">**APP\_Auth**</span></span>](iscardauth-app-auth.md)        | <span data-ttu-id="b837a-124">Позволяет приложению проходить проверку подлинности с помощью протокола запроса или подписи.</span><span class="sxs-lookup"><span data-stu-id="b837a-124">Allows the application to authenticate itself using a challenge/signature protocol.</span></span><br/> |
| [<span data-ttu-id="b837a-125">**Вызов**</span><span class="sxs-lookup"><span data-stu-id="b837a-125">**GetChallenge**</span></span>](iscardauth-getchallenge.md) | <span data-ttu-id="b837a-126">Возвращает запрос со смарт-карты.</span><span class="sxs-lookup"><span data-stu-id="b837a-126">Returns a challenge from the smart card.</span></span><br/>                                            |
| [<span data-ttu-id="b837a-127">**\_Проверка подлинности ICC**</span><span class="sxs-lookup"><span data-stu-id="b837a-127">**ICC\_Auth**</span></span>](iscardauth-icc-auth.md)        | <span data-ttu-id="b837a-128">Позволяет приложению проверять подлинность смарт-карты.</span><span class="sxs-lookup"><span data-stu-id="b837a-128">Allows an application to authenticate the smart card.</span></span><br/>                               |
| [<span data-ttu-id="b837a-129">**\_Проверка подлинности пользователя**</span><span class="sxs-lookup"><span data-stu-id="b837a-129">**User\_Auth**</span></span>](iscardauth-user-auth.md)      | <span data-ttu-id="b837a-130">Разрешает доступ к службам проверки подлинности пользователей.</span><span class="sxs-lookup"><span data-stu-id="b837a-130">Allows access to user authentication services.</span></span><br/>                                      |



 

## <a name="requirements"></a><span data-ttu-id="b837a-131">Требования</span><span class="sxs-lookup"><span data-stu-id="b837a-131">Requirements</span></span>



| <span data-ttu-id="b837a-132">Требование</span><span class="sxs-lookup"><span data-stu-id="b837a-132">Requirement</span></span> | <span data-ttu-id="b837a-133">Значение</span><span class="sxs-lookup"><span data-stu-id="b837a-133">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="b837a-134">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="b837a-134">Minimum supported client</span></span><br/> | <span data-ttu-id="b837a-135">Только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="b837a-135">Windows XP \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="b837a-136">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="b837a-136">Minimum supported server</span></span><br/> | <span data-ttu-id="b837a-137">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="b837a-137">Windows Server 2003 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="b837a-138">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="b837a-138">End of client support</span></span><br/>    | <span data-ttu-id="b837a-139">Windows XP</span><span class="sxs-lookup"><span data-stu-id="b837a-139">Windows XP</span></span><br/>                                |
| <span data-ttu-id="b837a-140">Поддержка конца сервера</span><span class="sxs-lookup"><span data-stu-id="b837a-140">End of server support</span></span><br/>    | <span data-ttu-id="b837a-141">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="b837a-141">Windows Server 2003</span></span><br/>                       |



 

 
