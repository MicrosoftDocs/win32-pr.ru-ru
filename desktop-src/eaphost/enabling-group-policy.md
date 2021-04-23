---
title: Включение групповая политика
description: Узнайте, как настроить этот метод, включив групповую политику. См. раздел рекомендации по отправителей запросов и Просмотр дополнительных доступных ресурсов.
ms.assetid: ac04b83b-1322-41d4-85e0-93687f10a7f6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: af7b57e736bf078068156f6aff10d294621749a2
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/21/2020
ms.locfileid: "104413772"
---
# <a name="enabling-group-policy"></a><span data-ttu-id="1720f-104">Включение групповая политика</span><span class="sxs-lookup"><span data-stu-id="1720f-104">Enabling Group Policy</span></span>

<span data-ttu-id="1720f-105">В этом разделе объясняется, как настроить вызывающий объект, включив групповую политику.</span><span class="sxs-lookup"><span data-stu-id="1720f-105">This topic explains how to configure the supplicant by enabling group policy.</span></span> <span data-ttu-id="1720f-106">EAPHost отправителей запросов может участвовать в групповой политике, чтобы администратор сети мог централизованно настраивать свои сетевые компьютеры.</span><span class="sxs-lookup"><span data-stu-id="1720f-106">EAPHost supplicants can participate in group policy to allow a network administrator to centrally configure their network machines.</span></span>

<span data-ttu-id="1720f-107">Точный метод и механизм, с помощью которых запрашивающая сторона принимает участие в групповой политике, — это по усмотрению запрашивающей стороны.</span><span class="sxs-lookup"><span data-stu-id="1720f-107">The precise method and mechanism by which the supplicant chooses to participate in group policy is at the discretion of the supplicant.</span></span> <span data-ttu-id="1720f-108">Примеры механизмов для участия в групповой политике включают расширения клиент-сервер, административный шаблон и т. д.</span><span class="sxs-lookup"><span data-stu-id="1720f-108">Examples of mechanisms for group policy participation include client/server-side extensions, administrative template, and so forth.</span></span>

## <a name="considerations-when-enabling-group-policy"></a><span data-ttu-id="1720f-109">Рекомендации по включению групповая политика</span><span class="sxs-lookup"><span data-stu-id="1720f-109">Considerations When Enabling Group Policy</span></span>

<span data-ttu-id="1720f-110">Ниже приведены рекомендации по отправителей запросов в отношении групповой политики и EAP.</span><span class="sxs-lookup"><span data-stu-id="1720f-110">These are the considerations for supplicants with respect to group policy and EAP.</span></span>

1.  <span data-ttu-id="1720f-111">Конфигурация EAP всегда должна храниться в формате XML везде, где это возможно, а не в двоичном формате.</span><span class="sxs-lookup"><span data-stu-id="1720f-111">EAP configuration should always be stored as XML whenever possible and not in the binary format.</span></span> <span data-ttu-id="1720f-112">Групповая политика может быть применена к любому компьютеру в домене, а конфигурация метода EAP и данные пользователя не гарантированно переносимы между архитектурой 32-разрядных и 64-разрядных процессоров.</span><span class="sxs-lookup"><span data-stu-id="1720f-112">Group policy may be applied to any machine in the domain, and EAP method configuration and user data are not guaranteed to be portable between 32-bit and 64-bit processor architectures.</span></span> <span data-ttu-id="1720f-113">XML разрешает проблемы с границами архитектуры процессора, так как запрашивающая сторона локально преобразует независимый XML-код архитектуры процессора в двоичное представление конфигурации во время проверки подлинности.</span><span class="sxs-lookup"><span data-stu-id="1720f-113">XML resolves the processor architecture boundary issues as the supplicant locally converts the processor-architecture independent XML to the binary representation of the configuration at authentication time.</span></span>

    <span data-ttu-id="1720f-114">Дополнительные сведения см. в следующих разделах:</span><span class="sxs-lookup"><span data-stu-id="1720f-114">For more information, see the following topics.</span></span>

    -   [<span data-ttu-id="1720f-115">Общие часто задаваемые вопросы</span><span class="sxs-lookup"><span data-stu-id="1720f-115">General Frequently Asked Questions</span></span>](general-frequently-asked-questions.md)
    -   <span data-ttu-id="1720f-116">[Метод EAP часто задаваемые вопросы](eap-method-frequently-asked-questions.md).</span><span class="sxs-lookup"><span data-stu-id="1720f-116">[EAP Method Frequently Asked Questions](eap-method-frequently-asked-questions.md).</span></span>
    -   [<span data-ttu-id="1720f-117">**EapHostPeerConfigXml2Blob**</span><span class="sxs-lookup"><span data-stu-id="1720f-117">**EapHostPeerConfigXml2Blob**</span></span>](/previous-versions/windows/desktop/api/eaphostpeerconfigapis/nf-eaphostpeerconfigapis-eaphostpeerconfigxml2blob)
    -   [<span data-ttu-id="1720f-118">**EapHostPeerCredentialsXml2Blob**</span><span class="sxs-lookup"><span data-stu-id="1720f-118">**EapHostPeerCredentialsXml2Blob**</span></span>](/previous-versions/windows/desktop/api/eaphostpeerconfigapis/nf-eaphostpeerconfigapis-eaphostpeercredentialsxml2blob)

