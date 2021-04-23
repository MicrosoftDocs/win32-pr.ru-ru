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
# <a name="representing-objects-in-xml"></a><span data-ttu-id="fe535-103">Представление объектов в XML</span><span class="sxs-lookup"><span data-stu-id="fe535-103">Representing Objects in XML</span></span>

<span data-ttu-id="fe535-104">Компонент кодировщика XML в инструментарии WMI создает XML-представления объектов.</span><span class="sxs-lookup"><span data-stu-id="fe535-104">The XML encoder component in WMI generates XML representations of objects.</span></span>

<span data-ttu-id="fe535-105">В C++ можно запустить кодировщик XML с помощью вызова метода [**ивбемобжекттекстсрк. gettext**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjecttextsrc-gettext) , указав объект, который должен быть представлен в формате XML, и текстовый формат для использования в представлении.</span><span class="sxs-lookup"><span data-stu-id="fe535-105">In C++, you can start the XML encoder with a call to the [**IWbemObjectTextSrc.GetText**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjecttextsrc-gettext) method, specifying the object to be represented in XML and the text format to use in the representation.</span></span> <span data-ttu-id="fe535-106">Дополнительные сведения и пример кода см. в разделе кодирование объекта в XML с помощью C/C++.</span><span class="sxs-lookup"><span data-stu-id="fe535-106">For more information and a code example, see To encode an object in XML using C/C++.</span></span>

<span data-ttu-id="fe535-107">В VBScript или Visual Basic для кодирования данных для экземпляра XML вызовите [**свбемобжектекс. gettext**](swbemobjectex-gettext-.md).</span><span class="sxs-lookup"><span data-stu-id="fe535-107">In VBScript or Visual Basic, to encode data for an XML instance, call [**SWbemObjectEx.GetText**](swbemobjectex-gettext-.md).</span></span> <span data-ttu-id="fe535-108">Дополнительные сведения и пример кода см. в разделе кодирование объекта в XML с помощью VBScript.</span><span class="sxs-lookup"><span data-stu-id="fe535-108">For more information and a code example, see To encode an object in XML using VBScript.</span></span>

<span data-ttu-id="fe535-109">В этом разделе обсуждаются следующие разделы:</span><span class="sxs-lookup"><span data-stu-id="fe535-109">The following sections are discussed in this topic:</span></span>

