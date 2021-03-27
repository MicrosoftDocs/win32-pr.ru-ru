---
description: Некоторые из системных элементов, найденных на панели управления, являются расширяемыми. Чтобы установить расширение панели управления, зарегистрируйте расширение оболочки следующим образом, где name — это предопределенное имя системного элемента (см. таблицу ниже).
title: Расширение элементов панели управления "система"
ms.topic: article
ms.date: 05/31/2018
ms.assetid: b8b18b71-c95f-4c71-8df4-fe9342ce0165
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 9b0f6628d7bc75378915c1d9f3e20327478742df
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104997302"
---
# <a name="extending-system-control-panel-items"></a><span data-ttu-id="8822d-104">Расширение элементов панели управления "система"</span><span class="sxs-lookup"><span data-stu-id="8822d-104">Extending System Control Panel Items</span></span>

<span data-ttu-id="8822d-105">Некоторые из системных элементов, найденных на панели управления, являются расширяемыми.</span><span class="sxs-lookup"><span data-stu-id="8822d-105">Some of the system items found in the Control Panel are extensible.</span></span> <span data-ttu-id="8822d-106">Чтобы установить расширение панели управления, зарегистрируйте расширение оболочки следующим образом, где *Name* — это предопределенное имя системного элемента (см. таблицу ниже).</span><span class="sxs-lookup"><span data-stu-id="8822d-106">To install a Control Panel extension, register your Shell extension as follows, where *name* is the predefined name of the system item (see table below).</span></span>

```
HKEY_LOCAL_MACHINE
   Software
      Microsoft
         Windows
            CurrentVersion
               Controls Folder
                  name
                     shellex
                        PropertySheetHandlers
```

