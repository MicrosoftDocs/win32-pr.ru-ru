---
description: В следующем разделе описывается работа API платформы оценки Windows как службы (WaaS).
ms.assetid: B107AAF3-4248-40EF-ABD2-C5B31602AEF7
title: Сведения о платформе оценки WaaS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bb96dd27fdc5b8838f2e2a26e74f0046eda8f20b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105663503"
---
# <a name="about-the-waas-assessment-platform"></a><span data-ttu-id="bf8d5-103">Сведения о платформе оценки WaaS</span><span class="sxs-lookup"><span data-stu-id="bf8d5-103">About the WaaS Assessment Platform</span></span>

<span data-ttu-id="bf8d5-104">В следующем разделе описывается работа API платформы оценки Windows как службы (WaaS).</span><span class="sxs-lookup"><span data-stu-id="bf8d5-104">The following topic describes how the Windows as a Service (WaaS) Assessment Platform API works.</span></span>

<span data-ttu-id="bf8d5-105">API оценки WaaS предоставляет вызывающей стороне следующие сведения:</span><span class="sxs-lookup"><span data-stu-id="bf8d5-105">The WaaS Assessment API offers the caller the following information:</span></span>

-   <span data-ttu-id="bf8d5-106">Если устройство находится на последних обновлениях Майкрософт.</span><span class="sxs-lookup"><span data-stu-id="bf8d5-106">If a device is on the latest Microsoft updates.</span></span>
-   <span data-ttu-id="bf8d5-107">Достигло ли устройство поддержки.</span><span class="sxs-lookup"><span data-stu-id="bf8d5-107">Whether the device has reached end of support.</span></span>
-   <span data-ttu-id="bf8d5-108">Время выпуска последних применимых обновлений для устройства.</span><span class="sxs-lookup"><span data-stu-id="bf8d5-108">The release times for the latest applicable updates for the device.</span></span>
-   <span data-ttu-id="bf8d5-109">Оценка причины, по которой устройство не является актуальным, и потенциальное воздействие на него на устройстве.</span><span class="sxs-lookup"><span data-stu-id="bf8d5-109">An assessment of why a device is not up-to-date and the potential impact it may have on the device.</span></span>

<span data-ttu-id="bf8d5-110">Платформа оценки WaaS использует модель COM API и запускается автоматически по крайней мере один раз в день.</span><span class="sxs-lookup"><span data-stu-id="bf8d5-110">The WaaS Assessment Platform uses the COM API model and runs automatically at least once a day.</span></span> <span data-ttu-id="bf8d5-111">Этот цикл перехватывает применимые сведения о выпуске.</span><span class="sxs-lookup"><span data-stu-id="bf8d5-111">This cycle catches applicable release information.</span></span> <span data-ttu-id="bf8d5-112">В течение кэшированного периода выполняется оценка для кэшированной информации о выпуске.</span><span class="sxs-lookup"><span data-stu-id="bf8d5-112">During the cached period, assessments are made against the cached release information.</span></span> <span data-ttu-id="bf8d5-113">Если вызов выполняется за пределами окна срока действия кэша, выполняется новый вызов и оценка, кэшируется и возвращается.</span><span class="sxs-lookup"><span data-stu-id="bf8d5-113">If a call is made outside of the cache expiration window, a fresh call and assessment is made, cached, and returned.</span></span> <span data-ttu-id="bf8d5-114">Когда выполняется вызов, клиент оценки WaaS обращается к службе оценки WaaS с атрибутами устройства и получает доссиер информации, применимой к устройству.</span><span class="sxs-lookup"><span data-stu-id="bf8d5-114">When a call is made, the WaaS Assessment Client contacts the WaaS Assessment Service with the device's attributes, and receives back a dossier of information applicable to the device.</span></span> <span data-ttu-id="bf8d5-115">Затем клиент использует эти сведения в отношении информации, собираемой на устройстве для выполнения оценки.</span><span class="sxs-lookup"><span data-stu-id="bf8d5-115">The client then uses this information against the information it gathers about the device to perform the assessment.</span></span>

> [!NOTE]
> <span data-ttu-id="bf8d5-116">Ваш код должен иметь права администратора для вызова API оценки WAAS.</span><span class="sxs-lookup"><span data-stu-id="bf8d5-116">Your code must have administrator privileges to call the Waas Assessment API.</span></span> <span data-ttu-id="bf8d5-117">Дополнительные сведения о разработке приложений, требующих прав администратора, см. в [этой статье](../secauthz/developing-applications-that-require-administrator-privilege.md).</span><span class="sxs-lookup"><span data-stu-id="bf8d5-117">For more details about developing applications that require administrator privileges, see [this article](../secauthz/developing-applications-that-require-administrator-privilege.md).</span></span>

 
