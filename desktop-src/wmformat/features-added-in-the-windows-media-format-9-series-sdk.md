---
title: Функции, добавленные в пакете SDK серии Windows Media Format 9
description: Функции, добавленные в пакете SDK серии Windows Media Format 9
ms.assetid: 73c4da27-a456-4845-a35b-edb75aa3f953
keywords:
- Windows Media Format SDK, функции
- Windows Media Format SDK, новые функции
- Пакет SDK для Windows Media Format, синхронные средства чтения
- Windows Media Format SDK, индексирование на основе кадров
- Windows Media Format SDK, коды времени SMPTE
- Windows Media Format SDK, фильтры DirectShow
- Windows Media Format SDK, возможность записи DRM
- Windows Media Format SDK, приемники файлов
- Windows Media Format SDK, ускорение видео DirectX (ДКСВА)
- Windows Media Format SDK, многоканальное аудио
- Windows Media Format SDK, водяные знаки
- Пакет SDK для Windows Media Format, поддержка нескольких языков
- Windows Media Format SDK, шаблоны соответствия устройств
- Windows Media Format SDK, перечисления кодеков
- Пакет SDK для Windows Media Format, взаимное исключение
- Windows Media Format SDK, несколько битов (MBR)
- Windows Media Format SDK, перекодирование с помощью интеллектуального повторного сжатия
- Windows Media Format SDK, интеллектуальное повторное сжатие
- Windows Media Format SDK, повторное сжатие
- Windows Media Format SDK, метаданные
- Windows Media Format SDK, динамически пропорции пикселей
- Пакет SDK для Windows Media Format, чередующиеся видеопотоки
- Windows Media Format SDK, многопроходная кодировка
- Windows Media Format SDK, Вмстуб. lib
- синхронные читатели, о
- индексирование на основе кадров
- Коды времени SMPTE, сведения
- Фильтры DirectShow
- приемники файлов, улучшения
- многоканальное аудио, о программе
- водяные знаки, о
- кодеки, перечисления
- взаимное исключение, сведения
- Управление цифровыми правами (DRM), возможность записи
- DRM (Управление цифровыми правами), возможность записи
- Ускорение видео DirectX (ДКСВА), о программе
- ДКСВА (ускорение видео DirectX), сведения
- Расширенный формат систем (ASF), поддержка нескольких языков
- ASF (Расширенный системный формат), поддержка нескольких языков
- несколько битов (MBR), о
- MBR (Многоразрядная скорость), сведения
- Перекодирование с помощью интеллектуального повторного сжатия
- интеллектуальное повторное сжатие
- повторное сжатие
- метаданные, Windows Media Format SDK
- динамическое пропорции пикселей
- потоки видео с чередованием
- 2-проходная кодировка, о
- 2. Передача кодирования, сведения
- Вмстуб. lib
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: adca7e39c89220c2c8c4cac6af354eefb77257aa
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104253334"
---
# <a name="features-added-in-the-windows-media-format-9-series-sdk"></a><span data-ttu-id="9a8a8-153">Функции, добавленные в пакете SDK серии Windows Media Format 9</span><span class="sxs-lookup"><span data-stu-id="9a8a8-153">Features Added in the Windows Media Format 9 Series SDK</span></span>

<span data-ttu-id="9a8a8-154">Пакет SDK для Windows Media Format 9 появилось множество улучшений и функций.</span><span class="sxs-lookup"><span data-stu-id="9a8a8-154">The Windows Media Format 9 Series SDK introduced many improvements and features.</span></span> <span data-ttu-id="9a8a8-155">В этом разделе приводятся общие сведения об этих функциях для пользователей, выполняющих переход с более ранней версии пакета SDK.</span><span class="sxs-lookup"><span data-stu-id="9a8a8-155">This section provides an overview of those features for the benefit of users migrating from an earlier version of the SDK.</span></span>

## <a name="synchronous-reading"></a><span data-ttu-id="9a8a8-156">Синхронное чтение</span><span class="sxs-lookup"><span data-stu-id="9a8a8-156">Synchronous Reading</span></span>