-   [<span data-ttu-id="fe535-110">Кодирование объекта с помощью C или C++</span><span class="sxs-lookup"><span data-stu-id="fe535-110">Encode an Object Using C or C++</span></span>](#encode-an-object-using-c-or-c)
-   [<span data-ttu-id="fe535-111">Кодирование объекта с помощью VBScript</span><span class="sxs-lookup"><span data-stu-id="fe535-111">Encode an Object Using VBScript</span></span>](#encode-an-object-using-vbscript)
-   [<span data-ttu-id="fe535-112">См. также</span><span class="sxs-lookup"><span data-stu-id="fe535-112">Related topics</span></span>](#related-topics)

## <a name="encode-an-object-using-c-or-c"></a><span data-ttu-id="fe535-113">Кодирование объекта с помощью C или C++</span><span class="sxs-lookup"><span data-stu-id="fe535-113">Encode an Object Using C or C++</span></span>

<span id="to_encode_an_object_in_xml_using_c_c_"></span><span id="TO_ENCODE_AN_OBJECT_IN_XML_USING_C_C_"></span>

<span data-ttu-id="fe535-114">Следующая процедура описывает, как кодировать объект в XML с помощью C или C++.</span><span class="sxs-lookup"><span data-stu-id="fe535-114">The following procedure describes how to encode an object in XML using C or C++.</span></span>

<span data-ttu-id="fe535-115">**Кодирование объекта в XML с помощью C или C++**</span><span class="sxs-lookup"><span data-stu-id="fe535-115">**To encode an object in XML using C or C++**</span></span>

1.  <span data-ttu-id="fe535-116">Настройте программу для доступа к данным WMI.</span><span class="sxs-lookup"><span data-stu-id="fe535-116">Set up your program to access WMI data.</span></span>

    <span data-ttu-id="fe535-117">Поскольку Инструментарий WMI основан на технологии COM, для доступа к инструментарию WMI необходимо выполнить требуемые вызовы функций [**CoInitializeEx**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex) и [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity) .</span><span class="sxs-lookup"><span data-stu-id="fe535-117">Because WMI is based on COM technology, you must perform the requisite calls to the [**CoInitializeEx**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex) and [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity) functions to access WMI.</span></span> <span data-ttu-id="fe535-118">Дополнительные сведения см. в разделе [Инициализация COM для приложения WMI](initializing-com-for-a-wmi-application.md).</span><span class="sxs-lookup"><span data-stu-id="fe535-118">For more information, see [Initializing COM for a WMI Application](initializing-com-for-a-wmi-application.md).</span></span>

2.  <span data-ttu-id="fe535-119">При необходимости создайте объект [**ивбемконтекст**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemcontext) и инициализируйте его.</span><span class="sxs-lookup"><span data-stu-id="fe535-119">Optionally, create an [**IWbemContext**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemcontext) object and initialize it.</span></span>

    <span data-ttu-id="fe535-120">Не нужно создавать объект [**ивбемконтекст**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemcontext) , если не требуется изменить операцию по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="fe535-120">You do not need to create the [**IWbemContext**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemcontext) object unless you need to change the default operation.</span></span> <span data-ttu-id="fe535-121">Объект контекста используется кодировщиком XML для управления объемом информации, включаемой в XML-представление объекта.</span><span class="sxs-lookup"><span data-stu-id="fe535-121">The context object is used by the XML encoder to control the amount of information included in the object's XML representation.</span></span>

    <span data-ttu-id="fe535-122">В следующей таблице перечислены необязательные значения, которые можно указать для объекта контекста.</span><span class="sxs-lookup"><span data-stu-id="fe535-122">The following table lists the optional values that can be specified for the context object.</span></span>

    

    <table>
    <thead>
    <tr class="header">
    <th><span data-ttu-id="fe535-123">Значение или тип</span><span class="sxs-lookup"><span data-stu-id="fe535-123">Value/type</span></span></th>
    <th><span data-ttu-id="fe535-124">Значение</span><span class="sxs-lookup"><span data-stu-id="fe535-124">Meaning</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td><span data-ttu-id="fe535-125">&quot;LocalOnly &quot; <strong>VT_BOOL</strong></span><span class="sxs-lookup"><span data-stu-id="fe535-125">&quot;LocalOnly&quot; <strong>VT_BOOL</strong></span></span></td>
    <td><span data-ttu-id="fe535-126">Если <strong>значение равно true</strong>, в результирующем XML-коде содержатся только свойства и методы, определенные локально в классе.</span><span class="sxs-lookup"><span data-stu-id="fe535-126">When <strong>TRUE</strong>, only properties and methods defined locally in the class are present in the resulting XML.</span></span> <span data-ttu-id="fe535-127">Значение по умолчанию — <strong>false</strong>.</span><span class="sxs-lookup"><span data-stu-id="fe535-127">The default value is <strong>FALSE</strong>.</span></span></td>
    </tr>
    <tr class="even">
    <td><span data-ttu-id="fe535-128">&quot;Инклудекуалифиерс &quot; <strong>VT_BOOL</strong></span><span class="sxs-lookup"><span data-stu-id="fe535-128">&quot;IncludeQualifiers&quot; <strong>VT_BOOL</strong></span></span></td>
    <td><span data-ttu-id="fe535-129">Если задано <strong>значение true</strong>, то в результирующий XML-документ включаются квалификаторы класса, экземпляра, свойств и методов.</span><span class="sxs-lookup"><span data-stu-id="fe535-129">When <strong>TRUE</strong>, class, instance, properties, and method qualifiers are included in the resulting XML.</span></span> <span data-ttu-id="fe535-130">Значение по умолчанию — <strong>false</strong>.</span><span class="sxs-lookup"><span data-stu-id="fe535-130">The default value is <strong>FALSE</strong>.</span></span></td>
    </tr>
    <tr class="odd">
    <td><span data-ttu-id="fe535-131">&quot;Ексклудесистемпропертиес &quot; <strong>VT_BOOL</strong></span><span class="sxs-lookup"><span data-stu-id="fe535-131">&quot;ExcludeSystemProperties&quot; <strong>VT_BOOL</strong></span></span></td>
    <td><span data-ttu-id="fe535-132">Если <strong>значение равно true</strong>, системные свойства WMI отфильтровываются из выходных данных.</span><span class="sxs-lookup"><span data-stu-id="fe535-132">When <strong>TRUE</strong>, WMI system properties are filtered out of the output.</span></span> <span data-ttu-id="fe535-133">Значение по умолчанию — <strong>false</strong>.</span><span class="sxs-lookup"><span data-stu-id="fe535-133">The default value is <strong>FALSE</strong>.</span></span></td>
    </tr>
    <tr class="even">
    <td><span data-ttu-id="fe535-134">&quot;Паслевел &quot; <strong>VT_I4</strong></span><span class="sxs-lookup"><span data-stu-id="fe535-134">&quot;PathLevel&quot; <strong>VT_I4</strong></span></span></td>
    <td><dl> <span data-ttu-id="fe535-135">0 = <CLASS> <INSTANCE> создается элемент или.</span><span class="sxs-lookup"><span data-stu-id="fe535-135">0 = A <CLASS> or <INSTANCE> element is generated.</span></span><br />
<span data-ttu-id="fe535-136">1 = <VALUE.NAMEDOBJECT> элемент создан.</span><span class="sxs-lookup"><span data-stu-id="fe535-136">1 = A <VALUE.NAMEDOBJECT> element is generated.</span></span><br />
<span data-ttu-id="fe535-137">2 = <VALUE.OBJECTWITHLOCALPATH> создается элемент.</span><span class="sxs-lookup"><span data-stu-id="fe535-137">2 = A <VALUE.OBJECTWITHLOCALPATH> element is generated.</span></span><br />
<span data-ttu-id="fe535-138">3 = создается <VALUE.OBJECTWITHPATH> .</span><span class="sxs-lookup"><span data-stu-id="fe535-138">3 = A <VALUE.OBJECTWITHPATH> is generated.</span></span><br />
    </dl> <span data-ttu-id="fe535-139">Значение по умолчанию равно нулю (0).</span><span class="sxs-lookup"><span data-stu-id="fe535-139">The default is 0 (zero).</span></span><br/></td>
    </tr>
    </tbody>
    </table>

    

     

    <span data-ttu-id="fe535-140">В следующем примере кода показано, как объект контекста инициализируется для включения квалификаторов и исключения системных свойств.</span><span class="sxs-lookup"><span data-stu-id="fe535-140">The following code example shows how the context object is initialized to include qualifiers and exclude system properties.</span></span>

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

    

3.  <span data-ttu-id="fe535-141">Получите ссылку на класс или экземпляр для кодирования в XML.</span><span class="sxs-lookup"><span data-stu-id="fe535-141">Get a reference to the class or instance to encode in XML.</span></span>

    <span data-ttu-id="fe535-142">После инициализации COM и подключения к инструментарию WMI вызовите [**GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject) для получения ссылки на указанный класс или экземпляр.</span><span class="sxs-lookup"><span data-stu-id="fe535-142">After you have initialized COM and are connected to WMI, call [**GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject) to retrieve a reference to the specified class or instance.</span></span> <span data-ttu-id="fe535-143">Если для указания класса или экземпляра использовалась BSTR, вызовите [**сисфристринг**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) , чтобы освободить память, выделенную [**сисаллокстринг**](/windows/win32/api/oleauto/nf-oleauto-sysallocstring).</span><span class="sxs-lookup"><span data-stu-id="fe535-143">If you used a BSTR to specify the class or instance, call [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) to free up the memory allocated by [**SysAllocString**](/windows/win32/api/oleauto/nf-oleauto-sysallocstring).</span></span>

    <span data-ttu-id="fe535-144">В следующем примере кода извлекается ссылка на экземпляр [**Win32 \_ LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) .</span><span class="sxs-lookup"><span data-stu-id="fe535-144">The following code example retrieves a reference to an [**Win32\_LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) instance.</span></span>

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

    

4.  <span data-ttu-id="fe535-145">Создайте объект [**ивбемобжекттекстсрк**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemobjecttextsrc) .</span><span class="sxs-lookup"><span data-stu-id="fe535-145">Create an [**IWbemObjectTextSrc**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemobjecttextsrc) object.</span></span>

    <span data-ttu-id="fe535-146">После создания ссылки на объект необходимо создать объект [**ивбемобжекттекстсрк**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemobjecttextsrc) с вызовом [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance).</span><span class="sxs-lookup"><span data-stu-id="fe535-146">After you have a reference to an object you must create the [**IWbemObjectTextSrc**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemobjecttextsrc) object with a call to [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance).</span></span> <span data-ttu-id="fe535-147">Объект **ивбемобжекттекстсрк** используется для создания фактического текста XML.</span><span class="sxs-lookup"><span data-stu-id="fe535-147">The **IWbemObjectTextSrc** object is used to generate the actual XML text.</span></span>

    <span data-ttu-id="fe535-148">В следующем примере кода показано, как создать объект [**ивбемобжекттекстсрк**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemobjecttextsrc) , вызвав [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance).</span><span class="sxs-lookup"><span data-stu-id="fe535-148">The following code example shows how to create an [**IWbemObjectTextSrc**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemobjecttextsrc) object by calling [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance).</span></span>

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

    

5.  <span data-ttu-id="fe535-149">Вызов метода [**ивбемобжекттекстсрк. gettext**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjecttextsrc-gettext) для получения XML-представления объекта.</span><span class="sxs-lookup"><span data-stu-id="fe535-149">Invoke the [**IWbemObjectTextSrc.GetText**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjecttextsrc-gettext) method to get an XML representation of an object.</span></span>

    <span data-ttu-id="fe535-150">После установки контекста для представления объекта, получения ссылки на объект и создания объекта [**ивбемобжекттекстсрк**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemobjecttextsrc) , можно приступать к ФОРМИРОВАНИЮ XML-представления указанного объекта путем вызова метода [**ивбемобжекттекстсрк. gettext**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjecttextsrc-gettext) .</span><span class="sxs-lookup"><span data-stu-id="fe535-150">After setting the context for the object's representation, getting a reference to the object, and creating an [**IWbemObjectTextSrc**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemobjecttextsrc) object, you are ready to generate an XML representation of the specified object by calling the [**IWbemObjectTextSrc.GetText**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjecttextsrc-gettext) method.</span></span>

    <span data-ttu-id="fe535-151">В следующем примере кода C++ создается XML-представление объекта, на который ссылается *пкласс*.</span><span class="sxs-lookup"><span data-stu-id="fe535-151">The following C++ example code generates an XML representation of the object referenced by *pClass*.</span></span> <span data-ttu-id="fe535-152">XML-представление возвращается в *стртекст*.</span><span class="sxs-lookup"><span data-stu-id="fe535-152">The XML representation is returned in *strText*.</span></span> <span data-ttu-id="fe535-153">Третий параметр в gettext [**указывает формат**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemobjecttextsrc) текста, используемый для XML, и должен быть либо WMI \_ obj \_ Text \_ CIM \_ DTD \_ 2 \_ 0 (0x1), либо \_ текст WMI obj \_ \_ WMI \_ DTD \_ 2 \_ 0 (0x2).</span><span class="sxs-lookup"><span data-stu-id="fe535-153">The third parameter of [**GetText**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemobjecttextsrc) specifies the text format to be used for the XML and must be either WMI\_OBJ\_TEXT\_CIM\_DTD\_2\_0 (0x1) or WMI\_OBJ\_TEXT\_WMI\_DTD\_2\_0 (0x2).</span></span> <span data-ttu-id="fe535-154">Дополнительные сведения об этих значениях см. в разделе значения параметров [**ивбемобжекттекстсрк:: GetText**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjecttextsrc-gettext) .</span><span class="sxs-lookup"><span data-stu-id="fe535-154">For more information about these values, see [**IWbemObjectTextSrc::GetText**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjecttextsrc-gettext) Parameter Values.</span></span>

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

    

<span data-ttu-id="fe535-155">Следующий пример кода C++ включает все шаги, описанные в предыдущей процедуре, и кодирует класс [**Win32 \_ LOGICALDISK**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) в XML, включая квалификаторы класса, свойства и метода и исключая системные свойства.</span><span class="sxs-lookup"><span data-stu-id="fe535-155">The following C++ example code includes all of the steps in the previous procedure and encodes the [**Win32\_LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) class in XML including class, property, and method qualifiers and excluding system properties.</span></span>


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



## <a name="encode-an-object-using-vbscript"></a><span data-ttu-id="fe535-156">Кодирование объекта с помощью VBScript</span><span class="sxs-lookup"><span data-stu-id="fe535-156">Encode an Object Using VBScript</span></span>

<span id="to_encode_an_object_in_xml_using_vbscript"></span><span id="TO_ENCODE_AN_OBJECT_IN_XML_USING_VBSCRIPT"></span>

<span data-ttu-id="fe535-157">Следующая процедура описывает, как кодировать объект в XML с помощью VBScript.</span><span class="sxs-lookup"><span data-stu-id="fe535-157">The following procedure describes how to encode an object in XML using VBScript.</span></span>

<span data-ttu-id="fe535-158">**Кодирование объекта в XML с помощью VBScript**</span><span class="sxs-lookup"><span data-stu-id="fe535-158">**To encode an object in XML using VBScript**</span></span>

1.  <span data-ttu-id="fe535-159">При необходимости создайте объект [**свбемнамедвалуесет**](swbemnamedvalueset.md) и инициализируйте его, чтобы задать значения контекста, необходимые для XML-представления.</span><span class="sxs-lookup"><span data-stu-id="fe535-159">Optionally, create an [**SWbemNamedValueSet**](swbemnamedvalueset.md) object and initialize it so as to set the context values required for the XML representation.</span></span>

    <span data-ttu-id="fe535-160">В следующем примере кода показано, как значения, указывающие кодировщику XML, создавать <значение. ОБЖЕКТВИСЛОКАЛПАС>, включая все квалификаторы и исключение системных свойств при формировании XML-представления объекта.</span><span class="sxs-lookup"><span data-stu-id="fe535-160">The following code example shows how the values instruct the XML encoder to generate a <VALUE.OBJECTWITHLOCALPATH> element, including all of the qualifiers and excluding system properties when it constructs the XML representation of the object.</span></span>

    ```VB
    ' Create an optional SWbemNamedValueSet object
    set context = CreateObject("wbemscripting.SWbemNamedValueSet")

    ' Initialize the value set object to set the context
    ' Generate a <VALUE.OBJECTWITHLOCALPATH> element
    context.add "PathLevel", 2 
    context.add "IncludeQualifiers", true 
    context.add "ExcludeSystemProperties", true '
    ```

    

2.  <span data-ttu-id="fe535-161">Получите экземпляр объекта или класса для представления в XML.</span><span class="sxs-lookup"><span data-stu-id="fe535-161">Retrieve an instance of the object or class to represent in XML.</span></span>

    <span data-ttu-id="fe535-162">В следующем примере кода извлекается экземпляр объекта.</span><span class="sxs-lookup"><span data-stu-id="fe535-162">The following code example retrieves an instance of the object.</span></span>

    ```VB
    ' Retrieve the object/class to be represented in XML
    set myObj = GetObject("winmgmts:\\.\root\cimv2:win32_LogicalDisk")
    ```

    

3.  <span data-ttu-id="fe535-163">Вызовите метод [**gettext \_**](swbemobjectex-gettext-.md) экземпляра, созданного на предыдущем шаге, используя значение 1 в качестве параметра, чтобы указать текстовый формат, соответствующий CIM DTD версии 2,0, или 2, чтобы указать текстовый формат, соответствующий WMI DTD версии 2,0.</span><span class="sxs-lookup"><span data-stu-id="fe535-163">Invoke the [**GetText\_**](swbemobjectex-gettext-.md) method of the instance created in the preceding step, using 1 as the parameter to specify the text format that corresponds to CIM DTD version 2.0, or 2 to specify the text format that corresponds to WMI DTD version 2.0.</span></span> <span data-ttu-id="fe535-164">Если вы создали объект [**свбемнамедвалуесет**](swbemnamedvalueset.md) на шаге 1, включите его в список параметров в качестве третьего параметра.</span><span class="sxs-lookup"><span data-stu-id="fe535-164">If you created the [**SWbemNamedValueSet**](swbemnamedvalueset.md) object in Step 1, include it in the parameter list as the third parameter.</span></span>

    <span data-ttu-id="fe535-165">В следующем примере кода показано, как вызвать метод [**gettext \_**](swbemobjectex-gettext-.md) экземпляра.</span><span class="sxs-lookup"><span data-stu-id="fe535-165">The following code example shows how to invoke the [**GetText\_**](swbemobjectex-gettext-.md) method of the instance.</span></span>

    ```VB
    ' Get the XML representation of the object
    strText = myObj.GetText_(2,,context)

    ' If you have not used a SWbemNamedValueSet object
    ' enter the following line.
    strText = myObj.GetText_(2)
    ```

    

4.  <span data-ttu-id="fe535-166">При необходимости убедитесь, что XML-код, созданный на шаге 3, правильно сформирован, путем создания и инициализации объекта модель DOM XML (DOM) и последующей загрузки XML-текста в него.</span><span class="sxs-lookup"><span data-stu-id="fe535-166">Optionally, validate that the XML generated in Step 3 is well-formed XML, by creating and initializing an XML Document Object Model (DOM) object and then load the XML text into it.</span></span>

    <span data-ttu-id="fe535-167">В следующем примере кода показано, как создать и инициализировать объект DOM XML и загрузить в него XML-текст.</span><span class="sxs-lookup"><span data-stu-id="fe535-167">The following code example shows how to create and initialize an XML DOM object and load the XML text into it.</span></span>

    ```VB
    ' Create an XMLDOM object
    set xml = CreateObject("Microsoft.xmldom")

    ' Initialize the XMLDOM object so results are returned synchronously
    xml.async = false

    ' Load the XML into the XMLDOM object
    xml.loadxml strText
    ```

    

5.  <span data-ttu-id="fe535-168">Вывод XML-представления объекта.</span><span class="sxs-lookup"><span data-stu-id="fe535-168">Output the XML representation of the object.</span></span>

    <span data-ttu-id="fe535-169">В следующем примере кода показано, как использовать Wscript для вывода XML.</span><span class="sxs-lookup"><span data-stu-id="fe535-169">The following code example shows how to use wscript to output the XML.</span></span>

    ```VB
    wscript.echo strText
    ```

    

    <span data-ttu-id="fe535-170">Если вы решили использовать XML DOM для проверки правильности сформированного XML, замените предыдущую строку следующим.</span><span class="sxs-lookup"><span data-stu-id="fe535-170">If you chose to use XML DOM to verify that the XML generated is well-formed, replace the previous line with the following.</span></span>

    ```VB
    wscript.echo xml.xml
    ```

    

<span data-ttu-id="fe535-171">Следующий пример кода VBScript включает все шаги, описанные в предыдущей процедуре, и кодирует класс [**Win32 \_ LOGICALDISK**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) в XML, включая квалификаторы класса, свойства и метода, а также свойства системы.</span><span class="sxs-lookup"><span data-stu-id="fe535-171">The following VBScript code example includes all of the steps in the preceding procedure and encodes the [**Win32\_LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) class in XML, including class, property, and method qualifiers and excluding system properties.</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="fe535-172">См. также</span><span class="sxs-lookup"><span data-stu-id="fe535-172">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fe535-173">Использование инструментария WMI</span><span class="sxs-lookup"><span data-stu-id="fe535-173">Using WMI</span></span>](using-wmi.md)
</dt> </dl>

 

