---
title: Регистрация COM-объекта страницы свойств в спецификаторе экрана
description: в этом разделе показано, как зарегистрировать библиотеку DLL расширения, содержащую страницу свойств Active Directory с Windowsным реестром и Active Directory.
ms.assetid: e2d6142b-c2fe-4435-b4af-83f7cd45218b
ms.tgt_platform: multiple
keywords:
- Регистрация COM-объекта страницы свойств в спецификаторе экрана Active Directory
- Active Directory COM-объекта страницы свойств, регистрация в спецификаторе экрана
- Описатели экрана Active Directory, регистрация COM-объекта страницы свойств в
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0f6685e406cb1bfdc16f73dd2fddd94a195fe74a
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/26/2021
ms.locfileid: "122881241"
---
# <a name="registering-the-property-page-com-object-in-a-display-specifier"></a>Регистрация COM-объекта страницы свойств в спецификаторе экрана

при использовании COM для создания библиотеки DLL расширения таблицы свойств для служб домен Active Directory необходимо также зарегистрировать расширение с помощью Windows реестра и служб домен Active Directory. регистрация расширения позволяет Active Directory административных оснасток MMC и оболочке Windows для распознавания расширения.

## <a name="registering-in-the-windows-registry"></a>регистрация в реестре Windows

как и все серверы COM, расширение страницы свойств должно быть зарегистрировано в реестре Windows. Расширение регистрируется в следующем разделе.

```
HKEY_CLASSES_ROOT
   CLSID
      <clsid>
```

*&lt; CLSID &gt;* — это строковое представление идентификатора CLSID, созданное функцией [**стрингфромклсид**](/windows/win32/api/combaseapi/nf-combaseapi-stringfromclsid) . В ключе *&lt; &gt; CLSID* имеется ключ **InprocServer32** , который идентифицирует объект как 32-разрядный сервер in-proc. В ключе **InprocServer32** расположение библиотеки DLL указывается в значении по умолчанию, а модель потоков указывается в значении **ThreadingModel** . Все расширения страниц свойств должны использовать модель потоков "апартамента".

## <a name="registering-with-active-directory-domain-services"></a>Регистрация в домен Active Directory Services

Регистрация расширения страницы свойств относится только к одному языку. Если расширение страницы свойств применяется ко всем языкам, оно должно быть зарегистрировано в объекте [**дисплайспеЦифиер**](/windows/desktop/ADSchema/c-displayspecifier) класса объекта во всех вложенных компонентах языкового стандарта в контейнере описатели вывода. Если расширение страницы свойств локализовано для определенного языкового стандарта, зарегистрируйте его в объекте **дисплайспеЦифиер** в этом вложенном элементе locale. Дополнительные сведения о контейнерах и языковых стандартах для описателей вывода см. в разделе [описатели](display-specifiers.md) и [контейнеры дисплайспеЦифиерс](displayspecifiers-container.md).

Существует три атрибута спецификаторов вывода, которые может зарегистрировать расширение страницы свойств. Это [**админпропертипажес**](/windows/desktop/ADSchema/a-adminpropertypages), [**шеллпропертипажес**](/windows/desktop/ADSchema/a-shellpropertypages)и [**админмултиселектпропертипажес**](/windows/desktop/ADSchema/a-adminmultiselectpropertypages).

Атрибут [**админпропертипажес**](/windows/desktop/ADSchema/a-adminpropertypages) определяет страницы административных свойств, отображаемые в Active Directory административных оснастках. Страница свойств отображается, когда пользователь просматривает свойства объектов соответствующего класса в одной из оснасток Active Directory администрирования MMC.

атрибут [**шеллпропертипажес**](/windows/desktop/ADSchema/a-shellpropertypages) определяет страницы свойств конечного пользователя, отображаемые в оболочке Windows. страница свойств отображается, когда пользователь просматривает свойства для объектов соответствующего класса в обозревателе Windows. начиная с операционных систем Windows Server 2003, оболочка Windows больше не отображает объекты из домен Active Directory служб.

[**админмултиселектпропертипажес**](/windows/desktop/ADSchema/a-adminmultiselectpropertypages) доступен только в операционных системах Windows Server 2003. Страница свойств отображается, когда пользователь просматривает свойства более чем одного объекта соответствующего класса в одной из оснасток Active Directory администрирования MMC.

