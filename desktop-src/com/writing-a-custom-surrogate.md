---
title: Написание пользовательского суррогата
description: Написание пользовательского суррогата
ms.assetid: 510e38e5-1965-46f4-b09c-6fa585cff993
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: af0899702f6626d586f8a819e8fee2c2e67b7c80
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/21/2020
ms.locfileid: "104339313"
---
# <a name="writing-a-custom-surrogate"></a><span data-ttu-id="34b88-103">Написание пользовательского суррогата</span><span class="sxs-lookup"><span data-stu-id="34b88-103">Writing a Custom Surrogate</span></span>

<span data-ttu-id="34b88-104">Хотя предоставляемый системой суррогат будет более адекватным для большинства ситуаций, в некоторых случаях может быть целесообразно написать пользовательский суррогат.</span><span class="sxs-lookup"><span data-stu-id="34b88-104">While the system-supplied surrogate will be more than adequate for most situations, there are some cases where writing a custom surrogate could be worthwhile.</span></span> <span data-ttu-id="34b88-105">Ниже приводятся некоторые примеры.</span><span class="sxs-lookup"><span data-stu-id="34b88-105">Following are some examples:</span></span>

-   <span data-ttu-id="34b88-106">Пользовательский суррогат может предоставлять некоторые оптимизации или семантику, отсутствующие в суррогате системы.</span><span class="sxs-lookup"><span data-stu-id="34b88-106">A custom surrogate could provide some optimizations or semantics not present in the system surrogate.</span></span>
-   <span data-ttu-id="34b88-107">Если внутрипроцессный DLL содержит код, который зависит от того, какой процесс находится в том же процессе, что и клиент, то сервер DLL не будет работать правильно, если он выполняется в системном суррогате.</span><span class="sxs-lookup"><span data-stu-id="34b88-107">If an in-process DLL contains code that depends on being in the same process as the client, the DLL server will not function correctly if it is running in the system surrogate.</span></span> <span data-ttu-id="34b88-108">Пользовательский суррогат можно адаптировать к конкретной библиотеке DLL для решения этой проблемы.</span><span class="sxs-lookup"><span data-stu-id="34b88-108">A custom surrogate could be tailored to a specific DLL to deal with this.</span></span>
-   <span data-ttu-id="34b88-109">Системный суррогат поддерживает модель смешанной потоковой передачи, чтобы она могла загружать как свободные, так и подразделенные библиотеки DLL модели.</span><span class="sxs-lookup"><span data-stu-id="34b88-109">The system surrogate supports a mixed-threading model so that it can load both free and apartment model DLLs.</span></span> <span data-ttu-id="34b88-110">Пользовательский суррогат может быть адаптирован для загрузки только библиотек подразделений для повышения эффективности или принятия аргумента командной строки для типа библиотеки DLL, для которой разрешена загрузка.</span><span class="sxs-lookup"><span data-stu-id="34b88-110">A custom surrogate might be tailored to load only apartment DLLs for reasons of efficiency or to accept a command-line argument for the type of DLL it is allowed to load.</span></span>
-   <span data-ttu-id="34b88-111">Пользовательский суррогат может принимать дополнительные параметры командной строки, которые не являются суррогатами системы.</span><span class="sxs-lookup"><span data-stu-id="34b88-111">A custom surrogate could take extra command-line parameters that the system surrogate does not.</span></span>
-   <span data-ttu-id="34b88-112">Системный суррогат вызывает [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) и указывает, что он должен использовать существующие параметры безопасности, найденные в разделе [AppID](appid-key.md) в реестре.</span><span class="sxs-lookup"><span data-stu-id="34b88-112">The system surrogate calls [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) and tells it to use any existing security settings found under the [AppID](appid-key.md) key in the registry.</span></span> <span data-ttu-id="34b88-113">Пользовательский суррогат может использовать другой контекст безопасности.</span><span class="sxs-lookup"><span data-stu-id="34b88-113">A custom surrogate could use another security context.</span></span>
-   <span data-ttu-id="34b88-114">Интерфейсы, которые не поддерживают удаленное взаимодействие (например, для последних Окксс), не будут работать с суррогатом системы.</span><span class="sxs-lookup"><span data-stu-id="34b88-114">Interfaces that aren't remotable (such as those for recent OCXs) will not work with the system surrogate.</span></span> <span data-ttu-id="34b88-115">Пользовательский суррогат может заключить интерфейсы библиотеки DLL в собственную реализацию и использовать прокси-библиотеки-заглушки с определением IDL с удаленным доступом, которое позволило бы разрешить удаленный интерфейс.</span><span class="sxs-lookup"><span data-stu-id="34b88-115">A custom surrogate could wrap the DLL's interfaces with its own implementation and use proxy/stub DLLs with a remotable IDL definition that would allow the interface to be remoted.</span></span>

