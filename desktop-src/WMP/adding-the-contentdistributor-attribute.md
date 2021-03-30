---
title: Добавление атрибута Контентдистрибутор
description: Добавление атрибута Контентдистрибутор
ms.assetid: b4ba5c9b-f28f-4275-bd39-c0ad1080d122
keywords:
- Интернет-магазины проигрывателя Windows Media, добавление атрибута Контентдистрибутор
- Интернет-магазины, добавление атрибута Контентдистрибутор
- Тип 1 Интернет-магазины, добавление атрибута Контентдистрибутор
- Тип 2 Интернет-магазинов, добавление атрибута Контентдистрибутор
- Интернет-магазины проигрывателя Windows Media, атрибут Контентдистрибутор
- Интернет-магазины, атрибут Контентдистрибутор
- Тип 1 Интернет-магазины, атрибут Контентдистрибутор
- Тип 2 Интернет-магазинов, атрибут Контентдистрибутор
- Добавление атрибута Контентдистрибутор
- контентдистрибутор
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1636c002affbcf1235283a22f7eb060c75f24a81
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104330099"
---
# <a name="adding-the-contentdistributor-attribute"></a><span data-ttu-id="b6754-113">Добавление атрибута Контентдистрибутор</span><span class="sxs-lookup"><span data-stu-id="b6754-113">Adding the ContentDistributor Attribute</span></span>

<span data-ttu-id="b6754-114">Когда пользователь пытается воспроизвести содержимое в Интернет-магазине или скопировать содержимое на компакт-диск или устройство, проигрыватель Windows Media вызывает определенные методы в COM-объекте.</span><span class="sxs-lookup"><span data-stu-id="b6754-114">When the user attempts to play online store content or to copy the content to a CD or device, Windows Media Player calls certain methods in your COM object.</span></span> <span data-ttu-id="b6754-115">Для этого проигрывателю требуется способ отличить содержимое от других поставщиков Интернет-магазинов.</span><span class="sxs-lookup"><span data-stu-id="b6754-115">To do this, the Player needs a way to differentiate your content from that of other online store providers.</span></span> <span data-ttu-id="b6754-116">Добавив имя ключа Интернет-магазина в качестве значения параметра **контентдистрибутор** (который является псевдонимом атрибута **WM/Контентдистрибутор** пакета SDK Windows Media Format) для содержимого на основе Windows Media, вы убедитесь, что проигрыватель может опознать содержимое, связанное со службой.</span><span class="sxs-lookup"><span data-stu-id="b6754-116">By adding your online store key name as the value for the **ContentDistributor** (which is an alias for the Windows Media Format SDK attribute named **WM/ContentDistributor**) attribute to your Windows Media-based content, you ensure that the Player can identify the content associated with your service.</span></span>

<span data-ttu-id="b6754-117">Добавление значения для **контентдистрибутор** также гарантирует, что проигрыватель Windows Media создаст узел в библиотеке для предоставленного содержимого.</span><span class="sxs-lookup"><span data-stu-id="b6754-117">Adding a value for **ContentDistributor** also ensures that Windows Media Player will create a node in the library for content you provide.</span></span> <span data-ttu-id="b6754-118">См. раздел [Интеграция библиотеки](library-integration.md).</span><span class="sxs-lookup"><span data-stu-id="b6754-118">See [Library Integration](library-integration.md).</span></span>

<span data-ttu-id="b6754-119">Это значение можно указать двумя способами.</span><span class="sxs-lookup"><span data-stu-id="b6754-119">You can specify this value two ways:</span></span>

-   <span data-ttu-id="b6754-120">Используйте объектную модель проигрывателя Windows Media.</span><span class="sxs-lookup"><span data-stu-id="b6754-120">Use the Windows Media Player object model.</span></span> <span data-ttu-id="b6754-121">При этом проигрыватель Windows Media добавляет указанное значение в базу данных библиотеки.</span><span class="sxs-lookup"><span data-stu-id="b6754-121">When you do this, Windows Media Player adds the value you specify to the library database.</span></span> <span data-ttu-id="b6754-122">В конечном итоге проигрыватель также запишет значение атрибута в файл цифрового мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="b6754-122">Eventually, the Player will also write the attribute value to the digital media file.</span></span>
-   <span data-ttu-id="b6754-123">Используйте пакет SDK Windows Media Format для программного добавления атрибута **WM/контентдистрибутор** .</span><span class="sxs-lookup"><span data-stu-id="b6754-123">Use the Windows Media Format SDK to programmatically add the **WM/ContentDistributor** attribute.</span></span> <span data-ttu-id="b6754-124">При этом проигрыватель Windows Media считывает значение атрибута и добавляет его в базу данных при добавлении файла цифрового мультимедиа в библиотеку.</span><span class="sxs-lookup"><span data-stu-id="b6754-124">When you do this, Windows Media Player reads the attribute value and adds it to the database when the digital media file is added to the library.</span></span>

