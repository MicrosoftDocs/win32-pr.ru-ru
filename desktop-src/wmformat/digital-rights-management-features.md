---
title: Функции цифровых Rights Management
description: Функции цифровых Rights Management
ms.assetid: c3c1e59f-8ff9-496c-8e63-0c1cf4ce7092
keywords:
- Windows Media Format SDK, функции DRM
- Управление цифровыми правами (DRM), функции
- DRM (Управление цифровыми правами), функции
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9bd9c30b350fdf430d5b20bbe112c5309ac9da4f
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "103792157"
---
# <a name="digital-rights-management-features"></a><span data-ttu-id="82ba9-106">Функции цифровых Rights Management</span><span class="sxs-lookup"><span data-stu-id="82ba9-106">Digital Rights Management Features</span></span>

<span data-ttu-id="82ba9-107">\[Компонент Windows Media DRM является устаревшим и не должен использоваться.</span><span class="sxs-lookup"><span data-stu-id="82ba9-107">\[The Windows Media DRM feature is deprecated and should not be used.</span></span> <span data-ttu-id="82ba9-108">Вместо этого используйте [Microsoft PlayReady](/windows/uwp/audio-video-camera/playready-client-sdk) .\]</span><span class="sxs-lookup"><span data-stu-id="82ba9-108">Use [Microsoft PlayReady](/windows/uwp/audio-video-camera/playready-client-sdk) instead.\]</span></span>

