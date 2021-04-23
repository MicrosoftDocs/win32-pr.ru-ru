---
title: Модель защищенного звукового пути (не рекомендуется)
description: Модель защищенного звукового пути (не рекомендуется)
ms.assetid: 8854411a-d917-497b-9c10-4c29bcb7832b
keywords:
- Пакет SDK для формата Windows Media, Microsoft Secure Audio Path (SAP)
- Управление цифровыми правами (DRM), Microsoft Secure Audio Path (SAP)
- DRM (Управление цифровыми правами), Microsoft Secure Audio Path (SAP)
- Windows Media Format SDK, защищенный звуковой путь (SAP)
- Управление цифровыми правами (DRM), защищенный звуковой путь (SAP)
- DRM (Управление цифровыми правами), безопасный звуковой путь (SAP)
- Microsoft Secure Audio Path (SAP), модель
- Защищенный звуковой путь (SAP), модель
- SAP (безопасный звуковой путь), модель
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aee21d05113deb3c4e8d64141374c87da090f41c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104410845"
---
# <a name="the-secure-audio-path-model-deprecated"></a><span data-ttu-id="74afd-112">Модель защищенного звукового пути (не рекомендуется)</span><span class="sxs-lookup"><span data-stu-id="74afd-112">The Secure Audio Path Model (deprecated)</span></span>

<span data-ttu-id="74afd-113">На этой странице документируется функция, которая будет поддерживаться с другим техническим решением в будущих версиях Windows.</span><span class="sxs-lookup"><span data-stu-id="74afd-113">This page documents a feature that will be supported with a different technical solution in future versions of Windows.</span></span>

<span data-ttu-id="74afd-114">Microsoft Secure Audio Path (SAP) — это функция Microsoft Windows® Me и Microsoft Windows XP.</span><span class="sxs-lookup"><span data-stu-id="74afd-114">Microsoft Secure Audio Path (SAP) is a feature of Microsoft Windows® Me and Microsoft Windows XP.</span></span> <span data-ttu-id="74afd-115">Требование воспроизведения звукового файла только через защищенный звуковой путь указывается в лицензии DRM и обеспечивается клиентскими компонентами DRM.</span><span class="sxs-lookup"><span data-stu-id="74afd-115">The requirement that an audio file be played only through a secure audio path is specified in the DRM license and enforced by the DRM client components.</span></span> <span data-ttu-id="74afd-116">При первоначальной защите файлов только для SAP не добавляется дополнительное шифрование.</span><span class="sxs-lookup"><span data-stu-id="74afd-116">There is no extra encryption added for SAP-only files when they are initially protected.</span></span> <span data-ttu-id="74afd-117">Шифрование SAP автоматически добавляется компонентами DRM во время воспроизведения, как и процесс проверки подлинности для всех компонентов программного обеспечения, участвующих в воспроизведении.</span><span class="sxs-lookup"><span data-stu-id="74afd-117">The SAP encryption is added automatically by the DRM components at playback time, as is the authentication process for all software components involved in playback.</span></span> <span data-ttu-id="74afd-118">Таким образом, работа SAP полностью прозрачна для приложений, поэтому в пакете SDK для Windows Media Format нет метода или свойства для включения или отключения SAP.</span><span class="sxs-lookup"><span data-stu-id="74afd-118">The workings of SAP are therefore completely transparent to applications, and that is why there is no method or property in the Windows Media Format SDK for enabling or disabling SAP.</span></span> <span data-ttu-id="74afd-119">При необходимости при создании защищенного файла владелец содержимого может добавить атрибут пользовательского заголовка с именем нечто вроде "Дрмхеадер. Сапрекуиред", чтобы указать серверу лицензий добавить требование SAP к лицензии.</span><span class="sxs-lookup"><span data-stu-id="74afd-119">If desired, when creating a protected file a content owner can add a custom header attribute called something like "DRMHeader.SAPRequired" in order to instruct a license server to add the SAP requirement to the license.</span></span> <span data-ttu-id="74afd-120">Реализация такой схемы связана с владельцем содержимого и службой лицензирования.</span><span class="sxs-lookup"><span data-stu-id="74afd-120">The implementation of such a scheme is up to the content owner and the license service.</span></span>

<span data-ttu-id="74afd-121">Если в текущей модели DRM не применяется SAP, то при воспроизведении защищенной цифровой музыки зашифрованное содержимое передается в клиентский компонент DRM.</span><span class="sxs-lookup"><span data-stu-id="74afd-121">In the current DRM model, if SAP is not applied, when protected digital music is played, the encrypted content passes to the DRM client component.</span></span> <span data-ttu-id="74afd-122">Клиент DRM проверяет, что приложение и компонент DRM, включающий пакет SDK для формата Windows Media, являются допустимыми.</span><span class="sxs-lookup"><span data-stu-id="74afd-122">The DRM client verifies that the application and the DRM component incorporating the Windows Media Format SDK are valid.</span></span> <span data-ttu-id="74afd-123">Если они допустимы, клиент DRM расшифровывает содержимое и отправляет его в приложение, которое затем отправляет его в звуковые компоненты нижнего уровня.</span><span class="sxs-lookup"><span data-stu-id="74afd-123">If they are valid, the DRM client decrypts the content and sends it to the application, which then sends it to the lower-level audio components.</span></span> <span data-ttu-id="74afd-124">На этом этапе Расшифрованная музыка доступна приложениям пользовательского режима, подключаемым модулям и драйверам режима ядра, которые могут перехватывать расшифрованные звуковые биты.</span><span class="sxs-lookup"><span data-stu-id="74afd-124">At this point, the decrypted music is available to user mode applications and plug-ins and kernel mode drivers that can intercept the decrypted audio bits.</span></span>

<span data-ttu-id="74afd-125">При применении требования к защищенному звуковому пути содержимое не расшифровывается приложением, а передается в зашифрованное состояние в компоненты более низкого уровня, все из которых прошло проверку подлинности Майкрософт в качестве надежного.</span><span class="sxs-lookup"><span data-stu-id="74afd-125">When the Secure Audio Path requirement is applied, the content is not decrypted by the application, but rather is passed in an encrypted state to lower level components, all of which have been authenticated by Microsoft as trustworthy.</span></span> <span data-ttu-id="74afd-126">Надежный звуковой компонент — это тот, который не делает звуковое содержимое доступным для любого системного компонента, кроме других конкретных доверенных компонентов.</span><span class="sxs-lookup"><span data-stu-id="74afd-126">A trusted audio component is one that does not make the audio content available to any system component except other specific trusted components.</span></span> <span data-ttu-id="74afd-127">Таким образом, цифровое содержимое остается защищенным вплоть до уровня драйвера.</span><span class="sxs-lookup"><span data-stu-id="74afd-127">In this way, the digital content remains protected all the way down to the driver level.</span></span>

<span data-ttu-id="74afd-128">На следующей схеме показана текущая модель в сравнении с моделью защищенного звукового пути.</span><span class="sxs-lookup"><span data-stu-id="74afd-128">The following diagram displays the current model in comparison to the Secure Audio Path model.</span></span>

![Схема модели защищенного звукового пути](images/sap.png)

 

 




