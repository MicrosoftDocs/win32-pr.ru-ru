---
title: Создание внешней ссылки
description: Если создается внешний объект crossRef, а контроллер домена использует его для создания ссылки, то объект crossRef предоставляет два важных элемента данных в следующих свойствах.
ms.assetid: 9805390c-9e8d-4afd-bffc-43abf6055413
ms.tgt_platform: multiple
keywords:
- Внешние ссылки Active Directory
- Active Directory примеры Active Directory, создание внешней ссылки
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 801a9306c374a0c22d206e9a0f9dbb8cd240da0c
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/17/2020
ms.locfileid: "103789594"
---
# <a name="creating-an-external-referral"></a>Создание внешней ссылки

Если создается внешний объект [**crossRef**](/windows/desktop/ADSchema/c-crossref) , а контроллер домена использует его для создания ссылки, то объект **crossRef** предоставляет два важных элемента данных в следующих свойствах. Дополнительные сведения о ситуациях, в которых это может произойти, см. в предыдущем разделе.



| Свойство                           | Описание                                                                                                                                                         |
|------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**днсрут**](/windows/desktop/ADSchema/a-dnsroot) | Указывает сервер или домен, который может обрабатывать данные из контекста именования, указанного в [**NCName**](/windows/desktop/ADSchema/a-ncname).                                           |
| [**Параметрами**](/windows/desktop/ADSchema/a-ncname)   | Задает различающееся имя для домена, схемы или контейнера конфигурации, которые находятся в корне на сервере или в домене, указанном параметром [**днсрут**](/windows/desktop/ADSchema/a-dnsroot). |



 

Например, если сервер с DNS-адресом serv1.northwest.Fabrikam.com выполняет контекст именования с корнем CN = MyContainer, OU = МИДом, O = Fabrikam, задайте для [**днсрут**](/windows/desktop/ADSchema/a-dnsroot) в качестве DNS-адреса этого сервера и [**NCName**](/windows/desktop/ADSchema/a-ncname) различающееся имя домена, схемы или контейнера конфигурации.

Дополнительные сведения и пример кода, демонстрирующий создание внешней ссылки, см. в разделе [пример кода для создания внешнего объекта crossRef](example-code-for-creating-an-external-crossref-object.md).

 

 