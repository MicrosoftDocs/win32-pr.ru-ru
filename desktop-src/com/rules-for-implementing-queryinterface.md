---
title: Правила реализации QueryInterface
description: Правила реализации QueryInterface
ms.assetid: 6db17ed8-06e4-4bae-bc26-113176cc7e0e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9c0d0df2d0382c670ed6f4a323f55dcdd1b187430282abe6699da186e574e390
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119047872"
---
# <a name="rules-for-implementing-queryinterface"></a>Правила реализации QueryInterface

Существует три основных правила, которые управляют реализацией метода [**IUnknown:: QueryInterface**](/windows/desktop/api/Unknwn/nf-unknwn-iunknown-queryinterface(q)) для COM-объекта:

-   Объекты должны иметь удостоверение.
-   Набор интерфейсов в экземпляре объекта должен быть статическим.
-   Для любого интерфейса объекта из любого другого интерфейса должно быть возможно успешное выполнение запроса.

## <a name="objects-must-have-identity"></a>Объекты должны иметь удостоверение

Для любого заданного экземпляра объекта вызов [**QueryInterface**](/windows/desktop/api/Unknwn/nf-unknwn-iunknown-queryinterface(q)) с \_ интерфейсом IID IUnknown должен всегда возвращать одно и то же значение физического указателя. Это позволяет вызывать **QueryInterface** на любом из двух интерфейсов и сравнивать результаты, чтобы определить, указывают ли они на один и тот же экземпляр объекта.

## <a name="the-set-of-interfaces-on-an-object-instance-must-be-static"></a>Набор интерфейсов в экземпляре объекта должен быть статическим

Набор интерфейсов, доступных для объекта через [**QueryInterface**](/windows/desktop/api/Unknwn/nf-unknwn-iunknown-queryinterface(q)) , должен быть статическим, а не динамическим. В частности, если **QueryInterface** возвращает \_ "ОК" для заданного IID, он никогда не должен возвращать e \_ Interface при последующих вызовах для того же объекта; и если **QueryInterface** ВОЗВРАЩАЕТ e \_ -интерфейс для заданного IID, последующие вызовы для одного и того же идентификатора IID на одном и том же объекте не должны возвращать значение S \_ ОК.

## <a name="it-must-be-possible-to-query-successfully-for-any-interface-on-an-object-from-any-other-interface"></a>Для любого интерфейса объекта из любого другого интерфейса необходимо иметь возможность успешного выполнения запроса.

Это происходит при наличии следующего кода:

``` syntax
IA * pA = (some function returning an IA *); 
IB * pB = NULL; 
HRESULT   hr; 
hr = pA->QueryInterface(IID_IB, &pB); 
 
```

применяются следующие правила.

-   Если у вас есть указатель на интерфейс в объекте, необходимо успешно вызвать метод [**QueryInterface**](/windows/desktop/api/Unknwn/nf-unknwn-iunknown-queryinterface(q)) для этого же интерфейса следующим образом:

    ``` syntax
    pA->QueryInterface(IID_IA, ...) 
     
    ```

-   Если вызов [**QueryInterface**](/windows/desktop/api/Unknwn/nf-unknwn-iunknown-queryinterface(q)) для второго указателя интерфейса завершился с ошибкой, вызов **QueryInterface** из этого указателя для первого интерфейса также должен быть выполнен. Если удалось получить pB, также необходимо выполнить следующее:

    ``` syntax
    pB->QueryInterface(IID_IA, ...) 
     
    ```

-   Любой интерфейс должен иметь возможность запрашивать любой другой интерфейс для объекта. Если запрос pB был успешно получен, и вы успешно запрашиваете третий интерфейс (IC) с помощью этого указателя, необходимо также иметь возможность успешного запроса для IC с помощью первого указателя, pA. В этом случае должна быть выполнена следующая последовательность:

    ``` syntax
    IC * pC = NULL; 
    hr = pB->QueryInterface(IID_IC, &pC); 
    pA->QueryInterface(IID_IC, ...) 
     
    ```

Реализации интерфейса должны поддерживать Счетчик необработанных ссылок на указатели на все интерфейсы данного объекта. Для счетчика следует использовать **целое число без знака** .

Если клиенту необходимо выяснить, что ресурсы были освобождены, то перед вызовом [**IUnknown:: Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release)необходимо использовать метод в интерфейсе объекта с семантикой более высокого уровня.

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Использование и реализация IUnknown](using-and-implementing-iunknown.md)
</dt> </dl>

 

 