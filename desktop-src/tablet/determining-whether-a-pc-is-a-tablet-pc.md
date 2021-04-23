---
description: Иногда может потребоваться определить, работает ли приложение на планшетном ПК, так как может потребоваться, чтобы ваши приложения могли использовать встроенные возможности рукописного ввода, распознавания и пера.
ms.assetid: 86a3eddb-6541-4b73-b2ca-6adedad1a1e5
title: Определение того, является ли компьютер планшетным ПК
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c793d5531d6091d4bce73d99bfa32d100c2b9304
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105712627"
---
# <a name="determining-whether-a-pc-is-a-tablet-pc"></a><span data-ttu-id="4f05b-103">Определение того, является ли компьютер планшетным ПК</span><span class="sxs-lookup"><span data-stu-id="4f05b-103">Determining Whether a PC is a Tablet PC</span></span>

<span data-ttu-id="4f05b-104">Иногда может потребоваться определить, работает ли приложение на планшетном ПК, так как может потребоваться, чтобы ваши приложения могли использовать встроенные возможности рукописного ввода, распознавания и пера.</span><span class="sxs-lookup"><span data-stu-id="4f05b-104">You may occasionally need to determine whether your application is running on a Tablet PC because you may want your applications to take advantage of inherent ink, recognition, and pen capabilities.</span></span> <span data-ttu-id="4f05b-105">Чтобы определить, имеет ли приложение доступ к функциям Tablet PC, можно использовать вызов Windows API Жетсистемметрикс (), как описано в этом разделе.</span><span class="sxs-lookup"><span data-stu-id="4f05b-105">To help you determine whether your application has access to the Tablet PC features, you can use the GetSystemMetrics() Windows API call as described in this topic.</span></span>

## <a name="client-side-applications"></a><span data-ttu-id="4f05b-106">Client-Side приложения</span><span class="sxs-lookup"><span data-stu-id="4f05b-106">Client-Side Applications</span></span>

<span data-ttu-id="4f05b-107">Чтобы определить, работает ли код на планшетном ПК, можно использовать следующие методы.</span><span class="sxs-lookup"><span data-stu-id="4f05b-107">You can use the following techniques to determine whether your code is running on a Tablet PC.</span></span>

