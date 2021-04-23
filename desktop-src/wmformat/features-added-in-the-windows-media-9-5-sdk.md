---
title: Компоненты, добавленные в пакет SDK для Windows Media 9,5
description: Компоненты, добавленные в пакет SDK для Windows Media 9,5
ms.assetid: 1525132c-8aa1-42bb-9552-41531fb83055
keywords:
- Windows Media Format SDK, функции
- Windows Media Format SDK, новые функции
- Windows Media Format SDK, интерфейс для обработки приложений
- Windows Media Format SDK, ускорение видео DirectX (ДКСВА)
- Windows Media Format SDK, интерфейс Ивмплайерхук
- ивмплайерхук
- Windows Media Format SDK, 64-разрядные версии Windows
- Windows Media Format SDK, кодек Windows Media Video Image
- Windows Media Format SDK, аудиокодеки
- Windows Media Format SDK, DRM 10 для сетевых устройств
- Windows Media Format SDK, лицензии DRM
- Windows Media Format SDK, кодек расширенного профиля
- Windows Media Format SDK, формат цифрового соединения Sony/Philips (S/PDIF)
- Windows Media Format SDK, форматы с низкой задержкой
- Windows Media Format SDK, приблизительный режим поиска
- Пакет SDK для Windows Media Format, запись списка воспроизведения
- Пакет SDK для Windows Media Format, поддержка нескольких языков
- Windows Media Format SDK, Windows Media диспетчер устройств SDK
- Windows Media Format SDK, интерфейсы кодеков
- кодеки, Windows Media Video Image
- Управление цифровыми правами (DRM), протокол безопасного обмена сетевыми устройствами
- DRM (Управление цифровыми правами), протокол безопасного обмена сетевыми устройствами
- Управление цифровыми правами (DRM), лицензии
- DRM (Управление цифровыми правами), лицензии
- кодеки, кодек расширенного профиля
- Формат цифровых соединений Sony/Philips (S/PDIF), передача или передача с помощью
- S/PDIF (формат цифрового соединения Sony/Philips), передача или передача с помощью
- Приблизительный режим поиска
- метаданные, поддержка нескольких языков
- Windows Media диспетчер устройств SDK
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5e58c9816ef80325422ee365b952842727b5004e
ms.sourcegitcommit: 3e70ae762629e244028b437420ed50b5850db4e3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/20/2020
ms.locfileid: "104133535"
---
# <a name="features-added-in-the-windows-media-95-sdk"></a><span data-ttu-id="b8dc4-133">Компоненты, добавленные в пакет SDK для Windows Media 9,5</span><span class="sxs-lookup"><span data-stu-id="b8dc4-133">Features Added in the Windows Media 9.5 SDK</span></span>

<span data-ttu-id="b8dc4-134">В пакете SDK Windows Media Format 9,5 появились новые функции, обеспечивающие повышенную безопасность и гибкость содержимого.</span><span class="sxs-lookup"><span data-stu-id="b8dc4-134">The Windows Media Format 9.5 SDK introduced new features to provide enhanced content security and flexibility.</span></span> <span data-ttu-id="b8dc4-135">В пакет SDK были внесены следующие изменения с момента выпуска 9 Series.</span><span class="sxs-lookup"><span data-stu-id="b8dc4-135">The following changes were made to the SDK since the 9 Series release.</span></span>

## <a name="new-interface-for-application-specific-processing-during-directx-video-acceleration"></a><span data-ttu-id="b8dc4-136">Новый интерфейс для обработки приложений во время ускорения видео DirectX</span><span class="sxs-lookup"><span data-stu-id="b8dc4-136">New Interface for Application-specific Processing During DirectX Video Acceleration</span></span>

<span data-ttu-id="b8dc4-137">Приложения проигрывателя, поддерживающие ускорение видео DirectX, теперь могут реализовывать интерфейс [**ивмплайерхук**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmplayerhook) для выполнения обработки приложений во время декодирования DirectX.</span><span class="sxs-lookup"><span data-stu-id="b8dc4-137">Player applications that support DirectX Video Acceleration can now implement the [**IWMPlayerHook**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmplayerhook) interface to perform application-specific processing during DirectX VA decoding.</span></span> <span data-ttu-id="b8dc4-138">Модуль чтения вызывает метод обратного вызова [**ивмплайерхук::P redecode**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmplayerhook-predecode) перед передачей в обработчик видео сжатых видеороликов для декодирования.</span><span class="sxs-lookup"><span data-stu-id="b8dc4-138">The reader calls the [**IWMPLayerHook::PreDecode**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmplayerhook-predecode) callback method before passing compressed video samples to the video processor for decoding.</span></span>

