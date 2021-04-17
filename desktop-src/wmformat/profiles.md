---
title: Профили
description: Профили
ms.assetid: 6e70393f-3dab-4036-8d34-a672ef1795c6
keywords:
- Windows Media Format SDK, профили
- Расширенный формат систем (ASF), профили
- ASF (Расширенный системный формат), профили
- Windows Media Format SDK, пркс файлы
- Расширенные системные форматы (ASF), пркс-файлы
- ASF (Расширенный системный формат), пркс-файлы
- Пакет Windows Media Format SDK, редактор профилей
- Расширенный формат систем (ASF), редактор профилей
- ASF (Расширенный системный формат), редактор профилей
- файлы пркс
- файлы пркс
- Редактор профилей
- Кодировщик Windows Media
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: de244445a7c1301c7a14ef273b81ac9fd9cbfb62
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/19/2020
ms.locfileid: "105691458"
---
# <a name="profiles"></a><span data-ttu-id="5debe-116">Профили</span><span class="sxs-lookup"><span data-stu-id="5debe-116">Profiles</span></span>

<span data-ttu-id="5debe-117">Профиль — это набор данных, описывающих конфигурацию ASF-файла.</span><span class="sxs-lookup"><span data-stu-id="5debe-117">A profile is a collection of data that describes the configuration of an ASF file.</span></span> <span data-ttu-id="5debe-118">Профиль должен содержать как минимум параметры конфигурации для одного потока.</span><span class="sxs-lookup"><span data-stu-id="5debe-118">At a minimum, a profile must contain configuration settings for a single stream.</span></span>

<span data-ttu-id="5debe-119">Сведения о потоке в профиле содержат скорость потока, окно буфера и свойства мультимедиа для него.</span><span class="sxs-lookup"><span data-stu-id="5debe-119">The stream information in a profile contains the bit rate, buffer window, and media properties for the stream.</span></span> <span data-ttu-id="5debe-120">В сведениях о потоках для аудио и видео описывается, как в файле настраивается носитель, включая, какой кодек (если он используется) будет использоваться для сжатия данных.</span><span class="sxs-lookup"><span data-stu-id="5debe-120">The stream information for audio and video describes exactly how the media is configured in the file, including which codec (if any) will be used to compress the data.</span></span>

<span data-ttu-id="5debe-121">Профиль также содержит сведения о различных функциях ASF-файлов, которые будут использоваться в файлах, созданных с помощью.</span><span class="sxs-lookup"><span data-stu-id="5debe-121">A profile also contains information about the various ASF file features that will be used in files created with it.</span></span> <span data-ttu-id="5debe-122">К ним относятся [взаимное исключение](mutual-exclusion.md), [Определение приоритетов потоков](stream-prioritization.md), [совместное использование пропускной способности](bandwidth-sharing.md)и [расширения модулей данных](data-unit-extensions.md).</span><span class="sxs-lookup"><span data-stu-id="5debe-122">These include [Mutual Exclusion](mutual-exclusion.md), [Stream Prioritization](stream-prioritization.md), [Bandwidth Sharing](bandwidth-sharing.md), and [Data Unit Extensions](data-unit-extensions.md).</span></span>

<span data-ttu-id="5debe-123">В предыдущих версиях пакета SDK для формата Windows Media предусмотрены предварительно настроенные системные профили, которые можно использовать для создания общих типов файлов или незначительно изменяются в соответствии с потребностями приложения.</span><span class="sxs-lookup"><span data-stu-id="5debe-123">Previous versions of the Windows Media Format SDK provided preconfigured system profiles, which could be used to create common types of files, or altered slightly to suit the needs of your application.</span></span> <span data-ttu-id="5debe-124">Системные профили не поддерживаются для кодеков Windows Media 9 Series.</span><span class="sxs-lookup"><span data-stu-id="5debe-124">System profiles are not supported for the Windows Media 9 Series codecs.</span></span> <span data-ttu-id="5debe-125">Это связано с тем, что число общих типов файлов увеличилось экспоненциально с добавлением новых функций.</span><span class="sxs-lookup"><span data-stu-id="5debe-125">This is because the number of "common" types of files has grown exponentially with the addition of new features.</span></span> <span data-ttu-id="5debe-126">Ожидается, что практически каждый создатель содержимого нуждается в отсутствии простых решений, предоставляемых системными профилями.</span><span class="sxs-lookup"><span data-stu-id="5debe-126">It is expected that virtually every content creator has needs that go beyond the simple solutions provided by system profiles.</span></span> <span data-ttu-id="5debe-127">Старые системные профили по-прежнему можно использовать в качестве отправной позиции.</span><span class="sxs-lookup"><span data-stu-id="5debe-127">You can still use the old system profiles as a starting place.</span></span> <span data-ttu-id="5debe-128">Дополнительные сведения см. [в разделе Использование системных профилей](using-system-profiles.md).</span><span class="sxs-lookup"><span data-stu-id="5debe-128">For more information, see [Using System Profiles](using-system-profiles.md).</span></span>