<span data-ttu-id="b6754-125">При создании COM-объекта Интернет-магазина значение атрибута File, заданное для **контентдистрибутор** , и значение, присваиваемое константе Ксзконтентдистрибуторид в йоурпрожект. h, должны точно совпадать.</span><span class="sxs-lookup"><span data-stu-id="b6754-125">When creating your online store COM object, the file attribute value you set for **ContentDistributor** and the value assigned to the constant kszContentDistributorID in YourProject.h must match exactly.</span></span> <span data-ttu-id="b6754-126">Помните, что вы указали это постоянное значение для COM-объекта при создании проекта с помощью мастера проектов.</span><span class="sxs-lookup"><span data-stu-id="b6754-126">Recall that you specified this constant value for your COM object when you created the project by using the project wizard.</span></span> <span data-ttu-id="b6754-127">Это значение можно изменить вручную.</span><span class="sxs-lookup"><span data-stu-id="b6754-127">You can change this value manually.</span></span> <span data-ttu-id="b6754-128">Просто обязательно используйте строку, уникально идентифицирующую вашу службу.</span><span class="sxs-lookup"><span data-stu-id="b6754-128">Just be sure to use a string that uniquely identifies your service.</span></span>

## <a name="using-the-windows-media-player-object-model"></a><span data-ttu-id="b6754-129">Использование объектной модели проигрывателя Windows Media</span><span class="sxs-lookup"><span data-stu-id="b6754-129">Using the Windows Media Player Object Model</span></span>

<span data-ttu-id="b6754-130">Чтобы указать значение для **контентдистрибутор** с помощью объектной модели проигрывателя Windows Media, используйте метод [Media. сетитеминфо](media-setiteminfo.md) .</span><span class="sxs-lookup"><span data-stu-id="b6754-130">To specify a value for **ContentDistributor** using the Windows Media Player object model, use the [Media.setItemInfo](media-setiteminfo.md) method.</span></span> <span data-ttu-id="b6754-131">В следующем примере кода указывается значение "Proseware" для **контентдистрибутор** для текущего воспроизводимого элемента мультимедиа:</span><span class="sxs-lookup"><span data-stu-id="b6754-131">The following example code specifies the value "Proseware" for **ContentDistributor** for the currently playing media item:</span></span>


```C++
// Retrieve the current media item.
var theMedia = Player.currentMedia;

//Test whether the media item was retrieved.
if(theMedia)
{
    // Set the ContentDistributor value.
    theMedia.setItemInfo("ContentDistributor", "Proseware");
}
```



## <a name="using-the-windows-media-format-sdk"></a><span data-ttu-id="b6754-132">Использование пакета SDK Windows Media Format</span><span class="sxs-lookup"><span data-stu-id="b6754-132">Using the Windows Media Format SDK</span></span>

<span data-ttu-id="b6754-133">Пакет SDK для проигрывателя Windows Media включает образец файла C++ с именем Сетконтентдистрибутор. cpp, демонстрирующий использование пакета SDK Windows Media Format 9 для добавления атрибута **WM/контентдистрибутор** .</span><span class="sxs-lookup"><span data-stu-id="b6754-133">The Windows Media Player SDK includes a sample C++ file, named SetContentDistributor.cpp, which demonstrates how to use the Windows Media Format 9 Series SDK to add the **WM/ContentDistributor** attribute.</span></span> <span data-ttu-id="b6754-134">Этот пример файла можно узнать в папке с именем Metadata, в которой установлен пакет SDK.</span><span class="sxs-lookup"><span data-stu-id="b6754-134">You can locate this sample file in the folder named Metadata where you installed the SDK.</span></span> <span data-ttu-id="b6754-135">Чтобы использовать этот код, необходимо выполнить следующие действия.</span><span class="sxs-lookup"><span data-stu-id="b6754-135">To use this code you must follow these steps:</span></span>

