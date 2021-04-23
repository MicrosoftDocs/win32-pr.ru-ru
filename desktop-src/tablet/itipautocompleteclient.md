---
description: Позволяет клиенту вызывать объект поставщика автоматического завершения для панели ввода текста приложения.
ms.assetid: 448b8136-ebcb-4116-9a81-a77a37d69e24
title: Интерфейс Итипаутокомплетеклиент (Типаутокомплете. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITipAutocompleteClient
api_type:
- COM
api_location:
- tiptsf.dll
ms.openlocfilehash: 7b9dad38d0e3f169019934b7e60a09096aced1b9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105712975"
---
# <a name="itipautocompleteclient-interface"></a><span data-ttu-id="6f1f0-103">Интерфейс Итипаутокомплетеклиент</span><span class="sxs-lookup"><span data-stu-id="6f1f0-103">ITipAutocompleteClient interface</span></span>

<span data-ttu-id="6f1f0-104">Позволяет клиенту вызывать объект поставщика автоматического завершения для панели ввода текста приложения.</span><span class="sxs-lookup"><span data-stu-id="6f1f0-104">Enables the client to call the application's Text Input Panel auto complete provider object.</span></span>

## <a name="members"></a><span data-ttu-id="6f1f0-105">Элементы</span><span class="sxs-lookup"><span data-stu-id="6f1f0-105">Members</span></span>

<span data-ttu-id="6f1f0-106">Интерфейс **итипаутокомплетеклиент** наследует от интерфейса [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="6f1f0-106">The **ITipAutocompleteClient** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="6f1f0-107">**Итипаутокомплетеклиент** также имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="6f1f0-107">**ITipAutocompleteClient** also has these types of members:</span></span>

-   [<span data-ttu-id="6f1f0-108">Методы</span><span class="sxs-lookup"><span data-stu-id="6f1f0-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="6f1f0-109">Методы</span><span class="sxs-lookup"><span data-stu-id="6f1f0-109">Methods</span></span>

<span data-ttu-id="6f1f0-110">Интерфейс **итипаутокомплетеклиент** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="6f1f0-110">The **ITipAutocompleteClient** interface has these methods.</span></span>



| <span data-ttu-id="6f1f0-111">Метод</span><span class="sxs-lookup"><span data-stu-id="6f1f0-111">Method</span></span>                                                              | <span data-ttu-id="6f1f0-112">Описание</span><span class="sxs-lookup"><span data-stu-id="6f1f0-112">Description</span></span>                                                                                                                                                          |
|:--------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="6f1f0-113">**адвисепровидер**</span><span class="sxs-lookup"><span data-stu-id="6f1f0-113">**AdviseProvider**</span></span>](itipautocompleteclient-adviseprovider.md)     | <span data-ttu-id="6f1f0-114">Регистрирует поставщик в клиенте, чтобы позволить клиенту вызывать объект поставщика автозавершения приложения.</span><span class="sxs-lookup"><span data-stu-id="6f1f0-114">Registers the provider with the client to enable the client to call the application's auto complete provider object.</span></span><br/>                                      |
| [<span data-ttu-id="6f1f0-115">**преферредректс**</span><span class="sxs-lookup"><span data-stu-id="6f1f0-115">**PreferredRects**</span></span>](itipautocompleteclient-preferredrects.md)     | <span data-ttu-id="6f1f0-116">Позволяет клиенту предлагать место расположения списка автозавершения, чтобы избежать перекрытия панели ввода.</span><span class="sxs-lookup"><span data-stu-id="6f1f0-116">Allows the client to suggest where to position the auto complete list to avoid overlapping the Input Panel.</span></span><br/>                                               |
| [<span data-ttu-id="6f1f0-117">**рекуестшовуи**</span><span class="sxs-lookup"><span data-stu-id="6f1f0-117">**RequestShowUI**</span></span>](itipautocompleteclient-requestshowui.md)       | <span data-ttu-id="6f1f0-118">Определяет, готова ли панель ввода к отображению списка автозавершения.</span><span class="sxs-lookup"><span data-stu-id="6f1f0-118">Determines whether Input Panel is ready to have the auto complete list shown.</span></span><br/>                                                                             |
| [<span data-ttu-id="6f1f0-119">**унадвисепровидер**</span><span class="sxs-lookup"><span data-stu-id="6f1f0-119">**UnadviseProvider**</span></span>](itipautocompleteclient-unadviseprovider.md) | <span data-ttu-id="6f1f0-120">Отменяет регистрацию связанного поставщика.</span><span class="sxs-lookup"><span data-stu-id="6f1f0-120">Unregisters the associated provider.</span></span><br/>                                                                                                                      |
| [<span data-ttu-id="6f1f0-121">**усерселектион**</span><span class="sxs-lookup"><span data-stu-id="6f1f0-121">**UserSelection**</span></span>](itipautocompleteclient-userselection.md)       | <span data-ttu-id="6f1f0-122">Уведомляет панель ввода о том, что пользователь выбрал что-либо в списке автозавершения, и отбросить оставшийся текст, который еще не был вставлен.</span><span class="sxs-lookup"><span data-stu-id="6f1f0-122">Notifies the Input Panel that the user has selected something in the auto complete list and to discard all remaining text that has not yet been inserted.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="6f1f0-123">Требования</span><span class="sxs-lookup"><span data-stu-id="6f1f0-123">Requirements</span></span>



| <span data-ttu-id="6f1f0-124">Требование</span><span class="sxs-lookup"><span data-stu-id="6f1f0-124">Requirement</span></span> | <span data-ttu-id="6f1f0-125">Значение</span><span class="sxs-lookup"><span data-stu-id="6f1f0-125">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6f1f0-126">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="6f1f0-126">Minimum supported client</span></span><br/> | <span data-ttu-id="6f1f0-127">Только классические приложения Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="6f1f0-127">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                                   |
| <span data-ttu-id="6f1f0-128">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="6f1f0-128">Minimum supported server</span></span><br/> | <span data-ttu-id="6f1f0-129">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="6f1f0-129">None supported</span></span><br/>                                                                                                       |
| <span data-ttu-id="6f1f0-130">Header</span><span class="sxs-lookup"><span data-stu-id="6f1f0-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="6f1f0-131"><dt>Типаутокомплете. h (также требуется Пенинпутпанел \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="6f1f0-131"><dt>TipAutoComplete.h (also requires Peninputpanel\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="6f1f0-132">DLL</span><span class="sxs-lookup"><span data-stu-id="6f1f0-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6f1f0-133"><dt>Tiptsf.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6f1f0-133"><dt>Tiptsf.dll</dt></span></span> </dl>                                           |



 

