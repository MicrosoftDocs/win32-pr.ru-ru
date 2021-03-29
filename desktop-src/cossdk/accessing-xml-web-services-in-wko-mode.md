---
description: Можно получить доступ к любой веб-службе XML и использовать ее, даже если эта веб-служба XML не была создана с помощью COM+ или даже Microsoft Windows, при условии, что веб-служба XML публикует описание синтаксиса WSDL.
ms.assetid: 5b21ff0c-f3a5-464b-b927-a7872ac54fe2
title: Доступ к веб-службам XML в режиме ВКО
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e726f430c47b3202932796455e1cf997e370a022
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103807295"
---
# <a name="accessing-xml-web-services-in-wko-mode"></a><span data-ttu-id="99114-103">Доступ к веб-службам XML в режиме ВКО</span><span class="sxs-lookup"><span data-stu-id="99114-103">Accessing XML Web Services in WKO Mode</span></span>

<span data-ttu-id="99114-104">Можно получить доступ к любой веб-службе XML и использовать ее, даже если эта веб-служба XML не была создана с помощью COM+ или даже Microsoft Windows, при условии, что веб-служба XML публикует описание синтаксиса WSDL.</span><span class="sxs-lookup"><span data-stu-id="99114-104">You can access and use any XML web service, even if that XML web service was not created using COM+ or even Microsoft Windows, as long as the XML Web Service publishes a WSDL description of its syntax.</span></span> <span data-ttu-id="99114-105">Просто создайте экземпляр компонента с помощью моникера SOAP: WSDL = URL, где URL — это URL-адрес описания языка WSDL XML Web Service, к которому требуется получить доступ.</span><span class="sxs-lookup"><span data-stu-id="99114-105">Just create an instance of the component by using the soap:wsdl=URL moniker, where URL is the URL of the WSDL description of the XML web service you want to access.</span></span> <span data-ttu-id="99114-106">Это режим хорошо известного объекта (ВКО) для доступа к веб-службам XML.</span><span class="sxs-lookup"><span data-stu-id="99114-106">This is the well-known object (WKO) mode of accessing XML web services.</span></span>

<span data-ttu-id="99114-107">Методы объекта могут вызываться без каких бы то ни было особых соображений.</span><span class="sxs-lookup"><span data-stu-id="99114-107">The object's methods can be called without any special considerations.</span></span> <span data-ttu-id="99114-108">Доступ к веб-службе XML осуществляется через запрос SOAP, и ответ интерпретируется прозрачно.</span><span class="sxs-lookup"><span data-stu-id="99114-108">The XML web service is accessed via a SOAP query, and the response is interpreted transparently.</span></span>

## <a name="component-services-administrative-tool"></a><span data-ttu-id="99114-109">Средство администрирования служб компонентов</span><span class="sxs-lookup"><span data-stu-id="99114-109">Component Services Administrative Tool</span></span>

<span data-ttu-id="99114-110">Не применяется.</span><span class="sxs-lookup"><span data-stu-id="99114-110">Does not apply.</span></span>

## <a name="visual-basic"></a><span data-ttu-id="99114-111">Visual Basic</span><span class="sxs-lookup"><span data-stu-id="99114-111">Visual Basic</span></span>

<span data-ttu-id="99114-112">В следующем фрагменте кода Microsoft Visual Basic показано использование веб-службы XML в режиме ВКО.</span><span class="sxs-lookup"><span data-stu-id="99114-112">The following Microsoft Visual Basic code fragment illustrates the use of an XML web service in WKO mode.</span></span>


```VB
Set Obj = GetObject("soap:wsdl=https://servername/vroot/progID.soap?WSDL")
output = Obj.Method(input)
```



