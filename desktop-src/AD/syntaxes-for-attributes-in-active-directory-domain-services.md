---
title: Синтаксис атрибутов в домен Active Directory Services
description: Домен Active Directory Services определяют набор синтаксисов атрибутов для указания типа данных, содержащихся в атрибуте.
ms.assetid: 79d27d47-5d03-4ad6-bf97-c387c34fa454
ms.tgt_platform: multiple
keywords:
- Синтаксис для атрибутов домен Active Directory Services Active Directory
- Атрибуты Active Directory, синтаксис для
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 04386e1b4981a81585fe208afa4cca6ed02d4c3c
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/17/2020
ms.locfileid: "104133647"
---
# <a name="syntaxes-for-attributes-in-active-directory-domain-services"></a>Синтаксис атрибутов в домен Active Directory Services

Домен Active Directory Services определяют набор синтаксисов атрибутов для указания типа данных, содержащихся в атрибуте. Предопределенные синтаксисы фактически не отображаются в каталоге и не могут добавлять новые синтаксисы. Для обнаружения синтаксиса класса атрибута можно использовать несколько методов:

-   Методы [**iAds. Get**](/windows/desktop/api/iads/nf-iads-iads-get), [**iAds. жетекс**](/windows/desktop/api/iads/nf-iads-iads-getex), [**iAds.**](/windows/desktop/api/iads/nf-iads-iads-put)WHERE и [**iAds. путекс**](/windows/desktop/api/iads/nf-iads-iads-putex) используют структуру [**Variant**](/windows/win32/api/oaidl/ns-oaidl-variant) для получения и задания значений атрибутов объекта. Элемент **VT** этой структуры является значением **VarType** , определяющим тип данных.
-   Методы интерфейсов [**идиректорйобжект**](/windows/desktop/api/iads/nn-iads-idirectoryobject) и [**IDirectorySearch**](/windows/desktop/api/iads/nn-iads-idirectorysearch) используют значение из перечисления [**адстипинум**](/windows/win32/api/iads/ne-iads-adstypeenum) для указания типа данных.
-   Чтобы указать синтаксис нового класса атрибута, установите атрибуты [**attributeSyntax**](/windows/desktop/ADSchema/a-attributesyntax) и [**oMSyntax**](/windows/desktop/ADSchema/a-omsyntax) объекта [**attributeSchema**](/windows/desktop/ADSchema/c-attributeschema) . Если значение **oMSyntax** равно 127, необходимо также задать атрибут [**омобжекткласс**](/windows/desktop/ADSchema/a-omobjectclass) . Дополнительные сведения см. [в разделе Выбор синтаксиса](choosing-a-syntax.md).

Полный список синтаксиса, предоставляемого домен Active Directory Services, включая соответствующие значения **VarType** и [**адстипинум**](/windows/win32/api/iads/ne-iads-adstypeenum) для каждого синтаксиса, см. в разделе [синтаксисы](/windows/desktop/ADSchema/syntaxes).

 

 