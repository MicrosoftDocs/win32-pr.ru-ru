---
title: Использование Иадсекстенсион
description: В этом разделе содержатся примеры кода C++ для использования интерфейса Иадсекстенсион.
ms.assetid: 56bc87b4-f3cf-4177-90cb-e745889f8fef
ms.tgt_platform: multiple
keywords:
- расширения ADSI, Иадсекстенсион
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a844d320b28548e9e9998881fd2a09815d1882e9
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104252756"
---
# <a name="iadsextension-usage"></a>Использование Иадсекстенсион

[**Иадсекстенсион**](/windows/desktop/api/Iads/nn-iads-iadsextension) — это необязательный интерфейс, реализуемый модулем записи расширений при соблюдении хотя бы одного из следующих условий.

-   Компонент расширения требует уведомления об инициализации, как определено в **ADSI \_ ext \_ * двкоде*** в методе [**работы**](/windows/desktop/api/Iads/nf-iads-iadsextension-operate) .
-   Расширение поддерживает два интерфейса или интерфейс диспетчеризации.

Если компонент расширения поддерживает интерфейс [**иадсекстенсион**](/windows/desktop/api/Iads/nn-iads-iadsextension) по первой причине, методы [**Иадсекстенсион::P риватежетидсофнамес**](/windows/desktop/api/Iads/nf-iads-iadsextension-privategetidsofnames) и [**иадсекстенсион::P риватеинвоке**](/windows/desktop/api/Iads/nf-iads-iadsextension-privateinvoke) могут возвращать **E \_ нотимпл**. Кроме того, если компонент расширения поддерживает два интерфейса или интерфейс диспетчеризации, метод [**работы**](/windows/desktop/api/Iads/nf-iads-iadsextension-operate) может игнорировать данные и вернуть **значение HRESULT** **\_ нотимпл E**.

В следующем коде показано расширение, реализующее реализацию [**иадсекстенсион**](/windows/desktop/api/Iads/nn-iads-iadsextension).


```C++
STDMETHOD(Operate)(ULONG dwCode, VARIANT varData1, VARIANT varData2, VARIANT varData3)
{
    HRESULT hr = S_OK;
    switch (dwCode) 
    {
    case ADS_EXT_INIT:
         // Prompt for a credential.
         // MessageBox(NULL, "INITCRED", "ADsExt", MB_OK);
          break;
    default:
          hr = E_FAIL;
          break;
    }        
    return hr;        
}
 
STDMETHOD(PrivateGetIDsOfNames)(REFIID riid, OLECHAR ** rgszNames, unsigned int cNames, LCID lcid, DISPID  * rgdispid)
{        
      if (rgdispid == NULL)
      {
        return E_POINTER;
      }    
    return  DispGetIDsOfNames(m_pTypeInfo, rgszNames, cNames, rgdispid);
}
 
STDMETHOD(PrivateInvoke)(DISPID dispidMember, REFIID riid, LCID lcid, WORD wFlags, DISPPARAMS * pdispparams, VARIANT * pvarResult, EXCEPINFO * pexcepinfo, UINT * puArgErr)
{
 return DispInvoke( (IHelloWorld*)this, 
           m_pTypeInfo,
        dispidMember, 
        wFlags, 
        pdispparams, 
        pvarResult, 
        pexcepinfo, 
        puArgErr );
}
```



 

 




