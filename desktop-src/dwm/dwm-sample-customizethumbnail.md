---
title: Настройка эскиза значка и растрового изображения для динамического предварительного просмотра
description: В этом примере показано, как настроить эскиз значка и динамический предварительный просмотр изображения (также называемый предварительным просмотром).
ms.assetid: 43fe71e7-4e5c-46fb-876b-e26996071665
ms.topic: article
ms.date: 05/31/2018
ms.custom: project-verbatim
ms.openlocfilehash: 8fceb94727257b51a2e6235cbfcc44b155635343
ms.sourcegitcommit: af120ad5c30da2fc5eb717ca2a1c4c45878efd71
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/20/2021
ms.locfileid: "105714070"
---
# <a name="customize-an-iconic-thumbnail-and-a-live-preview-bitmap"></a><span data-ttu-id="0c678-103">Настройка эскиза значка и растрового изображения для динамического предварительного просмотра</span><span class="sxs-lookup"><span data-stu-id="0c678-103">Customize an Iconic Thumbnail and a Live Preview Bitmap</span></span>

## <a name="description"></a><span data-ttu-id="0c678-104">Описание</span><span class="sxs-lookup"><span data-stu-id="0c678-104">Description</span></span>

<span data-ttu-id="0c678-105">Точечный эскиз и *динамический просмотр* (или *Предварительный просмотр*) можно настроить с помощью функций и сообщений, представленных в API-интерфейсах Windows 7 диспетчер окон рабочего стола (DWM).</span><span class="sxs-lookup"><span data-stu-id="0c678-105">You can customize an iconic thumbnail and a *live preview* (or *Peek preview*) bitmap by using functions and messages that are introduced in the Windows 7 Desktop Window Manager (DWM) APIs.</span></span>

<span data-ttu-id="0c678-106">В частности, вы используете функцию [**двмсетикониксумбнаил**](/windows/win32/api/Dwmapi/nf-dwmapi-dwmseticonicthumbnail) и сообщение [**WM \_ сендикониксумбнаилбитмап**](wm-dwmsendiconicthumbnail.md) для настройки эскиза значка.</span><span class="sxs-lookup"><span data-stu-id="0c678-106">Specifically, you use the [**DwmSetIconicThumbnail**](/windows/win32/api/Dwmapi/nf-dwmapi-dwmseticonicthumbnail) function and the [**WM\_SENDICONICTHUMBNAILBITMAP**](wm-dwmsendiconicthumbnail.md) message to customize an iconic thumbnail.</span></span> <span data-ttu-id="0c678-107">Вы также можете использовать функцию [**двмсетиконикливепревиевбитмап**](/windows/win32/api/Dwmapi/nf-dwmapi-dwmseticoniclivepreviewbitmap) и сообщение [**WM \_ сендиконикливепревиевбитмап**](wm-dwmsendiconiclivepreviewbitmap.md) для установки значка точечного рисунка динамического предварительного просмотра.</span><span class="sxs-lookup"><span data-stu-id="0c678-107">You can also use the [**DwmSetIconicLivePreviewBitmap**](/windows/win32/api/Dwmapi/nf-dwmapi-dwmseticoniclivepreviewbitmap) function and the [**WM\_SENDICONICLIVEPREVIEWBITMAP**](wm-dwmsendiconiclivepreviewbitmap.md) message to set an iconic live preview bitmap.</span></span>

<span data-ttu-id="0c678-108">Пример приложения, использующего функцию **двмсетикониксумбнаил** , см. в разделе [Пример табсумбнаилс](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/shell/appshellintegration/TabThumbnails).</span><span class="sxs-lookup"><span data-stu-id="0c678-108">For a sample application that uses the **DwmSetIconicThumbnail** function, see [TabThumbnails sample](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/shell/appshellintegration/TabThumbnails).</span></span>

<span data-ttu-id="0c678-109">На следующем рисунке показан эскиз по умолчанию, преобразованный в настроенный эскиз.</span><span class="sxs-lookup"><span data-stu-id="0c678-109">The following illustration shows a default thumbnail transformed into a customized thumbnail.</span></span>

![Иллюстрация исходного эскиза и измененного эскиза с пользовательским растровым изображением](images/customthumbnail.jpg)

## <a name="requirements"></a><span data-ttu-id="0c678-111">Требования</span><span class="sxs-lookup"><span data-stu-id="0c678-111">Requirements</span></span>

