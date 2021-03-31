---
title: Перемещение объектов
description: Перемещение объектов
ms.assetid: 3afdf480-a7ee-4b7b-99f6-4a8e8cb2096c
ms.tgt_platform: multiple
keywords:
- Active Directory примеры Active Directory, перемещение объектов
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7019904d0de42492b98ddd297ab007a6f4e52f6a
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/17/2020
ms.locfileid: "104069761"
---
# <a name="moving-objects"></a>Перемещение объектов

Чтобы переместить объект внутри домена, используйте метод [**иадсконтаинер. мовехере**](/windows/desktop/api/iads/nf-iads-iadscontainer-movehere) .

**Перемещение объекта в пределах домена**

1.  Выполните привязку к интерфейсу [**iAds**](/windows/desktop/api/iads/nn-iads-iads) объекта, который необходимо переместить.
2.  Получите путь к объекту для перемещения из свойства [**iAds. ADsPath**](/windows/desktop/ADSI/iads-property-methods) .
3.  Выполните привязку к интерфейсу [**иадсконтаинер**](/windows/desktop/api/iads/nn-iads-iadscontainer) контейнера, в который будет перемещен объект.
4.  Переместите объект с помощью метода [**иадсконтаинер. мовехере**](/windows/desktop/api/iads/nf-iads-iadscontainer-movehere) .

Если интерфейс существует для перемещенного объекта, интерфейс недействителен после перемещения объекта, поскольку объект каталога, представленный интерфейсом, больше не существует.

Дополнительные сведения и пример кода, демонстрирующий перемещение объекта, см. в разделе [пример кода для перемещения объекта](example-code-for-moving-an-object.md).

 

 