<span data-ttu-id="5debe-129">Необходимо предоставить модуль записи с профилем для каждого записываемого файла.</span><span class="sxs-lookup"><span data-stu-id="5debe-129">You must supply the writer with a profile for every file you write.</span></span> <span data-ttu-id="5debe-130">Можно указать профиль для использования с модулем записи, вызвав [**ивмвритер:: сетпрофиле**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-setprofile).</span><span class="sxs-lookup"><span data-stu-id="5debe-130">You can specify a profile to use with the writer by calling [**IWMWriter::SetProfile**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-setprofile).</span></span>

<span data-ttu-id="5debe-131">Данные профиля существуют в нескольких формах, которые могут использоваться пакетом SDK Windows Media Format.</span><span class="sxs-lookup"><span data-stu-id="5debe-131">Profile data exists in several different forms that can be used by the Windows Media Format SDK.</span></span> <span data-ttu-id="5debe-132">Сведения о профиле также можно получить несколькими способами.</span><span class="sxs-lookup"><span data-stu-id="5debe-132">Profile information can also be accessed in several ways.</span></span> <span data-ttu-id="5debe-133">Это может привести к путанице с тем, что представляет собой профиль и как он используется.</span><span class="sxs-lookup"><span data-stu-id="5debe-133">This can lead to confusion about what a profile is and how it is used.</span></span>

<span data-ttu-id="5debe-134">На следующей схеме показано, как данные профилирования используются в пакете SDK.</span><span class="sxs-lookup"><span data-stu-id="5debe-134">The following diagram shows how profile data is used in the SDK.</span></span>

![Схема, показывающая поток сведений о профиле.](images/formatsdk01.png)

<span data-ttu-id="5debe-136">Данные профиля принимают три различные формы: данные, содержащиеся в объекте профиля в приложении, XML-файл на диске, и данные в заголовке файла ASF.</span><span class="sxs-lookup"><span data-stu-id="5debe-136">Profile data takes three different forms: data contained within a profile object in an application, an XML file on disk, and data in the header of an ASF file.</span></span> <span data-ttu-id="5debe-137">Каждая из этих форм данных отображается в виде затененного прямоугольника на схеме.</span><span class="sxs-lookup"><span data-stu-id="5debe-137">Each of these forms of data is shown as a shaded rectangle in the diagram.</span></span>

## <a name="data-in-a-profile-object"></a><span data-ttu-id="5debe-138">Данные в объекте профиля</span><span class="sxs-lookup"><span data-stu-id="5debe-138">Data in a Profile Object</span></span>

<span data-ttu-id="5debe-139">При редактировании профиля используется объект профиля, который инкапсулирует все данные профиля.</span><span class="sxs-lookup"><span data-stu-id="5debe-139">When you are editing a profile, you use a profile object, which encapsulates all of the profile data.</span></span> <span data-ttu-id="5debe-140">Пустой объект профиля можно создать с помощью объекта диспетчера профилей.</span><span class="sxs-lookup"><span data-stu-id="5debe-140">You can create an empty profile object by using the profile manager object.</span></span> <span data-ttu-id="5debe-141">Можно также использовать объект диспетчера профилей для загрузки существующих данных профиля в объект профиля.</span><span class="sxs-lookup"><span data-stu-id="5debe-141">You can also use the profile manager object to load existing profile data into a profile object.</span></span>

