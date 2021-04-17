---
description: Родительский контроль Top-Level пользовательского интерфейса
ms.assetid: c6dfd3bc-191f-42d1-b9de-cc85a2da0a99
title: Родительский контроль Top-Level пользовательского интерфейса
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 321475097e25b812aca8d1e65f8b88843ebb1055
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105693144"
---
# <a name="parental-controls-top-level-user-interface"></a><span data-ttu-id="ad465-103">Родительский контроль Top-Level пользовательского интерфейса</span><span class="sxs-lookup"><span data-stu-id="ad465-103">Parental Controls Top-Level User Interface</span></span>

<span data-ttu-id="ad465-104">Строгая связь между учетными записями семейной безопасности и пользователя Windows посвящена Объединенной категории, отображаемой в виде **учетных записей пользователей и семейной безопасности** на панели управления для SKU Windows Vista, ориентированного на потребителей.</span><span class="sxs-lookup"><span data-stu-id="ad465-104">The strong link between Family Safety and Windows user accounts has driven a combined category appearing as **User Accounts and Family Safety** in Control Panel for consumer-oriented SKUs of Windows Vista.</span></span>

> [!Note]  
> <span data-ttu-id="ad465-105">Эта категория будет отображаться как **учетные записи пользователей** при присоединении компьютера с возможностью присоединения к домену.</span><span class="sxs-lookup"><span data-stu-id="ad465-105">The category will appear as **User Accounts** when a computer with domain-join capability is joined.</span></span>

 

<span data-ttu-id="ad465-106">Если учетная запись обычного пользователя еще не настроена для контролируемого пользователя, ссылка в панели управления предоставляет простой рабочий процесс для добавления новой учетной записи, управляемой с помощью родительского элемента управления.</span><span class="sxs-lookup"><span data-stu-id="ad465-106">If a standard user account has not yet been set up for the controlled user, a link in Control Panel provides a simple workflow for adding a new parentally controlled account.</span></span>

<span data-ttu-id="ad465-107">После создания учетной записи на панели управления родительского контроля предоставляются функциональные возможности верхнего уровня, доступные пользователю для контролируемого пользователя.</span><span class="sxs-lookup"><span data-stu-id="ad465-107">After an account is created, the Parental Controls Control Panel exposes the top-level user-facing functionality for the controlled user.</span></span> <span data-ttu-id="ad465-108">Элементов</span><span class="sxs-lookup"><span data-stu-id="ad465-108">Elements:</span></span>

-   <span data-ttu-id="ad465-109">Общее управление ограничениями родительского контроля на переключателях.</span><span class="sxs-lookup"><span data-stu-id="ad465-109">Overall Parental Controls restrictions on or off radio buttons.</span></span>
-   <span data-ttu-id="ad465-110">Независимые отчеты о действиях для переключателей элемента управления.</span><span class="sxs-lookup"><span data-stu-id="ad465-110">Independent Activity Reporting on or off control radio buttons.</span></span>
-   <span data-ttu-id="ad465-111">В разделе параметров с веб-ограничениями, реализованными корпорацией Майкрософт, отображается условие, а также доступные базовые типы ограничений, реализованные в автономном режиме Майкрософт.</span><span class="sxs-lookup"><span data-stu-id="ad465-111">A Settings section with the Microsoft-implemented Web Restrictions link conditionally shown, and available core offline Microsoft-implemented restrictions types shown.</span></span>
-   <span data-ttu-id="ad465-112">Область больше параметров, которая отображается, если расширения пользовательского интерфейса зарегистрированы корпорацией Майкрософт или сторонними производителями.</span><span class="sxs-lookup"><span data-stu-id="ad465-112">A More Settings area that appears if User Interface extensions are registered by Microsoft or third parties.</span></span>
-   <span data-ttu-id="ad465-113">Область сводки состояния, показывающая имя пользователя и плитку, ссылку Просмотр отчетов о действиях и состояние параметров родительского контроля.</span><span class="sxs-lookup"><span data-stu-id="ad465-113">A summary status area showing the user name and tile, the View activity reports link, and the state of Parental Controls settings.</span></span> <span data-ttu-id="ad465-114">При значении на дисплее включается уровень настройки фильтра веб-содержимого (если фильтр Microsoft активен) или имя фильтра, если оно переопределено сторонним расширением, и состояние автономных параметров для пользователя.</span><span class="sxs-lookup"><span data-stu-id="ad465-114">If on, the display includes the Web Content Filter setting level (if the Microsoft filter is active) or filter name if overridden by a third-party extension, and state of offline settings for the user.</span></span>

<span data-ttu-id="ad465-115">Для переключателя общий родительский контроль включен переключатель изначально установлен в состояние OFF.</span><span class="sxs-lookup"><span data-stu-id="ad465-115">The overall Parental Controls enable radio button is initially set to the off state.</span></span> <span data-ttu-id="ad465-116">При включении администратором отчеты о действиях также будут включены по умолчанию, но могут быть отключены независимо.</span><span class="sxs-lookup"><span data-stu-id="ad465-116">When turned on by an administrator, Activity Reporting will also be on by default, but may be turned off independently.</span></span> <span data-ttu-id="ad465-117">Как и почти все параметры родительского контроля, настройка может выполняться программно с помощью доступных интерфейсов API.</span><span class="sxs-lookup"><span data-stu-id="ad465-117">As with nearly all settings in Parental Controls, configuration may be performed programmatically through the available APIs.</span></span>

 

 



