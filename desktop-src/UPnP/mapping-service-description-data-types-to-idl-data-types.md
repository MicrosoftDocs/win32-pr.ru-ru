---
title: Сопоставление типов данных описания службы с типами данных IDL
description: В следующей таблице показано сопоставление типов данных XML, указанных в описании службы, с соответствующими типами данных, используемыми в IDL.
ms.assetid: eeb86177-8c3b-47f1-bbe1-f9aabd2dde76
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d6b5fac697c41f54279ecde7436900434895ff23
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104068437"
---
# <a name="mapping-service-description-data-types-to-idl-data-types"></a>Сопоставление типов данных описания службы с типами данных IDL

В следующей таблице показано сопоставление типов данных XML, указанных в описании службы, с соответствующими типами данных, используемыми в IDL.



| Тип данных XML | Тип данных IDL  |
|---------------|----------------|
| bin.base64    | SAFEARRAY      |
| bin.hex       | SAFEARRAY      |
| Логическое       | VARIANT \_ bool  |
| char          | WCHAR \_ t       |
| Дата          | DATE           |
| dateTime      | DATE           |
| dateTime.tz   | DATE           |
| fixed.14.4    | CY             |
| FLOAT         | FLOAT          |
| i1            | char           |
| i2            | short          |
| i4            | long           |
| INT           | long           |
| number        | BSTR           |
| r4            | FLOAT          |
| r8            | double         |
| строка        | BSTR           |
| time          | DATE           |
| time.tz       | DATE           |
| ui1           | unsigned char  |
| ui2           | unsigned short |
| ui4           | unsigned long  |
| uri           | BSTR           |
| uuid          | BSTR           |



 

 

 