<span data-ttu-id="5debe-142">Большая часть данных профиля должна добавляться и обрабатываться с помощью объектов, представляющих отдельные части профиля.</span><span class="sxs-lookup"><span data-stu-id="5debe-142">Most profile data must be added and manipulated through the use of objects representing individual parts of the profile.</span></span> <span data-ttu-id="5debe-143">К ним относятся объекты конфигурации потока, взаимоисключающие объекты, объекты совместного использования пропускной способности и объект определения приоритетов потоков.</span><span class="sxs-lookup"><span data-stu-id="5debe-143">These include stream configuration objects, mutual exclusion objects, bandwidth sharing objects, and a stream prioritization object.</span></span> <span data-ttu-id="5debe-144">Каждый из этих типов объектов можно создать с помощью методов в объекте Profile.</span><span class="sxs-lookup"><span data-stu-id="5debe-144">Each of these object types can be created using methods in the profile object.</span></span> <span data-ttu-id="5debe-145">Внесение изменений в эти объекты не влияет на объект Profile, пока не будет использован метод в объекте Profile для включения обновленных данных из другого объекта.</span><span class="sxs-lookup"><span data-stu-id="5debe-145">Making changes to these objects does not affect the profile object until you use a method in the profile object to include the updated data from the other object.</span></span>

## <a name="data-in-an-xml-file"></a><span data-ttu-id="5debe-146">Данные в XML-файле</span><span class="sxs-lookup"><span data-stu-id="5debe-146">Data in an XML File</span></span>

<span data-ttu-id="5debe-147">Данные профиля хранятся на диске в виде XML-файла с расширением имени файла пркс.</span><span class="sxs-lookup"><span data-stu-id="5debe-147">Profile data is stored on disk in the form of an XML file with the .prx file name extension.</span></span> <span data-ttu-id="5debe-148">В состав пакета SDK для Windows Media Format входит набор профилей, называемых системными профилями, охватывающий наиболее распространенные типы файлов ASF.</span><span class="sxs-lookup"><span data-stu-id="5debe-148">Included with the Windows Media Format SDK is a collection of profiles called system profiles that cover the most common types of ASF files.</span></span> <span data-ttu-id="5debe-149">Системные профили хранятся в файле с именем WMSysPr9. пркс.</span><span class="sxs-lookup"><span data-stu-id="5debe-149">System profiles are stored in a file named WMSysPr9.prx.</span></span> <span data-ttu-id="5debe-150">(Обратите внимание, что в этом файле нет системных профилей для серии Windows Media 9, поскольку концепция системных профилей больше не используется.) При сохранении пользовательских профилей их необходимо сохранить в собственных файлах.</span><span class="sxs-lookup"><span data-stu-id="5debe-150">(Note that this file actually contains no system profiles for Windows Media 9 Series because the concept of system profiles is no longer used.) When you save your own custom profiles, you must save them to your own files.</span></span>

<span data-ttu-id="5debe-151">Объект диспетчера профилей можно использовать для сохранения данных из объекта профиля в строку XML-текста.</span><span class="sxs-lookup"><span data-stu-id="5debe-151">You can use the profile manager object to save the data from a profile object to a string of XML text.</span></span> <span data-ttu-id="5debe-152">Затем можно использовать любые функции файлового ввода-вывода для сохранения строки в файл на диске.</span><span class="sxs-lookup"><span data-stu-id="5debe-152">You can then use whatever file I/O functions you like to save the string to a file on disk.</span></span>

## <a name="data-in-the-header-of-an-asf-file"></a><span data-ttu-id="5debe-153">Данные в заголовке файла ASF</span><span class="sxs-lookup"><span data-stu-id="5debe-153">Data in the Header of an ASF File</span></span>