<span data-ttu-id="99114-113">В этом фрагменте кода, который иллюстрирует использование компонента приложения COM+, предоставленного в виде веб-службы XML, ServerName — полное доменное имя сервера, на котором размещается веб-служба XML. vroot — это виртуальный корневой каталог IIS, из которого предоставляется веб-служба XML; и progID — это ProgID компонента, который вы хотите использовать.</span><span class="sxs-lookup"><span data-stu-id="99114-113">In this code fragment, which illustrates the use of a component of a COM+ application that has been exposed as an XML web service, servername is the fully qualified domain name of the server offering the XML web service; vroot is the IIS virtual root directory from which the XML web service is exposed; and progID is the ProgID of the component you want to use.</span></span>

## <a name="cc"></a><span data-ttu-id="99114-114">C/C++</span><span class="sxs-lookup"><span data-stu-id="99114-114">C/C++</span></span>

<span data-ttu-id="99114-115">В следующем фрагменте кода показано использование веб-службы XML в режиме ВКО.</span><span class="sxs-lookup"><span data-stu-id="99114-115">The following code fragment illustrates the use of an XML web service in WKO mode.</span></span>


```C++
HRESULT hr = CoGetObject(
     L"soap:wsdl=https://servername/vroot/progID.soap?WSDL",
     pBindOptions,
     IID_IUnknown,
     (void**)&pIUnknown);
if (FAILED(hr)) throw(hr); 
```



<span data-ttu-id="99114-116">В этом фрагменте кода, который иллюстрирует использование компонента приложения COM+, предоставленного в виде веб-службы XML, ServerName — полное доменное имя сервера, на котором размещается веб-служба XML. vroot — это виртуальный корневой каталог IIS, из которого предоставляется веб-служба XML; и progID — это ProgID компонента, который вы хотите использовать.</span><span class="sxs-lookup"><span data-stu-id="99114-116">In this code fragment, which illustrates the use of a component of a COM+ application that has been exposed as an XML web service, servername is the fully qualified domain name of the server offering the XML web service; vroot is the IIS virtual root directory from which the XML web service is exposed; and progID is the ProgID of the component you want to use.</span></span>

## <a name="remarks"></a><span data-ttu-id="99114-117">Комментарии</span><span class="sxs-lookup"><span data-stu-id="99114-117">Remarks</span></span>

<span data-ttu-id="99114-118">При первом обращении к веб-службе XML в режиме ВКО COM+ создает прокси-клиент и компилирует его в фоновый режим.</span><span class="sxs-lookup"><span data-stu-id="99114-118">When an XML web service is first accessed in WKO mode, COM+ generates a proxy client and compiles it in the background.</span></span> <span data-ttu-id="99114-119">Это поколение времени выполнения и отсутствие постоянных подключений в режиме ВКО значительно снижают производительность в сравнении с режимом Као.</span><span class="sxs-lookup"><span data-stu-id="99114-119">This run-time generation and the lack of persistent connections in WKO mode results in significantly reduced performance in comparison to CAO mode.</span></span>

## <a name="related-topics"></a><span data-ttu-id="99114-120">См. также</span><span class="sxs-lookup"><span data-stu-id="99114-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="99114-121">Доступ к веб-службам XML в режиме Као</span><span class="sxs-lookup"><span data-stu-id="99114-121">Accessing XML Web Services in CAO Mode</span></span>](accessing-xml-web-services-in-cao-mode.md)
</dt> <dt>

[<span data-ttu-id="99114-122">Общие сведения о службе COM+ SOAP</span><span class="sxs-lookup"><span data-stu-id="99114-122">COM+ SOAP Service Overview</span></span>](com--soap-service-overview.md)
</dt> <dt>

[<span data-ttu-id="99114-123">Создание веб-служб XML</span><span class="sxs-lookup"><span data-stu-id="99114-123">Creating XML Web Services</span></span>](creating-xml-web-services.md)
</dt> <dt>

[<span data-ttu-id="99114-124">Защита веб-служб XML</span><span class="sxs-lookup"><span data-stu-id="99114-124">Securing XML Web Services</span></span>](securing-xml-web-services.md)
</dt> </dl>

 

 