<span data-ttu-id="34b88-116">Основной суррогатный поток обычно должен выполнять следующие действия по настройке:</span><span class="sxs-lookup"><span data-stu-id="34b88-116">The main surrogate thread should typically perform the following setup steps:</span></span>

1.  <span data-ttu-id="34b88-117">Вызов [**CoInitializeEx**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializeex) для инициализации потока и установки потоковой модели.</span><span class="sxs-lookup"><span data-stu-id="34b88-117">Call [**CoInitializeEx**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializeex) to initialize the thread and set the threading model.</span></span>
2.  <span data-ttu-id="34b88-118">Если требуется, чтобы серверы DLL, работающие на сервере, могли использовать параметры безопасности в разделе реестра **AppID** , вызовите [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) с помощью \_ функции еоак AppID.</span><span class="sxs-lookup"><span data-stu-id="34b88-118">If you want the DLL servers that are to run in the server to be able to use the security settings in the **AppID** registry key, call [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) with the EOAC\_APPID capability.</span></span> <span data-ttu-id="34b88-119">В противном случае будут использоваться устаревшие параметры безопасности.</span><span class="sxs-lookup"><span data-stu-id="34b88-119">Otherwise, legacy security settings will be used.</span></span>
3.  <span data-ttu-id="34b88-120">Вызовите [**корегистерсуррогате**](/windows/desktop/api/combaseapi/nf-combaseapi-coregistersurrogate) , чтобы зарегистрировать суррогатный интерфейс в com.</span><span class="sxs-lookup"><span data-stu-id="34b88-120">Call [**CoRegisterSurrogate**](/windows/desktop/api/combaseapi/nf-combaseapi-coregistersurrogate) to register the surrogate interface to COM.</span></span>
4.  <span data-ttu-id="34b88-121">Вызовите [**исуррогате:: лоаддллсервер**](/windows/win32/api/objidlbase/nf-objidlbase-isurrogate-loaddllserver) для ЗАПРОШЕННОГО идентификатора CLSID.</span><span class="sxs-lookup"><span data-stu-id="34b88-121">Call [**ISurrogate::LoadDllServer**](/windows/win32/api/objidlbase/nf-objidlbase-isurrogate-loaddllserver) for the requested CLSID.</span></span>
5.  <span data-ttu-id="34b88-122">Поставьте главный поток в цикл, чтобы периодически вызывать [**кофриунуседлибрариес**](/windows/desktop/api/combaseapi/nf-combaseapi-cofreeunusedlibraries) .</span><span class="sxs-lookup"><span data-stu-id="34b88-122">Put main thread in a loop to call [**CoFreeUnusedLibraries**](/windows/desktop/api/combaseapi/nf-combaseapi-cofreeunusedlibraries) periodically.</span></span>
6.  <span data-ttu-id="34b88-123">Когда COM вызывает [**исуррогате:: фрисуррогате**](/windows/win32/api/objidlbase/nf-objidlbase-isurrogate-freesurrogate), отмените все фабрики классов и завершите работу.</span><span class="sxs-lookup"><span data-stu-id="34b88-123">When COM calls [**ISurrogate::FreeSurrogate**](/windows/win32/api/objidlbase/nf-objidlbase-isurrogate-freesurrogate), revoke all class factories and exit.</span></span>

