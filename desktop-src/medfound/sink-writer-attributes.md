---
description: Атрибуты модуля записи приемника
ms.assetid: f27b9beb-f35f-400e-a337-50d9de21e91e
title: Атрибуты модуля записи приемника
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e23dbca06c3ff1a4ac80b8e68413fdd0816d71a5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104155315"
---
# <a name="sink-writer-attributes"></a><span data-ttu-id="6cb0b-103">Атрибуты модуля записи приемника</span><span class="sxs-lookup"><span data-stu-id="6cb0b-103">Sink Writer Attributes</span></span>

<span data-ttu-id="6cb0b-104">Для инициализации модуля записи приемника можно использовать следующие атрибуты.</span><span class="sxs-lookup"><span data-stu-id="6cb0b-104">The following attributes can be used to initialize the sink writer.</span></span>



| <span data-ttu-id="6cb0b-105">attribute</span><span class="sxs-lookup"><span data-stu-id="6cb0b-105">Attribute</span></span>                                                                                  | <span data-ttu-id="6cb0b-106">Описание</span><span class="sxs-lookup"><span data-stu-id="6cb0b-106">Description</span></span>                                                                                                                                                                                                                        |
|--------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="6cb0b-107">MF \_ низкая \_ Задержка</span><span class="sxs-lookup"><span data-stu-id="6cb0b-107">MF\_LOW\_LATENCY</span></span>](mf-low-latency.md)                                                     | <span data-ttu-id="6cb0b-108">Включает обработку с низкой задержкой.</span><span class="sxs-lookup"><span data-stu-id="6cb0b-108">Enables low-latency processing.</span></span>                                                                                                                                                                                                    |
| [<span data-ttu-id="6cb0b-109">\_ \_ запретить \_ конвертеры MF ReadWrite</span><span class="sxs-lookup"><span data-stu-id="6cb0b-109">MF\_READWRITE\_DISABLE\_CONVERTERS</span></span>](mf-readwrite-disable-converters.md)                  | <span data-ttu-id="6cb0b-110">Включает или отключает преобразование формата модулем записи приемника.</span><span class="sxs-lookup"><span data-stu-id="6cb0b-110">Enables or disables format conversions by the sink writer.</span></span>                                                                                                                                                                         |
| [<span data-ttu-id="6cb0b-111">MF. \_ Чтение с \_ включением \_ аппаратных \_ преобразований</span><span class="sxs-lookup"><span data-stu-id="6cb0b-111">MF\_READWRITE\_ENABLE\_HARDWARE\_TRANSFORMS</span></span>](mf-readwrite-enable-hardware-transforms.md) | <span data-ttu-id="6cb0b-112">Позволяет модулю записи приемника использовать Media Foundation преобразования на основе оборудования (МФТС).</span><span class="sxs-lookup"><span data-stu-id="6cb0b-112">Enables the sink writer to use hardware-based Media Foundation transforms (MFTs).</span></span>                                                                                                                                                  |
| [<span data-ttu-id="6cb0b-113">\_ \_ \_ асинхронный обратный вызов для модуля записи MF SINK \_</span><span class="sxs-lookup"><span data-stu-id="6cb0b-113">MF\_SINK\_WRITER\_ASYNC\_CALLBACK</span></span>](mf-sink-writer-async-callback.md)                     | <span data-ttu-id="6cb0b-114">Содержит указатель на интерфейс обратного вызова приложения для модуля записи приемника.</span><span class="sxs-lookup"><span data-stu-id="6cb0b-114">Contains a pointer to the application's callback interface for the sink writer.</span></span>                                                                                                                                                    |
| [<span data-ttu-id="6cb0b-115">Программа \_ записи приемника MF \_ \_ отключает \_ регулирование</span><span class="sxs-lookup"><span data-stu-id="6cb0b-115">MF\_SINK\_WRITER\_DISABLE\_THROTTLING</span></span>](mf-sink-writer-disable-throttling.md)             | <span data-ttu-id="6cb0b-116">Указывает, ограничивает ли модуль записи приемника скорость входящих данных.</span><span class="sxs-lookup"><span data-stu-id="6cb0b-116">Specifies whether the sink writer limits the rate of incoming data.</span></span>                                                                                                                                                                |
| [<span data-ttu-id="6cb0b-117">MF \_ \_ контаинертипе</span><span class="sxs-lookup"><span data-stu-id="6cb0b-117">MF\_TRANSCODE\_CONTAINERTYPE</span></span>](mf-transcode-containertype.md)                             | <span data-ttu-id="6cb0b-118">Указывает тип контейнера выходного файла.</span><span class="sxs-lookup"><span data-stu-id="6cb0b-118">Specifies the container type of the output file.</span></span>                                                                                                                                                                                   |
| [<span data-ttu-id="6cb0b-119">\_Атрибут MFT фиелдофусе \_ Unlock \_</span><span class="sxs-lookup"><span data-stu-id="6cb0b-119">MFT\_FIELDOFUSE\_UNLOCK\_Attribute</span></span>](mft-fieldofuse-unlock-attribute.md)                  | <span data-ttu-id="6cb0b-120">Содержит указатель [**имффиелдофусемфтунлокк**](/windows/desktop/api/mfidl/nn-mfidl-imffieldofusemftunlock) , который используется для разблокировки MFT с ограничениями на использование полей.</span><span class="sxs-lookup"><span data-stu-id="6cb0b-120">Contains an [**IMFFieldOfUseMFTUnlock**](/windows/desktop/api/mfidl/nn-mfidl-imffieldofusemftunlock) pointer, which is used to unlock an MFT with field-of-use restrictions.</span></span> <span data-ttu-id="6cb0b-121">Дополнительные сведения см. в разделе [ограничения использования](field-of-use-restrictions.md).</span><span class="sxs-lookup"><span data-stu-id="6cb0b-121">For more information, see [Field of Use Restrictions](field-of-use-restrictions.md).</span></span> |
| [<span data-ttu-id="6cb0b-122">\_ \_ Диспетчер D3D модуля записи MF SINK \_ \_</span><span class="sxs-lookup"><span data-stu-id="6cb0b-122">MF\_SINK\_WRITER\_D3D\_MANAGER</span></span>](mf-sink-writer-d3d-manager.md)                           | <span data-ttu-id="6cb0b-123">Используйте этот атрибут, чтобы предоставить устройство Direct3D для любых видеокодировщиков или приемников мультимедиа, загруженных модулем записи приемника.</span><span class="sxs-lookup"><span data-stu-id="6cb0b-123">Use this attribute to provide a Direct3D device for any video encoders or media sinks loaded by the sink writer.</span></span>                                                                                                                   |



 

