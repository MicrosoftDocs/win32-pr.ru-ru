---
description: Примеры свойств MPEG
ms.assetid: 339aab84-e5ad-4071-8b67-2b04cb17e450
title: Примеры свойств MPEG
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8c20df4b9285a77d00bd98bc6f21558f0d6b3c60
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "105682267"
---
# <a name="mpeg-sample-properties"></a><span data-ttu-id="e3ccf-103">Примеры свойств MPEG</span><span class="sxs-lookup"><span data-stu-id="e3ccf-103">MPEG Sample Properties</span></span>

<span data-ttu-id="e3ccf-104">Примеры MPEG имеют следующие характеристики.</span><span class="sxs-lookup"><span data-stu-id="e3ccf-104">MPEG samples have the following characteristics.</span></span>

<span data-ttu-id="e3ccf-105">**Метки времени**</span><span class="sxs-lookup"><span data-stu-id="e3ccf-105">**Time Stamps**</span></span>

<span data-ttu-id="e3ccf-106">Не все примеры имеют время начала и окончания.</span><span class="sxs-lookup"><span data-stu-id="e3ccf-106">Not all samples have start and stop times.</span></span> <span data-ttu-id="e3ccf-107">Время окончания выборки для пакета и полезных данных не имеет смысла; Обычно для него задано время начала плюс один.</span><span class="sxs-lookup"><span data-stu-id="e3ccf-107">The sample stop time for packet and payload data is not useful; it is usually set to the start time plus one.</span></span> <span data-ttu-id="e3ccf-108">В примерах пакетов MPEG или полезных данных будет задано время запуска и окончания, если пакет системного уровня, из которого они создаются, имел допустимый PTS.</span><span class="sxs-lookup"><span data-stu-id="e3ccf-108">MPEG packet or payload data samples will have a start and stop time set if the system layer packet they are generated from had a valid PTS.</span></span>

<span data-ttu-id="e3ccf-109">Дополнительные сведения о метках времени см. в разделе 2.4.1 of ISO1-11172: "в заголовке пакета могут содержаться декодированные и (или) Метки времени презентации (DTS и PTS), которые ссылаются на первую единицу доступа в пакете."</span><span class="sxs-lookup"><span data-stu-id="e3ccf-109">For more information about time stamps, see section 2.4.1 of ISO1-11172: "The packet header may contain decoding and/or presentation time stamps (DTS and PTS) that refer to the first access unit in the packet."</span></span>

<span data-ttu-id="e3ccf-110">Для \_ основных типов потока MPEG время начала — это порядковый номер первого байта, который оценивается как 1 байт в секунду.</span><span class="sxs-lookup"><span data-stu-id="e3ccf-110">For MPEG\_Stream major types, the start time is the byte position of the first byte, rated at 1 byte per second.</span></span> <span data-ttu-id="e3ccf-111">Время окончания — это позиция байта последнего байта.</span><span class="sxs-lookup"><span data-stu-id="e3ccf-111">The stop time is the byte position of the last byte.</span></span> <span data-ttu-id="e3ccf-112">Следовательно, последовательные выборки должны иметь время окончания первого пакета, равное времени начала следующего пакета.</span><span class="sxs-lookup"><span data-stu-id="e3ccf-112">Thus, consecutive samples should have the stop time of the first packet equal to the start time of the next packet.</span></span> <span data-ttu-id="e3ccf-113">Для данных видеороликов источник носителя должен соответствовать формату файла компакт-диска, доступного в CDFS с стандартным блоком Metallica в начале.</span><span class="sxs-lookup"><span data-stu-id="e3ccf-113">For Video CD data, the origin of the medium must match the format of a video-CD file exposed by CDFS with the standard RIFF chunk at the start.</span></span>

<span data-ttu-id="e3ccf-114">Для видеофайлов и типов полезных данных MPEG метка времени — это время презентации для первого кадра видео, начало кода которого начинается в примере.</span><span class="sxs-lookup"><span data-stu-id="e3ccf-114">For MPEG video packet and payload types, the time stamp is the presentation time for the first video frame whose picture start code begins in the sample.</span></span>

<span data-ttu-id="e3ccf-115">Для типов звуковых пакетов и полезных данных MPEG метка времени — это время презентации для первого звукового кадра, код синхронизации которого начинается в примере.</span><span class="sxs-lookup"><span data-stu-id="e3ccf-115">For MPEG audio packet and payload types, the time stamp is the presentation time for the first audio frame whose sync code starts in the sample.</span></span>

<span data-ttu-id="e3ccf-116">Предполагается, что данные пакетов и полезных данных без меток времени могут быть успешно выполнены фильтрами обработки.</span><span class="sxs-lookup"><span data-stu-id="e3ccf-116">It is assumed that packet and payload data without time stamps can be successfully prerolled by the handling filters.</span></span>

<span data-ttu-id="e3ccf-117">**Нарушения**</span><span class="sxs-lookup"><span data-stu-id="e3ccf-117">**Discontinuities**</span></span>

<span data-ttu-id="e3ccf-118">Если в потоке есть разрыв (например, разрыв в данных в режиме реального времени или ошибка в данных или после поиска), свойство ненепрерывности задается на следующем примере носителя.</span><span class="sxs-lookup"><span data-stu-id="e3ccf-118">If there is a break in the stream (for example, a gap in the real-time data, or an error in the data or after a seek), the discontinuity property is set on the next media sample.</span></span> <span data-ttu-id="e3ccf-119">Это также позволяет отменять отметку времени.</span><span class="sxs-lookup"><span data-stu-id="e3ccf-119">This also allows for a time-stamp discontinuity.</span></span>

<span data-ttu-id="e3ccf-120">**Уведомления о завершении потока**</span><span class="sxs-lookup"><span data-stu-id="e3ccf-120">**End-of-Stream Notifications**</span></span>

<span data-ttu-id="e3ccf-121">Когда декодер получает это уведомление, он должен обработать все буферизованные данные.</span><span class="sxs-lookup"><span data-stu-id="e3ccf-121">When the decoder receives this notification, it must process any buffered data.</span></span> <span data-ttu-id="e3ccf-122">Все новые данные должны начинаться со свойства ненепрерывности.</span><span class="sxs-lookup"><span data-stu-id="e3ccf-122">Any new data must then start with the discontinuity property.</span></span>

## <a name="related-topics"></a><span data-ttu-id="e3ccf-123">См. также</span><span class="sxs-lookup"><span data-stu-id="e3ccf-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e3ccf-124">Поддержка MPEG-2 в DirectShow</span><span class="sxs-lookup"><span data-stu-id="e3ccf-124">MPEG-2 Support in DirectShow</span></span>](mpeg-2-support-in-directshow.md)
</dt> </dl>

 

 