2.  <span data-ttu-id="1720f-119">Если используется расширение на стороне сервера групповой политики, то расширение будет вызывать [**еафостпиржетмесодс**](/previous-versions/windows/desktop/api/eaphostpeerconfigapis/nf-eaphostpeerconfigapis-eaphostpeergetmethods) , как правило, для определения доступных методов и создания соответствующей конфигурации EAP для этой политики.</span><span class="sxs-lookup"><span data-stu-id="1720f-119">If a group policy server-side extension is used, the extension will call [**EapHostPeerGetMethods**](/previous-versions/windows/desktop/api/eaphostpeerconfigapis/nf-eaphostpeerconfigapis-eaphostpeergetmethods) typically to determine available methods and to generate appropriate EAP configuration for that policy.</span></span> <span data-ttu-id="1720f-120">Затем политика отправляется на соответствующие сетевые клиенты, где применяется политика.</span><span class="sxs-lookup"><span data-stu-id="1720f-120">The policy is then pushed out to appropriate network clients where the policy is applied.</span></span>

## <a name="related-topics"></a><span data-ttu-id="1720f-121">См. также</span><span class="sxs-lookup"><span data-stu-id="1720f-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1720f-122">Настройка пользовательского интерфейса метода EAP</span><span class="sxs-lookup"><span data-stu-id="1720f-122">Configuring the EAP Method User Interface</span></span>](configuring-the-eap-method-user-interface.md)
</dt> <dt>

[<span data-ttu-id="1720f-123">Реализация поддержки NAP In-Band для методов EAP</span><span class="sxs-lookup"><span data-stu-id="1720f-123">Implementing In-Band NAP Support for EAP Methods</span></span>](enabling-in-band-nap-support.md)
</dt> <dt>

[<span data-ttu-id="1720f-124">Реализация поддержки NAP для методов EAP</span><span class="sxs-lookup"><span data-stu-id="1720f-124">Implementing NAP Support for EAP Methods</span></span>](implementing-nap-for-eap-methods.md)
</dt> <dt>

[<span data-ttu-id="1720f-125">Передача данных между запрашивающим и методами EAP</span><span class="sxs-lookup"><span data-stu-id="1720f-125">Transferring Data Between the Supplicant and EAP Methods</span></span>](transferring-data-between-the-supplicant-and-eap-methods.md)
</dt> <dt>

[<span data-ttu-id="1720f-126">EAPHost отправителей запросов</span><span class="sxs-lookup"><span data-stu-id="1720f-126">EAPHost Supplicants</span></span>](eaphost-supplicants.md)
</dt> </dl>

 

 




