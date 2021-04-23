---
description: Указывает команду, которая может быть выполнена с помощью ShellExecute для запуска приложения при его закреплении на панели задач или при запуске нового экземпляра приложения с помощью списка переходов приложения.
ms.assetid: 83aab060-0629-48e3-a2db-9ba96a8631e5
title: System. Аппусермодел. Релаунчкомманд
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 84049f605896ba5e99a98f33557e6ee4dea37df5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105702017"
---
# <a name="systemappusermodelrelaunchcommand"></a><span data-ttu-id="2be23-103">System. Аппусермодел. Релаунчкомманд</span><span class="sxs-lookup"><span data-stu-id="2be23-103">System.AppUserModel.RelaunchCommand</span></span>

<span data-ttu-id="2be23-104">Указывает команду, которая может быть выполнена с помощью [**ShellExecute**](/windows/win32/api/shellapi/nf-shellapi-shellexecutea) для запуска приложения при его закреплении на панели задач или при запуске нового экземпляра приложения с помощью списка переходов приложения.</span><span class="sxs-lookup"><span data-stu-id="2be23-104">Specifies a command that can be executed through [**ShellExecute**](/windows/win32/api/shellapi/nf-shellapi-shellexecutea) to launch an application when it is pinned to the taskbar or when a new instance of the application is launched through the application's Jump List.</span></span>

<span data-ttu-id="2be23-105">Вот несколько примеров.</span><span class="sxs-lookup"><span data-stu-id="2be23-105">Examples include the following:</span></span>


```
shell:::{ED228FDF-9EA8-4870-83B1-96B02CFE0D52}

virtualhost.exe /virtualapp:12345

notepad.exe
```



<span data-ttu-id="2be23-106">Это свойство используется только в том случае, если окно имеет явный идентификатор модели пользователя приложения (AppUserModelID) ([System.AppUserModel.ID](./props-system-appusermodel-id.md), установленный через [**шжетпропертисторефорвиндов**](/windows/desktop/api/Shellapi/nf-shellapi-shgetpropertystoreforwindow)).</span><span class="sxs-lookup"><span data-stu-id="2be23-106">This property is used only if a window has an explicit Application User Model ID (AppUserModelID) ([System.AppUserModel.ID](./props-system-appusermodel-id.md), set through [**SHGetPropertyStoreForWindow**](/windows/desktop/api/Shellapi/nf-shellapi-shgetpropertystoreforwindow)).</span></span> <span data-ttu-id="2be23-107">Если окно не имеет явного AppUserModelID, это свойство игнорируется, а окно группируются и закрепляется как часть процесса, который его владеет.</span><span class="sxs-lookup"><span data-stu-id="2be23-107">If the window does not have an explicit AppUserModelID, this property is ignored and the window is grouped and pinned as if it were part of the process that owns it.</span></span> <span data-ttu-id="2be23-108">Дополнительные сведения о приложении явной Аппусермоделидс и их последствиях для закрепления панели задач см. в разделе [идентификаторы моделей пользователей приложений (аппусермоделидс)](../shell/appids.md).</span><span class="sxs-lookup"><span data-stu-id="2be23-108">For more information about the application of explicit AppUserModelIDs and their effect on taskbar pinning, see [Application User Model IDs (AppUserModelIDs)](../shell/appids.md).</span></span>

<span data-ttu-id="2be23-109">Это свойство предназначено для использования приложениями или окнами, которые хотят предоставлять сведения о перезапуске не по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="2be23-109">This property is meant to be used by applications or windows that want to provide non-default relaunch information.</span></span>

> [!Note]  
> <span data-ttu-id="2be23-110">[System. аппусермодел. релаунчкомманд]() и [System. аппусермодел. релаунчдисплайнамересаурце](./props-system-appusermodel-relaunchdisplaynameresource.md) всегда должны быть заданы вместе.</span><span class="sxs-lookup"><span data-stu-id="2be23-110">[System.AppUserModel.RelaunchCommand]() and [System.AppUserModel.RelaunchDisplayNameResource](./props-system-appusermodel-relaunchdisplaynameresource.md) must always be set together.</span></span> <span data-ttu-id="2be23-111">Если одно из этих свойств не задано, ни один из них не используется.</span><span class="sxs-lookup"><span data-stu-id="2be23-111">If one of those properties is not set, then neither is used.</span></span>

 

