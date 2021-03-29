---
description: Интерфейс Искардлокате предоставляет службы для поиска смарт-карты по ее имени.
ms.assetid: add00705-69d5-4562-a74f-94c6864f6bd8
title: Интерфейс Искардлокате (Скардмгр. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardLocate
- ISCardLocate.ConfigureCardGuidSearch
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: e65a8315e796db032dfa6e9cb8898d19437bad05
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105647436"
---
# <a name="iscardlocate-interface"></a><span data-ttu-id="60aad-103">Интерфейс Искардлокате</span><span class="sxs-lookup"><span data-stu-id="60aad-103">ISCardLocate interface</span></span>

<span data-ttu-id="60aad-104">\[Интерфейс **искардлокате** доступен для использования в операционных системах, указанных в разделе требования.</span><span class="sxs-lookup"><span data-stu-id="60aad-104">\[The **ISCardLocate** interface is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="60aad-105">Он недоступен для использования в Windows Server 2003 с пакетом обновления 1 (SP1) и более поздней версии, Windows Vista, Windows Server 2008 и последующих версиях операционной системы.</span><span class="sxs-lookup"><span data-stu-id="60aad-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="60aad-106">[Модули смарт-карт](/previous-versions/windows/desktop/secsmart/smart-card-modules) предоставляют аналогичные функции.\]</span><span class="sxs-lookup"><span data-stu-id="60aad-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="60aad-107">Интерфейс **искардлокате** предоставляет службы для поиска [*смарт-карты*](../secgloss/s-gly.md) по ее имени.</span><span class="sxs-lookup"><span data-stu-id="60aad-107">The **ISCardLocate** interface provides services for locating a [*smart card*](../secgloss/s-gly.md) by its name.</span></span>

<span data-ttu-id="60aad-108">При необходимости этот интерфейс может отображать [*Пользовательский интерфейс*](../secgloss/u-gly.md) смарт-карты.</span><span class="sxs-lookup"><span data-stu-id="60aad-108">This interface can display the smart card [*user interface*](../secgloss/u-gly.md) if it is required.</span></span>

<span data-ttu-id="60aad-109">В следующем сценарии показано типичное использование интерфейса **искардлокате** .</span><span class="sxs-lookup"><span data-stu-id="60aad-109">The following scenario shows a typical use of the **ISCardLocate** interface.</span></span> <span data-ttu-id="60aad-110">Интерфейс **искардлокате** используется для создания [*блока данных протокола приложения*](../secgloss/a-gly.md) (категориях APDU).</span><span class="sxs-lookup"><span data-stu-id="60aad-110">The **ISCardLocate** interface is used to build an [*application protocol data unit*](../secgloss/a-gly.md) (APDU).</span></span>

<span data-ttu-id="60aad-111">**Определение местоположения конкретной карточки по ее имени**</span><span class="sxs-lookup"><span data-stu-id="60aad-111">**To locate a specific card using its name**</span></span>

1.  <span data-ttu-id="60aad-112">Создайте интерфейс **искардлокате** .</span><span class="sxs-lookup"><span data-stu-id="60aad-112">Create an **ISCardLocate** interface.</span></span>
2.  <span data-ttu-id="60aad-113">Вызовите [**конфигурекарднамесеарч**](iscardlocate-configurecardnamesearch.md) , чтобы найти имя смарт-карты.</span><span class="sxs-lookup"><span data-stu-id="60aad-113">Call [**ConfigureCardNameSearch**](iscardlocate-configurecardnamesearch.md) to search for a smart card name.</span></span>
3.  <span data-ttu-id="60aad-114">Вызовите [**финдкард**](iscardlocate-findcard.md) , чтобы найти смарт-карту.</span><span class="sxs-lookup"><span data-stu-id="60aad-114">Call [**FindCard**](iscardlocate-findcard.md) to search for the smart card.</span></span>
4.  <span data-ttu-id="60aad-115">Интерпретация результатов.</span><span class="sxs-lookup"><span data-stu-id="60aad-115">Interpret the results.</span></span>
5.  <span data-ttu-id="60aad-116">Освободите интерфейс **искардлокате** .</span><span class="sxs-lookup"><span data-stu-id="60aad-116">Release the **ISCardLocate** interface.</span></span>

## <a name="members"></a><span data-ttu-id="60aad-117">Элементы</span><span class="sxs-lookup"><span data-stu-id="60aad-117">Members</span></span>

<span data-ttu-id="60aad-118">Интерфейс **искардлокате** наследует от интерфейса [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) .</span><span class="sxs-lookup"><span data-stu-id="60aad-118">The **ISCardLocate** interface inherits from the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface.</span></span> <span data-ttu-id="60aad-119">**Искардлокате** также имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="60aad-119">**ISCardLocate** also has these types of members:</span></span>

-   [<span data-ttu-id="60aad-120">Методы</span><span class="sxs-lookup"><span data-stu-id="60aad-120">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="60aad-121">Методы</span><span class="sxs-lookup"><span data-stu-id="60aad-121">Methods</span></span>

<span data-ttu-id="60aad-122">Интерфейс **искардлокате** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="60aad-122">The **ISCardLocate** interface has these methods.</span></span>



| <span data-ttu-id="60aad-123">Метод</span><span class="sxs-lookup"><span data-stu-id="60aad-123">Method</span></span>                                                                  | <span data-ttu-id="60aad-124">Описание</span><span class="sxs-lookup"><span data-stu-id="60aad-124">Description</span></span>                                                                |
|:------------------------------------------------------------------------|:---------------------------------------------------------------------------|
| <span data-ttu-id="60aad-125">**конфигурекардгуидсеарч**</span><span class="sxs-lookup"><span data-stu-id="60aad-125">**ConfigureCardGuidSearch**</span></span>                                             | <span data-ttu-id="60aad-126">Зарезервировано для последующего использования.</span><span class="sxs-lookup"><span data-stu-id="60aad-126">Reserved for future use.</span></span><br/>                                        |
| [<span data-ttu-id="60aad-127">**конфигурекарднамесеарч**</span><span class="sxs-lookup"><span data-stu-id="60aad-127">**ConfigureCardNameSearch**</span></span>](iscardlocate-configurecardnamesearch.md) | <span data-ttu-id="60aad-128">Указывает имя карточки, которая будет использоваться при поиске.</span><span class="sxs-lookup"><span data-stu-id="60aad-128">Specifies the card name to be used in the search.</span></span><br/>               |
| [<span data-ttu-id="60aad-129">**финдкард**</span><span class="sxs-lookup"><span data-stu-id="60aad-129">**FindCard**</span></span>](iscardlocate-findcard.md)                               | <span data-ttu-id="60aad-130">Выполняет поиск смарт-карты и открывает для нее допустимое соединение.</span><span class="sxs-lookup"><span data-stu-id="60aad-130">Searches for the smart card and opens a valid connection to it.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="60aad-131">Требования</span><span class="sxs-lookup"><span data-stu-id="60aad-131">Requirements</span></span>



| <span data-ttu-id="60aad-132">Требование</span><span class="sxs-lookup"><span data-stu-id="60aad-132">Requirement</span></span> | <span data-ttu-id="60aad-133">Значение</span><span class="sxs-lookup"><span data-stu-id="60aad-133">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="60aad-134">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="60aad-134">Minimum supported client</span></span><br/> | <span data-ttu-id="60aad-135">Только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="60aad-135">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="60aad-136">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="60aad-136">Minimum supported server</span></span><br/> | <span data-ttu-id="60aad-137">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="60aad-137">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="60aad-138">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="60aad-138">End of client support</span></span><br/>    | <span data-ttu-id="60aad-139">Windows XP</span><span class="sxs-lookup"><span data-stu-id="60aad-139">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="60aad-140">Поддержка конца сервера</span><span class="sxs-lookup"><span data-stu-id="60aad-140">End of server support</span></span><br/>    | <span data-ttu-id="60aad-141">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="60aad-141">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="60aad-142">Header</span><span class="sxs-lookup"><span data-stu-id="60aad-142">Header</span></span><br/>                   | <dl> <span data-ttu-id="60aad-143"><dt>Скардмгр. h</dt></span><span class="sxs-lookup"><span data-stu-id="60aad-143"><dt>Scardmgr.h</dt></span></span> </dl>   |
| <span data-ttu-id="60aad-144">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="60aad-144">Type library</span></span><br/>             | <dl> <span data-ttu-id="60aad-145"><dt>Скардмгр. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="60aad-145"><dt>Scardmgr.tlb</dt></span></span> </dl> |
| <span data-ttu-id="60aad-146">DLL</span><span class="sxs-lookup"><span data-stu-id="60aad-146">DLL</span></span><br/>                      | <dl> <span data-ttu-id="60aad-147"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="60aad-147"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="60aad-148">IID</span><span class="sxs-lookup"><span data-stu-id="60aad-148">IID</span></span><br/>                      | <span data-ttu-id="60aad-149">IID \_ искардлокате определен как 1461AACD-6810-11D0-918F-00AA00C18068</span><span class="sxs-lookup"><span data-stu-id="60aad-149">IID\_ISCardLocate is defined as 1461AACD-6810-11D0-918F-00AA00C18068</span></span><br/>         |



 

 
