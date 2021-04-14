---
title: Обязанности сервера COM
description: Обязанности сервера COM
ms.assetid: 9853bbf5-b989-45b7-8fa8-8cd2f0d48d3c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 86b9d3104af80a7b2dca49dbbd5b55e66a613ee7
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/21/2020
ms.locfileid: "104413829"
---
# <a name="com-server-responsibilities"></a>Обязанности сервера COM

Одним из наиболее важных способов получения указателя на объект является получение клиентом запроса о запуске сервера и его создании и активации экземпляра объекта, предоставленного сервером. Чтобы убедиться, что это происходит правильно, отвечает сервер. Существует несколько важных частей.

Сервер должен реализовать код для объекта класса с помощью реализации интерфейса [**IClassFactory**](/windows/win32/api/unknwn/nn-unknwn-iclassfactory) или [**IClassFactory2**](/windows/desktop/api/OCIdl/nn-ocidl-iclassfactory2) .

Сервер должен зарегистрировать свой идентификатор CLSID в системном реестре на компьютере, на котором он находится, и, в свою сторону, иметь возможность публикации расположения компьютера в других системах в сети, чтобы позволить клиентам вызывать его, не требуя от клиента получения сведений о расположении сервера.

Сервер в основном отвечает за безопасность; то есть, в большинстве случаев сервер определяет, будет ли он предоставлять указатель на один из его объектов клиенту.

Серверы внутри процесса должны реализовывать и экспортировать определенные функции, позволяющие клиентскому процессу создавать их экземпляры.

В следующих разделах описаны обязанности сервера COM.

-   [Реализация IClassFactory](implementing-iclassfactory.md)
-   [Лицензирование и IClassFactory2](licensing-and-iclassfactory2.md)
-   [Регистрация серверов COM](registering-com-servers.md)
-   [Вспомогательные методы реализации сервера](out-of-process-server-implementation-helpers.md)
-   [Создание и оптимизация GUID](guid-creation-and-optimizations.md)

## <a name="related-topics"></a>См. также

<dl> <dt>

[COM-клиенты и серверы](com-clients-and-servers.md)
</dt> </dl>

 

 