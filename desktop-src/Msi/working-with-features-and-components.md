---
description: Существует несколько функций, изменяющих установку компонентов продукта и компонентов. Ниже описано, как изменить компоненты и компоненты.
ms.assetid: 840656f9-ea85-49e7-8842-f779228c30d6
title: Работа с функциями и компонентами
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d579b82dfb312c1588b500d8959fad8a09e44753
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105673929"
---
# <a name="working-with-features-and-components"></a>Работа с функциями и компонентами

Существует несколько функций, изменяющих установку компонентов продукта [и](components-and-features.md)компонентов. Ниже описано, как изменить компоненты и компоненты.

**Изменение установки компонентов и компонентов**

1.  Задайте уровень установки компонента или компонента, вызвав функцию [**мсисетинсталллевел**](/windows/desktop/api/Msiquery/nf-msiquery-msisetinstalllevel) .

    Каждому компоненту пакета назначается уровень установки в [таблице Feature](feature-table.md). Если уровень установки компонента ниже уровня, установленного параметром [**мсисетинсталллевел**](/windows/desktop/api/Msiquery/nf-msiquery-msisetinstalllevel), этот компонент выбирается для установки. После вызова **мсисетинсталллевел** можно явно изменить, установлен ли компонент.

2.  Определите, какие состояния доступны для указанного компонента, вызвав функцию [**мсижетфеатуревалидстатес**](/windows/desktop/api/Msiquery/nf-msiquery-msigetfeaturevalidstatesa) .
3.  Получите требования к месту на диске для указанного компонента и его дочерних компонентов, вызвав функцию [**мсижетфеатурекост**](/windows/desktop/api/Msiquery/nf-msiquery-msigetfeaturecosta) .
4.  Получите текущее состояние компонента или компонента, вызвав функцию [**мсижетфеатурестате**](/windows/desktop/api/Msiquery/nf-msiquery-msigetfeaturestatea) или функцию [**мсижеткомпонентстате**](/windows/desktop/api/Msiquery/nf-msiquery-msigetcomponentstatea) .
5.  Измените состояние компонента или компонента с помощью функции [**мсисетфеатурестате**](/windows/desktop/api/Msiquery/nf-msiquery-msisetfeaturestatea) или функции [**мсисеткомпонентстате**](/windows/desktop/api/Msiquery/nf-msiquery-msisetcomponentstatea) .

 

 



