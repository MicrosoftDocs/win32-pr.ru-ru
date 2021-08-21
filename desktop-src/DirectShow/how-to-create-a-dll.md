---
description: создание библиотеки DLL для фильтра DirectShow
ms.assetid: 142bc8a2-240d-418f-9374-62d34a76ec38
title: создание библиотеки DLL для фильтра DirectShow
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 443f8aff88cf73198ed7c417da77f6febf33e18806efba5431e18117ddd2c32e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120079014"
---
# <a name="how-to-create-a-directshow-filter-dll"></a>создание библиотеки DLL для фильтра DirectShow

В этой статье описывается, как реализовать компонент в виде библиотеки динамической компоновки (DLL) в Microsoft DirectShow. Эта статья является продолжением [реализации IUnknown](how-to-implement-iunknown.md), который описывает, как реализовать интерфейс **IUnknown** путем наследования компонента от базового класса [**кункновн**](cunknown.md) .

Эта статья состоит из следующих разделов:

-   [Фабрики классов и шаблоны фабрики](class-factories-and-factory-templates.md)
-   [Массив шаблонов фабрики](factory-template-array.md)
-   [Функции DLL](dll-functions.md)

чтобы зарегистрировать фильтр DirectShow (в отличие от универсального COM-объекта), необходимо выполнить некоторые дополнительные действия, не описанные в этой статье. сведения о регистрации фильтров см. [в статье регистрация DirectShow фильтров](how-to-register-directshow-filters.md).

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[DirectShow и COM](directshow-and-com.md)
</dt> </dl>

 

 



