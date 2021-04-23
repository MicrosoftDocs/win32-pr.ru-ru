---
title: Объект WebViewFolderContents (Shldisp.h)
description: Реализуется оболочкой для использования внутри WebView.
ms.assetid: c9c46e21-2721-43c9-a6f4-38fafbda3798
keywords:
- Функции среды Windows для устаревших объектов Вебвиевфолдерконтентс
- Компоненты среды Windows для устаревших объектов Вебвиевфолдерконтентс, описание
topic_type:
- apiref
api_name:
- WebViewFolderContents
api_location:
- Shell32.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a9ea2020e2d9baaffbc026692faafc702db14781
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105710443"
---
# <a name="webviewfoldercontents-object"></a><span data-ttu-id="f3c16-105">Объект Вебвиевфолдерконтентс</span><span class="sxs-lookup"><span data-stu-id="f3c16-105">WebViewFolderContents object</span></span>

<span data-ttu-id="f3c16-106">Реализуется оболочкой для использования внутри *WebView*.</span><span class="sxs-lookup"><span data-stu-id="f3c16-106">Implemented by the Shell for use inside a *WebView*.</span></span> <span data-ttu-id="f3c16-107">**Вебвиевфолдерконтентс** автоматически инициализирует себя в текущей папке WebView.</span><span class="sxs-lookup"><span data-stu-id="f3c16-107">**WebViewFolderContents** automatically initializes itself to WebView's current folder.</span></span> <span data-ttu-id="f3c16-108">Он создает представление папки оболочки, которое отображает содержимое папки в одном из пяти форматов: мелкий значок, крупный значок, список, сведения или эскиз.</span><span class="sxs-lookup"><span data-stu-id="f3c16-108">It creates a Shell folder view that displays the contents of the folder in one of five formats: Small Icon, Large Icon, List, Details, or Thumbnail.</span></span> <span data-ttu-id="f3c16-109">Он не является допустимым за пределами WebView.</span><span class="sxs-lookup"><span data-stu-id="f3c16-109">It is not valid outside of a WebView.</span></span>

<span data-ttu-id="f3c16-110">Методы и свойства, предоставляемые **вебвиевфолдерконтентс** , идентичны параметрам объекта [**шеллфолдервиев**](/windows/desktop/shell/shellfolderview) .</span><span class="sxs-lookup"><span data-stu-id="f3c16-110">The methods and properties exposed by **WebViewFolderContents** are identical to those of the [**ShellFolderView**](/windows/desktop/shell/shellfolderview) object.</span></span>

## <a name="members"></a><span data-ttu-id="f3c16-111">Элементы</span><span class="sxs-lookup"><span data-stu-id="f3c16-111">Members</span></span>

<span data-ttu-id="f3c16-112">Объект **вебвиевфолдерконтентс** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="f3c16-112">The **WebViewFolderContents** object has these types of members:</span></span>

