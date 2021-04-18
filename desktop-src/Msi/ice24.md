---
description: ICE24 проверяет таблицу свойств в базе данных установщик Windows.
ms.assetid: 1250677b-691e-46bd-83e0-e349106c820b
title: ICE24
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 193af1e53a3274d1d1307f132fe066ca8940c282
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105650932"
---
# <a name="ice24"></a>ICE24

ICE24 проверяет следующие свойства в [таблице свойств](property-table.md):

-   , Что свойство [**ProductCode**](productcode.md) является допустимым типом данных [GUID](guid.md) .
-   Свойство [**ProductVersion**](productversion.md) является допустимой версией продукта.
-   Свойство [**продуктлангуаже**](productlanguage.md) является допустимым типом [языковых](language.md) данных.

## <a name="result"></a>Результат

ICE24 отправляет сообщение об ошибке, если любое из этих свойств имеет тип, отличный от допустимого типа данных.

## <a name="related-topics"></a>См. также

<dl> <dt>

[Справочник по ICE](ice-reference.md)
</dt> </dl>

 

 



