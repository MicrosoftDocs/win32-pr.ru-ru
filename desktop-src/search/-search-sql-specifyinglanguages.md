---
description: Можно указать язык, используемый в поисковых запросах.
ms.assetid: 3a7ecf8f-38ae-41d1-be70-e9ab23977a01
title: Указание языков
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e50b3f65a41670989d41e235831ec8c008a6d8cb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104540663"
---
# <a name="specifying-languages"></a>Указание языков

Можно указать язык, используемый в поисковых запросах. Предикаты FREETEXT и CONTAINS в предложении WHERE поддерживают указание языка. Язык запроса можно указать, предоставив числовой идентификатор кода языка (LCID) в предикате CONTAINS или FREETEXT. Этот код языка определяет, какой средство разбиения по словам следует использовать для синтаксического анализа строки запроса. Для этого используется следующий синтаксис:


```
CONTAINS | FREETEXT
([<column_identifier>,]'<content_search_condition>' [,LCID]) 
```



Дополнительные сведения см. в описании синтаксиса предикатов [Contains](-search-sql-contains.md) и [FREETEXT](-search-sql-freetext.md) .

 

 



