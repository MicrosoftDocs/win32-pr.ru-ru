---
description: Использование служб COM+ через Коентерсервицедомаин и Колеавесервицедомаин
ms.assetid: 763fb01e-5daf-4e9b-8ef1-9ae79c0a84cc
title: Использование служб COM+ через Коентерсервицедомаин и Колеавесервицедомаин
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 36d87931628e177374dd07b40e9917a56c168a81
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104141977"
---
# <a name="using-com-services-through-coenterservicedomain-and-coleaveservicedomain"></a>Использование служб COM+ через Коентерсервицедомаин и Колеавесервицедомаин

[**Коентерсервицедомаин**](/windows/desktop/api/ComSvcs/nf-comsvcs-coenterservicedomain) и [**колеавесервицедомаин**](/windows/desktop/api/ComSvcs/nf-comsvcs-coleaveservicedomain) используются вместе для заключения в область кода, которая выполняется в собственном контексте и может использовать службы COM+ без необходимости в компонентах COM+. Службы COM+, используемые в этом контексте, настраиваются с помощью объекта [**ксервицеконфиг**](cserviceconfig.md) , который передается в **коентерсервицедомаин**. Код, окруженный **коентерсервицедомаин** и **колеавесервицедомаин** , ведет себя так, как будто это метод, который вызывается для объекта, созданного в этом контексте.

Приложение для работы со скриптами может использовать эту пару функций для обеспечения поддержки времени выполнения служб COM+ без компонентов. Например, приложение для создания сценариев может быть разработано для предоставления тегов, позволяющих создателям сценариев вводить и оставлять в скрипте домен службы. Когда обработчик скриптов обрабатывает скрипт и обнаруживает теги, он может вызвать [**коентерсервицедомаин**](/windows/desktop/api/ComSvcs/nf-comsvcs-coenterservicedomain) с предварительно настроенным объектом [**ксервицеконфиг**](cserviceconfig.md) , запустить необходимый код и затем вызвать [**колеавесервицедомаин**](/windows/desktop/api/ComSvcs/nf-comsvcs-coleaveservicedomain).

## <a name="component-services-administrative-tool"></a>Средство администрирования служб компонентов

Не применяется.

## <a name="visual-basic"></a>Visual Basic

Не применяется.

## <a name="cc"></a>C/C++

В следующем фрагменте кода показано, как использовать службы COM+ между вызовами [**коентерсервицедомаин**](/windows/desktop/api/ComSvcs/nf-comsvcs-coenterservicedomain) и [**колеавесервицедомаин**](/windows/desktop/api/ComSvcs/nf-comsvcs-coleaveservicedomain). Обработка ошибок опущена для краткости. Этот фрагмент кода использует объект [**ксервицеконфиг**](cserviceconfig.md) , который был создан и настроен в [настройке служб COM+ с помощью ксервицеконфиг](configuring-com--services-with-cserviceconfig.md).


```C++
// A CServiceConfig object was created as follows:
// hr = CoCreateInstance(CLSID_CServiceConfig, NULL, CLSCTX_INPROC_SERVER, 
//   IID_IUnknown, (void**)&pUnknownCSC);

// Enter the Service Domain.
HRESULT hr = CoEnterServiceDomain(pUnknownCSC);
if (FAILED(hr)) throw(hr);

// Do the work that uses COM+ services here.
//DoMyWork();

// Leave the Service Domain.
CoLeaveServiceDomain(NULL);
```



## <a name="related-topics"></a>См. также

<dl> <dt>

[**коентерсервицедомаин**](/windows/desktop/api/ComSvcs/nf-comsvcs-coenterservicedomain)
</dt> <dt>

[**колеавесервицедомаин**](/windows/desktop/api/ComSvcs/nf-comsvcs-coleaveservicedomain)
</dt> <dt>

[Настройка служб COM+ с помощью Ксервицеконфиг](configuring-com--services-with-cserviceconfig.md)
</dt> <dt>

[**ксервицеконфиг**](cserviceconfig.md)
</dt> <dt>

[Использование служб COM+ через Кокреатеактивити](using-com--services-through-cocreateactivity.md)
</dt> </dl>

 

 



