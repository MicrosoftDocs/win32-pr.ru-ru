---
description: Предоставляет службы для настройки кода ЧВ (проверки держателя карты) и проверки пользователя.
ms.assetid: fa40c21c-1584-475e-89f6-f81f67e3b942
title: Интерфейс Искардверифи
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardVerify
api_type:
- COM
api_location: ''
ms.openlocfilehash: f929028f96faaab6ddb03538e854db01196ae180
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103814377"
---
# <a name="iscardverify-interface"></a><span data-ttu-id="d4044-103">Интерфейс Искардверифи</span><span class="sxs-lookup"><span data-stu-id="d4044-103">ISCardVerify interface</span></span>

<span data-ttu-id="d4044-104">\[Интерфейс **искардверифи** доступен для использования в операционных системах, указанных в разделе требования.</span><span class="sxs-lookup"><span data-stu-id="d4044-104">\[The **ISCardVerify** interface is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="d4044-105">Он недоступен для использования в Windows Server 2003 с пакетом обновления 1 (SP1) и более поздней версии, Windows Vista, Windows Server 2008 и последующих версиях операционной системы.</span><span class="sxs-lookup"><span data-stu-id="d4044-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="d4044-106">[Модули смарт-карт](/previous-versions/windows/desktop/secsmart/smart-card-modules) предоставляют аналогичные функции.\]</span><span class="sxs-lookup"><span data-stu-id="d4044-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="d4044-107">Следующее определение интерфейса предоставляется в качестве стандарта, который может быть выполнен при разработке [*поставщика услуг*](../secgloss/c-gly.md) [*смарт-карты*](../secgloss/s-gly.md) .</span><span class="sxs-lookup"><span data-stu-id="d4044-107">The following interface definition is provided as a standard that can be followed when developing a [*smart card*](../secgloss/s-gly.md) [*service provider*](../secgloss/c-gly.md).</span></span> <span data-ttu-id="d4044-108">Интерфейс **искардверифи** предоставляет службы для настройки кода ЧВ (проверки держателя карты) и проверки пользователя.</span><span class="sxs-lookup"><span data-stu-id="d4044-108">The **ISCardVerify** interface provides services for setting CHV (card holder verification) code and for verifying the user.</span></span>

<span data-ttu-id="d4044-109">Класс **искардверифи** определен для приложений, которые реализуют политику ЧВ для конкретного приложения, и имеют подробные сведения о внутренней реализации смарт-карты.</span><span class="sxs-lookup"><span data-stu-id="d4044-109">The **ISCardVerify** class is defined for applications that implement application-specific CHV policy, and that have a detailed knowledge of the smart card's internal implementation.</span></span>

<span data-ttu-id="d4044-110">Ниже приведен типичный пример использования интерфейса **искардверифи** .</span><span class="sxs-lookup"><span data-stu-id="d4044-110">Following is a typical use of the **ISCardVerify** interface.</span></span>

<span data-ttu-id="d4044-111">В следующей процедуре для изменения кода ЧВ используется **искардверифи** .</span><span class="sxs-lookup"><span data-stu-id="d4044-111">The following procedure uses **ISCardVerify** to change the CHV code.</span></span>

<span data-ttu-id="d4044-112">**Изменение кода ЧВ смарт-карты**</span><span class="sxs-lookup"><span data-stu-id="d4044-112">**To change the CHV code of a smart card**</span></span>

1.  <span data-ttu-id="d4044-113">Создайте интерфейс **искардверифи** (с помощью соответствующего метода интерфейса [**искардманаже**](iscardmanage.md) ).</span><span class="sxs-lookup"><span data-stu-id="d4044-113">Create an **ISCardVerify** interface (through the corresponding [**ISCardManage**](iscardmanage.md) interface method).</span></span>
2.  <span data-ttu-id="d4044-114">Вызовите метод [**чанжекоде**](iscardverify-changecode.md) и предоставьте новый код, указав, является ли он локальным или глобальным, и если он включен или отключен.</span><span class="sxs-lookup"><span data-stu-id="d4044-114">Call the [**ChangeCode**](iscardverify-changecode.md) method and provide new code, specifying if it is local or global and if it is enabled or disabled.</span></span>
3.  <span data-ttu-id="d4044-115">Освободите интерфейс **искардверифи** .</span><span class="sxs-lookup"><span data-stu-id="d4044-115">Release the **ISCardVerify** interface.</span></span>

## <a name="members"></a><span data-ttu-id="d4044-116">Элементы</span><span class="sxs-lookup"><span data-stu-id="d4044-116">Members</span></span>

<span data-ttu-id="d4044-117">Интерфейс **искардверифи** наследует от интерфейса [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) .</span><span class="sxs-lookup"><span data-stu-id="d4044-117">The **ISCardVerify** interface inherits from the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface.</span></span> <span data-ttu-id="d4044-118">**Искардверифи** также имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="d4044-118">**ISCardVerify** also has these types of members:</span></span>

-   [<span data-ttu-id="d4044-119">Методы</span><span class="sxs-lookup"><span data-stu-id="d4044-119">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="d4044-120">Методы</span><span class="sxs-lookup"><span data-stu-id="d4044-120">Methods</span></span>

<span data-ttu-id="d4044-121">Интерфейс **искардверифи** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="d4044-121">The **ISCardVerify** interface has these methods.</span></span>



| <span data-ttu-id="d4044-122">Метод</span><span class="sxs-lookup"><span data-stu-id="d4044-122">Method</span></span>                                                        | <span data-ttu-id="d4044-123">Описание</span><span class="sxs-lookup"><span data-stu-id="d4044-123">Description</span></span>                                                                                                                                 |
|:--------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="d4044-124">**чанжекоде**</span><span class="sxs-lookup"><span data-stu-id="d4044-124">**ChangeCode**</span></span>](iscardverify-changecode.md)                 | <span data-ttu-id="d4044-125">Изменяет текущий код ЧВ.</span><span class="sxs-lookup"><span data-stu-id="d4044-125">Changes the current CHV code.</span></span><br/>                                                                                                    |
| [<span data-ttu-id="d4044-126">**ресетсекуритистате**</span><span class="sxs-lookup"><span data-stu-id="d4044-126">**ResetSecurityState**</span></span>](iscardverify-resetsecuritystate.md) | <span data-ttu-id="d4044-127">Сбрасывает [*контекст безопасности*](../secgloss/s-gly.md) смарт-карты.</span><span class="sxs-lookup"><span data-stu-id="d4044-127">Resets the [*security context*](../secgloss/s-gly.md) of the smart card.</span></span><br/> |
| <span data-ttu-id="d4044-128">[**Внести**](/previous-versions/windows/desktop/legacy/aa377269(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="d4044-128">[**Unblock**](/previous-versions/windows/desktop/legacy/aa377269(v=vs.85))</span></span>                       | <span data-ttu-id="d4044-129">Повторно включает [*контекст безопасности*](../secgloss/s-gly.md).</span><span class="sxs-lookup"><span data-stu-id="d4044-129">Re-enables the [*security context*](../secgloss/s-gly.md).</span></span><br/>               |
| [<span data-ttu-id="d4044-130">**Проверка**</span><span class="sxs-lookup"><span data-stu-id="d4044-130">**Verify**</span></span>](iscardverify-verify.md)                         | <span data-ttu-id="d4044-131">Проверяет подлинность пользователя.</span><span class="sxs-lookup"><span data-stu-id="d4044-131">Authenticates the user.</span></span><br/>                                                                                                          |



 

## <a name="requirements"></a><span data-ttu-id="d4044-132">Требования</span><span class="sxs-lookup"><span data-stu-id="d4044-132">Requirements</span></span>



| <span data-ttu-id="d4044-133">Требование</span><span class="sxs-lookup"><span data-stu-id="d4044-133">Requirement</span></span> | <span data-ttu-id="d4044-134">Значение</span><span class="sxs-lookup"><span data-stu-id="d4044-134">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="d4044-135">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="d4044-135">Minimum supported client</span></span><br/> | <span data-ttu-id="d4044-136">Только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="d4044-136">Windows XP \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="d4044-137">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="d4044-137">Minimum supported server</span></span><br/> | <span data-ttu-id="d4044-138">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="d4044-138">Windows Server 2003 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="d4044-139">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="d4044-139">End of client support</span></span><br/>    | <span data-ttu-id="d4044-140">Windows XP</span><span class="sxs-lookup"><span data-stu-id="d4044-140">Windows XP</span></span><br/>                                |
| <span data-ttu-id="d4044-141">Поддержка конца сервера</span><span class="sxs-lookup"><span data-stu-id="d4044-141">End of server support</span></span><br/>    | <span data-ttu-id="d4044-142">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="d4044-142">Windows Server 2003</span></span><br/>                       |



 

 
