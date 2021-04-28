---
description: Устранение неполадок Windows
ms.assetid: fb2c487a-d395-45eb-9010-936a61a414d0
title: Устранение неполадок Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ff332afe1b586b05866d78b49013a264e815f3eb
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108088562"
---
# <a name="windows-troubleshooting"></a><span data-ttu-id="be37a-103">Устранение неполадок Windows</span><span class="sxs-lookup"><span data-stu-id="be37a-103">Windows Troubleshooting</span></span>

## <a name="affected-platforms"></a><span data-ttu-id="be37a-104">Затронутые платформы</span><span class="sxs-lookup"><span data-stu-id="be37a-104">Affected Platforms</span></span>

<span data-ttu-id="be37a-105">**Клиенты** — Windows 7</span><span class="sxs-lookup"><span data-stu-id="be37a-105">**Clients** - Windows 7</span></span>  
<span data-ttu-id="be37a-106">**Серверы** — Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="be37a-106">**Servers** - Windows Server 2008 R2</span></span>  









## <a name="description"></a><span data-ttu-id="be37a-107">Описание</span><span class="sxs-lookup"><span data-stu-id="be37a-107">Description</span></span>

<span data-ttu-id="be37a-108">Новый центр поддержки Windows 7 (прежнее название — центр решений), устранение неполадок Windows, предоставляет систематическую процедуру устранения неполадок для пользователя.</span><span class="sxs-lookup"><span data-stu-id="be37a-108">A new Windows 7 Action Center (formerly known as Solutions Center) feature, Windows Troubleshooting, delivers a systematic troubleshooting experience for the user.</span></span> <span data-ttu-id="be37a-109">Центр действий — один из пяти значков, закрепленных в систрай.</span><span class="sxs-lookup"><span data-stu-id="be37a-109">The Action Center is one of the five icons pinned in the systray.</span></span> <span data-ttu-id="be37a-110">Устранение неполадок в Windows позволяет просматривать и искать встроенные пакеты устранения неполадок, а также устранять неполадки пакетов, которые хранятся на сервере Microsoft в Интернете — лучше при подключении (БВК).</span><span class="sxs-lookup"><span data-stu-id="be37a-110">Windows Troubleshooting allows you to browse or search for in-box troubleshooting packs and for troubleshooting packs that are stored on a Microsoft server on the Internet – a Better When Connected (BWC) experience.</span></span> <span data-ttu-id="be37a-111">Можно выбрать и запустить пакет устранения неполадок, чтобы попытаться устранить проблему.</span><span class="sxs-lookup"><span data-stu-id="be37a-111">You can select and run a troubleshooting pack to attempt to resolve their problem.</span></span> <span data-ttu-id="be37a-112">Если не удается определить разрешение проблемы, вы можете найти справку, содержимое сообщества, статьи о поддержке или другие пакеты устранения неполадок для соответствующего связанного содержимого.</span><span class="sxs-lookup"><span data-stu-id="be37a-112">If you cannot identify a resolution to the problem, you have the option of searching help, community content, and support articles, or other troubleshooting packs for relevant related content.</span></span> <span data-ttu-id="be37a-113">Если не предоставить ответ на проблему, можно восстановить компьютер до момента возникновения проблемы или получить помощь через удаленный помощник.</span><span class="sxs-lookup"><span data-stu-id="be37a-113">Should that not provide an answer to the problem, you can restore the PC to a time prior to when the problem occurred or get help through remote assistance.</span></span> <span data-ttu-id="be37a-114">Цель — позволить легко и быстро найти решение проблемы.</span><span class="sxs-lookup"><span data-stu-id="be37a-114">The intent is to allow you to find a solution to the problem easily and quickly.</span></span>

## <a name="usage"></a><span data-ttu-id="be37a-115">Использование</span><span class="sxs-lookup"><span data-stu-id="be37a-115">Usage</span></span>

<span data-ttu-id="be37a-116">Центр действий четко видим и доступен из нескольких расположений.</span><span class="sxs-lookup"><span data-stu-id="be37a-116">The Action Center is clearly visible and available from several locations.</span></span> <span data-ttu-id="be37a-117">Вы можете запустить его из контекстного меню центра действий в систрай на панели управления в качестве ярлыка в разделе "система и обслуживание", на главной странице центра действий и из содержимого справки.</span><span class="sxs-lookup"><span data-stu-id="be37a-117">You can launch it from the context menu of the Action Center in the systray, from the control panel as a shortcut link under system and maintenance, from the main page of the Action Center, and from Help content.</span></span>

<span data-ttu-id="be37a-118">Устранение неполадок пакетов основано на сценариях PowerShell.</span><span class="sxs-lookup"><span data-stu-id="be37a-118">Troubleshooting packs are based upon powershell scripts.</span></span> <span data-ttu-id="be37a-119">Процесс создания и публикации пакета устранения неполадок будет сделан общедоступным, чтобы позволить поставщикам вычислительной техники, независимым поставщикам программного обеспечения и ИТ-специалистам разрабатывать и поставлять собственные материалы по устранению неполадок.</span><span class="sxs-lookup"><span data-stu-id="be37a-119">The process of authoring and publishing a troubleshooting pack will be made public to allow OEMs, IHVs, ISVs, and IT Professionals to develop and ship their own troubleshooting content.</span></span>

<span data-ttu-id="be37a-120">Для обеспечения единообразного взаимодействия с пользователем обязательно следуйте рекомендациям и рекомендациям, описанным в разделе Инструментарий по устранению неполадок Windows, при проектировании собственных пакетов устранения неполадок.</span><span class="sxs-lookup"><span data-stu-id="be37a-120">For a consistent user experience, be sure to follow the best practices and guidelines described in the Windows troubleshooting toolkit when designing your own troubleshooting packs.</span></span>

 

 



