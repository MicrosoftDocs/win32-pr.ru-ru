---
description: Автозапуск — это функция операционной системы Windows.
title: Создание приложения для чтения компакт-дисков с поддержкой автозапуска
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 5c583c1d-a4eb-4291-a839-c1ca7c51342c
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 33f3ccc0a253690cd377cad908f87b43ac1ea304
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104262923"
---
# <a name="creating-an-autorun-enabled-cd-rom-application"></a><span data-ttu-id="aefa4-103">Создание приложения для чтения компакт-дисков с поддержкой автозапуска</span><span class="sxs-lookup"><span data-stu-id="aefa4-103">Creating an AutoRun-enabled CD-ROM Application</span></span>

<span data-ttu-id="aefa4-104">Автозапуск — это функция операционной системы Windows.</span><span class="sxs-lookup"><span data-stu-id="aefa4-104">AutoRun is a feature of the Windows operating system.</span></span> <span data-ttu-id="aefa4-105">Она автоматизирует процедуры установки и настройки продуктов, предназначенных для платформ на базе Windows, которые распространяются на компакт-диски.</span><span class="sxs-lookup"><span data-stu-id="aefa4-105">It automates the procedures for installing and configuring products designed for Windows-based platforms that are distributed on CD-ROMs.</span></span> <span data-ttu-id="aefa4-106">Когда пользователи вставляют компакт-диск с поддержкой автозапуска в дисковод для чтения компакт-дисков, автозапуск автоматически запускает приложение на компакт-диске, которое устанавливает, настраивает или запускает выбранный продукт.</span><span class="sxs-lookup"><span data-stu-id="aefa4-106">When users insert an AutoRun-enabled compact disc into their CD-ROM drive, AutoRun automatically runs an application on the CD-ROM that installs, configures, or runs the selected product.</span></span>

<span data-ttu-id="aefa4-107">Автозапуск можно использовать для установки и запуска приложений компакт-дисков.</span><span class="sxs-lookup"><span data-stu-id="aefa4-107">AutoRun can be used to install and run CD-ROM applications.</span></span> <span data-ttu-id="aefa4-108">Хотя Автозапуск чаще всего используется для приложений Windows, его также можно использовать для установки, настройки или запуска приложений на основе MS-DOS в сеансе Windows Microsoft MS-DOS.</span><span class="sxs-lookup"><span data-stu-id="aefa4-108">Although AutoRun is most commonly used for Windows applications, it can also be used to install, configure, or run MS-DOS-based applications in a Windows Microsoft MS-DOS session.</span></span> <span data-ttu-id="aefa4-109">Каждое приложение на основе MS-DOS можно настроить с помощью собственного уникального значка, Config.sys файла и Autoexec.bat файла.</span><span class="sxs-lookup"><span data-stu-id="aefa4-109">You can configure each MS-DOS-based application with its own unique icon, Config.sys file, and Autoexec.bat file.</span></span> <span data-ttu-id="aefa4-110">Windows создает правильные файлы конфигурации для приложения на основе MS-DOS.</span><span class="sxs-lookup"><span data-stu-id="aefa4-110">Windows creates the correct configuration files for the MS-DOS-based application.</span></span> <span data-ttu-id="aefa4-111">Затем запускаемое приложение запускает приложение на основе MS-DOS в окне.</span><span class="sxs-lookup"><span data-stu-id="aefa4-111">The startup application then starts the MS-DOS-based application in a window.</span></span>

> [!Note]  
> <span data-ttu-id="aefa4-112">Чтобы функция автозапуска работала, на дисководе компакт-дисков должно быть установлено 32 или 64-разрядные драйверы устройств, которые определяют, когда пользователь вставляет диск CD и уведомляет систему.</span><span class="sxs-lookup"><span data-stu-id="aefa4-112">For AutoRun to work, the CD-ROM drive must have 32 or 64-bit device drivers that detect when a user inserts a compact disc and notify the system.</span></span>

 

<span data-ttu-id="aefa4-113">В следующих разделах описывается реализация приложения CD-ROM с поддержкой автозапуска.</span><span class="sxs-lookup"><span data-stu-id="aefa4-113">The following sections discuss how to implement an AutoRun-enabled CD-ROM application.</span></span>

-   [<span data-ttu-id="aefa4-114">Создание приложения AutoRun-Enabled</span><span class="sxs-lookup"><span data-stu-id="aefa4-114">Creating an AutoRun-Enabled Application</span></span>](autoplay-works.md)
-   [<span data-ttu-id="aefa4-115">Записи autorun. INF</span><span class="sxs-lookup"><span data-stu-id="aefa4-115">Autorun.inf Entries</span></span>](autorun-cmds.md)
-   [<span data-ttu-id="aefa4-116">Включение и отключение автозапуска</span><span class="sxs-lookup"><span data-stu-id="aefa4-116">Enabling and Disabling AutoRun</span></span>](autoplay-reg.md)

 

 



