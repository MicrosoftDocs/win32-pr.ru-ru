---
description: Содержит сведения об интерфейсе программирования для службы настройки беспроводной связи в Windows XP и Windows Server 2003.
ms.assetid: cd9e8fc0-0a65-4654-95aa-201751183521
title: Ссылка на беспроводную конфигурацию 0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3ebe202e16aa38fef617f382559f124772d50a58
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104264375"
---
# <a name="wireless-zero-configuration-reference"></a><span data-ttu-id="0ba6e-103">Ссылка на беспроводную конфигурацию 0</span><span class="sxs-lookup"><span data-stu-id="0ba6e-103">Wireless Zero Configuration Reference</span></span>

<span data-ttu-id="0ba6e-104">\[Программный интерфейс беспроводных конфигураций больше не поддерживается в Windows Vista и Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="0ba6e-104">\[The Wireless Zero Configuration programming interface is no longer supported as of Windows Vista and Windows Server 2008.</span></span> <span data-ttu-id="0ba6e-105">Вместо этого используйте [собственный интерфейс API Wi-Fi](native-wifi-reference.md), который предоставляет аналогичные функциональные возможности.</span><span class="sxs-lookup"><span data-stu-id="0ba6e-105">Instead, use the [Native Wifi API](native-wifi-reference.md), which provides similar functionality.</span></span> <span data-ttu-id="0ba6e-106">Дополнительные сведения см. [в статье о встроенном API Wi-Fi](about-the-native-wifi-api.md).\]</span><span class="sxs-lookup"><span data-stu-id="0ba6e-106">For more information, see [About the Native Wifi API](about-the-native-wifi-api.md).\]</span></span>

<span data-ttu-id="0ba6e-107">В этом разделе содержатся сведения об интерфейсе программирования для службы настройки беспроводной связи в Windows XP и Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="0ba6e-107">This section contains information on the programming interface for the Wireless Zero Configuration service on Windows XP and Windows Server 2003.</span></span> <span data-ttu-id="0ba6e-108">Статьи:</span><span class="sxs-lookup"><span data-stu-id="0ba6e-108">The topics include:</span></span>

-   [<span data-ttu-id="0ba6e-109">Функции настройки беспроводной связи нуль</span><span class="sxs-lookup"><span data-stu-id="0ba6e-109">Wireless Zero Configuration Functions</span></span>](wireless-zero-configuration-functions.md)
-   [<span data-ttu-id="0ba6e-110">Беспроводные структуры конфигурации</span><span class="sxs-lookup"><span data-stu-id="0ba6e-110">Wireless Zero Configuration Structures</span></span>](wireless-zero-configuration-structures.md)

<span data-ttu-id="0ba6e-111">Беспроводная настройка — это служба Windows в Windows XP и Windows Server 2003, которая используется для настройки беспроводных сетевых подключений и управления ими на беспроводном адаптере.</span><span class="sxs-lookup"><span data-stu-id="0ba6e-111">Wireless Zero Configuration is a Windows service on Windows XP and Windows Server 2003 that is used to configure and manage wireless network connections on a wireless adapter.</span></span> <span data-ttu-id="0ba6e-112">Имя службы для беспроводной нулевой конфигурации — ВЗКСВК.</span><span class="sxs-lookup"><span data-stu-id="0ba6e-112">The service name for Wireless Zero Configuration is WZCSVC.</span></span> <span data-ttu-id="0ba6e-113">В Windows XP отображаемое имя для службы ВЗКСВК — беспроводная нулевая Настройка.</span><span class="sxs-lookup"><span data-stu-id="0ba6e-113">On Windows XP, the display name for the WZCSVC service is Wireless Zero Configuration.</span></span> <span data-ttu-id="0ba6e-114">В Windows Server 2003 отображаемое имя для службы ВЗКСВК — конфигурация беспроводной связи.</span><span class="sxs-lookup"><span data-stu-id="0ba6e-114">On Windows Server 2003, the display name for the WZCSVC service is Wireless Configuration.</span></span>

