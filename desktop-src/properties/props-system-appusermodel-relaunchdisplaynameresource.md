---
description: Указывает отображаемое имя, используемое для ярлыка, созданного на панели задач при выборе пользователем закрепления приложения на панели задач или при запуске нового экземпляра с помощью списка переходов кнопки.
ms.assetid: a149838b-83b6-44ce-b705-e2804efb3d31
title: System. Аппусермодел. Релаунчдисплайнамересаурце
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d79c22d0ccecb8bac86fe5ca3636ed10ed2ca50b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104264577"
---
# <a name="systemappusermodelrelaunchdisplaynameresource"></a><span data-ttu-id="e2f04-103">System. Аппусермодел. Релаунчдисплайнамересаурце</span><span class="sxs-lookup"><span data-stu-id="e2f04-103">System.AppUserModel.RelaunchDisplayNameResource</span></span>

<span data-ttu-id="e2f04-104">Указывает отображаемое имя, используемое для ярлыка, созданного на панели задач при выборе пользователем закрепления приложения на панели задач или при запуске нового экземпляра с помощью списка переходов кнопки.</span><span class="sxs-lookup"><span data-stu-id="e2f04-104">Specifies the display name used for the shortcut created on the taskbar when the user chooses to pin an application to the taskbar or launch a new instance through its button's Jump List.</span></span> <span data-ttu-id="e2f04-105">Значение этого свойства должно быть одним из следующих:</span><span class="sxs-lookup"><span data-stu-id="e2f04-105">The value of this property must be one of the following:</span></span>

-   <span data-ttu-id="e2f04-106">Непрямая строка ресурса, например "@% системдир% \\ system32 \\shell32.dll,-19263".</span><span class="sxs-lookup"><span data-stu-id="e2f04-106">An indirect resource string such as "@%systemdir%\\system32\\shell32.dll,-19263".</span></span> <span data-ttu-id="e2f04-107">Обратите внимание, что символ "@" требуется для различения косвенной строки от обычной текстовой строки (описывается в следующем маркированном абзаце).</span><span class="sxs-lookup"><span data-stu-id="e2f04-107">Note that the '@' character is required to distinguish an indirect string from a plain-text string (described in the next bulleted paragraph).</span></span> <span data-ttu-id="e2f04-108">Эта непрямая строка состоит из двоичного файла и идентификатора ресурса строки, содержащейся в этом двоичном файле.</span><span class="sxs-lookup"><span data-stu-id="e2f04-108">This indirect string consists of a binary file and a resource ID of the string contained in that binary.</span></span> <span data-ttu-id="e2f04-109">Настоятельно рекомендуется использовать эту форму непрямого строкового типа, которая гарантирует, что отображаемое имя изменится соответствующим образом при изменении языка системы с помощью многоязыкового интерфейса пользователя (MUI).</span><span class="sxs-lookup"><span data-stu-id="e2f04-109">We strongly recommend that you use this indirect string form, which ensures that the display name changes appropriately when the system language is changed through the Multilingual User Interface (MUI).</span></span> <span data-ttu-id="e2f04-110">Символ "-" перед ИДЕНТИФИКАТОРом ресурса обязателен.</span><span class="sxs-lookup"><span data-stu-id="e2f04-110">The '-' character before the resource ID is required.</span></span>
-   <span data-ttu-id="e2f04-111">Обычная текстовая строка, которая не указывает на ресурс.</span><span class="sxs-lookup"><span data-stu-id="e2f04-111">A plain-text string that does not point to a resource.</span></span> <span data-ttu-id="e2f04-112">Этот параметр следует использовать только в том случае, если отображаемое имя динамически вычисляется или получается из источника данных, не поддерживающего MUI.</span><span class="sxs-lookup"><span data-stu-id="e2f04-112">This should only be used when the display name is dynamically calculated or obtained from a data source that does not support MUI.</span></span> <span data-ttu-id="e2f04-113">Например, строка может быть именем устройства, например Microsoft Zune, в случаях, когда приложение отображается, когда устройство подключено к компьютеру.</span><span class="sxs-lookup"><span data-stu-id="e2f04-113">For example, the string could be the name of a device, such as "Microsoft Zune", in cases where the application appears when that device is attached to the computer.</span></span>

