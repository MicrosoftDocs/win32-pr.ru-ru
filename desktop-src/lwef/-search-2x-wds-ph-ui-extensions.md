---
title: Добавление значков и контекстных меню с расширениями оболочки
description: Вы можете улучшить работу пользователей с помощью службы Microsoft Windows Desktop Search (WDS) и обработчика протокола, реализовав расширения оболочки.
ms.assetid: 899f3fd1-1ae9-45fe-ae6d-26d4f07bf6e4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: adbd6b0f4c647c47e11d14aea5e5af748a59ba53
ms.sourcegitcommit: b9a94cea8f83153214af4c09509e1cc61a1bb616
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/19/2020
ms.locfileid: "104260403"
---
# <a name="adding-icons-and-context-menus-with-shell-extensions"></a><span data-ttu-id="18ca7-103">Добавление значков и контекстных меню с расширениями оболочки</span><span class="sxs-lookup"><span data-stu-id="18ca7-103">Adding Icons and Context Menus with Shell Extensions</span></span>

> [!NOTE]
> <span data-ttu-id="18ca7-104">Windows Desktop Search 2. x — это устаревшая технология, которая изначально была доступна в качестве надстройки для Windows XP и Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="18ca7-104">Windows Desktop Search 2.x is an obsolete technology that was originally available as an add-in for Windows XP and Windows Server 2003.</span></span> <span data-ttu-id="18ca7-105">В более поздних выпусках используйте вместо этого [Поиск Windows](../search/-search-3x-wds-overview.md) .</span><span class="sxs-lookup"><span data-stu-id="18ca7-105">On later releases, use [Windows Search](../search/-search-3x-wds-overview.md) instead.</span></span>

<span data-ttu-id="18ca7-106">Вы можете улучшить работу пользователей с помощью службы Microsoft Windows Desktop Search (WDS) и обработчика протокола, реализовав расширения оболочки.</span><span class="sxs-lookup"><span data-stu-id="18ca7-106">You can improve your users' experience with Microsoft Windows Desktop Search (WDS) and your protocol handler by implementing Shell extensions.</span></span> <span data-ttu-id="18ca7-107">Без дополнительного расширения созданный обработчик протокола не будет включать следующие пользовательские интерфейсы:</span><span class="sxs-lookup"><span data-stu-id="18ca7-107">Without further extension, the protocol handler you create will not include the following user experiences:</span></span>

-   <span data-ttu-id="18ca7-108">WDS не будет отображать определенные значки для результатов.</span><span class="sxs-lookup"><span data-stu-id="18ca7-108">WDS will not display specific icons for your results.</span></span>
-   <span data-ttu-id="18ca7-109">Когда пользователь дважды щелкнул элемент, Пользовательский интерфейс не будет отвечать на событие.</span><span class="sxs-lookup"><span data-stu-id="18ca7-109">When users double-click an item, the user interface will not respond to the event.</span></span>
-   <span data-ttu-id="18ca7-110">Когда пользователь правой кнопкой мыши щелкнул элемент, контекстное меню не будет поддерживать никаких операций с элементом.</span><span class="sxs-lookup"><span data-stu-id="18ca7-110">When users right-click an item, the context menu will not support any operations for the item.</span></span>

<span data-ttu-id="18ca7-111">В **ишеллфолдер** требуются минимальные реализации **IPersist** и **иперсистфолдер** , а для **IContextMenu** и **иекстрактикон** требуется минимальная реализация **ишеллфолдер** . это два интерфейса, обеспечивающие более простой пользовательский интерфейс.</span><span class="sxs-lookup"><span data-stu-id="18ca7-111">Minimal implementations of **IPersist** and **IPersistFolder** are required by **IShellFolder**, and a minimal implementation of **IShellFolder** is required for **IContextMenu** and **IExtractIcon**, the two interfaces that provide a more seamless user experience.</span></span>

 

