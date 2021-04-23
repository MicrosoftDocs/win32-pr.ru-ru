---
title: сессионфуллкалкулаторклиентексампле
description: Клиентское приложение для взаимодействия со службой калькулятора сеансов.
ms.assetid: 0981474c-cb87-4069-ab84-7662776c182e
keywords:
- Сессионфуллкалкулаторклиентексампле Native-Web-Services
- ввсапи
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 831816270616d59c77aa3e178feee55af24e35c7
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103775764"
---
# <a name="sessionfullcalculatorclientexample"></a><span data-ttu-id="d2ff7-106">сессионфуллкалкулаторклиентексампле</span><span class="sxs-lookup"><span data-stu-id="d2ff7-106">SessionfullCalculatorClientExample</span></span>

<span data-ttu-id="d2ff7-107">Клиентское приложение для взаимодействия со службой калькулятора сеансов.</span><span class="sxs-lookup"><span data-stu-id="d2ff7-107">Client application to talk to a sessionful calculator service.</span></span>

-   [<span data-ttu-id="d2ff7-108">Сессионфуллкалкулаторклиент. cpp</span><span class="sxs-lookup"><span data-stu-id="d2ff7-108">SessionfullCalculatorClient.cpp</span></span>](#sessionfullcalculatorclientcpp)
-   [<span data-ttu-id="d2ff7-109">Сессионбаседкалкулаторсервице. WSDL</span><span class="sxs-lookup"><span data-stu-id="d2ff7-109">SessionBasedCalculatorService.wsdl</span></span>](#sessionbasedcalculatorservicewsdl)
-   [<span data-ttu-id="d2ff7-110">Makefile</span><span class="sxs-lookup"><span data-stu-id="d2ff7-110">Makefile</span></span>](#makefile)

## <a name="sessionfullcalculatorclientcpp"></a><span data-ttu-id="d2ff7-111">Сессионфуллкалкулаторклиент. cpp</span><span class="sxs-lookup"><span data-stu-id="d2ff7-111">SessionfullCalculatorClient.cpp</span></span>


```C++
//------------------------------------------------------------
// Copyright (C) Microsoft.  All rights reserved.
//------------------------------------------------------------

#ifndef UNICODE
#define UNICODE
#endif
#include <windows.h>
#include <stdio.h>
#include "WebServices.h"
#include "process.h"
#include "string.h"
#include "SessionBasedCalculatorService.wsdl.h"
// Print out rich error info
void PrintError(HRESULT errorCode, WS_ERROR* error)
{
    wprintf(L"Failure: errorCode=0x%lx\n", errorCode);

    if (errorCode == E_INVALIDARG || errorCode == WS_E_INVALID_OPERATION)
    {
        // Correct use of the APIs should never generate these errors
        wprintf(L"The error was due to an invalid use of an API.  This is likely due to a bug in the program.\n");
        DebugBreak();
    }

    HRESULT hr = NOERROR;
    if (error != NULL)
    {
        ULONG errorCount;
        hr = WsGetErrorProperty(error, WS_ERROR_PROPERTY_STRING_COUNT, &errorCount, sizeof(errorCount));
        if (FAILED(hr))
        {
            goto Exit;
        }
        for (ULONG i = 0; i < errorCount; i++)
        {
            WS_STRING string;
            hr = WsGetErrorString(error, i, &string);
            if (FAILED(hr))
            {
                goto Exit;
            }
            wprintf(L"%.*s\n", string.length, string.chars);
        }
    }
Exit:
    if (FAILED(hr))
    {
        wprintf(L"Could not get error string (errorCode=0x%lx)\n", hr);
    }
}
// Main entry point
int __cdecl wmain(int argc, __in_ecount(argc) wchar_t **argv)
{
    UNREFERENCED_PARAMETER(argc);
    UNREFERENCED_PARAMETER(argv);
    
    HRESULT hr = NOERROR;
    WS_ERROR* error = NULL;
    WS_HEAP* heap = NULL;
    WS_SERVICE_PROXY* proxy = NULL;
    int result = 0;
    WS_ENDPOINT_ADDRESS address = {};
    WS_STRING serviceUrl = WS_STRING_VALUE(L"net.tcp://localhost/example"); 
    // Create an error object for storing rich error information
    hr = WsCreateError(
        NULL, 
        0, 
        &error);
    if (FAILED(hr))
    {
        goto Exit;
    }
    // Create a heap to store deserialized data
    hr = WsCreateHeap(
        /*maxSize*/ 2048, 
        /*trimSize*/ 512, 
        NULL, 
        0, 
        &heap, 
        error);
    if (FAILED(hr))
    {
        goto Exit;
    }
    hr = WsCreateServiceProxy(
        WS_CHANNEL_TYPE_DUPLEX_SESSION, 
        WS_TCP_CHANNEL_BINDING, 
        NULL, 
        NULL, 
        0, 
        NULL,
        0,
        &proxy, 
        error);
    if (FAILED(hr))
    {
        goto Exit;
    }
                        
    
    // Initialize address of service
    address.url = serviceUrl;
    hr = WsOpenServiceProxy(
        proxy, 
        &address, 
        NULL, 
        error);
    if (FAILED(hr))
    {
        goto Exit;
    }
    
    hr = CalculatorBinding_Add(
        proxy, 
        1, 
        heap, 
        NULL, 
        0, 
        NULL, 
        error);
    if (FAILED(hr))
    {
        goto Exit;
    }
    
    wprintf(
        L"+1\n");
    hr = CalculatorBinding_Add(
        proxy, 
        2, 
        heap,
        NULL,
        0, 
        NULL,
        error);
    if (FAILED(hr))
    {
        goto Exit;
    }
    
    wprintf(
        L"+2\n");
    
    hr = CalculatorBinding_Add(
            proxy,
            3, 
            heap,
            NULL,
            0,
            NULL,
            error);
    if (FAILED(hr))
    {
        goto Exit;
    }
    
    wprintf(
        L"+3\n");
    hr = CalculatorBinding_Add(
            proxy,
            4, 
            heap,
            NULL,
            0, 
            NULL,
            error);
    if (FAILED(hr))
    {
        goto Exit;
    }
    
    wprintf(
        L"+4\n");
    hr = CalculatorBinding_Subtract(
            proxy,
            5, 
            heap,
            NULL,
            0,
            NULL,
            error);
    if (FAILED(hr))
    {
        goto Exit;
    }
    
    wprintf(
        L"-5\n");
    hr = CalculatorBinding_Total(
        proxy,
        &result,
        heap,
        NULL,
        0,
        NULL,
        error);
    if (FAILED(hr))
    {
        goto Exit;
    }
    
    wprintf(
        L"====\n");
    wprintf(
        L"%d\n", result);
    
    hr = CalculatorBinding_Clear(
        proxy,
        heap,
        NULL,
        0,
        NULL,
        error);
    if (FAILED(hr))
    {
        goto Exit;
    }
                   
Exit:
    if (FAILED(hr))
    {
        // Print out the error
        PrintError(hr, error);
    }
    fflush(
        stdout);
    if (proxy != NULL)
    {
        WsCloseServiceProxy(
            proxy, 
            NULL, 
            NULL);
    
        WsFreeServiceProxy(
            proxy);
    }
    
    
    if (heap != NULL)
    {
        WsFreeHeap(heap);
    }
    if (error != NULL)
    {
        WsFreeError(error);
    }
    fflush(stdout);
    return SUCCEEDED(hr) ? 0 : -1;
}


```



## <a name="sessionbasedcalculatorservicewsdl"></a><span data-ttu-id="d2ff7-112">Сессионбаседкалкулаторсервице. WSDL</span><span class="sxs-lookup"><span data-stu-id="d2ff7-112">SessionBasedCalculatorService.wsdl</span></span>

``` syntax
<?xml version="1.0" encoding="UTF-8"?>
<wsdl:definitions 
    xmlns:wsdl="http://schemas.xmlsoap.org/wsdl/" 
    xmlns:soap="http://schemas.xmlsoap.org/wsdl/soap/" 
    xmlns:http="http://schemas.xmlsoap.org/wsdl/http/" 
    xmlns:tns="http://www.example.org" 
    xmlns:xsd="http://www.w3.org/2001/XMLSchema" 
    xmlns:wsaw="http://www.w3.org/2006/05/addressing/wsdl" 
    targetNamespace="http://www.example.org">
    <wsdl:types>
        <xsd:schema targetNamespace="http://www.example.org" elementFormDefault="qualified">
            <xsd:element name="AddType">
                <xsd:complexType>
                    <xsd:sequence>
                        <xsd:element minOccurs="0" name="addend" type="xsd:int"/>
                    </xsd:sequence>
                </xsd:complexType>
            </xsd:element>
            <xsd:element name="SubtractType">
                <xsd:complexType>
                    <xsd:sequence>
                        <xsd:element minOccurs="0" name="subtractend" type="xsd:int"/>
                    </xsd:sequence>
                </xsd:complexType>
            </xsd:element>
            <xsd:element name="TotalResponseType">
                <xsd:complexType>
                    <xsd:sequence>
                        <xsd:element minOccurs="0" name="Total" type="xsd:int"/>
                    </xsd:sequence>
                </xsd:complexType>
            </xsd:element>
            <xsd:element name="AddResponseType">
                <xsd:complexType/>
            </xsd:element>
            <xsd:element name="SubtractResponseType">
                <xsd:complexType/>
            </xsd:element>
            <xsd:element name="TotalRequestType">
                <xsd:complexType/>
            </xsd:element>
            <xsd:element name="ClearType">
                <xsd:complexType/>
            </xsd:element>
        </xsd:schema>
    </wsdl:types>
    <wsdl:message name="AddMessage">
        <wsdl:part name="parameters" element="tns:AddType"/>
    </wsdl:message>
    <wsdl:message name="AddResponseMessage">
        <wsdl:part name="parameters" element="tns:AddResponseType"/>
    </wsdl:message>
    <wsdl:message name="SubtractMessage">
        <wsdl:part name="parameters" element="tns:SubtractType"/>
    </wsdl:message>
    <wsdl:message name="SubtractResponseMessage">
        <wsdl:part name="parameters" element="tns:SubtractResponseType"/>
    </wsdl:message>
    <wsdl:message name="TotalRequest">
        <wsdl:part name="parameters" element="tns:TotalRequestType"/>
    </wsdl:message>
    <wsdl:message name="TotalResponse">
        <wsdl:part name="parameters" element="tns:TotalResponseType"/>
    </wsdl:message>
    <wsdl:message name="ClearMessage">
        <wsdl:part name="parameters" element="tns:ClearType"/>
    </wsdl:message>
    <wsdl:portType name="ISessionBasedCalculator">
        <wsdl:operation name="Add">
            <wsdl:input message="tns:AddMessage" wsaw:Action="http://www.example.org/Add"/>
            <wsdl:output message="tns:AddResponseMessage" wsaw:Action="http://www.example.org/AddResponse"/>
        </wsdl:operation>
        <wsdl:operation name="Subtract">
            <wsdl:input message="tns:SubtractMessage" wsaw:Action="http://www.example.org/Subtract"/>
            <wsdl:output message="tns:SubtractResponseMessage" wsaw:Action="http://www.example.org/SubtractResponse"/>
        </wsdl:operation>
        <wsdl:operation name="Total">
            <wsdl:output message="tns:TotalResponse" wsaw:Action="http://www.example.org/TotalResponse"/>
            <wsdl:input message="tns:TotalRequest" wsaw:Action="http://www.example.org/Total"/>
        </wsdl:operation>
        <wsdl:operation name="Clear">
            <wsdl:input message="tns:ClearMessage" wsaw:Action="http://www.example.org/Clear"/>
        </wsdl:operation>
    </wsdl:portType>
    <wsdl:binding name="CalculatorBinding" type="tns:ISessionBasedCalculator">
        <soap:binding style="document" transport="http://schemas.xmlsoap.org/soap/http"/>
        <wsdl:operation name="Add">
            <soap:operation soapAction="http://www.example.org/Add"/>
            <wsdl:input>
                <soap:body use="literal"/>
            </wsdl:input>
            <wsdl:output>
                <soap:body use="literal"/>
            </wsdl:output>
        </wsdl:operation>
        <wsdl:operation name="Subtract">
            <soap:operation soapAction="http://www.example.org/Subtract"/>
            <wsdl:input>
                <soap:body use="literal"/>
            </wsdl:input>
            <wsdl:output>
                <soap:body use="literal"/>
            </wsdl:output>
        </wsdl:operation>
        <wsdl:operation name="Total">
            <soap:operation soapAction="http://www.example.org/Total"/>
            <wsdl:input>
                <soap:body use="literal"/>
            </wsdl:input>
            <wsdl:output>
                <soap:body use="literal"/>
            </wsdl:output>
        </wsdl:operation>
        <wsdl:operation name="Clear">
            <soap:operation soapAction="http://www.example.org/Clear"/>
            <wsdl:input>
                <soap:body use="literal"/>
            </wsdl:input>
        </wsdl:operation>
    </wsdl:binding>
    <wsdl:service name="SessionBasedService">
        <wsdl:port name="Calculator" binding="tns:CalculatorBinding">
            <soap:address location="No Target Address"/>
        </wsdl:port>
    </wsdl:service>
</wsdl:definitions>
```

## <a name="makefile"></a><span data-ttu-id="d2ff7-113">Makefile</span><span class="sxs-lookup"><span data-stu-id="d2ff7-113">Makefile</span></span>

``` syntax
!include <Win32.Mak>

EXTRA_LIBS = WebServices.lib rpcrt4.lib Iphlpapi.lib

all: $(OUTDIR) $(OUTDIR)\WsSessionfullCalculatorClient.exe

"$(OUTDIR)" :
    if not exist "$(OUTDIR)/$(NULL)" mkdir "$(OUTDIR)"
    
$(OUTDIR)\SessionBasedCalculatorService.wsdl.c: SessionBasedCalculatorService.wsdl
     Wsutil.exe /wsdl:SessionBasedCalculatorService.wsdl /string:WS_STRING /out:$(OUTDIR)
    
$(OUTDIR)\SessionBasedCalculatorService.wsdl.obj: $(OUTDIR)\SessionBasedCalculatorService.wsdl.c
    $(cc) $(cdebug) $(cflags) $(cvarsmt) /WX -I$(OUTDIR) /Fo"$(OUTDIR)\\" /Fd"$(OUTDIR)\\" $(OUTDIR)\SessionBasedCalculatorService.wsdl.c

$(OUTDIR)\SessionfullCalculatorClient.obj: SessionfullCalculatorClient.cpp $(OUTDIR)\SessionBasedCalculatorService.wsdl.c
    $(cc) $(cdebug) $(cflags) $(cvarsmt) /WX -I$(OUTDIR) /Fo"$(OUTDIR)\\" /Fd"$(OUTDIR)\\" SessionfullCalculatorClient.cpp

$(OUTDIR)\WsSessionfullCalculatorClient.exe: $(OUTDIR)\SessionfullCalculatorClient.obj $(OUTDIR)\SessionBasedCalculatorService.wsdl.obj
    $(link) $(ldebug) $(conlflags) $(conlibsmt) $(EXTRA_LIBS) -out:$(OUTDIR)\WsSessionfullCalculatorClient.exe $(OUTDIR)\SessionfullCalculatorClient.obj $(OUTDIR)\SessionBasedCalculatorService.wsdl.obj /PDB:$(OUTDIR)\WsSessionfullCalculatorClient.PDB

clean:
    $(CLEANUP)
```

 

 