1.  <span data-ttu-id="b6754-136">Установите пакет SDK серии Windows Media Format 9 и настройте среду выполнения, как описано в документации.</span><span class="sxs-lookup"><span data-stu-id="b6754-136">Install the Windows Media Format 9 Series SDK and configure the runtime as described in the documentation.</span></span>
2.  <span data-ttu-id="b6754-137">Создайте новый пустой проект C++ в Visual Studio и добавьте в проект пример файла с именем Сетконтентдистрибутор. cpp.</span><span class="sxs-lookup"><span data-stu-id="b6754-137">Create a new empty C++ project in Visual Studio and add the sample file named SetContentDistributor.cpp to the project.</span></span>
3.  <span data-ttu-id="b6754-138">Добавьте путь к папкам пакета SDK Windows Media Format 9 Series в список путей к файлам.</span><span class="sxs-lookup"><span data-stu-id="b6754-138">Add the path to the Windows Media Format 9 Series SDK Lib folders to your list of file paths.</span></span> <span data-ttu-id="b6754-139">В меню **Сервис** выберите пункт **Параметры**.</span><span class="sxs-lookup"><span data-stu-id="b6754-139">From the **Tools** menu, choose **Options**.</span></span>
4.  <span data-ttu-id="b6754-140">В диалоговом окне **Параметры** щелкните **проекты**, а затем выберите **каталоги VC + +**.</span><span class="sxs-lookup"><span data-stu-id="b6754-140">In the **Options** dialog box, click **Projects**, and then click **VC++ Directories**.</span></span>
5.  <span data-ttu-id="b6754-141">В раскрывающемся списке **Показывать каталоги для** выберите пункт **файлы библиотек**.</span><span class="sxs-lookup"><span data-stu-id="b6754-141">In the **Show Directories for** drop-down list box, click **Library files**.</span></span>
6.  <span data-ttu-id="b6754-142">Используйте кнопки, чтобы добавить пути в списки.</span><span class="sxs-lookup"><span data-stu-id="b6754-142">Use the buttons to add the paths to the list boxes.</span></span>
7.  <span data-ttu-id="b6754-143">Откройте диалоговое окно страницы свойств для проекта.</span><span class="sxs-lookup"><span data-stu-id="b6754-143">Open the property pages dialog box for your project.</span></span> <span data-ttu-id="b6754-144">Выберите **Свойства конфигурации**, затем **Компоновщик**, а затем введите **входные данные**.</span><span class="sxs-lookup"><span data-stu-id="b6754-144">Choose **Configuration Properties**, then **Linker**, and then **Input**.</span></span> <span data-ttu-id="b6754-145">В текстовом поле **Дополнительные зависимости** введите "вмвкоре. lib".</span><span class="sxs-lookup"><span data-stu-id="b6754-145">Type "wmvcore.lib" in the **Additional Dependencies** text box.</span></span>

<span data-ttu-id="b6754-146">В примере кода создается программа командной строки.</span><span class="sxs-lookup"><span data-stu-id="b6754-146">The sample code creates a command-line program.</span></span> <span data-ttu-id="b6754-147">Аргументы, указываемые при запуске программы, указывают путь к файлу цифрового носителя для изменения и строку для значения атрибута **контентдистрибутор** .</span><span class="sxs-lookup"><span data-stu-id="b6754-147">The arguments you provide when running the program specify the path to the digital media file to modify and a string for the **ContentDistributor** attribute value.</span></span> <span data-ttu-id="b6754-148">Код использует **ивмхеадеринфо:: setAttribute** для добавления атрибута к указанному файлу.</span><span class="sxs-lookup"><span data-stu-id="b6754-148">The code uses **IWMHeaderInfo::SetAttribute** to add the attribute to the file you specified.</span></span> <span data-ttu-id="b6754-149">Этот пример можно использовать как есть или использовать его в качестве отправной точки для собственной программы.</span><span class="sxs-lookup"><span data-stu-id="b6754-149">You can use this sample as is or use it as a starting point for your own program.</span></span>

## <a name="related-topics"></a><span data-ttu-id="b6754-150">См. также</span><span class="sxs-lookup"><span data-stu-id="b6754-150">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b6754-151">**Сведения, общие для типа 1 и 2 Интернет-магазинов**</span><span class="sxs-lookup"><span data-stu-id="b6754-151">**Information Common to Type 1 and Type 2 Online Stores**</span></span>](information-common-to-type-1-and-type-2-online-stores.md)
</dt> </dl>

 

 




