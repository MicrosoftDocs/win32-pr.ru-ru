---
title: Объекты ADSI, реализованные на уровне маршрутизатора
description: В следующей таблице представлено краткое описание COM-объектов, реализованных в маршрутизаторе ADSI.
ms.assetid: bd446e05-a15d-4354-9204-1df4e360497c
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 99cc96eac8a2d680cb83622e01d94f8ef7a1d236726ab6b6fef9b2e6c5c40f50
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118692821"
---
# <a name="adsi-objects-implemented-in-the-router-layer"></a>Объекты ADSI, реализованные на уровне маршрутизатора

В следующей таблице представлено краткое описание COM-объектов, реализованных в маршрутизаторе ADSI.



| Объект ADSI            | Описание                                                         | Поддерживаемые интерфейсы                                                                                                                                                                                                                                                                      |
|------------------------|---------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **акцессконтролентри** | Объект ADSI, представляющий запись управления доступом (ACE).       | [**IADsAccessControlEntry**](/windows/desktop/api/Iads/nn-iads-iadsaccesscontrolentry)                                                                                                                                                                                                                                  |
| **AccessControlList**  | Объект ADSI, представляющий список управления доступом (ACL).        | [**IADsAccessControlList**](/windows/desktop/api/Iads/nn-iads-iadsaccesscontrollist)                                                                                                                                                                                                                                    |
| **адснамеспацес**      | Объект ADSI, представляющий контейнер различных пространств имен. | <dl> <dt>[**IAds**](/windows/desktop/api/Iads/nn-iads-iads)</dt> <dt>[**иадсконтаинер**](/windows/desktop/api/Iads/nn-iads-iadscontainer)</dt> <dt>[**иадснамеспацес**](/windows/desktop/api/Iads/nn-iads-iadsnamespaces)</dt> </dl> |
| **ларжеинтежер**       | Объект ADSI, представляющий большое целое число.                     | [**IADsLargeInteger**](/windows/desktop/api/Iads/nn-iads-iadslargeinteger)                                                                                                                                                                                                                                              |
| **PropertyEntry**      | Объект ADSI, представляющий запись свойства.                    | [**иадспропертентри**](/windows/desktop/api/Iads/nn-iads-iadspropertyentry)                                                                                                                                                                                                                                            |
| **PropertyValue**      | Объект ADSI, представляющий значение свойства.                    | [**иадспропертивалуе**](/windows/desktop/api/Iads/nn-iads-iadspropertyvalue)                                                                                                                                                                                                                                            |
| **PropertyValue2**     | Объект ADSI, представляющий значение свойства.                    | [**IADsPropertyValue2**](/windows/desktop/api/Iads/nn-iads-iadspropertyvalue2)                                                                                                                                                                                                                                          |
| **SecurityDescriptor** | Объект ADSI, представляющий дескриптор безопасности.               | [**IADsSecurityDescriptor**](/windows/desktop/api/Iads/nn-iads-iadssecuritydescriptor)                                                                                                                                                                                                                                  |



 

 

 




