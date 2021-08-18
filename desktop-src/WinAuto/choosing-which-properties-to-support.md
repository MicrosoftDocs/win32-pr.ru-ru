---
title: Выбор свойств для поддержки
description: Свойства IAccessible предоставляют разработчикам сервера возможность описывать разнообразные элементы пользовательского интерфейса.
ms.assetid: c51fd8a1-dc23-4d64-8921-e0a795c3ffb8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 76a3c9ef5d56c6d963a05ac84b5e2cacafde488c377ebcc73fa1e2c4be1adab2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119133967"
---
# <a name="choosing-which-properties-to-support"></a>Выбор свойств для поддержки

Свойства [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) предоставляют разработчикам сервера возможность описывать разнообразные элементы пользовательского интерфейса. Но не все свойства применимы для каждого вида элементов пользовательского интерфейса. Кроме того, некоторые свойства предоставляют описательные сведения, которые полезны, но не являются обязательными.

Серверы должны поддерживать следующие свойства и методы для каждого объекта:

-   [**Имя**](name-property.md)
-   [**Role**](role-property.md)
-   [**Состояние**](state-property.md)
-   [**Location**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acclocation) и [ **IAccessible:: акчиттест**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest)
-   [**Parent**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent) и [ **IAccessible:: аккнавигате**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate)

Следующие свойства и метод должны поддерживаться, если они применимы к объекту:

-   [**KeyboardShortcut**](keyboardshortcut-property.md)
-   [**Значение**](value-property.md)

Если у объекта есть дочерние элементы, необходимо поддерживать следующие свойства и метод.

-   [**Дочерний элемент**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchild) и [ **ChildCount**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchildcount)
-   [**Фокус, выбор**](selection-and-focus-properties-and-methods.md)и [ **IAccessible:: аккселект**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect)

Следующие свойства являются необязательными, но предоставляют полезные описательные сведения об объекте. Свойство [**Description**](description-property.md) реализуется для описания точечных рисунков и других изображений.

-   [**Описание**](description-property.md)
-   [**DefaultAction**](defaultaction-property.md) и [ **IAccessible:: аккдодефаултактион**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accdodefaultaction)
-   [**Справка**](help-property.md)
-   [**хелптопик**](helptopic-property.md)

 

 




