---
description: Задает значок, используемый для ярлыка, созданного на панели задач при нажатии пользователем кнопки закрепить приложение на панели задач или запуска нового экземпляра с помощью его списка переходов.
ms.assetid: 3559d1f5-988c-41d9-ba9a-dfa4ba643ee2
title: System. Аппусермодел. Релаунчиконресаурце
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fc79c246fef7be5641c6488dcc34169cd5bbf98b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105662753"
---
# <a name="systemappusermodelrelaunchiconresource"></a><span data-ttu-id="fa0d0-103">System. Аппусермодел. Релаунчиконресаурце</span><span class="sxs-lookup"><span data-stu-id="fa0d0-103">System.AppUserModel.RelaunchIconResource</span></span>

<span data-ttu-id="fa0d0-104">Задает значок, используемый для ярлыка, созданного на панели задач при нажатии пользователем кнопки закрепить приложение на панели задач или запуска нового экземпляра с помощью его списка переходов.</span><span class="sxs-lookup"><span data-stu-id="fa0d0-104">Specifies the icon used for the shortcut created on the taskbar when the user chooses to pin an application to the taskbar or launch a new instance through its button's Jump List.</span></span> <span data-ttu-id="fa0d0-105">Это значок, используемый для группы панелей задач и отображаемый для закрепленного приложения независимо от того, работает ли это приложение.</span><span class="sxs-lookup"><span data-stu-id="fa0d0-105">This is the icon used for the taskbar group and is shown for a pinned application whether that application is running or not.</span></span> <span data-ttu-id="fa0d0-106">Он должен быть указан в одном из следующих форматов:</span><span class="sxs-lookup"><span data-stu-id="fa0d0-106">This should be specified in one of the following formats:</span></span>

-   <span data-ttu-id="fa0d0-107">Стандартный формат ресурсов, например "% системдир% \\ system32 \\shell32.dll,-128".</span><span class="sxs-lookup"><span data-stu-id="fa0d0-107">Standard resource format, such as "%systemdir%\\system32\\shell32.dll,-128".</span></span> <span data-ttu-id="fa0d0-108">Символ "-" перед ИДЕНТИФИКАТОРом ресурса обязателен.</span><span class="sxs-lookup"><span data-stu-id="fa0d0-108">The '-' character before the resource ID is required.</span></span> <span data-ttu-id="fa0d0-109">Не используйте символ "@" в начале строки пути.</span><span class="sxs-lookup"><span data-stu-id="fa0d0-109">Do not use the '@' character at the front of the path string.</span></span>
-   <span data-ttu-id="fa0d0-110">Прямой путь к файлу значка, например "% ProgramFiles% \\ Microsoft \\ Notepad \\ Notepad. ico, 0".</span><span class="sxs-lookup"><span data-stu-id="fa0d0-110">Direct path to an icon file, such as "%programfiles%\\Microsoft\\Notepad\\Notepad.ico,0".</span></span> <span data-ttu-id="fa0d0-111">Обратите внимание, что, поскольку ICO-файлы могут содержать несколько ресурсов значков, в строке необходимо указать идентификатор ресурса.</span><span class="sxs-lookup"><span data-stu-id="fa0d0-111">Note that because .ico files can contain multiple icon resources, a resource ID is required in the string.</span></span> <span data-ttu-id="fa0d0-112">Если ICO-файл является одним изображением, используйте "0" (без символа "-") в качестве идентификатора ресурса.</span><span class="sxs-lookup"><span data-stu-id="fa0d0-112">If the .ico file is a single image, use "0" (without the '-' character) as the resource ID.</span></span>

<span data-ttu-id="fa0d0-113">[System. аппусермодел. релаунчиконресаурце]() является необязательным свойством.</span><span class="sxs-lookup"><span data-stu-id="fa0d0-113">[System.AppUserModel.RelaunchIconResource]() is an optional property.</span></span> <span data-ttu-id="fa0d0-114">Если он не задан, используется значок целевого объекта для команды повторного запуска ([System. аппусермодел. релаунчкомманд](./props-system-appusermodel-relaunchcommand.md)).</span><span class="sxs-lookup"><span data-stu-id="fa0d0-114">If it is not set, the icon of the target of the relaunch command ([System.AppUserModel.RelaunchCommand](./props-system-appusermodel-relaunchcommand.md)) is used.</span></span> <span data-ttu-id="fa0d0-115">Однако, поскольку это может привести к нежелательным результатам, настоятельно рекомендуется явно указать значок с помощью этого свойства.</span><span class="sxs-lookup"><span data-stu-id="fa0d0-115">However, because that can lead to undesired results, we strongly encourage you to provide an icon explicitly through this property.</span></span>

