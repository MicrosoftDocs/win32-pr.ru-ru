---
description: Поставщики могут вызывать методы, реализованные WMI, из их реализаций методов.
ms.assetid: 5bfd9d9b-ffe5-4def-a97d-85c4c01223f0
ms.tgt_platform: multiple
title: Выполнение вызовов к WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 76adae33db786a8174879e6c7e88b62fb69f3c59598ae7f055f41865b32dbf7f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118317678"
---
# <a name="making-calls-to-wmi"></a>Выполнение вызовов к WMI

Поставщики могут вызывать методы, реализованные WMI, из их реализаций методов. Однако существуют особые соображения, когда поставщик вызывает реализацию WMI метода [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) в собственной реализации того же метода. Эти соображения важны, независимо от того, вызывает ли поставщик синхронную или асинхронную версию метода.

Каждый метод [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) , который может реализовать поставщик, имеет параметр *пкткс* — указатель на реализацию интерфейса [**ивбемконтекст**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemcontext) . Когда WMI вызывает поставщик, Инструментарий WMI передает допустимый указатель в этом параметре. Поставщик должен всегда передавать этот же указатель в любые вызовы инструментария WMI, которые они делают во время обслуживания запросов. Неправильное задание *пкткс* может привести к тому, что инструментарий WMI сможет запустить бесконечный цикл.

В следующем примере кода показан правильный способ вызова реализации WMI для [**GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject) из реализации [**жетобжектасинк**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync).


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



В примере кода C++ в этом разделе для правильной компиляции требуются следующие ссылки и \# инструкции include.


```C++
#define _WIN32_DCOM
#include <iostream>
using namespace std;
#include <comdef.h>
#include <Wbemidl.h>
#pragma comment(lib, "wbemuuid.lib")
```



Поставщики экземпляров, классов и свойств не должны выдавать никаких вызовов WMI, запрашивающих изменение данных, при обслуживании запроса на чтение. Единственными поставщиками, которые являются исключениями из этого правила, являются поставщики push-уведомлений. Поставщик услуг push-уведомлений — это поставщик классов, который хранит данные в репозитории WMI и использует инструментарий WMI для обработки запросов от клиентов. При обслуживании запроса на чтение поставщик push-уведомлений может обновить репозиторий WMI, но должен установить для параметра *лфлагс* значение WBEM, соответствующее параметру, в соответствующем вызове [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) . **\_ \_ \_**

Поставщики событий не должны вносить изменения в классы при обслуживании вызова. Они также не могут выдавать вызовы, связанные с событиями, например изменение фильтра событий.

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Разработка поставщика WMI](developing-a-wmi-provider.md)
</dt> <dt>

[Настройка дескрипторов безопасности Намепаце](setting-namespace-security-descriptors.md)
</dt> <dt>

[Защита поставщика](securing-your-provider.md)
</dt> </dl>

 

 