## <a name="ipersist"></a><span data-ttu-id="18ca7-112">IPersist</span><span class="sxs-lookup"><span data-stu-id="18ca7-112">IPersist</span></span>

<span data-ttu-id="18ca7-113">Интерфейс **IPersist** определяет единственный метод- **ClassID**, который предназначен для предоставления идентификатора CLSID объекта, который может храниться в системе постоянно.</span><span class="sxs-lookup"><span data-stu-id="18ca7-113">The **IPersist** interface defines the single method **GetClassID**, which is designed to supply the CLSID of an object that can be stored persistently in the system.</span></span>



| <span data-ttu-id="18ca7-114">Метод</span><span class="sxs-lookup"><span data-stu-id="18ca7-114">Method</span></span>       | <span data-ttu-id="18ca7-115">Описание</span><span class="sxs-lookup"><span data-stu-id="18ca7-115">Description</span></span>                                 |
|--------------|---------------------------------------------|
| <span data-ttu-id="18ca7-116">-ClassID ()</span><span class="sxs-lookup"><span data-stu-id="18ca7-116">GetClassID()</span></span> | <span data-ttu-id="18ca7-117">Возвращает идентификатор ClassID обработчика протокола.</span><span class="sxs-lookup"><span data-stu-id="18ca7-117">Returns the ClassID of the protocol handler</span></span> |



 

> [!Note]
>
> <span data-ttu-id="18ca7-118">Один и тот же CLSID должен быть реализован для **IPersist**, **иперсистфолдер** и **ишеллфолдер**.</span><span class="sxs-lookup"><span data-stu-id="18ca7-118">The same CLSID should be implemented for **IPersist**, **IPersistFolder** and **IShellFolder**.</span></span>

 

 

## <a name="ipersistfolder"></a><span data-ttu-id="18ca7-119">иперсистфолдер</span><span class="sxs-lookup"><span data-stu-id="18ca7-119">IPersistFolder</span></span>

<span data-ttu-id="18ca7-120">Интерфейс **иперсистфолдер** используется для инициализации объектов папки оболочки.</span><span class="sxs-lookup"><span data-stu-id="18ca7-120">The **IPersistFolder** interface is used to initialize Shell folder objects.</span></span> <span data-ttu-id="18ca7-121">Реализация этого интерфейса, производного от **IPersist**, заключается в том, как папка сообщается, где она находится в пространстве имен оболочки.</span><span class="sxs-lookup"><span data-stu-id="18ca7-121">Implementation of this interface, which is derived from **IPersist**, is how the folder is told where it is in the Shell namespace.</span></span>



| <span data-ttu-id="18ca7-122">Метод</span><span class="sxs-lookup"><span data-stu-id="18ca7-122">Method</span></span>       | <span data-ttu-id="18ca7-123">Описание</span><span class="sxs-lookup"><span data-stu-id="18ca7-123">Description</span></span>                                                                                            |
|--------------|--------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="18ca7-124">Initialize ()</span><span class="sxs-lookup"><span data-stu-id="18ca7-124">Initialize()</span></span> | <span data-ttu-id="18ca7-125">Указывает объекту папки оболочки инициализировать себя на основе переданных и возвратов \_ ОК</span><span class="sxs-lookup"><span data-stu-id="18ca7-125">Instructs a Shell folder object to initialize itself based on the information passed and returns S\_OK</span></span> |



 

> [!Note]
>
> <span data-ttu-id="18ca7-126">Один и тот же CLSID должен быть реализован для **IPersist**, **иперсистфолдер** и **ишеллфолдер**.</span><span class="sxs-lookup"><span data-stu-id="18ca7-126">The same CLSID should be implemented for **IPersist**, **IPersistFolder** and **IShellFolder**.</span></span>

 