<span data-ttu-id="9a8a8-157">Файлы ASF можно читать с помощью синхронных вызовов.</span><span class="sxs-lookup"><span data-stu-id="9a8a8-157">You can read ASF files with synchronous calls.</span></span> <span data-ttu-id="9a8a8-158">При синхронном чтении файла можно изменить параметры считывания.</span><span class="sxs-lookup"><span data-stu-id="9a8a8-158">When reading a file synchronously, you can change the settings of the reader while it is reading.</span></span> <span data-ttu-id="9a8a8-159">Синхронные операции чтения пакета SDK не обеспечивают поддержку чтения файлов через Интернет, но для чтения из пользовательских источников можно использовать стандартный COM-интерфейс **IStream**.</span><span class="sxs-lookup"><span data-stu-id="9a8a8-159">The synchronous reading operations of the SDK do not provide support for reading files over the Internet, but you can use the standard COM interface, **IStream**, to read from custom sources.</span></span>

## <a name="frame-based-indexing"></a><span data-ttu-id="9a8a8-160">Индексирование на основе кадров</span><span class="sxs-lookup"><span data-stu-id="9a8a8-160">Frame-based Indexing</span></span>

<span data-ttu-id="9a8a8-161">Файлы ASF можно индексировать на основе видеокадров.</span><span class="sxs-lookup"><span data-stu-id="9a8a8-161">You can index ASF files based on video frames.</span></span> <span data-ttu-id="9a8a8-162">Как читатель, так и синхронный читатель могут перейти к кадру видеопотока и синхронизировать другие потоки с этим кадром.</span><span class="sxs-lookup"><span data-stu-id="9a8a8-162">Both the reader and the synchronous reader can seek to a frame of a video stream and synchronize the other streams to that frame.</span></span>

## <a name="indexing-and-seeking-with-smpte-time-code"></a><span data-ttu-id="9a8a8-163">Индексирование и поиск с помощью кода времени SMPTE</span><span class="sxs-lookup"><span data-stu-id="9a8a8-163">Indexing and Seeking with SMPTE Time Code</span></span>

<span data-ttu-id="9a8a8-164">Пакет SDK Windows Media Format позволяет хранить коды времени SMPTE в файлах ASF.</span><span class="sxs-lookup"><span data-stu-id="9a8a8-164">The Windows Media Format SDK enables you to store SMPTE time codes in ASF files.</span></span> <span data-ttu-id="9a8a8-165">Файлы могут индексироваться с помощью кода времени SMPTE, а как асинхронный читатель, так и синхронный читатель могут искать записи индекса кода времени SMPTE.</span><span class="sxs-lookup"><span data-stu-id="9a8a8-165">Files can be indexed by SMPTE time code, and both the asynchronous reader and synchronous reader can seek to SMPTE time code index entries.</span></span>

## <a name="directshow-filters"></a><span data-ttu-id="9a8a8-166">Фильтры DirectShow</span><span class="sxs-lookup"><span data-stu-id="9a8a8-166">DirectShow Filters</span></span>

<span data-ttu-id="9a8a8-167">Пакет SDK для формата Windows Media включает два фильтра® Microsoft DirectShow, которые позволяют приложениям на основе DirectShow читать и записывать файлы ASF.</span><span class="sxs-lookup"><span data-stu-id="9a8a8-167">The Windows Media Format SDK includes two Microsoft DirectShow® filters that enable DirectShow-based applications to read and write ASF files.</span></span> <span data-ttu-id="9a8a8-168">DirectShow также позволяет приложениям собирать данные с аудио-видео устройств и распаковать данные из различных форматов перед их повторной кодировкой в виде содержимого Windows Media.</span><span class="sxs-lookup"><span data-stu-id="9a8a8-168">DirectShow also enables applications to capture data from audio-video devices and decompress data from a variety of formats before re-encoding it as Windows Media-based content.</span></span>

## <a name="enhanced-profiles"></a><span data-ttu-id="9a8a8-169">Расширенные профили</span><span class="sxs-lookup"><span data-stu-id="9a8a8-169">Enhanced Profiles</span></span>