Все эти атрибуты являются многозначными.

Значения для атрибутов [**админпропертипажес**](/windows/desktop/ADSchema/a-adminpropertypages) и [**шеллпропертипажес**](/windows/desktop/ADSchema/a-shellpropertypages) должны иметь следующий формат.


```C++
<order number>,<clsid>,<optional data>
```



Значения для атрибута [**админмултиселектпропертипажес**](/windows/desktop/ADSchema/a-adminmultiselectpropertypages) должны иметь следующий формат.


```C++
<order number>,<clsid>
```



&lt;Порядковый номер &gt; — это число без знака, представляющее расположение страницы на листе. При отображении страницы свойств значения сортируются с помощью сравнения "номер заказа" каждого значения &lt; &gt; . Если несколько значений имеют одинаковый &lt; порядковый номер, то &gt; эти COM-объекты страницы свойств загружаются в том порядке, в котором они считываются с Active Directory сервера. По возможности следует использовать несуществующий " &lt; номер заказа &gt; ", то есть один, который не используется другими значениями в свойстве. Нет предписанной начальной должности, и в &lt; последовательности "номер заказа" могут пропуски &gt; .

" &lt; CLSID &gt; " — это строковое представление идентификатора CLSID, созданное функцией [**стрингфромклсид**](/windows/win32/api/combaseapi/nf-combaseapi-stringfromclsid) .

" &lt; Необязательные данные &gt; " — это строковое значение, которое не является обязательным. Это значение может быть извлечено COM-объектом страницы свойств с помощью указателя [**IDataObject**](/windows/win32/api/objidl/nn-objidl-idataobject) , переданного в метод [**Ишеллекстинит:: Initialize**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishellextinit-initialize) . COM-объект страницы свойств получает эти данные путем вызова интерфейса [**IDataObject:: GetData**](/windows/win32/api/objidl/nf-objidl-idataobject-getdata) с форматом буфера обмена [**кфстр \_ дспропертипажеинфо**](cfstr-dspropertypageinfo.md) . Это обеспечивает **хглобал** , который содержит структуру [**Дспропертипажеинфо**](/windows/desktop/api/Dsclient/ns-dsclient-dspropertypageinfo) , структура **дспропертипажеинфо** содержит строку в Юникоде, содержащую " &lt; необязательные данные &gt; ". &lt;Использование необязательных данных &gt; с атрибутом [**админмултиселектпропертипажес**](/windows/desktop/ADSchema/a-adminmultiselectpropertypages) не допускается. В следующем примере кода C/C++ показано, как получить " &lt; необязательные данные &gt; ".


```C++
fe.cfFormat = RegisterClipboardFormat(CFSTR_DSPROPERTYPAGEINFO);
fe.ptd = NULL;
fe.dwAspect = DVASPECT_CONTENT;
fe.lindex = -1;
fe.tymed = TYMED_HGLOBAL;
hr = pDataObj->GetData(&fe, &stm);
if(SUCCEEDED(hr))
{
    DSPROPERTYPAGEINFO *pPageInfo;
    
    pPageInfo = (DSPROPERTYPAGEINFO*)GlobalLock(stm.hGlobal);
    if(pPageInfo)
    {
        LPWSTR  pwszData;

        pwszData = (LPWSTR)((LPBYTE)pPageInfo + pPageInfo->offsetString);
        pwszData = NULL;
        
        GlobalUnlock(stm.hGlobal);
    }

    ReleaseStgMedium(&stm);
}
```



Расширение страницы свойств может реализовывать несколько страниц свойств. одним из возможных способов использования " &lt; необязательных данных &gt; " является имя отображаемых страниц. Это обеспечивает гибкость при выборе реализации нескольких COM-объектов, по одному для каждой страницы или на один COM-объект для работы с несколькими страницами.

В следующем примере кода приведен пример значения, которое можно использовать для атрибутов [**админпропертипажес**](/windows/desktop/ADSchema/a-adminpropertypages), [**шеллпропертипажес**](/windows/desktop/ADSchema/a-shellpropertypages)или [**админмултиселектпропертипажес**](/windows/desktop/ADSchema/a-adminmultiselectpropertypages) .


```C++
1,{6dfe6485-a212-11d0-bcd5-00c04fd8d5b6}
```



