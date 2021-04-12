---
description: Функции перенаправления устройств перенаправляют стандартные устройства MS-DOS, буквы дисков и LPT-порты. Это позволяет приложениям, работающим в системе, использовать устройства и получать доступ к сети совершенно прозрачно.
ms.assetid: a61ab1e6-dad9-4dc0-a908-f8440619f610
title: Функции Device-Redirecting
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 577f8d108b6bfdeb01f786478cd736e6c84cc83d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104262889"
---
# <a name="device-redirecting-functions"></a><span data-ttu-id="81e40-104">Функции Device-Redirecting</span><span class="sxs-lookup"><span data-stu-id="81e40-104">Device-Redirecting Functions</span></span>

<span data-ttu-id="81e40-105">Функции перенаправления устройств перенаправляют стандартные устройства MS-DOS, буквы дисков и LPT-порты.</span><span class="sxs-lookup"><span data-stu-id="81e40-105">The device-redirecting functions redirect standard MS-DOS devices, drive letters and LPT ports.</span></span> <span data-ttu-id="81e40-106">Это позволяет приложениям, работающим в системе, использовать устройства и получать доступ к сети совершенно прозрачно.</span><span class="sxs-lookup"><span data-stu-id="81e40-106">This enables applications running on the system to use the devices and access the network in a totally transparent manner.</span></span>



| <span data-ttu-id="81e40-107">Функция</span><span class="sxs-lookup"><span data-stu-id="81e40-107">Function</span></span>                                                         | <span data-ttu-id="81e40-108">Описание</span><span class="sxs-lookup"><span data-stu-id="81e40-108">Description</span></span>                                                                                                                                                                                         |
|------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="81e40-109">**нпаддконнектион**</span><span class="sxs-lookup"><span data-stu-id="81e40-109">**NPAddConnection**</span></span>](/windows/desktop/api/Npapi/nf-npapi-npaddconnection)                       | <span data-ttu-id="81e40-110">Перенаправляет или подключает локальное устройство к сетевому ресурсу.</span><span class="sxs-lookup"><span data-stu-id="81e40-110">Redirects or connects a local device to a network resource.</span></span><br/>                                                                                                                              |
| [<span data-ttu-id="81e40-111">**NPAddConnection3**</span><span class="sxs-lookup"><span data-stu-id="81e40-111">**NPAddConnection3**</span></span>](/windows/desktop/api/Npapi/nf-npapi-npaddconnection3)                     | <span data-ttu-id="81e40-112">Выполняет то же действие, что и [**нпаддконнектион**](/windows/desktop/api/Npapi/nf-npapi-npaddconnection), но позволяет пользователю указать, какое окно должно владеть любыми диалоговыми окнами и как должно быть установлено соединение.</span><span class="sxs-lookup"><span data-stu-id="81e40-112">Performs the same action as [**NPAddConnection**](/windows/desktop/api/Npapi/nf-npapi-npaddconnection), but lets the user specify which window should own any dialog boxes and how the connection should be established.</span></span><br/> |
| [<span data-ttu-id="81e40-113">**нпканцелконнектион**</span><span class="sxs-lookup"><span data-stu-id="81e40-113">**NPCancelConnection**</span></span>](/windows/desktop/api/Npapi/nf-npapi-npcancelconnection)                 | <span data-ttu-id="81e40-114">Прерывает сетевое подключение.</span><span class="sxs-lookup"><span data-stu-id="81e40-114">Breaks a network connection.</span></span> <span data-ttu-id="81e40-115">Изменения сохраняются, если устройство отключено, если только подключение не подключено к устройствам.</span><span class="sxs-lookup"><span data-stu-id="81e40-115">The changes are remembered if a device is disconnected unless the connection is a deviceless connection.</span></span><br/>                                                    |
| [<span data-ttu-id="81e40-116">**нпжетконнектион**</span><span class="sxs-lookup"><span data-stu-id="81e40-116">**NPGetConnection**</span></span>](/windows/desktop/api/Npapi/nf-npapi-npgetconnection)                       | <span data-ttu-id="81e40-117">Возвращает сведения о соединении.</span><span class="sxs-lookup"><span data-stu-id="81e40-117">Returns information about a connection.</span></span><br/>                                                                                                                                                  |
| [<span data-ttu-id="81e40-118">**NPGetConnection3**</span><span class="sxs-lookup"><span data-stu-id="81e40-118">**NPGetConnection3**</span></span>](/windows/desktop/api/Npapi/nf-npapi-npgetconnection3)                     | <span data-ttu-id="81e40-119">Возвращает сведения о соединении, даже если подключение в данный момент отключено.</span><span class="sxs-lookup"><span data-stu-id="81e40-119">Returns information about a connection, even if the connection is currently disconnected.</span></span><br/>                                                                                                |
| [<span data-ttu-id="81e40-120">**нпжетконнектионперформанце**</span><span class="sxs-lookup"><span data-stu-id="81e40-120">**NPGetConnectionPerformance**</span></span>](/windows/desktop/api/Npapi/nf-npapi-npgetconnectionperformance) | <span data-ttu-id="81e40-121">Возвращает сведения о производительности соединения.</span><span class="sxs-lookup"><span data-stu-id="81e40-121">Returns performance information about a connection.</span></span><br/>                                                                                                                                      |
| [<span data-ttu-id="81e40-122">**нпжетуниверсалнаме**</span><span class="sxs-lookup"><span data-stu-id="81e40-122">**NPGetUniversalName**</span></span>](/windows/desktop/api/Npapi/nf-npapi-npgetuniversalname)                 | <span data-ttu-id="81e40-123">Возвращает удаленное или локальное универсальное имя в формате, указанном при вызове функции.</span><span class="sxs-lookup"><span data-stu-id="81e40-123">Returns the remote or local universal name, in the format specified during the function call.</span></span><br/>                                                                                            |



 

 

 




