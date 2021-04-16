---
title: Архивация и восстановление Windows 7 устарели
description: Архивация и восстановление Windows 7 устарели
ms.assetid: 89FB9C1B-FEE8-4508-9501-EA139F3706F7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dcc20fa7ada55ada1f3c2f70c54955cec3d51666
ms.sourcegitcommit: ea4baf9953a78d2d6bd530b680601e39f3884541
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/01/2020
ms.locfileid: "105672421"
---
# <a name="windows-7-backup-and-restore-deprecated"></a><span data-ttu-id="fcf7a-103">Архивация и восстановление Windows 7 устарели</span><span class="sxs-lookup"><span data-stu-id="fcf7a-103">Windows 7 Backup and Restore deprecated</span></span>

## <a name="platform"></a><span data-ttu-id="fcf7a-104">Платформа</span><span class="sxs-lookup"><span data-stu-id="fcf7a-104">Platform</span></span>

<span data-ttu-id="fcf7a-105">**Клиенты** — Windows 8</span><span class="sxs-lookup"><span data-stu-id="fcf7a-105">**Clients** – Windows 8</span></span> 


## <a name="description"></a><span data-ttu-id="fcf7a-106">Описание</span><span class="sxs-lookup"><span data-stu-id="fcf7a-106">Description</span></span>

<span data-ttu-id="fcf7a-107">При отсутствии изменений в поведении на резервное копирование и восстановление эта функция считается устаревшей и не будет обновлена.</span><span class="sxs-lookup"><span data-stu-id="fcf7a-107">While there is no behavioral change to Backup and Restore, this function is being deprecated and will not be updated.</span></span> <span data-ttu-id="fcf7a-108">Он использовался редко, и его функциональность заменена новой функцией истории файлов.</span><span class="sxs-lookup"><span data-stu-id="fcf7a-108">It was rarely used and its functionality has been replaced by the new File History feature.</span></span> <span data-ttu-id="fcf7a-109">Она будет поставляться в Windows 8 и энтузиастов, которые выполнили обновление с Windows 7 до Windows 8 или зависят от резервного копирования и восстановления или резервной копии образа диска, будут по-прежнему иметь возможность использовать ее.</span><span class="sxs-lookup"><span data-stu-id="fcf7a-109">It will ship in Windows 8 and enthusiasts who upgraded from Windows 7 to Windows 8 or depend on Backup and Restore or disk image backup will be still able to use it.</span></span> <span data-ttu-id="fcf7a-110">Однако все точки доступа к резервному копированию и восстановлению, за исключением панели управления, были удалены.</span><span class="sxs-lookup"><span data-stu-id="fcf7a-110">However, all access points to Backup and Restore, with the exception of the Control Panel, have been removed.</span></span> <span data-ttu-id="fcf7a-111">Приложение панели управления, используемое для резервного копирования и восстановления, было переименовано в восстановление файлов Windows 7.</span><span class="sxs-lookup"><span data-stu-id="fcf7a-111">The Control Panel applet used by Backup and Restore was renamed to Windows 7 File Recovery.</span></span>

<span data-ttu-id="fcf7a-112">Изготовители оборудования, устанавливающие раздел реестра для отключения уведомлений об архивации в своих образах, больше не нуждаются в этом.</span><span class="sxs-lookup"><span data-stu-id="fcf7a-112">OEMs that were setting the registry key to disable backup notification in their images will no longer need to do that.</span></span>

<span data-ttu-id="fcf7a-113">Мы не рекомендуем использовать обе функции одновременно.</span><span class="sxs-lookup"><span data-stu-id="fcf7a-113">We do not recommend using both features at the same time.</span></span> <span data-ttu-id="fcf7a-114">Проверка истории файлов. Если расписание резервного копирования существует и активно, а если оно найдено, оно не позволит пользователям включать его.</span><span class="sxs-lookup"><span data-stu-id="fcf7a-114">File History checks if Backup schedule exists and is active and if it finds one, it will not let users to turn it on.</span></span> <span data-ttu-id="fcf7a-115">В этом случае пользователям, желающим использовать журнал файлов, придется удалить расписание архивации Windows.</span><span class="sxs-lookup"><span data-stu-id="fcf7a-115">In this case, users who want to use File History will have to delete the Windows Backup schedule.</span></span>

## <a name="manifestation"></a><span data-ttu-id="fcf7a-116">Проявление</span><span class="sxs-lookup"><span data-stu-id="fcf7a-116">Manifestation</span></span>

<span data-ttu-id="fcf7a-117">Рабочие процессы могут быть прерваны, и документация, которая ссылается на предыдущий метод для доступа к функции резервного копирования и восстановления Windows, потребуется обновить, чтобы отразить эти изменения.</span><span class="sxs-lookup"><span data-stu-id="fcf7a-117">Workflows may be interrupted and documentation that refers to the previous method for accessing the Windows Backup and Restore feature will need to be updated to reflect these changes.</span></span>

## <a name="mitigation"></a><span data-ttu-id="fcf7a-118">Меры по снижению риска</span><span class="sxs-lookup"><span data-stu-id="fcf7a-118">Mitigation</span></span>

<span data-ttu-id="fcf7a-119">Приложения, которые могут запускать резервное копирование и восстановление, должны быть перезаписаны, чтобы проверить, включен ли журнал файлов, и позволить пользователям выбрать предпочтительный метод.</span><span class="sxs-lookup"><span data-stu-id="fcf7a-119">Apps that might trigger Backup and Restore should be rewritten to check if File History is on and let users choose their preferred method.</span></span>

 

 