<span data-ttu-id="2be23-112">Это свойство вместе с [System. аппусермодел. релаунчдисплайнамересаурце](./props-system-appusermodel-relaunchdisplaynameresource.md) и [System. аппусермодел. релаунчиконресаурце](./props-system-appusermodel-relaunchiconresource.md) можно использовать для визуального определения окна в качестве приложения для пользователя.</span><span class="sxs-lookup"><span data-stu-id="2be23-112">This property, together with [System.AppUserModel.RelaunchDisplayNameResource](./props-system-appusermodel-relaunchdisplaynameresource.md) and [System.AppUserModel.RelaunchIconResource](./props-system-appusermodel-relaunchiconresource.md) can be used to visually define a window as an application to the user.</span></span> <span data-ttu-id="2be23-113">Это полезно для сценариев ведущих приложений, где один экземпляр узла запускает несколько дочерних приложений.</span><span class="sxs-lookup"><span data-stu-id="2be23-113">This is useful for host application scenarios, where a single host instance runs multiple child applications.</span></span> <span data-ttu-id="2be23-114">Например, виртуальная машина, на которой размещается несколько виртуализированных приложений, может потребовать, чтобы эти виртуализированные приложения отображались как отдельные приложения для пользователя.</span><span class="sxs-lookup"><span data-stu-id="2be23-114">For example, a virtual machine that hosts several virtualized applications might want those virtualized applications to appear as individual applications to the user.</span></span> <span data-ttu-id="2be23-115">Виртуальная машина может пометить каждое окно явным образом AppUserModelID и соответствующие свойства перезапуска, чтобы они отображались как приложения.</span><span class="sxs-lookup"><span data-stu-id="2be23-115">The virtual machine could label each window with an explicit AppUserModelID and the appropriate relaunch properties to make them appear as applications.</span></span> <span data-ttu-id="2be23-116">Пользователь может затем закрепить их на панели задач и «перезапустить» закрепленный экземпляр.</span><span class="sxs-lookup"><span data-stu-id="2be23-116">The user could then pin them to the taskbar and "relaunch" the pinned instance.</span></span>

> [!Note]  
> <span data-ttu-id="2be23-117">Это свойство игнорируется, если задано значение [System. аппусермодел. превентпиннинг](./props-system-appusermodel-preventpinning.md) .</span><span class="sxs-lookup"><span data-stu-id="2be23-117">This property is ignored if [System.AppUserModel.PreventPinning](./props-system-appusermodel-preventpinning.md) is set.</span></span> <span data-ttu-id="2be23-118">Это позволяет приложению управлять группированием окон путем назначения им явных Аппусермоделидс, но предотвращая закрепление этих окон.</span><span class="sxs-lookup"><span data-stu-id="2be23-118">This enables an application to control the grouping of its windows by assigning them explicit AppUserModelIDs but preventing those windows from being pinned.</span></span>

 

<span data-ttu-id="2be23-119">Чтобы задать это свойство в окне, используйте [**шжетпропертисторефорвиндов**](/windows/desktop/api/Shellapi/nf-shellapi-shgetpropertystoreforwindow) для получения хранилища свойств окна и используйте методы, извлекают объект [**ипропертисторе**](/windows/win32/api/propsys/nn-propsys-ipropertystore) , чтобы установить свойство [System. аппусермодел. релаунчкомманд]() этого окна.</span><span class="sxs-lookup"><span data-stu-id="2be23-119">To set this property on a window, use [**SHGetPropertyStoreForWindow**](/windows/desktop/api/Shellapi/nf-shellapi-shgetpropertystoreforwindow) to retrieve the window's property store, and use the methods of that retrieved [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) object to set the [System.AppUserModel.RelaunchCommand]() property of that window.</span></span>

## <a name="windows-10-version-1703-windows-10-version-1607-windows-10-version-1511-windows-10-version-1507-windows-81-windows-8-windows-7"></a><span data-ttu-id="2be23-120">Windows 10, версия 1703, Windows 10, версия 1607, Windows 10, версия 1511, Windows 10, версия 1507, Windows 8.1, Windows 8, Windows 7</span><span class="sxs-lookup"><span data-stu-id="2be23-120">Windows 10, version 1703, Windows 10, version 1607, Windows 10, version 1511, Windows 10, version 1507, Windows 8.1, Windows 8, Windows 7</span></span>

```
propertyDescription
   name = System.AppUserModel.RelaunchCommand
   shellPKey = PKEY_AppUserModel_RelaunchCommand
   formatID = 9F4C2855-9F79-4B39-A8D0-E1D42DE1D5F3
   propID = 2
   SearchInfo
      InInvertedIndex = false
      IsColumn = false
   typeInfo
      type = String
      IsInnate = false
```

## <a name="remarks"></a><span data-ttu-id="2be23-121">Комментарии</span><span class="sxs-lookup"><span data-stu-id="2be23-121">Remarks</span></span>

<span data-ttu-id="2be23-122">Значения PKEY определены в списке PKEY. h.</span><span class="sxs-lookup"><span data-stu-id="2be23-122">PKEY values are defined in Propkey.h.</span></span>

## <a name="related-topics"></a><span data-ttu-id="2be23-123">См. также</span><span class="sxs-lookup"><span data-stu-id="2be23-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2be23-124">Идентификаторы модели пользователя приложения (Аппусермоделидс)</span><span class="sxs-lookup"><span data-stu-id="2be23-124">Application User Model IDs (AppUserModelIDs)</span></span>](../shell/appids.md)
</dt> <dt>

