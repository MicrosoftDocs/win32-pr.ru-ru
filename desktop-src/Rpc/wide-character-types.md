---
title: Типы Wide-Character
description: Microsoft RPC поддерживает широкий тип символов WCHAR \_ t.
ms.assetid: 1a601461-df34-456d-93e8-4cf0b655cf2c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4eff57cf22e4836032acb59e1585da15285f55718b6c5b91733b1955ea85072a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119010402"
---
# <a name="wide-character-types"></a>Типы Wide-Character

Microsoft RPC поддерживает широкий тип символов [**WCHAR \_ t**](/windows/desktop/Midl/wchar-t). Тип расширенных символов использует 2 байта для каждого символа. Определение языка ANSI C позволяет инициализировать длинные и длинные строки следующим образом:

``` syntax
wchar_t wcInitial = L'a';
wchar_t * pwszString = L"Hello, world";
```

 

 