<span data-ttu-id="5debe-154">Модуль записи получает информацию из профиля и использует ее для создания потоков, которые попадают в раздел данных ASF.</span><span class="sxs-lookup"><span data-stu-id="5debe-154">The writer takes the information from the profile and uses it to create the streams that go into the data section of the ASF file.</span></span> <span data-ttu-id="5debe-155">Основная часть данных профиля хранится в разделе заголовка файла при его написании.</span><span class="sxs-lookup"><span data-stu-id="5debe-155">The bulk of the profile data is stored in the header section of the file when a file is written.</span></span> <span data-ttu-id="5debe-156">При воспроизведении объект Reader (или синхронный объект Reader) может получить доступ к информации в заголовке файла.</span><span class="sxs-lookup"><span data-stu-id="5debe-156">At playback, the reader object (or the synchronous reader object) can access the information in the header of the file.</span></span> <span data-ttu-id="5debe-157">В этом случае объект Read создает объект профиля и заполняет его данными из заголовка.</span><span class="sxs-lookup"><span data-stu-id="5debe-157">In this case, the reading object creates a profile object and populates it with the data from the header.</span></span>

<span data-ttu-id="5debe-158">При доступе к данным профиля с помощью средства чтения (или синхронного средства чтения) можно вносить изменения в сведения о профиле, но не существует способа применить эти изменения к файлу в модуле чтения.</span><span class="sxs-lookup"><span data-stu-id="5debe-158">When you access the profile data by using the reader (or synchronous reader), you can make changes to the profile information, but there is no way to apply those changes to the file in the reader.</span></span> <span data-ttu-id="5debe-159">Вы можете применить сведения о профиле из файла в модуле чтения к профилю в средстве записи, чтобы создать новый файл с теми же параметрами, что и у файла в модуле чтения.</span><span class="sxs-lookup"><span data-stu-id="5debe-159">You can apply the profile information from a file in a reader to a profile in a writer to create a new file with the same settings as the file in the reader.</span></span> <span data-ttu-id="5debe-160">В этом случае любые изменения, внесенные в сведения о профиле до настройки профиля в модуле записи, будут отражены в сведениях о профиле, зарегистрированном модулем записи.</span><span class="sxs-lookup"><span data-stu-id="5debe-160">In this case, any changes you make to the profile information prior to setting the profile in the writer will be reflected in the profile information registered by the writer.</span></span>

## <a name="using-profile-editor"></a><span data-ttu-id="5debe-161">Использование редактора профилей</span><span class="sxs-lookup"><span data-stu-id="5debe-161">Using Profile Editor</span></span>

<span data-ttu-id="5debe-162">Вместо создания профилей с помощью пакета SDK Windows Media Format можно использовать редактор профилей — служебную программу, которая входит в состав кодировщика Windows Media.</span><span class="sxs-lookup"><span data-stu-id="5debe-162">Rather than creating profiles by using the Windows Media Format SDK, you can use Profile Editor, a utility that is included with Windows Media Encoder.</span></span> <span data-ttu-id="5debe-163">В приложении кодирования используйте метод **ивмпрофилеманажер:: лоадпрофилебидата** для загрузки сохраненного профиля.</span><span class="sxs-lookup"><span data-stu-id="5debe-163">In your encoding application, use the **IWMProfileManager::LoadProfileByData** method to load the saved profile.</span></span> <span data-ttu-id="5debe-164">В некоторых сценариях, например при использовании ограниченного количества профилей, которые никогда не изменялись динамически, для создания профилей удобнее использовать редактор профилей.</span><span class="sxs-lookup"><span data-stu-id="5debe-164">In some scenarios, for example if you use a limited number of profiles that are never modified dynamically, it might be more convenient to use the Profile Editor to create your profiles.</span></span>

<span data-ttu-id="5debe-165">Тем не менее, если вы используете редактор профилей, рекомендуется не использовать параметр "размер видео: то же, что и входные видео".</span><span class="sxs-lookup"><span data-stu-id="5debe-165">However, if you do use Profile Editor, it is recommended that you do not use the "Video Size: Same As Video Input" setting.</span></span> <span data-ttu-id="5debe-166">Если этот флажок установлен, редактор профилей будет создавать профиль с высотой и шириной вывода видео, установленным в ноль.</span><span class="sxs-lookup"><span data-stu-id="5debe-166">When this check box is checked, Profile Editor will create a profile with the video output height and width set to zero.</span></span> <span data-ttu-id="5debe-167">Когда кодировщик Windows Media обнаруживает эти профили, он устанавливает правильные значения, соответствующие входным данным видео.</span><span class="sxs-lookup"><span data-stu-id="5debe-167">When Windows Media Encoder encounters these profiles, it sets the correct values to match its video input.</span></span> <span data-ttu-id="5debe-168">Однако модуль записи в пакете SDK формата Windows Media не делает этого автоматически, поэтому необходимо убедиться, что приложение задает размер видеокадра в случаях, когда в профиле нет.</span><span class="sxs-lookup"><span data-stu-id="5debe-168">However, the Writer in the Windows Media Format SDK does not do so automatically, so you must ensure that your application sets the video frame size in cases where the profile has none.</span></span>

