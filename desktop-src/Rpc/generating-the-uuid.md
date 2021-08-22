---
title: Создание UUID
description: Первым шагом в определении интерфейса является использование служебной программы uuidgen для создания универсального уникального идентификатора (UUID).
ms.assetid: 870641b7-affc-4de4-bc7f-4c8ca2873fb6
keywords:
- Удаленный вызов процедур RPC, задачи, создание UUID
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 21c1fbb257a4ce41a4fc0159f703a01705b4dd5926356d7850ec4ce1e0d2e002
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118929531"
---
# <a name="generating-the-uuid"></a>Создание UUID

Первым шагом в определении интерфейса является использование служебной программы **uuidgen** для создания универсального уникального идентификатора (UUID). Идентификатор UUID позволяет клиентским и серверным приложениям однозначно находить друг друга. Программа **uuidgen** (Uuidgen.exe) автоматически устанавливается при установке пакета SDK для платформы.

Следующая команда создает UUID и создает файл шаблона с именем Hello. idl.

**uuidgen/i/Охелло.ИДЛ**

Шаблон Hello. idl будет выглядеть так (с другим UUID, конечно).

``` syntax
[
    uuid(7a98c250-6808-11cf-b73b-00aa00b677a7),
    version(1.0)
]
interface INTERFACENAME
{
 
}
```

 

 




