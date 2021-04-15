---
description: Интерфейс Искарддатабасе предоставляет методы для выполнения операций с базой данных в диспетчере ресурсов смарт-карт.
ms.assetid: 56db3bc0-33c3-4b9c-a4a7-374fc491d8fd
title: Интерфейс Искарддатабасе (Скардмгр. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardDatabase
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 1ae74c813b4d95cc9d02694ca9edb5c030e4f342
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105647181"
---
# <a name="iscarddatabase-interface"></a><span data-ttu-id="9c9ab-103">Интерфейс Искарддатабасе</span><span class="sxs-lookup"><span data-stu-id="9c9ab-103">ISCardDatabase interface</span></span>

<span data-ttu-id="9c9ab-104">\[Интерфейс **искарддатабасе** доступен для использования в операционных системах, указанных в разделе требования.</span><span class="sxs-lookup"><span data-stu-id="9c9ab-104">\[The **ISCardDatabase** interface is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="9c9ab-105">Он недоступен для использования в Windows Server 2003 с пакетом обновления 1 (SP1) и более поздней версии, Windows Vista, Windows Server 2008 и последующих версиях операционной системы.</span><span class="sxs-lookup"><span data-stu-id="9c9ab-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="9c9ab-106">[Модули смарт-карт](/previous-versions/windows/desktop/secsmart/smart-card-modules) предоставляют аналогичные функции.\]</span><span class="sxs-lookup"><span data-stu-id="9c9ab-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="9c9ab-107">Интерфейс **искарддатабасе** предоставляет методы для выполнения операций с базой данных в [*диспетчере ресурсов*](../secgloss/r-gly.md) [*смарт-карт*](../secgloss/s-gly.md) .</span><span class="sxs-lookup"><span data-stu-id="9c9ab-107">The **ISCardDatabase** interface provides the methods for performing the [*smart card*](../secgloss/s-gly.md) [*resource manager's*](../secgloss/r-gly.md) database operations.</span></span> <span data-ttu-id="9c9ab-108">Эти операции включают в себя список известных смарт-карт, [*читателей*](../secgloss/r-gly.md)и групп читателей, а также получение интерфейсов, поддерживаемых смарт-картой и ее [*основным поставщиком услуг*](../secgloss/p-gly.md).</span><span class="sxs-lookup"><span data-stu-id="9c9ab-108">These operations include listing known smart cards, [*readers*](../secgloss/r-gly.md), and reader groups, plus retrieving the interfaces supported by a smart card and its [*primary service provider*](../secgloss/p-gly.md).</span></span>

> [!Note]  
> <span data-ttu-id="9c9ab-109">Идентификатор основного поставщика услуг — это GUID COM, который можно использовать для создания экземпляров и использования COM-объектов для конкретной карточки.</span><span class="sxs-lookup"><span data-stu-id="9c9ab-109">The identifier of the primary service provider is a COM GUID that can be used to instantiate and use the COM objects for a specific card.</span></span>

 

<span data-ttu-id="9c9ab-110">В следующем примере показано типичное использование интерфейса **искарддатабасе** .</span><span class="sxs-lookup"><span data-stu-id="9c9ab-110">The following example shows a typical use of the **ISCardDatabase** interface.</span></span> <span data-ttu-id="9c9ab-111">В этом случае интерфейс **искарддатабасе** используется для перечисления всех известных смарт-карт.</span><span class="sxs-lookup"><span data-stu-id="9c9ab-111">In this case, the **ISCardDatabase** interface is used to list all the known smart cards.</span></span>

<span data-ttu-id="9c9ab-112">**Отправка транзакции на определенную карточку**</span><span class="sxs-lookup"><span data-stu-id="9c9ab-112">**To submit a transaction to a specific card**</span></span>

1.  <span data-ttu-id="9c9ab-113">Создайте интерфейс **искарддатабасе** .</span><span class="sxs-lookup"><span data-stu-id="9c9ab-113">Create an **ISCardDatabase** interface.</span></span>
2.  <span data-ttu-id="9c9ab-114">Вызовите [**листкардс**](iscarddatabase-listcards.md) , чтобы получить все известные смарт-карты на основе [*строки ATR*](../secgloss/a-gly.md) или поддерживаемых ими интерфейсов.</span><span class="sxs-lookup"><span data-stu-id="9c9ab-114">Call [**ListCards**](iscarddatabase-listcards.md) to retrieve all the known smart cards based on an [*ATR string*](../secgloss/a-gly.md) or their supported interfaces.</span></span>
3.  <span data-ttu-id="9c9ab-115">Освободите интерфейс **искарддатабасе** .</span><span class="sxs-lookup"><span data-stu-id="9c9ab-115">Release the **ISCardDatabase** interface.</span></span>

## <a name="members"></a><span data-ttu-id="9c9ab-116">Элементы</span><span class="sxs-lookup"><span data-stu-id="9c9ab-116">Members</span></span>

<span data-ttu-id="9c9ab-117">Интерфейс **искарддатабасе** наследует от интерфейса [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) .</span><span class="sxs-lookup"><span data-stu-id="9c9ab-117">The **ISCardDatabase** interface inherits from the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface.</span></span> <span data-ttu-id="9c9ab-118">**Искарддатабасе** также имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="9c9ab-118">**ISCardDatabase** also has these types of members:</span></span>

-   [<span data-ttu-id="9c9ab-119">Методы</span><span class="sxs-lookup"><span data-stu-id="9c9ab-119">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="9c9ab-120">Методы</span><span class="sxs-lookup"><span data-stu-id="9c9ab-120">Methods</span></span>

<span data-ttu-id="9c9ab-121">Интерфейс **искарддатабасе** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="9c9ab-121">The **ISCardDatabase** interface has these methods.</span></span>



| <span data-ttu-id="9c9ab-122">Метод</span><span class="sxs-lookup"><span data-stu-id="9c9ab-122">Method</span></span>                                                          | <span data-ttu-id="9c9ab-123">Описание</span><span class="sxs-lookup"><span data-stu-id="9c9ab-123">Description</span></span>                                                                                                                                                                                      |
|:----------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="9c9ab-124">**жетпровидеркардид**</span><span class="sxs-lookup"><span data-stu-id="9c9ab-124">**GetProviderCardId**</span></span>](iscarddatabase-getprovidercardid.md)   | <span data-ttu-id="9c9ab-125">Получает идентификатор [*основного поставщика услуг*](../secgloss/p-gly.md) для конкретной смарт-карты.</span><span class="sxs-lookup"><span data-stu-id="9c9ab-125">Retrieves the identifier of the [*primary service provider*](../secgloss/p-gly.md) for a specific smart card.</span></span><br/> |
| [<span data-ttu-id="9c9ab-126">**листкардинтерфацес**</span><span class="sxs-lookup"><span data-stu-id="9c9ab-126">**ListCardInterfaces**</span></span>](iscarddatabase-listcardinterfaces.md) | <span data-ttu-id="9c9ab-127">Получает идентификаторы интерфейса (GUID) всех интерфейсов, поддерживаемых конкретной смарт-картой.</span><span class="sxs-lookup"><span data-stu-id="9c9ab-127">Retrieves the interface identifiers (GUIDs) of all the interfaces supported by a specific smart card.</span></span><br/>                                                                                 |
| [<span data-ttu-id="9c9ab-128">**ListCards**</span><span class="sxs-lookup"><span data-stu-id="9c9ab-128">**ListCards**</span></span>](iscarddatabase-listcards.md)                   | <span data-ttu-id="9c9ab-129">Извлекает все имена смарт-карт, соответствующие определенному набору идентификаторов интерфейсов (GUID) или [*строку ATR*](../secgloss/a-gly.md).</span><span class="sxs-lookup"><span data-stu-id="9c9ab-129">Retrieves all the smart card names that match a specific set of interface identifiers (GUIDs) or an [*ATR string*](../secgloss/a-gly.md).</span></span><br/> |
| [<span data-ttu-id="9c9ab-130">**листреадерграупс**</span><span class="sxs-lookup"><span data-stu-id="9c9ab-130">**ListReaderGroups**</span></span>](iscarddatabase-listreadergroups.md)     | <span data-ttu-id="9c9ab-131">Извлекает имена [*групп читателей*](../secgloss/r-gly.md) , о которых имеет база данных Resource Manager.</span><span class="sxs-lookup"><span data-stu-id="9c9ab-131">Retrieves the names of the [*reader groups*](../secgloss/r-gly.md) that the resource manager has knowledge of.</span></span><br/>                        |
| [<span data-ttu-id="9c9ab-132">**листреадерс**</span><span class="sxs-lookup"><span data-stu-id="9c9ab-132">**ListReaders**</span></span>](iscarddatabase-listreaders.md)               | <span data-ttu-id="9c9ab-133">Получите имена [*читателей*](../secgloss/r-gly.md) , для которых диспетчер ресурсов имеет свои знания.</span><span class="sxs-lookup"><span data-stu-id="9c9ab-133">Retrieve the names of the [*readers*](../secgloss/r-gly.md) of which the resource manager has knowledge.</span></span><br/>                                          |



 

## <a name="requirements"></a><span data-ttu-id="9c9ab-134">Требования</span><span class="sxs-lookup"><span data-stu-id="9c9ab-134">Requirements</span></span>



| <span data-ttu-id="9c9ab-135">Требование</span><span class="sxs-lookup"><span data-stu-id="9c9ab-135">Requirement</span></span> | <span data-ttu-id="9c9ab-136">Значение</span><span class="sxs-lookup"><span data-stu-id="9c9ab-136">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="9c9ab-137">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="9c9ab-137">Minimum supported client</span></span><br/> | <span data-ttu-id="9c9ab-138">Только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="9c9ab-138">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="9c9ab-139">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="9c9ab-139">Minimum supported server</span></span><br/> | <span data-ttu-id="9c9ab-140">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="9c9ab-140">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="9c9ab-141">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="9c9ab-141">End of client support</span></span><br/>    | <span data-ttu-id="9c9ab-142">Windows XP</span><span class="sxs-lookup"><span data-stu-id="9c9ab-142">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="9c9ab-143">Поддержка конца сервера</span><span class="sxs-lookup"><span data-stu-id="9c9ab-143">End of server support</span></span><br/>    | <span data-ttu-id="9c9ab-144">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="9c9ab-144">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="9c9ab-145">Header</span><span class="sxs-lookup"><span data-stu-id="9c9ab-145">Header</span></span><br/>                   | <dl> <span data-ttu-id="9c9ab-146"><dt>Скардмгр. h</dt></span><span class="sxs-lookup"><span data-stu-id="9c9ab-146"><dt>Scardmgr.h</dt></span></span> </dl>   |
| <span data-ttu-id="9c9ab-147">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="9c9ab-147">Type library</span></span><br/>             | <dl> <span data-ttu-id="9c9ab-148"><dt>Скардмгр. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="9c9ab-148"><dt>Scardmgr.tlb</dt></span></span> </dl> |
| <span data-ttu-id="9c9ab-149">DLL</span><span class="sxs-lookup"><span data-stu-id="9c9ab-149">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9c9ab-150"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9c9ab-150"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="9c9ab-151">IID</span><span class="sxs-lookup"><span data-stu-id="9c9ab-151">IID</span></span><br/>                      | <span data-ttu-id="9c9ab-152">IID \_ искарддатабасе определен как 1461AAC8-6810-11D0-918F-00AA00C18068</span><span class="sxs-lookup"><span data-stu-id="9c9ab-152">IID\_ISCardDatabase is defined as 1461AAC8-6810-11D0-918F-00AA00C18068</span></span><br/>       |



 

 
