---
description: Следующие функции используются поставщиками времени.
ms.assetid: 05687a67-4e0b-4a44-9c2d-7e097be9008c
title: Функции поставщика времени
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 20a24f15bd67751dc09a689078a8a518224267c0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105664055"
---
# <a name="time-provider-functions"></a><span data-ttu-id="924af-103">Функции поставщика времени</span><span class="sxs-lookup"><span data-stu-id="924af-103">Time Provider Functions</span></span>

<span data-ttu-id="924af-104">Следующие функции используются поставщиками времени.</span><span class="sxs-lookup"><span data-stu-id="924af-104">The following functions are used by time providers.</span></span>



| <span data-ttu-id="924af-105">Функция</span><span class="sxs-lookup"><span data-stu-id="924af-105">Function</span></span>                                                               | <span data-ttu-id="924af-106">Описание</span><span class="sxs-lookup"><span data-stu-id="924af-106">Description</span></span>                                                                                            |
|------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="924af-107">**алертсамплесаваилфунк**</span><span class="sxs-lookup"><span data-stu-id="924af-107">**AlertSamplesAvailFunc**</span></span>](/windows/desktop/api/Timeprov/nc-timeprov-alertsamplesavailfunc)                     | <span data-ttu-id="924af-108">Уведомляет систему о наличии новых примеров.</span><span class="sxs-lookup"><span data-stu-id="924af-108">Notifies the system that there are new samples available.</span></span>                                              |
| [<span data-ttu-id="924af-109">**жеттимесисинфофунк**</span><span class="sxs-lookup"><span data-stu-id="924af-109">**GetTimeSysInfoFunc**</span></span>](/windows/desktop/api/Timeprov/nc-timeprov-gettimesysinfofunc)                           | <span data-ttu-id="924af-110">Извлекает сведения о состоянии системного времени.</span><span class="sxs-lookup"><span data-stu-id="924af-110">Retrieves the system time state information.</span></span>                                                           |
| [<span data-ttu-id="924af-111">**логтимепровевентфунк**</span><span class="sxs-lookup"><span data-stu-id="924af-111">**LogTimeProvEventFunc**</span></span>](/windows/desktop/api/Timeprov/nc-timeprov-logtimeproveventfunc)                       | <span data-ttu-id="924af-112">Регистрирует событие поставщика времени в журнале событий.</span><span class="sxs-lookup"><span data-stu-id="924af-112">Logs a time provider event in the event log.</span></span>                                                           |
| [<span data-ttu-id="924af-113">**сетпровидерстатусфунк**</span><span class="sxs-lookup"><span data-stu-id="924af-113">**SetProviderStatusFunc**</span></span>](/windows/desktop/api/Timeprov/nc-timeprov-setproviderstatusfunc)                 | <span data-ttu-id="924af-114">Задает сведения о состоянии поставщика времени.</span><span class="sxs-lookup"><span data-stu-id="924af-114">Sets the time provider's status information.</span></span>                                                           |
| [<span data-ttu-id="924af-115">**сетпровидерстатусинфофрифунк**</span><span class="sxs-lookup"><span data-stu-id="924af-115">**SetProviderStatusInfoFreeFunc**</span></span>](/windows/desktop/api/Timeprov/nc-timeprov-setproviderstatusinfofreefunc) | <span data-ttu-id="924af-116">Освобождает структуру [**сетпровидерстатусинфо**](/windows/desktop/api/Timeprov/ns-timeprov-setproviderstatusinfo) .</span><span class="sxs-lookup"><span data-stu-id="924af-116">Frees a [**SetProviderStatusInfo**](/windows/desktop/api/Timeprov/ns-timeprov-setproviderstatusinfo) structure.</span></span>                          |
| [<span data-ttu-id="924af-117">**тимепровклосе**</span><span class="sxs-lookup"><span data-stu-id="924af-117">**TimeProvClose**</span></span>](/windows/desktop/api/Timeprov/nf-timeprov-timeprovclose)                                 | <span data-ttu-id="924af-118">Функция обратного вызова, вызываемая диспетчером поставщиков времени для завершения работы поставщика времени.</span><span class="sxs-lookup"><span data-stu-id="924af-118">A callback function that is called by the time provider manager to shut down the time provider.</span></span>        |
| [<span data-ttu-id="924af-119">**тимепровкомманд**</span><span class="sxs-lookup"><span data-stu-id="924af-119">**TimeProvCommand**</span></span>](/windows/desktop/api/Timeprov/nf-timeprov-timeprovcommand)                             | <span data-ttu-id="924af-120">Функция обратного вызова, вызываемая диспетчером поставщика времени для отправки команд поставщику времени.</span><span class="sxs-lookup"><span data-stu-id="924af-120">A callback function that is called by the time provider manager to send commands to the time provider.</span></span> |
| [<span data-ttu-id="924af-121">**тимепровопен**</span><span class="sxs-lookup"><span data-stu-id="924af-121">**TimeProvOpen**</span></span>](/windows/desktop/api/Timeprov/nf-timeprov-timeprovopen)                                   | <span data-ttu-id="924af-122">Функция обратного вызова, вызываемая диспетчером поставщиков времени при загрузке библиотеки DLL поставщика времени.</span><span class="sxs-lookup"><span data-stu-id="924af-122">A callback function that is called by the time provider manager when the time provider DLL is loaded.</span></span>  |



 

 

 



