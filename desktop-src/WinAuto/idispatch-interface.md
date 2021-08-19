---
title: Интерфейс IDispatch и специальные возможности
description: Изначально интерфейс IDispatch разрабатывался для поддержки автоматизации.
ms.assetid: 5a95f002-4fd5-43d3-9b50-7b3f7790300a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 710fb0bc8142dfa863967114d3841506c220b3c058db042b867607ffe56cd5e8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119052712"
---
# <a name="idispatch-interface-and-accessibility"></a>Интерфейс IDispatch и специальные возможности

Изначально интерфейс [**IDispatch**](/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch) разрабатывался для поддержки автоматизации. Он предоставляет механизм поздней привязки для доступа и получения сведений о методах и свойствах объекта. Ранее разработчикам серверов пришлось реализовать как интерфейсы **IDispatch** , так и методы [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) для доступных объектов. то есть они должны были предоставить [сдвоенный интерфейс](dual-interfaces--iaccessible-and-idispatch.md). С помощью Microsoft Active Accessibility 2,0 серверы могут возвращать **E \_ нотимпл** из методов **IDispatch** , а Microsoft Active Accessibility будет реализовывать для них интерфейс **IAccessible** .

В дополнение к методам, унаследованным от [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown), разработчики серверов должны реализовать следующие методы в определении класса каждого предоставленного объекта:

-   [**Жеттипеинфокаунт**](/previous-versions/windows/desktop/api/oaidl/nf-oaidl-idispatch-gettypeinfocount) возвращает число описаний типов для объекта. Для объектов, поддерживающих [**IDispatch**](/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch), количество сведений о типе всегда равно единице.
-   [**GetTypeInfo**](/previous-versions/windows/desktop/api/oaidl/nf-oaidl-idispatch-gettypeinfo) Извлекает описание программируемого интерфейса объекта.
-   [**GetIDsOfNames**](/previous-versions/windows/desktop/api/oaidl/nf-oaidl-idispatch-getidsofnames) сопоставляет имя метода или свойства с **идентификатором DISPID**, который позже используется для вызова метода или свойства.
-   [**Invoke**](/previous-versions/windows/desktop/api/oaidl/nf-oaidl-idispatch-invoke) вызывает один из методов объекта или получает или задает одно из его свойств.

 

 