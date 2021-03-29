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
ms.openlocfilehash: 10c7b1dca9882f53b7fa746121ed431ace7f9af7
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "105654153"
---
# <a name="adsi-properties-and-attributes"></a>Свойства и атрибуты ADSI

Атрибуты иногда называют свойствами. Это может вызвать путаницу. В этой документации используются следующие определения свойств и атрибутов.

Свойства представляют собой именованные значения, связанные с программным объектом. Например, интерфейс [**iAds**](/windows/desktop/api/Iads/nn-iads-iads) предоставляет такие свойства, как [**класс**](iads-property-methods.md) и **имя**.

Атрибуты — это данные, связанные с объектами в службе каталогов. Например, объект пользователя будет иметь атрибут **CN** , который содержит строку, представляющую общее или относительное различающееся имя объекта. Атрибуты доступны через методы интерфейса ADSI, такие как [**iAds. Get**](/windows/desktop/api/Iads/nf-iads-iads-get) и [**iAds. Постановка**](/windows/desktop/api/Iads/nf-iads-iads-put).

Дополнительные сведения о свойствах и атрибутах ADSI см. в следующих статьях:

-   [Кэш атрибутов ADSI](the-adsi-attribute-cache.md)
-   [Сравнение одного и нескольких атрибутов значений](single-vs--multiple-value-attributes.md)
-   [Active Directory операционные атрибуты](active-directory-operational-attributes.md)

 

 




