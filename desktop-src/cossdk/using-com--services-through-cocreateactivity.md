---
description: Функция Кокреатеактивити используется для отправки пакетной работы в систему COM+. Это позволяет приложениям, основанным на сценариях, поддерживать конфигурацию службы COM+ на уровне приложения.
ms.assetid: af734507-516c-43f1-9c5e-c77cde1b8008
title: Использование служб COM+ через Кокреатеактивити
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f5b3296756b91d0f8ea29b1d67c11c78c431cfcd
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105701273"
---
# <a name="using-com-services-through-cocreateactivity"></a>Использование служб COM+ через Кокреатеактивити

Функция [**кокреатеактивити**](/windows/desktop/api/ComSvcs/nf-comsvcs-cocreateactivity) используется для отправки пакетной работы в систему com+. Это позволяет приложениям, основанным на сценариях, поддерживать конфигурацию службы COM+ на уровне приложения.

Требуемые службы COM+ настраиваются с помощью объекта [**ксервицеконфиг**](cserviceconfig.md) , который передается в функцию. Функция создает объект действия и возвращает интерфейс [**исервицеактивити**](/windows/desktop/api/ComSvcs/nn-comsvcs-iserviceactivity) этого объекта. Пакетная работа может быть отправлена либо синхронно, либо асинхронно с помощью методов [**синчронаускалл**](/windows/desktop/api/ComSvcs/nf-comsvcs-iserviceactivity-synchronouscall) или [**асинчронаускалл**](/windows/desktop/api/ComSvcs/nf-comsvcs-iserviceactivity-asynchronouscall) **исервицеактивити** соответственно. Указатель на интерфейс [**исервицекалл**](/windows/desktop/api/ComSvcs/nn-comsvcs-iservicecall) передается в каждый из этих методов, и пакетная работа реализуется разработчиком в методе [**OnCall**](/windows/desktop/api/ComSvcs/nf-comsvcs-iservicecall-oncall) интерфейса **исервицекалл** .

## <a name="component-services-administrative-tool"></a>Средство администрирования служб компонентов

Не применяется.

## <a name="visual-basic"></a>Visual Basic

Не применяется.

## <a name="cc"></a>C/C++

В следующем фрагменте кода показано, как использовать службы COM+ через [**кокреатеактивити**](/windows/desktop/api/ComSvcs/nf-comsvcs-cocreateactivity). Обработка ошибок опущена для краткости. Этот фрагмент кода использует объект [**ксервицеконфиг**](cserviceconfig.md) , который был создан и настроен в [настройке служб COM+ с помощью ксервицеконфиг](configuring-com--services-with-cserviceconfig.md).


```C++
// A CServiceConfig object was created as follows:
// hr = CoCreateInstance(CLSID_CServiceConfig, NULL, CLSCTX_INPROC_SERVER,
//   IID_IUnknown, (void**)&pUnknownCSC);

// Create the activity for our services.
HRESULT hr = CoCreateActivity(pUnknownCSC, IID_IServiceActivity, (void**)&pActivity);
if (FAILED(hr)) throw(hr);

// Do the batch work synchronously.
// The batch work is implemented in pServiceCall->OnCall().
hr = pActivity->SynchronousCall(pServiceCall);
if (FAILED(hr)) throw(hr);

```



## <a name="related-topics"></a>См. также

<dl> <dt>

[**кокреатеактивити**](/windows/desktop/api/ComSvcs/nf-comsvcs-cocreateactivity)
</dt> <dt>

[Настройка служб COM+ с помощью Ксервицеконфиг](configuring-com--services-with-cserviceconfig.md)
</dt> <dt>

[**ксервицеконфиг**](cserviceconfig.md)
</dt> <dt>

[Использование служб COM+ через Коентерсервицедомаин и Колеавесервицедомаин](using-com--services-through-coenterservicedomain-and-coleaveservicedomain.md)
</dt> </dl>

 

 



