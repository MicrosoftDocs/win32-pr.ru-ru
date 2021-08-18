---
description: Существует несколько функций, изменяющих установку компонентов продукта и компонентов. Ниже описано, как изменить компоненты и компоненты.
ms.assetid: 840656f9-ea85-49e7-8842-f779228c30d6
title: Работа с функциями и компонентами
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 18b77fd93a9f2ee8181020f6c436d7e61e09a0f6d7858f0159fb70a7c7d8eeef
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119145177"
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

 

 