> [!Note]  
> <span data-ttu-id="e2f04-114">[System. аппусермодел. релаунчкомманд](./props-system-appusermodel-relaunchcommand.md) и [System. аппусермодел. релаунчдисплайнамересаурце]() всегда должны быть заданы вместе.</span><span class="sxs-lookup"><span data-stu-id="e2f04-114">[System.AppUserModel.RelaunchCommand](./props-system-appusermodel-relaunchcommand.md) and [System.AppUserModel.RelaunchDisplayNameResource]() must always be set together.</span></span> <span data-ttu-id="e2f04-115">Если одно из этих свойств не задано, ни один из них не используется.</span><span class="sxs-lookup"><span data-stu-id="e2f04-115">If one of those properties is not set, then neither is used.</span></span>

 

<span data-ttu-id="e2f04-116">Это свойство используется только в том случае, если окно имеет явный идентификатор модели пользователя приложения (AppUserModelID) ([System.AppUserModel.ID](./props-system-appusermodel-id.md), установленный через [**шжетпропертисторефорвиндов**](/windows/desktop/api/Shellapi/nf-shellapi-shgetpropertystoreforwindow)).</span><span class="sxs-lookup"><span data-stu-id="e2f04-116">This property is used only if a window has an explicit Application User Model ID (AppUserModelID) ([System.AppUserModel.ID](./props-system-appusermodel-id.md), set through [**SHGetPropertyStoreForWindow**](/windows/desktop/api/Shellapi/nf-shellapi-shgetpropertystoreforwindow)).</span></span> <span data-ttu-id="e2f04-117">Если окно не имеет явного AppUserModelID, это свойство игнорируется, а окно группируются и закрепляется как часть процесса, который его владеет.</span><span class="sxs-lookup"><span data-stu-id="e2f04-117">If the window does not have an explicit AppUserModelID, this property is ignored and the window is grouped and pinned as if it were part of the process that owns it.</span></span> <span data-ttu-id="e2f04-118">Дополнительные сведения о приложении явной Аппусермоделидс и их последствиях для закрепления панели задач см. в разделе [идентификаторы моделей пользователей приложений (аппусермоделидс)](../shell/appids.md).</span><span class="sxs-lookup"><span data-stu-id="e2f04-118">For more information on the application of explicit AppUserModelIDs and their effect on taskbar pinning, see [Application User Model IDs (AppUserModelIDs)](../shell/appids.md).</span></span> <span data-ttu-id="e2f04-119">Это свойство предназначено для использования приложениями или окнами, которые хотят предоставлять сведения о перезапуске не по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="e2f04-119">This property is meant to be used by applications or windows that want to provide non-default relaunch information.</span></span> <span data-ttu-id="e2f04-120">Дополнительные сведения см. в разделе [System. аппусермодел. релаунчкомманд](./props-system-appusermodel-relaunchcommand.md).</span><span class="sxs-lookup"><span data-stu-id="e2f04-120">For more information, see [System.AppUserModel.RelaunchCommand](./props-system-appusermodel-relaunchcommand.md).</span></span>

> [!Note]  
> <span data-ttu-id="e2f04-121">Это свойство игнорируется, если задано значение [System. аппусермодел. превентпиннинг](./props-system-appusermodel-preventpinning.md) .</span><span class="sxs-lookup"><span data-stu-id="e2f04-121">This property is ignored if [System.AppUserModel.PreventPinning](./props-system-appusermodel-preventpinning.md) is set.</span></span> <span data-ttu-id="e2f04-122">Это позволяет приложению управлять группированием окон путем назначения им явных Аппусермоделидс, но предотвращая закрепление этих окон.</span><span class="sxs-lookup"><span data-stu-id="e2f04-122">This enables an application to control the grouping of its windows by assigning them explicit AppUserModelIDs but preventing those windows from being pinned.</span></span>

 

