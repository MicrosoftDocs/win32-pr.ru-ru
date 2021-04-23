---
description: Доступом к приложениям COM+, предоставляемым в виде веб-служб XML, управляет веб-сервер IIS, который обрабатывает входящие запросы.
ms.assetid: 440b0636-8afc-4fb3-a179-140958948b94
title: Защита веб-служб XML
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 94953ce0769c44ddaeda27cacdac99ab4ff252d5
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105701275"
---
# <a name="securing-xml-web-services"></a><span data-ttu-id="25b6c-103">Защита веб-служб XML</span><span class="sxs-lookup"><span data-stu-id="25b6c-103">Securing XML Web Services</span></span>

<span data-ttu-id="25b6c-104">Доступом к приложениям COM+, предоставляемым в виде веб-служб XML, управляет веб-сервер IIS, который обрабатывает входящие запросы.</span><span class="sxs-lookup"><span data-stu-id="25b6c-104">Access to COM+ applications exposed as XML web services is controlled by the IIS web server, which processes the incoming requests.</span></span> <span data-ttu-id="25b6c-105">Можно также настроить службы IIS так, чтобы они требовали взаимодействия с вызывающей стороной по защищенному каналу, установленному с помощью протокола SSL (SSL).</span><span class="sxs-lookup"><span data-stu-id="25b6c-105">You can also configure IIS to require the communications with the caller take place over a secure channel established using the Secure Sockets Layer (SSL) protocol.</span></span>

> [!Note]  
> <span data-ttu-id="25b6c-106">Защищенная веб-служба XML не поддерживает ВКО доступ через WSDL.</span><span class="sxs-lookup"><span data-stu-id="25b6c-106">A secured XML web service does not support WKO access via WSDL.</span></span> <span data-ttu-id="25b6c-107">Вместо этого клиенты, которые установили платформа .NET Framework версии 1,1, могут вызывать ее в режиме Као.</span><span class="sxs-lookup"><span data-stu-id="25b6c-107">Instead, clients that have installed the .NET Framework version 1.1 can call it in CAO mode.</span></span> <span data-ttu-id="25b6c-108">Если сторонним клиентам требуется доступ к веб-службе XML через WSDL, необходимо разрешить анонимный доступ.</span><span class="sxs-lookup"><span data-stu-id="25b6c-108">If third-party clients need to access your XML web service via WSDL, you must allow anonymous access.</span></span>

 

> [!Note]  
> <span data-ttu-id="25b6c-109">Чтобы использовать протокол SSL для установления безопасного канала связи, необходимо получить и установить SSL-сертификат.</span><span class="sxs-lookup"><span data-stu-id="25b6c-109">To use the SSL protocol to establish a secure communication channel, you must obtain and install an SSL certificate.</span></span>

 

## <a name="component-services-administrative-tool"></a><span data-ttu-id="25b6c-110">Средство администрирования служб компонентов</span><span class="sxs-lookup"><span data-stu-id="25b6c-110">Component Services Administrative Tool</span></span>

<span data-ttu-id="25b6c-111">Чтобы выбрать механизм проверки подлинности для веб-службы XML, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="25b6c-111">To select the authentication mechanism for an XML web service, use the following steps:</span></span>

1.  <span data-ttu-id="25b6c-112">Щелкните правой кнопкой мыши значок **Мой компьютер** на рабочем столе и выберите пункт **Управление**.</span><span class="sxs-lookup"><span data-stu-id="25b6c-112">Right-click the **My Computer** icon on your desktop, and click **Manage**.</span></span>

2.  <span data-ttu-id="25b6c-113">В разделе **службы и приложения** и **Служба** IIS выберите значок, соответствующий виртуальному корневому каталогу для веб-службы XML.</span><span class="sxs-lookup"><span data-stu-id="25b6c-113">Under **Services and Applications** and **Internet Information Service**, locate the icon corresponding to the virtual root directory for your XML web service.</span></span> <span data-ttu-id="25b6c-114">Щелкните правой кнопкой мыши значок каталога и выберите пункт **Свойства**.</span><span class="sxs-lookup"><span data-stu-id="25b6c-114">Right-click the directory icon, and choose **Properties**.</span></span>

