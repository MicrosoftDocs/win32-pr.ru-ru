---
description: Свойство Аудиостреамсаваилабле извлекает количество звуковых потоков, доступных в текущем заголовке.
ms.assetid: 4359ec30-920a-4b34-8e27-4cf1d9452aa8
title: Аудиостреамсаваилабле, свойство
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cb68020b30f4349fcbbb464150624d75250a0dbf
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "103894533"
---
# <a name="audiostreamsavailable-property"></a><span data-ttu-id="b535e-103">Аудиостреамсаваилабле, свойство</span><span class="sxs-lookup"><span data-stu-id="b535e-103">AudioStreamsAvailable Property</span></span>

> [!Note]  
> <span data-ttu-id="b535e-104">Этот компонент доступен для использования в операционных системах Microsoft Windows 2000, Windows XP и Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="b535e-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="b535e-105">В последующих версиях он может быть изменен или недоступен.</span><span class="sxs-lookup"><span data-stu-id="b535e-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="b535e-106">`AudioStreamsAvailable`Свойство получает количество звуковых потоков, доступных в текущем заголовке.</span><span class="sxs-lookup"><span data-stu-id="b535e-106">The `AudioStreamsAvailable` property retrieves the number of audio streams available in the current title.</span></span>

``` syntax
[ iStreams = ] MSWebDVD.AudioStreamsAvailable
```

## <a name="return-value"></a><span data-ttu-id="b535e-107">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="b535e-107">Return Value</span></span>

<span data-ttu-id="b535e-108">Возвращает целочисленное значение от 1 до 8, представляющее количество звуковых потоков, доступных в текущем заголовке.</span><span class="sxs-lookup"><span data-stu-id="b535e-108">Returns an integer value from 1 through 8 representing the number of audio streams available in the current title.</span></span>

## <a name="remarks"></a><span data-ttu-id="b535e-109">Комментарии</span><span class="sxs-lookup"><span data-stu-id="b535e-109">Remarks</span></span>

<span data-ttu-id="b535e-110">Это свойство доступно только для чтения и не имеет значения по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="b535e-110">This property is read-only with no default value.</span></span> <span data-ttu-id="b535e-111">Основным использованием нескольких звуковых потоков является предоставление звуковых дорожек фильмов более чем на одном языке.</span><span class="sxs-lookup"><span data-stu-id="b535e-111">The primary use of multiple audio streams is to provide movie soundtracks in more than one language.</span></span> <span data-ttu-id="b535e-112">Как правило, для каждого заголовка на диске включены все звуковые потоки.</span><span class="sxs-lookup"><span data-stu-id="b535e-112">Typically, not every title on a disc has all audio streams enabled.</span></span> <span data-ttu-id="b535e-113">Например, фильм может содержать звуковые дорожки на трех разных языках, но у трейлеров может быть только английская звуковая дорожка.</span><span class="sxs-lookup"><span data-stu-id="b535e-113">For example, the feature movie might have soundtracks in three different languages, but the trailers might have only an English soundtrack.</span></span> <span data-ttu-id="b535e-114">Прежде чем пользователь сможет выбрать поток, приложение должно определить, какие потоки доступны в текущем заголовке.</span><span class="sxs-lookup"><span data-stu-id="b535e-114">Before a user can select a stream, the application must determine which streams are available within the current title.</span></span> <span data-ttu-id="b535e-115">Обратите внимание, что определенные потоки идентифицируются индексом от нуля до 7.</span><span class="sxs-lookup"><span data-stu-id="b535e-115">Note that particular streams are identified by an index from zero through 7.</span></span>

<span data-ttu-id="b535e-116">Обычно диски представляют собой меню, в котором отображаются доступные звуковые дорожки, что позволяет пользователю выбрать аудиопоток для включения.</span><span class="sxs-lookup"><span data-stu-id="b535e-116">Discs generally present a menu showing the available soundtracks, enabling the user to select the audio stream to enable.</span></span>

## <a name="see-also"></a><span data-ttu-id="b535e-117">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="b535e-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b535e-118">**жетаудиолангуаже**</span><span class="sxs-lookup"><span data-stu-id="b535e-118">**GetAudioLanguage**</span></span>](getaudiolanguage-method.md)
</dt> </dl>

 

 



