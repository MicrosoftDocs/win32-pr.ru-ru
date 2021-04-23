---
title: Средства журнала событий Windows
description: Журнал событий Windows содержит следующие средства, используемые для построения поставщика.
ms.assetid: 20087fdf-3e9f-4090-8103-5864f1c9753c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 93e604c291ff1046789ef9f3efba00ebb7305122
ms.sourcegitcommit: c2a1c4314550ea9bd202d28adfcc7bfe6180932f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2020
ms.locfileid: "104412740"
---
# <a name="windows-event-log-tools"></a><span data-ttu-id="8ae08-103">Средства журнала событий Windows</span><span class="sxs-lookup"><span data-stu-id="8ae08-103">Windows Event Log Tools</span></span>

<span data-ttu-id="8ae08-104">Журнал событий Windows содержит следующие средства, используемые для построения поставщика.</span><span class="sxs-lookup"><span data-stu-id="8ae08-104">Windows Event Log provides the following tools that you use to build your provider.</span></span>



| <span data-ttu-id="8ae08-105">Средство</span><span class="sxs-lookup"><span data-stu-id="8ae08-105">Tool</span></span>                                                           | <span data-ttu-id="8ae08-106">Описание</span><span class="sxs-lookup"><span data-stu-id="8ae08-106">Description</span></span>                                                                                   |
|----------------------------------------------------------------|-----------------------------------------------------------------------------------------------|
| [<span data-ttu-id="8ae08-107">**Компилятор сообщений (MC.exe)**</span><span class="sxs-lookup"><span data-stu-id="8ae08-107">**Message Compiler (MC.exe)**</span></span>](message-compiler--mc-exe-.md)  | <span data-ttu-id="8ae08-108">Служебная программа командной строки, используемая для компиляции манифестов инструментирования и текстовых файлов сообщений.</span><span class="sxs-lookup"><span data-stu-id="8ae08-108">A command line utility used to compile instrumentation manifests and message text files.</span></span> |
| <span data-ttu-id="8ae08-109">WevtUtil.exe</span><span class="sxs-lookup"><span data-stu-id="8ae08-109">WevtUtil.exe</span></span>                                                   | <span data-ttu-id="8ae08-110">Программа командной строки, используемая в основном для регистрации поставщика на компьютере.</span><span class="sxs-lookup"><span data-stu-id="8ae08-110">A command line utility used primarily to register your provider on the computer.</span></span> <span data-ttu-id="8ae08-111">Кроме того, его можно использовать для получения метаданных о поставщике, его событиях и каналах, на которые он записывает события, а также для запроса событий из канала или файла журнала.</span><span class="sxs-lookup"><span data-stu-id="8ae08-111">You can also use it to get metadata information about the provider, its events, and the channels to which it logs events, and to query events from a channel or log file.</span></span> <span data-ttu-id="8ae08-112">Средство WevtUtil.exe входит в папку% WINDIR% \\ System32.</span><span class="sxs-lookup"><span data-stu-id="8ae08-112">The WevtUtil.exe tool is included in %windir%\\System32.</span></span> <span data-ttu-id="8ae08-113">Для получения сведений об использовании введите "wevtutil/?"</span><span class="sxs-lookup"><span data-stu-id="8ae08-113">For usage information, enter "wevtutil /?"</span></span> <span data-ttu-id="8ae08-114">в командной строке.</span><span class="sxs-lookup"><span data-stu-id="8ae08-114">at a command prompt.</span></span><br/> <span data-ttu-id="8ae08-115">Эта команда ограничена членами группы "Администраторы" и должна выполняться с повышенными привилегиями.</span><span class="sxs-lookup"><span data-stu-id="8ae08-115">This command is limited to members of the Administrators group and must be run with elevated privileges.</span></span>|