3.  <span data-ttu-id="25b6c-115">На вкладке **Безопасность каталога** диалогового окна Свойства выберите пункт **Проверка подлинности и управление доступом** и нажмите соответствующую кнопку **изменить** .</span><span class="sxs-lookup"><span data-stu-id="25b6c-115">On the **Directory Security** tab of the properties dialog, locate **Authentication and access control** and click the corresponding **Edit** button.</span></span>

4.  <span data-ttu-id="25b6c-116">В диалоговом окне **методы проверки подлинности** в разделе **доступ с проверкой подлинности** используйте флажки, чтобы выбрать механизмы проверки подлинности, которые вы хотите разрешить.</span><span class="sxs-lookup"><span data-stu-id="25b6c-116">In the **Authentication Methods** dialog box, under **Authenticated access**, use the check boxes to select the authentication mechanisms you wish to allow.</span></span> <span data-ttu-id="25b6c-117">Нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="25b6c-117">Click **OK**.</span></span>

    > [!Note]  
    > <span data-ttu-id="25b6c-118">Вы можете настроить службы IIS для проверки подлинности вызывающих объектов с помощью любого из следующих параметров в диалоговом окне **методы проверки подлинности** IIS: **Встроенная проверка** подлинности Windows, дайджест-проверка подлинности **для серверов доменов Windows**, обычная проверка подлинности **(пароль отправляется в виде открытого текста)** или **Проверка**</span><span class="sxs-lookup"><span data-stu-id="25b6c-118">You can configure IIS to authenticate callers by using any of the following options on the IIS **Authentication Methods** dialog: **Integrated Windows authentication**, **Digest authentication for Windows domain servers**, **Basic authentication (password is sent in clear text)**, or **.NET Passport authentication**.</span></span> <span data-ttu-id="25b6c-119">Можно также разрешить анонимный доступ.</span><span class="sxs-lookup"><span data-stu-id="25b6c-119">You can also allow anonymous access.</span></span>

     

5.  <span data-ttu-id="25b6c-120">В диалоговом окне Свойства нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="25b6c-120">In the properties dialog, click **OK**.</span></span>

<span data-ttu-id="25b6c-121">Чтобы разрешить небезопасный анонимный доступ к веб-службе XML, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="25b6c-121">To allow nonsecure, anonymous access to an XML web service, use the following steps:</span></span>

1.  <span data-ttu-id="25b6c-122">Щелкните правой кнопкой мыши значок **Мой компьютер** на рабочем столе и выберите пункт **Управление**.</span><span class="sxs-lookup"><span data-stu-id="25b6c-122">Right-click the **My Computer** icon on your desktop, and click **Manage**.</span></span>

2.  <span data-ttu-id="25b6c-123">В разделе **службы и приложения** и **Служба** IIS выберите значок, соответствующий виртуальному корневому каталогу для веб-службы XML.</span><span class="sxs-lookup"><span data-stu-id="25b6c-123">Under **Services and Applications** and **Internet Information Service**, locate the icon corresponding to the virtual root directory for your XML web service.</span></span> <span data-ttu-id="25b6c-124">Щелкните правой кнопкой мыши значок каталога и выберите пункт **Свойства**.</span><span class="sxs-lookup"><span data-stu-id="25b6c-124">Right-click the directory icon, and choose **Properties**.</span></span>

3.  <span data-ttu-id="25b6c-125">На вкладке **Безопасность каталога** диалогового окна Свойства выберите пункт **Проверка подлинности и управление доступом** и нажмите соответствующую кнопку **изменить** .</span><span class="sxs-lookup"><span data-stu-id="25b6c-125">On the **Directory Security** tab of the properties dialog, locate **Authentication and access control** and click the corresponding **Edit** button.</span></span> <span data-ttu-id="25b6c-126">Установите флажок **включить анонимный доступ** .</span><span class="sxs-lookup"><span data-stu-id="25b6c-126">Select the **Enable anonymous access** check box.</span></span> <span data-ttu-id="25b6c-127">Нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="25b6c-127">Click **OK**.</span></span>

