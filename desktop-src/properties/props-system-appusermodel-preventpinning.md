---
description: Отключает возможность закрепления ярлыка или окна на панели задач или в меню "Пуск". Это свойство также делает элемент недоступным для включения в список наиболее часто используемых программных элементов меню "Пуск".
ms.assetid: 86239BF8-BCFC-4e76-BF94-5ABA4639562C
title: System. Аппусермодел. Превентпиннинг
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7804c615bcb35909610b06622bd25fe3dccdd0f3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103910183"
---
# <a name="systemappusermodelpreventpinning"></a><span data-ttu-id="d2309-104">System. Аппусермодел. Превентпиннинг</span><span class="sxs-lookup"><span data-stu-id="d2309-104">System.AppUserModel.PreventPinning</span></span>

<span data-ttu-id="d2309-105">Отключает возможность закрепления ярлыка или окна на панели задач или в меню " **Пуск** ".</span><span class="sxs-lookup"><span data-stu-id="d2309-105">Disables the ability of a shortcut or window to be pinned to the taskbar or the **Start** menu.</span></span> <span data-ttu-id="d2309-106">Это свойство также делает элемент недоступным для включения в список наиболее часто используемых программных элементов меню " **Пуск** ".</span><span class="sxs-lookup"><span data-stu-id="d2309-106">This property also makes the item ineligible for inclusion in the **Start** menu's Most Frequently Used (MFU) list.</span></span>

<span data-ttu-id="d2309-107">Это свойство должно быть установлено в окне перед свойством [ \_ \_ идентификатора PKEY аппусермодел](./props-system-appusermodel-id.md) .</span><span class="sxs-lookup"><span data-stu-id="d2309-107">This property must be set on a window before the [PKEY\_AppUserModel\_ID](./props-system-appusermodel-id.md) property.</span></span> <span data-ttu-id="d2309-108">После \_ \_ установки свойства аппусермодел ID для PKEY изменения в [PKEY \_ аппусермодел \_ превентпиннинг]() игнорируются.</span><span class="sxs-lookup"><span data-stu-id="d2309-108">After the PKEY\_AppUserModel\_ID property is set, changes to [PKEY\_AppUserModel\_PreventPinning]() are ignored.</span></span>

<span data-ttu-id="d2309-109">Дополнительные сведения о идентификаторах моделей пользователей приложений (Аппусермоделидс) и других способах исключения элемента из панели задач и о включении часто используемых элементов см. в разделе [идентификаторы моделей пользователей приложений (аппусермоделидс)](../shell/appids.md).</span><span class="sxs-lookup"><span data-stu-id="d2309-109">For more information about Application User Model IDs (AppUserModelIDs) and other methods of excluding an item from being pinned to the taskbar and from MFU inclusion, see [Application User Model IDs (AppUserModelIDs)](../shell/appids.md).</span></span>

<span data-ttu-id="d2309-110">Чтобы задать это свойство в окне, используйте [**шжетпропертисторефорвиндов**](/windows/desktop/api/Shellapi/nf-shellapi-shgetpropertystoreforwindow) для получения хранилища свойств окна и используйте методы, извлекают объект [**ипропертисторе**](/windows/win32/api/propsys/nn-propsys-ipropertystore) , чтобы установить свойство [System. аппусермодел. превентпиннинг]() этого окна.</span><span class="sxs-lookup"><span data-stu-id="d2309-110">To set this property on a window, use [**SHGetPropertyStoreForWindow**](/windows/desktop/api/Shellapi/nf-shellapi-shgetpropertystoreforwindow) to retrieve the window's property store, and use the methods of that retrieved [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) object to set the [System.AppUserModel.PreventPinning]() property of that window.</span></span>

<span data-ttu-id="d2309-111">Установка этого свойства приводит к игнорированию следующих свойств:</span><span class="sxs-lookup"><span data-stu-id="d2309-111">Setting this property causes the following properties to be ignored:</span></span>

