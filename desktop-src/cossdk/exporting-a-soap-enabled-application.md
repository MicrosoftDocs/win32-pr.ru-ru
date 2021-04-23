---
description: При использовании COM+ для создания веб-службы XML эта служба может использоваться любым полномочным клиентом, включая те, которые не используют COM+ или даже Microsoft Windows.
ms.assetid: c40031a6-f3de-4ef4-b9aa-3f49e57da5b4
title: Экспорт приложения SOAP-Enabled
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2d5c92029f431fc06964f233c5746c283821d11c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103896141"
---
# <a name="exporting-a-soap-enabled-application"></a><span data-ttu-id="94c70-103">Экспорт приложения SOAP-Enabled</span><span class="sxs-lookup"><span data-stu-id="94c70-103">Exporting a SOAP-Enabled Application</span></span>

<span data-ttu-id="94c70-104">При использовании COM+ для создания веб-службы XML эта служба может использоваться любым полномочным клиентом, включая те, которые не используют COM+ или даже Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="94c70-104">When you use COM+ to create an XML web service, that service can be used by any authorized client, including those not using COM+ or even Microsoft Windows.</span></span> <span data-ttu-id="94c70-105">Однако особенно просто использовать веб-службу COM+ в режиме активируемого клиентом объекта (Као) из клиентского приложения COM+.</span><span class="sxs-lookup"><span data-stu-id="94c70-105">However, using a COM+ web service in client-activated object (CAO) mode from a COM+ client application is especially easy.</span></span> <span data-ttu-id="94c70-106">Просто экспортируйте приложение с поддержкой SOAP в режиме прокси-сервера, а затем [импортируйте](importing-a-soap-enabled-application.md) его в клиент, для которого требуется доступ к соответствующей веб-службе XML.</span><span class="sxs-lookup"><span data-stu-id="94c70-106">Just export the SOAP-enabled application in proxy mode, and then [import](importing-a-soap-enabled-application.md) it into the client for which you want to access the corresponding XML web service.</span></span>

## <a name="component-services-administrative-tool"></a><span data-ttu-id="94c70-107">Средство администрирования служб компонентов</span><span class="sxs-lookup"><span data-stu-id="94c70-107">Component Services Administrative Tool</span></span>

<span data-ttu-id="94c70-108">Чтобы экспортировать приложение с поддержкой SOAP с сервера, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="94c70-108">To export a SOAP-enabled application from a server, use the following steps:</span></span>

1.  <span data-ttu-id="94c70-109">В дереве консоли средства администрирования "службы компонентов" в разделе " **службы компонентов**" Откройте папку **приложения COM+** , связанную с компьютером, которым требуется управлять.</span><span class="sxs-lookup"><span data-stu-id="94c70-109">In the console tree of the Component Services administrative tool, under **Component Services**, open the **COM+ Applications** folder associated with the computer you want to manage.</span></span>

2.  <span data-ttu-id="94c70-110">Щелкните правой кнопкой мыши компонент, который нужно предоставить в виде веб-службы XML, и выберите пункт **Экспорт**.</span><span class="sxs-lookup"><span data-stu-id="94c70-110">Right-click the component you want to expose as an XML web service, and choose **Export**.</span></span> <span data-ttu-id="94c70-111">Откроется **Мастер экспорта приложений COM+** .</span><span class="sxs-lookup"><span data-stu-id="94c70-111">The **COM+ Application Export Wizard** appears.</span></span>

3.  <span data-ttu-id="94c70-112">В текстовом поле **введите полный путь и имя файла создаваемого приложения**, введите полный путь и имя файла MSI, который будет содержать экспортированное приложение, или нажмите кнопку **Обзор** , чтобы выбрать полный путь и имя файла с помощью диалогового окна.</span><span class="sxs-lookup"><span data-stu-id="94c70-112">In the text box labeled **Enter the full path and filename for the application file to be created**, enter the full path and filename for the MSI file that will contain the exported application, or click **Browse** to select the full path and filename using a dialog box.</span></span>

4.  <span data-ttu-id="94c70-113">В разделе **экспортировать как** выберите параметр **прокси приложения — установить на других компьютерах, чтобы разрешить доступ к этому** переключателю.</span><span class="sxs-lookup"><span data-stu-id="94c70-113">Under **Export As**, select the **Application Proxy – Install on other machines to enable access to this machine** radio button.</span></span>

## <a name="visual-basic"></a><span data-ttu-id="94c70-114">Visual Basic</span><span class="sxs-lookup"><span data-stu-id="94c70-114">Visual Basic</span></span>

<span data-ttu-id="94c70-115">Не применяется.</span><span class="sxs-lookup"><span data-stu-id="94c70-115">Does not apply.</span></span>

## <a name="cc"></a><span data-ttu-id="94c70-116">C/C++</span><span class="sxs-lookup"><span data-stu-id="94c70-116">C/C++</span></span>

<span data-ttu-id="94c70-117">Не применяется.</span><span class="sxs-lookup"><span data-stu-id="94c70-117">Does not apply.</span></span>

## <a name="related-topics"></a><span data-ttu-id="94c70-118">См. также</span><span class="sxs-lookup"><span data-stu-id="94c70-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="94c70-119">Общие сведения о службе COM+ SOAP</span><span class="sxs-lookup"><span data-stu-id="94c70-119">COM+ SOAP Service Overview</span></span>](com--soap-service-overview.md)
</dt> <dt>

[<span data-ttu-id="94c70-120">Создание веб-служб XML</span><span class="sxs-lookup"><span data-stu-id="94c70-120">Creating XML Web Services</span></span>](creating-xml-web-services.md)
</dt> <dt>

[<span data-ttu-id="94c70-121">Импорт SOAP-Enabled приложения</span><span class="sxs-lookup"><span data-stu-id="94c70-121">Importing a SOAP-Enabled Application</span></span>](importing-a-soap-enabled-application.md)
</dt> </dl>

 

 



