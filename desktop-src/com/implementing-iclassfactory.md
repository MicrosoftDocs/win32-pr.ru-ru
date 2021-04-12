---
title: Реализация IClassFactory
description: Реализация IClassFactory
ms.assetid: 96466756-c135-4ee5-a48c-f31129878473
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b057657508b3060506c15c68308ea6a5332e5099
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/21/2020
ms.locfileid: "104413789"
---
# <a name="implementing-iclassfactory"></a>Реализация IClassFactory

Когда клиент использует идентификатор CLSID для запроса создания экземпляра объекта, первым шагом является создание объекта класса, промежуточного объекта, который содержит реализацию методов интерфейса [**IClassFactory**](/windows/win32/api/unknwn/nn-unknwn-iclassfactory) . Хотя модель COM предоставляет несколько функций создания экземпляров, первый шаг в реализации этих функций — это создание объекта класса.

В результате все серверы должны реализовывать методы интерфейса [**IClassFactory**](/windows/win32/api/unknwn/nn-unknwn-iclassfactory) , который содержит два метода:

-   [**CreateInstance**](/windows/desktop/api/Unknwn/nf-unknwn-iclassfactory-createinstance). Этот метод должен создать неинициализированный экземпляр объекта и вернуть указатель на запрошенный интерфейс для объекта.
-   [**Локксервер**](/windows/win32/api/unknwn/nf-unknwn-iclassfactory-lockserver). Этот метод просто увеличивает счетчик ссылок на объект класса, чтобы убедиться, что сервер остается в памяти и не завершает работу до того, как клиент будет готов.

Чтобы сервер был ответственным за собственное лицензирование, COM определяет [**IClassFactory2**](/windows/desktop/api/OCIdl/nn-ocidl-iclassfactory2), который наследует определение от [**IClassFactory**](/windows/win32/api/unknwn/nn-unknwn-iclassfactory). Таким же, сервер, реализующий **IClassFactory2** , должен по определению реализовывать методы **IClassFactory**.

COM также предоставляет вспомогательные функции для реализации серверов вне процесса. Дополнительные сведения см. в разделе [вспомогательные методы реализации сервера](out-of-process-server-implementation-helpers.md).

## <a name="related-topics"></a>См. также

<dl> <dt>

[Обязанности сервера COM](com-server-responsibilities.md)
</dt> <dt>

[Лицензирование и IClassFactory2](licensing-and-iclassfactory2.md)
</dt> </dl>

 

 