<span data-ttu-id="fa0d0-116">Это свойство используется только в том случае, если окно имеет явный идентификатор модели пользователя приложения (AppUserModelID) ([System.AppUserModel.ID](./props-system-appusermodel-id.md), установленный через [**шжетпропертисторефорвиндов**](/windows/desktop/api/Shellapi/nf-shellapi-shgetpropertystoreforwindow)).</span><span class="sxs-lookup"><span data-stu-id="fa0d0-116">This property is used only if a window has an explicit Application User Model ID (AppUserModelID) ([System.AppUserModel.ID](./props-system-appusermodel-id.md), set through [**SHGetPropertyStoreForWindow**](/windows/desktop/api/Shellapi/nf-shellapi-shgetpropertystoreforwindow)).</span></span> <span data-ttu-id="fa0d0-117">Если окно не имеет явного AppUserModelID (System.AppUserModel.ID), это свойство игнорируется, а окно группируются и закрепляется как часть его процесса-владельца.</span><span class="sxs-lookup"><span data-stu-id="fa0d0-117">If the window does not have an explicit AppUserModelID (System.AppUserModel.ID), this property is ignored and the window is grouped and pinned as if it were part of its owning process.</span></span> <span data-ttu-id="fa0d0-118">Дополнительные сведения о приложении явной Аппусермоделидс и их последствиях для закрепления панели задач см. в разделе [идентификаторы моделей пользователей приложений (аппусермоделидс)](../shell/appids.md).</span><span class="sxs-lookup"><span data-stu-id="fa0d0-118">For more information on the application of explicit AppUserModelIDs and their effect on taskbar pinning, see [Application User Model IDs (AppUserModelIDs)](../shell/appids.md).</span></span> <span data-ttu-id="fa0d0-119">Это свойство предназначено для использования приложениями или окнами, которые хотят предоставлять сведения о перезапуске не по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="fa0d0-119">This property is meant to be used by applications or windows that want to provide non-default relaunch information.</span></span> <span data-ttu-id="fa0d0-120">Дополнительные сведения см. в разделе [System. аппусермодел. релаунчкомманд](./props-system-appusermodel-relaunchcommand.md).</span><span class="sxs-lookup"><span data-stu-id="fa0d0-120">For more information, see [System.AppUserModel.RelaunchCommand](./props-system-appusermodel-relaunchcommand.md).</span></span>

<span data-ttu-id="fa0d0-121">Если в окне задан явный AppUserModelID, но это свойство не задано, система пытается найти ярлык с тем же AppUserModelID и закрепляет этот ярлык на панели задач для представления окна.</span><span class="sxs-lookup"><span data-stu-id="fa0d0-121">If an explicit AppUserModelID is set on the window, but this property is not set, the system attempts to find a shortcut with the same AppUserModelID, and pins that shortcut to the taskbar to represent the window.</span></span> <span data-ttu-id="fa0d0-122">Если такое сочетание клавиш не удается найти, используется резервный исполняемый файл процесса, которому он принадлежит.</span><span class="sxs-lookup"><span data-stu-id="fa0d0-122">If no such shortcut can be located, then the backing executable of the process that owns it is used.</span></span>

> [!Note]  
> <span data-ttu-id="fa0d0-123">Это свойство игнорируется, если задано значение [System. аппусермодел. превентпиннинг](./props-system-appusermodel-preventpinning.md) .</span><span class="sxs-lookup"><span data-stu-id="fa0d0-123">This property is ignored if [System.AppUserModel.PreventPinning](./props-system-appusermodel-preventpinning.md) is set.</span></span> <span data-ttu-id="fa0d0-124">Это позволяет приложению управлять группированием окон путем назначения им явных Аппусермоделидс, но предотвращая закрепление этих окон.</span><span class="sxs-lookup"><span data-stu-id="fa0d0-124">This enables an application to control the grouping of its windows by assigning them explicit AppUserModelIDs but preventing those windows from being pinned.</span></span>

 

