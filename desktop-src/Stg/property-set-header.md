---
title: Заголовок набора свойств
description: В начале потока набора свойств указан заголовок. Он состоит из индикатора порядка байтов, версии формата, исходной версии операционной системы, идентификатора класса (CLSID) и зарезервированного поля.
ms.assetid: 6f4531d5-99d8-43ff-b6c1-5975b7527fc0
keywords:
- Структурированное хранилище заголовка набора свойств
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8f8d66eeec6525414ba3c6f0a0bb4f4fa34431c6
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104332728"
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

 

 