-   [<span data-ttu-id="f3c16-113">События</span><span class="sxs-lookup"><span data-stu-id="f3c16-113">Events</span></span>](#events)
-   [<span data-ttu-id="f3c16-114">Методы</span><span class="sxs-lookup"><span data-stu-id="f3c16-114">Methods</span></span>](#methods)
-   [<span data-ttu-id="f3c16-115">Свойства</span><span class="sxs-lookup"><span data-stu-id="f3c16-115">Properties</span></span>](#properties)

### <a name="events"></a><span data-ttu-id="f3c16-116">События</span><span class="sxs-lookup"><span data-stu-id="f3c16-116">Events</span></span>

<span data-ttu-id="f3c16-117">Объект **вебвиевфолдерконтентс** содержит эти события.</span><span class="sxs-lookup"><span data-stu-id="f3c16-117">The **WebViewFolderContents** object has these events.</span></span>



| <span data-ttu-id="f3c16-118">Событие</span><span class="sxs-lookup"><span data-stu-id="f3c16-118">Event</span></span>                                                              | <span data-ttu-id="f3c16-119">Описание</span><span class="sxs-lookup"><span data-stu-id="f3c16-119">Description</span></span>                                                                              |
|:-------------------------------------------------------------------|:-----------------------------------------------------------------------------------------|
| [<span data-ttu-id="f3c16-120">**SelectionChanged**</span><span class="sxs-lookup"><span data-stu-id="f3c16-120">**SelectionChanged**</span></span>](webviewfoldercontents-selectionchanged.md) | <span data-ttu-id="f3c16-121">Происходит при изменении состояния выбора любого элемента или элементов в представлении.</span><span class="sxs-lookup"><span data-stu-id="f3c16-121">Occurs when the selection state of any item or items in the view has changed.</span></span><br/> |



 

### <a name="methods"></a><span data-ttu-id="f3c16-122">Методы</span><span class="sxs-lookup"><span data-stu-id="f3c16-122">Methods</span></span>

<span data-ttu-id="f3c16-123">Объект **вебвиевфолдерконтентс** содержит эти методы.</span><span class="sxs-lookup"><span data-stu-id="f3c16-123">The **WebViewFolderContents** object has these methods.</span></span>



| <span data-ttu-id="f3c16-124">Метод</span><span class="sxs-lookup"><span data-stu-id="f3c16-124">Method</span></span>                                                       | <span data-ttu-id="f3c16-125">Описание</span><span class="sxs-lookup"><span data-stu-id="f3c16-125">Description</span></span>                                                                                                          |
|:-------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="f3c16-126">**попупитеммену**</span><span class="sxs-lookup"><span data-stu-id="f3c16-126">**PopupItemMenu**</span></span>](webviewfoldercontents-popupitemmenu.md) | <span data-ttu-id="f3c16-127">Создает контекстное меню для указанного элемента и возвращает выбранную командную строку.</span><span class="sxs-lookup"><span data-stu-id="f3c16-127">Creates a shortcut menu for the specified item and returns the selected command string.</span></span><br/>                   |
| [<span data-ttu-id="f3c16-128">**SelectedItems**</span><span class="sxs-lookup"><span data-stu-id="f3c16-128">**SelectedItems**</span></span>](webviewfoldercontents-selecteditems.md) | <span data-ttu-id="f3c16-129">Возвращает объект [**фолдеритемс**](../shell/folderitems.md) , представляющий все выбранные элементы в представлении.</span><span class="sxs-lookup"><span data-stu-id="f3c16-129">Gets a [**FolderItems**](../shell/folderitems.md) object that represents all of the selected items in the view.</span></span><br/> |
| [<span data-ttu-id="f3c16-130">**SelectItem**</span><span class="sxs-lookup"><span data-stu-id="f3c16-130">**SelectItem**</span></span>](webviewfoldercontents-selectitem.md)       | <span data-ttu-id="f3c16-131">Задает состояние выбора элемента в представлении.</span><span class="sxs-lookup"><span data-stu-id="f3c16-131">Sets the selection state of an item in the view.</span></span><br/>                                                          |



 

### <a name="properties"></a><span data-ttu-id="f3c16-132">Свойства</span><span class="sxs-lookup"><span data-stu-id="f3c16-132">Properties</span></span>

<span data-ttu-id="f3c16-133">Объект **вебвиевфолдерконтентс** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="f3c16-133">The **WebViewFolderContents** object has these properties.</span></span>



| <span data-ttu-id="f3c16-134">Свойство</span><span class="sxs-lookup"><span data-stu-id="f3c16-134">Property</span></span>                                                            | <span data-ttu-id="f3c16-135">Тип доступа</span><span class="sxs-lookup"><span data-stu-id="f3c16-135">Access type</span></span>          | <span data-ttu-id="f3c16-136">Описание</span><span class="sxs-lookup"><span data-stu-id="f3c16-136">Description</span></span>                                                                                                                              |
|:--------------------------------------------------------------------|:---------------------|:-----------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="f3c16-137">**Приложение**</span><span class="sxs-lookup"><span data-stu-id="f3c16-137">**Application**</span></span>](webviewfoldercontents-application.md)<br/> | <span data-ttu-id="f3c16-138">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="f3c16-138">Read-only</span></span><br/> | <span data-ttu-id="f3c16-139">Не реализован.</span><span class="sxs-lookup"><span data-stu-id="f3c16-139">Not implemented.</span></span><br/>                                                                                                              |
| [<span data-ttu-id="f3c16-140">**фокуседитем**</span><span class="sxs-lookup"><span data-stu-id="f3c16-140">**FocusedItem**</span></span>](webviewfoldercontents-focuseditem.md)<br/> | <span data-ttu-id="f3c16-141">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="f3c16-141">Read-only</span></span><br/> | <span data-ttu-id="f3c16-142">Возвращает объект [**FolderItem**](../shell/folderitem.md) , представляющий элемент, имеющий фокус ввода.</span><span class="sxs-lookup"><span data-stu-id="f3c16-142">Gets a [**FolderItem**](../shell/folderitem.md) object that represents the item that has the input focus.</span></span><br/>                           |
| [<span data-ttu-id="f3c16-143">**Folder**</span><span class="sxs-lookup"><span data-stu-id="f3c16-143">**Folder**</span></span>](webviewfoldercontents-folder.md)<br/>           | <span data-ttu-id="f3c16-144">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="f3c16-144">Read-only</span></span><br/> | <span data-ttu-id="f3c16-145">Возвращает объект [**Folder**](../shell/folder.md) , представляющий представление.</span><span class="sxs-lookup"><span data-stu-id="f3c16-145">Gets a [**Folder**](../shell/folder.md) object that represents the view.</span></span><br/>                                                            |
| [<span data-ttu-id="f3c16-146">**Parent**</span><span class="sxs-lookup"><span data-stu-id="f3c16-146">**Parent**</span></span>](webviewfoldercontents-parent.md)<br/>           | <span data-ttu-id="f3c16-147">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="f3c16-147">Read-only</span></span><br/> | <span data-ttu-id="f3c16-148">Не реализован.</span><span class="sxs-lookup"><span data-stu-id="f3c16-148">Not implemented.</span></span><br/>                                                                                                              |
| [<span data-ttu-id="f3c16-149">**Скрипт**</span><span class="sxs-lookup"><span data-stu-id="f3c16-149">**Script**</span></span>](webviewfoldercontents-script.md)<br/>           | <span data-ttu-id="f3c16-150">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="f3c16-150">Read-only</span></span><br/> | <span data-ttu-id="f3c16-151">Возвращает объект скрипта для представления.</span><span class="sxs-lookup"><span data-stu-id="f3c16-151">Gets the scripting object for the view.</span></span><br/>                                                                                       |
| [<span data-ttu-id="f3c16-152">**виевоптионс**</span><span class="sxs-lookup"><span data-stu-id="f3c16-152">**ViewOptions**</span></span>](webviewfoldercontents-viewoptions.md)<br/> | <span data-ttu-id="f3c16-153">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="f3c16-153">Read-only</span></span><br/> | <span data-ttu-id="f3c16-154">Возвращает набор флагов [**шеллфолдервиевоптионс**](/windows/desktop/api/shldisp/ne-shldisp-shellfolderviewoptions) , которые указывают текущие параметры представления.</span><span class="sxs-lookup"><span data-stu-id="f3c16-154">Gets a set of [**ShellFolderViewOptions**](/windows/desktop/api/shldisp/ne-shldisp-shellfolderviewoptions) flags that indicate the current options of the view.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="f3c16-155">Требования</span><span class="sxs-lookup"><span data-stu-id="f3c16-155">Requirements</span></span>



| <span data-ttu-id="f3c16-156">Требование</span><span class="sxs-lookup"><span data-stu-id="f3c16-156">Requirement</span></span> | <span data-ttu-id="f3c16-157">Значение</span><span class="sxs-lookup"><span data-stu-id="f3c16-157">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f3c16-158">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="f3c16-158">Minimum supported client</span></span><br/> | <span data-ttu-id="f3c16-159">Windows 2000 Professional, только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="f3c16-159">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="f3c16-160">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="f3c16-160">Minimum supported server</span></span><br/> | <span data-ttu-id="f3c16-161">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="f3c16-161">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="f3c16-162">Заголовок</span><span class="sxs-lookup"><span data-stu-id="f3c16-162">Header</span></span><br/>                   | <dl> <span data-ttu-id="f3c16-163"><dt>Шлдисп. h</dt></span><span class="sxs-lookup"><span data-stu-id="f3c16-163"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="f3c16-164">IDL</span><span class="sxs-lookup"><span data-stu-id="f3c16-164">IDL</span></span><br/>                      | <dl> <span data-ttu-id="f3c16-165"><dt>Шлдисп. idl</dt></span><span class="sxs-lookup"><span data-stu-id="f3c16-165"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="f3c16-166">DLL</span><span class="sxs-lookup"><span data-stu-id="f3c16-166">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f3c16-167"><dt>Shell32.dll (версия 4,71 или более поздняя)</dt></span><span class="sxs-lookup"><span data-stu-id="f3c16-167"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

