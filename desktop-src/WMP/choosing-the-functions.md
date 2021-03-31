---
title: Выбор функций
description: Выбор функций
ms.assetid: ded3c578-5087-4e4f-bf21-2149cf72719d
keywords:
- Обложки мобильных устройств проигрывателя Windows Media, функции для аудио
- обложки, функции для аудио
- Создание обложек, функций для аудио
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a139dc21a7d10847a7920955988ec2b02fced0f3
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104411303"
---
# <a name="choosing-the-functions"></a><span data-ttu-id="fd6aa-106">Выбор функций</span><span class="sxs-lookup"><span data-stu-id="fd6aa-106">Choosing the Functions</span></span>

<span data-ttu-id="fd6aa-107">Цель этой обложки — предоставить базовую функциональность для воспроизведения звука.</span><span class="sxs-lookup"><span data-stu-id="fd6aa-107">The purpose of this skin is to provide basic functionality for playing audio.</span></span> <span data-ttu-id="fd6aa-108">Будут использованы следующие функции:</span><span class="sxs-lookup"><span data-stu-id="fd6aa-108">The following functions will be used:</span></span>



| <span data-ttu-id="fd6aa-109">Функция</span><span class="sxs-lookup"><span data-stu-id="fd6aa-109">Function</span></span>                     | <span data-ttu-id="fd6aa-110">Описание</span><span class="sxs-lookup"><span data-stu-id="fd6aa-110">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                          |
|------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fd6aa-111">Плайпаусе или Плайпаусестоп\*</span><span class="sxs-lookup"><span data-stu-id="fd6aa-111">PlayPause or PlayPauseStop\*</span></span> | <span data-ttu-id="fd6aa-112">Запуск элемента мультимедиа имеет простую важность.</span><span class="sxs-lookup"><span data-stu-id="fd6aa-112">Starting the media item is of prime importance.</span></span> <span data-ttu-id="fd6aa-113">При создании обложки для проигрывателя Windows Media 10 Mobile или более поздней версии следует использовать Плайпаусестоп.</span><span class="sxs-lookup"><span data-stu-id="fd6aa-113">If you are creating a skin for Windows Media Player 10 Mobile or later, then you should use PlayPauseStop.</span></span> <span data-ttu-id="fd6aa-114">При работе с более ранней версией проигрывателя Windows Media Mobile необходимо использовать Плайпаусе.</span><span class="sxs-lookup"><span data-stu-id="fd6aa-114">If you are working with an earlier version of Windows Media Player Mobile, then you must use PlayPause.</span></span> <span data-ttu-id="fd6aa-115">Обе функции предоставляют дополнительные функциональные возможности приостановки, но только Плайпаусестоп позволяет остановить вещание в реальном времени, когда функция приостановки недоступна.</span><span class="sxs-lookup"><span data-stu-id="fd6aa-115">Both functions give you the added functionality of pausing, but only PlayPauseStop allows you to stop a live broadcast when pause functionality is not available.</span></span> |
| <span data-ttu-id="fd6aa-116">Stop</span><span class="sxs-lookup"><span data-stu-id="fd6aa-116">Stop</span></span>                         | <span data-ttu-id="fd6aa-117">Чтобы закончить воспроизведение элемента, необходимо добавить параметр "останавливаться".</span><span class="sxs-lookup"><span data-stu-id="fd6aa-117">You will want to add Stop to stop playing the item.</span></span> <span data-ttu-id="fd6aa-118">Если вы создаете обложку для проигрывателя Windows Media 10 Mobile или более поздней версии, функция Плайпаусестоп уже предоставляет эту функцию.</span><span class="sxs-lookup"><span data-stu-id="fd6aa-118">If you are creating a skin for Windows Media Player 10 Mobile or later, the PlayPauseStop function already provides this functionality.</span></span>                                                                                                                                                                                                                                          |
| <span data-ttu-id="fd6aa-119">Следующая</span><span class="sxs-lookup"><span data-stu-id="fd6aa-119">Next</span></span>                         | <span data-ttu-id="fd6aa-120">Если у вас есть список воспроизведения, вы сможете выбрать следующий элемент.</span><span class="sxs-lookup"><span data-stu-id="fd6aa-120">If you have a playlist, you will want to be able to choose the next item.</span></span> <span data-ttu-id="fd6aa-121">Это необходимо для простой навигации по цифровым носителям.</span><span class="sxs-lookup"><span data-stu-id="fd6aa-121">You need this for basic navigation of digital media.</span></span>                                                                                                                                                                                                                                                                                                       |
| <span data-ttu-id="fd6aa-122">Предыдущий</span><span class="sxs-lookup"><span data-stu-id="fd6aa-122">Prev</span></span>                         | <span data-ttu-id="fd6aa-123">Хотя вы можете использовать Next для прохода по списку воспроизведения, пока вы не поступаете к началу, добавление в начале, что позволит пользователю перейти назад и вперед при навигации по списку воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="fd6aa-123">While you could use Next to cycle through the playlist until you came to the beginning, adding Prev will make it easy for the user to go backward as well as forward when navigating the playlist.</span></span>                                                                                                                                                                                                                                   |
| <span data-ttu-id="fd6aa-124">Волумеуп или Волумедовн\*</span><span class="sxs-lookup"><span data-stu-id="fd6aa-124">VolumeUp or VolumeDown\*</span></span>     | <span data-ttu-id="fd6aa-125">Вам потребуется предоставить пользователю возможность включения или уменьшения объема тома.</span><span class="sxs-lookup"><span data-stu-id="fd6aa-125">You will want to provide the user with the ability to turn the volume up or down.</span></span>                                                                                                                                                                                                                                                                                                                                                    |



 

<span data-ttu-id="fd6aa-126">\*Доступно для проигрывателя Windows Media 10 Mobile или более поздней версии.</span><span class="sxs-lookup"><span data-stu-id="fd6aa-126">\*Available for Windows Media Player 10 Mobile or later.</span></span>

## <a name="related-topics"></a><span data-ttu-id="fd6aa-127">См. также</span><span class="sxs-lookup"><span data-stu-id="fd6aa-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fd6aa-128">**Путеводитель по обложкам**</span><span class="sxs-lookup"><span data-stu-id="fd6aa-128">**Skin Guide**</span></span>](skin-guide.md)
</dt> </dl>

 

 




