---
description: Системы на базе Windows могут иметь несколько экземпляров типа объекта Трустеддомаин.
ms.assetid: 13efedb5-ebb6-459b-8c4f-06774226278c
title: Тип объекта Трустеддомаин
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 70f0a4e6eca0790d877a9a23e4d83725d4e80798
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103809293"
---
# <a name="the-trusteddomain-object-type"></a>Тип объекта Трустеддомаин

Системы на базе Windows могут иметь несколько экземпляров типа объекта [**трустеддомаин**](trusteddomain-object.md) . Объекты **трустеддомаин** имеют два поля, которые должны быть уникальными для всех объектов **трустеддомаин** :

-   Имя [ **трустеддомаин**](trusteddomain-object.md)
-   [*Идентификатор безопасности*](/windows/desktop/SecGloss/s-gly) (SID) [**трустеддомаин**](trusteddomain-object.md).

Попытка создать новый объект **трустеддомаин** с именем или идентификатором безопасности, который уже используется другим объектом **трустеддомаин** , будет отклонен.

 

 
