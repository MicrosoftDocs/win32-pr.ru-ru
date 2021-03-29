---
description: Взаимодействие с устаревшими API аудио
ms.assetid: 34939f6d-a6e4-4f7a-afa3-b1fed52b471f
title: Взаимодействие с устаревшими API аудио
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4a6b9a80b55695ffcfd3ac54e871f00ea27744d8
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103990692"
---
# <a name="interoperability-with-legacy-audio-apis"></a><span data-ttu-id="e7b4e-103">Взаимодействие с устаревшими API аудио</span><span class="sxs-lookup"><span data-stu-id="e7b4e-103">Interoperability with Legacy Audio APIs</span></span>

<span data-ttu-id="e7b4e-104">Многие существующие приложения используют устаревшие аудио API, такие как DirectSound, DirectShow и функции мультимедиа Windows.</span><span class="sxs-lookup"><span data-stu-id="e7b4e-104">Many existing applications use legacy audio APIs such as DirectSound, DirectShow, and the Windows multimedia functions.</span></span> <span data-ttu-id="e7b4e-105">Благодаря незначительным изменениям эти приложения можно дополнить, чтобы использовать [роли устройств](device-roles.md), [элементы управления громкостью](session-volume-controls.md)и другие функции основных API-интерфейсов аудио в Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="e7b4e-105">With only minor modifications, these applications can be augmented to make use of [device roles](device-roles.md), [session volume controls](session-volume-controls.md), and other features of the core audio APIs in Windows Vista.</span></span>

<span data-ttu-id="e7b4e-106">Как обсуждалось в [пользовательских компонентах аудио](user-mode-audio-components.md), основные API-интерфейсы используются в качестве основы, на которой строятся аудио API более высокого уровня.</span><span class="sxs-lookup"><span data-stu-id="e7b4e-106">As discussed in [User-Mode Audio Components](user-mode-audio-components.md), the core audio APIs serve as the foundation on which higher-level audio APIs are built.</span></span> <span data-ttu-id="e7b4e-107">В Windows Vista звуковые устройства, к которым приложения обращаются через устаревшие API аудио, такие как DirectSound, и функции Windows Media **вавеауткскскс** и **вавеинкскскс** , на самом деле являются [устройствами конечных точек аудио](audio-endpoint-devices.md) , реализованными основными API-интерфейсами аудио.</span><span class="sxs-lookup"><span data-stu-id="e7b4e-107">In Windows Vista, the audio devices that applications access through legacy audio APIs such as DirectSound and the Windows media **waveOutXxx** and **waveInXxx** functions are, in fact, [audio endpoint devices](audio-endpoint-devices.md) that are implemented by the core audio APIs.</span></span> <span data-ttu-id="e7b4e-108">Из-за встроенных ограничений интерфейсов устаревших API аудио приложение может получить доступ к некоторым, но не всем возможностям устройств конечных точек звука через эти интерфейсы.</span><span class="sxs-lookup"><span data-stu-id="e7b4e-108">Because of inherent limitations in the interfaces of legacy audio APIs, an application can access some but not all of the capabilities of audio endpoint devices through these interfaces.</span></span> <span data-ttu-id="e7b4e-109">В следующих разделах описываются методы улучшения существующих приложений за счет доступа к дополнительным возможностям устройств конечных точек звука непосредственно через основные API-интерфейсы аудио.</span><span class="sxs-lookup"><span data-stu-id="e7b4e-109">The following sections describe techniques for enhancing existing applications by accessing additional capabilities of audio endpoint devices directly through the core audio APIs.</span></span> <span data-ttu-id="e7b4e-110">Для этих улучшений обычно требуется внести незначительные изменения в существующий код приложения.</span><span class="sxs-lookup"><span data-stu-id="e7b4e-110">These enhancements typically require only minor changes to the existing application code.</span></span>

<span data-ttu-id="e7b4e-111">В следующих разделах описывается включение функций основных API аудио в существующие приложения, использующие устаревшие API аудио:</span><span class="sxs-lookup"><span data-stu-id="e7b4e-111">The following sections describe how to incorporate features of the core audio APIs into existing applications that use legacy audio APIs:</span></span>

-   [<span data-ttu-id="e7b4e-112">Роли устройств для приложений DirectSound</span><span class="sxs-lookup"><span data-stu-id="e7b4e-112">Device Roles for DirectSound Applications</span></span>](device-roles-for-directsound-applications.md)
-   [<span data-ttu-id="e7b4e-113">Роли устройств для приложений DirectShow</span><span class="sxs-lookup"><span data-stu-id="e7b4e-113">Device Roles for DirectShow Applications</span></span>](device-roles-for-directshow-applications.md)
-   [<span data-ttu-id="e7b4e-114">Роли устройств для устаревших приложений мультимедиа Windows</span><span class="sxs-lookup"><span data-stu-id="e7b4e-114">Device Roles for Legacy Windows Multimedia Applications</span></span>](device-roles-for-legacy-windows-multimedia-applications.md)
-   [<span data-ttu-id="e7b4e-115">События аудио для устаревших звуковых приложений</span><span class="sxs-lookup"><span data-stu-id="e7b4e-115">Audio Events for Legacy Audio Applications</span></span>](audio-events-for-legacy-audio-applications.md)
-   [<span data-ttu-id="e7b4e-116">Звуковые сигналы уведомлений для устаревших звуковых приложений</span><span class="sxs-lookup"><span data-stu-id="e7b4e-116">Notification Sounds for Legacy Audio Applications</span></span>](notification-sounds-for-legacy-audio-applications.md)

## <a name="related-topics"></a><span data-ttu-id="e7b4e-117">См. также</span><span class="sxs-lookup"><span data-stu-id="e7b4e-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e7b4e-118">Роли устройств</span><span class="sxs-lookup"><span data-stu-id="e7b4e-118">Device Roles</span></span>](device-roles.md)
</dt> </dl>

 

 



