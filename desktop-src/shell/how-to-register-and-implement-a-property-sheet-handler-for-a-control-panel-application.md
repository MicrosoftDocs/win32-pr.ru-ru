---
description: Во многих приложениях панели управления отображается страница свойств, позволяющая пользователям просматривать и изменять различные параметры устройства и системы.
title: Регистрация и реализация обработчика страницы свойств для приложения панели управления
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 47f7f8fe80bf5c7baceddac64d513d950378bcdf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103909535"
---
# <a name="how-to-register-and-implement-a-property-sheet-handler-for-a-control-panel-application"></a><span data-ttu-id="3fbe0-103">Регистрация и реализация обработчика страницы свойств для приложения панели управления</span><span class="sxs-lookup"><span data-stu-id="3fbe0-103">How to Register and Implement a Property Sheet Handler for a Control Panel Application</span></span>

<span data-ttu-id="3fbe0-104">Во многих приложениях панели управления отображается страница свойств, позволяющая пользователям просматривать и изменять различные параметры устройства и системы.</span><span class="sxs-lookup"><span data-stu-id="3fbe0-104">Many Control Panel applications display a Properties property sheet to enable users to view and modify various device and system settings.</span></span> <span data-ttu-id="3fbe0-105">Два из этих приложений — мышь и экран — позволяют обработчикам страниц свойств заменять одну или несколько страниц на настраиваемую страницу.</span><span class="sxs-lookup"><span data-stu-id="3fbe0-105">Two of these applications—Mouse and Display—allow property sheet handlers to replace one or more of their pages with a custom page.</span></span> <span data-ttu-id="3fbe0-106">На следующем снимке экрана показана вкладка свойств **мыши** .</span><span class="sxs-lookup"><span data-stu-id="3fbe0-106">The following screen shot shows the **Mouse Properties** property sheet.</span></span>

![Страница свойств свойств мыши](images/propsheethandler3.jpg)

<span data-ttu-id="3fbe0-108">Обработчики страниц свойств для приложений панели управления похожи на те, которые относятся к типам файлов, с двумя основными исключениями:</span><span class="sxs-lookup"><span data-stu-id="3fbe0-108">Property sheet handlers for Control Panel applications are similar to those for file types, with two primary exceptions:</span></span>

-   <span data-ttu-id="3fbe0-109">Они вызываются приложением панели управления, а не оболочкой.</span><span class="sxs-lookup"><span data-stu-id="3fbe0-109">They are called by a Control Panel application, not the Shell.</span></span>
-   <span data-ttu-id="3fbe0-110">Они регистрируются по-разному.</span><span class="sxs-lookup"><span data-stu-id="3fbe0-110">They are registered differently.</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="3fbe0-111">Что необходимо знать</span><span class="sxs-lookup"><span data-stu-id="3fbe0-111">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="3fbe0-112">Технологии</span><span class="sxs-lookup"><span data-stu-id="3fbe0-112">Technologies</span></span>

-   <span data-ttu-id="3fbe0-113">Shell</span><span class="sxs-lookup"><span data-stu-id="3fbe0-113">Shell</span></span>

### <a name="prerequisites"></a><span data-ttu-id="3fbe0-114">Предварительные условия</span><span class="sxs-lookup"><span data-stu-id="3fbe0-114">Prerequisites</span></span>

-   <span data-ttu-id="3fbe0-115">Знакомство с панелью управления</span><span class="sxs-lookup"><span data-stu-id="3fbe0-115">An understanding of the Control Panel</span></span>
-   <span data-ttu-id="3fbe0-116">Общие сведения о контекстных меню</span><span class="sxs-lookup"><span data-stu-id="3fbe0-116">An understanding of shortcut menus</span></span>

## <a name="instructions"></a><span data-ttu-id="3fbe0-117">Инструкции</span><span class="sxs-lookup"><span data-stu-id="3fbe0-117">Instructions</span></span>

### <a name="step-1-registering-a-property-sheet-handler-for-a-control-panel-application"></a><span data-ttu-id="3fbe0-118">Шаг 1. регистрация обработчика страницы свойств для приложения панели управления</span><span class="sxs-lookup"><span data-stu-id="3fbe0-118">Step 1: Registering a Property Sheet Handler for a Control Panel Application</span></span>

