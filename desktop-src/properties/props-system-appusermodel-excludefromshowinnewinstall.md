---
description: Предотвращает получение выделенной записи в меню "Пуск" для вновь установленного ярлыка приложения.
ms.assetid: ff85da6f-a506-4225-8ac9-4a8a7be8d599
title: System. Аппусермодел. Ексклудефромшовинневинсталл
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 206cbbc6b07b0d3fec5833c046d4cb44c1e5e4e5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105702253"
---
# <a name="systemappusermodelexcludefromshowinnewinstall"></a><span data-ttu-id="0d46d-103">System. Аппусермодел. Ексклудефромшовинневинсталл</span><span class="sxs-lookup"><span data-stu-id="0d46d-103">System.AppUserModel.ExcludeFromShowInNewInstall</span></span>

<span data-ttu-id="0d46d-104">Предотвращает получение выделенной записи в меню " **Пуск** " для вновь установленного ярлыка приложения.</span><span class="sxs-lookup"><span data-stu-id="0d46d-104">Prevents a **Start** menu entry for a newly installed application shortcut from receiving a highlight.</span></span> <span data-ttu-id="0d46d-105">Это эквивалентно сбросу параметра **выделить недавно установленные программы** в окне **Настройка меню "Пуск** " для отдельного элемента.</span><span class="sxs-lookup"><span data-stu-id="0d46d-105">This is equivalent to clearing the **Highlight newly installed programs** option in the **Customize Start Menu** window on an individual item.</span></span> <span data-ttu-id="0d46d-106">Это свойство должно быть задано для сочетаний клавиш для средств и вторичных приложений.</span><span class="sxs-lookup"><span data-stu-id="0d46d-106">This property should be set on shortcuts for tools and secondary applications.</span></span>

> [!Note]  
> <span data-ttu-id="0d46d-107">Это свойство используется только в меню Пуск в Windows Vista и Windows 7.</span><span class="sxs-lookup"><span data-stu-id="0d46d-107">This property is property is only used by the Start menu on Windows Vista and Windows 7.</span></span> <span data-ttu-id="0d46d-108">Свойство не используется начальным экраном или меню "Пуск" в Windows 8 и более поздних версиях</span><span class="sxs-lookup"><span data-stu-id="0d46d-108">The property is not used by the Start screen or Start menu on Windows 8 and later</span></span>

 

<span data-ttu-id="0d46d-109">.</span><span class="sxs-lookup"><span data-stu-id="0d46d-109">.</span></span>

## <a name="windows-10-version-1703-windows-10-version-1607-windows-10-version-1511-windows-10-version-1507-windows-81-windows-8-windows-7"></a><span data-ttu-id="0d46d-110">Windows 10, версия 1703, Windows 10, версия 1607, Windows 10, версия 1511, Windows 10, версия 1507, Windows 8.1, Windows 8, Windows 7</span><span class="sxs-lookup"><span data-stu-id="0d46d-110">Windows 10, version 1703, Windows 10, version 1607, Windows 10, version 1511, Windows 10, version 1507, Windows 8.1, Windows 8, Windows 7</span></span>

```
propertyDescription
   name = System.AppUserModel.ExcludeFromShowInNewInstall
   shellPKey = PKEY_AppUserModel_ExcludeFromShowInNewInstall
   formatID = 9F4C2855-9F79-4B39-A8D0-E1D42DE1D5F3
   propID = 8
   SearchInfo
      InInvertedIndex = false
      IsColumn = false
   typeInfo
      type = Boolean
      IsInnate = false
```

## <a name="remarks"></a><span data-ttu-id="0d46d-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="0d46d-111">Remarks</span></span>

<span data-ttu-id="0d46d-112">Значения PKEY определены в списке PKEY. h.</span><span class="sxs-lookup"><span data-stu-id="0d46d-112">PKEY values are defined in Propkey.h.</span></span>

## <a name="related-topics"></a><span data-ttu-id="0d46d-113">См. также</span><span class="sxs-lookup"><span data-stu-id="0d46d-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0d46d-114">Идентификаторы модели пользователя приложения (Аппусермоделидс)</span><span class="sxs-lookup"><span data-stu-id="0d46d-114">Application User Model IDs (AppUserModelIDs)</span></span>](../shell/appids.md)
</dt> <dt>

[<span data-ttu-id="0d46d-115">System.AppUserModel.ID</span><span class="sxs-lookup"><span data-stu-id="0d46d-115">System.AppUserModel.ID</span></span>](./props-system-appusermodel-id.md)
</dt> <dt>

[<span data-ttu-id="0d46d-116">**шжетпропертисторефорвиндов**</span><span class="sxs-lookup"><span data-stu-id="0d46d-116">**SHGetPropertyStoreForWindow**</span></span>](/windows/desktop/api/Shellapi/nf-shellapi-shgetpropertystoreforwindow)
</dt> <dt>

