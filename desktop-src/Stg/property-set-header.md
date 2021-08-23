---
title: Заголовок набора свойств
description: В начале потока набора свойств указан заголовок. Он состоит из индикатора порядка байтов, версии формата, исходной версии операционной системы, идентификатора класса (CLSID) и зарезервированного поля.
ms.assetid: 6f4531d5-99d8-43ff-b6c1-5975b7527fc0
keywords:
- структурированный служба хранилища заголовка набора свойств
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 506249ae917c6fbf00853a2547188a08ce14ebb29bc24d7e6daaa1aaa830cb3e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119662224"
---
# <a name="property-set-header"></a>Заголовок набора свойств

В начале потока набора свойств указан заголовок. Он состоит из индикатора порядка байтов, версии формата, исходной версии операционной системы, идентификатора класса (CLSID) и зарезервированного поля.

В следующей псевдо-структуре показан заголовок.

``` syntax
typedef struct tagPROPERTYSETHEADER 
{ 
    // Header 
    WORD   wByteOrder ;  // Always 0xFFFE 
    WORD   wFormat ;     // Always 0 
    DWORD   dwOSVer ;    // System version 
    CLSID  clsID ;       // Application CLSID 
    DWORD  reserved ;    // Should be 1 
} PROPERTYSETHEADER;
```

 

 