-   [<span data-ttu-id="4f05b-108">Использование Жетсистемметрикс (SM \_ TABLETPC)</span><span class="sxs-lookup"><span data-stu-id="4f05b-108">Using GetSystemMetrics (SM\_TABLETPC)</span></span>](/windows)
-   [<span data-ttu-id="4f05b-109">Использование двоичных файлов платформы планшетов</span><span class="sxs-lookup"><span data-stu-id="4f05b-109">Using the Presence of Tablet Platform Binaries</span></span>](#using-the-presence-of-tablet-platform-binaries)
-   [<span data-ttu-id="4f05b-110">Веб-приложения</span><span class="sxs-lookup"><span data-stu-id="4f05b-110">Web-Based Applications</span></span>](#web-based-applications)

### <a name="using-getsystemmetrics-sm_tabletpc"></a><span data-ttu-id="4f05b-111">Использование Жетсистемметрикс (SM \_ TABLETPC)</span><span class="sxs-lookup"><span data-stu-id="4f05b-111">Using GetSystemMetrics (SM\_TABLETPC)</span></span>

### <a name="windows-xp-tablet-pc-edition"></a><span data-ttu-id="4f05b-112">Windows XP Tablet PC Edition</span><span class="sxs-lookup"><span data-stu-id="4f05b-112">Windows XP Tablet PC Edition</span></span>

<span data-ttu-id="4f05b-113">В Microsoft Windows XP Tablet PC Edition используйте функцию Жетсистемметрикс (SM \_ TABLETPC), чтобы определить, является ли компьютер планшетным ПК.</span><span class="sxs-lookup"><span data-stu-id="4f05b-113">In Microsoft Windows XP Tablet PC Edition, use the GetSystemMetrics(SM\_TABLETPC) function to determine whether a computer is a Tablet PC.</span></span> <span data-ttu-id="4f05b-114">Жетсистемметрикс (SM \_ TABLETPC) позволяет возвращать значение true на компьютере под управлением Windows XP Tablet PC Edition.</span><span class="sxs-lookup"><span data-stu-id="4f05b-114">GetSystemMetrics(SM\_TABLETPC) is designed to return TRUE on a computer running Windows XP Tablet PC Edition.</span></span>

### <a name="windows-vista"></a><span data-ttu-id="4f05b-115">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="4f05b-115">Windows Vista</span></span>

<span data-ttu-id="4f05b-116">В Windows Vista больше не существует отдельного пакета SDK для планшетных ПК.</span><span class="sxs-lookup"><span data-stu-id="4f05b-116">In Windows Vista, there is no longer a distinct Tablet PC SDK.</span></span> <span data-ttu-id="4f05b-117">Windows SDK теперь содержит раздел с названием "планшетный ПК и технология сенсорного ввода", а логика Жетсистемметрикс (SM \_ TABLETPC) изменилась, чтобы отразить это.</span><span class="sxs-lookup"><span data-stu-id="4f05b-117">The Windows SDK now contains a section called "Tablet PC and Touch Technology" and the logic of GetSystemMetrics(SM\_TABLETPC) has been changed to reflect this.</span></span> <span data-ttu-id="4f05b-118">Жетсистемметрикс (SM \_ TABLETPC) теперь возвращает значение true, если выполняются все приведенные ниже условия.</span><span class="sxs-lookup"><span data-stu-id="4f05b-118">GetSystemMetrics(SM\_TABLETPC) now returns true if all of the following are true:</span></span>

-   <span data-ttu-id="4f05b-119">В системе имеется интегрированный дигитайзер, либо перо, либо сенсорный ввод.</span><span class="sxs-lookup"><span data-stu-id="4f05b-119">There is an integrated digitizer, either pen or touch, on the system.</span></span>
-   <span data-ttu-id="4f05b-120">Установлен необязательный компонент Tablet PC.</span><span class="sxs-lookup"><span data-stu-id="4f05b-120">The Tablet PC optional component is installed.</span></span> <span data-ttu-id="4f05b-121">Этот компонент содержит такие функции, как панель ввода Tablet PC и журнал Windows.</span><span class="sxs-lookup"><span data-stu-id="4f05b-121">This component contains features such as Tablet PC Input Panel and Windows Journal.</span></span>
-   <span data-ttu-id="4f05b-122">Компьютер лицензирован для использования дополнительного компонента.</span><span class="sxs-lookup"><span data-stu-id="4f05b-122">The computer is licensed to use the optional component.</span></span> <span data-ttu-id="4f05b-123">Версии Premium Windows Vista, такие как Windows Vista Home Premium, Windows Vista для малого бизнеса, Windows Vista Professional, Windows Vista Enterprise и Windows Vista Ultimate, имеют лицензию на использование дополнительного компонента.</span><span class="sxs-lookup"><span data-stu-id="4f05b-123">Premium versions of Windows Vista—such as Windows Vista Home Premium, Windows Vista Small Business, Windows Vista Professional, Windows Vista Enterprise, and Windows Vista Ultimate—are licensed to use the optional component.</span></span>
-   <span data-ttu-id="4f05b-124">Служба ввода Tablet PC запущена.</span><span class="sxs-lookup"><span data-stu-id="4f05b-124">Tablet PC Input Service is running.</span></span> <span data-ttu-id="4f05b-125">Служба ввода Tablet PC — это новая служба для Windows Vista, которая управляет вводом на планшетном ПК.</span><span class="sxs-lookup"><span data-stu-id="4f05b-125">Tablet PC Input Service is a new service for Windows Vista that controls Tablet PC input.</span></span>

<span data-ttu-id="4f05b-126">Благодаря этой повышенной точности Жетсистемметрикс (SM \_ TABLETPC) остается рекомендуемым способом определить, является ли компьютер, работающий под управлением Windows Vista, планшетным ПК.</span><span class="sxs-lookup"><span data-stu-id="4f05b-126">With this increased accuracy, GetSystemMetrics(SM\_TABLETPC) continues to be the recommended way to determine whether a computer running Windows Vista is a Tablet PC.</span></span>

### <a name="using-the-presence-of-tablet-platform-binaries"></a><span data-ttu-id="4f05b-127">Использование двоичных файлов платформы планшетов</span><span class="sxs-lookup"><span data-stu-id="4f05b-127">Using the Presence of Tablet Platform Binaries</span></span>

<span data-ttu-id="4f05b-128">В Windows XP Tablet PC Edition и Windows Vista можно искать наличие двоичных файлов рукописного ввода, таких как inkobj.dll и Microsoft.Ink.dll, и использовать их поддерживаемые функции, если они есть.</span><span class="sxs-lookup"><span data-stu-id="4f05b-128">In both Windows XP Tablet PC Edition and Windows Vista, you can search for the presence of the ink binaries—such as inkobj.dll and Microsoft.Ink.dll—and use their supported functionality if they are present.</span></span>

<span data-ttu-id="4f05b-129">В Windows Vista двоичные файлы платформы Tablet PC устанавливаются во всех клиентских версиях по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="4f05b-129">In Windows Vista, the Tablet PC Platform binaries are installed on all client versions by default.</span></span> <span data-ttu-id="4f05b-130">В этих версиях доступны функции входа и рукописного ввода.</span><span class="sxs-lookup"><span data-stu-id="4f05b-130">Input and inking functionality are available on those versions.</span></span> <span data-ttu-id="4f05b-131">Распознавание доступно только в версии Premium Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="4f05b-131">Recognition is available only in premium versions of Windows Vista.</span></span>

### <a name="web-based-applications"></a><span data-ttu-id="4f05b-132">Web-Based приложения</span><span class="sxs-lookup"><span data-stu-id="4f05b-132">Web-Based Applications</span></span>

<span data-ttu-id="4f05b-133">В Windows Vista строка агента пользователя, сообщаемая в Internet Explorer, включает "Tablet PC 2,0", если в соответствии с Жетсистемметрикс (SM \_ TABLETPC) устройство является планшетным ПК.</span><span class="sxs-lookup"><span data-stu-id="4f05b-133">In Windows Vista, the user-agent string reported by Internet Explorer includes "Tablet PC 2.0" if, according to GetSystemMetrics(SM\_TABLETPC), the device is a Tablet PC.</span></span>

<span data-ttu-id="4f05b-134">В Windows XP Tablet PC Edition 2005 строка агента пользователя включает в себя Tablet PC 1,7.</span><span class="sxs-lookup"><span data-stu-id="4f05b-134">In Windows XP Tablet PC Edition 2005, the user-agent string includes Tablet PC 1.7.</span></span> <span data-ttu-id="4f05b-135">Строка агента пользователя выглядит примерно следующим образом:</span><span class="sxs-lookup"><span data-stu-id="4f05b-135">The user-agent string looks something like the following:</span></span>

`Mozilla/4.0 (compatible; MSIE 6.0; Windows NT 5.1; .NET CLR 1.0.3705; Tablet PC 2.0)`

<span data-ttu-id="4f05b-136">Используйте это значение, чтобы определить, является ли клиентский компьютер планшетом, и поддерживает веб-элементы управления рукописного ввода.</span><span class="sxs-lookup"><span data-stu-id="4f05b-136">Use this value to determine whether the client computer is a Tablet PC and supports Web-based inking controls.</span></span>

## <a name="related-topics"></a><span data-ttu-id="4f05b-137">См. также</span><span class="sxs-lookup"><span data-stu-id="4f05b-137">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4f05b-138">**жетсистемметрикс**</span><span class="sxs-lookup"><span data-stu-id="4f05b-138">**GetSystemMetrics**</span></span>](/windows/desktop/api/winuser/nf-winuser-getsystemmetrics)
</dt> </dl>

 

 
