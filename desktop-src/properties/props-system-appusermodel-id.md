---
description: Явный идентификатор модели пользователя приложения (AppUserModelID), используемый для связывания процессов, файлов и окон с определенным приложением.
ms.assetid: 07858b3c-e601-40ec-a87a-d66612d5473a
title: System.AppUserModel.ID
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 82c636b2c946f1138f4a25c3129a7a3b44d31558
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104344782"
---
# <a name="systemappusermodelid"></a><span data-ttu-id="2da5c-103">System.AppUserModel.ID</span><span class="sxs-lookup"><span data-stu-id="2da5c-103">System.AppUserModel.ID</span></span>

<span data-ttu-id="2da5c-104">Явный идентификатор модели пользователя приложения (AppUserModelID), используемый для связывания процессов, файлов и окон с определенным приложением.</span><span class="sxs-lookup"><span data-stu-id="2da5c-104">An explicit Application User Model ID (AppUserModelID) used to associate processes, files, and windows with a particular application.</span></span> <span data-ttu-id="2da5c-105">В некоторых случаях достаточно полагаться на внутренний AppUserModelID, назначенный процессу системы.</span><span class="sxs-lookup"><span data-stu-id="2da5c-105">In some cases, it is sufficient to rely on the internal AppUserModelID assigned to a process by the system.</span></span> <span data-ttu-id="2da5c-106">Однако приложение, владеющее несколькими процессами или приложением, которое выполняется в хост-процессе, может потребовать явно идентифицировать себя через это свойство, чтобы оно могло сгруппировать разрозненные окна под одной кнопкой на панели задач и управлять содержимым списка переходов этого приложения.</span><span class="sxs-lookup"><span data-stu-id="2da5c-106">However, an application that owns multiple processes or an application that is running in a host process might need to explicitly identify itself through this property so that it can group its otherwise disparate windows under a single taskbar button and control the contents of that application's Jump List.</span></span>

<span data-ttu-id="2da5c-107">Чтобы задать это свойство в окне, используйте [**шжетпропертисторефорвиндов**](/windows/desktop/api/Shellapi/nf-shellapi-shgetpropertystoreforwindow) для получения хранилища свойств окна и используйте методы, извлекают объект [**ипропертисторе**](/windows/win32/api/propsys/nn-propsys-ipropertystore) , чтобы установить свойство [System.AppUserModel.ID]() этого окна.</span><span class="sxs-lookup"><span data-stu-id="2da5c-107">To set this property on a window, use [**SHGetPropertyStoreForWindow**](/windows/desktop/api/Shellapi/nf-shellapi-shgetpropertystoreforwindow) to retrieve the window's property store, and use the methods of that retrieved [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) object to set the [System.AppUserModel.ID]() property of that window.</span></span>

<span data-ttu-id="2da5c-108">Дополнительные сведения см. в разделе [идентификаторы моделей пользователей приложения (аппусермоделидс)](../shell/appids.md).</span><span class="sxs-lookup"><span data-stu-id="2da5c-108">For more information, see [Application User Model IDs (AppUserModelIDs)](../shell/appids.md).</span></span>

<span data-ttu-id="2da5c-109">Когда свойство [System.AppUserModel.ID]() установлено, панель задач уведомляется о необходимости обновления сведений в окне или ярлыке, заданному этим AppUserModelID.</span><span class="sxs-lookup"><span data-stu-id="2da5c-109">At the time the [System.AppUserModel.ID]() property is set, the taskbar is notified to refresh its information on the window or shortcut given that AppUserModelID.</span></span>

<span data-ttu-id="2da5c-110">Другие свойства окна и ярлыка можно использовать в сочетании с явным AppUserModelID для дальнейшего управления группированием и закреплением, связанным с окном, отображаемым именем и значком, используемым для него на панели задач, и командой для запуска приложения, закрепленного на панели задач, или нового экземпляра приложения с помощью списка переходов этого приложения.</span><span class="sxs-lookup"><span data-stu-id="2da5c-110">Other window and shortcut properties can be used in conjunction with an explicit AppUserModelID to further control the grouping and pinning associated with a window, the display name and icon used for it in the taskbar, and the command to launch either an application pinned to the taskbar or a new instance of the application through that application's Jump List.</span></span> <span data-ttu-id="2da5c-111">Эти свойства должны быть установлены перед установкой свойства [System.AppUserModel.ID]() .</span><span class="sxs-lookup"><span data-stu-id="2da5c-111">These properties should be set before setting the [System.AppUserModel.ID]() property.</span></span> <span data-ttu-id="2da5c-112">Дополнительные сведения см. в следующих разделах:</span><span class="sxs-lookup"><span data-stu-id="2da5c-112">For more information, see the following topics:</span></span>

