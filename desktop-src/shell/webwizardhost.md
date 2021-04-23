---
description: Предоставляет методы, позволяющие HTML-страницам, размещенным в расширении мастера, взаимодействовать с мастером.
ms.assetid: 7b3690dc-2007-43a0-80a3-4a68e3c8464d
title: Объект Вебвизардхост (Шлдисп. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WebWizardHost
api_type:
- COM
api_location:
- Shldisp.h
ms.openlocfilehash: 1fbaf53db11fda577e9e9c5384af5f7c62fe1944
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103998438"
---
# <a name="webwizardhost-object"></a><span data-ttu-id="a8ab8-103">Объект Вебвизардхост</span><span class="sxs-lookup"><span data-stu-id="a8ab8-103">WebWizardHost object</span></span>

<span data-ttu-id="a8ab8-104">Предоставляет методы, позволяющие HTML-страницам, размещенным в расширении мастера, взаимодействовать с мастером.</span><span class="sxs-lookup"><span data-stu-id="a8ab8-104">Exposes methods that enable HTML pages which are hosted in a wizard extension to communicate with the wizard.</span></span>

## <a name="members"></a><span data-ttu-id="a8ab8-105">Элементы</span><span class="sxs-lookup"><span data-stu-id="a8ab8-105">Members</span></span>

<span data-ttu-id="a8ab8-106">Объект **вебвизардхост** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="a8ab8-106">The **WebWizardHost** object has these types of members:</span></span>

-   [<span data-ttu-id="a8ab8-107">Методы</span><span class="sxs-lookup"><span data-stu-id="a8ab8-107">Methods</span></span>](#methods)
-   [<span data-ttu-id="a8ab8-108">Свойства</span><span class="sxs-lookup"><span data-stu-id="a8ab8-108">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="a8ab8-109">Методы</span><span class="sxs-lookup"><span data-stu-id="a8ab8-109">Methods</span></span>

<span data-ttu-id="a8ab8-110">Объект **вебвизардхост** содержит эти методы.</span><span class="sxs-lookup"><span data-stu-id="a8ab8-110">The **WebWizardHost** object has these methods.</span></span>



| <span data-ttu-id="a8ab8-111">Метод</span><span class="sxs-lookup"><span data-stu-id="a8ab8-111">Method</span></span>                                                      | <span data-ttu-id="a8ab8-112">Описание</span><span class="sxs-lookup"><span data-stu-id="a8ab8-112">Description</span></span>                                                                                                                                                                        |
|:------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="a8ab8-113">**Отменить**</span><span class="sxs-lookup"><span data-stu-id="a8ab8-113">**Cancel**</span></span>](iwebwizardhost-cancel.md)                     | <span data-ttu-id="a8ab8-114">Имитирует нажатие кнопки **"Отмена** ".</span><span class="sxs-lookup"><span data-stu-id="a8ab8-114">Simulates a **Cancel** button click.</span></span><br/>                                                                                                                                    |
| [<span data-ttu-id="a8ab8-115">**финалбакк**</span><span class="sxs-lookup"><span data-stu-id="a8ab8-115">**FinalBack**</span></span>](iwebwizardhost-finalback.md)               | <span data-ttu-id="a8ab8-116">Переход к странице на стороне клиента, непосредственно предшествующей странице, на которой размещены HTML-страницы на стороне сервера.</span><span class="sxs-lookup"><span data-stu-id="a8ab8-116">Navigates to the client-side page immediately preceding the page hosting the server-side HTML pages.</span></span><br/>                                                                    |
| [<span data-ttu-id="a8ab8-117">**финалнекст**</span><span class="sxs-lookup"><span data-stu-id="a8ab8-117">**FinalNext**</span></span>](iwebwizardhost-finalnext.md)               | <span data-ttu-id="a8ab8-118">Переход к странице мастера на стороне клиента, расположенной после страницы, на которой размещены HTML-страницы на стороне сервера, или завершение работы мастера при отсутствии дополнительных страниц на стороне клиента.</span><span class="sxs-lookup"><span data-stu-id="a8ab8-118">Navigates to the client-side wizard page that follows the page that hosts the server-side HTML pages, or finishes the wizard if there are no further client-side pages.</span></span><br/> |
| [<span data-ttu-id="a8ab8-119">**сесеадертекст**</span><span class="sxs-lookup"><span data-stu-id="a8ab8-119">**SetHeaderText**</span></span>](iwebwizardhost-setheadertext.md)       | <span data-ttu-id="a8ab8-120">Задает заголовок и подзаголовок, которые отображаются в заголовке мастера.</span><span class="sxs-lookup"><span data-stu-id="a8ab8-120">Sets the title and subtitle that appear in the wizard header.</span></span> <span data-ttu-id="a8ab8-121">В общем случае клиент отобразит заголовок над HTML и под заголовком окна.</span><span class="sxs-lookup"><span data-stu-id="a8ab8-121">In general, the client will display the header above the HTML and below the title bar.</span></span><br/>                    |
| [<span data-ttu-id="a8ab8-122">**сетвизардбуттонс**</span><span class="sxs-lookup"><span data-stu-id="a8ab8-122">**SetWizardButtons**</span></span>](iwebwizardhost-setwizardbuttons.md) | <span data-ttu-id="a8ab8-123">Обновляет кнопки **назад**, **Далее** и **Готово** в кадре мастера клиента.</span><span class="sxs-lookup"><span data-stu-id="a8ab8-123">Updates the **Back**, **Next**, and **Finish** buttons in the client's wizard frame.</span></span><br/>                                                                                    |



 

### <a name="properties"></a><span data-ttu-id="a8ab8-124">Свойства</span><span class="sxs-lookup"><span data-stu-id="a8ab8-124">Properties</span></span>

<span data-ttu-id="a8ab8-125">Объект **вебвизардхост** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="a8ab8-125">The **WebWizardHost** object has these properties.</span></span>



| <span data-ttu-id="a8ab8-126">Свойство</span><span class="sxs-lookup"><span data-stu-id="a8ab8-126">Property</span></span>                                               | <span data-ttu-id="a8ab8-127">Тип доступа</span><span class="sxs-lookup"><span data-stu-id="a8ab8-127">Access type</span></span>           | <span data-ttu-id="a8ab8-128">Описание</span><span class="sxs-lookup"><span data-stu-id="a8ab8-128">Description</span></span>                                              |
|:-------------------------------------------------------|:----------------------|:---------------------------------------------------------|
| [<span data-ttu-id="a8ab8-129">**Заголовок**</span><span class="sxs-lookup"><span data-stu-id="a8ab8-129">**Caption**</span></span>](iwebwizardhost-caption.md)<br/>   | <span data-ttu-id="a8ab8-130">Чтение/запись</span><span class="sxs-lookup"><span data-stu-id="a8ab8-130">Read/write</span></span><br/> | <span data-ttu-id="a8ab8-131">Не реализован.</span><span class="sxs-lookup"><span data-stu-id="a8ab8-131">Not implemented.</span></span><br/>                              |
| [<span data-ttu-id="a8ab8-132">**Свойство**</span><span class="sxs-lookup"><span data-stu-id="a8ab8-132">**Property**</span></span>](iwebwizardhost-property.md)<br/> | <span data-ttu-id="a8ab8-133">Чтение/запись</span><span class="sxs-lookup"><span data-stu-id="a8ab8-133">Read/write</span></span><br/> | <span data-ttu-id="a8ab8-134">Задает или получает текущее значение свойства.</span><span class="sxs-lookup"><span data-stu-id="a8ab8-134">Sets or retrieves a property's current value.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="a8ab8-135">Требования</span><span class="sxs-lookup"><span data-stu-id="a8ab8-135">Requirements</span></span>



| <span data-ttu-id="a8ab8-136">Требование</span><span class="sxs-lookup"><span data-stu-id="a8ab8-136">Requirement</span></span> | <span data-ttu-id="a8ab8-137">Значение</span><span class="sxs-lookup"><span data-stu-id="a8ab8-137">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="a8ab8-138">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="a8ab8-138">Minimum supported client</span></span><br/> | <span data-ttu-id="a8ab8-139">Только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="a8ab8-139">Windows XP \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="a8ab8-140">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="a8ab8-140">Minimum supported server</span></span><br/> | <span data-ttu-id="a8ab8-141">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="a8ab8-141">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="a8ab8-142">Header</span><span class="sxs-lookup"><span data-stu-id="a8ab8-142">Header</span></span><br/>                   | <dl> <span data-ttu-id="a8ab8-143"><dt>Шлдисп. h</dt></span><span class="sxs-lookup"><span data-stu-id="a8ab8-143"><dt>Shldisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="a8ab8-144">IDL</span><span class="sxs-lookup"><span data-stu-id="a8ab8-144">IDL</span></span><br/>                      | <dl> <span data-ttu-id="a8ab8-145"><dt>Шлдисп. idl</dt></span><span class="sxs-lookup"><span data-stu-id="a8ab8-145"><dt>Shldisp.idl</dt></span></span> </dl> |
| <span data-ttu-id="a8ab8-146">IID</span><span class="sxs-lookup"><span data-stu-id="a8ab8-146">IID</span></span><br/>                      | <span data-ttu-id="a8ab8-147">\_ВЕБВИЗАРДХОСТ CLSID</span><span class="sxs-lookup"><span data-stu-id="a8ab8-147">CLSID\_WebWizardHost</span></span><br/>                                                        |



 

 