> [!IMPORTANT]
> для оболочки Windows данные описателя вывода извлекаются при входе пользователя и кэшируются для сеанса пользователя. Для административных оснасток данные описателя просмотра извлекаются при загрузке оснастки и кэшируются на время существования процесса. для оболочки Windows это означает, что изменения описателей вывода вступают в силу после выхода пользователя из системы и последующего входа в систему. Для административных оснасток изменения вступают в силу при загрузке оснастки или файла консоли.

 

## <a name="adding-a-value-to-the-property-sheet-extension-attributes"></a>Добавление значения в атрибуты расширения на странице свойств

Следующая процедура описывает, как зарегистрировать расширение таблицы свойств в одном из атрибутов расширения на странице свойств.

**Регистрация расширения таблицы свойств в одном из атрибутов расширения на странице свойств**

1.  Убедитесь, что расширение еще не существует в значениях атрибута.
2.  Добавьте новое значение в конец списка упорядочения страниц свойств. Задается часть " &lt; номер заказа &gt; " в значении атрибута для следующего значения после самого высокого номера заказа.
3.  Метод [**iAds::P утекс**](/windows/desktop/api/iads/nf-iads-iads-putex) используется для добавления нового значения к атрибуту. Параметр *лнконтролкоде* должен быть установлен в **объявление \_ Свойства ADS \_ ,** чтобы новое значение добавлялось к существующим значениям и не перезаписывать существующие значения. Метод [**iAds:: сетинфо**](/windows/desktop/api/iads/nf-iads-iads-setinfo) должен вызываться впоследствии для фиксации изменений в каталоге.

Имейте в виду, что одно и то же расширение вкладки свойств можно зарегистрировать для нескольких классов объектов.

Метод [**iAds::P утекс**](/windows/desktop/api/iads/nf-iads-iads-putex) используется для добавления нового значения к атрибуту. Параметр *лнконтролкоде* должен быть установлен в значение **\_ \_ append свойства**, чтобы новое значение применялись к существующим значениям и не было, таким образом, перезаписать существующие значения. Метод [**iAds:: сетинфо**](/windows/desktop/api/iads/nf-iads-iads-setinfo) должен быть вызван после фиксации изменения в каталоге.

В следующем примере кода расширение страницы свойств добавляется в класс Group в языковой стандарт компьютера по умолчанию. Имейте в виду, что функция **аддпропертипажетодисплайспеЦифиер** проверяет CLSID расширения страницы свойств в существующих значениях, получает наибольший порядковый номер и добавляет значение для страницы свойств с помощью метода [**iAds::P утекс**](/windows/desktop/api/iads/nf-iads-iads-putex) с **\_ \_ добавлением в свойство ADS** кода элемента управления.