[<span data-ttu-id="2be23-125">System.AppUserModel.ID</span><span class="sxs-lookup"><span data-stu-id="2be23-125">System.AppUserModel.ID</span></span>](./props-system-appusermodel-id.md)
</dt> <dt>

[<span data-ttu-id="2be23-126">пропертидескриптионлист</span><span class="sxs-lookup"><span data-stu-id="2be23-126">propertyDescriptionList</span></span>](./propdesc-schema-propertydescriptionlist.md)
</dt> <dt>

[<span data-ttu-id="2be23-127">пропертидескриптион</span><span class="sxs-lookup"><span data-stu-id="2be23-127">propertyDescription</span></span>](./propdesc-schema-propertydescription.md)
</dt> <dt>

[<span data-ttu-id="2be23-128">сеарчинфо</span><span class="sxs-lookup"><span data-stu-id="2be23-128">searchInfo</span></span>](./propdesc-schema-searchinfo.md)
</dt> <dt>

[<span data-ttu-id="2be23-129">лабелинфо</span><span class="sxs-lookup"><span data-stu-id="2be23-129">labelInfo</span></span>](./propdesc-schema-labelinfo.md)
</dt> <dt>

[<span data-ttu-id="2be23-130">typeInfo</span><span class="sxs-lookup"><span data-stu-id="2be23-130">typeInfo</span></span>](./propdesc-schema-typeinfo.md)
</dt> <dt>

[<span data-ttu-id="2be23-131">displayInfo</span><span class="sxs-lookup"><span data-stu-id="2be23-131">displayInfo</span></span>](./propdesc-schema-displayinfo.md)
</dt> <dt>

[<span data-ttu-id="2be23-132">aliasInfo</span><span class="sxs-lookup"><span data-stu-id="2be23-132">aliasInfo</span></span>](./propdesc-schema-aliasinfo.md)
</dt> <dt>

[<span data-ttu-id="2be23-133">stringFormat</span><span class="sxs-lookup"><span data-stu-id="2be23-133">stringFormat</span></span>](./propdesc-schema-stringformat.md)
</dt> <dt>

[<span data-ttu-id="2be23-134">булеанформат</span><span class="sxs-lookup"><span data-stu-id="2be23-134">booleanFormat</span></span>](./propdesc-schema-booleanformat.md)
</dt> <dt>

[<span data-ttu-id="2be23-135">numberFormat</span><span class="sxs-lookup"><span data-stu-id="2be23-135">numberFormat</span></span>](./propdesc-schema-numberformat.md)
</dt> <dt>

[<span data-ttu-id="2be23-136">dateTimeFormat</span><span class="sxs-lookup"><span data-stu-id="2be23-136">dateTimeFormat</span></span>](./propdesc-schema-datetimeformat.md)
</dt> <dt>

[<span data-ttu-id="2be23-137">енумератедлист</span><span class="sxs-lookup"><span data-stu-id="2be23-137">enumeratedList</span></span>](./propdesc-schema-enumeratedlist.md)
</dt> <dt>

[<span data-ttu-id="2be23-138">enum</span><span class="sxs-lookup"><span data-stu-id="2be23-138">enum</span></span>](./propdesc-schema-enum.md)
</dt> <dt>

[<span data-ttu-id="2be23-139">енумранже</span><span class="sxs-lookup"><span data-stu-id="2be23-139">enumRange</span></span>](./propdesc-schema-enumrange.md)
</dt> <dt>

[<span data-ttu-id="2be23-140">image</span><span class="sxs-lookup"><span data-stu-id="2be23-140">image</span></span>](./propdesc-schema-image.md)
</dt> <dt>

[<span data-ttu-id="2be23-141">дравконтрол</span><span class="sxs-lookup"><span data-stu-id="2be23-141">drawControl</span></span>](./propdesc-schema-drawcontrol.md)
</dt> <dt>

[<span data-ttu-id="2be23-142">едитконтрол</span><span class="sxs-lookup"><span data-stu-id="2be23-142">editControl</span></span>](./propdesc-schema-editcontrol.md)
</dt> <dt>

[<span data-ttu-id="2be23-143">филтерконтрол</span><span class="sxs-lookup"><span data-stu-id="2be23-143">filterControl</span></span>](./propdesc-schema-filtercontrol.md)
</dt> <dt>

[<span data-ttu-id="2be23-144">куериконтрол</span><span class="sxs-lookup"><span data-stu-id="2be23-144">queryControl</span></span>](./propdesc-schema-querycontrol.md)
</dt> <dt>

[<span data-ttu-id="2be23-145">релатедпропертинфо</span><span class="sxs-lookup"><span data-stu-id="2be23-145">relatedPropertyInfo</span></span>](./propdesc-schema-relatedpropertyinfo.md)
</dt> <dt>

[<span data-ttu-id="2be23-146">relatedProperty</span><span class="sxs-lookup"><span data-stu-id="2be23-146">relatedProperty</span></span>](./propdesc-schema-relatedproperty.md)
</dt> </dl>

 

 