<span data-ttu-id="3fbe0-119">Обработчик страницы свойств приложения панели управления должен быть зарегистрирован в подразделе панели управления.</span><span class="sxs-lookup"><span data-stu-id="3fbe0-119">A Control Panel application property sheet handler must be registered under the Control Panel subkey.</span></span> <span data-ttu-id="3fbe0-120">Этот ключ может находиться в одном из двух расположений в зависимости от того, будет ли обработчик выполняться отдельно для каждого пользователя или компьютера.</span><span class="sxs-lookup"><span data-stu-id="3fbe0-120">This key can be in either of two locations, depending on whether the handler is to be per-user or per-computer.</span></span> <span data-ttu-id="3fbe0-121">Для регистрации "на пользователя" в разделе "Панель управления" находится **\_ Текущая \_ Пользовательская** \\ **Панель управления**: hKey.</span><span class="sxs-lookup"><span data-stu-id="3fbe0-121">For per-user registration, the Control Panel subkey is **HKEY\_CURRENT\_USER**\\**Control Panel**.</span></span> <span data-ttu-id="3fbe0-122">Макрос РЕГСТР \_ path \_ контролпанел, как определено в регстр. h, может использоваться в коде вместо "Панель управления".</span><span class="sxs-lookup"><span data-stu-id="3fbe0-122">The macro REGSTR\_PATH\_CONTROLPANEL as defined in Regstr.h can be used in code in place of "Control Panel".</span></span> <span data-ttu-id="3fbe0-123">Для регистрации на компьютере расположение:</span><span class="sxs-lookup"><span data-stu-id="3fbe0-123">For per-computer registration, the location is:</span></span>

```
HKEY_LOCAL_MACHINE
   Software
      Microsoft
         Windows
            Current Version
               Controls Folder
```

<span data-ttu-id="3fbe0-124">Этот путь можно называть в коде как \_ путь к локальному \_ компьютеру \\ регстр \_ \_ контролсфолдер, используя \_ макрос Регстр Path \_ контролсфолдер, определенный в регстр. h.</span><span class="sxs-lookup"><span data-stu-id="3fbe0-124">This path can be referred to in code as HKEY\_LOCAL\_MACHINE\\REGSTR\_PATH\_CONTROLSFOLDER, using the REGSTR\_PATH\_CONTROLSFOLDER macro that is defined in Regstr.h.</span></span>

<span data-ttu-id="3fbe0-125">Приложения панели управления, которые позволяют обработчикам страниц свойств заменять страницы, имеют подраздел в подразделе панели управления с именем для приложения, например мышь и экран.</span><span class="sxs-lookup"><span data-stu-id="3fbe0-125">The Control Panel applications that allow property sheet handlers to replace pages have a subkey under the Control Panel's subkey, named for the application, such as Mouse and Display.</span></span> <span data-ttu-id="3fbe0-126">Подраздел приложения должен иметь подраздел **шеллекс** с подразделом **пропертишисандлерс** .</span><span class="sxs-lookup"><span data-stu-id="3fbe0-126">The application's subkey must have a **shellex** subkey with a **PropertySheetHandlers** subkey.</span></span> <span data-ttu-id="3fbe0-127">Чтобы зарегистрировать обработчик страницы свойств, добавьте его идентификатор GUID в подраздел **пропертишисандлерс** , связанный с приложением панели управления.</span><span class="sxs-lookup"><span data-stu-id="3fbe0-127">To register a property sheet handler, add its GUID to the **PropertySheetHandlers** subkey that is associated with the Control Panel application.</span></span> <span data-ttu-id="3fbe0-128">Для этого создайте подраздел подраздела **пропертишисандлерс** с именем для обработчика страницы свойств и присвойте его значение по умолчанию строковому формату GUID обработчика.</span><span class="sxs-lookup"><span data-stu-id="3fbe0-128">To do so, create a subkey of the **PropertySheetHandlers** subkey, named for the property sheet handler, and set its default value to the string form of the handler's GUID.</span></span>

