---
title: Написание пользовательского суррогата
description: Написание пользовательского суррогата
ms.assetid: 510e38e5-1965-46f4-b09c-6fa585cff993
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 32c6098f4d0e9d99be86956bacce413e7e8a4b864a91212d6c2a1a257d9c1db7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119047662"
---
# <a name="writing-a-custom-surrogate"></a>Написание пользовательского суррогата

Хотя предоставляемый системой суррогат будет более адекватным для большинства ситуаций, в некоторых случаях может быть целесообразно написать пользовательский суррогат. Ниже приводятся некоторые примеры.

-   Пользовательский суррогат может предоставлять некоторые оптимизации или семантику, отсутствующие в суррогате системы.
-   Если внутрипроцессный DLL содержит код, который зависит от того, какой процесс находится в том же процессе, что и клиент, то сервер DLL не будет работать правильно, если он выполняется в системном суррогате. Пользовательский суррогат можно адаптировать к конкретной библиотеке DLL для решения этой проблемы.
-   Системный суррогат поддерживает модель смешанной потоковой передачи, чтобы она могла загружать как свободные, так и подразделенные библиотеки DLL модели. Пользовательский суррогат может быть адаптирован для загрузки только библиотек подразделений для повышения эффективности или принятия аргумента командной строки для типа библиотеки DLL, для которой разрешена загрузка.
-   Пользовательский суррогат может принимать дополнительные параметры командной строки, которые не являются суррогатами системы.
-   Системный суррогат вызывает [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) и указывает, что он должен использовать существующие параметры безопасности, найденные в разделе [AppID](appid-key.md) в реестре. Пользовательский суррогат может использовать другой контекст безопасности.
-   Интерфейсы, которые не поддерживают удаленное взаимодействие (например, для последних Окксс), не будут работать с суррогатом системы. Пользовательский суррогат может заключить интерфейсы библиотеки DLL в собственную реализацию и использовать прокси-библиотеки-заглушки с определением IDL с удаленным доступом, которое позволило бы разрешить удаленный интерфейс.

Основной суррогатный поток обычно должен выполнять следующие действия по настройке:

1.  Вызов [**CoInitializeEx**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializeex) для инициализации потока и установки потоковой модели.
2.  Если требуется, чтобы серверы DLL, работающие на сервере, могли использовать параметры безопасности в разделе реестра **AppID** , вызовите [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) с помощью \_ функции еоак AppID. В противном случае будут использоваться устаревшие параметры безопасности.
3.  Вызовите [**корегистерсуррогате**](/windows/desktop/api/combaseapi/nf-combaseapi-coregistersurrogate) , чтобы зарегистрировать суррогатный интерфейс в com.
4.  Вызовите [**исуррогате:: лоаддллсервер**](/windows/win32/api/objidlbase/nf-objidlbase-isurrogate-loaddllserver) для ЗАПРОШЕННОГО идентификатора CLSID.
5.  Поставьте главный поток в цикл, чтобы периодически вызывать [**кофриунуседлибрариес**](/windows/desktop/api/combaseapi/nf-combaseapi-cofreeunusedlibraries) .
6.  Когда COM вызывает [**исуррогате:: фрисуррогате**](/windows/win32/api/objidlbase/nf-objidlbase-isurrogate-freesurrogate), отмените все фабрики классов и завершите работу.

Суррогатный процесс должен реализовывать интерфейс [**исуррогате**](/windows/win32/api/objidlbase/nn-objidlbase-isurrogate) . Этот интерфейс должен быть зарегистрирован при запуске нового суррогата и после вызова [**CoInitializeEx**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializeex). Как показано на предыдущих шагах, интерфейс **исуррогате** имеет два метода, которые вызываются com: [**лоаддллсервер**](/windows/win32/api/objidlbase/nf-objidlbase-isurrogate-loaddllserver)для динамической загрузки новых серверов DLL в существующие суррогаты. и [**фрисуррогате**](/windows/win32/api/objidlbase/nf-objidlbase-isurrogate-freesurrogate), чтобы освободить суррогат.

