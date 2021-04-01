---
description: Преимущества потоковой передачи мультимедиа
ms.assetid: 01020ad5-430d-4b4d-8de3-bcc81270e132
title: Преимущества потоковой передачи мультимедиа
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bd907d9b8e91cb61709479a2d600323d6d420958
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/03/2021
ms.locfileid: "104157003"
---
# <a name="advantages-of-multimedia-streaming"></a><span data-ttu-id="8731d-103">Преимущества потоковой передачи мультимедиа</span><span class="sxs-lookup"><span data-stu-id="8731d-103">Advantages of Multimedia Streaming</span></span>

> [!Note]  
> <span data-ttu-id="8731d-104">Эти API-интерфейсы являются устаревшими.</span><span class="sxs-lookup"><span data-stu-id="8731d-104">These APIs are deprecated.</span></span> <span data-ttu-id="8731d-105">Приложения должны использовать [**образец фильтра захвата**](sample-grabber-filter.md) или реализовать настраиваемый фильтр для получения данных из графа фильтра DirectShow.</span><span class="sxs-lookup"><span data-stu-id="8731d-105">Applications should use the [**Sample Grabber**](sample-grabber-filter.md) filter or implement a custom filter to get data from a DirectShow filter graph.</span></span>

 

<span data-ttu-id="8731d-106">Когда разработчики используют потоковую передачу мультимедиа в своих приложениях, значительно сокращается потребность в программировании для конкретного формата.</span><span class="sxs-lookup"><span data-stu-id="8731d-106">When developers use multimedia streaming in their applications, it greatly reduces the amount of format-specific programming needed.</span></span> <span data-ttu-id="8731d-107">Как правило, приложение, которое должно получать мультимедийные данные из файла или аппаратного источника, должно иметь все сведения о формате данных и оборудовании устройства.</span><span class="sxs-lookup"><span data-stu-id="8731d-107">Typically, an application that must obtain media data from a file or hardware source must know everything about the data format and the hardware device.</span></span> <span data-ttu-id="8731d-108">Приложение должно работать с подключением, передавать данные, выполнять все необходимые преобразования данных, а также обеспечивать визуализацию данных или хранение файлов.</span><span class="sxs-lookup"><span data-stu-id="8731d-108">The application must handle the connection, transfer of data, any necessary data conversion, and the actual data rendering or file storage.</span></span> <span data-ttu-id="8731d-109">Так как каждый формат и устройство немного отличаются, этот процесс часто является сложным и громоздким.</span><span class="sxs-lookup"><span data-stu-id="8731d-109">Because each format and device is slightly different, this process is often complex and cumbersome.</span></span> <span data-ttu-id="8731d-110">Потоковая передача мультимедиа, с другой стороны, автоматически согласовывает передачу и преобразование данных из источника в приложение.</span><span class="sxs-lookup"><span data-stu-id="8731d-110">Multimedia streaming, on the other hand, automatically negotiates the transfer and conversion of data from the source to the application.</span></span> <span data-ttu-id="8731d-111">Интерфейсы потоковой передачи предоставляют единообразный и предсказуемый метод доступа к данным и управления им, что позволяет приложению легко воспроизводить данные независимо от их исходного источника или формата.</span><span class="sxs-lookup"><span data-stu-id="8731d-111">The streaming interfaces provide a uniform and predictable method of data access and control, which makes it easy for an application to play back the data, regardless of its original source or format.</span></span>

<span data-ttu-id="8731d-112">В следующих шагах показано, как реализовать потоковую передачу, с аппаратного устройства в подготовленное к просмотру воспроизведение.</span><span class="sxs-lookup"><span data-stu-id="8731d-112">The following steps show how to implement streaming, from hardware device to rendered playback.</span></span>

1.  <span data-ttu-id="8731d-113">Источник данных видео, например DirectShow, предоставляет интерфейсы потоковой передачи.</span><span class="sxs-lookup"><span data-stu-id="8731d-113">A source of video data, such as DirectShow, exposes the streaming interfaces.</span></span>
2.  <span data-ttu-id="8731d-114">Для обработки преобразования формата данных разработчик приложения использует интерфейсы потоковой передачи мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="8731d-114">The application developer uses the multimedia streaming interfaces to handle data format conversion.</span></span>
3.  <span data-ttu-id="8731d-115">Разработчик приложения использует интерфейсы DirectDraw для визуализации результирующих данных.</span><span class="sxs-lookup"><span data-stu-id="8731d-115">The application developer uses the DirectDraw interfaces to render the resulting data.</span></span>

<span data-ttu-id="8731d-116">Спецификация потоков мультимедиа состоит из нескольких интерфейсов. Каждый интерфейс включает методы, управляющие определенным аспектом потоковой обработки или обработку определенного типа данных.</span><span class="sxs-lookup"><span data-stu-id="8731d-116">The specification for multimedia streams comprises several interfaces; each interface includes methods that control a certain aspect of the streaming process or handle a certain type of data.</span></span> <span data-ttu-id="8731d-117">Дополнительные сведения см. в разделе [список интерфейсов потоковой передачи мультимедиа](list-of-multimedia-streaming-interfaces.md) .</span><span class="sxs-lookup"><span data-stu-id="8731d-117">See [List of Multimedia Streaming Interfaces](list-of-multimedia-streaming-interfaces.md) for additional information.</span></span>

## <a name="related-topics"></a><span data-ttu-id="8731d-118">См. также</span><span class="sxs-lookup"><span data-stu-id="8731d-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8731d-119">Сведения об архитектуре потоковой передачи мультимедиа</span><span class="sxs-lookup"><span data-stu-id="8731d-119">About the Multimedia Streaming Architecture</span></span>](about-the-multimedia-streaming-architecture.md)
</dt> </dl>

 

 



