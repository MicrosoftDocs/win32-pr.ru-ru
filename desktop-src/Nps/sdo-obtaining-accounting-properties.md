---
title: Получение свойств учета
description: Объект Account является одним из объектов в коллекции обработчиков запросов.
ms.assetid: eb5c8606-d3f0-4c33-9035-7b7b1369cb0d
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 77390a6aa67e946de6d69dd3d1bc28a76907b7ad31b497d4921c7a2d7493c328
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118361732"
---
# <a name="obtaining-accounting-properties"></a>Получение свойств учета

> [!Note]  
> служба проверки подлинности в интернете (IAS) переименовала сервер политики сети (NPS), начиная с Windows Server 2008. Содержимое этого раздела относится как к IAS, так и к NPS. По всему тексту NPS используется для ссылки на все версии службы, включая версии, изначально называемые IAS.

 

Объект Account является одним из объектов в коллекции обработчиков запросов. Значением перечисления для коллекции обработчиков запросов является **свойство \_ службы IAS \_ рекуессандлерс \_ Collection**. Имя обработчика для объекта учета — Microsoft Accounting.

следующий Visual Basic код обращается к свойствам, доступным в обработчике объектов учета.


```VB
Set sdoRequestHandler = sdoCollRequestHandlers.Item("Microsoft Accounting")
vtTemp = sdoRequestHandler.GetProperty(PROPERTY_ACCOUNTING_LOG_ACCOUNTING)
vtTemp = sdoRequestHandler.GetProperty(PROPERTY_ACCOUNTING_LOG_ACCOUNTING_INTERIM)
vtTemp = sdoRequestHandler.GetProperty(PROPERTY_ACCOUNTING_LOG_AUTHENTICATION)
vtTemp = sdoRequestHandler.GetProperty(PROPERTY_ACCOUNTING_LOG_FILE_DIRECTORY)
vtTemp = sdoRequestHandler.GetProperty(PROPERTY_ACCOUNTING_LOG_IAS1_FORMAT)
vtTemp = sdoRequestHandler.GetProperty(PROPERTY_ACCOUNTING_LOG_OPEN_NEW_FREQUENCY)
vtTemp = sdoRequestHandler.GetProperty(PROPERTY_ACCOUNTING_LOG_OPEN_NEW_SIZE)
```



Чтобы получить доступ к свойствам учета с помощью C++, сначала получите коллекцию обработчиков запросов. [Извлечение коллекции](/windows/desktop/Nps/sdo-retrieving-a-collection) содержит код C++, демонстрирующий получение коллекции. Значением перечисления для коллекции обработчиков запросов является **свойство \_ службы IAS \_ рекуессандлерс \_ Collection**. (Значения, соответствующие различным коллекциям NPS, перечисляются типом перечисления [**иаспропертиес**](/windows/desktop/api/sdoias/ne-sdoias-iasproperties) .)

Коллекция обработчиков запросов содержит объект с именем «Microsoft account». Извлеките этот объект из коллекции. Раздел, в котором [извлекается объект из коллекции](/windows/desktop/Nps/sdo-retrieving-an-object-from-a-collection) , содержит код C++, демонстрирующий получение объекта из коллекции.

Получив объект Microsoft account, получите интерфейс [**исдо**](/windows/desktop/api/sdoias/nn-sdoias-isdo) для объекта с помощью [**IUnknown:: QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)). В разделе [Получение ПОЛЬЗОВАТЕЛЬСКОГО SDO](/windows/desktop/Nps/sdo-retrieving-a-user-sdo) содержится код C++, демонстрирующий получение интерфейса **исдо** для объекта. Затем можно использовать метод [**исдо::**](/windows/desktop/api/sdoias/nf-sdoias-isdo-getproperty) GetObject для получения значений свойств для объекта Microsoft account.

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Получение коллекции](/windows/desktop/Nps/sdo-retrieving-a-collection)
</dt> <dt>

[Получение объекта из коллекции](/windows/desktop/Nps/sdo-retrieving-an-object-from-a-collection)
</dt> <dt>

[Получение SDO пользователя](/windows/desktop/Nps/sdo-retrieving-a-user-sdo)
</dt> <dt>

[**исдо**](/windows/desktop/api/sdoias/nn-sdoias-isdo)
</dt> <dt>

[**IUnknown:: QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q))
</dt> <dt>

[**иаспропертиес**](/windows/desktop/api/sdoias/ne-sdoias-iasproperties)
</dt> </dl>

 

 