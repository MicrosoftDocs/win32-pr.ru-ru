---
title: Использование примера классического приложения
description: Использование примера классического приложения
ms.assetid: 5e3e5283-9e27-4f6a-93a9-84d84f2e875a
keywords:
- Диспетчер устройств Windows Media, примеры
- Диспетчер устройств, примеры
- Классические приложения, примеры
- Windows Media диспетчер устройств, пример классического приложения
- Диспетчер устройств, пример классического приложения
- Примеры, классические приложения
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bd511ea5241f458d2cd926dc8fb2f3681757ff8b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103774282"
---
# <a name="using-the-sample-desktop-application"></a><span data-ttu-id="c1086-109">Использование примера классического приложения</span><span class="sxs-lookup"><span data-stu-id="c1086-109">Using the Sample Desktop Application</span></span>

<span data-ttu-id="c1086-110">Пример классического приложения — это простое окно с двумя панелями, которое, в своюмся, выглядит как проводник Windows.</span><span class="sxs-lookup"><span data-stu-id="c1086-110">The sample desktop application is a basic two-paned window somewhat like Windows Explorer.</span></span> <span data-ttu-id="c1086-111">Она позволяет просматривать содержимое устройства, используя древовидное представление папок в левой области, а также файлы на правой панели.</span><span class="sxs-lookup"><span data-stu-id="c1086-111">It allows you to browse the contents of a device, using a tree view display of folders in the left pane, and files in the right pane.</span></span> <span data-ttu-id="c1086-112">Корневой каталог каждого дерева папок логически считается другим устройством, хотя некоторые устройства могут представлять себя как несколько объектов (по одному для каждого корневого хранилища).</span><span class="sxs-lookup"><span data-stu-id="c1086-112">The root of each folder tree is logically considered a different device, although some devices might represent themselves as several objects (one for each root storage).</span></span> <span data-ttu-id="c1086-113">Чтобы прочитать основные свойства папки или файла, щелкните объект правой кнопкой мыши и выберите пункт **Свойства**.</span><span class="sxs-lookup"><span data-stu-id="c1086-113">To read the basic properties of either a folder or a file, right-click the object and select **Properties**.</span></span>

<span data-ttu-id="c1086-114">Вы можете удалить файлы на устройстве, выбрав файл в правой области и выбрав пункт **Удалить** в меню **файл** .</span><span class="sxs-lookup"><span data-stu-id="c1086-114">You can delete files on the device by selecting a file in the right pane and selecting **Delete** on the **File** menu.</span></span> <span data-ttu-id="c1086-115">Чтобы добавить файлы мультимедиа на устройство, можно перетащить файлы с рабочего стола на правую панель программы.</span><span class="sxs-lookup"><span data-stu-id="c1086-115">To add media files to the device, you can drag files from the desktop onto the right pane of the program.</span></span> <span data-ttu-id="c1086-116">Обратите внимание, что файлы должны иметь формат мультимедиа, поддерживаемый устройством. файлы неприемлемых форматов (не являющихся файлами мультимедиа, например TXT-файлами или форматами мультимедиа, которые не поддерживаются устройством) не будут отправляться на устройство.</span><span class="sxs-lookup"><span data-stu-id="c1086-116">Note that files must be of a media format supported by the device; files of unacceptable formats (non-media files such as .txt files, or media formats not supported by the device) will not be sent to the device.</span></span> <span data-ttu-id="c1086-117">(Обратите внимание, что это ограничение является программой; Windows Media диспетчер устройств позволяет отправить любой файл на устройство, если оно будет принято устройством.)</span><span class="sxs-lookup"><span data-stu-id="c1086-117">(Note that this restriction is the program's; Windows Media Device Manager enables you to send any file to a device if the device will accept it.)</span></span>

<span data-ttu-id="c1086-118">Для записи событий обратного вызова, отправленных в интерфейс [**ивмдмоператион**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmoperation) , необходимо установить флажок "использовать интерфейс операции" в меню " **Параметры** ".</span><span class="sxs-lookup"><span data-stu-id="c1086-118">To capture callback events sent to the [**IWMDMOperation**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmoperation) interface, you must check the "Use Operation Interface" option in the **Options** menu.</span></span>

<span data-ttu-id="c1086-119">В меню **Параметры** также можно выбрать, следует ли использовать несколько дополнительных интерфейсов с функциями, поддерживаемыми дополнительными устройствами.</span><span class="sxs-lookup"><span data-stu-id="c1086-119">The **Options** menu also enables you to choose whether to use several more advanced interfaces with features supported by advanced devices.</span></span>

<span data-ttu-id="c1086-120">Меню **контейнеры** содержит параметры, позволяющие создать список воспроизведения или альбом.</span><span class="sxs-lookup"><span data-stu-id="c1086-120">The **Containers** menu has options to allow you to create a playlist or an album.</span></span> <span data-ttu-id="c1086-121">Чтобы создать список воспроизведения, выберите одну или несколько песен на устройстве и щелкните **создать список воспроизведения** в меню **контейнеры** .</span><span class="sxs-lookup"><span data-stu-id="c1086-121">To create a playlist, select one or more songs on the device and click **Create Playlist** on the **Containers** menu.</span></span> <span data-ttu-id="c1086-122">Эта функция работает только на устройствах MTP, так как код поддерживает только создание "виртуального" файла списка воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="c1086-122">This feature only works on MTP devices, because the code only supports the creation of an "virtual" playlist file.</span></span> <span data-ttu-id="c1086-123">(Виртуальный список воспроизведения — это список воспроизведения, который задается только значениями метаданных, а не физическим файлом, например WPL-файлом.) Для использования этой функции устройство должно поддерживать пустые списки воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="c1086-123">(A virtual playlist is a playlist that is specified only by metadata values, rather than by a physical file, for example a WPL file.) The device must support empty playlists to use this feature.</span></span>

<span data-ttu-id="c1086-124">Чтобы создать альбом (список воспроизведения со связанным изображением), выберите одну или несколько песен на устройстве и щелкните **создать альбом** в меню **контейнеры** .</span><span class="sxs-lookup"><span data-stu-id="c1086-124">To create an album (a playlist with an associated image), select one or more songs on the device and click **Create Album** on the **Containers** menu.</span></span> <span data-ttu-id="c1086-125">Диалоговое окно позволяет перейти к файлу изображения на компьютере, чтобы связать его с альбомом.</span><span class="sxs-lookup"><span data-stu-id="c1086-125">A dialog box allows you to browse to a picture file on your computer to associate with the album.</span></span> <span data-ttu-id="c1086-126">Аналогично тому, как он создает списки воспроизведения, приложение создает пустой файл альбома. Если устройство не поддерживает пустые альбомы, этот компонент работать не будет.</span><span class="sxs-lookup"><span data-stu-id="c1086-126">Similarly to the way it creates playlists, the application creates an "empty" album file; if the device does not support empty albums, this feature will not work.</span></span>

## <a name="related-topics"></a><span data-ttu-id="c1086-127">См. также</span><span class="sxs-lookup"><span data-stu-id="c1086-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c1086-128">**Пример классического приложения**</span><span class="sxs-lookup"><span data-stu-id="c1086-128">**Sample Desktop Application**</span></span>](sample-desktop-application.md)
</dt> </dl>

 

 




