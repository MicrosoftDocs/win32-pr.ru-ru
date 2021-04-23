---
description: Демонстрирует использование \_ интерфейсов API командной консоли NotifyIcon и оболочки \_ нотификонжетрект для отображения значка уведомления.
title: Пример NotificationIcon
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 9F31DB2D-4B12-4f65-AC91-25B4B5B1CB46
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 1569d162aef358130910081bee80354cb64f690d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104985577"
---
# <a name="notificationicon-sample"></a><span data-ttu-id="3d7b6-103">Пример NotificationIcon</span><span class="sxs-lookup"><span data-stu-id="3d7b6-103">NotificationIcon Sample</span></span>

<span data-ttu-id="3d7b6-104">Демонстрирует использование интерфейсов API [**командной консоли \_ NotifyIcon**](/windows/desktop/api/Shellapi/nf-shellapi-shell_notifyicona) и [**оболочки \_ нотификонжетрект**](/windows/desktop/api/Shellapi/nf-shellapi-shell_notifyicongetrect) для отображения значка уведомления.</span><span class="sxs-lookup"><span data-stu-id="3d7b6-104">Demonstrates how to use the [**Shell\_NotifyIcon**](/windows/desktop/api/Shellapi/nf-shellapi-shell_notifyicona) and [**Shell\_NotifyIconGetRect**](/windows/desktop/api/Shellapi/nf-shellapi-shell_notifyicongetrect) APIs to display a notification icon.</span></span>

