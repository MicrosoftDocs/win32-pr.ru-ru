---
description: В следующих примерах для создания специальных записей BLOB-объектов используется функция Сетстрингинблоб.
ms.assetid: 4a921b0d-9934-48e2-8837-be0bd7b7fa7a
title: Специальные записи BLOB-объектов
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b0659fa05219dcc715c6c00b3d28635e2500f73e4e5bece72049ee43839a0820
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118363142"
---
# <a name="special-blob-entries"></a>Специальные записи BLOB-объектов

В следующих примерах для создания специальных записей BLOB-объектов используется функция [**сетстрингинблоб**](setstringinblob.md) .

## <a name="npp-name"></a>Имя НПП

``` syntax
SetStringInBlob(
   hBlob,
   OWNER_NPP,
   CATEGORY_LOCATION,
   TAG_NAME,
   "My NPP Name"); 
```

## <a name="npp-class-identifier"></a>Идентификатор класса НПП

``` syntax
SetClassIDInBlob(
   hBlob,
   OWNER_NPP,
   CATEGORY_LOCATION,
   TAG_CLASSID,
   &CLSID_ThisNPP);
```

## <a name="cfgproc-procedure-name"></a>Имя процедуры КФГПРОК

``` syntax
SetStringInBlob(
   hBlob,
   OWNER_NPP,
   CATEGORY_FINDER,
   TAG_PROCNAME,
   "MyGetNPPBlobs");
```

## <a name="tree-root-name-for-finder-ui"></a>Корневое имя дерева для пользовательского интерфейса Finder

``` syntax
SetStringInBlob(
   hBlob,
   OWNER_NPP,
   CATEGORY_FINDER,
   TAG_ROOT,
   "My Tree Root name");
```

## <a name="display-string-for-finder-ui"></a>Отображение строки для пользовательского интерфейса Finder

``` syntax
SetStringInBlob(
   hBlob,
   OWNER_NPP,
   CATEGORY_FINDER,
   TAG_DISP_STRING,
   "Double click to select my UI");
```

## <a name="interface-tags"></a>Теги интерфейса

Этот пример включает все интерфейсы, поддерживаемые НПП.

``` syntax
SetBoolInBlob(  
   hBlob,
   OWNER_NPP,
   CATEGORY_CONFIG,
   TAG_INTERFACE_REALTIME_CAPTURE,
   TRUE);
```

 

 



