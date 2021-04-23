---
title: Требования IIS для отправки BITS
description: Для отправки BITS требуется IIS 6,0 на Windows Server 2003 и IIS 7,0 в Windows Server 2008; Служба BITS не поддерживает IIS 5,1 в Windows XP.
ms.assetid: 8ab07af5-3b59-4c98-8e57-f614deb8b594
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d8fc1eb9bae86e7bb2635b3a250e8a9efe1bc630
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103773655"
---
# <a name="iis-requirements-for-bits-uploads"></a><span data-ttu-id="7760c-103">Требования IIS для отправки BITS</span><span class="sxs-lookup"><span data-stu-id="7760c-103">IIS Requirements for BITS Uploads</span></span>

<span data-ttu-id="7760c-104">Для отправки BITS требуется IIS 6,0 на Windows Server 2003 и IIS 7,0 в Windows Server 2008; Служба BITS не поддерживает IIS 5,1 в Windows XP.</span><span class="sxs-lookup"><span data-stu-id="7760c-104">For uploads, BITS requires IIS 6.0 on Windows Server 2003, and IIS 7.0 on Windows Server 2008; BITS does not support IIS 5.1 on Windows XP.</span></span> <span data-ttu-id="7760c-105">Виртуальный каталог IIS должен быть включен для отправки и настроен для расширений IIS BITS.</span><span class="sxs-lookup"><span data-stu-id="7760c-105">The IIS virtual directory must be enabled for uploads and have the BITS IIS extensions configured.</span></span>

<span data-ttu-id="7760c-106">**Основные установки Windows Server:** Расширения BITS для IIS не поддерживаются.</span><span class="sxs-lookup"><span data-stu-id="7760c-106">**Core installations of Windows Server:** BITS IIS extensions are not supported.</span></span>

<span data-ttu-id="7760c-107">В Windows Server 2008 используйте **Диспетчер сервера** , чтобы установить компонент серверные расширения BITS.</span><span class="sxs-lookup"><span data-stu-id="7760c-107">On Windows Server 2008, use the **Server Manager** to install the BITS Server Extensions feature.</span></span> <span data-ttu-id="7760c-108">В **Диспетчер сервера** щелкните **компоненты** в левой области.</span><span class="sxs-lookup"><span data-stu-id="7760c-108">From **Server Manager**, click **Features** in the left pane.</span></span> <span data-ttu-id="7760c-109">В **мастере добавления компонентов** проверьте серверные расширения BITS.</span><span class="sxs-lookup"><span data-stu-id="7760c-109">In the **Add Features Wizard**, check BITS Server Extensions.</span></span> <span data-ttu-id="7760c-110">Обратите внимание, что необходимо установить роли совместимости управления IIS 6.</span><span class="sxs-lookup"><span data-stu-id="7760c-110">Note that the IIS 6 Management Compatibility roles must be installed.</span></span>

<span data-ttu-id="7760c-111">В Windows Server 2003 используйте **Мастер компонентов Windows** для установки расширения сервера BITS.</span><span class="sxs-lookup"><span data-stu-id="7760c-111">On Windows Server 2003, use the **Windows Components Wizard** to install the BITS server extension.</span></span> <span data-ttu-id="7760c-112">В **панели управления** выберите **Установка и удаление программ**.</span><span class="sxs-lookup"><span data-stu-id="7760c-112">From **Control Panel**, select **Add or Remove Programs**.</span></span> <span data-ttu-id="7760c-113">Затем выберите **Добавить или удалить компоненты Windows** , чтобы открыть **Мастер компонентов Windows**.</span><span class="sxs-lookup"><span data-stu-id="7760c-113">Then, select **Add/Remove Windows Components** to display the **Windows Components Wizard**.</span></span> <span data-ttu-id="7760c-114">Серверное расширение BITS является подкомпонентом службы IIS (IIS), который является подкомпонентом сервера веб-приложений.</span><span class="sxs-lookup"><span data-stu-id="7760c-114">The BITS server extension is a subcomponent of Internet Information Services (IIS) which is a sub-component of Web Application Server.</span></span>

> [!Note]  
> <span data-ttu-id="7760c-115">Если служба IISAdmin перезапущена, Рабочий процесс IIS необходимо перезапустить, прежде чем служба BITS сможет возобновить передачу.</span><span class="sxs-lookup"><span data-stu-id="7760c-115">If the IISAdmin service is restarted, the IIS worker process must be recycled before the BITS service can resume uploads.</span></span> <span data-ttu-id="7760c-116">Рабочий процесс IIS можно вручную перезапустить с помощью служебной программы командной строки **IISReset.exe** .</span><span class="sxs-lookup"><span data-stu-id="7760c-116">The IIS worker process can be manually recycled by using the **IISReset.exe** command line utility.</span></span>

 

<span data-ttu-id="7760c-117">Сведения о настройке служб IIS для отправки см. в разделе [Настройка сервера для отправки](setting-up-the-server-for-uploads.md).</span><span class="sxs-lookup"><span data-stu-id="7760c-117">For information on configuring IIS for uploads, see [Setting Up the Server for Uploads](setting-up-the-server-for-uploads.md).</span></span>

<span data-ttu-id="7760c-118">Дополнительные сведения о свойствах, которые служба BITS добавляет в IIS, см. в разделе [Параметры сервера BITS для заданий отправки](bits-server-settings-for-upload-jobs.md).</span><span class="sxs-lookup"><span data-stu-id="7760c-118">For details on the properties that BITS adds to IIS, see [BITS Server Settings for Upload Jobs](bits-server-settings-for-upload-jobs.md).</span></span>

 

 