<span data-ttu-id="3d7b6-105">В этом разделе содержатся следующие подразделы.</span><span class="sxs-lookup"><span data-stu-id="3d7b6-105">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="3d7b6-106">Описание</span><span class="sxs-lookup"><span data-stu-id="3d7b6-106">Description</span></span>](#description)
-   [<span data-ttu-id="3d7b6-107">Требования</span><span class="sxs-lookup"><span data-stu-id="3d7b6-107">Requirements</span></span>](#requirements)
-   [<span data-ttu-id="3d7b6-108">Загрузка образца</span><span class="sxs-lookup"><span data-stu-id="3d7b6-108">Downloading the Sample</span></span>](#downloading-the-sample)
-   [<span data-ttu-id="3d7b6-109">Создание примера</span><span class="sxs-lookup"><span data-stu-id="3d7b6-109">Building the Sample</span></span>](#building-the-sample)
-   [<span data-ttu-id="3d7b6-110">Запуск примера</span><span class="sxs-lookup"><span data-stu-id="3d7b6-110">Running the Sample</span></span>](#running-the-sample)

## <a name="description"></a><span data-ttu-id="3d7b6-111">Описание</span><span class="sxs-lookup"><span data-stu-id="3d7b6-111">Description</span></span>

<span data-ttu-id="3d7b6-112">Кроме того, чтобы отобразить значок уведомления, в этом примере также демонстрируется отображение форматированного всплывающего окна, контекстного меню и всплывающего уведомления в дополнение к использованию [**оболочки \_ NotifyIcon**](/windows/desktop/api/Shellapi/nf-shellapi-shell_notifyicona) и [**\_ нотификонжетрект оболочки**](/windows/desktop/api/Shellapi/nf-shellapi-shell_notifyicongetrect) .</span><span class="sxs-lookup"><span data-stu-id="3d7b6-112">In addition to the use of [**Shell\_NotifyIcon**](/windows/desktop/api/Shellapi/nf-shellapi-shell_notifyicona) and [**Shell\_NotifyIconGetRect**](/windows/desktop/api/Shellapi/nf-shellapi-shell_notifyicongetrect) to display a notification icon, this sample also demonstrates how to display a rich flyout window, context menu, and balloon notification.</span></span>

> [!Note]  
> <span data-ttu-id="3d7b6-113">[**Оболочка \_ Нотификонжетрект**](/windows/desktop/api/Shellapi/nf-shellapi-shell_notifyicongetrect) доступен только в Windows 7 и более поздних версиях.</span><span class="sxs-lookup"><span data-stu-id="3d7b6-113">[**Shell\_NotifyIconGetRect**](/windows/desktop/api/Shellapi/nf-shellapi-shell_notifyicongetrect) is only available on Windows 7 and later versions.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="3d7b6-114">Требования</span><span class="sxs-lookup"><span data-stu-id="3d7b6-114">Requirements</span></span>



| <span data-ttu-id="3d7b6-115">Продукт</span><span class="sxs-lookup"><span data-stu-id="3d7b6-115">Product</span></span>                                | <span data-ttu-id="3d7b6-116">Минимальная версия продукта</span><span class="sxs-lookup"><span data-stu-id="3d7b6-116">Minimum Product Version</span></span> |
|----------------------------------------|-------------------------|
| <span data-ttu-id="3d7b6-117">Windows</span><span class="sxs-lookup"><span data-stu-id="3d7b6-117">Windows</span></span>                                | <span data-ttu-id="3d7b6-118">Windows 7</span><span class="sxs-lookup"><span data-stu-id="3d7b6-118">Windows 7</span></span>               |
| <span data-ttu-id="3d7b6-119">Windows SDK</span><span class="sxs-lookup"><span data-stu-id="3d7b6-119">Windows Software Development Kit (SDK)</span></span> | <span data-ttu-id="3d7b6-120">7.0</span><span class="sxs-lookup"><span data-stu-id="3d7b6-120">7.0</span></span>                     |



 

## <a name="downloading-the-sample"></a><span data-ttu-id="3d7b6-121">Загрузка образца</span><span class="sxs-lookup"><span data-stu-id="3d7b6-121">Downloading the Sample</span></span>

| <span data-ttu-id="3d7b6-122">Расположение</span><span class="sxs-lookup"><span data-stu-id="3d7b6-122">Location</span></span>      | <span data-ttu-id="3d7b6-123">URL-адрес пути</span><span class="sxs-lookup"><span data-stu-id="3d7b6-123">Path URL</span></span>                                                                                             |
|---------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3d7b6-124">GitHub</span><span class="sxs-lookup"><span data-stu-id="3d7b6-124">GitHub</span></span>  | [<span data-ttu-id="3d7b6-125">Пример Нотификатионикон</span><span class="sxs-lookup"><span data-stu-id="3d7b6-125">NotificationIcon sample</span></span>](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/shell/appshellintegration/NotificationIcon) |

## <a name="building-the-sample"></a><span data-ttu-id="3d7b6-126">Построение образца</span><span class="sxs-lookup"><span data-stu-id="3d7b6-126">Building the Sample</span></span>

<span data-ttu-id="3d7b6-127">Чтобы построить образец из командной строки, выполните следующую команду:</span><span class="sxs-lookup"><span data-stu-id="3d7b6-127">To build the sample from the command prompt:</span></span>

1.  <span data-ttu-id="3d7b6-128">Откройте окно командной строки и перейдите в каталог проекта **нотификатионикон** .</span><span class="sxs-lookup"><span data-stu-id="3d7b6-128">Open the command prompt window and navigate to the **NotificationIcon** project directory.</span></span>
2.  <span data-ttu-id="3d7b6-129">Введите `msbuild NotificationIcon.sln`.</span><span class="sxs-lookup"><span data-stu-id="3d7b6-129">Enter `msbuild NotificationIcon.sln`.</span></span>

<span data-ttu-id="3d7b6-130">Чтобы создать пример с использованием Microsoft Visual Studio (предпочтительно):</span><span class="sxs-lookup"><span data-stu-id="3d7b6-130">To build the sample using Microsoft Visual Studio (preferred):</span></span>

1.  <span data-ttu-id="3d7b6-131">Откройте проводник Windows и перейдите в каталог проекта **нотификатионикон** .</span><span class="sxs-lookup"><span data-stu-id="3d7b6-131">Open Windows Explorer and navigate to the **NotificationIcon** project directory.</span></span>
2.  <span data-ttu-id="3d7b6-132">Дважды щелкните значок файла Нотификатионикон. sln, чтобы открыть проект в Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="3d7b6-132">Double-click the icon for the NotificationIcon.sln file to open the project in Visual Studio.</span></span>
3.  <span data-ttu-id="3d7b6-133">В меню **Сборка** выберите пункт **построить решение**.</span><span class="sxs-lookup"><span data-stu-id="3d7b6-133">From the **Build** menu, select **Build Solution**.</span></span>

## <a name="running-the-sample"></a><span data-ttu-id="3d7b6-134">Запуск примера</span><span class="sxs-lookup"><span data-stu-id="3d7b6-134">Running the Sample</span></span>

1.  <span data-ttu-id="3d7b6-135">Перейдите в каталог, содержащий новый исполняемый файл, с помощью командной строки или проводника Windows.</span><span class="sxs-lookup"><span data-stu-id="3d7b6-135">Navigate to the directory that contains the new executable, using the command prompt or Windows Explorer.</span></span>
2.  <span data-ttu-id="3d7b6-136">В командной строке введите `NotificationIcon.exe` .</span><span class="sxs-lookup"><span data-stu-id="3d7b6-136">At the command line, enter `NotificationIcon.exe`.</span></span> <span data-ttu-id="3d7b6-137">Кроме того, в проводнике Windows дважды щелкните значок NotificationIcon.exe.</span><span class="sxs-lookup"><span data-stu-id="3d7b6-137">Alternatively, from Windows Explorer double-click the icon for NotificationIcon.exe.</span></span>

> [!Note]  
> <span data-ttu-id="3d7b6-138">Значки уведомлений, заданные с помощью идентификатора GUID, защищаются от подмены путем проверки того, что они регистрируются только одним приложением.</span><span class="sxs-lookup"><span data-stu-id="3d7b6-138">Notification icons specified with a GUID are protected against spoofing by validating that only a single application registers them.</span></span> <span data-ttu-id="3d7b6-139">Эта регистрация выполняется при первом вызове оболочки \_ NotifyIcon (ним \_ Add,...) и сохранении полного пути вызывающего приложения.</span><span class="sxs-lookup"><span data-stu-id="3d7b6-139">This registration is performed the first time you call Shell\_NotifyIcon(NIM\_ADD, ...) and the full path name of the calling application is stored.</span></span> <span data-ttu-id="3d7b6-140">Если позже вы переместит двоичный файл в другое расположение, система не разрешит добавить значок снова.</span><span class="sxs-lookup"><span data-stu-id="3d7b6-140">If you later move your binary file to a different location, the system will not allow the icon to be added again.</span></span> <span data-ttu-id="3d7b6-141">Дополнительные сведения см. в разделе [**оболочка \_ NotifyIcon**](/windows/desktop/api/Shellapi/nf-shellapi-shell_notifyicona) .</span><span class="sxs-lookup"><span data-stu-id="3d7b6-141">Please see [**Shell\_NotifyIcon**](/windows/desktop/api/Shellapi/nf-shellapi-shell_notifyicona) for more information.</span></span>

 

 

 



