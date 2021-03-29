---
title: Типы Wide-Character
description: Microsoft RPC поддерживает широкий тип символов WCHAR \_ t.
ms.assetid: 1a601461-df34-456d-93e8-4cf0b655cf2c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 821d69999a0ec7e175409120f223721defd6cd10
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104134263"
---
# <a name="wide-character-types"></a>Типы Wide-Character

Microsoft RPC поддерживает широкий тип символов [**WCHAR \_ t**](/windows/desktop/Midl/wchar-t). Тип расширенных символов использует 2 байта для каждого символа. Определение языка ANSI C позволяет инициализировать длинные и длинные строки следующим образом:

``` syntax
wchar_t wcInitial = L'a';
wchar_t * pwszString = L"Hello, world";
```

 

 