<span data-ttu-id="9a8a8-170">Профили могут содержать сведения о совместном использовании пропускной способности и сведения о приоритизации потоков.</span><span class="sxs-lookup"><span data-stu-id="9a8a8-170">Profiles can contain bandwidth sharing information and stream prioritization information.</span></span> <span data-ttu-id="9a8a8-171">Совместное использование пропускной способности позволяет указать, что два или больше потоков, независимо от их отдельных ставок, никогда не будут использовать больше указанного объема пропускной способности.</span><span class="sxs-lookup"><span data-stu-id="9a8a8-171">Bandwidth sharing enables you to specify that two or more streams, regardless of their individual bit rates, will never use more than a specified amount of bandwidth.</span></span> <span data-ttu-id="9a8a8-172">Данные, совместно использующие пропускную способность в профиле, являются исключительно информационными; Он не применяется ни одной логикой в пакете SDK.</span><span class="sxs-lookup"><span data-stu-id="9a8a8-172">The bandwidth sharing data in a profile is purely informational; it is not enforced by any logic in the SDK.</span></span> <span data-ttu-id="9a8a8-173">Определение приоритетов потоков позволяет указать порядок приоритета потоков в профиле.</span><span class="sxs-lookup"><span data-stu-id="9a8a8-173">Stream prioritization enables you to specify an order of priority for the streams in a profile.</span></span> <span data-ttu-id="9a8a8-174">Если при воспроизведении недостаточно пропускной способности для правильного потокового воспроизведения файла, потоки с наименьшим приоритетом можно игнорировать, чтобы повысить производительность.</span><span class="sxs-lookup"><span data-stu-id="9a8a8-174">If there is not enough bandwidth at playback to stream the file properly, the lowest priority streams can be ignored in order to improve performance.</span></span>

## <a name="drm-writing-capability"></a><span data-ttu-id="9a8a8-175">Возможность записи DRM</span><span class="sxs-lookup"><span data-stu-id="9a8a8-175">DRM Writing Capability</span></span>

<span data-ttu-id="9a8a8-176">В дополнение к существующей поддержке чтения DRM пакет SDK для Windows Media Format 9 добавляет поддержку для записи ASF-файлов с защитой версии 1 или DRM версии 7.</span><span class="sxs-lookup"><span data-stu-id="9a8a8-176">In addition to the existing DRM-reading support, the Windows Media Format 9 Series SDK added support for writing ASF files with either DRM version 1 or DRM version 7 protection.</span></span> <span data-ttu-id="9a8a8-177">Эта новая возможность позволяет выполнять сценарии "Live DRM", такие как веб-трансляции с оплатой по количеству интерактивных событий спортивных мероприятий или концертов.</span><span class="sxs-lookup"><span data-stu-id="9a8a8-177">This new capability enables "Live DRM" scenarios such as pay-per-view webcasting of live sporting events or concerts.</span></span>

## <a name="enhanced-file-sink"></a><span data-ttu-id="9a8a8-178">Расширенный приемник файлов</span><span class="sxs-lookup"><span data-stu-id="9a8a8-178">Enhanced File Sink</span></span>

<span data-ttu-id="9a8a8-179">В версию 9 серии пакета SDK было добавлено несколько новых возможностей приемника файлов.</span><span class="sxs-lookup"><span data-stu-id="9a8a8-179">Several new file sink capabilities were added to the 9 Series version of the SDK.</span></span> <span data-ttu-id="9a8a8-180">Можно настроить приемник файлов, чтобы отключить автоматическое индексирование только что созданных файлов ASF.</span><span class="sxs-lookup"><span data-stu-id="9a8a8-180">You can configure the file sink to disable automatic indexing of newly created ASF files.</span></span> <span data-ttu-id="9a8a8-181">Кроме того, можно настроить его для небуферизованного ввода и вывода.</span><span class="sxs-lookup"><span data-stu-id="9a8a8-181">You also have the option to configure it for unbuffered input and output.</span></span>

## <a name="directx-video-acceleration"></a><span data-ttu-id="9a8a8-182">Ускорение видео DirectX</span><span class="sxs-lookup"><span data-stu-id="9a8a8-182">DirectX Video Acceleration</span></span>