<span data-ttu-id="0ba6e-115">Служба настройки беспроводной связи обычно запускается во время загрузки.</span><span class="sxs-lookup"><span data-stu-id="0ba6e-115">The Wireless Zero Configuration service is normally started at boot time.</span></span> <span data-ttu-id="0ba6e-116">Интерфейс программирования для службы настройки беспроводной связи можно использовать, только если запущена служба настройки беспроводной связи.</span><span class="sxs-lookup"><span data-stu-id="0ba6e-116">The programming interface for the Wireless Zero Configuration service can be used only if the Wireless Zero Configuration service has been started.</span></span> <span data-ttu-id="0ba6e-117">Если служба настройки беспроводной связи не запущена, функции беспроводной настройки будут возвращать ошибку.</span><span class="sxs-lookup"><span data-stu-id="0ba6e-117">If the Wireless Zero Configuration service is not started, then the Wireless Zero Configuration functions will return an error.</span></span>

<span data-ttu-id="0ba6e-118">Чтобы включить службу настройки беспроводной связи, чтобы она автоматически запускалась, нажмите кнопку **Пуск** .</span><span class="sxs-lookup"><span data-stu-id="0ba6e-118">To enable the Wireless Zero Configuration service so it starts up automatically, go to the **Start** button.</span></span> <span data-ttu-id="0ba6e-119">Выберите параметр **Параметры** , а затем выберите **Панель управления**.</span><span class="sxs-lookup"><span data-stu-id="0ba6e-119">Select the **Settings** option and then select **Control Panel**.</span></span> <span data-ttu-id="0ba6e-120">Если вы используете представление Windows XP, выберите категорию **производительность и обслуживание** , а затем щелкните **Администрирование**.</span><span class="sxs-lookup"><span data-stu-id="0ba6e-120">If you are using the Windows XP view, select the **Performance and Maintenance** category and then select **Administrative Tools**.</span></span> <span data-ttu-id="0ba6e-121">Если используется классический вид, выберите **Администрирование**.</span><span class="sxs-lookup"><span data-stu-id="0ba6e-121">If you are using the Classic View, then select **Administrative Tools**.</span></span> <span data-ttu-id="0ba6e-122">Щелкните значок **службы** в левой области.</span><span class="sxs-lookup"><span data-stu-id="0ba6e-122">Click the **Services** icon in the left pane.</span></span> <span data-ttu-id="0ba6e-123">Щелкните значок беспроводной настройки на правой панели и измените **Тип запуска** Dropbox на **Автоматический**.</span><span class="sxs-lookup"><span data-stu-id="0ba6e-123">Click the Wireless Zero Configuration icon in the right pane and change the **Startup Type** dropbox to **Automatic**.</span></span> <span data-ttu-id="0ba6e-124">Этот параметр позволяет настроить автоматический запуск службы во время загрузки.</span><span class="sxs-lookup"><span data-stu-id="0ba6e-124">This setting will set the service to start automatically at boot time.</span></span> <span data-ttu-id="0ba6e-125">Затем нажмите кнопку **запустить** , чтобы запустить службу беспроводной нулевой настройки Wireless Zero и нажать кнопку **ОК** .</span><span class="sxs-lookup"><span data-stu-id="0ba6e-125">Then click the **Start** button to start the Wireless Zero Wireless Zero Configuration service and click the **OK** button.</span></span>

<span data-ttu-id="0ba6e-126">Беспроводную конфигурацию также можно запустить и остановить из командной строки.</span><span class="sxs-lookup"><span data-stu-id="0ba6e-126">The Wireless Zero Configuration can also be started and stopped from a command prompt.</span></span> <span data-ttu-id="0ba6e-127">Чтобы запустить беспроводную конфигурацию, выполните следующую команду:</span><span class="sxs-lookup"><span data-stu-id="0ba6e-127">To start the Wireless Zero Configuration, run the following command:</span></span>

<span data-ttu-id="0ba6e-128">**NET start взксвк**</span><span class="sxs-lookup"><span data-stu-id="0ba6e-128">**net start wzcsvc**</span></span>

<span data-ttu-id="0ba6e-129">Чтобы отключить беспроводную конфигурацию, выполните следующую команду:</span><span class="sxs-lookup"><span data-stu-id="0ba6e-129">To stop the Wireless Zero Configuration, run the following command:</span></span>

<span data-ttu-id="0ba6e-130">**NET взксвк**</span><span class="sxs-lookup"><span data-stu-id="0ba6e-130">**net stop wzcsvc**</span></span>

 

 



