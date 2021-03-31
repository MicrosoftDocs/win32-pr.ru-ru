---
title: Директивы Pragma
description: Версия-кандидат не поддерживает директивы pragma, поддерживаемые компилятором C/C++.
ms.assetid: c7a944c0-a3d4-4568-a9ac-c338f0eaa427
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ab0c92136ba5e00d5b821d35ea05a337e7d6abe7
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "104069981"
---
# <a name="pragma-directives"></a>Директивы Pragma

Версия-кандидат не поддерживает директивы pragma, поддерживаемые компилятором C/C++. Однако версия-кандидат поддерживает следующую директиву pragma для изменения кодовой страницы:

``` syntax
#pragma code_page( [ DEFAULT | CodePageNum ] )
```

Эта директива pragma не поддерживается в включенном файле ресурсов (. RC). Поэтому, если у вас есть родительский RC-файл и он включает RC-файлы для нескольких языков, используйте эту директиву pragma перед включением другого RC-файла вместо использования его в самом файле прилагаемого RC-файла. Это продемонстрировано в следующем примере.

``` syntax
#include "English.rc"
#pragma code_page(932)
#include "Japanese.rc"
```

Список значений для Кодепаженум см. в разделе [идентификаторы кодовых страниц](../intl/code-page-identifiers.md).

 

 