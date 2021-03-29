---
description: Интерфейс Иупдатеинсталлер определяет следующие свойства.
ms.assetid: 876a2150-40a1-42a3-bc9a-05dec94fccd3
title: Свойства Иупдатеинсталлер
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 77df235c49e7b6f27b0f93ec3b0c4def12135065
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103897562"
---
# <a name="iupdateinstaller-properties"></a><span data-ttu-id="18d0a-103">Свойства Иупдатеинсталлер</span><span class="sxs-lookup"><span data-stu-id="18d0a-103">IUpdateInstaller Properties</span></span>

<span data-ttu-id="18d0a-104">Интерфейс [**иупдатеинсталлер**](/windows/desktop/api/Wuapi/nn-wuapi-iupdateinstaller) определяет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="18d0a-104">The [**IUpdateInstaller**](/windows/desktop/api/Wuapi/nn-wuapi-iupdateinstaller) interface defines the following properties.</span></span>



| <span data-ttu-id="18d0a-105">Свойство</span><span class="sxs-lookup"><span data-stu-id="18d0a-105">Property</span></span>                                                                                      | <span data-ttu-id="18d0a-106">Описание</span><span class="sxs-lookup"><span data-stu-id="18d0a-106">Description</span></span>                                                                                                                           |
|-----------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="18d0a-107">**алловсаурцепромптс**</span><span class="sxs-lookup"><span data-stu-id="18d0a-107">**AllowSourcePrompts**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iupdateinstaller-get_allowsourceprompts)                             | <span data-ttu-id="18d0a-108">Возвращает и задает логическое значение, указывающее, следует ли отображать запросы к источнику пользователю при установке обновлений.</span><span class="sxs-lookup"><span data-stu-id="18d0a-108">Gets and sets a Boolean value that indicates whether to show source prompts to the user when installing the updates.</span></span>                  |
| [<span data-ttu-id="18d0a-109">**ClientApplicationID**</span><span class="sxs-lookup"><span data-stu-id="18d0a-109">**ClientApplicationID**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iupdateinstaller-get_clientapplicationid)                           | <span data-ttu-id="18d0a-110">Возвращает и задает текущее клиентское приложение.</span><span class="sxs-lookup"><span data-stu-id="18d0a-110">Gets and sets the current client application.</span></span>                                                                                         |
| [<span data-ttu-id="18d0a-111">**IsBusy**</span><span class="sxs-lookup"><span data-stu-id="18d0a-111">**IsBusy**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iupdateinstaller-get_isbusy)                                                     | <span data-ttu-id="18d0a-112">Возвращает логическое значение, указывающее, выполняется ли установка или удаление на компьютере в определенное время.</span><span class="sxs-lookup"><span data-stu-id="18d0a-112">Gets a Boolean value that indicates whether an installation or uninstallation is in progress on a computer at a specific time.</span></span>        |
| [<span data-ttu-id="18d0a-113">**Принудительно**</span><span class="sxs-lookup"><span data-stu-id="18d0a-113">**IsForced**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iupdateinstaller-get_isforced)                                                 | <span data-ttu-id="18d0a-114">Возвращает или задает логическое значение, указывающее, следует ли принудительно установить или удалить обновление.</span><span class="sxs-lookup"><span data-stu-id="18d0a-114">Gets or sets a Boolean value that indicates whether to forcibly install or uninstall an update.</span></span>                                       |
| [<span data-ttu-id="18d0a-115">**паренсвнд**</span><span class="sxs-lookup"><span data-stu-id="18d0a-115">**ParentHwnd**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iupdateinstaller-get_parenthwnd)                                             | <span data-ttu-id="18d0a-116">Возвращает и задает маркер родительского окна, которое может содержать диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="18d0a-116">Gets and sets a handle to the parent window that can contain a dialog box.</span></span>                                                            |
| [<span data-ttu-id="18d0a-117">**парентвиндов**</span><span class="sxs-lookup"><span data-stu-id="18d0a-117">**ParentWindow**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iupdateinstaller-get_parentwindow)                                         | <span data-ttu-id="18d0a-118">Возвращает и задает интерфейс, представляющий родительское окно, которое может содержать диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="18d0a-118">Gets and sets the interface that represents the parent window that can contain a dialog box.</span></span>                                          |
| [<span data-ttu-id="18d0a-119">**ребутрекуиредбефореинсталлатион**</span><span class="sxs-lookup"><span data-stu-id="18d0a-119">**RebootRequiredBeforeInstallation**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iupdateinstaller-get_rebootrequiredbeforeinstallation) | <span data-ttu-id="18d0a-120">Возвращает логическое значение, указывающее, требуется ли перезагрузка системы перед установкой или удалением обновлений.</span><span class="sxs-lookup"><span data-stu-id="18d0a-120">Gets a Boolean value that indicates whether a system restart is required before installing or uninstalling updates.</span></span>                   |
| [<span data-ttu-id="18d0a-121">**Обновления**</span><span class="sxs-lookup"><span data-stu-id="18d0a-121">**Updates**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iupdateinstaller-get_updates)                                                   | <span data-ttu-id="18d0a-122">Возвращает и задает интерфейс, который содержит доступную только для чтения коллекцию обновлений, указанных для установки или удаления.</span><span class="sxs-lookup"><span data-stu-id="18d0a-122">Gets and sets an interface that contains a read-only collection of the updates that are specified for installation or uninstallation.</span></span> |



 

 

 



