---
description: Интерфейс Иупдатеколлектион определяет следующие свойства.
ms.assetid: 38420d5e-4d36-4ed7-be06-e1df903929a7
title: Свойства Иупдатеколлектион
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 599e7ba6efd20810ad61a8f59f5cfec67ce82b9e95f42df5250360238c43d044
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119859764"
---
# <a name="iupdatecollection-properties"></a>Свойства Иупдатеколлектион

Интерфейс [**иупдатеколлектион**](/windows/desktop/api/Wuapi/nn-wuapi-iupdatecollection) определяет следующие свойства.



| Свойство                                        | Описание                                                                                                              |
|-------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------|
| [**\_NewEnum**](/windows/desktop/api/Wuapi/nf-wuapi-iupdatecollection-get__newenum) | Возвращает интерфейс [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) , который можно использовать для перечисления коллекции. |
| [**Count**](/windows/desktop/api/Wuapi/nf-wuapi-iupdatecollection-get_count)        | Получает количество элементов коллекции.                                                                           |
| [**Компонент**](/windows/desktop/api/Wuapi/nf-wuapi-iupdatecollection-get_item)          | Возвращает или задает интерфейс [**иупдате**](/windows/desktop/api/Wuapi/nn-wuapi-iupdate) в коллекции.                                                    |
| [**Доступно**](/windows/desktop/api/Wuapi/nf-wuapi-iupdatecollection-get_readonly)  | Возвращает логическое значение, указывающее, доступна ли коллекция обновлений только для чтения.                                          |



 

 

 