<span data-ttu-id="18ca7-127">Этот интерфейс не используется напрямую.</span><span class="sxs-lookup"><span data-stu-id="18ca7-127">You do not use this interface directly.</span></span> <span data-ttu-id="18ca7-128">Он используется реализацией файловой системы интерфейса Ишеллфолдер:: Биндтубжект при инициализации объекта папки оболочки.</span><span class="sxs-lookup"><span data-stu-id="18ca7-128">It is used by the file system implementation of the IShellFolder::BindToObject interface when it initializes a Shell folder object.</span></span>

 

## <a name="ishellfolder"></a><span data-ttu-id="18ca7-129">ишеллфолдер</span><span class="sxs-lookup"><span data-stu-id="18ca7-129">IShellFolder</span></span>

<span data-ttu-id="18ca7-130">Интерфейс **ишеллфолдер** используется для управления папками, а частичная реализация необходима, чтобы интерфейсы значков и контекста, реализованные для обработчика протокола, были правильно работают в пользовательском интерфейсе "результаты поиска Windows Desktop".</span><span class="sxs-lookup"><span data-stu-id="18ca7-130">The **IShellFolder** interface is used to manage folders, and a partial implementation is required so that the icon and context interfaces implemented for a protocol handler will behave correctly in the Windows Desktop Search results user interface.</span></span> <span data-ttu-id="18ca7-131">Большинство необходимых функциональных возможностей предоставляется с помощью метода **жетуиобжектоф** .</span><span class="sxs-lookup"><span data-stu-id="18ca7-131">Most of the functionality required is exposed through the **GetUIObjectOf** method.</span></span> <span data-ttu-id="18ca7-132">Этот метод позволяет надстройке запрашивать интерфейсы **иекстрактикон** и **IContextMenu** .</span><span class="sxs-lookup"><span data-stu-id="18ca7-132">This method enables an add-in to query for the **IExtractIcon** and **IContextMenu** interfaces.</span></span>

<span data-ttu-id="18ca7-133">Интерфейс **ишеллфолдер** использует PIDL вместо URL-адресов.</span><span class="sxs-lookup"><span data-stu-id="18ca7-133">The **IShellFolder** interface uses PIDLs instead of URLs.</span></span> <span data-ttu-id="18ca7-134">В отличие от требований полного расширения пространства имен надстройки могут использовать простую структуру IDL, содержащую только URL-адрес.</span><span class="sxs-lookup"><span data-stu-id="18ca7-134">In contrast to the requirements of a complete Namespace extension, add-ins can use a simple IDL structure that contains only the URL.</span></span>

<span data-ttu-id="18ca7-135">Должны быть реализованы следующие методы **ишеллфолдер** .</span><span class="sxs-lookup"><span data-stu-id="18ca7-135">The following methods of **IShellFolder** must be implemented.</span></span> <span data-ttu-id="18ca7-136">Обратите внимание, что для пяти этих методов требуется минимальная реализация.</span><span class="sxs-lookup"><span data-stu-id="18ca7-136">Note that five of these methods require minimal implementation.</span></span>