<span data-ttu-id="e2f04-123">Чтобы задать это свойство в окне, используйте [**шжетпропертисторефорвиндов**](/windows/desktop/api/Shellapi/nf-shellapi-shgetpropertystoreforwindow) для получения хранилища свойств окна и используйте методы, извлекают объект [**ипропертисторе**](/windows/win32/api/propsys/nn-propsys-ipropertystore) , чтобы установить свойство [System. аппусермодел. релаунчдисплайнамересаурце]() этого окна.</span><span class="sxs-lookup"><span data-stu-id="e2f04-123">To set this property on a window, use [**SHGetPropertyStoreForWindow**](/windows/desktop/api/Shellapi/nf-shellapi-shgetpropertystoreforwindow) to retrieve the window's property store, and use the methods of that retrieved [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) object to set the [System.AppUserModel.RelaunchDisplayNameResource]() property of that window.</span></span>

## <a name="windows-10-version-1703-windows-10-version-1607-windows-10-version-1511-windows-10-version-1507-windows-81-windows-8-windows-7"></a><span data-ttu-id="e2f04-124">Windows 10, версия 1703, Windows 10, версия 1607, Windows 10, версия 1511, Windows 10, версия 1507, Windows 8.1, Windows 8, Windows 7</span><span class="sxs-lookup"><span data-stu-id="e2f04-124">Windows 10, version 1703, Windows 10, version 1607, Windows 10, version 1511, Windows 10, version 1507, Windows 8.1, Windows 8, Windows 7</span></span>

```
propertyDescription
   name = System.AppUserModel.RelaunchDisplayNameResource
   shellPKey = PKEY_AppUserModel_RelaunchDisplayNameResource
   formatID = 9F4C2855-9F79-4B39-A8D0-E1D42DE1D5F3
   propID = 4
   SearchInfo
      InInvertedIndex = false
      IsColumn = false
   typeInfo
      type = String
      IsInnate = false
```

## <a name="remarks"></a><span data-ttu-id="e2f04-125">Комментарии</span><span class="sxs-lookup"><span data-stu-id="e2f04-125">Remarks</span></span>

<span data-ttu-id="e2f04-126">Значения PKEY определены в списке PKEY. h.</span><span class="sxs-lookup"><span data-stu-id="e2f04-126">PKEY values are defined in Propkey.h.</span></span>

## <a name="related-topics"></a><span data-ttu-id="e2f04-127">См. также</span><span class="sxs-lookup"><span data-stu-id="e2f04-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e2f04-128">Идентификаторы модели пользователя приложения (Аппусермоделидс)</span><span class="sxs-lookup"><span data-stu-id="e2f04-128">Application User Model IDs (AppUserModelIDs)</span></span>](../shell/appids.md)
</dt> <dt>

[<span data-ttu-id="e2f04-129">System.AppUserModel.ID</span><span class="sxs-lookup"><span data-stu-id="e2f04-129">System.AppUserModel.ID</span></span>](./props-system-appusermodel-id.md)
</dt> <dt>

[<span data-ttu-id="e2f04-130">пропертидескриптионлист</span><span class="sxs-lookup"><span data-stu-id="e2f04-130">propertyDescriptionList</span></span>](./propdesc-schema-propertydescriptionlist.md)
</dt> <dt>

[<span data-ttu-id="e2f04-131">пропертидескриптион</span><span class="sxs-lookup"><span data-stu-id="e2f04-131">propertyDescription</span></span>](./propdesc-schema-propertydescription.md)
</dt> <dt>

[<span data-ttu-id="e2f04-132">сеарчинфо</span><span class="sxs-lookup"><span data-stu-id="e2f04-132">searchInfo</span></span>](./propdesc-schema-searchinfo.md)
</dt> <dt>

[<span data-ttu-id="e2f04-133">лабелинфо</span><span class="sxs-lookup"><span data-stu-id="e2f04-133">labelInfo</span></span>](./propdesc-schema-labelinfo.md)
</dt> <dt>

