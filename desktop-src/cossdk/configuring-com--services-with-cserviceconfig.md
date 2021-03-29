---
description: Настройка служб COM+ с помощью Ксервицеконфиг
ms.assetid: c44743a8-8b91-4e2a-9ba4-4cb6ae787999
title: Настройка служб COM+ с помощью Ксервицеконфиг
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bc8bbc6c3131347f450340863db70fd9b3999730
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103807187"
---
# <a name="configuring-com-services-with-cserviceconfig"></a>Настройка служб COM+ с помощью Ксервицеконфиг

Класс [**ксервицеконфиг**](cserviceconfig.md) используется для настройки служб COM+, которые могут использоваться без компонентов. Он выполняет статистическую обработку свободных потоков, поэтому его можно использовать в разных апартаментах. Чтобы настроить отдельную службу, необходимо вызвать [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) для интерфейса, связанного со службой, а затем вызвать методы для этого интерфейса, чтобы установить соответствующую конфигурацию. В следующей таблице описаны интерфейсы, реализуемые с помощью класса **ксервицеконфиг** .



| Интерфейс                                                                         | Описание                                                                                                                                                                                              |
|-----------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**исервицеинхеританцеконфиг**](/windows/desktop/api/ComSvcs/nn-comsvcs-iserviceinheritanceconfig)<br/>         | Интерфейс по умолчанию для класса. Он используется для быстрой инициализации многих служб COM+.<br/>                                                                                              |
| [**исервицекомтиинтринсиксконфиг**](/windows/desktop/api/ComSvcs/nn-comsvcs-iservicecomtiintrinsicsconfig)<br/> | Используется для настройки сведений о встроенных функциях интегратора транзакций COM (COMTI). COMTI позволяет разработчикам интегрировать программы транзакций на основе мэйнфреймов с приложениями на основе компонентов.<br/> |
| [**исервицеиисинтринсиксконфиг**](/windows/desktop/api/ComSvcs/nn-comsvcs-iserviceiisintrinsicsconfig)<br/>     | Используется для настройки сведений о встроенных параметрах службы IIS (IIS).<br/>                                                                                                             |
| [**исервицепартитионконфиг**](/windows/desktop/api/ComSvcs/nn-comsvcs-iservicepartitionconfig)<br/>             | Используется для настройки использования разделов COM+ со службами.<br/>                                                                                                                             |
| [**исервицескссконфиг**](/windows/desktop/api/ComSvcs/nn-comsvcs-iservicesxsconfig)<br/>                         | Используется для настройки параллельных сборок.<br/>                                                                                                                                                    |
| [**исервицесинчронизатионконфиг**](/windows/desktop/api/ComSvcs/nn-comsvcs-iservicesynchronizationconfig)<br/> | Используется для настройки служб синхронизации COM+.<br/>                                                                                                                                              |
| [**исервицесреадпулконфиг**](/windows/desktop/api/ComSvcs/nn-comsvcs-iservicethreadpoolconfig)<br/>           | Используется для настройки пула потоков для службы COM+. Пул потоков можно настроить только при использовании функции [**кокреатеактивити**](/windows/desktop/api/ComSvcs/nf-comsvcs-cocreateactivity) .<br/>                          |
| [**исервицетраккерконфиг**](/windows/desktop/api/ComSvcs/nn-comsvcs-iservicetrackerconfig)<br/>                 | Используется для настройки свойства Tracker. Средство отслеживания — это механизм создания отчетов, используемый кодом мониторинга для отслеживания кода, в котором работает.<br/>                                                         |
| [**исервицетрансактионконфиг**](/windows/desktop/api/ComSvcs/nn-comsvcs-iservicetransactionconfig)<br/>         | Используется для настройки службы транзакций COM+.<br/>                                                                                                                                               |



 

## <a name="component-services-administrative-tool"></a>Средство администрирования служб компонентов

Не применяется.

## <a name="visual-basic"></a>Visual Basic

Не применяется.

## <a name="cc"></a>C/C++

В следующем фрагменте кода показано, как создать и настроить объект [**ксервицеконфиг**](cserviceconfig.md) для использования транзакций COM+.


```C++
// Create a CServiceConfig object.
HRESULT hr = CoCreateInstance(CLSID_CServiceConfig, NULL, CLSCTX_INPROC_SERVER, 
  IID_IUnknown, (void**)&pUnknownCSC);
if (FAILED(hr)) throw(hr);

// Query for the IServiceInheritanceConfig interface.
hr = pUnknownCSC->QueryInterface(IID_IServiceInheritanceConfig, 
  (void**)&pInheritanceConfig);
if (FAILED(hr)) throw(hr);

// Inherit the current context before using transactions.
hr = pInheritanceConfig->ContainingContextTreatment(CSC_Inherit);
if (FAILED(hr)) throw(hr);

// Query for the IServiceTransactionConfig interface.
hr = pUnknownCSC->QueryInterface(IID_IServiceTransactionConfig, 
  (void**)&pTransactionConfig);
if (FAILED(hr)) throw(hr);

// Configure transactions to always create a new one.
hr = pTransactionConfig->ConfigureTransaction(CSC_NewTransaction);
if (FAILED(hr)) throw(hr);

// Set the isolation level of the transactions to ReadCommitted.
hr = pTransactionConfig->IsolationLevel( 
  COMAdminTxIsolationLevelReadCommitted);
if (FAILED(hr)) throw(hr);

// Set the transaction time-out to 1 minute.
hr = pTransactionConfig->TransactionTimeout(60);
if (FAILED(hr)) throw(hr);

```



## <a name="related-topics"></a>См. также

<dl> <dt>

[**ксервицеконфиг**](cserviceconfig.md)
</dt> <dt>

[Использование служб COM+ через Кокреатеактивити](using-com--services-through-cocreateactivity.md)
</dt> <dt>

[Использование служб COM+ через Коентерсервицедомаин и Колеавесервицедомаин](using-com--services-through-coenterservicedomain-and-coleaveservicedomain.md)
</dt> </dl>

 