4.  <span data-ttu-id="25b6c-128">На вкладке **Безопасность каталога** диалогового окна Свойства выберите пункт **безопасные подключения** и нажмите соответствующую кнопку **изменить** .</span><span class="sxs-lookup"><span data-stu-id="25b6c-128">On the **Directory Security** tab of the properties dialog, locate **Secure communications** and click the corresponding **Edit** button.</span></span> <span data-ttu-id="25b6c-129">Снимите флажок **обязательное использование безопасного канала (SSL)** .</span><span class="sxs-lookup"><span data-stu-id="25b6c-129">Uncheck the **Require secure channel (SSL)** check box.</span></span> <span data-ttu-id="25b6c-130">Нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="25b6c-130">Click **OK**.</span></span>

5.  <span data-ttu-id="25b6c-131">В диалоговом окне Свойства нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="25b6c-131">In the properties dialog, click **OK**.</span></span>

## <a name="visual-basic"></a><span data-ttu-id="25b6c-132">Visual Basic</span><span class="sxs-lookup"><span data-stu-id="25b6c-132">Visual Basic</span></span>

<span data-ttu-id="25b6c-133">Не применяется.</span><span class="sxs-lookup"><span data-stu-id="25b6c-133">Does not apply.</span></span>

## <a name="cc"></a><span data-ttu-id="25b6c-134">C/C++</span><span class="sxs-lookup"><span data-stu-id="25b6c-134">C/C++</span></span>

<span data-ttu-id="25b6c-135">Не применяется.</span><span class="sxs-lookup"><span data-stu-id="25b6c-135">Does not apply.</span></span>

## <a name="additional-security-considerations"></a><span data-ttu-id="25b6c-136">Дополнительные вопросы безопасности</span><span class="sxs-lookup"><span data-stu-id="25b6c-136">Additional Security Considerations</span></span>

<span data-ttu-id="25b6c-137">Запросив безопасный канал, вы помогаете защитить конфиденциальность данных путем шифрования обмена данными между клиентом и веб-службой XML.</span><span class="sxs-lookup"><span data-stu-id="25b6c-137">By requiring a secure channel, you help protect the confidentiality of the data exchanged by encrypting the communications between the client and your XML web service.</span></span> <span data-ttu-id="25b6c-138">Если вы разрешаете проверку подлинности с помощью незашифрованных текстовых паролей, необходимо использовать безопасный канал, чтобы предотвратить предоставление доступа к паролям в сети.</span><span class="sxs-lookup"><span data-stu-id="25b6c-138">If you allow authentication using clear text passwords, you should require a secure channel in order to avoid exposing passwords on the network.</span></span>

## <a name="related-topics"></a><span data-ttu-id="25b6c-139">См. также</span><span class="sxs-lookup"><span data-stu-id="25b6c-139">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="25b6c-140">Доступ к веб-службам XML в режиме Као</span><span class="sxs-lookup"><span data-stu-id="25b6c-140">Accessing XML Web Services in CAO Mode</span></span>](accessing-xml-web-services-in-cao-mode.md)
</dt> <dt>

[<span data-ttu-id="25b6c-141">Доступ к веб-службам XML в режиме ВКО</span><span class="sxs-lookup"><span data-stu-id="25b6c-141">Accessing XML Web Services in WKO Mode</span></span>](accessing-xml-web-services-in-wko-mode.md)
</dt> <dt>

[<span data-ttu-id="25b6c-142">Вопросы безопасности службы COM+ SOAP</span><span class="sxs-lookup"><span data-stu-id="25b6c-142">COM+ SOAP Service Security Considerations</span></span>](com--soap-service-security-considerations.md)
</dt> <dt>

[<span data-ttu-id="25b6c-143">Создание веб-служб XML</span><span class="sxs-lookup"><span data-stu-id="25b6c-143">Creating XML Web Services</span></span>](creating-xml-web-services.md)
</dt> </dl>

 

 



