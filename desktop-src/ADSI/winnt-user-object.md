---
title: Объект пользователя WinNT
description: объект пользователя WinNT представляет учетную запись пользователя в домене Windows NT 4,0.
ms.assetid: c57016e2-538b-4f37-a1bb-699fcf3c080d
ms.tgt_platform: multiple
keywords:
- Интерфейс ADSI для пользовательских объектов
- Службы WinNT Provider ADSI, объект User
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 50a89c2c4daf0d02e1cb9a150e35702ab4f8775f6bcc993db2b0348768bb1603
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119023002"
---
# <a name="winnt-user-object"></a>Объект пользователя WinNT

объект пользователя WinNT представляет учетную запись пользователя в домене Windows NT 4,0. Объект содержит специальные функции. В одном экземпляре он не поддерживает все методы свойств интерфейса [**IADsUser**](/windows/desktop/api/Iads/nn-iads-iadsuser) . Во втором экземпляре он поддерживает некоторые пользовательские свойства, доступ к которым можно получить только с помощью метода [**iAds. Get**](/windows/desktop/api/Iads/nf-iads-iads-get) или [**iAds. постановки**](/windows/desktop/api/Iads/nf-iads-iads-put) .

Дополнительные сведения об объектах пользователя WinNT см. в следующих статьях:

-   [Неподдерживаемые свойства IADsUser](unsupported-iadsuser-properties.md)
-   [Настраиваемые свойства пользователя WinNT](winnt-custom-user-properties.md)
-   [Примеры управления учетными записями пользователей WinNT](winnt-user-account-management-examples.md)

 

 




