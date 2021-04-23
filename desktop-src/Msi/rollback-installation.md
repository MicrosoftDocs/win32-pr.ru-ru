---
description: Когда установщик Windows обрабатывает скрипт установки для установки продукта или приложения, он одновременно создает сценарий отката и сохраняет копию каждого файла, который был удален во время установки.
ms.assetid: 6c70e788-beb0-46db-94b0-1bbaac972acf
title: Откат установки
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cc958c7d5e1dead2cd3e3e0b6081e7c71cd9af7a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104155511"
---
# <a name="rollback-installation"></a><span data-ttu-id="3e10d-103">Откат установки</span><span class="sxs-lookup"><span data-stu-id="3e10d-103">Rollback Installation</span></span>

<span data-ttu-id="3e10d-104">Когда установщик Windows обрабатывает скрипт установки для установки продукта или приложения, он одновременно создает сценарий отката и сохраняет копию каждого файла, который был удален во время установки.</span><span class="sxs-lookup"><span data-stu-id="3e10d-104">When the Windows Installer processes the installation script for the installation of a product or application, it simultaneously generates a rollback script and saves a copy of every file deleted during the installation.</span></span> <span data-ttu-id="3e10d-105">Эти файлы хранятся в скрытом системном каталоге и автоматически удаляются после успешного завершения установки.</span><span class="sxs-lookup"><span data-stu-id="3e10d-105">These files are kept in a hidden system directory and are automatically deleted once the installation is successfully completed.</span></span> <span data-ttu-id="3e10d-106">Если установка завершается неудачно, установщик автоматически выполняет установку отката, которая возвращает систему в исходное состояние.</span><span class="sxs-lookup"><span data-stu-id="3e10d-106">If however the installation is unsuccessful, the installer automatically performs a rollback installation that returns the system to its original state.</span></span>

<span data-ttu-id="3e10d-107">Автоматический откат неудачной установки является поведением установщика по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="3e10d-107">Automatic rollback of an unsuccessful installation is the default behavior of the installer.</span></span> <span data-ttu-id="3e10d-108">Чтобы отключить откат во время установки, используйте один из следующих способов.</span><span class="sxs-lookup"><span data-stu-id="3e10d-108">To disable rollback during an installation use one of the following:</span></span>

-   [<span data-ttu-id="3e10d-109">**ДИСАБЛЕРОЛЛБАКК, свойство**</span><span class="sxs-lookup"><span data-stu-id="3e10d-109">**DISABLEROLLBACK Property**</span></span>](-disablerollback.md)
-   [<span data-ttu-id="3e10d-110">**ПРОМПТРОЛЛБАКККОСТ, свойство**</span><span class="sxs-lookup"><span data-stu-id="3e10d-110">**PROMPTROLLBACKCOST Property**</span></span>](promptrollbackcost.md)
-   [<span data-ttu-id="3e10d-111">Действие Дисаблероллбакк</span><span class="sxs-lookup"><span data-stu-id="3e10d-111">DisableRollback Action</span></span>](disablerollback-action.md)
-   [<span data-ttu-id="3e10d-112">дисаблероллбакк</span><span class="sxs-lookup"><span data-stu-id="3e10d-112">DisableRollback</span></span>](disablerollback.md)
-   [<span data-ttu-id="3e10d-113">Енаблероллбакк таблице ControlEvent событие</span><span class="sxs-lookup"><span data-stu-id="3e10d-113">EnableRollback ControlEvent</span></span>](enablerollback-controlevent.md)

<span data-ttu-id="3e10d-114">При отключении отката установщик устанавливает свойство [**роллбаккдисаблед**](rollbackdisabled.md) .</span><span class="sxs-lookup"><span data-stu-id="3e10d-114">Whenever rollback is disabled, the installer sets the [**RollbackDisabled**](rollbackdisabled.md) property.</span></span>

<span data-ttu-id="3e10d-115">Если при установке используются [Настраиваемые действия](custom-actions.md), то для использования функции отката требуется дополнительная разработка пакета установки.</span><span class="sxs-lookup"><span data-stu-id="3e10d-115">If an installation uses [custom actions](custom-actions.md), additional authoring of the installation package is required to use rollback functionality.</span></span> <span data-ttu-id="3e10d-116">Дополнительные сведения см. в разделе [ROLLBACK Custom Actions](rollback-custom-actions.md).</span><span class="sxs-lookup"><span data-stu-id="3e10d-116">For more information, see [Rollback Custom Actions](rollback-custom-actions.md).</span></span>

 

 



