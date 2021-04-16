---
title: Создание и удаление объектов
description: При использовании ADSI объекты создаются и удаляются с помощью интерфейса Иадсконтаинер или Идиректорйобжект.
ms.assetid: 4d1f7ac5-48d3-4ea9-91e4-0cd4bb2ec9f8
ms.tgt_platform: multiple
keywords:
- Создание и удаление объектов ADSI
- ADSI, создание и удаление объектов
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4730c4cc6a95ad37bfd3953474d3d488fcf05abb
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/21/2020
ms.locfileid: "104488280"
---
# <a name="creating-and-deleting-objects"></a>Создание и удаление объектов

При использовании ADSI объекты создаются и удаляются с помощью интерфейса [**иадсконтаинер**](/windows/desktop/api/Iads/nn-iads-iadscontainer) или [**идиректорйобжект**](/windows/desktop/api/Iads/nn-iads-idirectoryobject) .

## <a name="creating-an-object-with-iadscontainer"></a>Создание объекта с помощью Иадсконтаинер

**Создание объекта с помощью интерфейса Иадсконтаинер**

1.  Выполните привязку к контейнеру, который будет содержать создаваемый объект, и получите интерфейс [**иадсконтаинер**](/windows/desktop/api/Iads/nn-iads-iadscontainer) .
2.  Используйте метод [**иадсконтаинер. Create**](/windows/desktop/api/Iads/nf-iads-iadscontainer-create) , чтобы создать новый объект в контейнере.
3.  Задайте значения для всех необходимых атрибутов объекта с помощью метода [**iAds.**](/windows/desktop/api/Iads/nf-iads-iads-put) WHERE или [**iAds. путекс**](/windows/desktop/api/Iads/nf-iads-iads-putex) . Атрибуты, необходимые для создания объекта, зависят от службы каталогов и типа создаваемого объекта. Дополнительные сведения о создании Active Directory объектов см. в разделе [Создание и удаление объектов Active Directory](/windows/desktop/AD/creating-and-deleting-objects-in-active-directory-domain-services).
4.  Задайте значения для всех требуемых дополнительных атрибутов объекта с помощью метода [**iAds.**](/windows/desktop/api/Iads/nf-iads-iads-put) WHERE или [**iAds. путекс**](/windows/desktop/api/Iads/nf-iads-iads-putex) .
5.  Вызовите метод [**iAds. сетинфо**](/windows/desktop/api/Iads/nf-iads-iads-setinfo) , чтобы зафиксировать объект и его атрибуты. Новый объект фактически не создается в базовой службе каталогов до тех пор, пока не будет вызван метод **iAds. сетинфо** для фиксации атрибутов.

## <a name="creating-an-object-with-idirectoryobject"></a>Создание объекта с помощью Идиректорйобжект

**Создание объекта с помощью интерфейса Идиректорйобжект**

1.  Выполните привязку к контейнеру, который будет содержать создаваемый объект, и получите интерфейс [**идиректорйобжект**](/windows/desktop/api/Iads/nn-iads-idirectoryobject) .
2.  Выделите массив структур [**\_ \_ сведений attr**](/windows/desktop/api/Iads/ns-iads-ads_attr_info) , содержащий одну структуру для каждого атрибута, который должен быть задан при создании объекта.
3.  Заполните [**структуру \_ \_ сведений attr ADS**](/windows/desktop/api/Iads/ns-iads-ads_attr_info) для каждого обязательного атрибута объекта. Атрибуты, необходимые для создания объекта, зависят от службы каталогов и типа создаваемого объекта. Дополнительные сведения о создании Active Directory объектов см. в разделе [Создание и удаление объектов Active Directory](/windows/desktop/AD/creating-and-deleting-objects-in-active-directory-domain-services).
4.  Заполните [**структуру \_ \_ сведений о attr в ADS**](/windows/desktop/api/Iads/ns-iads-ads_attr_info) для каждого необязательного атрибута объекта.
5.  Чтобы создать объект в контейнере, используйте метод [**идиректорйобжект:: креатедсобжект**](/windows/desktop/api/Iads/nf-iads-idirectoryobject-createdsobject) . Этот метод также фиксирует объект в базовой службе каталогов. Если массив [**\_ \_ сведений о**](/windows/desktop/api/Iads/ns-iads-ads_attr_info) атрибутах ADS не содержит все необходимые атрибуты для объекта, **идиректорйобжект:: креатедсобжект** завершится ошибкой.

## <a name="deleting-an-object"></a>Удаление объекта

Чтобы удалить объект, используйте метод [**иадсконтаинер::D удалить**](/windows/desktop/api/Iads/nf-iads-iadscontainer-delete) или [**Идиректорйобжект::D елетедсобжект**](/windows/desktop/api/Iads/nf-iads-idirectoryobject-deletedsobject) . Эти методы завершатся ошибкой, если удаленный объект содержит любые дочерние объекты. Используйте метод [**иадсделетеопс::D елетеобжект**](/windows/desktop/api/Iads/nf-iads-iadsdeleteops-deleteobject) , чтобы удалить контейнер и все дочерние объекты контейнера.

Что происходит с удаленным объектом, зависит от базовой службы каталогов. Дополнительные сведения об удалении объектов Active Directory см. в разделе [Создание и удаление объектов Active Directory](/windows/desktop/AD/creating-and-deleting-objects-in-active-directory-domain-services).

 

 