[<span data-ttu-id="0d46d-117">пропертидескриптионлист</span><span class="sxs-lookup"><span data-stu-id="0d46d-117">propertyDescriptionList</span></span>](./propdesc-schema-propertydescriptionlist.md)
</dt> <dt>

[<span data-ttu-id="0d46d-118">пропертидескриптион</span><span class="sxs-lookup"><span data-stu-id="0d46d-118">propertyDescription</span></span>](./propdesc-schema-propertydescription.md)
</dt> <dt>

[<span data-ttu-id="0d46d-119">сеарчинфо</span><span class="sxs-lookup"><span data-stu-id="0d46d-119">searchInfo</span></span>](./propdesc-schema-searchinfo.md)
</dt> <dt>

[<span data-ttu-id="0d46d-120">лабелинфо</span><span class="sxs-lookup"><span data-stu-id="0d46d-120">labelInfo</span></span>](./propdesc-schema-labelinfo.md)
</dt> <dt>

[<span data-ttu-id="0d46d-121">typeInfo</span><span class="sxs-lookup"><span data-stu-id="0d46d-121">typeInfo</span></span>](./propdesc-schema-typeinfo.md)
</dt> <dt>

[<span data-ttu-id="0d46d-122">displayInfo</span><span class="sxs-lookup"><span data-stu-id="0d46d-122">displayInfo</span></span>](./propdesc-schema-displayinfo.md)
</dt> <dt>

[<span data-ttu-id="0d46d-123">aliasInfo</span><span class="sxs-lookup"><span data-stu-id="0d46d-123">aliasInfo</span></span>](./propdesc-schema-aliasinfo.md)
</dt> <dt>

[<span data-ttu-id="0d46d-124">stringFormat</span><span class="sxs-lookup"><span data-stu-id="0d46d-124">stringFormat</span></span>](./propdesc-schema-stringformat.md)
</dt> <dt>

[<span data-ttu-id="0d46d-125">булеанформат</span><span class="sxs-lookup"><span data-stu-id="0d46d-125">booleanFormat</span></span>](./propdesc-schema-booleanformat.md)
</dt> <dt>

[<span data-ttu-id="0d46d-126">numberFormat</span><span class="sxs-lookup"><span data-stu-id="0d46d-126">numberFormat</span></span>](./propdesc-schema-numberformat.md)
</dt> <dt>

[<span data-ttu-id="0d46d-127">dateTimeFormat</span><span class="sxs-lookup"><span data-stu-id="0d46d-127">dateTimeFormat</span></span>](./propdesc-schema-datetimeformat.md)
</dt> <dt>

[<span data-ttu-id="0d46d-128">енумератедлист</span><span class="sxs-lookup"><span data-stu-id="0d46d-128">enumeratedList</span></span>](./propdesc-schema-enumeratedlist.md)
</dt> <dt>

[<span data-ttu-id="0d46d-129">enum</span><span class="sxs-lookup"><span data-stu-id="0d46d-129">enum</span></span>](./propdesc-schema-enum.md)
</dt> <dt>

[<span data-ttu-id="0d46d-130">енумранже</span><span class="sxs-lookup"><span data-stu-id="0d46d-130">enumRange</span></span>](./propdesc-schema-enumrange.md)
</dt> <dt>

[<span data-ttu-id="0d46d-131">image</span><span class="sxs-lookup"><span data-stu-id="0d46d-131">image</span></span>](./propdesc-schema-image.md)
</dt> <dt>

[<span data-ttu-id="0d46d-132">дравконтрол</span><span class="sxs-lookup"><span data-stu-id="0d46d-132">drawControl</span></span>](./propdesc-schema-drawcontrol.md)
</dt> <dt>

[<span data-ttu-id="0d46d-133">едитконтрол</span><span class="sxs-lookup"><span data-stu-id="0d46d-133">editControl</span></span>](./propdesc-schema-editcontrol.md)
</dt> <dt>

[<span data-ttu-id="0d46d-134">филтерконтрол</span><span class="sxs-lookup"><span data-stu-id="0d46d-134">filterControl</span></span>](./propdesc-schema-filtercontrol.md)
</dt> <dt>

[<span data-ttu-id="0d46d-135">куериконтрол</span><span class="sxs-lookup"><span data-stu-id="0d46d-135">queryControl</span></span>](./propdesc-schema-querycontrol.md)
</dt> <dt>

[<span data-ttu-id="0d46d-136">релатедпропертинфо</span><span class="sxs-lookup"><span data-stu-id="0d46d-136">relatedPropertyInfo</span></span>](./propdesc-schema-relatedpropertyinfo.md)
</dt> <dt>

[<span data-ttu-id="0d46d-137">relatedProperty</span><span class="sxs-lookup"><span data-stu-id="0d46d-137">relatedProperty</span></span>](./propdesc-schema-relatedproperty.md)
</dt> <dt>

<span data-ttu-id="0d46d-138">[стартпиноптион](/previous-versions//jj553605(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="0d46d-138">[startPinOption](/previous-versions//jj553605(v=vs.85))</span></span>
</dt> </dl>

 

 