<span data-ttu-id="34b88-124">Суррогатный процесс должен реализовывать интерфейс [**исуррогате**](/windows/win32/api/objidlbase/nn-objidlbase-isurrogate) .</span><span class="sxs-lookup"><span data-stu-id="34b88-124">A surrogate process must implement the [**ISurrogate**](/windows/win32/api/objidlbase/nn-objidlbase-isurrogate) interface.</span></span> <span data-ttu-id="34b88-125">Этот интерфейс должен быть зарегистрирован при запуске нового суррогата и после вызова [**CoInitializeEx**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializeex).</span><span class="sxs-lookup"><span data-stu-id="34b88-125">This interface should be registered when a new surrogate is started and after calling [**CoInitializeEx**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializeex).</span></span> <span data-ttu-id="34b88-126">Как показано на предыдущих шагах, интерфейс **исуррогате** имеет два метода, которые вызываются com: [**лоаддллсервер**](/windows/win32/api/objidlbase/nf-objidlbase-isurrogate-loaddllserver)для динамической загрузки новых серверов DLL в существующие суррогаты. и [**фрисуррогате**](/windows/win32/api/objidlbase/nf-objidlbase-isurrogate-freesurrogate), чтобы освободить суррогат.</span><span class="sxs-lookup"><span data-stu-id="34b88-126">As indicated in the preceding steps, the **ISurrogate** interface has two methods that COM calls: [**LoadDllServer**](/windows/win32/api/objidlbase/nf-objidlbase-isurrogate-loaddllserver), to dynamically load new DLL servers into existing surrogates; and [**FreeSurrogate**](/windows/win32/api/objidlbase/nf-objidlbase-isurrogate-freesurrogate), to free the surrogate.</span></span>

<span data-ttu-id="34b88-127">Реализация [**лоаддллсервер**](/windows/win32/api/objidlbase/nf-objidlbase-isurrogate-loaddllserver), которая вызывает com с запросом загрузки, должна сначала создать объект фабрики класса, поддерживающий [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown), [**IClassFactory**](/windows/win32/api/unknwn/nn-unknwn-iclassfactory)и [**IMarshal**](/windows/win32/api/objidlbase/nn-objidlbase-imarshal), а затем вызвать [**CoRegisterClassObject**](/windows/desktop/api/combaseapi/nf-combaseapi-coregisterclassobject) для регистрации объекта в качестве фабрики класса для запрошенного идентификатора CLSID.</span><span class="sxs-lookup"><span data-stu-id="34b88-127">The implementation of [**LoadDllServer**](/windows/win32/api/objidlbase/nf-objidlbase-isurrogate-loaddllserver), which COM calls with a load request, must first create a class factory object that supports [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown), [**IClassFactory**](/windows/win32/api/unknwn/nn-unknwn-iclassfactory), and [**IMarshal**](/windows/win32/api/objidlbase/nn-objidlbase-imarshal), and then call [**CoRegisterClassObject**](/windows/desktop/api/combaseapi/nf-combaseapi-coregisterclassobject) to register the object as the class factory for the requested CLSID.</span></span>

<span data-ttu-id="34b88-128">Фабрика классов, зарегистрированная суррогатным процессом, не является действительной фабрикой класса, реализованной на сервере DLL, но является фабрикой универсального класса, реализованной суррогатным процессом, который поддерживает [**IClassFactory**](/windows/win32/api/unknwn/nn-unknwn-iclassfactory) и [**IMarshal**](/windows/win32/api/objidlbase/nn-objidlbase-imarshal).</span><span class="sxs-lookup"><span data-stu-id="34b88-128">The class factory registered by the surrogate process is not the actual class factory implemented by the DLL server but is a generic class factory implemented by the surrogate process that supports [**IClassFactory**](/windows/win32/api/unknwn/nn-unknwn-iclassfactory) and [**IMarshal**](/windows/win32/api/objidlbase/nn-objidlbase-imarshal).</span></span> <span data-ttu-id="34b88-129">Поскольку это фабрика класса суррогата, а не зарегистрированный сервер DLL, фабрике класса-суррогата потребуется использовать реальную фабрику классов для создания экземпляра объекта для зарегистрированного идентификатора CLSID.</span><span class="sxs-lookup"><span data-stu-id="34b88-129">Because it is the surrogate's class factory, rather than that of the DLL server that is being registered, the surrogate's class factory will need to use the real class factory to create an instance of the object for the registered CLSID.</span></span> <span data-ttu-id="34b88-130">Суррогат [**IClassFactory:: CreateInstance**](/windows/desktop/api/Unknwn/nf-unknwn-iclassfactory-createinstance) должен выглядеть примерно так, как показано в следующем примере:</span><span class="sxs-lookup"><span data-stu-id="34b88-130">The surrogate's [**IClassFactory::CreateInstance**](/windows/desktop/api/Unknwn/nf-unknwn-iclassfactory-createinstance) should look something like the following example:</span></span>


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



