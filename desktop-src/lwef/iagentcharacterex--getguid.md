---
title: Иажентчарактерекс
description: Иажентчарактерекс
ms.assetid: 25fb2531-a81c-4add-8134-77b1cd57cfe3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1c9e0e14d0931774bf6ab5e1c8599bbebaadd0ed
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103986679"
---
# <a name="iagentcharacterexgetguid"></a>Иажентчарактерекс:: a GUID

\[Microsoft Agent является устаревшим в Windows 7 и может быть недоступен в последующих версиях Windows.\]

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

 

 