<span data-ttu-id="3fbe0-129">В следующем примере обработчик страницы свойств для приложения панели управления мыши регистрируется отдельно для каждого компьютера.</span><span class="sxs-lookup"><span data-stu-id="3fbe0-129">The following example registers a property sheet handler for the Mouse Control Panel application on a per-computer basis.</span></span> <span data-ttu-id="3fbe0-130">Чтобы зарегистрировать его отдельно для каждого пользователя, замените путь к **\_ локальному \_ компьютеру** \\ **регстр \_ path \_ контролсфолдер** с **hKey \_ текущий \_ пользователь** \\ **регстр \_ path \_ контролпанел**.</span><span class="sxs-lookup"><span data-stu-id="3fbe0-130">To register it on a per-user basis, replace **HKEY\_LOCAL\_MACHINE**\\**REGSTR\_PATH\_CONTROLSFOLDER** with **HKEY\_CURRENT\_USER**\\**REGSTR\_PATH\_CONTROLPANEL**.</span></span>

```
HKEY_LOCAL_MACHINE
   REGSTR_PATH_CONTROLSFOLDER
      Mouse
         shellex
            PropertySheetHandlers
               MyPropHandler
                  (Default) = {MyPropHandler CLSID GUID}
```

### <a name="step-2-implementing-a-property-sheet-handler-for-a-control-panel-application"></a><span data-ttu-id="3fbe0-131">Шаг 2. Реализация обработчика страницы свойств для приложения панели управления</span><span class="sxs-lookup"><span data-stu-id="3fbe0-131">Step 2: Implementing a Property Sheet Handler for a Control Panel Application</span></span>

<span data-ttu-id="3fbe0-132">Процедура реализации обработчика страницы свойств панели управления очень похожа на описанную в разделе [Регистрация и реализация обработчика страницы свойств для типа файла](how-to-register-and-implement-a-property-sheet-handler-for-a-file-type.md).</span><span class="sxs-lookup"><span data-stu-id="3fbe0-132">The procedure for implementing a Control Panel property sheet handler is very similar to that discussed in [How to Register and Implement a Property Sheet Handler for a File Type](how-to-register-and-implement-a-property-sheet-handler-for-a-file-type.md).</span></span> <span data-ttu-id="3fbe0-133">Основное отличие заключается в том, что теперь [**ишеллпропшитекст:: реплацепаже**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellpropsheetext-replacepage) требуется реализация без маркера вместо [**Ишеллпропшитекст:: аддпажес**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellpropsheetext-addpages).</span><span class="sxs-lookup"><span data-stu-id="3fbe0-133">The primary difference is that now [**IShellPropSheetExt::ReplacePage**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellpropsheetext-replacepage) needs a nontoken implementation instead of [**IShellPropSheetExt::AddPages**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellpropsheetext-addpages).</span></span>

<span data-ttu-id="3fbe0-134">Когда приложение панели управления собирается отобразить свою страницу свойств, оно вызывает метод [**ишеллпропшитекст:: реплацепаже**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellpropsheetext-replacepage) обработчика страницы свойств один раз для каждой заменяющих страниц.</span><span class="sxs-lookup"><span data-stu-id="3fbe0-134">When a Control Panel application is about to display its property sheet, it calls the property sheet handler's [**IShellPropSheetExt::ReplacePage**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellpropsheetext-replacepage) method once for each page that can be replaced.</span></span> <span data-ttu-id="3fbe0-135">Для параметра *упажеид* задается идентификатор страницы.</span><span class="sxs-lookup"><span data-stu-id="3fbe0-135">The *uPageID* parameter is set to the page's ID.</span></span> <span data-ttu-id="3fbe0-136">Идентификаторы для доступных страниц определяются в Кплекст. h.</span><span class="sxs-lookup"><span data-stu-id="3fbe0-136">The IDs for the available pages are defined in Cplext.h.</span></span> <span data-ttu-id="3fbe0-137">Доступные в настоящее время идентификаторы перечислены в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="3fbe0-137">The currently available IDs are listed in the following table.</span></span> 

