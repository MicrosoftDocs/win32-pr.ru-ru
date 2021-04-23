---
title: Пример классического приложения
description: Пример классического приложения
ms.assetid: 3736dd01-b02f-4056-b19b-0e7cc6c9aa67
keywords:
- Диспетчер устройств Windows Media, примеры
- Диспетчер устройств, примеры
- Классические приложения, примеры
- Windows Media диспетчер устройств, пример классического приложения
- Диспетчер устройств, пример классического приложения
- Пример приложения вмдмапп
- Примеры, классические приложения
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2f4008a25ca4448d4d4be7c9f667c5a9e4f08023
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104411002"
---
# <a name="sample-desktop-application"></a><span data-ttu-id="5afb4-110">Пример классического приложения</span><span class="sxs-lookup"><span data-stu-id="5afb4-110">Sample Desktop Application</span></span>

<span data-ttu-id="5afb4-111">Диспетчер устройств Windows Media поставляется с примером классического приложения под названием вмдмапп.</span><span class="sxs-lookup"><span data-stu-id="5afb4-111">The Windows Media Device Manager ships with a sample desktop application called wmdmapp.</span></span> <span data-ttu-id="5afb4-112">Это приложение имеет графический пользовательский интерфейс, позволяющий просматривать подключенные устройства, создавать списки воспроизведения на устройстве и перетаскивать файлы мультимедиа на устройство.</span><span class="sxs-lookup"><span data-stu-id="5afb4-112">This application has a graphical user interface that allows you to browse connected devices, create playlists on the device, and drag media files to the device.</span></span>

<span data-ttu-id="5afb4-113">Этот пример приложения состоит из двух частей:</span><span class="sxs-lookup"><span data-stu-id="5afb4-113">This sample application consists of two pieces:</span></span>

-   <span data-ttu-id="5afb4-114">wmdapp.exe, исполняемый файл, который отображает окно и выполняет большую часть пользовательского интерфейса и основных функций программы, и</span><span class="sxs-lookup"><span data-stu-id="5afb4-114">wmdapp.exe, an executable that displays a window and performs most of the user interface and basic functionality of the program, and</span></span>
-   <span data-ttu-id="5afb4-115">proghelp.dll, вспомогательная библиотека DLL, которая выполняет служебные функции для приложения.</span><span class="sxs-lookup"><span data-stu-id="5afb4-115">proghelp.dll, a helper DLL that performs utility functions for the application.</span></span> <span data-ttu-id="5afb4-116">Эту библиотеку DLL необходимо зарегистрировать после сборки проекта.</span><span class="sxs-lookup"><span data-stu-id="5afb4-116">You must register this DLL after building the project.</span></span>

<span data-ttu-id="5afb4-117">Чтобы скомпилировать пример приложения, можно использовать Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="5afb4-117">To compile the sample application, you can use Visual Studio.</span></span> <span data-ttu-id="5afb4-118">В следующем разделе описано, как это сделать.</span><span class="sxs-lookup"><span data-stu-id="5afb4-118">The following section describes how this is done:</span></span>

-   [<span data-ttu-id="5afb4-119">Компиляция примера приложения с помощью Visual Studio</span><span class="sxs-lookup"><span data-stu-id="5afb4-119">Compiling the Sample Application Using Visual Studio</span></span>](compiling-the-sample-application-using-visual-studio.md)

<span data-ttu-id="5afb4-120">После компиляции проекта зарегистрируйте файл proghelp.dll.</span><span class="sxs-lookup"><span data-stu-id="5afb4-120">After compiling the project, register the proghelp.dll file.</span></span> <span data-ttu-id="5afb4-121">Чтобы зарегистрировать эту библиотеку DLL, откройте командную строку и перейдите в каталог, содержащий эту библиотеку DLL, и введите `regsvr32 proghelp.dll` .</span><span class="sxs-lookup"><span data-stu-id="5afb4-121">To register this DLL, open a command prompt and browse to the directory containing this DLL and type `regsvr32 proghelp.dll`.</span></span>

 

 