<span data-ttu-id="9a8a8-183">Ускорение видео DirectX (ДКСВА) — это технология, позволяющая воспроизводить видео с высокой скоростью (DVD-качеством или лучше) на менее мощных компьютерах с графическими картами с поддержкой ДКСВА.</span><span class="sxs-lookup"><span data-stu-id="9a8a8-183">DirectX Video Acceleration (DXVA) is a technology that enables playback of high-bit-rate video (DVD quality or better) on less powerful machines with DXVA-enabled graphics cards.</span></span> <span data-ttu-id="9a8a8-184">Объект модуля чтения этого пакета SDK можно использовать для включения ускорения видео DirectX, если оно поддерживается оборудованием при воспроизведении файлов ASF.</span><span class="sxs-lookup"><span data-stu-id="9a8a8-184">You can use the reader object of this SDK to enable DirectX Video Acceleration, if the hardware supports it, when playing ASF files.</span></span>

## <a name="multichannel-audio"></a><span data-ttu-id="9a8a8-185">Многоканальное аудио</span><span class="sxs-lookup"><span data-stu-id="9a8a8-185">Multichannel Audio</span></span>

<span data-ttu-id="9a8a8-186">Вы можете кодировать и воспроизводить многоканальное аудио.</span><span class="sxs-lookup"><span data-stu-id="9a8a8-186">You can encode and play multichannel audio.</span></span> <span data-ttu-id="9a8a8-187">Кодек Windows Media Audio 9 Professional поддерживает форматы с 6 каналами и 8 каналами, а также с стереосистемой высокой четкости.</span><span class="sxs-lookup"><span data-stu-id="9a8a8-187">The Windows Media Audio 9 Professional codec supports formats with 6 channels and 8 channels as well as high definition stereo.</span></span>

## <a name="watermarking"></a><span data-ttu-id="9a8a8-188">Водяные знаки</span><span class="sxs-lookup"><span data-stu-id="9a8a8-188">Watermarking</span></span>

<span data-ttu-id="9a8a8-189">Файлы ASF можно кодировать с помощью цифровых водяных знаков для обеспечения безопасности.</span><span class="sxs-lookup"><span data-stu-id="9a8a8-189">You can encode ASF files with digital watermarks for security.</span></span> <span data-ttu-id="9a8a8-190">Все системы водяного знака отличаются в своем подходе, но все они внедряются в закодированное содержимое.</span><span class="sxs-lookup"><span data-stu-id="9a8a8-190">All watermarking systems are different in their approach, but all embed identification into encoded content.</span></span> <span data-ttu-id="9a8a8-191">Водяные знаки выполняются с помощью специальных объектов мультимедиа®ов DirectX сторонних производителей (дмос).</span><span class="sxs-lookup"><span data-stu-id="9a8a8-191">Watermarking is performed using special third-party DirectX® media objects (DMOs).</span></span>

## <a name="support-for-multiple-languages-in-asf-files"></a><span data-ttu-id="9a8a8-192">Поддержка нескольких языков в файлах ASF</span><span class="sxs-lookup"><span data-stu-id="9a8a8-192">Support for Multiple Languages in ASF files</span></span>

<span data-ttu-id="9a8a8-193">В файлах ASF можно поддерживать несколько языков, как в потоках, так и в метаданных.</span><span class="sxs-lookup"><span data-stu-id="9a8a8-193">You can support multiple languages in ASF files, both in streams and in metadata.</span></span> <span data-ttu-id="9a8a8-194">Например, можно создать видеофайл с аудио-потоками на нескольких языках.</span><span class="sxs-lookup"><span data-stu-id="9a8a8-194">For example, you can create a video file with audio streams in several languages.</span></span> <span data-ttu-id="9a8a8-195">При воспроизведении пользователь может выбрать язык, который будет использоваться, или ваше приложение может запросить сведения о системе на воспроизводимом компьютере и выбрать язык автоматически.</span><span class="sxs-lookup"><span data-stu-id="9a8a8-195">At playback, the user can select which language to use, or your application can query the system information on the playing computer and select a language automatically.</span></span> <span data-ttu-id="9a8a8-196">Атрибуты метаданных также могут быть указаны несколько раз со значениями на разных языках.</span><span class="sxs-lookup"><span data-stu-id="9a8a8-196">Metadata attributes can also be entered multiple times, with the values in different languages.</span></span>