| <span data-ttu-id="18ca7-137">Метод</span><span class="sxs-lookup"><span data-stu-id="18ca7-137">Method</span></span>             | <span data-ttu-id="18ca7-138">Описание</span><span class="sxs-lookup"><span data-stu-id="18ca7-138">Description</span></span>                                                                                                                                                                                                 |
|--------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="18ca7-139">Биндтубжект ()</span><span class="sxs-lookup"><span data-stu-id="18ca7-139">BindToObject()</span></span>     | <span data-ttu-id="18ca7-140">Возвращает E \_ нотимпл</span><span class="sxs-lookup"><span data-stu-id="18ca7-140">Returns E\_NOTIMPL</span></span>                                                                                                                                                                                          |
| <span data-ttu-id="18ca7-141">Биндтостораже ()</span><span class="sxs-lookup"><span data-stu-id="18ca7-141">BindToStorage()</span></span>    | <span data-ttu-id="18ca7-142">Возвращает E \_ нотимпл</span><span class="sxs-lookup"><span data-stu-id="18ca7-142">Returns E\_NOTIMPL</span></span>                                                                                                                                                                                          |
| <span data-ttu-id="18ca7-143">Креатевиевобжект ()</span><span class="sxs-lookup"><span data-stu-id="18ca7-143">CreateViewObject()</span></span> | <span data-ttu-id="18ca7-144">Возвращает E \_ нотимпл</span><span class="sxs-lookup"><span data-stu-id="18ca7-144">Returns E\_NOTIMPL</span></span>                                                                                                                                                                                          |
| <span data-ttu-id="18ca7-145">Сетнамеоф ()</span><span class="sxs-lookup"><span data-stu-id="18ca7-145">SetNameOf()</span></span>        | <span data-ttu-id="18ca7-146">Возвращает E \_ нотимпл</span><span class="sxs-lookup"><span data-stu-id="18ca7-146">Returns E\_NOTIMPL</span></span>                                                                                                                                                                                          |
| <span data-ttu-id="18ca7-147">Парседисплайнаме ()</span><span class="sxs-lookup"><span data-stu-id="18ca7-147">ParseDisplayName()</span></span> | <span data-ttu-id="18ca7-148">Преобразует URL-адрес в структуру ПИДЛ</span><span class="sxs-lookup"><span data-stu-id="18ca7-148">Converts a URL to the PIDL structure</span></span>                                                                                                                                                                        |
| <span data-ttu-id="18ca7-149">Компареидс ()</span><span class="sxs-lookup"><span data-stu-id="18ca7-149">CompareIDs()</span></span>       | <span data-ttu-id="18ca7-150">Сравнивает два значения ПИДЛ</span><span class="sxs-lookup"><span data-stu-id="18ca7-150">Compares two PIDL values</span></span>                                                                                                                                                                                    |
| <span data-ttu-id="18ca7-151">Жетдисплайнамеоф ()</span><span class="sxs-lookup"><span data-stu-id="18ca7-151">GetDisplayNameOf()</span></span> | <span data-ttu-id="18ca7-152">Возвращает URL-адрес для ПИДЛ</span><span class="sxs-lookup"><span data-stu-id="18ca7-152">Returns the URL for a PIDL</span></span>                                                                                                                                                                                  |
| <span data-ttu-id="18ca7-153">Жетуиобжектоф ()</span><span class="sxs-lookup"><span data-stu-id="18ca7-153">GetUIObjectOf()</span></span>    | <span data-ttu-id="18ca7-154">Этот метод аналогичен методу OLE COM QueryInterface.</span><span class="sxs-lookup"><span data-stu-id="18ca7-154">This method is similar to the OLE COM QueryInterface method.</span></span> <span data-ttu-id="18ca7-155">Если запрошен значок, вызывающий объект запрашивает IID \_ иекстрактикон; если контекстное меню запрашивается, вызывающий объект запрашивает идентификатор IID \_ IContextMenu.</span><span class="sxs-lookup"><span data-stu-id="18ca7-155">If an icon is requested, the caller requests the IID\_IExtractIcon; if a context menu is requested, the caller requests the IID\_IContextMenu.</span></span> |



 

> [!Note]
>
> <span data-ttu-id="18ca7-156">Один и тот же CLSID должен быть реализован для **IPersist**, **иперсистфолдер** и **ишеллфолдер**.</span><span class="sxs-lookup"><span data-stu-id="18ca7-156">The same CLSID should be implemented for **IPersist**, **IPersistFolder** and **IShellFolder**.</span></span>

 

<span data-ttu-id="18ca7-157">**Ишеллфолдер** не используется для перечисления папок.</span><span class="sxs-lookup"><span data-stu-id="18ca7-157">**IShellFolder** is not used to enumerate folders.</span></span> <span data-ttu-id="18ca7-158">Это означает, что отображаемое имя папки будет физическим URL-адресом.</span><span class="sxs-lookup"><span data-stu-id="18ca7-158">This means that the display name of a folder will be the physical URL.</span></span> <span data-ttu-id="18ca7-159">Это может измениться в будущем.</span><span class="sxs-lookup"><span data-stu-id="18ca7-159">This may change in the future.</span></span>

 

