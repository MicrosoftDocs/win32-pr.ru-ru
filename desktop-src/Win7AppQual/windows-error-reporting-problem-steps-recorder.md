---
description: .
ms.assetid: ce5db84a-53b6-4a7f-bee4-d198d8a6781e
title: Средство записи действий отчеты об ошибках Windows проблем
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 25fb70acef867b878063bd6011fde6867f7f0e75
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103818072"
---
# <a name="windows-error-reporting-problem-steps-recorder"></a><span data-ttu-id="aa7be-103">Средство записи действий отчеты об ошибках Windows проблем</span><span class="sxs-lookup"><span data-stu-id="aa7be-103">Windows Error Reporting Problem Steps Recorder</span></span>

## <a name="affected-platforms"></a><span data-ttu-id="aa7be-104">Затронутые платформы</span><span class="sxs-lookup"><span data-stu-id="aa7be-104">Affected Platforms</span></span>

<span data-ttu-id="aa7be-105">**Клиенты** — Windows 7</span><span class="sxs-lookup"><span data-stu-id="aa7be-105">**Clients** – Windows 7</span></span>  
<span data-ttu-id="aa7be-106">**Серверы** — Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="aa7be-106">**Servers** – Windows Server 2008 R2</span></span>  


## <a name="description"></a><span data-ttu-id="aa7be-107">Описание</span><span class="sxs-lookup"><span data-stu-id="aa7be-107">Description</span></span>

<span data-ttu-id="aa7be-108">До Windows 7 отчеты об ошибках Windows (WER) собрались отчеты об ошибках, в которых были указаны проблемы, требующие восстановления.</span><span class="sxs-lookup"><span data-stu-id="aa7be-108">Prior to Windows 7, Windows Error Reporting (WER) collected error reports that indicated problems in need of repair.</span></span> <span data-ttu-id="aa7be-109">Эти отчеты об ошибках содержат полезную информацию, описывающую общую природу проблемы, но недостаточно информации для определения ее основной причины.</span><span class="sxs-lookup"><span data-stu-id="aa7be-109">These error reports contain helpful information that describes the general nature of a problem, but not enough information to determine its root cause.</span></span> <span data-ttu-id="aa7be-110">Для этого разработчикам требуется средство для воспроизведения сценария аварийного завершения или зависания для отладки.</span><span class="sxs-lookup"><span data-stu-id="aa7be-110">For that, developers need a tool to reproduce the crash/hang scenario for debugging.</span></span>

<span data-ttu-id="aa7be-111">Новое приложение, записывающее действия по задачам (PSR.exe), будет доставляться во всех сборках Windows 7.</span><span class="sxs-lookup"><span data-stu-id="aa7be-111">A new application, Problem Steps Recorder (PSR.exe), is shipping on all builds of Windows 7.</span></span> <span data-ttu-id="aa7be-112">Эта функция включает сбор действий, выполняемых пользователем при сбое, чтобы тестеры и разработчики могли воспроизвести ситуацию для анализа и отладки.</span><span class="sxs-lookup"><span data-stu-id="aa7be-112">This feature enables the collection of the actions performed by a user while encountering a crash so that testers and developers can reproduce the situation for analysis and debugging.</span></span>

## <a name="usage"></a><span data-ttu-id="aa7be-113">Использование</span><span class="sxs-lookup"><span data-stu-id="aa7be-113">Usage</span></span>

<span data-ttu-id="aa7be-114">В настоящее время разработчик службы отчеты об ошибках Windows должен запросить включение PSR для приложения. Организации службы поддержки Майкрософт также используют это средство при устранении неполадок с конечными пользователями.</span><span class="sxs-lookup"><span data-stu-id="aa7be-114">Currently, a Windows Error Reporting service developer must request PSR enablement for an application; Microsoft support organizations also use this tool while troubleshooting with end users.</span></span> <span data-ttu-id="aa7be-115">Планируется сделать PSR доступным в веб-службах Windows Quality Online Services (Винкуал) после выпуска Windows 7.</span><span class="sxs-lookup"><span data-stu-id="aa7be-115">Plans are in place to make PSR available at Windows Quality Online Services (Winqual) after the release of Windows 7.</span></span>

<span data-ttu-id="aa7be-116">**Примечание.** Если PSR включен для приложения, приложение может столкнуться с некоторым снижением производительности.</span><span class="sxs-lookup"><span data-stu-id="aa7be-116">**Note:** With PSR enabled for an application, the application may see some performance degradation.</span></span>

## <a name="links-to-other-resources"></a><span data-ttu-id="aa7be-117">Ссылки на другие ресурсы</span><span class="sxs-lookup"><span data-stu-id="aa7be-117">Links to Other Resources</span></span>

-   [<span data-ttu-id="aa7be-118">отчеты об ошибках Windows запись блога</span><span class="sxs-lookup"><span data-stu-id="aa7be-118">Windows Error Reporting blog entry</span></span>](/archive/blogs/wer/)
-   [<span data-ttu-id="aa7be-119">Веб-службы Windows Quality Services (Винкуал)</span><span class="sxs-lookup"><span data-stu-id="aa7be-119">Windows Quality Online Services (Winqual)</span></span>](https://winqual.microsoft.com)

 

 
