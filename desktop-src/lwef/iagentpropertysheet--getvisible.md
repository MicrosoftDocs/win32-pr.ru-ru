---
title: Иажентпропертишит
description: Иажентпропертишит
ms.assetid: 5e95c4da-28a3-4686-8699-ff7b16b3808f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3ac95d1da3d1c0b4e5bf65c2f5f43c67153cc1d6af934e1814735abb12ed8d00
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117692306"
---
# <a name="iagentpropertysheetgetvisible"></a>Иажентпропертишит:: Visible

\[Microsoft Agent является устаревшим по отношению к Windows 7 и может быть недоступен в последующих версиях Windows.\]

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

## <a name="see-also"></a>См. также

[**Иажентпропертишит:: Сетвисибле**](iagentpropertysheet--setvisible.md)


 

 




