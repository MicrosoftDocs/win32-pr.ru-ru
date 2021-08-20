---
title: Регистрация серверов COM
description: Регистрация серверов COM
ms.assetid: aaa09a1b-deb8-424f-a911-ae22d39919d3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b0a26db770585afddb07630aecb60e1ae3f86d8ddb6ff112e36993454e9f4f82
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118104835"
---
# <a name="registering-com-servers"></a>Регистрация серверов COM

Определив класс в коде (убедившись, что он реализует [**IClassFactory**](/windows/win32/api/unknwn/nn-unknwn-iclassfactory) или [**IClassFactory2**](/windows/desktop/api/OCIdl/nn-ocidl-iclassfactory2)) и назначил ему идентификатор CLSID, необходимо разместить в реестре сведения, позволяющие com, по запросу клиента с идентификатором CLSID, создать экземпляры своих объектов. Эти сведения сообщают системе, для определенного идентификатора CLSID, где находится код DLL или EXE для этого класса и как он запускается.

Существует более одного способа регистрации класса в реестре. Кроме того, существует и другие способы «регистрации» класса с системой при его выполнении, чтобы система знала, что выполняющийся объект в данный момент находится в системе.

Дополнительные сведения о регистрации см. в следующих разделах:

-   [Регистрация класса при установке](registering-a-class-at-installation.md)
-   [Регистрация работающего сервера EXE](registering-a-running-exe-server.md)
-   [Регистрация объектов в таблице ROT](registering-objects-in-the-rot.md)
-   [Самостоятельная регистрация](self-registration.md)
-   [Установка в качестве приложения службы](installing-as-a-service-application.md)

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Обязанности сервера COM](com-server-responsibilities.md)
</dt> </dl>

 

 