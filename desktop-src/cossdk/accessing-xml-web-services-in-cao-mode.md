---
description: Если веб-служба XML, к которой нужно получить доступ, была создана путем предоставления доступа к приложению COM+, рассмотрите возможность доступа к нему в режиме активируемого клиентом объекта (Као), что позволяет избежать создания прокси-сервера во время выполнения и повысить производительность с помощью постоянных соединений.
ms.assetid: 471de0fa-3429-45f8-abe2-aff0cf6fb350
title: Доступ к веб-службам XML в режиме Као
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 50f1e15c18a925ba88f1b9c7c8267bfb2ef12292
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105682343"
---
# <a name="accessing-xml-web-services-in-cao-mode"></a><span data-ttu-id="279dd-103">Доступ к веб-службам XML в режиме Као</span><span class="sxs-lookup"><span data-stu-id="279dd-103">Accessing XML Web Services in CAO Mode</span></span>

<span data-ttu-id="279dd-104">Если веб-служба XML, к которой нужно получить доступ, была создана путем предоставления доступа к приложению COM+, рассмотрите возможность доступа к нему в режиме активируемого клиентом объекта (Као), что позволяет избежать создания прокси-сервера во время выполнения и повысить производительность с помощью постоянных соединений.</span><span class="sxs-lookup"><span data-stu-id="279dd-104">If the XML web service you want to access was created by exposing a COM+ application, consider accessing it in client-activated object (CAO) mode, which avoids the run-time generation of a proxy and increases performance by using persistent connections.</span></span> <span data-ttu-id="279dd-105">Чтобы получить доступ к веб-службе XML в режиме Као, сначала [экспортируйте](exporting-a-soap-enabled-application.md) соответствующее приложение с поддержкой SOAP с сервера в режиме прокси-сервера, а затем [импортируйте](importing-a-soap-enabled-application.md) приложение в клиент, из которого вы хотите получить доступ к приложению как к веб-службе XML.</span><span class="sxs-lookup"><span data-stu-id="279dd-105">To access an XML web service in CAO mode, first [export](exporting-a-soap-enabled-application.md) the corresponding SOAP-enabled application from your server in proxy mode and then [import](importing-a-soap-enabled-application.md) the application into the client from which you want to access the application as an XML web service.</span></span> <span data-ttu-id="279dd-106">Затем на клиенте можно создать экземпляры компонентов приложения так же, как компоненты локальных приложений, например с помощью **GetObject** и [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance).</span><span class="sxs-lookup"><span data-stu-id="279dd-106">The application's components can then be instantiated on the client just like the components of local applications—for example, using **GetObject** and [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance).</span></span>

## <a name="user-interface"></a><span data-ttu-id="279dd-107">Пользовательский интерфейс</span><span class="sxs-lookup"><span data-stu-id="279dd-107">User Interface</span></span>

<span data-ttu-id="279dd-108">Не применяется.</span><span class="sxs-lookup"><span data-stu-id="279dd-108">Does not apply.</span></span>

## <a name="visual-basic"></a><span data-ttu-id="279dd-109">Visual Basic</span><span class="sxs-lookup"><span data-stu-id="279dd-109">Visual Basic</span></span>

<span data-ttu-id="279dd-110">В следующем Visual Basic фрагменте кода показано использование компонента приложения COM+, доступного в виде веб-службы XML в режиме Као.</span><span class="sxs-lookup"><span data-stu-id="279dd-110">The following Visual Basic code fragment illustrates the use of a component of a COM+ application that has been exposed as an XML web service in CAO mode.</span></span>


```VB
Set Obj = GetObject("progID")
output = Obj.Method(input)
```



## <a name="cc"></a><span data-ttu-id="279dd-111">C/C++</span><span class="sxs-lookup"><span data-stu-id="279dd-111">C/C++</span></span>

<span data-ttu-id="279dd-112">В следующем фрагменте кода показано использование компонента приложения COM+, доступного в виде веб-службы XML, в режиме Као.</span><span class="sxs-lookup"><span data-stu-id="279dd-112">The following code fragment illustrates the use of a component of a COM+ application that has been exposed as an XML web service in CAO mode.</span></span>


```C++
HRESULT hr = CoCreateInstance(
     CLSID_CObject,  // CLSID of the server component
     NULL,
     pBindOptions,
     IID_IUnknown,
     (void**)&pIUnknown);
if (FAILED(hr)) throw(hr);
```



## <a name="related-topics"></a><span data-ttu-id="279dd-113">См. также</span><span class="sxs-lookup"><span data-stu-id="279dd-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="279dd-114">Доступ к веб-службам XML в режиме ВКО</span><span class="sxs-lookup"><span data-stu-id="279dd-114">Accessing XML Web Services in WKO Mode</span></span>](accessing-xml-web-services-in-wko-mode.md)
</dt> <dt>

[<span data-ttu-id="279dd-115">Общие сведения о службе COM+ SOAP</span><span class="sxs-lookup"><span data-stu-id="279dd-115">COM+ SOAP Service Overview</span></span>](com--soap-service-overview.md)
</dt> <dt>

[<span data-ttu-id="279dd-116">Создание веб-служб XML</span><span class="sxs-lookup"><span data-stu-id="279dd-116">Creating XML Web Services</span></span>](creating-xml-web-services.md)
</dt> <dt>

[<span data-ttu-id="279dd-117">Защита веб-служб XML</span><span class="sxs-lookup"><span data-stu-id="279dd-117">Securing XML Web Services</span></span>](securing-xml-web-services.md)
</dt> </dl>

 

 
