---
description: Когда приложение с поддержкой SOAP было экспортировано с сервера в режиме прокси-сервера, клиенты, которые его импортируют, могут автоматически обращаться к методам компонентов, которые он содержит, в качестве веб-служб, предлагаемых сервером в режиме активируемого клиентом объекта (Као). Это позволяет легко развертывать функциональные возможности приложения COM+ по сети в виде веб-службы XML.
ms.assetid: 7f4783f7-4f53-4f0b-bb64-ae7903097d6c
title: Импорт SOAP-Enabled приложения
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2d9faca91a726caea765d4b2ca227ddba0ff3a2f
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104539302"
---
# <a name="importing-a-soap-enabled-application"></a><span data-ttu-id="00c33-104">Импорт SOAP-Enabled приложения</span><span class="sxs-lookup"><span data-stu-id="00c33-104">Importing a SOAP-Enabled Application</span></span>

<span data-ttu-id="00c33-105">Когда приложение с поддержкой SOAP было [экспортировано](exporting-a-soap-enabled-application.md) с сервера в режиме прокси-сервера, клиенты, которые его импортируют, могут автоматически обращаться к методам компонентов, которые он содержит, в качестве веб-служб, предлагаемых сервером в режиме активируемого клиентом объекта (Као).</span><span class="sxs-lookup"><span data-stu-id="00c33-105">When a SOAP-enabled application has been [exported](exporting-a-soap-enabled-application.md) from a server in proxy mode, clients that import it can automatically access the methods of the components it contains, remotely, as web services offered by the server in client-activated object (CAO) mode.</span></span> <span data-ttu-id="00c33-106">Это позволяет легко развертывать функциональные возможности приложения COM+ по сети в виде веб-службы XML.</span><span class="sxs-lookup"><span data-stu-id="00c33-106">This allows you to very easily deploy the functionality of a COM+ application across a network as an XML web service.</span></span>

<span data-ttu-id="00c33-107">Когда компоненты приложения, импортированные таким образом, используются на клиенте, они не запускаются на клиенте, а становятся доступными удаленно с помощью веб-службы XML, предоставляемой сервером, с которого было экспортировано приложение.</span><span class="sxs-lookup"><span data-stu-id="00c33-107">When the components of an application imported in this way are used on the client, they do not run on the client but instead are accessed remotely by using the XML web service provided by the server from which the application was exported.</span></span> <span data-ttu-id="00c33-108">Дополнительные сведения об использовании компонентов приложения, импортированных таким образом, см. [в разделе доступ к веб-службам XML в режиме Као](accessing-xml-web-services-in-cao-mode.md).</span><span class="sxs-lookup"><span data-stu-id="00c33-108">For details on using the components of an application imported in this way, see [Accessing XML Web Services in CAO Mode](accessing-xml-web-services-in-cao-mode.md).</span></span>

## <a name="component-services-administrative-tool"></a><span data-ttu-id="00c33-109">Средство администрирования служб компонентов</span><span class="sxs-lookup"><span data-stu-id="00c33-109">Component Services Administrative Tool</span></span>

<span data-ttu-id="00c33-110">Чтобы импортировать приложение с поддержкой SOAP в клиент, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="00c33-110">To import a SOAP-enabled application into a client, use the following steps:</span></span>

1.  <span data-ttu-id="00c33-111">В дереве консоли средства администрирования "службы компонентов" в разделе " **службы компонентов**" Откройте папку, связанную с клиентским компьютером, на котором нужно установить приложение.</span><span class="sxs-lookup"><span data-stu-id="00c33-111">In the console tree of the Component Services administrative tool, under **Component Services**, open the folder associated with the client computer on which you want to install the application.</span></span>

2.  <span data-ttu-id="00c33-112">Щелкните правой кнопкой мыши папку **приложения COM+** клиента и выберите пункт **создать**.</span><span class="sxs-lookup"><span data-stu-id="00c33-112">Right-click the client's **COM+ Applications** folder, and then choose **New**.</span></span> <span data-ttu-id="00c33-113">Откроется **Мастер установки приложения COM+** .</span><span class="sxs-lookup"><span data-stu-id="00c33-113">The **COM+ Application Install Wizard** appears.</span></span>

3.  <span data-ttu-id="00c33-114">В **мастере установки приложения COM+** щелкните **установить предварительно созданные приложения**.</span><span class="sxs-lookup"><span data-stu-id="00c33-114">In the **COM+ Application Install Wizard**, click **Install pre-built application(s)**.</span></span>

4.  <span data-ttu-id="00c33-115">Просмотрите сеть, чтобы найти или указать сетевой путь к MSI файл на сервере, с которого требуется установить приложение.</span><span class="sxs-lookup"><span data-stu-id="00c33-115">Browse the network to locate or specify the network path of the MSI file on the server from which you want to install the application.</span></span>

## <a name="visual-basic"></a><span data-ttu-id="00c33-116">Visual Basic</span><span class="sxs-lookup"><span data-stu-id="00c33-116">Visual Basic</span></span>

<span data-ttu-id="00c33-117">Не применяется.</span><span class="sxs-lookup"><span data-stu-id="00c33-117">Does not apply.</span></span>

## <a name="cc"></a><span data-ttu-id="00c33-118">C/C++</span><span class="sxs-lookup"><span data-stu-id="00c33-118">C/C++</span></span>

<span data-ttu-id="00c33-119">Не применяется.</span><span class="sxs-lookup"><span data-stu-id="00c33-119">Does not apply.</span></span>

## <a name="remarks"></a><span data-ttu-id="00c33-120">Комментарии</span><span class="sxs-lookup"><span data-stu-id="00c33-120">Remarks</span></span>

<span data-ttu-id="00c33-121">COM-компоненты идентифицируются по идентификатору GUID, который изменяется при повторной компиляции компонентов.</span><span class="sxs-lookup"><span data-stu-id="00c33-121">COM components are identified by a GUID, which changes if the components are recompiled.</span></span> <span data-ttu-id="00c33-122">Если перекомпилируется настроенный COM-компонент, предоставляемый в виде XML, клиентские приложения, использующие ее, будут нарушены.</span><span class="sxs-lookup"><span data-stu-id="00c33-122">If a configured COM component that is exposed as an XML web service is recompiled, client applications that use it will break.</span></span> <span data-ttu-id="00c33-123">Поэтому при перекомпиляции компонента, предоставляемого в виде веб-службы XML, клиенты должны повторно импортировать приложения, использующие этот компонент.</span><span class="sxs-lookup"><span data-stu-id="00c33-123">Therefore, when a component that is exposed as an XML web service is recompiled, clients should re-import the applications that use the component.</span></span>

## <a name="related-topics"></a><span data-ttu-id="00c33-124">См. также</span><span class="sxs-lookup"><span data-stu-id="00c33-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="00c33-125">Общие сведения о службе COM+ SOAP</span><span class="sxs-lookup"><span data-stu-id="00c33-125">COM+ SOAP Service Overview</span></span>](com--soap-service-overview.md)
</dt> <dt>

[<span data-ttu-id="00c33-126">Создание веб-служб XML</span><span class="sxs-lookup"><span data-stu-id="00c33-126">Creating XML Web Services</span></span>](creating-xml-web-services.md)
</dt> <dt>

[<span data-ttu-id="00c33-127">Экспорт приложения SOAP-Enabled</span><span class="sxs-lookup"><span data-stu-id="00c33-127">Exporting a SOAP-Enabled Application</span></span>](exporting-a-soap-enabled-application.md)
</dt> </dl>

 

 