## <a name="device-conformance-templates"></a><span data-ttu-id="9a8a8-197">Шаблоны соответствия устройств</span><span class="sxs-lookup"><span data-stu-id="9a8a8-197">Device Conformance Templates</span></span>

<span data-ttu-id="9a8a8-198">Чтобы помочь в нацеливании содержимого на определенные клиентские устройства, кодеки Windows Media теперь поддерживают шаблоны соответствия устройств.</span><span class="sxs-lookup"><span data-stu-id="9a8a8-198">To assist in targeting content to specific client devices, the Windows Media codecs now support device conformance templates.</span></span> <span data-ttu-id="9a8a8-199">Каждый шаблон содержит определенный диапазон параметров и функций кодеков, которые следует использовать для мультимедиа, предназначенного для определенной категории платформ.</span><span class="sxs-lookup"><span data-stu-id="9a8a8-199">Each template contains a defined range of settings and codec features that should be used for media intended for a particular category of platforms.</span></span> <span data-ttu-id="9a8a8-200">Системные профили больше не поддерживаются в последних версиях кодеков Windows Media.</span><span class="sxs-lookup"><span data-stu-id="9a8a8-200">System profiles are no longer supported with the latest versions of the Windows Media codecs.</span></span> <span data-ttu-id="9a8a8-201">Все профили должны быть настроены в соответствии со своими потребностями.</span><span class="sxs-lookup"><span data-stu-id="9a8a8-201">All profiles must be customized to suit your needs.</span></span> <span data-ttu-id="9a8a8-202">Шаблоны соответствия устройств можно использовать для создания профилей.</span><span class="sxs-lookup"><span data-stu-id="9a8a8-202">You can use device conformance templates to assist you in designing your profiles.</span></span>

## <a name="expanded-codec-enumeration"></a><span data-ttu-id="9a8a8-203">Расширенное перечисление кодеков</span><span class="sxs-lookup"><span data-stu-id="9a8a8-203">Expanded Codec Enumeration</span></span>

<span data-ttu-id="9a8a8-204">Объект диспетчера профилей может выполнять запросы к аудиокодекам Windows Media Audio и Video для поддерживаемых форматов.</span><span class="sxs-lookup"><span data-stu-id="9a8a8-204">The profile manager object can query the Windows Media Audio and Video codecs for supported formats.</span></span> <span data-ttu-id="9a8a8-205">Можно задать параметры для извлекаемых форматов.</span><span class="sxs-lookup"><span data-stu-id="9a8a8-205">You can set parameters for the formats retrieved.</span></span> <span data-ttu-id="9a8a8-206">Например, можно получить все форматы битовой частоты переменной на основе качества, поддерживаемые кодеком Windows Media Audio 9.</span><span class="sxs-lookup"><span data-stu-id="9a8a8-206">For example, you can retrieve all the quality-based variable bit rate formats supported by the Windows Media Audio 9 codec.</span></span>

## <a name="improved-mutual-exclusion"></a><span data-ttu-id="9a8a8-207">Улучшено взаимоисключающее исключение</span><span class="sxs-lookup"><span data-stu-id="9a8a8-207">Improved Mutual Exclusion</span></span>

<span data-ttu-id="9a8a8-208">В взаимоисключающем объекте можно создавать именованные записи, содержащие несколько потоков.</span><span class="sxs-lookup"><span data-stu-id="9a8a8-208">You can create named records containing multiple streams within a mutual exclusion object.</span></span> <span data-ttu-id="9a8a8-209">Можно также наименовать взаимоисключающие объекты, чтобы упростить их определение.</span><span class="sxs-lookup"><span data-stu-id="9a8a8-209">You can also name mutual exclusion objects to make them easier to identify.</span></span> <span data-ttu-id="9a8a8-210">Это позволяет создавать слои взаимного исключения.</span><span class="sxs-lookup"><span data-stu-id="9a8a8-210">This enables you to create layers of mutual exclusion.</span></span> <span data-ttu-id="9a8a8-211">Например, файл может содержать потоки, которые являются взаимоисключающими по скорости потока и по языку.</span><span class="sxs-lookup"><span data-stu-id="9a8a8-211">For example, a file can contain streams that are mutually exclusive by bit rate and by language.</span></span> <span data-ttu-id="9a8a8-212">При взаимном исключении на основе языка будут использоваться группы потоков, каждая из которых состоит из потоков на том же языке, но взаимоисключающая с побитовой скоростью.</span><span class="sxs-lookup"><span data-stu-id="9a8a8-212">The language-based mutual exclusion would involve groups of streams, each group consisting of streams in the same language but mutually exclusive by bit rate.</span></span>