-   [<span data-ttu-id="d2309-112">System. Аппусермодел. Релаунчкомманд</span><span class="sxs-lookup"><span data-stu-id="d2309-112">System.AppUserModel.RelaunchCommand</span></span>](./props-system-appusermodel-relaunchcommand.md)
-   [<span data-ttu-id="d2309-113">System. Аппусермодел. Релаунчдисплайнамересаурце</span><span class="sxs-lookup"><span data-stu-id="d2309-113">System.AppUserModel.RelaunchDisplayNameResource</span></span>](./props-system-appusermodel-relaunchdisplaynameresource.md)
-   [<span data-ttu-id="d2309-114">System. Аппусермодел. Релаунчиконресаурце</span><span class="sxs-lookup"><span data-stu-id="d2309-114">System.AppUserModel.RelaunchIconResource</span></span>](./props-system-appusermodel-relaunchiconresource.md)

## <a name="windows-10-version-1703-windows-10-version-1607-windows-10-version-1511-windows-10-version-1507-windows-81-windows-8-windows-7"></a><span data-ttu-id="d2309-115">Windows 10, версия 1703, Windows 10, версия 1607, Windows 10, версия 1511, Windows 10, версия 1507, Windows 8.1, Windows 8, Windows 7</span><span class="sxs-lookup"><span data-stu-id="d2309-115">Windows 10, version 1703, Windows 10, version 1607, Windows 10, version 1511, Windows 10, version 1507, Windows 8.1, Windows 8, Windows 7</span></span>

```
propertyDescription
   name = System.AppUserModel.PreventPinning
   shellPKey = PKEY_AppUserModel_PreventPinning
   formatID = 9F4C2855-9F79-4B39-A8D0-E1D42DE1D5F3
   propID = 9
   SearchInfo
      InInvertedIndex = false
      IsColumn = false
   typeInfo
      type = Boolean
      IsInnate = false
```

## <a name="remarks"></a><span data-ttu-id="d2309-116">Комментарии</span><span class="sxs-lookup"><span data-stu-id="d2309-116">Remarks</span></span>

<span data-ttu-id="d2309-117">Значения PKEY определены в списке PKEY. h.</span><span class="sxs-lookup"><span data-stu-id="d2309-117">PKEY values are defined in Propkey.h.</span></span>

## <a name="related-topics"></a><span data-ttu-id="d2309-118">См. также</span><span class="sxs-lookup"><span data-stu-id="d2309-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d2309-119">Идентификаторы модели пользователя приложения (Аппусермоделидс)</span><span class="sxs-lookup"><span data-stu-id="d2309-119">Application User Model IDs (AppUserModelIDs)</span></span>](../shell/appids.md)
</dt> <dt>

[<span data-ttu-id="d2309-120">System.AppUserModel.ID</span><span class="sxs-lookup"><span data-stu-id="d2309-120">System.AppUserModel.ID</span></span>](./props-system-appusermodel-id.md)
</dt> <dt>

[<span data-ttu-id="d2309-121">**шжетпропертисторефорвиндов**</span><span class="sxs-lookup"><span data-stu-id="d2309-121">**SHGetPropertyStoreForWindow**</span></span>](/windows/desktop/api/Shellapi/nf-shellapi-shgetpropertystoreforwindow)
</dt> <dt>

[<span data-ttu-id="d2309-122">пропертидескриптионлист</span><span class="sxs-lookup"><span data-stu-id="d2309-122">propertyDescriptionList</span></span>](./propdesc-schema-propertydescriptionlist.md)
</dt> <dt>

[<span data-ttu-id="d2309-123">пропертидескриптион</span><span class="sxs-lookup"><span data-stu-id="d2309-123">propertyDescription</span></span>](./propdesc-schema-propertydescription.md)
</dt> <dt>

[<span data-ttu-id="d2309-124">сеарчинфо</span><span class="sxs-lookup"><span data-stu-id="d2309-124">searchInfo</span></span>](./propdesc-schema-searchinfo.md)
</dt> <dt>