-   [<span data-ttu-id="2da5c-113">System. Аппусермодел. Превентпиннинг</span><span class="sxs-lookup"><span data-stu-id="2da5c-113">System.AppUserModel.PreventPinning</span></span>](./props-system-appusermodel-preventpinning.md)
-   [<span data-ttu-id="2da5c-114">System. Аппусермодел. Релаунчкомманд</span><span class="sxs-lookup"><span data-stu-id="2da5c-114">System.AppUserModel.RelaunchCommand</span></span>](./props-system-appusermodel-relaunchcommand.md)
-   [<span data-ttu-id="2da5c-115">System. Аппусермодел. Релаунчдисплайнамересаурце</span><span class="sxs-lookup"><span data-stu-id="2da5c-115">System.AppUserModel.RelaunchDisplayNameResource</span></span>](./props-system-appusermodel-relaunchdisplaynameresource.md)
-   [<span data-ttu-id="2da5c-116">System. Аппусермодел. Релаунчиконресаурце</span><span class="sxs-lookup"><span data-stu-id="2da5c-116">System.AppUserModel.RelaunchIconResource</span></span>](./props-system-appusermodel-relaunchiconresource.md)

## <a name="windows-10-version-1703-windows-10-version-1607-windows-10-version-1511-windows-10-version-1507-windows-81-windows-8-windows-7"></a><span data-ttu-id="2da5c-117">Windows 10, версия 1703, Windows 10, версия 1607, Windows 10, версия 1511, Windows 10, версия 1507, Windows 8.1, Windows 8, Windows 7</span><span class="sxs-lookup"><span data-stu-id="2da5c-117">Windows 10, version 1703, Windows 10, version 1607, Windows 10, version 1511, Windows 10, version 1507, Windows 8.1, Windows 8, Windows 7</span></span>

```
propertyDescription
   name = System.AppUserModel.ID
   shellPKey = PKEY_AppUserModel_ID
   formatID = 9F4C2855-9F79-4B39-A8D0-E1D42DE1D5F3
   propID = 5
   SearchInfo
      InInvertedIndex = false
      IsColumn = false
   typeInfo
      type = String
      IsInnate = false
```

## <a name="remarks"></a><span data-ttu-id="2da5c-118">Комментарии</span><span class="sxs-lookup"><span data-stu-id="2da5c-118">Remarks</span></span>

<span data-ttu-id="2da5c-119">Значения PKEY определены в списке PKEY. h.</span><span class="sxs-lookup"><span data-stu-id="2da5c-119">PKEY values are defined in Propkey.h.</span></span>

## <a name="related-topics"></a><span data-ttu-id="2da5c-120">См. также</span><span class="sxs-lookup"><span data-stu-id="2da5c-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2da5c-121">Идентификаторы модели пользователя приложения (Аппусермоделидс)</span><span class="sxs-lookup"><span data-stu-id="2da5c-121">Application User Model IDs (AppUserModelIDs)</span></span>](../shell/appids.md)
</dt> <dt>

[<span data-ttu-id="2da5c-122">**шжетпропертисторефорвиндов**</span><span class="sxs-lookup"><span data-stu-id="2da5c-122">**SHGetPropertyStoreForWindow**</span></span>](/windows/desktop/api/Shellapi/nf-shellapi-shgetpropertystoreforwindow)
</dt> <dt>

[<span data-ttu-id="2da5c-123">пропертидескриптионлист</span><span class="sxs-lookup"><span data-stu-id="2da5c-123">propertyDescriptionList</span></span>](./propdesc-schema-propertydescriptionlist.md)
</dt> <dt>

[<span data-ttu-id="2da5c-124">пропертидескриптион</span><span class="sxs-lookup"><span data-stu-id="2da5c-124">propertyDescription</span></span>](./propdesc-schema-propertydescription.md)
</dt> <dt>

