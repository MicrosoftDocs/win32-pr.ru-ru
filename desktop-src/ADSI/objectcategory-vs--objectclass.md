---
title: objectCategory и objectClass
description: Атрибуты objectCategory и objectClass могут ссылаться на данный класс схемы объекта Directory.
ms.assetid: 66dadedb-61e4-4184-9b87-0fff036a94d9
ms.tgt_platform: multiple
keywords:
- objectCategory и objectClass ADSI
- атрибуты Аси, поиск по атрибутам objectCategory и objectClass
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0d3833f8cf26cb2272fbe1e7c1063322f39a8c0147e4b22382d26067f90e72e6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117839224"
---
# <a name="objectcategory-vs-objectclass"></a>objectCategory и objectClass

Атрибуты **objectCategory** и **objectClass** могут ссылаться на данный класс схемы объекта Directory. Однако существует важное различие между ними в семантике. "objectClass = радости" относится к таким объектам каталога, в которых "радость" представляет любой класс в иерархии классов объектов. «objectCategory = радости», с другой стороны, относится к объектам каталога, в которых «радость» определяет конкретный класс в иерархии классов объектов.

**objectClass** может принимать несколько значений, тогда как **objectCategory** принимает одно значение. По этой причине **objectCategory** лучше подходит для сопоставления типов объектов в поиске по каталогу. ADSI использует его в качестве критерия сопоставления по умолчанию. Поиск, использующий один **objectClass** , не масштабируется до больших баз данных. ADSI поддерживает синтаксис "(objectCategory = Сомедн)" и "(objectCategory = \_ отображаемое \_ имя LDAP \_ для \_ класса)".

Исключением является то, что фильтр поиска LDAP "(objectClass = \* )" не задает поиск в классе Object, а только проверяет наличие объектов.

 

 




