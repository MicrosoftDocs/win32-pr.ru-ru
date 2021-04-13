---
description: Звуковые сигналы уведомлений для устаревших звуковых приложений
ms.assetid: c5ad67d9-56fb-4bf0-aea4-5b49b0e5bf95
title: Звуковые сигналы уведомлений для устаревших звуковых приложений
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0e9ee2ef1155694e32a21779c55d290da6b3799c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104539005"
---
# <a name="notification-sounds-for-legacy-audio-applications"></a><span data-ttu-id="30427-103">Звуковые сигналы уведомлений для устаревших звуковых приложений</span><span class="sxs-lookup"><span data-stu-id="30427-103">Notification Sounds for Legacy Audio Applications</span></span>

<span data-ttu-id="30427-104">В Windows Vista операционная система назначит все свои звуки системного уведомления для межпроцессного звукового сеанса, который воспроизводится через устройство конечной точки отрисовки, которое в настоящее время назначено [роли устройства](device-roles.md)еконсоле.</span><span class="sxs-lookup"><span data-stu-id="30427-104">In Windows Vista, the operating system assigns all of its system notification sounds to a cross-process audio session that plays through the rendering endpoint device that is currently assigned to the eConsole [device role](device-roles.md).</span></span> <span data-ttu-id="30427-105">В программе системного управления громкостью, Сндвол, отображается ползунок громкости, выделенный для звуковых уведомлений системы.</span><span class="sxs-lookup"><span data-stu-id="30427-105">The system volume-control program, Sndvol, displays a volume slider that is dedicated to system notification sounds.</span></span>

<span data-ttu-id="30427-106">Некоторые приложения воспроизводят звуки уведомлений.</span><span class="sxs-lookup"><span data-stu-id="30427-106">Some applications play notification sounds.</span></span> <span data-ttu-id="30427-107">Вместо того, чтобы требовать от пользователя управлять звуковыми сигналами приложения через отдельный ползунок громкости в Сндвол, приложение может назначить звуки уведомлений тому же сеансу, что и системное уведомление.</span><span class="sxs-lookup"><span data-stu-id="30427-107">Instead of requiring the user to manage an application's notification sounds through a separate volume slider in Sndvol, the application can assign its notification sounds to the same session as the system notification sounds.</span></span> <span data-ttu-id="30427-108">Ползунок Сндвол Volume, управляющий системным уведомлением, затем управляет звуковыми уведомлениями из приложения.</span><span class="sxs-lookup"><span data-stu-id="30427-108">The Sndvol volume slider that controls the system notification sounds then controls the notification sounds from the application.</span></span>

<span data-ttu-id="30427-109">Чтобы обеспечить такое поведение, Windows Vista определяет \_ системный флаг snd для устаревшей функции [**PlaySound**](/previous-versions//dd743680(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="30427-109">To enable this behavior, Windows Vista defines a SND\_SYSTEM flag for the legacy [**PlaySound**](/previous-versions//dd743680(v=vs.85)) function.</span></span> <span data-ttu-id="30427-110">(Этот флаг не поддерживается в более ранних версиях Windows, включая Windows Server 2003, Windows XP и Windows 2000.) Если вызывающий объект устанавливает этот флаг, функция **PlaySound** назначает воспроизводимый им звук в межпроцессный сеанс, который используется операционной системой для звуковых оповещений.</span><span class="sxs-lookup"><span data-stu-id="30427-110">(This flag is not supported in earlier versions of Windows, including Windows Server 2003, Windows XP, and Windows 2000.) If the caller sets this flag, then the **PlaySound** function assigns the sound that it plays to the cross-process session that the operating system uses for its notification sounds.</span></span> <span data-ttu-id="30427-111">Если вызывающий объект не устанавливает флаг, то метод **PlaySound** назначает воспроизводимый им звук в сеансе по умолчанию — сеанс конкретного процесса, ОПРЕДЕЛЯЕМый идентификатором GUID GUID значения \_ null.</span><span class="sxs-lookup"><span data-stu-id="30427-111">If the caller does not set the flag, then **PlaySound** assigns the sound that it plays to the default session—the process-specific session that is identified by the session GUID value GUID\_NULL.</span></span> <span data-ttu-id="30427-112">\_Система snd определена в файле заголовка ммсистем. h.</span><span class="sxs-lookup"><span data-stu-id="30427-112">SND\_SYSTEM is defined in the header file Mmsystem.h.</span></span> <span data-ttu-id="30427-113">Дополнительные сведения о **PlaySound** см. в документации по Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="30427-113">For more information about **PlaySound**, see the Windows SDK documentation.</span></span>

## <a name="related-topics"></a><span data-ttu-id="30427-114">См. также</span><span class="sxs-lookup"><span data-stu-id="30427-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="30427-115">Взаимодействие с устаревшими API аудио</span><span class="sxs-lookup"><span data-stu-id="30427-115">Interoperability with Legacy Audio APIs</span></span>](interoperability-with-legacy-audio-apis.md)
</dt> </dl>

 

 
