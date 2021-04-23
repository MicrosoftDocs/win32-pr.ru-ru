---
description: Поставщики могут вызывать методы, реализованные WMI, из их реализаций методов.
ms.assetid: 5bfd9d9b-ffe5-4def-a97d-85c4c01223f0
ms.tgt_platform: multiple
title: Выполнение вызовов к WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 534e478336cdd9675e382ef9b089f2d7bc595b03
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104080833"
---
# <a name="making-calls-to-wmi"></a><span data-ttu-id="788ca-103">Выполнение вызовов к WMI</span><span class="sxs-lookup"><span data-stu-id="788ca-103">Making Calls to WMI</span></span>

<span data-ttu-id="788ca-104">Поставщики могут вызывать методы, реализованные WMI, из их реализаций методов.</span><span class="sxs-lookup"><span data-stu-id="788ca-104">Providers can call methods implemented by WMI from within their method implementations.</span></span> <span data-ttu-id="788ca-105">Однако существуют особые соображения, когда поставщик вызывает реализацию WMI метода [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) в собственной реализации того же метода.</span><span class="sxs-lookup"><span data-stu-id="788ca-105">However, there are special considerations when a provider calls the WMI implementation of an [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) method from within its own implementation of the same method.</span></span> <span data-ttu-id="788ca-106">Эти соображения важны, независимо от того, вызывает ли поставщик синхронную или асинхронную версию метода.</span><span class="sxs-lookup"><span data-stu-id="788ca-106">These considerations are important regardless of whether the provider calls the synchronous or asynchronous version of the method.</span></span>

<span data-ttu-id="788ca-107">Каждый метод [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) , который может реализовать поставщик, имеет параметр *пкткс* — указатель на реализацию интерфейса [**ивбемконтекст**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemcontext) .</span><span class="sxs-lookup"><span data-stu-id="788ca-107">Each [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) method that a provider can implement has a *pCtx* parameter, a pointer to an [**IWbemContext**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemcontext) interface implementation.</span></span> <span data-ttu-id="788ca-108">Когда WMI вызывает поставщик, Инструментарий WMI передает допустимый указатель в этом параметре.</span><span class="sxs-lookup"><span data-stu-id="788ca-108">When WMI calls the provider, WMI passes a valid pointer in this parameter.</span></span> <span data-ttu-id="788ca-109">Поставщик должен всегда передавать этот же указатель в любые вызовы инструментария WMI, которые они делают во время обслуживания запросов.</span><span class="sxs-lookup"><span data-stu-id="788ca-109">A provider must always pass this same pointer in any calls to WMI that they make while servicing requests.</span></span> <span data-ttu-id="788ca-110">Неправильное задание *пкткс* может привести к тому, что инструментарий WMI сможет запустить бесконечный цикл.</span><span class="sxs-lookup"><span data-stu-id="788ca-110">Neglecting to set *pCtx* appropriately can cause WMI to start an infinite loop.</span></span>

<span data-ttu-id="788ca-111">В следующем примере кода показан правильный способ вызова реализации WMI для [**GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject) из реализации [**жетобжектасинк**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync).</span><span class="sxs-lookup"><span data-stu-id="788ca-111">The following code example shows the correct way to call the WMI implementation of [**GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject) from within an implementation of [**GetObjectAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync).</span></span>


```C++
STDMETHODIMP CClassProv::GetObjectAsync (BSTR ObjectPath,
    long lFlags, IWbemContext *pCtx,
    IWbemObjectSink *pHandler)
{
  IWbemClassObject *pclObj = NULL;
  IWbemServices* m_pNamespace;
  HRESULT hr = m_pNamespace->GetObject(
      _bstr_t(L"AClass"), 0, pCtx, &pclObj, 
      NULL );
  pclObj->Release();
  return pHandler->SetStatus(0, hr, NULL, NULL);
}
```



<span data-ttu-id="788ca-112">В примере кода C++ в этом разделе для правильной компиляции требуются следующие ссылки и \# инструкции include.</span><span class="sxs-lookup"><span data-stu-id="788ca-112">The C++ code example in this topic requires the following references and \#include statements to compile correctly.</span></span>


```C++
#define _WIN32_DCOM
#include <iostream>
using namespace std;
#include <comdef.h>
#include <Wbemidl.h>
#pragma comment(lib, "wbemuuid.lib")
```



<span data-ttu-id="788ca-113">Поставщики экземпляров, классов и свойств не должны выдавать никаких вызовов WMI, запрашивающих изменение данных, при обслуживании запроса на чтение.</span><span class="sxs-lookup"><span data-stu-id="788ca-113">Instance, class, and property providers must not issue any calls to WMI requesting the modification of data while servicing a read request.</span></span> <span data-ttu-id="788ca-114">Единственными поставщиками, которые являются исключениями из этого правила, являются поставщики push-уведомлений.</span><span class="sxs-lookup"><span data-stu-id="788ca-114">The only providers that are exceptions to this rule are push providers.</span></span> <span data-ttu-id="788ca-115">Поставщик услуг push-уведомлений — это поставщик классов, который хранит данные в репозитории WMI и использует инструментарий WMI для обработки запросов от клиентов.</span><span class="sxs-lookup"><span data-stu-id="788ca-115">A push provider is a class provider that stores data in the WMI repository and relies on WMI to handle requests from clients.</span></span> <span data-ttu-id="788ca-116">При обслуживании запроса на чтение поставщик push-уведомлений может обновить репозиторий WMI, но должен установить для параметра *лфлагс* значение WBEM, соответствующее параметру, в соответствующем вызове [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) . **\_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="788ca-116">While servicing a read request, a push provider can update the WMI repository, but must set the *lFlags* parameter to **WBEM\_FLAG\_OWNER\_UPDATE** in the appropriate [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) call.</span></span>

<span data-ttu-id="788ca-117">Поставщики событий не должны вносить изменения в классы при обслуживании вызова.</span><span class="sxs-lookup"><span data-stu-id="788ca-117">Event providers must not make any class changes while servicing a call.</span></span> <span data-ttu-id="788ca-118">Они также не могут выдавать вызовы, связанные с событиями, например изменение фильтра событий.</span><span class="sxs-lookup"><span data-stu-id="788ca-118">They also cannot issue any event-related calls, such as modifying an event filter.</span></span>

## <a name="related-topics"></a><span data-ttu-id="788ca-119">См. также</span><span class="sxs-lookup"><span data-stu-id="788ca-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="788ca-120">Разработка поставщика WMI</span><span class="sxs-lookup"><span data-stu-id="788ca-120">Developing a WMI Provider</span></span>](developing-a-wmi-provider.md)
</dt> <dt>

[<span data-ttu-id="788ca-121">Настройка дескрипторов безопасности Намепаце</span><span class="sxs-lookup"><span data-stu-id="788ca-121">Setting Namepace Security Descriptors</span></span>](setting-namespace-security-descriptors.md)
</dt> <dt>

[<span data-ttu-id="788ca-122">Защита поставщика</span><span class="sxs-lookup"><span data-stu-id="788ca-122">Securing Your Provider</span></span>](securing-your-provider.md)
</dt> </dl>

 

 



