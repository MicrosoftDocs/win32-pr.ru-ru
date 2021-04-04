---
title: Класс объекта и категория объекта
description: Каждый экземпляр класса объектов имеет многозначное свойство objectClass, определяющее класс, экземпляр которого является объектом, а также все структурные или абстрактные классы, от которых он является производным.
ms.assetid: b3c5f9ee-98e0-42dd-9b61-3731e14b9cd4
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c74941b4f32cc197d3dbbf3aa0dc3179b4098ee8
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/17/2020
ms.locfileid: "103987317"
---
# <a name="object-class-and-object-category"></a>Класс объекта и категория объекта

Каждый экземпляр класса объектов имеет многозначное свойство [**objectClass**](/windows/desktop/ADSchema/a-objectclass) , определяющее класс, экземпляр которого является объектом, а также все структурные или абстрактные классы, от которых он является производным. Таким образом, свойство **objectClass** объекта пользователя определяет классы [**Top**](/windows/desktop/ADSchema/c-top), [**Person**](/windows/desktop/ADSchema/c-person), [**организатионалперсон**](/windows/desktop/ADSchema/c-organizationalperson)и [**User**](/windows/desktop/ADSchema/c-user) . Свойство **objectClass** не включает вспомогательные классы в списке. Система устанавливает значение **objectClass** при создании экземпляра объекта и не может быть изменено.

Каждый экземпляр класса объектов также имеет свойство [**objectCategory**](/windows/desktop/ADSchema/a-objectcategory) , которое является однозначным свойством, которое содержит различающееся имя либо класса, экземпляр которого является объектом, либо одного из его классов. При создании объекта система устанавливает свойство **objectCategory** в значение, заданное свойством [**дефаултобжекткатегори**](/windows/desktop/ADSchema/a-defaultobjectcategory) своего класса объекта. Свойство **objectCategory** объекта не может быть изменено.

Дополнительные сведения и пример кода, который извлекает свойство [**objectClass**](/windows/desktop/ADSchema/a-objectclass) объекта, см. в разделе [Получение атрибута objectClass](retrieving-the-objectclass-property.md).

> [!IMPORTANT]
> До Windows Server 2008 атрибут [**objectClass**](/windows/desktop/ADSchema/a-objectclass) не индексируется. Это связано с тем, что оно имеет несколько значений и строго не является уникальным; то есть каждый экземпляр атрибута **objectClass** включает в себя класс [**Top**](/windows/desktop/ADSchema/c-top) . Это означает, что индекс будет очень большим и неэффективным. Для нахождение объектов заданного класса используйте атрибут [**objectCategory**](/windows/desktop/ADSchema/a-objectcategory) , который является однозначным и индексированным. Дополнительные сведения об использовании этих свойств в фильтрах поиска см. в разделе [Выбор искомых](deciding-what-to-find.md)данных.

 

Для большинства классов [**дефаултобжекткатегори**](/windows/desktop/ADSchema/a-defaultobjectcategory) представляет собой различающееся имя объекта [**classSchema**](/windows/desktop/ADSchema/c-classschema) класса. Например, **дефаултобжекткатегори** для класса [**OrganizationalUnit**](/windows/desktop/ADSchema/c-organizationalunit) : CN = организация-единица, CN = Схема, CN = Configuration, <DC = forestroot>». Однако некоторые классы ссылаются на другой класс в качестве их **дефаултобжекткатегори**. Это позволяет запросу легко находить группы связанных объектов, даже если они отличаются от классов. Например, классы [**пользователь**](/windows/desktop/ADSchema/c-user), [**Person**](/windows/desktop/ADSchema/c-person), [**организатионалперсон**](/windows/desktop/ADSchema/c-organizationalperson)и [**Contact**](/windows/desktop/ADSchema/c-contact) все указывают класс **Person** в своих свойствах **дефаултобжекткатегори** . Это позволяет фильтрам поиска, например (objectCategory = Person), находить экземпляры всех этих классов с помощью одного запроса. Запросы для людей очень распространены, поэтому это простая оптимизация.

При создании подкласса из структурного класса рекомендуется установить значение [**дефаултобжекткатегори**](/windows/desktop/ADSchema/a-defaultobjectcategory) нового класса, совпадающее с тем же различающимся именем суперкласса. Это позволяет стандартному пользовательскому интерфейсу найти подкласс.

 

 