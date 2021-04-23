---
title: Примеры приложений для Windows Media Format SDK
description: Примеры приложений для Windows Media Format SDK
ms.assetid: 037741cb-c5fb-485f-bf62-79b5465abfe4
keywords:
- Windows Media Format SDK, примеры приложений
- Управление цифровыми правами (DRM), примеры приложений
- DRM (Управление цифровыми правами), примеры приложений
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 20ce7a9baf53c289e9420cf3c226bf21a3c6bd16
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/10/2020
ms.locfileid: "104488760"
---
# <a name="windows-media-format-sdk-sample-applications"></a><span data-ttu-id="09f47-106">Примеры приложений для Windows Media Format SDK</span><span class="sxs-lookup"><span data-stu-id="09f47-106">Windows Media Format SDK Sample Applications</span></span>

<span data-ttu-id="09f47-107">Образец кода, прилагаемый к этому пакету SDK, представлен в виде проектов для Microsoft Visual Studio 2005.</span><span class="sxs-lookup"><span data-stu-id="09f47-107">The sample code supplied with this SDK is in the form of projects for Microsoft Visual Studio 2005.</span></span> <span data-ttu-id="09f47-108">Большинство примеров находятся в C++, но для Манажедвмфсдквраппер и Манажедметадатаедит требуется C#.</span><span class="sxs-lookup"><span data-stu-id="09f47-108">Most of the samples are in C++, but ManagedWMFSDKWrapper and ManagedMetadataEdit require C#.</span></span>

<span data-ttu-id="09f47-109">Эти примеры не будут работать, если не установлен пакет SDK для Windows Media Format или пакет SDK для Windows Player.</span><span class="sxs-lookup"><span data-stu-id="09f47-109">These samples will not work unless the Windows Media Format SDK or the Windows Player SDK has been installed.</span></span>

