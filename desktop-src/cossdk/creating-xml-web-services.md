---
description: Любое приложение COM+ может быть представлено в виде веб-службы XML.
ms.assetid: 03c3d5a7-eb98-4916-b6ef-ef6aac86c574
title: Создание веб-служб XML
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b10652531e64fec38f2ac221184cb589a27b343d
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105701209"
---
# <a name="creating-xml-web-services"></a><span data-ttu-id="85b1f-103">Создание веб-служб XML</span><span class="sxs-lookup"><span data-stu-id="85b1f-103">Creating XML Web Services</span></span>

<span data-ttu-id="85b1f-104">Любое приложение COM+ может быть представлено в виде веб-службы XML.</span><span class="sxs-lookup"><span data-stu-id="85b1f-104">Any COM+ application can be exposed as an XML web service.</span></span> <span data-ttu-id="85b1f-105">Методы в интерфейсах по умолчанию настроенных компонентов приложения (компоненты в каталоге серверов COM+) затем могут быть вызваны удаленно.</span><span class="sxs-lookup"><span data-stu-id="85b1f-105">The methods in the default interfaces of the applications configured components (components in the servers COM+ catalog) can then be called remotely.</span></span> <span data-ttu-id="85b1f-106">Средство администрирования служб компонентов можно использовать для создания виртуального корневого каталога IIS, из которого можно вызывать методы компонентов с помощью SOAP.</span><span class="sxs-lookup"><span data-stu-id="85b1f-106">You can use the Component Services administrative tool to create an IIS virtual root directory from which the component methods can be called by using SOAP.</span></span>

> [!Note]  
> <span data-ttu-id="85b1f-107">Чтобы предоставить приложение COM+ в качестве веб-службы XML, на компьютере должен быть установлен платформа .NET Framework.</span><span class="sxs-lookup"><span data-stu-id="85b1f-107">The .NET Framework must be installed on your computer in order to expose a COM+ application as an XML web service.</span></span>

 

<span data-ttu-id="85b1f-108">**Предоставление приложения COM+ в виде веб-службы XML**</span><span class="sxs-lookup"><span data-stu-id="85b1f-108">**To expose a COM+ application as an XML web service**</span></span>

1.  <span data-ttu-id="85b1f-109">В дереве консоли средства администрирования "службы компонентов" в разделе " **службы компонентов**" Откройте папку **приложения COM+** , связанную с компьютером, которым требуется управлять.</span><span class="sxs-lookup"><span data-stu-id="85b1f-109">In the console tree of the Component Services administrative tool, under **Component Services**, open the **COM+ Applications** folder associated with the computer you want to manage.</span></span>

2.  <span data-ttu-id="85b1f-110">Щелкните правой кнопкой мыши приложение, которое нужно предоставить в качестве веб-службы XML, и выберите пункт **Свойства**.</span><span class="sxs-lookup"><span data-stu-id="85b1f-110">Right-click the application you want to expose as an XML web service, and choose **Properties**.</span></span>

3.  <span data-ttu-id="85b1f-111">Откройте вкладку **Активация** в диалоговом окне Свойства.</span><span class="sxs-lookup"><span data-stu-id="85b1f-111">Click the **Activation** tab in the properties dialog.</span></span>

4.  <span data-ttu-id="85b1f-112">Установите флажок **использовать SOAP** .</span><span class="sxs-lookup"><span data-stu-id="85b1f-112">Select the **Uses SOAP** check box.</span></span>

5.  <span data-ttu-id="85b1f-113">В текстовом поле **SOAP vroot** введите имя виртуального корневого каталога IIS, из которого можно получить удаленный доступ к методам компонентов.</span><span class="sxs-lookup"><span data-stu-id="85b1f-113">In the **SOAP VRoot** text box, enter the name of the IIS virtual root directory from which the components methods can be accessed remotely.</span></span> <span data-ttu-id="85b1f-114">Обратите внимание, что VRoot SOAP не может быть подкаталогом другого каталога VRoot SOAP.</span><span class="sxs-lookup"><span data-stu-id="85b1f-114">Note that a SOAP VRoot cannot be a subdirectory of another SOAP VRoot directory.</span></span>

