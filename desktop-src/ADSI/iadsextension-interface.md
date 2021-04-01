---
title: Интерфейс Иадсекстенсион
description: В этом разделе содержатся примеры кода C++ для использования интерфейса Иадсекстенсион.
ms.assetid: fa94cc55-1ab2-4b6e-a3b6-8c20542adb42
ms.tgt_platform: multiple
keywords:
- Иадсекстенсион ADSI, использование
- ADSI ADSI, пример кода C/C++, использование Иадсекстенсион
- расширения ADSI, Иадсекстенсион
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a6c950b6d305cc4c90ed75ff0cc96b5f7f344e12
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/21/2020
ms.locfileid: "103793819"
---
# <a name="iadsextension-interface"></a><span data-ttu-id="86db5-106">Интерфейс Иадсекстенсион</span><span class="sxs-lookup"><span data-stu-id="86db5-106">IADsExtension Interface</span></span>

<span data-ttu-id="86db5-107">Интерфейс [**иадсекстенсион**](/windows/desktop/api/Iads/nn-iads-iadsextension) определяется следующим образом:</span><span class="sxs-lookup"><span data-stu-id="86db5-107">The [**IADsExtension**](/windows/desktop/api/Iads/nn-iads-iadsextension) interface is defined as follows:</span></span>


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



<span data-ttu-id="86db5-108">Агрегатор (ADSI) вызывает метод [**иадсекстенсион:: оперирует**](/windows/desktop/api/Iads/nf-iads-iadsextension-operate) .</span><span class="sxs-lookup"><span data-stu-id="86db5-108">The aggregator (ADSI) calls the [**IADsExtension::Operate**](/windows/desktop/api/Iads/nf-iads-iadsextension-operate) method.</span></span> <span data-ttu-id="86db5-109">Расширение должно интерпретировать параметр *двкоде* и каждый параметр *вардата* в соответствии с документацией поставщика.</span><span class="sxs-lookup"><span data-stu-id="86db5-109">The extension should interpret the *dwCode* parameter and each *varData* parameter, according to the provider's documentation.</span></span>

<span data-ttu-id="86db5-110">Агрегатор (ADSI) вызывает метод [**иадсекстенсион::P риватежетидсофнамес**](/windows/desktop/api/Iads/nf-iads-iadsextension-privategetidsofnames) .</span><span class="sxs-lookup"><span data-stu-id="86db5-110">The aggregator (ADSI), calls the [**IADsExtension::PrivateGetIDsOfNames**](/windows/desktop/api/Iads/nf-iads-iadsextension-privategetidsofnames) method.</span></span> <span data-ttu-id="86db5-111">Он вызывается после того, как ADSI определит расширение для обслуживания диспетчеризации.</span><span class="sxs-lookup"><span data-stu-id="86db5-111">It is called after ADSI determines the extension to service the dispatch.</span></span> <span data-ttu-id="86db5-112">Расширение может использовать сведения о типе для получения DISPID, то есть с помощью функции [**диспжетидсофнамес**](/previous-versions/windows/desktop/api/oleauto/nf-oleauto-dispgetidsofnames) .</span><span class="sxs-lookup"><span data-stu-id="86db5-112">The extension could use the type information for getting the DISPID, that is, using the [**DispGetIDsOfNames**](/previous-versions/windows/desktop/api/oleauto/nf-oleauto-dispgetidsofnames) function.</span></span>

<span data-ttu-id="86db5-113">Обычно ADSI вызывает метод [**приватеинвоке**](/windows/desktop/api/Iads/nf-iads-iadsextension-privateinvoke) после вызова функции [**приватежетидсофнамес**](/windows/desktop/api/Iads/nf-iads-iadsextension-privategetidsofnames) .</span><span class="sxs-lookup"><span data-stu-id="86db5-113">ADSI normally calls the [**PrivateInvoke**](/windows/desktop/api/Iads/nf-iads-iadsextension-privateinvoke) method after calling the [**PrivateGetIDsOfNames**](/windows/desktop/api/Iads/nf-iads-iadsextension-privategetidsofnames) function.</span></span> <span data-ttu-id="86db5-114">Расширение должно вызывать фактический метод, который он реализует.</span><span class="sxs-lookup"><span data-stu-id="86db5-114">The extension should call the actual method that it implements.</span></span> <span data-ttu-id="86db5-115">Кроме того, расширение может использовать сведения о типе и вызывать функцию [**диспинвоке**](/windows/win32/api/oleauto/nf-oleauto-dispinvoke) .</span><span class="sxs-lookup"><span data-stu-id="86db5-115">Alternatively, the extension can use type information and call the [**DispInvoke**](/windows/win32/api/oleauto/nf-oleauto-dispinvoke) function.</span></span>

<span data-ttu-id="86db5-116">Все параметры имеют то же значение, что и параметры в стандартном методе [**IDispatch:: Invoke**](/windows/win32/api/oaidl/nf-oaidl-idispatch-invoke) .</span><span class="sxs-lookup"><span data-stu-id="86db5-116">All parameters have the same meaning as the parameters in the standard [**IDispatch::Invoke**](/windows/win32/api/oaidl/nf-oaidl-idispatch-invoke) method.</span></span>

 

 