---
title: Компиляция примера приложения с помощью Visual Studio
description: Компиляция примера приложения с помощью Visual Studio
ms.assetid: 78345cdb-5f0d-4ea8-9492-30386f5fa6ee
keywords:
- Диспетчер устройств Windows Media, примеры
- Диспетчер устройств, примеры
- Классические приложения, примеры
- Windows Media диспетчер устройств, пример классического приложения
- Диспетчер устройств, пример классического приложения
- Примеры, классические приложения
- Примеры, компиляция с помощью Visual Studio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cf47f7a45ad17711145df810926fafb0f2aedcec
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104067744"
---
# <a name="compiling-the-sample-application-using-visual-studio"></a><span data-ttu-id="9fd58-110">Компиляция примера приложения с помощью Visual Studio</span><span class="sxs-lookup"><span data-stu-id="9fd58-110">Compiling the Sample Application Using Visual Studio</span></span>

<span data-ttu-id="9fd58-111">Пакет Windows Media диспетчер устройств SDK включает решение Visual Studio, совместимое с Microsoft Visual Studio 2005.</span><span class="sxs-lookup"><span data-stu-id="9fd58-111">The Windows Media Device Manager SDK includes a Visual Studio solution that is compatible with Microsoft Visual Studio 2005.</span></span>

<span data-ttu-id="9fd58-112">Перед компиляцией примера приложения необходимо переименовать файл заголовка штипес. h, чтобы избежать конфликтов с файлом с тем же именем, который находится в пакете Microsoft Platform SDK.</span><span class="sxs-lookup"><span data-stu-id="9fd58-112">Before you compile the sample application, you must rename the header file shtypes.h to prevent conflicts with a file of the same name that is found in the Microsoft Platform SDK.</span></span> <span data-ttu-id="9fd58-113">Например, можно переименовать <*путь установки пакета SDK* > \\ WMFSDK11 \\ включить \\ штипес. h в *путь установки пакета SDK* для <> \\ WMFSDK11 \\ включить \\ штипес. h. Backup.</span><span class="sxs-lookup"><span data-stu-id="9fd58-113">For example, you could rename <*SDK Installation Path*>\\WMFSDK11\\include\\shtypes.h to <*SDK Installation Path*>\\WMFSDK11\\include\\shtypes.h.backup.</span></span>

<span data-ttu-id="9fd58-114">Чтобы создать приложение, запустите экземпляр Visual Studio 2005, откройте файл решения вмдмапп. sln, который находится в папке <*пакета SDK путь установки* > \\ WMFSDK11 \\ приложения \\ вмдмапп и выберите параметр **Сборка/Сборка решения** .</span><span class="sxs-lookup"><span data-stu-id="9fd58-114">To build the application, start an instance of Visual Studio 2005, open the solution file, wmdmapp.sln, which is found in the folder <*SDK installation path*>\\WMFSDK11\\apps\\wmdmapp and choose the **Build/Build Solution** option.</span></span> <span data-ttu-id="9fd58-115">При этом будут созданы два файла проекта: вспомогательный проект, прогхелп. vcproj, а также основное приложение вмдмапп. vcproj.</span><span class="sxs-lookup"><span data-stu-id="9fd58-115">This will create two project files: the helper project, proghelp.vcproj, as well as the main application wmdmapp.vcproj.</span></span> <span data-ttu-id="9fd58-116">Кроме того, он создаст вспомогательную библиотеку DLL хода выполнения и основное приложение (WMDMApp.exe).</span><span class="sxs-lookup"><span data-stu-id="9fd58-116">In addition, it will create the progress helper DLL and the main application (WMDMApp.exe).</span></span>

## <a name="related-topics"></a><span data-ttu-id="9fd58-117">См. также</span><span class="sxs-lookup"><span data-stu-id="9fd58-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9fd58-118">**Пример классического приложения**</span><span class="sxs-lookup"><span data-stu-id="9fd58-118">**Sample Desktop Application**</span></span>](sample-desktop-application.md)
</dt> </dl>

 

 




