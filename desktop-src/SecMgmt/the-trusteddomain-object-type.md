---
description: системы на основе Windows могут иметь несколько экземпляров типа объекта трустеддомаин.
ms.assetid: 13efedb5-ebb6-459b-8c4f-06774226278c
title: Тип объекта Трустеддомаин
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bdab860f9192e48433242251578a20a45bf294164c0bffff8b6f00562a1442e9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119004842"
---
# <a name="the-trusteddomain-object-type"></a>Тип объекта Трустеддомаин

системы на основе Windows могут иметь несколько экземпляров типа объекта [**трустеддомаин**](trusteddomain-object.md) . Объекты **трустеддомаин** имеют два поля, которые должны быть уникальными для всех объектов **трустеддомаин** :

-   Имя [ **трустеддомаин**](trusteddomain-object.md)
-   [*Идентификатор безопасности*](/windows/desktop/SecGloss/s-gly) (SID) [**трустеддомаин**](trusteddomain-object.md).

Попытка создать новый объект **трустеддомаин** с именем или идентификатором безопасности, который уже используется другим объектом **трустеддомаин** , будет отклонен.

 

 
