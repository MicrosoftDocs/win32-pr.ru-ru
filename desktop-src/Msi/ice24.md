---
description: ICE24 проверяет таблицу свойств в базе данных установщик Windows.
ms.assetid: 1250677b-691e-46bd-83e0-e349106c820b
title: ICE24
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fa3cbeb62285aa9c22a366647dbaeec9e54097a07bb4e876e6bff11bd435cdb0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119528994"
---
# <a name="ice24"></a>ICE24

ICE24 проверяет следующие свойства в [таблице свойств](property-table.md):

-   , Что свойство [**ProductCode**](productcode.md) является допустимым типом данных [GUID](guid.md) .
-   Свойство [**ProductVersion**](productversion.md) является допустимой версией продукта.
-   Свойство [**продуктлангуаже**](productlanguage.md) является допустимым типом [языковых](language.md) данных.

## <a name="result"></a>Результат

ICE24 отправляет сообщение об ошибке, если любое из этих свойств имеет тип, отличный от допустимого типа данных.

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Справочник по ICE](ice-reference.md)
</dt> </dl>

 

 



