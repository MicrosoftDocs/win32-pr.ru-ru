---
description: Настройка модуля записи ASF
ms.assetid: 5708c4a0-6197-4a42-adfd-01c6dfe86302
title: Настройка модуля записи ASF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 62a6dfc1827743dce946188ebf9e050226b5c484
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "105662027"
---
# <a name="configuring-the-asf-writer"></a><span data-ttu-id="0f38e-103">Настройка модуля записи ASF</span><span class="sxs-lookup"><span data-stu-id="0f38e-103">Configuring the ASF Writer</span></span>

<span data-ttu-id="0f38e-104">При создании фильтра [модуля записи WM ASF](wm-asf-writer-filter.md) он автоматически настраивается с помощью профиля вмпрофиле \_ V80 \_ 256Video.</span><span class="sxs-lookup"><span data-stu-id="0f38e-104">When the [WM ASF Writer](wm-asf-writer-filter.md) filter is created, it is configured automatically with the WMProfile\_V80\_256Video profile.</span></span> <span data-ttu-id="0f38e-105">Этот профиль использует кодеки Windows Media Audio и Windows Media Video версии 8, которые не являются последними кодеками Windows Media 9 Series.</span><span class="sxs-lookup"><span data-stu-id="0f38e-105">This profile uses the Windows Media Audio and Windows Media Video version 8 codecs, which are not as recent as the Windows Media 9 Series codecs.</span></span> <span data-ttu-id="0f38e-106">Рекомендуется создать настраиваемый профиль, использующий кодеки Windows Media 9, и настроить модуль записи WM ASF с помощью настраиваемого профиля, как описано в разделе [Настройка профилей и других свойств ASF-файлов](configuring-profiles-and-other-asf-file-properties.md).</span><span class="sxs-lookup"><span data-stu-id="0f38e-106">It is recommended to create a custom profile that uses the Windows Media 9 Series codecs, and configure the WM ASF Writer with the custom profile, as described in [Configuring Profiles and Other ASF File Properties](configuring-profiles-and-other-asf-file-properties.md).</span></span> <span data-ttu-id="0f38e-107">Перед настройкой фильтра необходимо добавить фильтр модуля записи WM ASF в граф фильтра, а затем настроить фильтр перед его подключением к другим фильтрам.</span><span class="sxs-lookup"><span data-stu-id="0f38e-107">You must add the WM ASF Writer filter to the filter graph before configuring the filter, and configure the filter before connecting it to any other filters.</span></span>

<span data-ttu-id="0f38e-108">Все входные данные должны иметь отметку времени, и все входные ПИН-коды должны быть подключены, прежде чем можно будет запустить или приостановить фильтр.</span><span class="sxs-lookup"><span data-stu-id="0f38e-108">All input data must be time-stamped, and all input pins must be connected before the filter can be run or paused.</span></span> <span data-ttu-id="0f38e-109">Таким образом, если вы настроите фильтр с профилем, который содержит аудиопоток и поток видео, фильтр создаст звук и ПИН-код входного видео, и оба контакта должны быть подключены, прежде чем можно будет запустить фильтр.</span><span class="sxs-lookup"><span data-stu-id="0f38e-109">Therefore, if you configure the filter with a profile that has an audio stream and a video stream, the filter will create an audio and a video input pin, and both pins must be connected before the filter can be run.</span></span> <span data-ttu-id="0f38e-110">Поскольку пакет SDK для формата Windows Media требует, чтобы поток аудио работал, модуль записи WM ASF всегда должен иметь входной ПИН-код, даже если он предназначен для фиктивного потока, то есть звукового потока с низкими разрядами.</span><span class="sxs-lookup"><span data-stu-id="0f38e-110">Because the Windows Media Format SDK requires an audio stream to work, the WM ASF Writer must always have an input audio pin, even if it is for a dummy stream—that is, a muted, low-bit-rate audio stream.</span></span>

<span data-ttu-id="0f38e-111">Добавление модулей обработки данных</span><span class="sxs-lookup"><span data-stu-id="0f38e-111">Adding Data Unit Extensions</span></span>

<span data-ttu-id="0f38e-112">Вы можете настроить поток профиля для модулей обработки данных, например коды времени SMPTE до или после подключения фильтра, при условии, что выполняется следующий порядок операций:</span><span class="sxs-lookup"><span data-stu-id="0f38e-112">You can configure a profile stream for data unit extensions, such as SMPTE time codes, either before or after the filter is connected, as long as you follow this order of operations:</span></span>

