---
title: Контейнер ДисплайспеЦифиерс
description: Описатели вывода хранятся в контейнере ДисплайспеЦифиерс контейнера конфигурации по языку. Так как контейнер конфигурации реплицируется во всем лесу, описатели вывода распространяются во всех доменах леса.
ms.assetid: d7647c50-f95c-41ef-8d67-dc72542cae5a
ms.tgt_platform: multiple
keywords:
- Контейнер ДисплайспеЦифиерс
- Контейнер, описатели экрана
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 406258a6c9983581491420a49621e3d10df4601e
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/17/2020
ms.locfileid: "104487456"
---
# <a name="displayspecifiers-container"></a><span data-ttu-id="5c438-106">Контейнер ДисплайспеЦифиерс</span><span class="sxs-lookup"><span data-stu-id="5c438-106">DisplaySpecifiers Container</span></span>

<span data-ttu-id="5c438-107">Описатели вывода хранятся в контейнере ДисплайспеЦифиерс контейнера конфигурации по языку.</span><span class="sxs-lookup"><span data-stu-id="5c438-107">Display specifiers are stored, by locale, in the DisplaySpecifiers container of the Configuration container.</span></span> <span data-ttu-id="5c438-108">Так как контейнер конфигурации реплицируется во всем лесу, описатели вывода распространяются во всех доменах леса.</span><span class="sxs-lookup"><span data-stu-id="5c438-108">Because the Configuration container is replicated across the entire forest, display specifiers are propagated across all domains in a forest.</span></span>

<span data-ttu-id="5c438-109">Контейнер конфигурации хранит контейнер ДисплайспеЦифиерс, в котором хранятся контейнеры, соответствующие каждому языку.</span><span class="sxs-lookup"><span data-stu-id="5c438-109">The Configuration container stores the DisplaySpecifiers container, which then stores containers that correspond to each locale.</span></span> <span data-ttu-id="5c438-110">Эти контейнеры языковых стандартов именуются с помощью шестнадцатеричного представления идентификатора локали.</span><span class="sxs-lookup"><span data-stu-id="5c438-110">These locale containers are named using the hexadecimal representation of the locale identifier.</span></span> <span data-ttu-id="5c438-111">Например, контейнер языкового стандарта US/English называется 409, в качестве контейнера языкового стандарта немецкого языка — 407, а в контейнере японского языкового стандарта — имя 411.</span><span class="sxs-lookup"><span data-stu-id="5c438-111">For example, the US/English locale container is named 409, the German locale's container is named 407, and the Japanese locale's container is named 411.</span></span> <span data-ttu-id="5c438-112">Дополнительные сведения и список возможных идентификаторов языков см. в разделе [константы и строки идентификатора языка](/windows/desktop/Intl/language-identifier-constants-and-strings).</span><span class="sxs-lookup"><span data-stu-id="5c438-112">For more information, and a list of possible language identifiers, see [Language Identifier Constants and Strings](/windows/desktop/Intl/language-identifier-constants-and-strings).</span></span>

<span data-ttu-id="5c438-113">Каждый контейнер языкового стандарта хранит объекты класса [**дисплайспеЦифиер**](/windows/desktop/ADSchema/c-displayspecifier) .</span><span class="sxs-lookup"><span data-stu-id="5c438-113">Each locale container stores objects of the [**displaySpecifier**](/windows/desktop/ADSchema/c-displayspecifier) class.</span></span>

<span data-ttu-id="5c438-114">Чтобы перечислить все описатели вывода для языкового стандарта, перечислите все объекты [**дисплайспеЦифиер**](/windows/desktop/ADSchema/c-displayspecifier) в указанном контейнере языкового стандарта в контейнере дисплайспеЦифиерс.</span><span class="sxs-lookup"><span data-stu-id="5c438-114">To list all display specifiers for a locale, enumerate all the [**displaySpecifier**](/windows/desktop/ADSchema/c-displayspecifier) objects in the specified locale container within the DisplaySpecifiers container.</span></span>

<span data-ttu-id="5c438-115">В следующем примере кода содержится функция, которая выполняет привязку к контейнеру спецификатора вывода для указанного языкового стандарта:</span><span class="sxs-lookup"><span data-stu-id="5c438-115">The following code example contains a function that binds to the display specifier container for the specified locale:</span></span>


```C++
/**********
This function returns a pointer to the display specifier container 
for the specified locale.

If locale is NULL, use default system locale and then return the 
locale in the locale parameter.
***********/
HRESULT BindToDisplaySpecifiersContainerByLocale(
    LCID *locale,
    IADs **ppDispSpecCont)
{
HRESULT hr = E_FAIL;
 
if ((!ppDispSpecCont)||(!locale))
    return E_POINTER;
 
// If no locale is specified, use the default system locale.
if (!(*locale))
{
    *locale = GetSystemDefaultLCID();
    if (!(*locale))
        return E_FAIL;
}
 
// Be sure that the locale is valid.
if (!IsValidLocale(*locale, LCID_SUPPORTED))
    return E_INVALIDARG;
 
LPOLESTR szPath = new OLECHAR[MAX_PATH*2];
IADs *pObj = NULL;
VARIANT var;
 
hr = ADsOpenObject(L"LDAP://rootDSE",
                     NULL,
                     NULL,
                     ADS_SECURE_AUTHENTICATION,
                     IID_IADs,
                     (void**)&pObj);
 
if (SUCCEEDED(hr))
{
    // Get the DN to the configuration container.
    hr = pObj->Get(CComBSTR("configurationNamingContext"), &var);
    if (SUCCEEDED(hr))
    {
        // Build the string to bind to the container for the
        // specified locale in the DisplaySpecifiers container.
        swprintf_s(
            szPath, 
            L"LDAP://cn=%x,cn=DisplaySpecifiers,%s", 
            *locale, 
            var.bstrVal);

        // Bind to the container.
        *ppDispSpecCont = NULL;
        hr = ADsOpenObject(szPath,
                     NULL,
                     NULL,
                     ADS_SECURE_AUTHENTICATION,
                     IID_IADs,
                     (void**)ppDispSpecCont);
 
        if(FAILED(hr))
        {
            if ((*ppDispSpecCont))
            {
                (*ppDispSpecCont)->Release();
                (*ppDispSpecCont) = NULL;
            }
        }
    }
}
 
// Cleanup.
VariantClear(&var);
if (pObj)
    pObj->Release();
 
return hr;
}
```



 

 