<span data-ttu-id="fa0d0-125">Чтобы задать это свойство в окне, используйте [**шжетпропертисторефорвиндов**](/windows/desktop/api/Shellapi/nf-shellapi-shgetpropertystoreforwindow) для получения хранилища свойств окна и используйте методы, извлекают объект [**ипропертисторе**](/windows/win32/api/propsys/nn-propsys-ipropertystore) , чтобы установить свойство [System. аппусермодел. релаунчиконресаурце]() этого окна.</span><span class="sxs-lookup"><span data-stu-id="fa0d0-125">To set this property on a window, use [**SHGetPropertyStoreForWindow**](/windows/desktop/api/Shellapi/nf-shellapi-shgetpropertystoreforwindow) to retrieve the window's property store, and use the methods of that retrieved [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) object to set the [System.AppUserModel.RelaunchIconResource]() property of that window.</span></span>

## <a name="windows-10-version-1703-windows-10-version-1607-windows-10-version-1511-windows-10-version-1507-windows-81"></a><span data-ttu-id="fa0d0-126">Windows 10, версия 1703, Windows 10, версия 1607, Windows 10, версия 1511, Windows 10, версия 1507, Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="fa0d0-126">Windows 10, version 1703, Windows 10, version 1607, Windows 10, version 1511, Windows 10, version 1507, Windows 8.1</span></span>

```
propertyDescription
   name = System.AppUserModel.RelaunchIconResource
   shellPKey = PKEY_AppUserModel_RelaunchIconResource
   formatID = 9F4C2855-9F79-4B39-A8D0-E1D42DE1D5F3
   propID = 3
   SearchInfo
      InInvertedIndex = false
      IsColumn = true
   typeInfo
      type = String
      IsInnate = false
```

## <a name="windows-8-windows-7"></a><span data-ttu-id="fa0d0-127">Windows 8, Windows 7</span><span class="sxs-lookup"><span data-stu-id="fa0d0-127">Windows 8, Windows 7</span></span>

```
propertyDescription
   name = System.AppUserModel.RelaunchIconResource
   shellPKey = PKEY_AppUserModel_RelaunchIconResource
   formatID = 9F4C2855-9F79-4B39-A8D0-E1D42DE1D5F3
   propID = 3
   SearchInfo
      InInvertedIndex = false
      IsColumn = false
   typeInfo
      type = String
      IsInnate = false
```

## <a name="related-topics"></a><span data-ttu-id="fa0d0-128">См. также</span><span class="sxs-lookup"><span data-stu-id="fa0d0-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fa0d0-129">Идентификаторы модели пользователя приложения (Аппусермоделидс)</span><span class="sxs-lookup"><span data-stu-id="fa0d0-129">Application User Model IDs (AppUserModelIDs)</span></span>](../shell/appids.md)
</dt> <dt>

[<span data-ttu-id="fa0d0-130">System.AppUserModel.ID</span><span class="sxs-lookup"><span data-stu-id="fa0d0-130">System.AppUserModel.ID</span></span>](./props-system-appusermodel-id.md)
</dt> <dt>

[<span data-ttu-id="fa0d0-131">пропертидескриптионлист</span><span class="sxs-lookup"><span data-stu-id="fa0d0-131">propertyDescriptionList</span></span>](./propdesc-schema-propertydescriptionlist.md)
</dt> <dt>

[<span data-ttu-id="fa0d0-132">пропертидескриптион</span><span class="sxs-lookup"><span data-stu-id="fa0d0-132">propertyDescription</span></span>](./propdesc-schema-propertydescription.md)
</dt> <dt>

[<span data-ttu-id="fa0d0-133">сеарчинфо</span><span class="sxs-lookup"><span data-stu-id="fa0d0-133">searchInfo</span></span>](./propdesc-schema-searchinfo.md)
</dt> <dt>