[<span data-ttu-id="2da5c-125">сеарчинфо</span><span class="sxs-lookup"><span data-stu-id="2da5c-125">searchInfo</span></span>](./propdesc-schema-searchinfo.md)
</dt> <dt>

[<span data-ttu-id="2da5c-126">лабелинфо</span><span class="sxs-lookup"><span data-stu-id="2da5c-126">labelInfo</span></span>](./propdesc-schema-labelinfo.md)
</dt> <dt>

[<span data-ttu-id="2da5c-127">typeInfo</span><span class="sxs-lookup"><span data-stu-id="2da5c-127">typeInfo</span></span>](./propdesc-schema-typeinfo.md)
</dt> <dt>

[<span data-ttu-id="2da5c-128">displayInfo</span><span class="sxs-lookup"><span data-stu-id="2da5c-128">displayInfo</span></span>](./propdesc-schema-displayinfo.md)
</dt> <dt>

[<span data-ttu-id="2da5c-129">aliasInfo</span><span class="sxs-lookup"><span data-stu-id="2da5c-129">aliasInfo</span></span>](./propdesc-schema-aliasinfo.md)
</dt> <dt>

[<span data-ttu-id="2da5c-130">stringFormat</span><span class="sxs-lookup"><span data-stu-id="2da5c-130">stringFormat</span></span>](./propdesc-schema-stringformat.md)
</dt> <dt>

[<span data-ttu-id="2da5c-131">булеанформат</span><span class="sxs-lookup"><span data-stu-id="2da5c-131">booleanFormat</span></span>](./propdesc-schema-booleanformat.md)
</dt> <dt>

[<span data-ttu-id="2da5c-132">numberFormat</span><span class="sxs-lookup"><span data-stu-id="2da5c-132">numberFormat</span></span>](./propdesc-schema-numberformat.md)
</dt> <dt>

[<span data-ttu-id="2da5c-133">dateTimeFormat</span><span class="sxs-lookup"><span data-stu-id="2da5c-133">dateTimeFormat</span></span>](./propdesc-schema-datetimeformat.md)
</dt> <dt>

[<span data-ttu-id="2da5c-134">енумератедлист</span><span class="sxs-lookup"><span data-stu-id="2da5c-134">enumeratedList</span></span>](./propdesc-schema-enumeratedlist.md)
</dt> <dt>

[<span data-ttu-id="2da5c-135">enum</span><span class="sxs-lookup"><span data-stu-id="2da5c-135">enum</span></span>](./propdesc-schema-enum.md)
</dt> <dt>

[<span data-ttu-id="2da5c-136">енумранже</span><span class="sxs-lookup"><span data-stu-id="2da5c-136">enumRange</span></span>](./propdesc-schema-enumrange.md)
</dt> <dt>

[<span data-ttu-id="2da5c-137">image</span><span class="sxs-lookup"><span data-stu-id="2da5c-137">image</span></span>](./propdesc-schema-image.md)
</dt> <dt>

[<span data-ttu-id="2da5c-138">дравконтрол</span><span class="sxs-lookup"><span data-stu-id="2da5c-138">drawControl</span></span>](./propdesc-schema-drawcontrol.md)
</dt> <dt>

[<span data-ttu-id="2da5c-139">едитконтрол</span><span class="sxs-lookup"><span data-stu-id="2da5c-139">editControl</span></span>](./propdesc-schema-editcontrol.md)
</dt> <dt>

[<span data-ttu-id="2da5c-140">филтерконтрол</span><span class="sxs-lookup"><span data-stu-id="2da5c-140">filterControl</span></span>](./propdesc-schema-filtercontrol.md)
</dt> <dt>

[<span data-ttu-id="2da5c-141">куериконтрол</span><span class="sxs-lookup"><span data-stu-id="2da5c-141">queryControl</span></span>](./propdesc-schema-querycontrol.md)
</dt> <dt>

[<span data-ttu-id="2da5c-142">релатедпропертинфо</span><span class="sxs-lookup"><span data-stu-id="2da5c-142">relatedPropertyInfo</span></span>](./propdesc-schema-relatedpropertyinfo.md)
</dt> <dt>

[<span data-ttu-id="2da5c-143">relatedProperty</span><span class="sxs-lookup"><span data-stu-id="2da5c-143">relatedProperty</span></span>](./propdesc-schema-relatedproperty.md)
</dt> </dl>

 

 
