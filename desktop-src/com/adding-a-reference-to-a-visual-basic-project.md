---
title: добавление ссылки на Visual Basic Project
description: добавление ссылки на Visual Basic Project
ms.assetid: 635b1fe9-e592-42d7-a0ee-34fea205f412
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: deba6030e57839e0f436239790aaa6f02e2fb29981ce021b0de2d09af2acdff6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120097074"
---
# <a name="adding-a-reference-to-a-visual-basic-project"></a>добавление ссылки на Visual Basic Project

в следующей процедуре описывается добавление ссылки на COM-объект в проект Visual Basic. Приложение может использовать классы этого объекта.

При добавлении объекта в качестве ссылки можно использовать только библиотеку типов, предоставленную элементом управления, или библиотеку типов "RAW". в отличие от этого, добавление элемента управления в качестве компонента также предоставляет Visual Basic свойства и методы расширения, как если бы они были частью элемента управления.

**создание Visual Basic ссылки на компонент**

1.  В меню **Проект** выберите пункт **Ссылки**.
2.  Установите флажок рядом с компонентом, который нужно добавить. Если компонент отсутствует в списке, найдите .dll или OCX-файл с помощью **кнопки Обзор**.
3.  Нажмите **OK**.

Компонент теперь является частью проекта. Приложение может создавать экземпляры классов с помощью ключевого слова **New** .

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[добавление компонента в Visual Basic Project](adding-a-component-to-a-visual-basic-project.md)
</dt> <dt>

[Перевод в Visual Basic](translating-to-visual-basic.md)
</dt> </dl>

 

 




