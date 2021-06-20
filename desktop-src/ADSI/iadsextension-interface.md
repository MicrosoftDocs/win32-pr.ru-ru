---
title: Интерфейс Иадсекстенсион
description: Эта статья содержит определение кода C++ для интерфейса Иадсекстенсион и обсуждение его методов.
ms.assetid: fa94cc55-1ab2-4b6e-a3b6-8c20542adb42
ms.tgt_platform: multiple
keywords:
- Иадсекстенсион ADSI, использование
- ADSI ADSI, пример кода C/C++, использование Иадсекстенсион
- расширения ADSI, Иадсекстенсион
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ae7d59048d29620cdc2d3703b9ba26a852441a47
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/19/2021
ms.locfileid: "112405947"
---
# <a name="iadsextension-interface"></a>Интерфейс Иадсекстенсион

Интерфейс [**иадсекстенсион**](/windows/desktop/api/Iads/nn-iads-iadsextension) определяется следующим образом:


```C++
IADsExtension : public IUnknown
    {
    public:
        virtual HRESULT STDMETHODCALLTYPE Operate( 
            /* [in] */ DWORD dwCode,
            /* [in] */ VARIANT varData1,
            /* [in] */ VARIANT varData2,
            /* [in] */ VARIANT varData3) = 0;
 
        virtual HRESULT STDMETHODCALLTYPE PrivateGetIDsOfNames( 
            /* [in] */ REFIID riid,
            /* [in] */ OLECHAR **rgszNames,
            /* [in] */ unsigned int cNames,
            /* [in] */ LCID lcid,
            /* [out] */ DISPID *rgDispid) = 0;
 
        virtual HRESULT STDMETHODCALLTYPE PrivateInvoke( 
            /* [in] */ DISPID dispidMember,
            /* [in] */ REFIID riid,
            /* [in] */ LCID lcid,
            /* [in] */ WORD wFlags,
            /* [in] */ DISPPARAMS *pdispparams,
            /* [out] */ VARIANT *pvarResult,
            /* [out] */ EXCEPINFO *pexcepinfo,
            /* [out] */ unsigned int *puArgErr) = 0;
    };
```



Агрегатор (ADSI) вызывает метод [**иадсекстенсион:: оперирует**](/windows/desktop/api/Iads/nf-iads-iadsextension-operate) . Расширение должно интерпретировать параметр *двкоде* и каждый параметр *вардата* в соответствии с документацией поставщика.

Агрегатор (ADSI) вызывает метод [**иадсекстенсион::P риватежетидсофнамес**](/windows/desktop/api/Iads/nf-iads-iadsextension-privategetidsofnames) . Он вызывается после того, как ADSI определит расширение для обслуживания диспетчеризации. Расширение может использовать сведения о типе для получения DISPID, то есть с помощью функции [**диспжетидсофнамес**](/previous-versions/windows/desktop/api/oleauto/nf-oleauto-dispgetidsofnames) .

Обычно ADSI вызывает метод [**приватеинвоке**](/windows/desktop/api/Iads/nf-iads-iadsextension-privateinvoke) после вызова функции [**приватежетидсофнамес**](/windows/desktop/api/Iads/nf-iads-iadsextension-privategetidsofnames) . Расширение должно вызывать фактический метод, который он реализует. Кроме того, расширение может использовать сведения о типе и вызывать функцию [**диспинвоке**](/windows/win32/api/oleauto/nf-oleauto-dispinvoke) .

Все параметры имеют то же значение, что и параметры в стандартном методе [**IDispatch:: Invoke**](/windows/win32/api/oaidl/nf-oaidl-idispatch-invoke) .

 

 