<span data-ttu-id="8822d-107">Это похоже на способ регистрации расширения для предопределенного объекта оболочки.</span><span class="sxs-lookup"><span data-stu-id="8822d-107">This is similar to the way you would register an extension for a predefined Shell object.</span></span> <span data-ttu-id="8822d-108">Поскольку единственными расширениями оболочки, поддерживаемыми элементами панели управления, являются страницы свойств, регистрация должна находиться в подразделе **шеллекс** \\ **пропертишисандлерс** .</span><span class="sxs-lookup"><span data-stu-id="8822d-108">Because the only Shell extensions supported by Control Panel items are property sheets, the registration must be under the **shellex**\\**PropertySheetHandlers** subkey.</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="8822d-109">Элемент панели управления</span><span class="sxs-lookup"><span data-stu-id="8822d-109">Control Panel item</span></span></th>
<th><span data-ttu-id="8822d-110"><em>name</em></span><span class="sxs-lookup"><span data-stu-id="8822d-110"><em>name</em></span></span></th>
<th><span data-ttu-id="8822d-111">Примечания</span><span class="sxs-lookup"><span data-stu-id="8822d-111">Remarks</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="8822d-112">Отображение</span><span class="sxs-lookup"><span data-stu-id="8822d-112">Display</span></span></td>
<td><span data-ttu-id="8822d-113">Поддержки</span><span class="sxs-lookup"><span data-stu-id="8822d-113">Desk</span></span></td>
<td><span data-ttu-id="8822d-114">Также поддерживает замену страницы <strong>рабочего стола</strong> .</span><span class="sxs-lookup"><span data-stu-id="8822d-114">Also supports replacement of the <strong>Desktop</strong> page.</span></span>
<blockquote>
[!Note]<br />
<span data-ttu-id="8822d-115">В Windows Vista эта поддержка больше не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="8822d-115">This is no longer supported under Windows Vista.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8822d-116">Дополнительные параметры экрана</span><span class="sxs-lookup"><span data-stu-id="8822d-116">Display Settings Advanced</span></span></td>
<td><span data-ttu-id="8822d-117">Устройство</span><span class="sxs-lookup"><span data-stu-id="8822d-117">Device</span></span></td>
<td><span data-ttu-id="8822d-118">Дополнительные свойства, не зависящие от оборудования.</span><span class="sxs-lookup"><span data-stu-id="8822d-118">Nonhardware-specific advanced properties.</span></span>
<blockquote>
[!Note]<br />
<span data-ttu-id="8822d-119">В Windows Vista эта поддержка больше не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="8822d-119">This is no longer supported under Windows Vista.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="8822d-120">Дополнительные параметры экрана</span><span class="sxs-lookup"><span data-stu-id="8822d-120">Display Settings Advanced</span></span></td>
<td><span data-ttu-id="8822d-121">Отображение</span><span class="sxs-lookup"><span data-stu-id="8822d-121">Display</span></span></td>
<td><span data-ttu-id="8822d-122">Дополнительные свойства, относящиеся к оборудованию.</span><span class="sxs-lookup"><span data-stu-id="8822d-122">Hardware-specific advanced properties.</span></span>
<blockquote>
[!Note]<br />
<span data-ttu-id="8822d-123">В Windows Vista эта поддержка больше не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="8822d-123">This is no longer supported under Windows Vista.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8822d-124">Свойства браузера</span><span class="sxs-lookup"><span data-stu-id="8822d-124">Internet Options</span></span></td>
<td><span data-ttu-id="8822d-125">Интернет</span><span class="sxs-lookup"><span data-stu-id="8822d-125">Internet</span></span></td>
<td><span data-ttu-id="8822d-126">Максимальное число страниц расширения — 18.</span><span class="sxs-lookup"><span data-stu-id="8822d-126">The maximum number of extension pages is 18.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="8822d-127">Keyboard (Клавиатура)</span><span class="sxs-lookup"><span data-stu-id="8822d-127">Keyboard</span></span></td>
<td><span data-ttu-id="8822d-128">Keyboard (Клавиатура)</span><span class="sxs-lookup"><span data-stu-id="8822d-128">Keyboard</span></span></td>
<td><span data-ttu-id="8822d-129">Максимальное число страниц расширения — 30.</span><span class="sxs-lookup"><span data-stu-id="8822d-129">The maximum number of extension pages is 30.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8822d-130">Мышь</span><span class="sxs-lookup"><span data-stu-id="8822d-130">Mouse</span></span></td>
<td><span data-ttu-id="8822d-131">Мышь</span><span class="sxs-lookup"><span data-stu-id="8822d-131">Mouse</span></span></td>
<td><span data-ttu-id="8822d-132">Также поддерживает замену стандартных страниц.</span><span class="sxs-lookup"><span data-stu-id="8822d-132">Also supports replacement of standard pages.</span></span> <span data-ttu-id="8822d-133">Максимальное число страниц расширения — 8.</span><span class="sxs-lookup"><span data-stu-id="8822d-133">The maximum number of extension pages is 8.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="8822d-134">Параметры электропитания</span><span class="sxs-lookup"><span data-stu-id="8822d-134">Power Options</span></span></td>
<td><span data-ttu-id="8822d-135">Мощный</span><span class="sxs-lookup"><span data-stu-id="8822d-135">Power</span></span></td>
<td><span data-ttu-id="8822d-136">Максимальное число страниц, включая стандартные страницы, равно 18.</span><span class="sxs-lookup"><span data-stu-id="8822d-136">The maximum number of pages, including standard pages, is 18.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8822d-137">Система</span><span class="sxs-lookup"><span data-stu-id="8822d-137">System</span></span></td>
<td><span data-ttu-id="8822d-138">Система</span><span class="sxs-lookup"><span data-stu-id="8822d-138">System</span></span></td>
<td><span data-ttu-id="8822d-139">Максимальное число страниц расширения — 8.</span><span class="sxs-lookup"><span data-stu-id="8822d-139">The maximum number of extension pages is 8.</span></span>
<blockquote>
[!Note]<br />
<span data-ttu-id="8822d-140">В Windows Vista эта поддержка больше не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="8822d-140">This is no longer supported under Windows Vista.</span></span>
</blockquote>
<br/></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="8822d-141">Элемент **Установка и удаление программ** на панели управления Windows XP не является страницей свойств и поэтому не может быть расширен методами, обсуждаемыми здесь.</span><span class="sxs-lookup"><span data-stu-id="8822d-141">The **Add or Remove Programs** item in the Windows XP Control Panel is not a property sheet and therefore cannot be extended by the methods discussed here.</span></span> <span data-ttu-id="8822d-142">Вместо этого его содержимое получает издательы приложений.</span><span class="sxs-lookup"><span data-stu-id="8822d-142">Instead, its content is obtained from application publishers.</span></span> <span data-ttu-id="8822d-143">Дополнительные сведения о добавлении содержимого для **установки и удаления программ** см. в [**разделе иапппублишер**](/windows/desktop/api/Shappmgr/nn-shappmgr-iapppublisher), [**иенумпублишедаппс**](/windows/desktop/api/Shappmgr/nn-shappmgr-ienumpublishedapps)и [**ипублишедапп**](/windows/desktop/api/Shappmgr/nn-shappmgr-ipublishedapp).</span><span class="sxs-lookup"><span data-stu-id="8822d-143">For more information on adding content to **Add or Remove Programs**, see [**IAppPublisher**](/windows/desktop/api/Shappmgr/nn-shappmgr-iapppublisher), [**IEnumPublishedApps**](/windows/desktop/api/Shappmgr/nn-shappmgr-ienumpublishedapps), and [**IPublishedApp**](/windows/desktop/api/Shappmgr/nn-shappmgr-ipublishedapp).</span></span>

