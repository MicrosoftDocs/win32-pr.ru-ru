---
title: Перечисление Виевконтентс
description: Используется по содержимому Иресултсвиевер для указания или установки способа отображения текущего набора возвращаемых данных запроса.
ms.assetid: aebcbcac-4c45-4097-91a1-5e00611c152c
keywords:
- Перечисление Виевконтентс. устаревшие функции среды Windows
topic_type:
- apiref
api_name:
- ViewContents
api_location:
- WdsView.idl
api_type:
- IDLDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9f465b16ef81dd71695f8de0b04b6d7567480f4c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105699234"
---
# <a name="viewcontents-enumeration"></a>Перечисление Виевконтентс

> [!NOTE]
> Windows Desktop Search 2. x — это устаревшая технология, которая изначально была доступна в качестве надстройки для Windows XP и Windows Server 2003. В более поздних выпусках используйте [API поиска Windows](../search/-search-reference-entry-page.md) . 

Используется [**иресултсвиевер:: Content**](-search-2x-iresultsviewer-contents.md) , чтобы указать или задать способ отображения текущего набора возвращаемых данных запроса.

## <a name="syntax"></a>Синтаксис


```C++
typedef enum ViewContentsEnum { 
  ResultsDisplayed     = 0,
  ShellViewDisplayed   = 1,
  WebBrowserDisplayed  = 2
} ViewContents;
```



## <a name="constants"></a>Константы

<dl> <dt>

<span id="ResultsDisplayed"></span><span id="resultsdisplayed"></span><span id="RESULTSDISPLAYED"></span>**ресултсдисплайед**
</dt> <dd>

Указывает тип содержимого, отображаемого в представлении результатов.

</dd> <dt>

<span id="ShellViewDisplayed"></span><span id="shellviewdisplayed"></span><span id="SHELLVIEWDISPLAYED"></span>**шеллвиевдисплайед**
</dt> <dd>

Указывает, что тип содержимого, отображаемого в представлении результатов, в настоящее время установлен на представление оболочки.

</dd> <dt>

<span id="WebBrowserDisplayed"></span><span id="webbrowserdisplayed"></span><span id="WEBBROWSERDISPLAYED"></span>**веббровсердисплайед**
</dt> <dd>

Указывает, что тип содержимого, отображаемого в представлении результатов, в настоящее время установлен в представление браузера.

</dd> </dl>

## <a name="requirements"></a>Требования



| Требование | Значение |
|----------------|----------------------------------------------------------------------------------------|
| IDL<br/> | <dl> <dt>Вдсвиев. idl</dt> </dl> |



 

 