<span data-ttu-id="5debe-169">**Примечание** . Некоторые элементы конфигурации потока не хранятся в профиле.</span><span class="sxs-lookup"><span data-stu-id="5debe-169">**Note** Some stream configuration items are not stored in the profile.</span></span> <span data-ttu-id="5debe-170">Данные в профиле описывают формат готового ASF файла.</span><span class="sxs-lookup"><span data-stu-id="5debe-170">The data in the profile describes the format of the finished ASF file.</span></span> <span data-ttu-id="5debe-171">Входные свойства носителя и другие данные конфигурации, используемые объектом модуля записи для настройки кодеков, не сохраняются в профиле.</span><span class="sxs-lookup"><span data-stu-id="5debe-171">Input media properties and other configuration data used by the writer object to configure the codecs are not saved in the profile.</span></span> <span data-ttu-id="5debe-172">Сюда входят все свойства, заданные с помощью метода [**ивмпропертиваулт:: SetProperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmpropertyvault-setproperty) .</span><span class="sxs-lookup"><span data-stu-id="5debe-172">This includes all properties set by using the [**IWMPropertyVault::SetProperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmpropertyvault-setproperty) method.</span></span>

## <a name="related-topics"></a><span data-ttu-id="5debe-173">См. также</span><span class="sxs-lookup"><span data-stu-id="5debe-173">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5debe-174">**Объект, совместно использующие пропускную способность**</span><span class="sxs-lookup"><span data-stu-id="5debe-174">**Bandwidth Sharing Object**</span></span>](bandwidth-sharing-object.md)
</dt> <dt>

[<span data-ttu-id="5debe-175">**Основные понятия**</span><span class="sxs-lookup"><span data-stu-id="5debe-175">**Concepts**</span></span>](concepts.md)
</dt> <dt>

[<span data-ttu-id="5debe-176">**Интерфейс Ивмпрофиле**</span><span class="sxs-lookup"><span data-stu-id="5debe-176">**IWMProfile Interface**</span></span>](iwmprofile.md)
</dt> <dt>

[<span data-ttu-id="5debe-177">**Интерфейс Ивмпрофилеманажер**</span><span class="sxs-lookup"><span data-stu-id="5debe-177">**IWMProfileManager Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmprofilemanager)
</dt> <dt>

[<span data-ttu-id="5debe-178">**Объект взаимного исключения**</span><span class="sxs-lookup"><span data-stu-id="5debe-178">**Mutual Exclusion Object**</span></span>](mutual-exclusion-object.md)
</dt> <dt>

[<span data-ttu-id="5debe-179">**Объект диспетчера профилей**</span><span class="sxs-lookup"><span data-stu-id="5debe-179">**Profile Manager Object**</span></span>](profile-manager-object.md)
</dt> <dt>

[<span data-ttu-id="5debe-180">**Объект конфигурации потока**</span><span class="sxs-lookup"><span data-stu-id="5debe-180">**Stream Configuration Object**</span></span>](stream-configuration-object.md)
</dt> <dt>

[<span data-ttu-id="5debe-181">**Объект определения приоритетов потоков**</span><span class="sxs-lookup"><span data-stu-id="5debe-181">**Stream Prioritization Object**</span></span>](stream-prioritization-object.md)
</dt> <dt>

[<span data-ttu-id="5debe-182">**Работа с профилями**</span><span class="sxs-lookup"><span data-stu-id="5debe-182">**Working with Profiles**</span></span>](working-with-profiles.md)
</dt> </dl>

 

 




