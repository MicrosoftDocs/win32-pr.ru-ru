---
description: Создает XML-представления объектов.
ms.assetid: 06d2b532-7ab2-489d-9021-27b5187c8f2b
ms.tgt_platform: multiple
title: Представление объектов в XML
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9698c54eeff61517a1389ceea14bc2415727f085
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105702000"
---
# <a name="representing-objects-in-xml"></a>Представление объектов в XML

Компонент кодировщика XML в инструментарии WMI создает XML-представления объектов.

В C++ можно запустить кодировщик XML с помощью вызова метода [**ивбемобжекттекстсрк. gettext**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjecttextsrc-gettext) , указав объект, который должен быть представлен в формате XML, и текстовый формат для использования в представлении. Дополнительные сведения и пример кода см. в разделе кодирование объекта в XML с помощью C/C++.

В VBScript или Visual Basic для кодирования данных для экземпляра XML вызовите [**свбемобжектекс. gettext**](swbemobjectex-gettext-.md). Дополнительные сведения и пример кода см. в разделе кодирование объекта в XML с помощью VBScript.

В этом разделе обсуждаются следующие разделы:

-   [Кодирование объекта с помощью C или C++](#encode-an-object-using-c-or-c)
-   [Кодирование объекта с помощью VBScript](#encode-an-object-using-vbscript)
-   [См. также](#related-topics)

## <a name="encode-an-object-using-c-or-c"></a>Кодирование объекта с помощью C или C++

<span id="to_encode_an_object_in_xml_using_c_c_"></span><span id="TO_ENCODE_AN_OBJECT_IN_XML_USING_C_C_"></span>

Следующая процедура описывает, как кодировать объект в XML с помощью C или C++.

**Кодирование объекта в XML с помощью C или C++**

1.  Настройте программу для доступа к данным WMI.

    Поскольку Инструментарий WMI основан на технологии COM, для доступа к инструментарию WMI необходимо выполнить требуемые вызовы функций [**CoInitializeEx**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex) и [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity) . Дополнительные сведения см. в разделе [Инициализация COM для приложения WMI](initializing-com-for-a-wmi-application.md).

2.  При необходимости создайте объект [**ивбемконтекст**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemcontext) и инициализируйте его.

    Не нужно создавать объект [**ивбемконтекст**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemcontext) , если не требуется изменить операцию по умолчанию. Объект контекста используется кодировщиком XML для управления объемом информации, включаемой в XML-представление объекта.

    В следующей таблице перечислены необязательные значения, которые можно указать для объекта контекста.

    

    <table>
    <thead>
    <tr class="header">
    <th>Значение или тип</th>
    <th>Значение</th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td>&quot;LocalOnly &quot; <strong>VT_BOOL</strong></td>
    <td>Если <strong>значение равно true</strong>, в результирующем XML-коде содержатся только свойства и методы, определенные локально в классе. Значение по умолчанию — <strong>false</strong>.</td>
    </tr>
    <tr class="even">
    <td>&quot;Инклудекуалифиерс &quot; <strong>VT_BOOL</strong></td>
    <td>Если задано <strong>значение true</strong>, то в результирующий XML-документ включаются квалификаторы класса, экземпляра, свойств и методов. Значение по умолчанию — <strong>false</strong>.</td>
    </tr>
    <tr class="odd">
    <td>&quot;Ексклудесистемпропертиес &quot; <strong>VT_BOOL</strong></td>
    <td>Если <strong>значение равно true</strong>, системные свойства WMI отфильтровываются из выходных данных. Значение по умолчанию — <strong>false</strong>.</td>
    </tr>
    <tr class="even">
    <td>&quot;Паслевел &quot; <strong>VT_I4</strong></td>
    <td><dl> 0 = <CLASS> <INSTANCE> создается элемент или.<br />
1 = <VALUE.NAMEDOBJECT> элемент создан.<br />
2 = <VALUE.OBJECTWITHLOCALPATH> создается элемент.<br />
3 = создается <VALUE.OBJECTWITHPATH> .<br />
    </dl> Значение по умолчанию равно нулю (0).<br/></td>
    </tr>
    </tbody>
    </table>

    

     

    В следующем примере кода показано, как объект контекста инициализируется для включения квалификаторов и исключения системных свойств.

    ```C++
    VARIANT vValue;
    IWbemContext *pContext = NULL;
    HRESULT hr = CoCreateInstance (CLSID_WbemContext, 
                           NULL, 
                           CLSCTX_INPROC_SERVER,
                           IID_IWbemContext, 
                           (void**) &pContext);
    if (FAILED(hr))
    {
      printf("Create context failed with %x\n", hr);
      return hr;
    }

    // Generate a <VALUE.OBJECTWITHLOCALPATH> element
    VariantInit(&vValue);
    vValue.vt = VT_I4;
    vValue.lVal = 2;
    pContext->SetValue(L"PathLevel", 0, &vValue);
    VariantClear(&vValue);

    // Include qualifiers
    VariantInit(&vValue);
    vValue.vt = VT_BOOL;
    vValue.boolVal = VARIANT_TRUE;
    pContext->SetValue(L"IncludeQualifiers", 0, &vValue);
    VariantClear(&vValue);

    // Exclude system properties
    VariantInit(&vValue);
    vValue.vt = VT_BOOL;
    vValue.boolVal = VARIANT_TRUE;
    pContext->SetValue(L"ExcludeSystemProperties", 0, &vValue);
    VariantClear(&vValue);
    ```

    

3.  Получите ссылку на класс или экземпляр для кодирования в XML.

    После инициализации COM и подключения к инструментарию WMI вызовите [**GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject) для получения ссылки на указанный класс или экземпляр. Если для указания класса или экземпляра использовалась BSTR, вызовите [**сисфристринг**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) , чтобы освободить память, выделенную [**сисаллокстринг**](/windows/win32/api/oleauto/nf-oleauto-sysallocstring).

    В следующем примере кода извлекается ссылка на экземпляр [**Win32 \_ LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) .

    ```C++
    HRESULT hr = NULL;
    IWbemClassObject *pClass = NULL;
    BSTR strObj = SysAllocString(L"Win32_LogicalDisk");

    hr = pConnection->GetObject(strObj, 
                                0, 
                                NULL, 
                                &pClass, 
                                NULL);

    SysFreeString(strObj);
    if (FAILED(hr))
    {
      printf("GetObject failed with %x\n",hr)
      return hr;
    }
    ```

    

4.  Создайте объект [**ивбемобжекттекстсрк**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemobjecttextsrc) .

    После создания ссылки на объект необходимо создать объект [**ивбемобжекттекстсрк**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemobjecttextsrc) с вызовом [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance). Объект **ивбемобжекттекстсрк** используется для создания фактического текста XML.

    В следующем примере кода показано, как создать объект [**ивбемобжекттекстсрк**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemobjecttextsrc) , вызвав [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance).

    ```C++
    HRESULT hr = NULL;
    IWbemObjectTextSrc *pSrc = NULL;

    hr = CoCreateInstance (CLSID_WbemObjectTextSrc, 
                           NULL,
                           CLSCTX_INPROC_SERVER,
                           IID_IWbemObjectTextSrc, 
                           (void**) &pSrc);

    if (FAILED(hr))
    {
        printf("CoCreateInstance of IWbemObjectTextSrc failed %x\n",hr);
        return hr;
    }
    ```

    

5.  Вызов метода [**ивбемобжекттекстсрк. gettext**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjecttextsrc-gettext) для получения XML-представления объекта.

    После установки контекста для представления объекта, получения ссылки на объект и создания объекта [**ивбемобжекттекстсрк**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemobjecttextsrc) , можно приступать к ФОРМИРОВАНИЮ XML-представления указанного объекта путем вызова метода [**ивбемобжекттекстсрк. gettext**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjecttextsrc-gettext) .

    В следующем примере кода C++ создается XML-представление объекта, на который ссылается *пкласс*. XML-представление возвращается в *стртекст*. Третий параметр в gettext [**указывает формат**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemobjecttextsrc) текста, используемый для XML, и должен быть либо WMI \_ obj \_ Text \_ CIM \_ DTD \_ 2 \_ 0 (0x1), либо \_ текст WMI obj \_ \_ WMI \_ DTD \_ 2 \_ 0 (0x2). Дополнительные сведения об этих значениях см. в разделе значения параметров [**ивбемобжекттекстсрк:: GetText**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjecttextsrc-gettext) .

    ```C++
    HRESULT hr = NULL;
    BSTR strText = NULL;
    hr = pSrc->GetText(0, 
                       pClass, 
                       WMI_OBJ_TEXT_CIM_DTD_2_0,
                       pContext, 
                       &strText);

    // Perform a task with strText
    SysFreeString(strText);

    if (FAILED(hr))
    {
      printf("GetText failed with %x\n", hr);
      return hr;
    }
    ```

    

Следующий пример кода C++ включает все шаги, описанные в предыдущей процедуре, и кодирует класс [**Win32 \_ LOGICALDISK**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) в XML, включая квалификаторы класса, свойства и метода и исключая системные свойства.


```C++
// The following #define statement is needed so that 
// the proper values are loaded by the #include files.
#define _WIN32_WINNT 0x0500

#include <stdio.h>
#include <wbemcli.h>
#pragma comment(lib, "wbemuuid.lib")

// Initialize the context object
// ---------------------------------------------
void FillUpContext(IWbemContext *pContext)
{
  VARIANT vValue;

  // IncludeQualifiers
  VariantInit(&vValue);
  vValue.vt = VT_BOOL;
  vValue.boolVal = VARIANT_FALSE;
  pContext->SetValue(L"IncludeQualifiers", 0, &vValue);
  VariantClear(&vValue);

  VariantInit(&vValue);
  vValue.vt = VT_I4;
  vValue.lVal = 0;
  pContext->SetValue(L"PathLevel", 0, &vValue);
  VariantClear(&vValue);

  // ExcludeSystemProperties
  VariantInit(&vValue);
  vValue.vt = VT_BOOL;
  vValue.boolVal = VARIANT_TRUE;
  pContext->SetValue(L"ExcludeSystemProperties", 0, &vValue);
  VariantClear(&vValue);
}

// Main method ... drives the program
// ---------------------------------------------
int _cdecl main(int argc, char * argv[])
{
  BSTR strNs = NULL;
  BSTR strObj = NULL;
  BSTR strText = NULL;

  if(FAILED(CoInitialize(NULL)))
    return 1;
  HRESULT hr = E_FAIL;
  IWbemObjectTextSrc *pSrc = NULL;

  IWbemLocator *pL = NULL;
  if(SUCCEEDED(hr = CoCreateInstance (CLSID_WbemLocator, 
                                      NULL, 
                                      CLSCTX_INPROC_SERVER,
                                      IID_IWbemLocator, 
                                      (void**) &pL)))
  {
    // Create a context object
    IWbemContext *pContext = NULL;
    if(SUCCEEDED(hr = CoCreateInstance (CLSID_WbemContext, 
                                        NULL, 
                                        CLSCTX_INPROC_SERVER,
                                        IID_IWbemContext, 
                                        (void**) &pContext)))
    {
      FillUpContext(pContext);
      IWbemServices *pConnection = NULL;
      strNs = SysAllocString(L"root\\cimv2");
      strText = NULL;
      if(SUCCEEDED(hr = pL->ConnectServer(strNs, 
                                          NULL, 
                                          NULL, 
                                          NULL, 
                                          0, 
                                          NULL, 
                                          NULL, 
                                          &pConnection)))
      {
        IWbemClassObject *pClass = NULL;
        strObj = SysAllocString(L"Win32_LogicalDisk");

        if(SUCCEEDED(hr = CoCreateInstance (CLSID_WbemObjectTextSrc, 
                                            NULL,
                                            CLSCTX_INPROC_SERVER,
                                            IID_IWbemObjectTextSrc, 
                                            (void**) &pSrc)))
        {
          // Test for GetObject
          if(SUCCEEDED(hr = pConnection->GetObject(strObj, 
                                                   0, 
                                                   NULL, 
                                                   &pClass, 
                                                   NULL)))
          {
            if(SUCCEEDED(hr = pSrc->GetText(0, 
                                            pClass, 
                                            WMI_OBJ_TEXT_CIM_DTD_2_0,
                                            pContext, 
                                            &strText)))
            {
              printf("GETOBJECT SUCCEEDED\n");
              printf("==========================================\n");
              wprintf(strText);
              pContext->Release();
              pClass->Release();
            }
            else
            {
              printf("GetText failed with %x\n", hr);
              // Free up the object
              pContext->Release();
              pClass->Release();
            }
          }
          else
            printf("GetObject failed with %x\n", hr);
        }
        else
          printf("CoCreateInstance on WbemObjectTextSrc failed with %x\n", hr);
      }
      else
        printf("ConnectServer on root\\cimv2 failed with %x\n", hr);
    }
    else
      printf("CoCreateInstance on Context failed with %x\n", hr);
  }
  else
    printf("CoCreateInstance on Locator failed with %x\n", hr);

// Clean up memory
  if (strNs != NULL)
    SysFreeString(strNs);
  if (strObj != NULL)
    SysFreeString(strObj);
  if (strText != NULL)
    SysFreeString(strText);
  if (pSrc != NULL)
    pSrc->Release();
  if (pL != NULL)
    pL->Release();
  return 0;
}
```



## <a name="encode-an-object-using-vbscript"></a>Кодирование объекта с помощью VBScript

<span id="to_encode_an_object_in_xml_using_vbscript"></span><span id="TO_ENCODE_AN_OBJECT_IN_XML_USING_VBSCRIPT"></span>

Следующая процедура описывает, как кодировать объект в XML с помощью VBScript.

**Кодирование объекта в XML с помощью VBScript**

1.  При необходимости создайте объект [**свбемнамедвалуесет**](swbemnamedvalueset.md) и инициализируйте его, чтобы задать значения контекста, необходимые для XML-представления.

    В следующем примере кода показано, как значения, указывающие кодировщику XML, создавать <значение. ОБЖЕКТВИСЛОКАЛПАС>, включая все квалификаторы и исключение системных свойств при формировании XML-представления объекта.

    ```VB
    ' Create an optional SWbemNamedValueSet object
    set context = CreateObject("wbemscripting.SWbemNamedValueSet")

    ' Initialize the value set object to set the context
    ' Generate a <VALUE.OBJECTWITHLOCALPATH> element
    context.add "PathLevel", 2 
    context.add "IncludeQualifiers", true 
    context.add "ExcludeSystemProperties", true '
    ```

    

2.  Получите экземпляр объекта или класса для представления в XML.

    В следующем примере кода извлекается экземпляр объекта.

    ```VB
    ' Retrieve the object/class to be represented in XML
    set myObj = GetObject("winmgmts:\\.\root\cimv2:win32_LogicalDisk")
    ```

    

3.  Вызовите метод [**gettext \_**](swbemobjectex-gettext-.md) экземпляра, созданного на предыдущем шаге, используя значение 1 в качестве параметра, чтобы указать текстовый формат, соответствующий CIM DTD версии 2,0, или 2, чтобы указать текстовый формат, соответствующий WMI DTD версии 2,0. Если вы создали объект [**свбемнамедвалуесет**](swbemnamedvalueset.md) на шаге 1, включите его в список параметров в качестве третьего параметра.

    В следующем примере кода показано, как вызвать метод [**gettext \_**](swbemobjectex-gettext-.md) экземпляра.

    ```VB
    ' Get the XML representation of the object
    strText = myObj.GetText_(2,,context)

    ' If you have not used a SWbemNamedValueSet object
    ' enter the following line.
    strText = myObj.GetText_(2)
    ```

    

4.  При необходимости убедитесь, что XML-код, созданный на шаге 3, правильно сформирован, путем создания и инициализации объекта модель DOM XML (DOM) и последующей загрузки XML-текста в него.

    В следующем примере кода показано, как создать и инициализировать объект DOM XML и загрузить в него XML-текст.

    ```VB
    ' Create an XMLDOM object
    set xml = CreateObject("Microsoft.xmldom")

    ' Initialize the XMLDOM object so results are returned synchronously
    xml.async = false

    ' Load the XML into the XMLDOM object
    xml.loadxml strText
    ```

    

5.  Вывод XML-представления объекта.

    В следующем примере кода показано, как использовать Wscript для вывода XML.

    ```VB
    wscript.echo strText
    ```

    

    Если вы решили использовать XML DOM для проверки правильности сформированного XML, замените предыдущую строку следующим.

    ```VB
    wscript.echo xml.xml
    ```

    

Следующий пример кода VBScript включает все шаги, описанные в предыдущей процедуре, и кодирует класс [**Win32 \_ LOGICALDISK**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) в XML, включая квалификаторы класса, свойства и метода, а также свойства системы.


```VB
' Create optional SWbemNamedValueSet object
set context = CreateObject("Wbemscripting.SWbemNamedValueSet")

' Initialize the context object
context.add "PathLevel", 2
context.add "IncludeQualifiers", true
context.add "ExcludeSystemProperties", true

' Retrieve the object/class to be represented in XML
set myObj = GetObject("winmgmts:\\.\root\cimv2:Win32_LogicalDisk")

' Get the XML representation of the object
strText = myObj.GetText_(2,,context)
' If you have not used a SWbemNamedValueSet object 
'   use the following line
'   strText = myObj.GetText(2)

' Print the XML representation
wscript.echo strText

' If you choose to use the XML DOM to verify 
'   that the XML generated is well-formed, replace the last
'   line in the above code example with the following lines:

' Create an XMLDOM object
set xml = CreateObject("Microsoft.xmldom")

' Initialize the XMLDOM object so results are 
'   returned synchronously
xml.async = false

' Load the XML into the XMLDOM object
xml.loadxml strText

' Print the XML representation
wscript.echo xml.xml
```



## <a name="related-topics"></a>См. также

<dl> <dt>

[Использование инструментария WMI](using-wmi.md)
</dt> </dl>

 