| <span data-ttu-id="0c678-112">Требование</span><span class="sxs-lookup"><span data-stu-id="0c678-112">Requirement</span></span> | <span data-ttu-id="0c678-113">Значение</span><span class="sxs-lookup"><span data-stu-id="0c678-113">Value</span></span> |
|--------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0c678-114">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="0c678-114">Minimum supported client</span></span> | <span data-ttu-id="0c678-115">Windows 7 или Windows Vista с пакетом обновления 2 (SP2) и обновлением платформы для Windows Vista</span><span class="sxs-lookup"><span data-stu-id="0c678-115">Windows 7 or Windows Vista with Service Pack 2 (SP2) and Platform Update for Windows Vista</span></span>                          |
| <span data-ttu-id="0c678-116">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="0c678-116">Minimum supported server</span></span> | <span data-ttu-id="0c678-117">Windows Server 2008 R2 или Windows Server 2008 с пакетом обновления 2 (SP2) и обновлением платформы для Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="0c678-117">Windows Server 2008 R2 or Windows Server 2008 with Service Pack 2 (SP2) and Platform Update for Windows Server 2008</span></span> |
| <span data-ttu-id="0c678-118">Минимальное Windows SDK</span><span class="sxs-lookup"><span data-stu-id="0c678-118">Minimum Windows SDK</span></span>      | [<span data-ttu-id="0c678-119">Пакет средств разработки программного обеспечения (SDK) для Windows 7</span><span class="sxs-lookup"><span data-stu-id="0c678-119">Windows Software Development Kit (SDK) for Windows 7</span></span>](https://msdn.microsoft.com/windows/bb980924.aspx)             |

## <a name="building-the-tabthumbnails-sample"></a><span data-ttu-id="0c678-120">Создание образца Табсумбнаилс</span><span class="sxs-lookup"><span data-stu-id="0c678-120">Building the TabThumbnails sample</span></span>

<span data-ttu-id="0c678-121">**Построение образца с помощью Microsoft Visual Studio (предпочтительный метод)**</span><span class="sxs-lookup"><span data-stu-id="0c678-121">**To build the sample by using Microsoft Visual Studio (preferred method)**</span></span>

1.  <span data-ttu-id="0c678-122">Откройте проводник Windows и перейдите в папку, где находится файл Табсумбнаилс. sln.</span><span class="sxs-lookup"><span data-stu-id="0c678-122">Open Windows Explorer and browse to the folder where the TabThumbnails.sln file is located.</span></span>
2.  <span data-ttu-id="0c678-123">Дважды щелкните файл решения (SLN), чтобы открыть его в Microsoft Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="0c678-123">Double-click the solution file (.sln) to open the file in Microsoft Visual Studio.</span></span>
3.  <span data-ttu-id="0c678-124">В меню **Сборка** выберите **Собрать решение**.</span><span class="sxs-lookup"><span data-stu-id="0c678-124">On the **Build** menu, click **Build Solution**.</span></span> <span data-ttu-id="0c678-125">Приложение строится в \\ каталоге отладки или выпуска по умолчанию \\ .</span><span class="sxs-lookup"><span data-stu-id="0c678-125">The application is built in the default \\Debug or \\Release directory.</span></span>

<span data-ttu-id="0c678-126">**Построение образца с помощью командной строки**</span><span class="sxs-lookup"><span data-stu-id="0c678-126">**To build the sample by using the command prompt**</span></span>

1.  <span data-ttu-id="0c678-127">Откройте окно командной строки и перейдите к каталогу примеров.</span><span class="sxs-lookup"><span data-stu-id="0c678-127">Open a Command Prompt window and browse to the sample directory.</span></span>
2.  <span data-ttu-id="0c678-128">Введите `msbuild TabThumbnails.sln`.</span><span class="sxs-lookup"><span data-stu-id="0c678-128">Enter `msbuild TabThumbnails.sln`.</span></span>

## <a name="related-topics"></a><span data-ttu-id="0c678-129">См. также</span><span class="sxs-lookup"><span data-stu-id="0c678-129">Related topics</span></span>

[<span data-ttu-id="0c678-130">Диспетчер окон рабочего стола</span><span class="sxs-lookup"><span data-stu-id="0c678-130">Desktop Window Manager</span></span>](dwm-overview.md)

[<span data-ttu-id="0c678-131">Разработка для Windows</span><span class="sxs-lookup"><span data-stu-id="0c678-131">Windows Development</span></span>](/windows/desktop/win32-and-com-development)