## <a name="related-topics"></a><span data-ttu-id="8822d-144">См. также</span><span class="sxs-lookup"><span data-stu-id="8822d-144">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8822d-145">Элементы панели управления</span><span class="sxs-lookup"><span data-stu-id="8822d-145">Control Panel Items</span></span>](control-panel-applications.md)
</dt> <dt>

[<span data-ttu-id="8822d-146">Руководство по работе пользователей</span><span class="sxs-lookup"><span data-stu-id="8822d-146">User Experience Guidelines</span></span>](user-experience-guidelines.md)
</dt> <dt>

[<span data-ttu-id="8822d-147">Регистрация элементов панели управления</span><span class="sxs-lookup"><span data-stu-id="8822d-147">Registering Control Panel Items</span></span>](registering-control-panel-items.md)
</dt> <dt>

[<span data-ttu-id="8822d-148">Использование Кплапплет</span><span class="sxs-lookup"><span data-stu-id="8822d-148">Using CPLApplet</span></span>](using-cplapplet.md)
</dt> <dt>

[<span data-ttu-id="8822d-149">Обработка сообщений в панели управления</span><span class="sxs-lookup"><span data-stu-id="8822d-149">Control Panel Message Processing</span></span>](message-processing.md)
</dt> <dt>

[<span data-ttu-id="8822d-150">Исполнение элементов панели управления</span><span class="sxs-lookup"><span data-stu-id="8822d-150">Executing Control Panel Items</span></span>](executing-control-panel-items.md)
</dt> <dt>

[<span data-ttu-id="8822d-151">Назначение категорий панели управления</span><span class="sxs-lookup"><span data-stu-id="8822d-151">Assigning Control Panel Categories</span></span>](assigning-control-panel-categories.md)
</dt> <dt>

[<span data-ttu-id="8822d-152">Создание ссылок на задачи с возможностью поиска для элемента панели управления</span><span class="sxs-lookup"><span data-stu-id="8822d-152">Creating Searchable Task Links for a Control Panel Item</span></span>](creating-searchable-task-links.md)
</dt> <dt>

[<span data-ttu-id="8822d-153">Доступ к панели управления в защищенном режиме в Windows Vista</span><span class="sxs-lookup"><span data-stu-id="8822d-153">Accessing the Control Panel in Safe Mode under Windows Vista</span></span>](accessing-the-cp-in-safe-mode-under-vista.md)
</dt> </dl>

 

 