1.  <span data-ttu-id="0f38e-113">Добавьте в поток одно или несколько расширений модулей данных с помощью **IWMStreamConfig2:: адддатаунитекстенсион**.</span><span class="sxs-lookup"><span data-stu-id="0f38e-113">Add one or more data unit extensions to the stream using **IWMStreamConfig2::AddDataUnitExtension**.</span></span>
2.  <span data-ttu-id="0f38e-114">Вызовите **ивмпрофиле:: реконфигстреам** , чтобы обновить профиль.</span><span class="sxs-lookup"><span data-stu-id="0f38e-114">Call **IWMProfile::ReconfigStream** to update the profile.</span></span>
3.  <span data-ttu-id="0f38e-115">Вызовите [**иконфигасфвритер:: конфигурефилтерусингпрофиле**](/previous-versions/windows/desktop/api/Dshowasf/nf-dshowasf-iconfigasfwriter-configurefilterusingprofile) с обновленным объектом Profile.</span><span class="sxs-lookup"><span data-stu-id="0f38e-115">Call [**IConfigAsfWriter::ConfigureFilterUsingProfile**](/previous-versions/windows/desktop/api/Dshowasf/nf-dshowasf-iconfigasfwriter-configurefilterusingprofile) with the updated profile object.</span></span>
4.  <span data-ttu-id="0f38e-116">Найдите ПИН-код входного видео и вызовите его метод [**иамвмбуфферпасс:: сетнотифи**](/previous-versions/windows/desktop/api/Dshowasf/nf-dshowasf-iamwmbufferpass-setnotify) , чтобы зарегистрировать определяемый приложением интерфейс [**иамвмбуфферпасскаллбакк**](/previous-versions/windows/desktop/api/Dshowasf/nn-dshowasf-iamwmbufferpasscallback) .</span><span class="sxs-lookup"><span data-stu-id="0f38e-116">Find the video input pin, and call its [**IAMWMBufferPass::SetNotify**](/previous-versions/windows/desktop/api/Dshowasf/nf-dshowasf-iamwmbufferpass-setnotify) method to register your application-defined [**IAMWMBufferPassCallback**](/previous-versions/windows/desktop/api/Dshowasf/nn-dshowasf-iamwmbufferpasscallback) interface.</span></span>

<span data-ttu-id="0f38e-117">При запуске графа метод [**иамвмбуфферпасскаллбакк:: notify**](/previous-versions/windows/desktop/api/Dshowasf/nf-dshowasf-iamwmbufferpasscallback-notify) будет вызываться для каждого кадра, и вы сможете получить и задать свойства в образце с помощью его методов интерфейса **INSSBuffer3** .</span><span class="sxs-lookup"><span data-stu-id="0f38e-117">When the graph runs, your [**IAMWMBufferPassCallback::Notify**](/previous-versions/windows/desktop/api/Dshowasf/nf-dshowasf-iamwmbufferpasscallback-notify) method will be called for each frame, and you will be able to get and set properties on the sample using its **INSSBuffer3** interface methods.</span></span>

> [!Note]  
> <span data-ttu-id="0f38e-118">В некоторых сценариях с интенсивным использованием процессора, таких как инверсный чересстрочности, модуль записи WM ASF может потребовать больше буферов вывода, чем может поддерживать некоторые нисходящие фильтры.</span><span class="sxs-lookup"><span data-stu-id="0f38e-118">In some processor-intensive scenarios such as inverse telecine, the WM ASF Writer may require more output buffers than some downstream filters can support.</span></span> <span data-ttu-id="0f38e-119">Например, декодер DV не принимает более одного буфера для выходного ПИН-кода, и это справедливо для распаковки AVI в определенных условиях.</span><span class="sxs-lookup"><span data-stu-id="0f38e-119">The DV Decoder, for example, will not accept more than one buffer for its output pin and the same is true for the AVI Decompressor in certain conditions.</span></span> <span data-ttu-id="0f38e-120">При возникновении проблем при попытке подключения к этим фильтрам или, возможно, при запуске графа, может потребоваться написать промежуточный фильтр, который принимает любое количество буферов на выходном ПИН-коде.</span><span class="sxs-lookup"><span data-stu-id="0f38e-120">If you encounter problems when attempting to connect to these filters, or possibly when running the graph, it may be necessary to write an intermediary filter that accepts any number of buffers on its output pin.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="0f38e-121">См. также</span><span class="sxs-lookup"><span data-stu-id="0f38e-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0f38e-122">Создание файлов ASF в DirectShow</span><span class="sxs-lookup"><span data-stu-id="0f38e-122">Creating ASF Files in DirectShow</span></span>](creating-asf-files-in-directshow.md)
</dt> </dl>

 

 