[<span data-ttu-id="d2309-125">лабелинфо</span><span class="sxs-lookup"><span data-stu-id="d2309-125">labelInfo</span></span>](./propdesc-schema-labelinfo.md)
</dt> <dt>

[<span data-ttu-id="d2309-126">typeInfo</span><span class="sxs-lookup"><span data-stu-id="d2309-126">typeInfo</span></span>](./propdesc-schema-typeinfo.md)
</dt> <dt>

[<span data-ttu-id="d2309-127">displayInfo</span><span class="sxs-lookup"><span data-stu-id="d2309-127">displayInfo</span></span>](./propdesc-schema-displayinfo.md)
</dt> <dt>

[<span data-ttu-id="d2309-128">aliasInfo</span><span class="sxs-lookup"><span data-stu-id="d2309-128">aliasInfo</span></span>](./propdesc-schema-aliasinfo.md)
</dt> <dt>

[<span data-ttu-id="d2309-129">stringFormat</span><span class="sxs-lookup"><span data-stu-id="d2309-129">stringFormat</span></span>](./propdesc-schema-stringformat.md)
</dt> <dt>

[<span data-ttu-id="d2309-130">булеанформат</span><span class="sxs-lookup"><span data-stu-id="d2309-130">booleanFormat</span></span>](./propdesc-schema-booleanformat.md)
</dt> <dt>

[<span data-ttu-id="d2309-131">numberFormat</span><span class="sxs-lookup"><span data-stu-id="d2309-131">numberFormat</span></span>](./propdesc-schema-numberformat.md)
</dt> <dt>

[<span data-ttu-id="d2309-132">dateTimeFormat</span><span class="sxs-lookup"><span data-stu-id="d2309-132">dateTimeFormat</span></span>](./propdesc-schema-datetimeformat.md)
</dt> <dt>

[<span data-ttu-id="d2309-133">енумератедлист</span><span class="sxs-lookup"><span data-stu-id="d2309-133">enumeratedList</span></span>](./propdesc-schema-enumeratedlist.md)
</dt> <dt>

[<span data-ttu-id="d2309-134">enum</span><span class="sxs-lookup"><span data-stu-id="d2309-134">enum</span></span>](./propdesc-schema-enum.md)
</dt> <dt>

[<span data-ttu-id="d2309-135">енумранже</span><span class="sxs-lookup"><span data-stu-id="d2309-135">enumRange</span></span>](./propdesc-schema-enumrange.md)
</dt> <dt>

[<span data-ttu-id="d2309-136">image</span><span class="sxs-lookup"><span data-stu-id="d2309-136">image</span></span>](./propdesc-schema-image.md)
</dt> <dt>

[<span data-ttu-id="d2309-137">дравконтрол</span><span class="sxs-lookup"><span data-stu-id="d2309-137">drawControl</span></span>](./propdesc-schema-drawcontrol.md)
</dt> <dt>

[<span data-ttu-id="d2309-138">едитконтрол</span><span class="sxs-lookup"><span data-stu-id="d2309-138">editControl</span></span>](./propdesc-schema-editcontrol.md)
</dt> <dt>

[<span data-ttu-id="d2309-139">филтерконтрол</span><span class="sxs-lookup"><span data-stu-id="d2309-139">filterControl</span></span>](./propdesc-schema-filtercontrol.md)
</dt> <dt>

[<span data-ttu-id="d2309-140">куериконтрол</span><span class="sxs-lookup"><span data-stu-id="d2309-140">queryControl</span></span>](./propdesc-schema-querycontrol.md)
</dt> <dt>

[<span data-ttu-id="d2309-141">релатедпропертинфо</span><span class="sxs-lookup"><span data-stu-id="d2309-141">relatedPropertyInfo</span></span>](./propdesc-schema-relatedpropertyinfo.md)
</dt> <dt>

[<span data-ttu-id="d2309-142">relatedProperty</span><span class="sxs-lookup"><span data-stu-id="d2309-142">relatedProperty</span></span>](./propdesc-schema-relatedproperty.md)
</dt> </dl>

 

 