## <a name="expanded-multiple-bit-rate-support"></a><span data-ttu-id="9a8a8-213">Расширенная поддержка нескольких битов разрядов</span><span class="sxs-lookup"><span data-stu-id="9a8a8-213">Expanded Multiple Bit Rate Support</span></span>

<span data-ttu-id="9a8a8-214">Поддержка взаимного исключения включена для звука с несколькими скоростями (MBR) и для видео с потоками различных размеров образов.</span><span class="sxs-lookup"><span data-stu-id="9a8a8-214">Mutual exclusion support is included for multiple bit rate (MBR) audio and for video with streams of varying image sizes.</span></span>

## <a name="attributes-for-streams"></a><span data-ttu-id="9a8a8-215">Атрибуты для потоков</span><span class="sxs-lookup"><span data-stu-id="9a8a8-215">Attributes for Streams</span></span>

<span data-ttu-id="9a8a8-216">Можно назначить атрибуты отдельным потокам в файлах ASF.</span><span class="sxs-lookup"><span data-stu-id="9a8a8-216">You can assign attributes to individual streams in ASF files.</span></span> <span data-ttu-id="9a8a8-217">Для файлов MP3 по-прежнему необходимо использовать атрибуты уровня файла.</span><span class="sxs-lookup"><span data-stu-id="9a8a8-217">You must still use file-level attributes for MP3 files.</span></span> <span data-ttu-id="9a8a8-218">Эта функция не добавляет никакие методы в пакет SDK, но существующие методы теперь принимают номера потоков, отличные от нуля.</span><span class="sxs-lookup"><span data-stu-id="9a8a8-218">This feature does not add any methods to the SDK, but the existing methods will now accept stream numbers other than zero.</span></span>

## <a name="transcoding-with-smart-recompression"></a><span data-ttu-id="9a8a8-219">Перекодирование с помощью интеллектуального повторного сжатия</span><span class="sxs-lookup"><span data-stu-id="9a8a8-219">Transcoding with Smart Recompression</span></span>

<span data-ttu-id="9a8a8-220">Интеллектуальное повторное сжатие позволяет перекодировать звуковые файлы Windows Media с высокой скоростью до более низкой скорости с более низким качеством, чем ранее достижимые.</span><span class="sxs-lookup"><span data-stu-id="9a8a8-220">Smart recompression allows you to transcode Windows Media audio files from a high bit rate to a lower bit rate with better quality than previously achievable.</span></span>

## <a name="expanded-metadata-support"></a><span data-ttu-id="9a8a8-221">Расширенная поддержка метаданных</span><span class="sxs-lookup"><span data-stu-id="9a8a8-221">Expanded Metadata Support</span></span>

<span data-ttu-id="9a8a8-222">Пакет Windows Media Format SDK предоставляет следующие новые функции метаданных:</span><span class="sxs-lookup"><span data-stu-id="9a8a8-222">The Windows Media Format SDK provides the following new metadata features:</span></span>

-   <span data-ttu-id="9a8a8-223">Теги метаданных на основе индекса, позволяющие использовать несколько тегов с одинаковыми именами.</span><span class="sxs-lookup"><span data-stu-id="9a8a8-223">Index-based metadata tags, enabling multiple tags with the same name.</span></span>
-   <span data-ttu-id="9a8a8-224">Возможность чтения атрибутов заголовка DRM без файла Вмстубдрм. lib.</span><span class="sxs-lookup"><span data-stu-id="9a8a8-224">Ability to read DRM header attributes without a WMStubDRM.lib file.</span></span>
-   <span data-ttu-id="9a8a8-225">Атрибуты с более чем 64 килобайтами связанных данных.</span><span class="sxs-lookup"><span data-stu-id="9a8a8-225">Attributes with more than 64 kilobytes of associated data.</span></span>
-   <span data-ttu-id="9a8a8-226">Атрибуты на нескольких языках.</span><span class="sxs-lookup"><span data-stu-id="9a8a8-226">Attributes in multiple languages.</span></span>
-   <span data-ttu-id="9a8a8-227">Десятки новых предопределенных атрибутов.</span><span class="sxs-lookup"><span data-stu-id="9a8a8-227">Dozens of new predefined attributes.</span></span>