[<span data-ttu-id="fa0d0-134">лабелинфо</span><span class="sxs-lookup"><span data-stu-id="fa0d0-134">labelInfo</span></span>](./propdesc-schema-labelinfo.md)
</dt> <dt>

[<span data-ttu-id="fa0d0-135">typeInfo</span><span class="sxs-lookup"><span data-stu-id="fa0d0-135">typeInfo</span></span>](./propdesc-schema-typeinfo.md)
</dt> <dt>

[<span data-ttu-id="fa0d0-136">displayInfo</span><span class="sxs-lookup"><span data-stu-id="fa0d0-136">displayInfo</span></span>](./propdesc-schema-displayinfo.md)
</dt> <dt>

[<span data-ttu-id="fa0d0-137">aliasInfo</span><span class="sxs-lookup"><span data-stu-id="fa0d0-137">aliasInfo</span></span>](./propdesc-schema-aliasinfo.md)
</dt> <dt>

[<span data-ttu-id="fa0d0-138">stringFormat</span><span class="sxs-lookup"><span data-stu-id="fa0d0-138">stringFormat</span></span>](./propdesc-schema-stringformat.md)
</dt> <dt>

[<span data-ttu-id="fa0d0-139">булеанформат</span><span class="sxs-lookup"><span data-stu-id="fa0d0-139">booleanFormat</span></span>](./propdesc-schema-booleanformat.md)
</dt> <dt>

[<span data-ttu-id="fa0d0-140">numberFormat</span><span class="sxs-lookup"><span data-stu-id="fa0d0-140">numberFormat</span></span>](./propdesc-schema-numberformat.md)
</dt> <dt>

[<span data-ttu-id="fa0d0-141">dateTimeFormat</span><span class="sxs-lookup"><span data-stu-id="fa0d0-141">dateTimeFormat</span></span>](./propdesc-schema-datetimeformat.md)
</dt> <dt>

[<span data-ttu-id="fa0d0-142">енумератедлист</span><span class="sxs-lookup"><span data-stu-id="fa0d0-142">enumeratedList</span></span>](./propdesc-schema-enumeratedlist.md)
</dt> <dt>

[<span data-ttu-id="fa0d0-143">enum</span><span class="sxs-lookup"><span data-stu-id="fa0d0-143">enum</span></span>](./propdesc-schema-enum.md)
</dt> <dt>

[<span data-ttu-id="fa0d0-144">енумранже</span><span class="sxs-lookup"><span data-stu-id="fa0d0-144">enumRange</span></span>](./propdesc-schema-enumrange.md)
</dt> <dt>

[<span data-ttu-id="fa0d0-145">image</span><span class="sxs-lookup"><span data-stu-id="fa0d0-145">image</span></span>](./propdesc-schema-image.md)
</dt> <dt>

[<span data-ttu-id="fa0d0-146">дравконтрол</span><span class="sxs-lookup"><span data-stu-id="fa0d0-146">drawControl</span></span>](./propdesc-schema-drawcontrol.md)
</dt> <dt>

[<span data-ttu-id="fa0d0-147">едитконтрол</span><span class="sxs-lookup"><span data-stu-id="fa0d0-147">editControl</span></span>](./propdesc-schema-editcontrol.md)
</dt> <dt>

[<span data-ttu-id="fa0d0-148">филтерконтрол</span><span class="sxs-lookup"><span data-stu-id="fa0d0-148">filterControl</span></span>](./propdesc-schema-filtercontrol.md)
</dt> <dt>

[<span data-ttu-id="fa0d0-149">куериконтрол</span><span class="sxs-lookup"><span data-stu-id="fa0d0-149">queryControl</span></span>](./propdesc-schema-querycontrol.md)
</dt> <dt>

[<span data-ttu-id="fa0d0-150">релатедпропертинфо</span><span class="sxs-lookup"><span data-stu-id="fa0d0-150">relatedPropertyInfo</span></span>](./propdesc-schema-relatedpropertyinfo.md)
</dt> <dt>

[<span data-ttu-id="fa0d0-151">relatedProperty</span><span class="sxs-lookup"><span data-stu-id="fa0d0-151">relatedProperty</span></span>](./propdesc-schema-relatedproperty.md)
</dt> </dl>

 

 