<span data-ttu-id="82ba9-109">Управление цифровыми правами (DRM) — это технология, которую владельцы содержимого могут использовать для защиты цифровых файлов мультимедиа путем их шифрования с помощью ключа (фрагмента данных, который блокирует и разблокирует содержимое).</span><span class="sxs-lookup"><span data-stu-id="82ba9-109">Digital rights management (DRM) is a technology that content owners can use to protect digital media files by encrypting them with a key (a piece of data that locks and unlocks the content).</span></span> <span data-ttu-id="82ba9-110">Чтобы воспроизвести защищенный ASF-файл, потребитель должен получить отдельную лицензию, содержащую ключ.</span><span class="sxs-lookup"><span data-stu-id="82ba9-110">To play a protected ASF file, a consumer must obtain a separate license containing the key.</span></span> <span data-ttu-id="82ba9-111">Каждая лицензия также содержит права, определяемые владельцем содержимого или издателем лицензий, которые определяют, как потребитель может использовать этот файл.</span><span class="sxs-lookup"><span data-stu-id="82ba9-111">Each license also contains rights, determined by the content owner or license issuer, which specify how the consumer can use the file.</span></span> <span data-ttu-id="82ba9-112">С помощью технологии DRM владельцы содержимого могут предоставлять песни, видео и другие цифровые файлы мультимедиа через Интернет в защищенном формате файлов и управлять использованием их цифрового содержимого.</span><span class="sxs-lookup"><span data-stu-id="82ba9-112">Using DRM technology, content owners can deliver songs, videos, and other digital media files over the Internet in a protected file format and control the use of their digital content.</span></span> <span data-ttu-id="82ba9-113">Технология Microsoft DRM также поддерживается диспетчером прав Windows Media, кодировщиком Windows Media и проигрывателем Windows Media.</span><span class="sxs-lookup"><span data-stu-id="82ba9-113">Microsoft DRM technology is also supported by the Windows Media Rights Manager, the Windows Media Encoder, and Windows Media Player.</span></span> <span data-ttu-id="82ba9-114">Дополнительные сведения о технологии DRM корпорации Майкрософт см. на [веб-сайте Microsoft Windows Media](https://support.microsoft.com/help/17946/windows-media).</span><span class="sxs-lookup"><span data-stu-id="82ba9-114">For more background information on Microsoft's DRM technology, see the [Microsoft Windows Media Web site](https://support.microsoft.com/help/17946/windows-media).</span></span>

> [!Note]  
> <span data-ttu-id="82ba9-115">DRM не поддерживает версию этого пакета SDK на базе x64.</span><span class="sxs-lookup"><span data-stu-id="82ba9-115">DRM is not supported by the x64-based version of this SDK.</span></span>

 

<span data-ttu-id="82ba9-116">В следующих разделах обсуждаются основные функции DRM, относящиеся к Windows Media Format SDK.</span><span class="sxs-lookup"><span data-stu-id="82ba9-116">The following sections discuss the main DRM-related features of the Windows Media Format SDK.</span></span>



| <span data-ttu-id="82ba9-117">Section</span><span class="sxs-lookup"><span data-stu-id="82ba9-117">Section</span></span>                                                                                            | <span data-ttu-id="82ba9-118">Описание</span><span class="sxs-lookup"><span data-stu-id="82ba9-118">Description</span></span>                                                                                                                          |
|----------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="82ba9-119">Основы DRM</span><span class="sxs-lookup"><span data-stu-id="82ba9-119">DRM Basics</span></span>](drm-basics.md)                                                                       | <span data-ttu-id="82ba9-120">Содержит краткий обзор функциональных возможностей DRM, предоставляемых пакетом SDK Windows Media Format.</span><span class="sxs-lookup"><span data-stu-id="82ba9-120">Provides a brief overview of the DRM functionality provided by the Windows Media Format SDK.</span></span>                                         |
| [<span data-ttu-id="82ba9-121">Версии DRM</span><span class="sxs-lookup"><span data-stu-id="82ba9-121">DRM Versions</span></span>](drm-versions.md)                                                                   | <span data-ttu-id="82ba9-122">Описание основных различий между версиями защиты DRM, доступными для приложений.</span><span class="sxs-lookup"><span data-stu-id="82ba9-122">Describes the main differences between the versions of DRM protection available to applications.</span></span>                                     |
| [<span data-ttu-id="82ba9-123">Live DRM</span><span class="sxs-lookup"><span data-stu-id="82ba9-123">Live DRM</span></span>](live-drm.md)                                                                           | <span data-ttu-id="82ba9-124">Описание сценариев, которые можно выполнить с помощью "на лету" защиты DRM.</span><span class="sxs-lookup"><span data-stu-id="82ba9-124">Describes the scenarios made possible by "on the fly" DRM protection.</span></span>                                                                |
| [<span data-ttu-id="82ba9-125">Индивидуальное управление цифровыми правами</span><span class="sxs-lookup"><span data-stu-id="82ba9-125">DRM Individualization</span></span>](drm-individualization.md)                                                 | <span data-ttu-id="82ba9-126">Описывает обновление безопасности приложения, которое могут потребоваться владельцам содержимого DRM или поставщикам лицензий.</span><span class="sxs-lookup"><span data-stu-id="82ba9-126">Describes the application security upgrade that DRM content owners or license issuers can require.</span></span>                                   |
| [<span data-ttu-id="82ba9-127">Резервное копирование и восстановление лицензий DRM</span><span class="sxs-lookup"><span data-stu-id="82ba9-127">Backing Up and Restoring of DRM Licenses</span></span>](backing-up-and-restoring-of-drm-licenses.md)           | <span data-ttu-id="82ba9-128">Описание достоинств и недостатков, позволяющих пользователям создавать резервные копии и восстанавливать лицензии на содержимое.</span><span class="sxs-lookup"><span data-stu-id="82ba9-128">Describes the pros and cons of permitting users to back up and restore their content licenses.</span></span>                                       |
| [<span data-ttu-id="82ba9-129">Просмотр атрибутов DRM в редакторе метаданных</span><span class="sxs-lookup"><span data-stu-id="82ba9-129">Viewing DRM Attributes in the Metadata Editor</span></span>](viewing-drm-attributes-in-the-metadata-editor.md) | <span data-ttu-id="82ba9-130">Описание возможностей этого вспомогательного объекта DRM и сценариев, для которых он предназначен для поддержки.</span><span class="sxs-lookup"><span data-stu-id="82ba9-130">Describes the capabilities of this DRM helper object and the scenarios it was designed to support.</span></span>                                   |
| [<span data-ttu-id="82ba9-131">Уровни защиты выходных данных</span><span class="sxs-lookup"><span data-stu-id="82ba9-131">Output Protection Levels</span></span>](output-protection-levels.md)                                           | <span data-ttu-id="82ba9-132">Описывает, как уровни защиты выходных данных делают лицензии DRM версии 10 более гибкими.</span><span class="sxs-lookup"><span data-stu-id="82ba9-132">Describes how Output Protection Levels make DRM version 10 licenses more flexible.</span></span>                                                   |
| [<span data-ttu-id="82ba9-133">Отзыв лицензий</span><span class="sxs-lookup"><span data-stu-id="82ba9-133">License Revocation</span></span>](license-revocation.md)                                                       | <span data-ttu-id="82ba9-134">Описание отзыва лицензий.</span><span class="sxs-lookup"><span data-stu-id="82ba9-134">Describes license revocation.</span></span>                                                                                                        |
| [<span data-ttu-id="82ba9-135">Windows Media DRM 10 для сетевых устройств</span><span class="sxs-lookup"><span data-stu-id="82ba9-135">Windows Media DRM 10 for Network Devices</span></span>](windows-media-drm-10-for-network-devices.md)           | <span data-ttu-id="82ba9-136">Представляет Windows Media DRM 10 для сетевых устройств и его реализацию в этом пакете SDK.</span><span class="sxs-lookup"><span data-stu-id="82ba9-136">Introduces Windows Media DRM 10 for Network Devices and its implementation in this SDK.</span></span>                                              |
| [<span data-ttu-id="82ba9-137">Путь безопасного аудио (Майкрософт)</span><span class="sxs-lookup"><span data-stu-id="82ba9-137">Microsoft Secure Audio Path</span></span>](microsoft-secure-audio-path--deprecated.md)                         | <span data-ttu-id="82ba9-138">Описывает архитектуру Microsoft Secure Audio Path, которая обеспечивает наивысшую степень защиты защищенного аудио содержимого.</span><span class="sxs-lookup"><span data-stu-id="82ba9-138">Describes the Microsoft Secure Audio Path architecture, which provides the highest degree of protection for protected audio content.</span></span> |
| [<span data-ttu-id="82ba9-139">Запись списка воспроизведения</span><span class="sxs-lookup"><span data-stu-id="82ba9-139">Playlist Burning</span></span>](playlist-burning.md)                                                           | <span data-ttu-id="82ba9-140">Описание функции записи списка воспроизведения в DRM и ее поддержки в пакете SDK формата Windows Media.</span><span class="sxs-lookup"><span data-stu-id="82ba9-140">Describes the playlist-burning feature of DRM and how it is supported in the Windows Media Format SDK.</span></span>                               |



 

## <a name="related-topics"></a><span data-ttu-id="82ba9-141">См. также</span><span class="sxs-lookup"><span data-stu-id="82ba9-141">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="82ba9-142">**Включение поддержки DRM**</span><span class="sxs-lookup"><span data-stu-id="82ba9-142">**Enabling DRM Support**</span></span>](enabling-drm-support.md)
</dt> <dt>

[<span data-ttu-id="82ba9-143">**Компоненты**</span><span class="sxs-lookup"><span data-stu-id="82ba9-143">**Features**</span></span>](features.md)
</dt> </dl>

 

 