## <a name="dynamic-pixel-aspect-ratio"></a><span data-ttu-id="9a8a8-228">Динамическое пропорции пикселей</span><span class="sxs-lookup"><span data-stu-id="9a8a8-228">Dynamic Pixel Aspect Ratio</span></span>

<span data-ttu-id="9a8a8-229">Видеопотокы, состоящие из различных типов содержимого, могут быть адаптированы путем определения пропорций пикселов разнородных выборок в потоке.</span><span class="sxs-lookup"><span data-stu-id="9a8a8-229">Video streams that are composed of various types of content can be accommodated by identifying the pixel aspect ratio of the disparate samples in the stream.</span></span> <span data-ttu-id="9a8a8-230">Это позволяет воспроизводить приложение, чтобы обеспечить лучшее воспроизведение такого содержимого.</span><span class="sxs-lookup"><span data-stu-id="9a8a8-230">This enables the playing application to provide better playback of such content.</span></span>

## <a name="interlaced-video-streams"></a><span data-ttu-id="9a8a8-231">Потоки видео с чередованием</span><span class="sxs-lookup"><span data-stu-id="9a8a8-231">Interlaced Video Streams</span></span>

<span data-ttu-id="9a8a8-232">Предыдущие версии пакета SDK Windows Media Format позволяют кодировать содержимое с [*чередованием*](wmformat-glossary.md) в поток видео с последовательным сканированием.</span><span class="sxs-lookup"><span data-stu-id="9a8a8-232">Previous versions of the Windows Media Format SDK have provided the ability to encode [*interlaced*](wmformat-glossary.md) content into a progressive-scan video stream.</span></span> <span data-ttu-id="9a8a8-233">Начиная с пакета SDK для Windows Media Format 9, вы можете закодировать видео с чередованием, сохранив свой формат с чередованием.</span><span class="sxs-lookup"><span data-stu-id="9a8a8-233">Starting with the Windows Media Format 9 Series SDK, you can encode interlaced video while preserving its interlaced format.</span></span> <span data-ttu-id="9a8a8-234">Это может привести к улучшению воспроизведения, особенно на чередующихся устройствах, таких как телевизионные наборы.</span><span class="sxs-lookup"><span data-stu-id="9a8a8-234">This can result in improved playback, particularly on interlaced devices, such as television sets.</span></span>

## <a name="two-pass-encoding"></a><span data-ttu-id="9a8a8-235">Кодировка Two-Pass</span><span class="sxs-lookup"><span data-stu-id="9a8a8-235">Two-Pass Encoding</span></span>

<span data-ttu-id="9a8a8-236">Новые кодеки Windows Media поддерживают двустороннюю кодировку.</span><span class="sxs-lookup"><span data-stu-id="9a8a8-236">The new Windows Media codecs enable two-pass encoding.</span></span> <span data-ttu-id="9a8a8-237">Содержимое, закодированное на двух этапах, может обеспечить более высокое качество вывода.</span><span class="sxs-lookup"><span data-stu-id="9a8a8-237">Content encoded in two passes can achieve higher quality output.</span></span>

## <a name="new-speech-codec"></a><span data-ttu-id="9a8a8-238">Новый кодек речи</span><span class="sxs-lookup"><span data-stu-id="9a8a8-238">New Speech Codec</span></span>

<span data-ttu-id="9a8a8-239">Этот пакет SDK включает новый голосовой кодек Windows Media Audio 9, оптимизированный для кодирования человеческого голоса с низкой скоростью.</span><span class="sxs-lookup"><span data-stu-id="9a8a8-239">This SDK includes the new Windows Media Audio 9 Voice codec which is optimized for encoding the human voice while using a low bit rate.</span></span> <span data-ttu-id="9a8a8-240">Этот кодек также обеспечивает высокую производительность для смешанного содержимого музыки.</span><span class="sxs-lookup"><span data-stu-id="9a8a8-240">This codec also provides superior performance for mixed music-voice content.</span></span>

