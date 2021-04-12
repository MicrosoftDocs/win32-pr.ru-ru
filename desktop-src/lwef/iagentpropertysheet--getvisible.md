---
title: Иажентпропертишит
description: Иажентпропертишит
ms.assetid: 5e95c4da-28a3-4686-8699-ff7b16b3808f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bcda8be2a3ae3e4084087225e0d7ed79d33621a8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104330347"
---
# <a name="iagentpropertysheetgetvisible"></a>Иажентпропертишит:: Visible

\[Microsoft Agent является устаревшим в Windows 7 и может быть недоступен в последующих версиях Windows.\]

``` syntax
HRESULT GetVisible(
   long * pbVisible  // address of variable for property sheet
);                   // Visible setting
```

Определяет, является ли страница свойств Microsoft Agent видимой или скрытой.

-   Возвращает значение S \_ , чтобы указать, что операция выполнена успешно.

<dl> <dt>

<span id="pbVisible"></span><span id="pbvisible"></span><span id="PBVISIBLE"></span>*пбвисибле*
</dt> <dd>

Адрес переменной, которая получает **значение true** , если страница свойств является видимой, и **false** , если она скрыта.

</dd> </dl>

## <a name="see-also"></a>См. также:

[**Иажентпропертишит:: Сетвисибле**](iagentpropertysheet--setvisible.md)


 

 




