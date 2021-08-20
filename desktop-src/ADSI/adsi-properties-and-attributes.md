---
title: Свойства и атрибуты ADSI
description: Атрибуты иногда называют свойствами. Это может вызвать путаницу. В этой документации используются следующие определения свойств и атрибутов.
ms.assetid: 8e391d36-5a8d-4960-805a-0caf281cab80
ms.tgt_platform: multiple
keywords:
- Свойства ADSI и атрибуты ADSI
- ADSI ADSI, использование, доступ к данным, свойствам и атрибутам и управление ими
- свойства ADSI
- атрибуты ADSI
- свойства ADSI, определение
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b05637cada9a62cee129e9645385233b4700cbf2762b9446ba9a871d1897d440
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119082798"
---
# <a name="adsi-properties-and-attributes"></a>Свойства и атрибуты ADSI

Атрибуты иногда называют свойствами. Это может вызвать путаницу. В этой документации используются следующие определения свойств и атрибутов.

Свойства представляют собой именованные значения, связанные с программным объектом. Например, интерфейс [**iAds**](/windows/desktop/api/Iads/nn-iads-iads) предоставляет такие свойства, как [**класс**](iads-property-methods.md) и **имя**.

Атрибуты — это данные, связанные с объектами в службе каталогов. Например, объект пользователя будет иметь атрибут **CN** , который содержит строку, представляющую общее или относительное различающееся имя объекта. Атрибуты доступны через методы интерфейса ADSI, такие как [**iAds. Get**](/windows/desktop/api/Iads/nf-iads-iads-get) и [**iAds. Постановка**](/windows/desktop/api/Iads/nf-iads-iads-put).

Дополнительные сведения о свойствах и атрибутах ADSI см. в следующих статьях:

-   [Кэш атрибутов ADSI](the-adsi-attribute-cache.md)
-   [Сравнение одного и нескольких атрибутов значений](single-vs--multiple-value-attributes.md)
-   [Active Directory операционные атрибуты](active-directory-operational-attributes.md)

 

 




