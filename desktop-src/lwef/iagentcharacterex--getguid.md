---
title: Иажентчарактерекс
description: Иажентчарактерекс
ms.assetid: 25fb2531-a81c-4add-8134-77b1cd57cfe3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1e43a98617b1e2d25a25167ad5b95462eeb462f40f5a353b5a5ec45ffb3a9cca
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118477972"
---
# <a name="iagentcharacterexgetguid"></a>Иажентчарактерекс:: a GUID

\[Microsoft Agent является устаревшим по отношению к Windows 7 и может быть недоступен в последующих версиях Windows.\]

``` syntax
HRESULT GetGUID(
   BSTR * pbszGUID  // address of character's ID
);
```

Возвращает уникальный идентификатор для символа.

-   Возвращает значение S \_ , чтобы указать, что операция выполнена успешно.

<dl> <dt>

<span id="pbszGUID"></span><span id="pbszguid"></span><span id="PBSZGUID"></span>*пбсзгуид*
</dt> <dd>

Адрес объекта BSTR, который получает идентификатор для символа.

</dd> </dl>

Свойство возвращает строковое представление GUID (в формате, заключенном в фигурные скобки и тире), которое используется сервером для уникальной идентификации символа. Идентификатор символа задается при компиляции с помощью редактора символов Microsoft Agent. свойство доступно только для чтения.

 

 