```C++
//  Add msvcrt.dll to the project.
//  Add activeds.lib to the project.
//  Add adsiid.lib to the project.

#include "stdafx.h"
#include <wchar.h>
#include <objbase.h>
#include <activeds.h>
#include "atlbase.h"

HRESULT AddPropertyPageToDisplaySpecifier(LPOLESTR szClassName, //  ldapDisplayName of the class.
                                          CLSID *pPropPageCLSID //  CLSID of property page COM object.
                                         );

HRESULT BindToDisplaySpecifiersContainerByLocale(LCID *locale,
                                                 IADsContainer **ppDispSpecCont
                                                 );

HRESULT GetDisplaySpecifier(IADsContainer *pContainer, LPOLESTR szDispSpec, IADs **ppObject);

//  Entry point for the application.
void wmain(int argc, wchar_t *argv[ ])
{

    wprintf(L"This program adds a sample property page to the display specifier for group class in the local computer's default locale.\n");

    // Initialize COM.
    CoInitialize(NULL);
    HRESULT hr = S_OK;

    //  Class ID for the sample property page.
    LPOLESTR szCLSID = L"{D9FCE809-8A10-11d2-A7E7-00C04F79DC0F}";
    LPOLESTR szClass = L"group";
    CLSID clsid;
    //  Convert to GUID.
    hr = CLSIDFromString(
        szCLSID,  //  Pointer to the string representation of the CLSID.
        &clsid    //  Pointer to the CLSID.
        );

    hr = AddPropertyPageToDisplaySpecifier(szClass, //  ldapDisplayName of the class.
                                           &clsid //  CLSID of property page COM object.
                                          );
    if (S_OK == hr)
        wprintf(L"Property page registered successfully\n");
    else if (S_FALSE == hr)
        wprintf(L"Property page was not added because it was already registered.\n");
    else
        wprintf(L"Property page was not added. HR: %x.\n");

    //  Uninitialize COM.
    CoUninitialize();
    return;
}

//  Adds a property page to Active Directory admin snap-ins.
HRESULT AddPropertyPageToDisplaySpecifier(LPOLESTR szClassName, //  ldapDisplayName of class.
                                          CLSID *pPropPageCLSID //  CLSID of property page COM object.
                                         )
{
    HRESULT hr = E_FAIL;
    IADsContainer *pContainer = NULL;
    LPOLESTR szDispSpec = new OLECHAR[MAX_PATH];
    IADs *pObject = NULL;
    VARIANT var;
    CComBSTR sbstrProperty = L"adminPropertyPages";
    LCID locale = NULL;
    //  Get the display specifier container using default system locale.
    //  When adding a property page COM object, specify the locale
    //  because the registration is locale-specific.
    //  This means if you created a property page
    //  for German, explicitly add it to the 407 container,
    //  so that it will be used when a computer is running with locale
    //  set to German and not the locale set on the
    //  computer where this application is running.
    hr = BindToDisplaySpecifiersContainerByLocale(&locale,
                                                  &pContainer
                                                 );
    //  Handle fail case where dispspec object
    //  is not found and give option to create one.

    if (SUCCEEDED(hr))
    {
        //  Bind to display specifier object for the specified class.
        //  Build the display specifier name.
#ifdef _MBCS
        wcscpy_s(szDispSpec, szClassName);
        wcscat_s(szDispSpec, L"-Display");
        hr = GetDisplaySpecifier(pContainer, szDispSpec, &pObject);
#endif _MBCS#endif _MBCS
        if (SUCCEEDED(hr))
        {
            //  Convert GUID to string.
            LPOLESTR szDSGUID = new WCHAR [39];
            ::StringFromGUID2(*pPropPageCLSID, szDSGUID, 39); 

            //  Get the adminPropertyPages property.
            hr = pObject->GetEx(sbstrProperty, &var);
            if (SUCCEEDED(hr))
            {
                LONG lstart, lend;
                SAFEARRAY *sa = V_ARRAY(&var);
                VARIANT varItem;
                //  Get the lower and upper bound.
                hr = SafeArrayGetLBound(sa, 1, &lstart);
                if (SUCCEEDED(hr))
                {
                    hr = SafeArrayGetUBound(sa, 1, &lend);
                }
                if (SUCCEEDED(hr))
                {
                    //  Iterate the values to verify if the prop page CLSID
                    //  is already registered.
                    VariantInit(&varItem);
                    BOOL bExists = FALSE;
                    UINT uiLastItem = 0;
                    UINT uiTemp = 0;
                    INT iOffset = 0;
                    LPOLESTR szMainStr = new OLECHAR[MAX_PATH];
                    LPOLESTR szItem = new OLECHAR[MAX_PATH];
                    LPOLESTR szStr = NULL;
                    for (long idx=lstart; idx <= lend; idx++)
                    {
                        hr = SafeArrayGetElement(sa, &idx, &varItem);
                        if (SUCCEEDED(hr))
                        {
#ifdef _MBCS
                            //  Verify that the specified CLSID is already registered.
                            wcscpy_s(szMainStr,varItem.bstrVal);
                            if (wcsstr(szMainStr,szDSGUID))
                                bExists = TRUE;
                            //  Get the index which is the number before the first comma.
                            szStr = wcschr(szMainStr, ',');
                            iOffset = (int)(szStr - szMainStr);
                            wcsncpy_s(szItem, szMainStr, iOffset);
                            szItem[iOffset]=0L;
                            uiTemp = _wtoi(szItem);
                            if (uiTemp > uiLastItem)
                                uiLastItem = uiTemp;
                            VariantClear(&varItem);
#endif _MBCS
                        }
                    }
                    //  If the CLSID is not registered, add it.
                    if (!bExists)
                    {
                        //  Build the value to add.
                        LPOLESTR szValue = new OLECHAR[MAX_PATH];
                        //  Next index to add at end of list.
#ifdef _MBCS
                        uiLastItem++;
                        _itow_s(uiLastItem, szValue, 10);   
                        wcscat_s(szValue,L",");
                        //  Add the class ID for the property page.
                        wcscat_s(szValue,szDSGUID);
                        wprintf(L"Value to add: %s\n", szValue);
#endif _MBCS

                        VARIANT varAdd;
                        //  Only one value to add
                        LPOLESTR pszAddStr[1];
                        pszAddStr[0]=szValue;
                        ADsBuildVarArrayStr(pszAddStr, 1, &varAdd);

                        hr = pObject->PutEx(ADS_PROPERTY_APPEND, sbstrProperty, varAdd);
                        if (SUCCEEDED(hr))
                        {
                            //  Commit the change.
                            hr = pObject->SetInfo();
                        }
                    }
                    else
                        hr = S_FALSE;
                }
            }
            VariantClear(&var);
        }
        if (pObject)
            pObject->Release();
    }

    return hr;
}

//  This function returns a pointer to the display specifier container 
//  for the specified locale.
//  If locale is NULL, use the default system locale and then return the locale in the locale param.
HRESULT BindToDisplaySpecifiersContainerByLocale(LCID *locale,
                                                 IADsContainer **ppDispSpecCont
                                                )
{
    HRESULT hr = E_FAIL;

    if ((!ppDispSpecCont)||(!locale))
        return E_POINTER;

    //  If no locale is specified, use the default system locale.
    if (!(*locale))
    {
        *locale = GetSystemDefaultLCID();
        if (!(*locale))
            return E_FAIL;
    }

    //  Verify that it is a valid locale.
    if (!IsValidLocale(*locale, LCID_SUPPORTED))
        return E_INVALIDARG;

    LPOLESTR szPath = new OLECHAR[MAX_PATH*2];
    IADs *pObj = NULL;
    VARIANT var;

    hr = ADsOpenObject(L"LDAP://rootDSE",
                       NULL,
                       NULL,
                       ADS_SECURE_AUTHENTICATION, // Use Secure Authentication.
                       IID_IADs,
                       (void**)&pObj);

    if (SUCCEEDED(hr))
    {
        //  Get the DN to the config container.
        hr = pObj->Get(CComBSTR("configurationNamingContext"), &var);
        if (SUCCEEDED(hr))
        {
#ifdef _MBCS
            //  Build the string to bind to the DisplaySpecifiers container.
            swprintf_s(szPath,L"LDAP://cn=%x,cn=DisplaySpecifiers,%s", *locale, var.bstrVal);
            //  Bind to the DisplaySpecifiers container.
            *ppDispSpecCont = NULL;
            hr = ADsOpenObject(szPath,
                               NULL,
                               NULL,
                               ADS_SECURE_AUTHENTICATION, // Use Secure Authentication.
                               IID_IADsContainer,
                               (void**)ppDispSpecCont);
#endif _MBCS

            if(FAILED(hr))
            {
                if (*ppDispSpecCont)
                {
                    (*ppDispSpecCont)->Release();
                    (*ppDispSpecCont) = NULL;
                }
            }
        }
    }
    //   Cleanup.
    VariantClear(&var);
    if (pObj)
        pObj->Release();

    return hr;
}

HRESULT GetDisplaySpecifier(IADsContainer *pContainer, LPOLESTR szDispSpec, IADs **ppObject)
{
    HRESULT hr = E_FAIL;
    CComBSTR sbstrDSPath;
    IDispatch *pDisp = NULL;

    if (!pContainer)
    {
        hr = E_POINTER;
        return hr;
    }

    //  Verify other pointers.
    //  Initialize the output pointer.
    (*ppObject) = NULL;

    //  Build relative path to the display specifier object.
    sbstrDSPath = "CN=";
    sbstrDSPath += szDispSpec;

    //  Use child object binding with IADsContainer::GetObject.
    hr = pContainer->GetObject(CComBSTR("displaySpecifier"),
        sbstrDSPath,
        &pDisp);
    if (SUCCEEDED(hr))
    {
        hr = pDisp->QueryInterface(IID_IADs, (void**)ppObject);
        if (FAILED(hr))
        {
            //  Clean up.
            if (*ppObject)
                (*ppObject)->Release();
        }
    }

    if (pDisp)
        pDisp->Release();

    return hr;

}
```



 

 