6.  <span data-ttu-id="85b1f-115">Нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="85b1f-115">Click **OK**.</span></span>

    <span data-ttu-id="85b1f-116">Если указать виртуальный корневой каталог IIS в виде *VRoot* , а полное доменное имя сервера — *ServerName*, то URL-адрес, по которому компонент будет представлен в виде веб-службы XML, будет HTTPS://*ServerName* / *VRoot*/.</span><span class="sxs-lookup"><span data-stu-id="85b1f-116">If you specify the IIS virtual root directory as *vroot* and if your servers fully qualified domain name is *servername*, the URL where your component is exposed as an XML web service is https://*servername*/*vroot*/.</span></span>

    <span data-ttu-id="85b1f-117">Соответствующий каталог в файловой системе — \\ Windows \\ system32 \\ COM \\ соапврутс \\ *VRoot* \\ ; COM+ помещает в него несколько файлов конфигурации и ASP.NET программы.</span><span class="sxs-lookup"><span data-stu-id="85b1f-117">The corresponding directory in your file system is \\windows\\system32\\com\\SoapVRoots\\*vroot*\\; COM+ places several configuration files and ASP.NET programs there.</span></span> <span data-ttu-id="85b1f-118">Для веб-службы XML при высокой нагрузке может потребоваться изменить параметры, хранящиеся в файле web.config. Сведения об этом файле см. в документации по службам IIS.</span><span class="sxs-lookup"><span data-stu-id="85b1f-118">For an XML web service under heavy load, you may want to adjust the parameters stored in the file web.config. For information about this file, consult the IIS documentation.</span></span>

    <span data-ttu-id="85b1f-119">Параметры безопасности по умолчанию для приложения COM+, предоставляемые в виде веб-службы XML, различаются в зависимости от установленной версии платформа .NET Framework.</span><span class="sxs-lookup"><span data-stu-id="85b1f-119">The default security settings for a COM+ application exposed as an XML web service differ depending on which version of the .NET Framework is installed.</span></span> <span data-ttu-id="85b1f-120">Если установлена версия 1,0, веб-службы XML по умолчанию являются небезопасными. все вызовы принимаются и шифрование не используется.</span><span class="sxs-lookup"><span data-stu-id="85b1f-120">If version 1.0 is installed, XML web services are nonsecure by default; all calls are accepted and no encryption is used.</span></span> <span data-ttu-id="85b1f-121">Если установлена версия 1,1 или более поздняя, веб-службы XML защищены по умолчанию. вызывающие объекты должны пройти проверку подлинности и обязательное шифрование.</span><span class="sxs-lookup"><span data-stu-id="85b1f-121">If version 1.1 or later is installed, XML web services are secure by default; callers must be authenticated and encryption is required.</span></span>

## <a name="related-topics"></a><span data-ttu-id="85b1f-122">См. также</span><span class="sxs-lookup"><span data-stu-id="85b1f-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="85b1f-123">Доступ к веб-службам XML в режиме Као</span><span class="sxs-lookup"><span data-stu-id="85b1f-123">Accessing XML Web Services in CAO Mode</span></span>](accessing-xml-web-services-in-cao-mode.md)
</dt> <dt>

[<span data-ttu-id="85b1f-124">Доступ к веб-службам XML в режиме ВКО</span><span class="sxs-lookup"><span data-stu-id="85b1f-124">Accessing XML Web Services in WKO Mode</span></span>](accessing-xml-web-services-in-wko-mode.md)
</dt> <dt>

[<span data-ttu-id="85b1f-125">Общие сведения о службе COM+ SOAP</span><span class="sxs-lookup"><span data-stu-id="85b1f-125">COM+ SOAP Service Overview</span></span>](com--soap-service-overview.md)
</dt> <dt>

[<span data-ttu-id="85b1f-126">Защита веб-служб XML</span><span class="sxs-lookup"><span data-stu-id="85b1f-126">Securing XML Web Services</span></span>](securing-xml-web-services.md)
</dt> </dl>

 

 