<span data-ttu-id="09f47-110">Сведения об использовании для каждого примера содержатся в файле readme.txt в каждом каталоге выборки.</span><span class="sxs-lookup"><span data-stu-id="09f47-110">Usage information for each sample is contained in a readme.txt file in each sample directory.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="09f47-111">SAML</span><span class="sxs-lookup"><span data-stu-id="09f47-111">Samle</span></span></th>
<th><span data-ttu-id="09f47-112">Описание</span><span class="sxs-lookup"><span data-stu-id="09f47-112">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="09f47-113">AudioPlayer</span><span class="sxs-lookup"><span data-stu-id="09f47-113">AudioPlayer</span></span></td>
<td><span data-ttu-id="09f47-114">Воспроизводит файлы Windows Media, включая файлы, защищенные с использованием DRM.</span><span class="sxs-lookup"><span data-stu-id="09f47-114">Plays Windows Media files including DRM-protected files.</span></span> <span data-ttu-id="09f47-115">Управление осуществляется с помощью графического пользовательского интерфейса, а команды включают воспроизведение, паузу, Поиск и остановку.</span><span class="sxs-lookup"><span data-stu-id="09f47-115">It is controlled through a GUI, and commands include Play, Pause, Seek and Stop.</span></span> <span data-ttu-id="09f47-116">Он может воспроизводить локальные файлы или файлы, считанные из Интернета (включая выходные данные в Интернет, с помощью примера Вмвнетврите).</span><span class="sxs-lookup"><span data-stu-id="09f47-116">It can play local files or files read from the Internet (including those output to the Internet by using the WMVNetWrite sample).</span></span>
<blockquote>
[!Note]<br />
<span data-ttu-id="09f47-117">Части этого образца DRM не поддерживаются в версиях Windows на базе x64.</span><span class="sxs-lookup"><span data-stu-id="09f47-117">The DRM portions of this sample are not supported on x64-based versions of Windows.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="09f47-118">дрмхеадер</span><span class="sxs-lookup"><span data-stu-id="09f47-118">DRMHeader</span></span></td>
<td><span data-ttu-id="09f47-119">Дрмхеадер — это консольное приложение, использующее интерфейс <a href="/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdrmeditor"><strong>ивмдрмедитор</strong></a> редактора метаданных для чтения атрибутов DRM файлов без связывания с статической библиотекой DRM.</span><span class="sxs-lookup"><span data-stu-id="09f47-119">DRMHeader is a console application that uses the metadata editor's <a href="/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdrmeditor"><strong>IWMDRMEditor</strong></a> interface to read DRM attributes of files without linking to the DRM static library.</span></span>
<blockquote>
[!Note]<br />
<span data-ttu-id="09f47-120">Этот пример не поддерживается в версиях Windows на базе x64.</span><span class="sxs-lookup"><span data-stu-id="09f47-120">This sample is not supported on x64-based versions of Windows.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="09f47-121">дрмшов</span><span class="sxs-lookup"><span data-stu-id="09f47-121">DRMShow</span></span></td>
<td><span data-ttu-id="09f47-122">Дрмшов — это консольное приложение, которое показывает, как считывать свойства <a href="wmformat-glossary.md"><em>DRM</em></a> файла Windows Media с помощью метода <strong>Ивмдрмреадер:: жетдрмпроперти</strong> . В этом примере демонстрируется использование метода <strong>ивмдрмреадер:: жетдрмпроперти</strong> и свойств, которые могут быть получены из модуля чтения DRM.</span><span class="sxs-lookup"><span data-stu-id="09f47-122">DRMShow is a console application that shows how to read <a href="wmformat-glossary.md"><em>DRM</em></a> properties of a Windows Media file using the <strong>IWMDRMReader::GetDRMProperty</strong> method.This sample demonstrates the use of the <strong>IWMDRMReader::GetDRMProperty</strong> method and the properties that can be retrieved from the DRM reader.</span></span> <span data-ttu-id="09f47-123">Он не показывает, как получить лицензию для содержимого, защищенного DRM.</span><span class="sxs-lookup"><span data-stu-id="09f47-123">It does not demonstrate how to acquire a license for DRM-protected content.</span></span> <span data-ttu-id="09f47-124">Для этого примера требуется библиотека заглушки DRM Вмстубдрм. lib для сборки.</span><span class="sxs-lookup"><span data-stu-id="09f47-124">This sample requires the DRM stub library WMStubDRM.lib to build.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="09f47-125">Этот пример не поддерживается в версиях Windows на базе x64.</span><span class="sxs-lookup"><span data-stu-id="09f47-125">This sample is not supported on x64-based versions of Windows.</span></span>
</blockquote>
<br/> <span data-ttu-id="09f47-126">Когда вы получаете Вмстубдрм. lib от корпорации Майкрософт, библиотеке назначается уровень безопасности приложения.</span><span class="sxs-lookup"><span data-stu-id="09f47-126">When you acquire the WMStubDRM.lib from Microsoft, the library is assigned an application security level.</span></span> <span data-ttu-id="09f47-127">Если уровень безопасности полученной библиотеки недостаточно для воспроизведения защищенного файла, в этом примере отобразится ошибка.</span><span class="sxs-lookup"><span data-stu-id="09f47-127">If the security level of the library you receive is not sufficient to play a protected file, this sample will display an error.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="09f47-128">Директшовинтероп/Дскопи</span><span class="sxs-lookup"><span data-stu-id="09f47-128">DirectShowInterop/DSCopy</span></span></td>
<td><span data-ttu-id="09f47-129">Перекодировать один или несколько файлов в файл ASF с помощью фильтра модуля записи DirectShow WM ASF.</span><span class="sxs-lookup"><span data-stu-id="09f47-129">Transcodes one or more files to an ASF file using the DirectShow  WM ASF Writer filter.</span></span> <span data-ttu-id="09f47-130">Входной файл может иметь любой сжатый или несжатый формат, поддерживаемый DirectShow.</span><span class="sxs-lookup"><span data-stu-id="09f47-130">The input file may be any compressed or uncompressed format supported by DirectShow.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="09f47-131">Директшовинтероп/Дсплай</span><span class="sxs-lookup"><span data-stu-id="09f47-131">DirectShowInterop/DSPlay</span></span></td>
<td><span data-ttu-id="09f47-132">Этот пример является интерактивным проигрывателем файлов аудио-или видеоклипа с поддержкой <a href="wmformat-glossary.md"><em>DRM</em></a> .</span><span class="sxs-lookup"><span data-stu-id="09f47-132">This sample is an interactive audio/video media file player with <a href="wmformat-glossary.md"><em>DRM</em></a> support.</span></span> <span data-ttu-id="09f47-133">Он использует фильтр чтения WM ASF в DirectShow для воспроизведения файлов Windows Media (ASF, WMA, WMV) без защиты DRM и файлов, использующих DRM на уровне 100 или ниже.</span><span class="sxs-lookup"><span data-stu-id="09f47-133">It uses DirectShow's WM ASF Reader filter to play Windows Media files (ASF, WMA, WMV) without DRM protection and files which use DRM at a level of 100 or below.</span></span> <span data-ttu-id="09f47-134">Дополнительные сведения см. в разделе readme.txt в каталоге примера.</span><span class="sxs-lookup"><span data-stu-id="09f47-134">See readme.txt in the sample's directory for more information.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="09f47-135">Директшовинтероп/Дссикфм</span><span class="sxs-lookup"><span data-stu-id="09f47-135">DirectShowInterop/DSSeekFm</span></span></td>
<td><span data-ttu-id="09f47-136">В этом примере показано, как использовать фильтр чтения DirectShow WM ASF для воспроизведения содержимого ASF в графе фильтра DirectShow, а также как использовать кадр для поиска в пакете SDK Windows Media Format.</span><span class="sxs-lookup"><span data-stu-id="09f47-136">This sample demonstrates how to use the DirectShow WM ASF Reader Filter to play ASF content in a DirectShow filter graph, and also how to use the frame seeking support in the Windows Media Format SDK.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="09f47-137">Управляемый/Вмфсдквраппер</span><span class="sxs-lookup"><span data-stu-id="09f47-137">Managed/WMFSDKWrapper</span></span></td>
<td><span data-ttu-id="09f47-138">Эта управляемая сборка выступает в качестве оболочки, используемой примерами управляемого кода для доступа к некоторым интерфейсам метаданных этого пакета SDK.</span><span class="sxs-lookup"><span data-stu-id="09f47-138">This managed assembly serves as a wrapper used by managed-code samples for accessing some metadata interfaces of this SDK.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="09f47-139">Управляемый/Метадатаедит</span><span class="sxs-lookup"><span data-stu-id="09f47-139">Managed/MetadataEdit</span></span></td>
<td><span data-ttu-id="09f47-140">Это приложение C# можно использовать для просмотра и редактирования метаданных из файлов Windows Media.</span><span class="sxs-lookup"><span data-stu-id="09f47-140">This C# application can be used to view and edit metadata from Windows Media files.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="09f47-141">метадатаедит</span><span class="sxs-lookup"><span data-stu-id="09f47-141">MetaDataEdit</span></span></td>
<td><span data-ttu-id="09f47-142">Это версия управляемого приложения Метадатаедит на C++.</span><span class="sxs-lookup"><span data-stu-id="09f47-142">This is a C++ version of the Managed MetadataEdit application.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="09f47-143">реадфромстреам</span><span class="sxs-lookup"><span data-stu-id="09f47-143">ReadFromStream</span></span></td>
<td><span data-ttu-id="09f47-144">В этом примере консольного приложения показано, как считывать данные из <strong>IStream</strong> с помощью вмреадер.</span><span class="sxs-lookup"><span data-stu-id="09f47-144">This console application sample shows how to read data from <strong>IStream</strong> with WMReader.</span></span> <span data-ttu-id="09f47-145">Источник <strong>IStream</strong> реализован для использования файла в формате Windows Media Format (WMA/WMV/ASF).</span><span class="sxs-lookup"><span data-stu-id="09f47-145"><strong>IStream</strong> source has been implemented to use a file in Windows Media Format (WMA/WMV/ASF).</span></span>
<blockquote>
[!Note]<br />
<span data-ttu-id="09f47-146">В этом примере не показано, как обрабатывать примеры носителей, поступающие из Вмреадер.</span><span class="sxs-lookup"><span data-stu-id="09f47-146">This sample does not show how to process the media samples coming out of WMReader.</span></span> <span data-ttu-id="09f47-147">Примеры обработки аудио-и видеороликов или других типов примеров мультимедиа см. в других примерах, например AudioPlayer, которые включены в пакет SDK Windows Media Format.</span><span class="sxs-lookup"><span data-stu-id="09f47-147">For examples on how to process audio/video or other types of media samples, please refer to other samples, for instance AudioPlayer, that are included with the Windows Media Format SDK.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="09f47-148">ункомпавитовмв</span><span class="sxs-lookup"><span data-stu-id="09f47-148">UncompAVIToWMV</span></span></td>
<td><span data-ttu-id="09f47-149">В этом примере консольного приложения показан код, необходимый для сжатия файла AVI в WMV-файл.</span><span class="sxs-lookup"><span data-stu-id="09f47-149">This console application sample shows the necessary code to compress an AVI file to a WMV file.</span></span> <span data-ttu-id="09f47-150">В нем показано, как объединить примеры для аудио-и видеопотоков из нескольких AVI-файлов и либо объединить их в похожие потоки, либо создать новый поток на основе профиля исходного потока.</span><span class="sxs-lookup"><span data-stu-id="09f47-150">It shows how to merge samples for audio and video streams from several AVI files and either merge these into similar streams or create a new stream based on the source stream profile.</span></span> <span data-ttu-id="09f47-151">Здесь также показано, как создать произвольный поток, выполнить многопроходную кодировку, добавить код времени SMPTE и применить защиту DRM версии 1.</span><span class="sxs-lookup"><span data-stu-id="09f47-151">It also shows how to create an arbitrary stream, do multipass encoding, add SMPTE time code, and apply DRM version 1 protection.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="09f47-152">Вмженпрофиле/exe</span><span class="sxs-lookup"><span data-stu-id="09f47-152">WMGenProfile/exe</span></span></td>
<td><span data-ttu-id="09f47-153">Этот пример был обновлен из выпуска 7,1.</span><span class="sxs-lookup"><span data-stu-id="09f47-153">This sample has been updated from the 7.1 release.</span></span> <span data-ttu-id="09f47-154">Теперь это приложение с диалоговым окном MFC.</span><span class="sxs-lookup"><span data-stu-id="09f47-154">It is now an MFC Dialog application.</span></span> <span data-ttu-id="09f47-155">Пример Вмженпрофиле демонстрирует использование статической библиотеки Вмженпрофиле.</span><span class="sxs-lookup"><span data-stu-id="09f47-155">WMGenProfile sample demonstrates the use of the WMGenProfile static library.</span></span> <span data-ttu-id="09f47-156">Он также служит средством создания профилей.</span><span class="sxs-lookup"><span data-stu-id="09f47-156">It also serves as a tool for the creation of profiles.</span></span> <span data-ttu-id="09f47-157">Это средство предназначено для разработчиков, знакомых с форматом Windows Media.</span><span class="sxs-lookup"><span data-stu-id="09f47-157">This tool is meant for developers familiar with the Windows Media Format.</span></span> <span data-ttu-id="09f47-158">Пользовательский интерфейс не тестировался для взаимодействия с пользователем и не является рекомендацией по представлению этой информации пользователю.</span><span class="sxs-lookup"><span data-stu-id="09f47-158">The UI has not been tested for user experience and is not meant as a recommendation about how to present this information to a user.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="09f47-159">Вмженпрофиле/lib</span><span class="sxs-lookup"><span data-stu-id="09f47-159">WMGenProfile/lib</span></span></td>
<td><span data-ttu-id="09f47-160">В примере библиотеки Женпрофиле демонстрируется создание профилей.</span><span class="sxs-lookup"><span data-stu-id="09f47-160">The GenProfile library sample demonstrates the creation of profiles.</span></span> <span data-ttu-id="09f47-161">В нем показано, как создавать типы и потоки мультимедиа для различных типов потоков (аудио, видео, сценариев, изображений, передачи файлов и веб-страниц).</span><span class="sxs-lookup"><span data-stu-id="09f47-161">It shows how to create media types and streams for various stream types (audio, video, script, image, file transfer, and Web).</span></span> <span data-ttu-id="09f47-162">Он не показывает, как работать с системными профилями и как преобразовать системные профили в профили, указывающие кодеки Windows Media Audio и видео 9 Series.</span><span class="sxs-lookup"><span data-stu-id="09f47-162">It does not demonstrate how to work with system profiles or how to convert system profiles to profiles that specify the Windows Media Audio and Video 9 Series codecs.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="09f47-163">вмпроп</span><span class="sxs-lookup"><span data-stu-id="09f47-163">WMProp</span></span></td>
<td><span data-ttu-id="09f47-164">Это консольное приложение демонстрирует извлечение атрибутов с помощью объекта редактора метаданных и сведений о профиле из средства чтения.</span><span class="sxs-lookup"><span data-stu-id="09f47-164">This console application demonstrates how to retrieve attributes by using the metadata editor object and profile information from the reader.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="09f47-165">вмстатс</span><span class="sxs-lookup"><span data-stu-id="09f47-165">WMStats</span></span></td>
<td><span data-ttu-id="09f47-166">Это консольное приложение отображает статистику чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="09f47-166">This console application displays Reader and Writer statistics.</span></span> <span data-ttu-id="09f47-167">На одном компьютере можно одновременно использовать несколько экземпляров Вмстатс.</span><span class="sxs-lookup"><span data-stu-id="09f47-167">Multiple instances of WMStats can also be used concurrently on one machine.</span></span> <span data-ttu-id="09f47-168">Запустите один экземпляр в качестве сервера для отправки потока в сеть, а затем запустите второй экземпляр в качестве клиента для проверки правильности потоковой передачи сервера.</span><span class="sxs-lookup"><span data-stu-id="09f47-168">Start one instance as a server to send the stream to the network and then run a second instance as a client to verify that server is streaming correctly.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="09f47-169">вмсинкреадер</span><span class="sxs-lookup"><span data-stu-id="09f47-169">WMSyncReader</span></span></td>
<td><span data-ttu-id="09f47-170">В этом примере консольного приложения показано, как прочитать файл мультимедиа с помощью <strong>ивмсинкреадер</strong> без создания дополнительного потока или использования обратных вызовов.</span><span class="sxs-lookup"><span data-stu-id="09f47-170">This console application sample shows how to read a media file using <strong>IWMSyncReader</strong> without creating any extra thread or using callbacks.</span></span> <span data-ttu-id="09f47-171">Реализованы следующие функции: чтение сжатых или распакованных выборок.</span><span class="sxs-lookup"><span data-stu-id="09f47-171">The following features are implemented :Reading compressed or decompressed samples</span></span><br/> <span data-ttu-id="09f47-172">Поиск на основе времени</span><span class="sxs-lookup"><span data-stu-id="09f47-172">Time-based seeking</span></span><br/> <span data-ttu-id="09f47-173">Поиск на основе кадров</span><span class="sxs-lookup"><span data-stu-id="09f47-173">Frame-based seeking</span></span><br/> <span data-ttu-id="09f47-174">Производный источник <strong>IStream</strong></span><span class="sxs-lookup"><span data-stu-id="09f47-174"><strong>IStream</strong> derived source</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="09f47-175">вмваппенд</span><span class="sxs-lookup"><span data-stu-id="09f47-175">WMVAppend</span></span></td>
<td><span data-ttu-id="09f47-176">Это консольное приложение принимает два файла Windows Media для ввода и пытается создать выходной файл с содержимым первого, за которым следуют второй.</span><span class="sxs-lookup"><span data-stu-id="09f47-176">This console application takes two Windows Media files for input, and attempts to create an output file with the contents of the first followed by the second.</span></span> <span data-ttu-id="09f47-177">В примере сравниваются профили двух входных файлов, чтобы убедиться, что они имеют достаточное сходство для добавления.</span><span class="sxs-lookup"><span data-stu-id="09f47-177">The sample compares the profiles of the two input files to ensure they are similar enough to be appended.</span></span> <span data-ttu-id="09f47-178">Если это не так, появится сообщение об ошибке.</span><span class="sxs-lookup"><span data-stu-id="09f47-178">If this is not the case, an error message appears.</span></span> <span data-ttu-id="09f47-179">Например, сообщение об ошибке возникает, когда один файл является только звуком, а второй — звуковым видеофайлом, или если у двух звуковых файлов разная скорость. Пример принимает источники переменной скорости (VBR).</span><span class="sxs-lookup"><span data-stu-id="09f47-179">For example, an error message occurs when one file is audio only and the second is an audio-video file, or when two audio files have different bit rates.The sample accepts variable bit rate (VBR) sources.</span></span> <span data-ttu-id="09f47-180">Однако при сравнении профилей с двумя источниками VBR в примере игнорируется средняя разность скорости, поскольку два потока VBR будут иметь разную среднюю скорость, даже если они были созданы с помощью одного и того же профиля.</span><span class="sxs-lookup"><span data-stu-id="09f47-180">However, when comparing the profiles of the two VBR sources, the sample ignores the average bit rate difference because two VBR streams will have different average bit rates even if they were created using the same profile.</span></span> <span data-ttu-id="09f47-181">Вмваппенд не может сравнить пиковую скорость потока с неограниченным числом потоков VBR или уровень качества потоков с частотой VBR, так как эта информация не существует в исходных файлах.</span><span class="sxs-lookup"><span data-stu-id="09f47-181">WMVAppend cannot compare the peak bit rate of unconstrained bit-rate-based VBR streams, or the quality level of quality-based VBR streams, because this information does not exist in the source files.</span></span> <span data-ttu-id="09f47-182">Таким образом, пользователь обязан обеспечить создание двух исходных файлов с использованием одного профиля.</span><span class="sxs-lookup"><span data-stu-id="09f47-182">It is therefore the user's responsibility to make sure that two source files are created using the same profile.</span></span> <span data-ttu-id="09f47-183">В противном случае может быть создано недопустимое содержимое.</span><span class="sxs-lookup"><span data-stu-id="09f47-183">Otherwise, invalid content can be created.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="09f47-184">вмвкопи</span><span class="sxs-lookup"><span data-stu-id="09f47-184">WMVCopy</span></span></td>
<td><span data-ttu-id="09f47-185">В этом примере показан код, необходимый для копирования файла WMV.</span><span class="sxs-lookup"><span data-stu-id="09f47-185">This sample shows the code necessary to copy a WMV file.</span></span> <span data-ttu-id="09f47-186">В нем показано, как читать и записывать сжатые образцы, считывать атрибуты и скрипты заголовка, а также изменять атрибуты заголовка.</span><span class="sxs-lookup"><span data-stu-id="09f47-186">It shows how to read and write compressed samples, read header attributes and scripts, and modify header attributes.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="09f47-187">вмвнетврите</span><span class="sxs-lookup"><span data-stu-id="09f47-187">WMVNetWrite</span></span></td>
<td><span data-ttu-id="09f47-188">Это консольное приложение демонстрирует потоковую передачу файла Windows Media через Интернет.</span><span class="sxs-lookup"><span data-stu-id="09f47-188">This console application shows how a Windows Media file is streamed across the Internet.</span></span> <span data-ttu-id="09f47-189">Для примера требуется указать порт, а затем файл можно воспроизвести с помощью проигрывателя.</span><span class="sxs-lookup"><span data-stu-id="09f47-189">The sample requires a port to be specified, and then the file can be played using a player.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="09f47-190">вмврекомпресс</span><span class="sxs-lookup"><span data-stu-id="09f47-190">WMVRecompress</span></span></td>
<td><span data-ttu-id="09f47-191">В этом консольном приложении показано, как повторно сжать WMV-файл.</span><span class="sxs-lookup"><span data-stu-id="09f47-191">This console application shows how to recompress a WMV file.</span></span> <span data-ttu-id="09f47-192">В нем демонстрируется чтение несжатых образцов, написание несжатых образцов и выполнение многопроходной кодировки, многоканальный выход и интеллектуальное повторное сжатие.</span><span class="sxs-lookup"><span data-stu-id="09f47-192">It demonstrates reading uncompressed samples, writing uncompressed samples, and doing multi-pass encoding, multi-channel output, and smart recompression.</span></span></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a><span data-ttu-id="09f47-193">См. также</span><span class="sxs-lookup"><span data-stu-id="09f47-193">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="09f47-194">**О пакете SDK для формата Windows Media**</span><span class="sxs-lookup"><span data-stu-id="09f47-194">**About the Windows Media Format SDK**</span></span>](about-the-windows-media-format-sdk.md)
</dt> <dt>

[<span data-ttu-id="09f47-195">**Инструкции по программированию**</span><span class="sxs-lookup"><span data-stu-id="09f47-195">**Programming Guide**</span></span>](programming-guide.md)
</dt> </dl>

 

 