| <span data-ttu-id="3fbe0-138">Идентификатор страницы</span><span class="sxs-lookup"><span data-stu-id="3fbe0-138">Page ID</span></span>                      | <span data-ttu-id="3fbe0-139">Описание</span><span class="sxs-lookup"><span data-stu-id="3fbe0-139">Description</span></span>         | <span data-ttu-id="3fbe0-140">Приложение панели управления</span><span class="sxs-lookup"><span data-stu-id="3fbe0-140">Control Panel application</span></span> |
|------------------------------|---------------------|---------------------------|
| <span data-ttu-id="3fbe0-141">\_кнопки мыши \_ кплпаже</span><span class="sxs-lookup"><span data-stu-id="3fbe0-141">CPLPAGE\_MOUSE\_BUTTONS</span></span>      | <span data-ttu-id="3fbe0-142">Страница "кнопки"</span><span class="sxs-lookup"><span data-stu-id="3fbe0-142">The Buttons page</span></span>    | <span data-ttu-id="3fbe0-143">Мышь</span><span class="sxs-lookup"><span data-stu-id="3fbe0-143">Mouse</span></span>                     |
| <span data-ttu-id="3fbe0-144">КПЛПАЖЕ \_ мышь \_ птрмотион</span><span class="sxs-lookup"><span data-stu-id="3fbe0-144">CPLPAGE\_MOUSE\_PTRMOTION</span></span>    | <span data-ttu-id="3fbe0-145">Страница «Перемещение»</span><span class="sxs-lookup"><span data-stu-id="3fbe0-145">The Motion page</span></span>     | <span data-ttu-id="3fbe0-146">Мышь</span><span class="sxs-lookup"><span data-stu-id="3fbe0-146">Mouse</span></span>                     |
| <span data-ttu-id="3fbe0-147">КПЛПАЖЕ \_ \_ колесика мыши</span><span class="sxs-lookup"><span data-stu-id="3fbe0-147">CPLPAGE\_MOUSE\_WHEEL</span></span>        | <span data-ttu-id="3fbe0-148">Страница колесика</span><span class="sxs-lookup"><span data-stu-id="3fbe0-148">The Wheel page</span></span>      | <span data-ttu-id="3fbe0-149">Мышь</span><span class="sxs-lookup"><span data-stu-id="3fbe0-149">Mouse</span></span>                     |
| <span data-ttu-id="3fbe0-150">\_скорость клавиатуры \_ кплпаже</span><span class="sxs-lookup"><span data-stu-id="3fbe0-150">CPLPAGE\_KEYBOARD\_SPEED</span></span>     | <span data-ttu-id="3fbe0-151">Страница «скорость»</span><span class="sxs-lookup"><span data-stu-id="3fbe0-151">The Speed page</span></span>      | <span data-ttu-id="3fbe0-152">Клавиатура</span><span class="sxs-lookup"><span data-stu-id="3fbe0-152">Keyboard</span></span>                  |
| <span data-ttu-id="3fbe0-153">\_фон экрана \_ кплпаже</span><span class="sxs-lookup"><span data-stu-id="3fbe0-153">CPLPAGE\_DISPLAY\_BACKGROUND</span></span> | <span data-ttu-id="3fbe0-154">Фоновая страница</span><span class="sxs-lookup"><span data-stu-id="3fbe0-154">The Background page</span></span> | <span data-ttu-id="3fbe0-155">Отображение</span><span class="sxs-lookup"><span data-stu-id="3fbe0-155">Display</span></span>                   |



 

## <a name="remarks"></a><span data-ttu-id="3fbe0-156">Примечания</span><span class="sxs-lookup"><span data-stu-id="3fbe0-156">Remarks</span></span>

<span data-ttu-id="3fbe0-157">Процедура создания и замены страницы идентична процедуре добавления страницы.</span><span class="sxs-lookup"><span data-stu-id="3fbe0-157">The procedure for creating and replacing a page is identical to that for adding a page.</span></span> <span data-ttu-id="3fbe0-158">Дополнительные сведения см. [в разделе Регистрация и реализация обработчика страницы свойств для типа файла](how-to-register-and-implement-a-property-sheet-handler-for-a-file-type.md).</span><span class="sxs-lookup"><span data-stu-id="3fbe0-158">For more information, see [How to Register and Implement a Property Sheet Handler for a File Type](how-to-register-and-implement-a-property-sheet-handler-for-a-file-type.md).</span></span>

 

 



