---
description: Воспроизведение звуковых потоков Караоке
ms.assetid: 1a8d0f42-35b8-4743-9ae7-619b99936f76
title: Воспроизведение звуковых потоков Караоке
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 907bfa3e359915cf537de75cdc739630fe607d97
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "105673052"
---
# <a name="playing-karaoke-audio-streams"></a><span data-ttu-id="cfcf6-103">Воспроизведение звуковых потоков Караоке</span><span class="sxs-lookup"><span data-stu-id="cfcf6-103">Playing Karaoke Audio Streams</span></span>

<span data-ttu-id="cfcf6-104">Навигатор DVD может играть DVD-Video диски с аудио-потоками Караоке, но для воспроизведения караоке также требуется декодер, поддерживающий многоканальный микширование караоке.</span><span class="sxs-lookup"><span data-stu-id="cfcf6-104">The DVD Navigator can play DVD-Video discs with karaoke audio streams, but karaoke playback also requires a decoder that supports multichannel karaoke mixing.</span></span> <span data-ttu-id="cfcf6-105">В частности, декодер должен поддерживать [**набор свойств Караоке на DVD-диске**](dvd-karaoke-property-set.md) ( \_ свойство AM \_ двдкараоке).</span><span class="sxs-lookup"><span data-stu-id="cfcf6-105">Specifically, the decoder must support the [**DVD Karaoke Property Set**](dvd-karaoke-property-set.md) (AM\_PROPERTY\_DVDKARAOKE).</span></span>

<span data-ttu-id="cfcf6-106">Диски караоке — это тип DVD-Video диска с одинаковой структурой навигации.</span><span class="sxs-lookup"><span data-stu-id="cfcf6-106">Karaoke discs are a type of DVD-Video disc and have the same navigation structure.</span></span> <span data-ttu-id="cfcf6-107">Песни обычно форматируются в виде заголовков, а заголовки могут быть сгруппированы в наборы заголовков на основе исполнителя, музыкального стиля или других критериев.</span><span class="sxs-lookup"><span data-stu-id="cfcf6-107">Songs are generally formatted as titles, and titles can be grouped into title sets based on performer, musical style, or other criteria.</span></span> <span data-ttu-id="cfcf6-108">Основное различие между караоке и другими типами DVD-Videos является звуковым потоком.</span><span class="sxs-lookup"><span data-stu-id="cfcf6-108">The main difference between karaoke and other types of DVD-Videos is the audio stream.</span></span> <span data-ttu-id="cfcf6-109">Диски караоке содержат многоканальное аудио, обычно Dolby AC-3.</span><span class="sxs-lookup"><span data-stu-id="cfcf6-109">Karaoke discs all contain multichannel audio, usually Dolby AC-3.</span></span> <span data-ttu-id="cfcf6-110">Каналы 0 и 1 всегда содержат фоновую Instrumental музыку, а каналы с 2 по 5 могут содержать любое сочетание вокала, руководств мелодиес и звуковых эффектов.</span><span class="sxs-lookup"><span data-stu-id="cfcf6-110">Channels 0 and 1 always contain the background instrumental music, while channels 2 through 5 can each contain any combination of guide vocals, guide melodies, and sound effects.</span></span> <span data-ttu-id="cfcf6-111">Приложение Караоке может управлять громкостью и конечным докладчиком для каждого вспомогательного канала.</span><span class="sxs-lookup"><span data-stu-id="cfcf6-111">A karaoke application can control the volume and destination speaker for each auxiliary channel.</span></span>

<span data-ttu-id="cfcf6-112">Когда Навигатор DVD обнаруживает содержимое Караоке на диске и переходит в режим Караоке, он информирует декодер, который затем должен отключить верхние три канала (вспомогательные каналы), пока они не будут явно включены приложением.</span><span class="sxs-lookup"><span data-stu-id="cfcf6-112">When the DVD Navigator detects karaoke content on a disc and goes into karaoke mode, it informs the decoder, which then should mute the upper three channels (the auxiliary channels) until any or all of them are explicitly turned on by an application.</span></span> <span data-ttu-id="cfcf6-113">Основные задачи приложения караоке:</span><span class="sxs-lookup"><span data-stu-id="cfcf6-113">The basic tasks of a karaoke application are to:</span></span>

1.  <span data-ttu-id="cfcf6-114">Определите количество вспомогательных каналов и их содержимое с помощью методов [**IDvdInfo2**](/windows/desktop/api/Strmif/nn-strmif-idvdinfo2) .</span><span class="sxs-lookup"><span data-stu-id="cfcf6-114">Determine the number of auxiliary channels and their contents using [**IDvdInfo2**](/windows/desktop/api/Strmif/nn-strmif-idvdinfo2) methods.</span></span>
2.  <span data-ttu-id="cfcf6-115">Предоставьте пользовательский интерфейс, отображающий содержимое канала и позволяющий пользователям включать или отключать любой вспомогательный канал в любое время с помощью [**IDvdControl2:: селекткараокеаудиопресентатионмоде**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-selectkaraokeaudiopresentationmode).</span><span class="sxs-lookup"><span data-stu-id="cfcf6-115">Provide a user interface that displays the channel contents and enables users to turn any auxiliary channel on or off at any time, using [**IDvdControl2::SelectKaraokeAudioPresentationMode**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-selectkaraokeaudiopresentationmode).</span></span>

<span data-ttu-id="cfcf6-116">Эти шаги показаны в примере приложения DVD в Двдкоре. cpp в методе **жетаудиоаттрибутес** .</span><span class="sxs-lookup"><span data-stu-id="cfcf6-116">These steps are illustrated in the DVD Sample application in DVDCore.cpp in the **GetAudioAttributes** method.</span></span>

## <a name="related-topics"></a><span data-ttu-id="cfcf6-117">См. также</span><span class="sxs-lookup"><span data-stu-id="cfcf6-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="cfcf6-118">DVD-приложения</span><span class="sxs-lookup"><span data-stu-id="cfcf6-118">DVD Applications</span></span>](dvd-applications.md)
</dt> </dl>

 

 



