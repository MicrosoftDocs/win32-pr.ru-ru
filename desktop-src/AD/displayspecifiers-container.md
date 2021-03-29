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
# <a name="displayspecifiers-container"></a>Контейнер ДисплайспеЦифиерс

Описатели вывода хранятся в контейнере ДисплайспеЦифиерс контейнера конфигурации по языку. Так как контейнер конфигурации реплицируется во всем лесу, описатели вывода распространяются во всех доменах леса.

Контейнер конфигурации хранит контейнер ДисплайспеЦифиерс, в котором хранятся контейнеры, соответствующие каждому языку. Эти контейнеры языковых стандартов именуются с помощью шестнадцатеричного представления идентификатора локали. Например, контейнер языкового стандарта US/English называется 409, в качестве контейнера языкового стандарта немецкого языка — 407, а в контейнере японского языкового стандарта — имя 411. Дополнительные сведения и список возможных идентификаторов языков см. в разделе [константы и строки идентификатора языка](/windows/desktop/Intl/language-identifier-constants-and-strings).

Каждый контейнер языкового стандарта хранит объекты класса [**дисплайспеЦифиер**](/windows/desktop/ADSchema/c-displayspecifier) .

Чтобы перечислить все описатели вывода для языкового стандарта, перечислите все объекты [**дисплайспеЦифиер**](/windows/desktop/ADSchema/c-displayspecifier) в указанном контейнере языкового стандарта в контейнере дисплайспеЦифиерс.

В следующем примере кода содержится функция, которая выполняет привязку к контейнеру спецификатора вывода для указанного языкового стандарта:


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



 

 