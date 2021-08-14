---
description: Можно указать язык, используемый в поисковых запросах.
ms.assetid: 3a7ecf8f-38ae-41d1-be70-e9ab23977a01
title: Указание языков
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 13ab2b5b5c5da4e9f71e49330d966895415467a671289bd4f5607e1265d22a7f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118226819"
---
# <a name="specifying-languages"></a>Указание языков

Можно указать язык, используемый в поисковых запросах. Предикаты FREETEXT и CONTAINS в предложении WHERE поддерживают указание языка. Язык запроса можно указать, предоставив числовой идентификатор кода языка (LCID) в предикате CONTAINS или FREETEXT. Этот код языка определяет, какой средство разбиения по словам следует использовать для синтаксического анализа строки запроса. Для этого используется следующий синтаксис:


```
CONTAINS | FREETEXT
([<column_identifier>,]'<content_search_condition>' [,LCID]) 
```



Дополнительные сведения см. в описании синтаксиса предикатов [Contains](-search-sql-contains.md) и [FREETEXT](-search-sql-freetext.md) .

 

 