> [!Note]  
> <span data-ttu-id="b8dc4-139">Чтобы использовать интерфейс **ивмплайерхук** и связанный интерфейс [**IWMReaderAdvanced5**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced5) , в пакете SDK формата Windows Media необходимо установить обновление с номером 888656.</span><span class="sxs-lookup"><span data-stu-id="b8dc4-139">To use the **IWMPlayerHook** interface and the associated [**IWMReaderAdvanced5**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced5) interface, you must have update number 888656 installed in the Windows Media Format SDK.</span></span> <span data-ttu-id="b8dc4-140">Обновление можно загрузить с [веб-сайта корпорации Майкрософт](https://support.microsoft.com/?id=888656).</span><span class="sxs-lookup"><span data-stu-id="b8dc4-140">You can download the update from the [Microsoft Web site](https://support.microsoft.com/?id=888656).</span></span>

 

## <a name="windows-media-format-sdk-version-for-x64-based-versions-of-windows"></a><span data-ttu-id="b8dc4-141">Версия пакета SDK для Windows Media Format для 64-разрядных версий Windows</span><span class="sxs-lookup"><span data-stu-id="b8dc4-141">Windows Media Format SDK version for x64-based versions of Windows</span></span>

<span data-ttu-id="b8dc4-142">Доступна версия пакета SDK для Windows Media Format, основанная на 64-разрядной версии.</span><span class="sxs-lookup"><span data-stu-id="b8dc4-142">An x64-based version of the Windows Media Format SDK is available.</span></span> <span data-ttu-id="b8dc4-143">Эта документация относится как к 32-разрядным версиям, так и к версии пакета SDK на основе x64.</span><span class="sxs-lookup"><span data-stu-id="b8dc4-143">This documentation applies to both the 32-bit versions and the x64-based version of the SDK.</span></span> <span data-ttu-id="b8dc4-144">Однако система управления цифровыми правами (DRM) не поддерживается в пакете SDK для Windows Media формата x64.</span><span class="sxs-lookup"><span data-stu-id="b8dc4-144">However, digital rights management (DRM) is not supported in the x64-based Windows Media Format SDK.</span></span>

## <a name="new-version-of-the-windows-media-video-image-codec"></a><span data-ttu-id="b8dc4-145">Новая версия кодека видеообраза Windows Media</span><span class="sxs-lookup"><span data-stu-id="b8dc4-145">New Version of the Windows Media Video Image Codec</span></span>

<span data-ttu-id="b8dc4-146">Кодек Windows Media Video 9 Image v2 упрощает примеры геометрических вычислений для панорамирования и масштабирования.</span><span class="sxs-lookup"><span data-stu-id="b8dc4-146">The Windows Media Video 9 Image v2 codec simplifies the sample geometry calculations for panning and zooming.</span></span> <span data-ttu-id="b8dc4-147">Новый кодек также поддерживает несколько сложных переходов между изображениями.</span><span class="sxs-lookup"><span data-stu-id="b8dc4-147">The new codec also supports several complex transitions between images.</span></span>

## <a name="new-version-of-the-windows-media-audio-codecs"></a><span data-ttu-id="b8dc4-148">Новая версия аудиокодеков Windows Media</span><span class="sxs-lookup"><span data-stu-id="b8dc4-148">New Version of the Windows Media Audio Codecs</span></span>

<span data-ttu-id="b8dc4-149">Пакет SDK Windows Media Format 9,5 содержит следующие обновленные аудиокодеки:</span><span class="sxs-lookup"><span data-stu-id="b8dc4-149">The Windows Media Format 9.5 SDK includes the following updated audio codecs:</span></span>

-   <span data-ttu-id="b8dc4-150">Windows Media Audio 9,1</span><span class="sxs-lookup"><span data-stu-id="b8dc4-150">Windows Media Audio 9.1</span></span>
-   <span data-ttu-id="b8dc4-151">Windows Media Audio 9,1 Professional</span><span class="sxs-lookup"><span data-stu-id="b8dc4-151">Windows Media Audio 9.1 Professional</span></span>
-   <span data-ttu-id="b8dc4-152">Windows Media Audio 9,1 без потерь</span><span class="sxs-lookup"><span data-stu-id="b8dc4-152">Windows Media Audio 9.1 Lossless</span></span>

## <a name="windows-media-drm-10-for-network-devices-protocol-support"></a><span data-ttu-id="b8dc4-153">Поддержка протокола Windows Media DRM 10 для сетевых устройств</span><span class="sxs-lookup"><span data-stu-id="b8dc4-153">Windows Media DRM 10 for Network Devices Protocol Support</span></span>

<span data-ttu-id="b8dc4-154">Пакет SDK для формата Windows Media 9,5 поддерживает новый протокол защиты Windows Media DRM 10 для сетевых устройств.</span><span class="sxs-lookup"><span data-stu-id="b8dc4-154">The Windows Media Format 9.5 SDK supports the new Windows Media DRM 10 for Network Devices secure transfer protocol.</span></span> <span data-ttu-id="b8dc4-155">Этот протокол можно использовать для потоковой передачи зашифрованного содержимого в локальную сеть на устройство воспроизведения, например в набор видео-приемников.</span><span class="sxs-lookup"><span data-stu-id="b8dc4-155">This protocol can be used to stream encrypted content over a local network to a playback device, such as a set-top video receiver.</span></span>

<span data-ttu-id="b8dc4-156">Большинство процедур, используемых для реализации поддержки Windows Media DRM 10 для сетевых устройств, должны выполняться приложением.</span><span class="sxs-lookup"><span data-stu-id="b8dc4-156">Most of the procedures used to implement support for Windows Media DRM 10 for Network Devices must be performed by the application.</span></span> <span data-ttu-id="b8dc4-157">Однако можно использовать методы пакета SDK Windows Media Format для предоставления следующих функциональных возможностей.</span><span class="sxs-lookup"><span data-stu-id="b8dc4-157">However, you can use methods of the Windows Media Format SDK to provide the following functionality:</span></span>

-   <span data-ttu-id="b8dc4-158">Обслуживание базы данных устройств, включая те, для которых включена поддержка Windows Media DRM 10 для сетевых устройств.</span><span class="sxs-lookup"><span data-stu-id="b8dc4-158">Maintain a database of devices, including those that are enabled for Windows Media DRM 10 for Network Devices.</span></span>
-   <span data-ttu-id="b8dc4-159">Проверьте устройства, чтобы убедиться, что они достаточно близки для клиента в сети для безопасной потоковой передачи.</span><span class="sxs-lookup"><span data-stu-id="b8dc4-159">Validate devices to ensure that they are "near" enough to the client on the network for secure streaming.</span></span>
-   <span data-ttu-id="b8dc4-160">Преобразуйте защищенные DRM файлы в потоки Windows Media DRM 10 для сетевых устройств.</span><span class="sxs-lookup"><span data-stu-id="b8dc4-160">Convert DRM-protected files to Windows Media DRM 10 for Network Devices streams.</span></span>
-   <span data-ttu-id="b8dc4-161">Запись файлов с использованием ранее зашифрованных данных.</span><span class="sxs-lookup"><span data-stu-id="b8dc4-161">Write files using previously encrypted data.</span></span>

## <a name="support-for-new-drm-licenses"></a><span data-ttu-id="b8dc4-162">Поддержка новых лицензий DRM</span><span class="sxs-lookup"><span data-stu-id="b8dc4-162">Support for New DRM Licenses</span></span>

<span data-ttu-id="b8dc4-163">Новые лицензии, созданные с помощью пакета SDK Windows Media Rights Manager, используют уровни защиты выходных данных (Оплс) для указания прав и ограничений на воспроизведение и копирование содержимого.</span><span class="sxs-lookup"><span data-stu-id="b8dc4-163">New licenses created by using the Windows Media Rights Manager SDK use Output Protection Levels (OPLs) to specify rights and restrictions for playing and copying content.</span></span> <span data-ttu-id="b8dc4-164">Пакет SDK для формата Windows Media обеспечивает поддержку чтения Оплс из лицензии.</span><span class="sxs-lookup"><span data-stu-id="b8dc4-164">The Windows Media Format SDK provides support for reading the OPLs from a license.</span></span>

## <a name="new-video-codec"></a><span data-ttu-id="b8dc4-165">Новый видеокодек</span><span class="sxs-lookup"><span data-stu-id="b8dc4-165">New Video Codec</span></span>

<span data-ttu-id="b8dc4-166">Расширенный профиль Windows Media Video 9 — это высококачественный кодек Windows Media Video 9, в ходе которого добавлена поддержка чередования кодирования.</span><span class="sxs-lookup"><span data-stu-id="b8dc4-166">The Windows Media Video 9 Advanced Profile codec builds on the high quality of the Windows Media Video 9 codec while adding support for interlaced encoding.</span></span>

## <a name="spdif-output"></a><span data-ttu-id="b8dc4-167">Выходные данные S/PDIF</span><span class="sxs-lookup"><span data-stu-id="b8dc4-167">S/PDIF Output</span></span>

<span data-ttu-id="b8dc4-168">Содержимое, закодированное с помощью одного из кодеков Windows Media Audio Professional, теперь может передаваться или передаваться с помощью формата цифрового соединения Sony/PDIF.</span><span class="sxs-lookup"><span data-stu-id="b8dc4-168">Content encoded with one of the Windows Media Audio Professional codecs can now be transferred or transmitted using the Sony/Philips Digital Interconnect Format (S/PDIF).</span></span>

## <a name="low-delay-audio"></a><span data-ttu-id="b8dc4-169">Low-Delay звук</span><span class="sxs-lookup"><span data-stu-id="b8dc4-169">Low-Delay Audio</span></span>

<span data-ttu-id="b8dc4-170">Кодеки Windows Media Audio 9,1 и Windows Media Audio 9,1 Professional теперь поддерживают несколько форматов с низкой задержкой.</span><span class="sxs-lookup"><span data-stu-id="b8dc4-170">The Windows Media Audio 9.1 and Windows Media Audio 9.1 Professional codecs now each support several low-delay formats.</span></span> <span data-ttu-id="b8dc4-171">Эти форматы создают звуковые потоки, которые могут быть запущены быстрее, уменьшая задержку в сценариях переключения потоков.</span><span class="sxs-lookup"><span data-stu-id="b8dc4-171">These formats produce audio streams that can be started more quickly, reducing latency in stream-switching scenarios.</span></span> <span data-ttu-id="b8dc4-172">Общая задержка в прямых трансляциях также улучшена с помощью форматов с низкой задержкой.</span><span class="sxs-lookup"><span data-stu-id="b8dc4-172">Overall latency in live broadcasts is also improved by using low-delay formats.</span></span>

## <a name="approximate-seeking-mode"></a><span data-ttu-id="b8dc4-173">Приблизительный режим поиска</span><span class="sxs-lookup"><span data-stu-id="b8dc4-173">Approximate Seeking Mode</span></span>

<span data-ttu-id="b8dc4-174">Теперь можно выполнить поиск приблизительного времени в файле ASF с помощью средства чтения.</span><span class="sxs-lookup"><span data-stu-id="b8dc4-174">You can now seek to an approximate time in an ASF file with the reader.</span></span> <span data-ttu-id="b8dc4-175">Этот режим повышает производительность при выполнении неточного поиска, например, когда пользователь щелкает строку поиска в проигрывателе Windows Media.</span><span class="sxs-lookup"><span data-stu-id="b8dc4-175">This mode improves performance when performing an imprecise seek, such as when a user clicks the seek bar in Windows Media Player.</span></span> <span data-ttu-id="b8dc4-176">Примерное поиск возвращает пример носителя для предыдущего клеанпоинт вместо реконструирования образца для точного времени.</span><span class="sxs-lookup"><span data-stu-id="b8dc4-176">Approximate seeking returns the media sample for the previous cleanpoint instead of reconstructing the sample for the precise time sought.</span></span>

## <a name="playlist-burning"></a><span data-ttu-id="b8dc4-177">Запись списка воспроизведения</span><span class="sxs-lookup"><span data-stu-id="b8dc4-177">Playlist Burning</span></span>

<span data-ttu-id="b8dc4-178">Windows Media DRM 10 поддерживает права копирования звуковых файлов на компакт-диск с Красной книгой в составе списка воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="b8dc4-178">Windows Media DRM 10 supports rights for copying audio files to Red Book CD as part of a playlist.</span></span> <span data-ttu-id="b8dc4-179">Пакет Windows Media Format SDK предоставляет методы для проверки того, разрешено ли копирование файлов из списка воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="b8dc4-179">The Windows Media Format SDK provides methods for verifying whether the files in a playlist are allowed to be copied.</span></span>

## <a name="improved-multiple-language-support-for-metadata"></a><span data-ttu-id="b8dc4-180">Улучшенная поддержка Multiple-Language для метаданных</span><span class="sxs-lookup"><span data-stu-id="b8dc4-180">Improved Multiple-Language Support for Metadata</span></span>

<span data-ttu-id="b8dc4-181">В пакете SDK серии Windows Media Format 9 все метаданные, добавленные в файл, были назначены списку языков, которому был присвоен идентификатор языка по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="b8dc4-181">In the Windows Media Format 9 Series SDK, all metadata added to a file was assigned to a language list that was given the language identifier of the default language.</span></span> <span data-ttu-id="b8dc4-182">Это привело к проблемам, когда распространители содержимого в разных языковых стандартах добавили некоторые метаданные, так как пользователи в национальной настройке распространителя видят только несколько атрибутов, добавленных для их языка.</span><span class="sxs-lookup"><span data-stu-id="b8dc4-182">This caused problems when content distributors in different locales added some metadata, because users in the distributor's locale only see the few attributes added for their language.</span></span> <span data-ttu-id="b8dc4-183">Пакет SDK для Windows Media Format 9,5 позволяет решить эту проблему, не создавая список языков, пока в файле не будут присутствуют атрибуты из двух языков.</span><span class="sxs-lookup"><span data-stu-id="b8dc4-183">The Windows Media Format 9.5 SDK solves this problem by not creating a language list until there are attributes from two languages present in the file.</span></span> <span data-ttu-id="b8dc4-184">На этом этапе все метаданные связаны с языковым стандартом второго языка, который затем становится значением по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="b8dc4-184">At that point, all of the metadata is associated with the locale of the second language, which then becomes the default.</span></span> <span data-ttu-id="b8dc4-185">Таким образом, распространитель содержимого может размещать все исходные метаданные для файла, такие как заголовок и автор, не затрагивая, добавляя некоторые атрибуты, относящиеся к их языковому стандарту.</span><span class="sxs-lookup"><span data-stu-id="b8dc4-185">In this way, a content distributor can keep all of the original metadata for a file, such as title and author, intact while adding some attributes pertinent to their locale.</span></span>

## <a name="windows-media-device-manager-sdk-included-in-installation"></a><span data-ttu-id="b8dc4-186">Пакет Windows Media диспетчер устройств SDK, входящий в установку</span><span class="sxs-lookup"><span data-stu-id="b8dc4-186">Windows Media Device Manager SDK Included in Installation</span></span>

<span data-ttu-id="b8dc4-187">Пакет установки пакета SDK для Windows Media Format 9,5 устанавливает пакет Windows Media диспетчер устройств SDK.</span><span class="sxs-lookup"><span data-stu-id="b8dc4-187">The installation package for the Windows Media Format 9.5 SDK installs the Windows Media Device Manager SDK.</span></span> <span data-ttu-id="b8dc4-188">Документацию по пакету Windows Media диспетчер устройств SDK можно найти в папке C: \\ вмсдк \\ WMFSDK95 \\ вмдм \\ документы (папка будет отличаться, если пакет SDK формата Windows Media не установлен в папку по умолчанию).</span><span class="sxs-lookup"><span data-stu-id="b8dc4-188">The documentation for the Windows Media Device Manager SDK can be found in the C:\\WMSDK\\WMFSDK95\\WMDM\\docs folder (your folder will be different if you do not install the Windows Media Format SDK in the default folder.)</span></span>

## <a name="codec-interface-documentation"></a><span data-ttu-id="b8dc4-189">Документация по интерфейсу кодека</span><span class="sxs-lookup"><span data-stu-id="b8dc4-189">Codec Interface Documentation</span></span>

<span data-ttu-id="b8dc4-190">Эта документация содержит сведения об использовании кодеков аудио и видео Windows Media вне пакета SDK Windows Media Format.</span><span class="sxs-lookup"><span data-stu-id="b8dc4-190">This documentation includes information about using the Windows Media Audio and Video codecs outside of the Windows Media Format SDK.</span></span> <span data-ttu-id="b8dc4-191">Эта документация была изначально выпущена как часть загрузки из сети разработчиков Майкрософт.</span><span class="sxs-lookup"><span data-stu-id="b8dc4-191">This documentation was originally released as part of a download from the Microsoft Developer Network.</span></span> <span data-ttu-id="b8dc4-192">Примеры приложений, демонстрирующие использование кодека дмос напрямую, включены в установку пакета SDK для Windows Media Format вместе с заголовками.</span><span class="sxs-lookup"><span data-stu-id="b8dc4-192">The sample applications that demonstrate using the codec DMOs directly are included in the Windows Media Format SDK installation along with headers.</span></span>

## <a name="related-topics"></a><span data-ttu-id="b8dc4-193">См. также</span><span class="sxs-lookup"><span data-stu-id="b8dc4-193">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b8dc4-194">**О пакете SDK для формата Windows Media**</span><span class="sxs-lookup"><span data-stu-id="b8dc4-194">**About the Windows Media Format SDK**</span></span>](about-the-windows-media-format-sdk.md)
</dt> </dl>

 

 