## <a name="accessible-video-frame-duration"></a><span data-ttu-id="9a8a8-241">Длительность кадра видео со специальными возможностями</span><span class="sxs-lookup"><span data-stu-id="9a8a8-241">Accessible Video Frame Duration</span></span>

<span data-ttu-id="9a8a8-242">У вас может быть объект модуля записи этого пакета SDK, который предоставляет читателю время для кадров видео.</span><span class="sxs-lookup"><span data-stu-id="9a8a8-242">You can have the writer object of this SDK provide the duration of video frames to the reader.</span></span>

## <a name="streaming-html"></a><span data-ttu-id="9a8a8-243">Потоковая передача HTML</span><span class="sxs-lookup"><span data-stu-id="9a8a8-243">Streaming HTML</span></span>

<span data-ttu-id="9a8a8-244">С помощью предыдущей версии этого пакета SDK вы могли использовать команду сценария, чтобы сообщить приложению о необходимости открыть веб-страницу.</span><span class="sxs-lookup"><span data-stu-id="9a8a8-244">With previous version of this SDK, you were able to use a script command to signal your application to open a Web page.</span></span> <span data-ttu-id="9a8a8-245">Начиная с пакета SDK для Windows Media Format 9, можно хранить компоненты веб-страниц в файлах ASF, чтобы избежать задержки в презентациях.</span><span class="sxs-lookup"><span data-stu-id="9a8a8-245">Starting with the Windows Media Format 9 Series SDK, you can store the components of Web pages in your ASF files, to ensure that there is no lag in presentations.</span></span>

## <a name="wmstublib-no-longer-required-for-build-environment"></a><span data-ttu-id="9a8a8-246">Вмстуб. lib больше не требуется для среды сборки</span><span class="sxs-lookup"><span data-stu-id="9a8a8-246">WMStub.lib no longer required for build environment</span></span>

<span data-ttu-id="9a8a8-247">Параметры среды сборки для пакета SDK Windows Media Format изменились, начиная с пакета SDK серии Windows Media Format 9.</span><span class="sxs-lookup"><span data-stu-id="9a8a8-247">The build-environment settings for the Windows Media Format SDK changed starting with the Windows Media Format 9 Series SDK.</span></span> <span data-ttu-id="9a8a8-248">Вам больше не нужно включать Вмстуб. lib для приложений, использующих этот пакет SDK.</span><span class="sxs-lookup"><span data-stu-id="9a8a8-248">You no longer need to include WMStub.lib for applications using this SDK.</span></span> <span data-ttu-id="9a8a8-249">Тем не менее приложения с поддержкой DRM должны получить и подписать отдельное лицензионное соглашение, а также получить уникальную статическую библиотеку от корпорации Майкрософт.</span><span class="sxs-lookup"><span data-stu-id="9a8a8-249">However, DRM-enabled applications still must obtain and sign a separate license agreement, and obtain a unique static library from Microsoft.</span></span> <span data-ttu-id="9a8a8-250">Обратитесь wmla@microsoft.com за дополнительными сведениями о библиотеке DRM и лицензионном соглашении.</span><span class="sxs-lookup"><span data-stu-id="9a8a8-250">Contact wmla@microsoft.com for more information about the DRM library and license agreement.</span></span> <span data-ttu-id="9a8a8-251">Дополнительные сведения о создании проектов с помощью этого пакета SDK см. в разделе [файлы библиотеки и параметры компилятора](library-files-and-compiler-settings.md).</span><span class="sxs-lookup"><span data-stu-id="9a8a8-251">For more information about building projects with this SDK, see [Library Files and Compiler Settings](library-files-and-compiler-settings.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="9a8a8-252">См. также</span><span class="sxs-lookup"><span data-stu-id="9a8a8-252">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9a8a8-253">**О пакете SDK для формата Windows Media**</span><span class="sxs-lookup"><span data-stu-id="9a8a8-253">**About the Windows Media Format SDK**</span></span>](about-the-windows-media-format-sdk.md)
</dt> </dl>

 

 




