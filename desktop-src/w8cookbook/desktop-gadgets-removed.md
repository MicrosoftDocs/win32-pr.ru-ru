---
title: Мини-приложения рабочего стола удалены
description: Мини-приложения рабочего стола удалены
ms.assetid: 0074204B-F568-4F9B-A0F7-3E330B91E4CD
keywords:
- приложения
- мини-приложения рабочего стола
- Боковая панель Windows
- Боковая панель
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5c37c058a75aca82d7727566041af4c30f3bb474
ms.sourcegitcommit: ea4baf9953a78d2d6bd530b680601e39f3884541
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/01/2020
ms.locfileid: "104413912"
---
# <a name="desktop-gadgets-removed"></a><span data-ttu-id="5fb64-107">Мини-приложения рабочего стола удалены</span><span class="sxs-lookup"><span data-stu-id="5fb64-107">Desktop gadgets removed</span></span>

## <a name="platforms"></a><span data-ttu-id="5fb64-108">Платформы</span><span class="sxs-lookup"><span data-stu-id="5fb64-108">Platforms</span></span>

 <span data-ttu-id="5fb64-109">**Клиенты** — Windows 8</span><span class="sxs-lookup"><span data-stu-id="5fb64-109">**Clients** - Windows 8</span></span>  
<span data-ttu-id="5fb64-110">**Серверы** — Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="5fb64-110">**Servers** - Windows Server 2012</span></span>  



## <a name="description"></a><span data-ttu-id="5fb64-111">Описание</span><span class="sxs-lookup"><span data-stu-id="5fb64-111">Description</span></span>

<span data-ttu-id="5fb64-112">С точки зрения функциональности мини-приложения уже устарели и их классируют новые динамические плитки и приложения.</span><span class="sxs-lookup"><span data-stu-id="5fb64-112">From a functionality standpoint, Gadgets have already been deprecated and are outclassed by new live tiles and apps.</span></span> <span data-ttu-id="5fb64-113">Мини-приложения также представляют угрозу безопасности пользователям.</span><span class="sxs-lookup"><span data-stu-id="5fb64-113">Gadgets also present a security risk to users.</span></span> <span data-ttu-id="5fb64-114">В качестве платформы существуют уязвимости, которые могут использовать даже опасные мини-приложения.</span><span class="sxs-lookup"><span data-stu-id="5fb64-114">As a platform, vulnerabilities exist such that even benign Gadgets could be exploited.</span></span> <span data-ttu-id="5fb64-115">Поэтому, чтобы правилами Windows 8 в качестве самой современной и защищенной операционной системы, мы решили полностью удалить мини-приложения из операционной системы.</span><span class="sxs-lookup"><span data-stu-id="5fb64-115">Therefore, in order to uphold Windows 8 as our most modern and secure operating system, we have chosen to remove Gadgets from the operating system entirely.</span></span> <span data-ttu-id="5fb64-116">Пользователи Windows 7 с мини-приложениями на их рабочем столе получат уведомления, и мини-приложения будут удалены.</span><span class="sxs-lookup"><span data-stu-id="5fb64-116">Windows 7 users with Gadgets on their Desktop will be notified and Gadgets will be uninstalled.</span></span>

## <a name="manifestation"></a><span data-ttu-id="5fb64-117">Проявление</span><span class="sxs-lookup"><span data-stu-id="5fb64-117">Manifestation</span></span>

<span data-ttu-id="5fb64-118">Мини-приложения рабочего стола не будут доступны на рабочем столе Windows.</span><span class="sxs-lookup"><span data-stu-id="5fb64-118">Desktop Gadgets will not be available on the Windows Desktop.</span></span>

## <a name="mitigation"></a><span data-ttu-id="5fb64-119">Меры по снижению риска</span><span class="sxs-lookup"><span data-stu-id="5fb64-119">Mitigation</span></span>

<span data-ttu-id="5fb64-120">API-интерфейсы мини-приложений и структура папок на настольных компьютерах останутся на месте для Windows 8.</span><span class="sxs-lookup"><span data-stu-id="5fb64-120">The Desktop Gadgets API and folder structure will remain in place for Windows 8.</span></span> <span data-ttu-id="5fb64-121">Приложения, которые программно устанавливают и запускают мини-приложения с помощью этого API, продолжают работать без ошибок (хотя сами мини-приложения не будут выполняться).</span><span class="sxs-lookup"><span data-stu-id="5fb64-121">Applications which programmatically install and run Gadgets using this API will continue to run without fail (although the Gadgets themselves will not).</span></span>

## <a name="solution"></a><span data-ttu-id="5fb64-122">Решение</span><span class="sxs-lookup"><span data-stu-id="5fb64-122">Solution</span></span>

<span data-ttu-id="5fb64-123">Разработчикам классических приложений не следует упаковывать мини-приложения в свои установщики.</span><span class="sxs-lookup"><span data-stu-id="5fb64-123">Desktop app developers should not package Gadgets in their installers.</span></span> <span data-ttu-id="5fb64-124">Эти мини-приложения будут просто занимать место для пользователя и не смогут работать в системе.</span><span class="sxs-lookup"><span data-stu-id="5fb64-124">These Gadgets will just take up space for the user and will not be able to be run in the system.</span></span>

## <a name="tests"></a><span data-ttu-id="5fb64-125">Тесты</span><span class="sxs-lookup"><span data-stu-id="5fb64-125">Tests</span></span>

<span data-ttu-id="5fb64-126">Разработчики могут проверить совместимость этого изменения, отключив дополнительный компонент для мини-приложений рабочего стола в Windows 7.</span><span class="sxs-lookup"><span data-stu-id="5fb64-126">Developers are able to test compatibility of this change by disabling the optional component for Desktop Gadgets in Windows 7.</span></span> <span data-ttu-id="5fb64-127">Чтобы отключить мини-приложения на компьютере с Windows 7, выполните следующие действия:</span><span class="sxs-lookup"><span data-stu-id="5fb64-127">To disable Gadgets on a Windows 7 PC, follow the steps below:</span></span>

1.  <span data-ttu-id="5fb64-128">Перейдите к разделу Включение или отключение компонентов Windows на панели управления.</span><span class="sxs-lookup"><span data-stu-id="5fb64-128">Navigate to Turn Windows Features on or off from the Control Panel.</span></span>
2.  <span data-ttu-id="5fb64-129">Снимите флажок рядом с пунктом "платформа мини-приложений Windows".</span><span class="sxs-lookup"><span data-stu-id="5fb64-129">Uncheck the box next to “Windows Gadget Platform”.</span></span>
3.  <span data-ttu-id="5fb64-130">Нажмите кнопку ОК и следуйте дополнительным инструкциям на экране.</span><span class="sxs-lookup"><span data-stu-id="5fb64-130">Click OK and follow any additional on-screen instructions.</span></span>

## <a name="resources"></a><span data-ttu-id="5fb64-131">Ресурсы</span><span class="sxs-lookup"><span data-stu-id="5fb64-131">Resources</span></span>

[<span data-ttu-id="5fb64-132">Уязвимости в мини-приложениях делают возможным удаленный запуск программного кода</span><span class="sxs-lookup"><span data-stu-id="5fb64-132">Vulnerabilities in Gadgets Could Allow Remote Code Execution</span></span>](https://support.microsoft.com/kb/2719662)

 

 




