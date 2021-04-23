---
title: Индивидуальное управление цифровыми правами
description: Индивидуальное управление цифровыми правами
ms.assetid: 8f129bc1-3db9-4b41-9d60-daff037237ff
keywords:
- Пакет SDK для Windows Media Format, индивидуальное управление цифровыми правами DRM
- Управление цифровыми правами (DRM), индивидуальность
- DRM (Управление цифровыми правами), индивидуальность
- индивидуальное управление цифровыми правами
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 217be5cb5c1c7abef882c28961439baa93011c29
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104329147"
---
# <a name="drm-individualization"></a><span data-ttu-id="e0a65-107">Индивидуальное управление цифровыми правами</span><span class="sxs-lookup"><span data-stu-id="e0a65-107">DRM Individualization</span></span>

<span data-ttu-id="e0a65-108">Владельцам защищенного содержимого могут потребоваться обновления некоторых компонентов управления цифровыми правами (DRM), включенных в пакет SDK Windows Media Format, перед обращением к их содержимому.</span><span class="sxs-lookup"><span data-stu-id="e0a65-108">Owners of protected content may require users to upgrade some of the digital rights management (DRM) components included in the Windows Media Format SDK before accessing their content.</span></span> <span data-ttu-id="e0a65-109">Если пользователь принимает обновление, отдельная версия файла безопасности (уникально для компьютера) будет скачана с веб-сайта корпорации Майкрософт.</span><span class="sxs-lookup"><span data-stu-id="e0a65-109">If a user accepts the upgrade, an individualized version of a security file (one unique to their computer) will be downloaded from a Microsoft Web site.</span></span> <span data-ttu-id="e0a65-110">Если пользователь отклоняет обновление, он не сможет получить доступ к содержимому. Тем не менее они по-прежнему смогут обращаться к незащищенному содержимому и защищенному содержимому, которое не требует обновления.</span><span class="sxs-lookup"><span data-stu-id="e0a65-110">If the user declines the upgrade, they will not be able to access the content; however, they will still be able to access unprotected content and protected content that does not require the upgrade.</span></span> <span data-ttu-id="e0a65-111">Выполнение обновления системы безопасности позволяет повысить уровень защиты, предлагаемый DRM.</span><span class="sxs-lookup"><span data-stu-id="e0a65-111">Performing a security upgrade helps increase the level of protection offered by DRM.</span></span>

<span data-ttu-id="e0a65-112">Индивидуальная настройка может выполняться либо во время установки, либо когда приложение впервые встречает защищенный ASF-файл, требующий этого.</span><span class="sxs-lookup"><span data-stu-id="e0a65-112">Individualization can be done either at setup time or when an application first encounters a protected ASF file that requires it.</span></span> <span data-ttu-id="e0a65-113">Поскольку этот процесс изменяет системные компоненты пользователя, приложение должно уведомить пользователя и получить информированное согласие перед выполнением обновления.</span><span class="sxs-lookup"><span data-stu-id="e0a65-113">Because this process modifies a user's system components, the application must notify the user and obtain their informed consent before performing the upgrade.</span></span> <span data-ttu-id="e0a65-114">Например, проигрыватель Microsoft Windows Media отображает диалоговое окно со следующим текстом:</span><span class="sxs-lookup"><span data-stu-id="e0a65-114">Microsoft Windows Media Player, for example, shows a dialog box with the following text:</span></span>

<span data-ttu-id="e0a65-115">**Требуется обновление системы безопасности**</span><span class="sxs-lookup"><span data-stu-id="e0a65-115">**Security Upgrade Required**</span></span>

<span data-ttu-id="e0a65-116">**Владелец защищенного содержимого, к которому вы пытаетесь получить доступ, требует сначала обновить некоторые компоненты Microsoft Digital Rights Management (DRM) на вашем компьютере.**</span><span class="sxs-lookup"><span data-stu-id="e0a65-116">**The owner of the protected content you are trying to access requires you to first upgrade some of the Microsoft digital rights management (DRM) components on your computer.**</span></span>

<span data-ttu-id="e0a65-117">**Нажмите кнопку ОК, чтобы обновить компоненты DRM.**</span><span class="sxs-lookup"><span data-stu-id="e0a65-117">**Click OK to upgrade your DRM components.**</span></span>

<span data-ttu-id="e0a65-118">**Дополнительно**</span><span class="sxs-lookup"><span data-stu-id="e0a65-118">**Details:**</span></span>

<span data-ttu-id="e0a65-119">**После нажатия кнопки ОК в службу Microsoft в Интернете отправляются уникальный идентификатор и файл безопасности DRM. Файл заменяется настроенной версией, содержащей уникальный идентификатор. Это повышает уровень защиты, обеспечиваемый DRM.**</span><span class="sxs-lookup"><span data-stu-id="e0a65-119">**When you click OK, a unique identifier and a DRM security file are sent to a Microsoft service on the Internet. The file is replaced with a customized version that contains your unique identifier. This increases the level of protection provided by DRM.**</span></span>

<span data-ttu-id="e0a65-120">Любое приложение, поддерживающее индивидуальную установку, должно использовать те же или похожие слова.</span><span class="sxs-lookup"><span data-stu-id="e0a65-120">Any application that supports individualization should use the same or similar wording.</span></span> <span data-ttu-id="e0a65-121">Дополнительные сведения о политике конфиденциальности корпорации Майкрософт см. в разделе заявление [о конфиденциальности](privacy-statement.md) этой документации.</span><span class="sxs-lookup"><span data-stu-id="e0a65-121">For more information on Microsoft's Privacy Policy, see the [Privacy Statement](privacy-statement.md) section of this documentation.</span></span>

> [!Note]  
> <span data-ttu-id="e0a65-122">DRM не поддерживает версию этого пакета SDK на базе x64.</span><span class="sxs-lookup"><span data-stu-id="e0a65-122">DRM is not supported by the x64-based version of this SDK.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="e0a65-123">См. также</span><span class="sxs-lookup"><span data-stu-id="e0a65-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e0a65-124">**Функции цифровых Rights Management**</span><span class="sxs-lookup"><span data-stu-id="e0a65-124">**Digital Rights Management Features**</span></span>](digital-rights-management-features.md)
</dt> <dt>

[<span data-ttu-id="e0a65-125">**Приложения DRM индивидуализинг**</span><span class="sxs-lookup"><span data-stu-id="e0a65-125">**Individualizing DRM Applications**</span></span>](individualizing-drm-applications.md)
</dt> </dl>

 

 