Реализация [**лоаддллсервер**](/windows/win32/api/objidlbase/nf-objidlbase-isurrogate-loaddllserver), которая вызывает com с запросом загрузки, должна сначала создать объект фабрики класса, поддерживающий [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown), [**IClassFactory**](/windows/win32/api/unknwn/nn-unknwn-iclassfactory)и [**IMarshal**](/windows/win32/api/objidlbase/nn-objidlbase-imarshal), а затем вызвать [**CoRegisterClassObject**](/windows/desktop/api/combaseapi/nf-combaseapi-coregisterclassobject) для регистрации объекта в качестве фабрики класса для запрошенного идентификатора CLSID.

Фабрика классов, зарегистрированная суррогатным процессом, не является действительной фабрикой класса, реализованной на сервере DLL, но является фабрикой универсального класса, реализованной суррогатным процессом, который поддерживает [**IClassFactory**](/windows/win32/api/unknwn/nn-unknwn-iclassfactory) и [**IMarshal**](/windows/win32/api/objidlbase/nn-objidlbase-imarshal). Поскольку это фабрика класса суррогата, а не зарегистрированный сервер DLL, фабрике класса-суррогата потребуется использовать реальную фабрику классов для создания экземпляра объекта для зарегистрированного идентификатора CLSID. Суррогат [**IClassFactory:: CreateInstance**](/windows/desktop/api/Unknwn/nf-unknwn-iclassfactory-createinstance) должен выглядеть примерно так, как показано в следующем примере:


```C++
STDMETHODIMP CSurrogateFactory::CreateInstance(
  IUnknown* pUnkOuter, 
  REFIID iid, 
  void** ppv)
{
    void* pcf;
    HRESULT hr;
 
    hr = CoGetClassObject(clsid, CLSCTX_INPROC_SERVER, NULL, IID_IClassFactory, &pcf);
    if ( FAILED(hr) )
        return hr;
    hr = ((IClassFactory*)pcf)->CreateInstance(pUnkOuter, iid, ppv);
    ((IClassFactory*)pcf)->Release();
    return hr;
}
 
```



Фабрика класса-суррогата также должна поддерживать [**IMarshal**](/windows/win32/api/objidlbase/nn-objidlbase-imarshal) , так как вызов [**кожетклассобжект**](/windows/desktop/api/combaseapi/nf-combaseapi-cogetclassobject) может запросить любой интерфейс из зарегистрированной фабрики класса, а не только [**IClassFactory**](/windows/win32/api/unknwn/nn-unknwn-iclassfactory). Кроме того, поскольку универсальная фабрика классов поддерживает только [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) и **IClassFactory**, запросы для других интерфейсов должны направляться в реальный объект. Таким образом, должен быть метод [**MarshalInterface**](/windows/win32/api/objidlbase/nf-objidlbase-imarshal-marshalinterface) , который должен выглядеть следующим образом:


```C++
STDMETHODIMP CSurrogateFactory::MarshalInterface(
  IStream *pStm,  
  REFIID riid, void *pv, 
  WORD dwDestContext, 
  void *pvDestContext, 
  DWORD mshlflags )
{   
    void * pCF = NULL;
    HRESULT hr;
 
    hr = CoGetClassObject(clsid, CLSCTX_INPROC_SERVER, NULL, riid, &pCF);
    if ( FAILED(hr) )
        return hr;   
    hr = CoMarshalInterface(pStm, riid, (IUnknown*)pCF, dwDestContext, pvDestContext,  mshlflags);
    ((IUnknown*)pCF)->Release();
    return S_OK;
 
```



Суррогат, который вмещает сервер DLL, должен опубликовать объекты класса (-ов) сервера DLL с помощью вызова [**CoRegisterClassObject**](/windows/desktop/api/combaseapi/nf-combaseapi-coregisterclassobject). Все фабрики классов для суррогатов DLL должны быть зарегистрированы как \_ суррогаты регклс. РЕГКЛС \_ синглусе и регклс \_ мултиплеусе не должны использоваться для серверов DLL, загруженных в суррогаты.

Следуйте приведенным ниже рекомендациям по созданию суррогатного процесса, когда это необходимо, чтобы обеспечить правильное поведение.

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Суррогаты библиотеки DLL](dll-surrogates.md)
</dt> </dl>

 

 