<span data-ttu-id="34b88-131">Фабрика класса-суррогата также должна поддерживать [**IMarshal**](/windows/win32/api/objidlbase/nn-objidlbase-imarshal) , так как вызов [**кожетклассобжект**](/windows/desktop/api/combaseapi/nf-combaseapi-cogetclassobject) может запросить любой интерфейс из зарегистрированной фабрики класса, а не только [**IClassFactory**](/windows/win32/api/unknwn/nn-unknwn-iclassfactory).</span><span class="sxs-lookup"><span data-stu-id="34b88-131">The surrogate's class factory must also support [**IMarshal**](/windows/win32/api/objidlbase/nn-objidlbase-imarshal) because a call to [**CoGetClassObject**](/windows/desktop/api/combaseapi/nf-combaseapi-cogetclassobject) can request any interface from the registered class factory, not just [**IClassFactory**](/windows/win32/api/unknwn/nn-unknwn-iclassfactory).</span></span> <span data-ttu-id="34b88-132">Кроме того, поскольку универсальная фабрика классов поддерживает только [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) и **IClassFactory**, запросы для других интерфейсов должны направляться в реальный объект.</span><span class="sxs-lookup"><span data-stu-id="34b88-132">Further, since the generic class factory supports only [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) and **IClassFactory**, requests for other interfaces must be directed to the real object.</span></span> <span data-ttu-id="34b88-133">Таким образом, должен быть метод [**MarshalInterface**](/windows/win32/api/objidlbase/nf-objidlbase-imarshal-marshalinterface) , который должен выглядеть следующим образом:</span><span class="sxs-lookup"><span data-stu-id="34b88-133">Thus, there should be a [**MarshalInterface**](/windows/win32/api/objidlbase/nf-objidlbase-imarshal-marshalinterface) method which should be similar to the following:</span></span>


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



<span data-ttu-id="34b88-134">Суррогат, который вмещает сервер DLL, должен опубликовать объекты класса (-ов) сервера DLL с помощью вызова [**CoRegisterClassObject**](/windows/desktop/api/combaseapi/nf-combaseapi-coregisterclassobject).</span><span class="sxs-lookup"><span data-stu-id="34b88-134">The surrogate that houses a DLL server must publish the DLL server's class object(s) with a call to [**CoRegisterClassObject**](/windows/desktop/api/combaseapi/nf-combaseapi-coregisterclassobject).</span></span> <span data-ttu-id="34b88-135">Все фабрики классов для суррогатов DLL должны быть зарегистрированы как \_ суррогаты регклс.</span><span class="sxs-lookup"><span data-stu-id="34b88-135">All class factories for DLL surrogates should be registered as REGCLS\_SURROGATE.</span></span> <span data-ttu-id="34b88-136">РЕГКЛС \_ синглусе и регклс \_ мултиплеусе не должны использоваться для серверов DLL, загруженных в суррогаты.</span><span class="sxs-lookup"><span data-stu-id="34b88-136">REGCLS\_SINGLUSE and REGCLS\_MULTIPLEUSE should not be used for DLL servers loaded into surrogates.</span></span>

<span data-ttu-id="34b88-137">Следуйте приведенным ниже рекомендациям по созданию суррогатного процесса, когда это необходимо, чтобы обеспечить правильное поведение.</span><span class="sxs-lookup"><span data-stu-id="34b88-137">Following these guidelines for creating a surrogate process when it is necessary to do so should ensure proper behavior.</span></span>

## <a name="related-topics"></a><span data-ttu-id="34b88-138">См. также</span><span class="sxs-lookup"><span data-stu-id="34b88-138">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="34b88-139">Суррогаты библиотеки DLL</span><span class="sxs-lookup"><span data-stu-id="34b88-139">DLL Surrogates</span></span>](dll-surrogates.md)
</dt> </dl>

 

 