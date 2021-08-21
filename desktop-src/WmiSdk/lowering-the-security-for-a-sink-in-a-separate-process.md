---
description: Windows Инструментарий управления (WMI) может создавать приемник для получения асинхронных обратных вызовов для клиентского приложения в отдельном процессе.
ms.assetid: 3d3111ac-7d83-48d6-94e4-36cb46a506fa
ms.tgt_platform: multiple
title: Понижение безопасности приемника в отдельном процессе
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bea1898503c57edc40b2eec147d251127fac8467bd1128656aed873d08366696
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118818402"
---
# <a name="lowering-the-security-for-a-sink-in-a-separate-process"></a>Понижение безопасности приемника в отдельном процессе

Windows Инструментарий управления (WMI) может создавать приемник для получения асинхронных обратных вызовов для клиентского приложения в отдельном процессе. Отдельный процесс Unsecapp.exe. Используйте интерфейс [**ивбемунсекуредапартмент**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemunsecuredapartment) . **Ивбемунсекуредапартмент** позволяет управлять проверкой подлинности обратных вызовов в приемнике Unsecapp.exe. Дополнительные сведения см. [в разделе Настройка безопасности при асинхронном вызове](setting-security-on-an-asynchronous-call.md).

Затем можно снизить безопасность этого процесса, и WMI сможет получить доступ к приемнику без ограничений. Для помощи с этим методом Инструментарий WMI предоставляет Unsecapp.exe процесс для работы в качестве отдельного процесса. Unsecapp.exe можно разместить с помощью вызова интерфейса [**иунсекуредапартмент**](/windows/desktop/api/Wbemcli/nn-wbemcli-iunsecuredapartment) .

Интерфейс [**иунсекуредапартмент**](/windows/desktop/api/Wbemcli/nn-wbemcli-iunsecuredapartment) позволяет клиентскому приложению создавать отдельный выделенный процесс, выполняющий Unsecapp.exe для размещения реализации [**ивбемобжектсинк**](iwbemobjectsink.md) . Выделенный процесс может вызвать [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity) , чтобы предоставить WMI доступ к выделенному процессу, не нарушая безопасность основного процесса. После инициализации выделенный процесс выступает в качестве посредника между основным процессом и WMI.

В следующей процедуре описывается выполнение асинхронного вызова с помощью [**иунсекуредапартмент**](/windows/desktop/api/Wbemcli/nn-wbemcli-iunsecuredapartment).

**Выполнение асинхронного вызова с помощью Иунсекуредапартмент**

1.  Создайте выделенный процесс с вызовом [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance).

    В следующем примере кода метод [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) вызывается для создания выделенного процесса.

    ```C++
    IUnsecuredApartment* pUnsecApp = NULL;

    CoCreateInstance(CLSID_UnsecuredApartment, NULL, 
      CLSCTX_LOCAL_SERVER, IID_IUnsecuredApartment, 
      (void**)&pUnsecApp);
    ```

    

2.  Создайте экземпляр объекта приемника.

    В следующем примере кода создается новый объект приемника.

    ```C++
    CMySink* pSink = new CMySink;
    pSink->AddRef();
    ```

    

3.  Создайте заглушку для приемника.

    Заглушка — это функция-оболочка, созданная из приемника.

    В следующем примере кода вызывается [**креатеобжектстуб**](/windows/desktop/api/Wbemcli/nf-wbemcli-iunsecuredapartment-createobjectstub) , чтобы создать заглушку для приемника.

    ```C++
    IUnknown* pStubUnk = NULL; 
    pUnsecApp->CreateObjectStub(pSink, &pStubUnk);
    ```

    

4.  Вызовите [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) для оболочки и запросите указатель на интерфейс [**ивбемобжектсинк**](iwbemobjectsink.md) .

    В следующем примере кода метод [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) вызывается и запрашивается указатель на интерфейс [**ивбемобжектсинк**](iwbemobjectsink.md) .

    ```C++
    IWbemObjectSink* pStubSink = NULL;
    pStubUnk->QueryInterface(IID_IWbemObjectSink, (void **)&pStubSink); pStubUnk->Release();
    ```

    

5.  Освободите указатель объекта приемника.

    Можно освободить указатель на объект, так как заглушка теперь является владельцем указателя.

    В следующем примере кода освобождается указатель объекта приемника.

    ```C++
    pSink->Release();
    ```

    

6.  Используйте заглушку при любом асинхронном вызове.

    По завершении работы с вызовом Освободите локальный счетчик ссылок.

    В следующем примере кода заглушка используется в асинхронном вызове.

    ```C++
    // pServices is an IWbemServices* object
    pServices->CreateInstanceEnumAsync(strClassName, 0, NULL, pStubSink);
    ```

    

    Иногда может потребоваться отменить асинхронный вызов после выполнения вызова. Если необходимо отменить вызов, отмените вызов с тем же указателем, который был изначально выполнил вызов.

    В следующем примере кода показано, как отменить асинхронный вызов.

    ```C++
    pServices->CancelAsyncCall(pStubSink);
    ```

    

7.  При завершении использования асинхронного вызова Освободите локальный счетчик ссылок.

    Не забудьте освободить указатель *пстубсинк* только после того, как вы подтвердите, что асинхронный вызов не нужно отменять. Кроме того, не освобождайте *пстубсинк* после того, как инструментарий WMI освобождает указатель приемника *псинк* . При освобождении *пстубсинк* после *псинк* создается циклическая ссылка, в которой приемник и заглушка постоянно остаются в памяти. Вместо этого можно освободить указатель в вызове [**ивбемобжектсинк:: SetStatus**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjectsink-setstatus) , СДЕЛАНном WMI, чтобы сообщить о завершении исходного асинхронного вызова.

8.  После завершения выполните деинициализацию COM с помощью вызова метода [**Release ()**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release).

    В следующем примере кода показано, как вызвать метод [**Release ()**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) для указателя *пунсекапп* .

    ```C++
    pUnsecApp->Release();
    ```

    

    В примерах кода в этом разделе \# для правильной компиляции требуется следующая инструкция Reference и include.

    ```C++
    #include <wbemidl.h>
    #pragma comment(lib, "wbemuuid.lib")
    ```

    

Дополнительные сведения о функции и параметрах [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity) см. в документации по [com](../cossdk/component-services-portal.md) в пакете SDK для платформы.

 

 
