---
description: В следующих примерах для создания специальных записей BLOB-объектов используется функция Сетстрингинблоб.
ms.assetid: 4a921b0d-9934-48e2-8837-be0bd7b7fa7a
title: Специальные записи BLOB-объектов
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5cfc40029e0a0f88c2f7bd242881b0d750a5dfa1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103810282"
---
# <a name="special-blob-entries"></a><span data-ttu-id="52a36-103">Специальные записи BLOB-объектов</span><span class="sxs-lookup"><span data-stu-id="52a36-103">Special BLOB Entries</span></span>

<span data-ttu-id="52a36-104">В следующих примерах для создания специальных записей BLOB-объектов используется функция [**сетстрингинблоб**](setstringinblob.md) .</span><span class="sxs-lookup"><span data-stu-id="52a36-104">The following examples use the [**SetStringInBlob**](setstringinblob.md) function to create special BLOB entries.</span></span>

## <a name="npp-name"></a><span data-ttu-id="52a36-105">Имя НПП</span><span class="sxs-lookup"><span data-stu-id="52a36-105">NPP Name</span></span>

``` syntax
SetStringInBlob(
   hBlob,
   OWNER_NPP,
   CATEGORY_LOCATION,
   TAG_NAME,
   "My NPP Name"); 
```

## <a name="npp-class-identifier"></a><span data-ttu-id="52a36-106">Идентификатор класса НПП</span><span class="sxs-lookup"><span data-stu-id="52a36-106">NPP Class Identifier</span></span>

``` syntax
SetClassIDInBlob(
   hBlob,
   OWNER_NPP,
   CATEGORY_LOCATION,
   TAG_CLASSID,
   &CLSID_ThisNPP);
```

## <a name="cfgproc-procedure-name"></a><span data-ttu-id="52a36-107">Имя процедуры КФГПРОК</span><span class="sxs-lookup"><span data-stu-id="52a36-107">CFGPROC Procedure Name</span></span>

``` syntax
SetStringInBlob(
   hBlob,
   OWNER_NPP,
   CATEGORY_FINDER,
   TAG_PROCNAME,
   "MyGetNPPBlobs");
```

## <a name="tree-root-name-for-finder-ui"></a><span data-ttu-id="52a36-108">Корневое имя дерева для пользовательского интерфейса Finder</span><span class="sxs-lookup"><span data-stu-id="52a36-108">Tree Root Name for Finder UI</span></span>

``` syntax
SetStringInBlob(
   hBlob,
   OWNER_NPP,
   CATEGORY_FINDER,
   TAG_ROOT,
   "My Tree Root name");
```

## <a name="display-string-for-finder-ui"></a><span data-ttu-id="52a36-109">Отображение строки для пользовательского интерфейса Finder</span><span class="sxs-lookup"><span data-stu-id="52a36-109">Display String for Finder UI</span></span>

``` syntax
SetStringInBlob(
   hBlob,
   OWNER_NPP,
   CATEGORY_FINDER,
   TAG_DISP_STRING,
   "Double click to select my UI");
```

## <a name="interface-tags"></a><span data-ttu-id="52a36-110">Теги интерфейса</span><span class="sxs-lookup"><span data-stu-id="52a36-110">Interface Tags</span></span>

<span data-ttu-id="52a36-111">Этот пример включает все интерфейсы, поддерживаемые НПП.</span><span class="sxs-lookup"><span data-stu-id="52a36-111">This example includes every interface supported by the NPP.</span></span>

``` syntax
SetBoolInBlob(  
   hBlob,
   OWNER_NPP,
   CATEGORY_CONFIG,
   TAG_INTERFACE_REALTIME_CAPTURE,
   TRUE);
```

 

 