<span data-ttu-id="6cb0b-124">Используйте эти атрибуты со следующими методами и функциями:</span><span class="sxs-lookup"><span data-stu-id="6cb0b-124">Use these attributes with the following methods and functions:</span></span>

-   [<span data-ttu-id="6cb0b-125">**Имфреадвритеклассфактори:: Креатеинстанцефромобжект**</span><span class="sxs-lookup"><span data-stu-id="6cb0b-125">**IMFReadWriteClassFactory::CreateInstanceFromObject**</span></span>](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfreadwriteclassfactory-createinstancefromobject)
-   [<span data-ttu-id="6cb0b-126">**Имфреадвритеклассфактори:: Креатеинстанцефромурл**</span><span class="sxs-lookup"><span data-stu-id="6cb0b-126">**IMFReadWriteClassFactory::CreateInstanceFromURL**</span></span>](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfreadwriteclassfactory-createinstancefromurl)
-   [<span data-ttu-id="6cb0b-127">**мфкреатесинквритерфроммедиасинк**</span><span class="sxs-lookup"><span data-stu-id="6cb0b-127">**MFCreateSinkWriterFromMediaSink**</span></span>](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesinkwriterfrommediasink)
-   [<span data-ttu-id="6cb0b-128">**мфкреатесинквритерфромурл**</span><span class="sxs-lookup"><span data-stu-id="6cb0b-128">**MFCreateSinkWriterFromURL**</span></span>](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesinkwriterfromurl)

<span data-ttu-id="6cb0b-129">Чтобы использовать любой из этих атрибутов, сначала вызовите [**мфкреатеаттрибутес**](/windows/desktop/api/mfapi/nf-mfapi-mfcreateattributes) , чтобы создать новое хранилище атрибутов.</span><span class="sxs-lookup"><span data-stu-id="6cb0b-129">To use any of these attributes, first call [**MFCreateAttributes**](/windows/desktop/api/mfapi/nf-mfapi-mfcreateattributes) to create a new attribute store.</span></span> <span data-ttu-id="6cb0b-130">Затем используйте интерфейс [**имфаттрибутес**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) , чтобы задать необходимые атрибуты в хранилище атрибутов.</span><span class="sxs-lookup"><span data-stu-id="6cb0b-130">Then use the [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) interface to set the desired attributes on the attribute store.</span></span> <span data-ttu-id="6cb0b-131">Передайте указатель **имфаттрибутес** в параметр *паттрибутес* любого из указанных выше методов или функций.</span><span class="sxs-lookup"><span data-stu-id="6cb0b-131">Pass the **IMFAttributes** pointer to the *pAttributes* parameter of any of the methods or functions listed previously.</span></span>

## <a name="related-topics"></a><span data-ttu-id="6cb0b-132">См. также</span><span class="sxs-lookup"><span data-stu-id="6cb0b-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6cb0b-133">**имфсинквритер**</span><span class="sxs-lookup"><span data-stu-id="6cb0b-133">**IMFSinkWriter**</span></span>](/windows/desktop/api/mfreadwrite/nn-mfreadwrite-imfsinkwriter)
</dt> <dt>

[<span data-ttu-id="6cb0b-134">Атрибуты Media Foundation</span><span class="sxs-lookup"><span data-stu-id="6cb0b-134">Media Foundation Attributes</span></span>](media-foundation-attributes.md)
</dt> </dl>

 

 



