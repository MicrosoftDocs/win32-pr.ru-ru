---
description: Управляет стороны приложения для интеграции автоматического завершения автоматической сборки панели ввода текста.
ms.assetid: 02601258-d867-4c01-b094-bf9ff96d2f6e
title: Интерфейс Итипаутокомплетепровидер (Типаутокомплете. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITipAutocompleteProvider
api_type:
- COM
api_location:
- tiptsf.dll
ms.openlocfilehash: 3c300e2724ccabbc8388ef647f8f0145531cfc8d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105713061"
---
# <a name="itipautocompleteprovider-interface"></a><span data-ttu-id="2585e-103">Интерфейс Итипаутокомплетепровидер</span><span class="sxs-lookup"><span data-stu-id="2585e-103">ITipAutocompleteProvider interface</span></span>

<span data-ttu-id="2585e-104">Управляет стороны приложения для интеграции автоматического завершения автоматической сборки панели ввода текста.</span><span class="sxs-lookup"><span data-stu-id="2585e-104">Manages the application's side of the Text Input Panel auto complete integration.</span></span>

## <a name="members"></a><span data-ttu-id="2585e-105">Элементы</span><span class="sxs-lookup"><span data-stu-id="2585e-105">Members</span></span>

<span data-ttu-id="2585e-106">Интерфейс **итипаутокомплетепровидер** наследует от интерфейса [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="2585e-106">The **ITipAutocompleteProvider** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="2585e-107">**Итипаутокомплетепровидер** также имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="2585e-107">**ITipAutocompleteProvider** also has these types of members:</span></span>

-   [<span data-ttu-id="2585e-108">Методы</span><span class="sxs-lookup"><span data-stu-id="2585e-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="2585e-109">Методы</span><span class="sxs-lookup"><span data-stu-id="2585e-109">Methods</span></span>

<span data-ttu-id="2585e-110">Интерфейс **итипаутокомплетепровидер** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="2585e-110">The **ITipAutocompleteProvider** interface has these methods.</span></span>



| <span data-ttu-id="2585e-111">Метод</span><span class="sxs-lookup"><span data-stu-id="2585e-111">Method</span></span>                                                                  | <span data-ttu-id="2585e-112">Описание</span><span class="sxs-lookup"><span data-stu-id="2585e-112">Description</span></span>                                                                                                          |
|:------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="2585e-113">**Казывающи**</span><span class="sxs-lookup"><span data-stu-id="2585e-113">**Show**</span></span>](itipautocompleteprovider-show.md)                           | <span data-ttu-id="2585e-114">Отображает или скрывает список автозавершения.</span><span class="sxs-lookup"><span data-stu-id="2585e-114">Displays or hides the auto complete list.</span></span><br/>                                                                 |
| [<span data-ttu-id="2585e-115">**упдатепендингтекст**</span><span class="sxs-lookup"><span data-stu-id="2585e-115">**UpdatePendingText**</span></span>](itipautocompleteprovider-updatependingtext.md) | <span data-ttu-id="2585e-116">Используется клиентом автоматического завершения для уведомления приложения о тексте, которое пользователь направит на панель ввода.</span><span class="sxs-lookup"><span data-stu-id="2585e-116">Used by the auto complete client to notify the application of the text a user has inked into Input Panel.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="2585e-117">Требования</span><span class="sxs-lookup"><span data-stu-id="2585e-117">Requirements</span></span>



| <span data-ttu-id="2585e-118">Требование</span><span class="sxs-lookup"><span data-stu-id="2585e-118">Requirement</span></span> | <span data-ttu-id="2585e-119">Значение</span><span class="sxs-lookup"><span data-stu-id="2585e-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2585e-120">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="2585e-120">Minimum supported client</span></span><br/> | <span data-ttu-id="2585e-121">Только классические приложения Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="2585e-121">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                                   |
| <span data-ttu-id="2585e-122">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="2585e-122">Minimum supported server</span></span><br/> | <span data-ttu-id="2585e-123">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="2585e-123">None supported</span></span><br/>                                                                                                       |
| <span data-ttu-id="2585e-124">Header</span><span class="sxs-lookup"><span data-stu-id="2585e-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="2585e-125"><dt>Типаутокомплете. h (также требуется Пенинпутпанел \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="2585e-125"><dt>TipAutoComplete.h (also requires Peninputpanel\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="2585e-126">DLL</span><span class="sxs-lookup"><span data-stu-id="2585e-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2585e-127"><dt>Tiptsf.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2585e-127"><dt>Tiptsf.dll</dt></span></span> </dl>                                           |



## <a name="see-also"></a><span data-ttu-id="2585e-128">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="2585e-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2585e-129">Справочник по панели ввода текста</span><span class="sxs-lookup"><span data-stu-id="2585e-129">Text Input Panel Reference</span></span>](text-input-panel-reference.md)
</dt> <dt>

[<span data-ttu-id="2585e-130">**Интерфейс Итипаутокомплетеклиент**</span><span class="sxs-lookup"><span data-stu-id="2585e-130">**ITipAutocompleteClient Interface**</span></span>](itipautocompleteclient.md)
</dt> </dl>

 

