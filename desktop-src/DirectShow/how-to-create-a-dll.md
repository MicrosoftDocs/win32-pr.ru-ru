---
description: Создание библиотеки DLL фильтра DirectShow
ms.assetid: 142bc8a2-240d-418f-9374-62d34a76ec38
title: Создание библиотеки DLL фильтра DirectShow
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ee964115e040d11ae10562b05899b2895f03d2fe
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "105650412"
---
# <a name="how-to-create-a-directshow-filter-dll"></a>Создание библиотеки DLL фильтра DirectShow

В этой статье описывается, как реализовать компонент в виде библиотеки динамической компоновки (DLL) в Microsoft DirectShow. Эта статья является продолжением [реализации IUnknown](how-to-implement-iunknown.md), который описывает, как реализовать интерфейс **IUnknown** путем наследования компонента от базового класса [**кункновн**](cunknown.md) .

Эта статья состоит из следующих разделов:

-   [Фабрики классов и шаблоны фабрики](class-factories-and-factory-templates.md)
-   [Массив шаблонов фабрики](factory-template-array.md)
-   [Функции DLL](dll-functions.md)

Для регистрации фильтра DirectShow (в отличие от универсального COM-объекта) требуются некоторые дополнительные действия, не описанные в этой статье. Сведения о регистрации фильтров см. [в статье регистрация фильтров DirectShow](how-to-register-directshow-filters.md).

## <a name="related-topics"></a>См. также

<dl> <dt>

[DirectShow и COM](directshow-and-com.md)
</dt> </dl>

 

 



