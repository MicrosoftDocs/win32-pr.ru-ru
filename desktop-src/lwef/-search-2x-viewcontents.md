---
title: Перечисление Виевконтентс
description: Используется по содержимому Иресултсвиевер для указания или установки способа отображения текущего набора возвращаемых данных запроса.
ms.assetid: aebcbcac-4c45-4097-91a1-5e00611c152c
keywords:
- виевконтентс перечисления устаревших компонентов среды Windows
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
ms.openlocfilehash: 2070b68ec62a8dd6ca86758b98a6399ee41180eaad24613d17d0825a927b1871
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119829114"
---
# <a name="viewcontents-enumeration"></a>Перечисление Виевконтентс

> [!NOTE]
> Windows настольный поиск 2. x — это устаревшая технология, которая изначально была доступна в качестве надстройки для Windows XP и Windows Server 2003. в более поздних выпусках используйте вместо этого [API Windows поиска](../search/-search-reference-entry-page.md) . 

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



 

 