[<span data-ttu-id="e2f04-134">typeInfo</span><span class="sxs-lookup"><span data-stu-id="e2f04-134">typeInfo</span></span>](./propdesc-schema-typeinfo.md)
</dt> <dt>

[<span data-ttu-id="e2f04-135">displayInfo</span><span class="sxs-lookup"><span data-stu-id="e2f04-135">displayInfo</span></span>](./propdesc-schema-displayinfo.md)
</dt> <dt>

[<span data-ttu-id="e2f04-136">aliasInfo</span><span class="sxs-lookup"><span data-stu-id="e2f04-136">aliasInfo</span></span>](./propdesc-schema-aliasinfo.md)
</dt> <dt>

[<span data-ttu-id="e2f04-137">stringFormat</span><span class="sxs-lookup"><span data-stu-id="e2f04-137">stringFormat</span></span>](./propdesc-schema-stringformat.md)
</dt> <dt>

[<span data-ttu-id="e2f04-138">булеанформат</span><span class="sxs-lookup"><span data-stu-id="e2f04-138">booleanFormat</span></span>](./propdesc-schema-booleanformat.md)
</dt> <dt>

[<span data-ttu-id="e2f04-139">numberFormat</span><span class="sxs-lookup"><span data-stu-id="e2f04-139">numberFormat</span></span>](./propdesc-schema-numberformat.md)
</dt> <dt>

[<span data-ttu-id="e2f04-140">dateTimeFormat</span><span class="sxs-lookup"><span data-stu-id="e2f04-140">dateTimeFormat</span></span>](./propdesc-schema-datetimeformat.md)
</dt> <dt>

[<span data-ttu-id="e2f04-141">енумератедлист</span><span class="sxs-lookup"><span data-stu-id="e2f04-141">enumeratedList</span></span>](./propdesc-schema-enumeratedlist.md)
</dt> <dt>

[<span data-ttu-id="e2f04-142">enum</span><span class="sxs-lookup"><span data-stu-id="e2f04-142">enum</span></span>](./propdesc-schema-enum.md)
</dt> <dt>

[<span data-ttu-id="e2f04-143">енумранже</span><span class="sxs-lookup"><span data-stu-id="e2f04-143">enumRange</span></span>](./propdesc-schema-enumrange.md)
</dt> <dt>

[<span data-ttu-id="e2f04-144">image</span><span class="sxs-lookup"><span data-stu-id="e2f04-144">image</span></span>](./propdesc-schema-image.md)
</dt> <dt>

[<span data-ttu-id="e2f04-145">дравконтрол</span><span class="sxs-lookup"><span data-stu-id="e2f04-145">drawControl</span></span>](./propdesc-schema-drawcontrol.md)
</dt> <dt>

[<span data-ttu-id="e2f04-146">едитконтрол</span><span class="sxs-lookup"><span data-stu-id="e2f04-146">editControl</span></span>](./propdesc-schema-editcontrol.md)
</dt> <dt>

[<span data-ttu-id="e2f04-147">филтерконтрол</span><span class="sxs-lookup"><span data-stu-id="e2f04-147">filterControl</span></span>](./propdesc-schema-filtercontrol.md)
</dt> <dt>

[<span data-ttu-id="e2f04-148">куериконтрол</span><span class="sxs-lookup"><span data-stu-id="e2f04-148">queryControl</span></span>](./propdesc-schema-querycontrol.md)
</dt> <dt>

[<span data-ttu-id="e2f04-149">релатедпропертинфо</span><span class="sxs-lookup"><span data-stu-id="e2f04-149">relatedPropertyInfo</span></span>](./propdesc-schema-relatedpropertyinfo.md)
</dt> <dt>

[<span data-ttu-id="e2f04-150">relatedProperty</span><span class="sxs-lookup"><span data-stu-id="e2f04-150">relatedProperty</span></span>](./propdesc-schema-relatedproperty.md)
</dt> </dl>

 

 