## <a name="icontextmenu"></a><span data-ttu-id="18ca7-160">IContextMenu</span><span class="sxs-lookup"><span data-stu-id="18ca7-160">IContextMenu</span></span>

<span data-ttu-id="18ca7-161">Когда WDS отображает результаты для пользователя, пользователь может щелкнуть правой кнопкой мыши элемент и просмотреть контекстное меню, определенное интерфейсом **IContextMenu** .</span><span class="sxs-lookup"><span data-stu-id="18ca7-161">When WDS displays results to the user, the user can right-click an item and see a context menu defined by your **IContextMenu** interface.</span></span>

<span data-ttu-id="18ca7-162">Действие по умолчанию в контекстном меню — это то же действие, которое предпринимается при двойном щелчке элемента.</span><span class="sxs-lookup"><span data-stu-id="18ca7-162">The default action on the context menu is the same action taken when the item is double-clicked.</span></span> <span data-ttu-id="18ca7-163">При отсутствии соответствующих интерфейсов **ишеллфолдер** или **IContextMenu** для элемента поведение по умолчанию для события двойного щелчка заключается в передаче URL-адреса в качестве аргумента функции ShellExecute.</span><span class="sxs-lookup"><span data-stu-id="18ca7-163">Without the corresponding **IShellFolder** or **IContextMenu** interfaces for the item, the default behavior for a double-click event is to pass the URL as an argument to the ShellExecute function.</span></span>

 

## <a name="iextracticon"></a><span data-ttu-id="18ca7-164">иекстрактикон</span><span class="sxs-lookup"><span data-stu-id="18ca7-164">IExtractIcon</span></span>

<span data-ttu-id="18ca7-165">**Иекстрактикон** получает значок для ПОЛЬЗОВАТЕЛЬСКОГО интерфейса WDS на основе URL-адреса в Пидл, предоставленного обработчиком протокола.</span><span class="sxs-lookup"><span data-stu-id="18ca7-165">**IExtractIcon** retrieves an icon for the WDS user interface based on the URL in the PIDL provided by your protocol handler.</span></span>

 

## <a name="code-sample"></a><span data-ttu-id="18ca7-166">Образец кода</span><span class="sxs-lookup"><span data-stu-id="18ca7-166">Code Sample</span></span>

<span data-ttu-id="18ca7-167">В [примере кода пользовательского интерфейса обработчика пользовательских протоколов](-search-2x-wds-ph-ui-samplecode.md) демонстрируется реализация **ишеллфолдер** и вспомогательных интерфейсов, а также поддержка манипуляций с PIDL.</span><span class="sxs-lookup"><span data-stu-id="18ca7-167">The [Custom Protocol Handler User Interface Sample Code](-search-2x-wds-ph-ui-samplecode.md) demonstrates an implementation of **IShellFolder** and supporting interfaces and includes support for manipulating the PIDLs.</span></span>

## <a name="related-topics"></a><span data-ttu-id="18ca7-168">Связанные темы</span><span class="sxs-lookup"><span data-stu-id="18ca7-168">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="18ca7-169">**Reference**</span><span class="sxs-lookup"><span data-stu-id="18ca7-169">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="18ca7-170">Пример кода пользовательского интерфейса обработчика настраиваемых протоколов</span><span class="sxs-lookup"><span data-stu-id="18ca7-170">Custom Protocol Handler User Interface Sample Code</span></span>](-search-2x-wds-ph-ui-samplecode.md)
</dt> <dt>

[<span data-ttu-id="18ca7-171">Установка и регистрация обработчиков протоколов</span><span class="sxs-lookup"><span data-stu-id="18ca7-171">Installing and Registering Protocol Handlers</span></span>](-search-2x-wds-ph-install-registration.md)
</dt> </dl>

 

 




