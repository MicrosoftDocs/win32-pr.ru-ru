---
title: Player. Опенстате
description: Свойство Опенстате извлекает значение, указывающее состояние источника содержимого.
ms.assetid: d38eadad-d0f0-40a9-92c6-1c745a0d4f1b
keywords:
- Проигрыватель проигрывателя Windows Media Player. Опенстате
topic_type:
- apiref
api_name:
- Player.openState
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b87ad682a0c9ea6420ec291cbe66a7f81c9062e4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105704120"
---
# <a name="playeropenstate"></a><span data-ttu-id="91798-104">Player. Опенстате</span><span class="sxs-lookup"><span data-stu-id="91798-104">Player.openState</span></span>

<span data-ttu-id="91798-105">Свойство **опенстате** извлекает значение, указывающее состояние источника содержимого.</span><span class="sxs-lookup"><span data-stu-id="91798-105">The **openState** property retrieves a value indicating the state of the content source.</span></span>

## <a name="syntax"></a><span data-ttu-id="91798-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="91798-106">Syntax</span></span>

<span data-ttu-id="91798-107">*проигрыватель* . **опенстате**</span><span class="sxs-lookup"><span data-stu-id="91798-107">*player* .**openState**</span></span>

## <a name="possible-values"></a><span data-ttu-id="91798-108">Возможные значения</span><span class="sxs-lookup"><span data-stu-id="91798-108">Possible Values</span></span>

<span data-ttu-id="91798-109">Это **значение доступно только для** чтения (**Long**).</span><span class="sxs-lookup"><span data-stu-id="91798-109">This property is a read only **Number** (**long**).</span></span> <span data-ttu-id="91798-110">Константу перечисления в стиле C можно получить с помощью префикса "вмпос" в качестве значения состояния.</span><span class="sxs-lookup"><span data-stu-id="91798-110">The C-style enumeration constant can be derived by prefixing the state value with "wmpos".</span></span> <span data-ttu-id="91798-111">Например, константа для состояния Плайлистопенинг — **вмпосплайлистопенинг**.</span><span class="sxs-lookup"><span data-stu-id="91798-111">For example, the constant for the PlaylistOpening state is **wmposPlaylistOpening**.</span></span>



| <span data-ttu-id="91798-112">Значение</span><span class="sxs-lookup"><span data-stu-id="91798-112">Value</span></span> | <span data-ttu-id="91798-113">Состояние</span><span class="sxs-lookup"><span data-stu-id="91798-113">State</span></span>                   | <span data-ttu-id="91798-114">Описание</span><span class="sxs-lookup"><span data-stu-id="91798-114">Description</span></span>                                                                                                                                            |
|-------|-------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="91798-115">0</span><span class="sxs-lookup"><span data-stu-id="91798-115">0</span></span>     | <span data-ttu-id="91798-116">Не определено.</span><span class="sxs-lookup"><span data-stu-id="91798-116">Undefined</span></span>               | <span data-ttu-id="91798-117">Проигрыватель Windows Media находится в неопределенном состоянии.</span><span class="sxs-lookup"><span data-stu-id="91798-117">Windows Media Player is in an undefined state.</span></span>                                                                                                         |
| <span data-ttu-id="91798-118">1</span><span class="sxs-lookup"><span data-stu-id="91798-118">1</span></span>     | <span data-ttu-id="91798-119">плайлистчангинг</span><span class="sxs-lookup"><span data-stu-id="91798-119">PlaylistChanging</span></span>        | <span data-ttu-id="91798-120">Будет загружен новый список воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="91798-120">New playlist is about to be loaded.</span></span>                                                                                                                    |
| <span data-ttu-id="91798-121">2</span><span class="sxs-lookup"><span data-stu-id="91798-121">2</span></span>     | <span data-ttu-id="91798-122">плайлистлокатинг</span><span class="sxs-lookup"><span data-stu-id="91798-122">PlaylistLocating</span></span>        | <span data-ttu-id="91798-123">Проигрыватель Windows Media пытается выполнить обнаружение списка воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="91798-123">Windows Media Player is attempting to locate the playlist.</span></span> <span data-ttu-id="91798-124">Список воспроизведения может быть локальным (библиотекой или метафайлом с расширением файла. ASX) или удаленным.</span><span class="sxs-lookup"><span data-stu-id="91798-124">The playlist can be local (library or metafile with an .asx file name extension) or remote.</span></span> |
| <span data-ttu-id="91798-125">3</span><span class="sxs-lookup"><span data-stu-id="91798-125">3</span></span>     | <span data-ttu-id="91798-126">плайлистконнектинг</span><span class="sxs-lookup"><span data-stu-id="91798-126">PlaylistConnecting</span></span>      | <span data-ttu-id="91798-127">Подключение к списку воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="91798-127">Connecting to the playlist.</span></span>                                                                                                                            |
| <span data-ttu-id="91798-128">4</span><span class="sxs-lookup"><span data-stu-id="91798-128">4</span></span>     | <span data-ttu-id="91798-129">плайлистлоадинг</span><span class="sxs-lookup"><span data-stu-id="91798-129">PlaylistLoading</span></span>         | <span data-ttu-id="91798-130">Список воспроизведения найден и теперь извлекается.</span><span class="sxs-lookup"><span data-stu-id="91798-130">Playlist has been found and is now being retrieved.</span></span>                                                                                                    |
| <span data-ttu-id="91798-131">5</span><span class="sxs-lookup"><span data-stu-id="91798-131">5</span></span>     | <span data-ttu-id="91798-132">плайлистопенинг</span><span class="sxs-lookup"><span data-stu-id="91798-132">PlaylistOpening</span></span>         | <span data-ttu-id="91798-133">Получен список воспроизведения, который теперь анализируется и загружается.</span><span class="sxs-lookup"><span data-stu-id="91798-133">Playlist has been retrieved and is now being parsed and loaded.</span></span>                                                                                        |
| <span data-ttu-id="91798-134">6</span><span class="sxs-lookup"><span data-stu-id="91798-134">6</span></span>     | <span data-ttu-id="91798-135">плайлистопенномедиа</span><span class="sxs-lookup"><span data-stu-id="91798-135">PlaylistOpenNoMedia</span></span>     | <span data-ttu-id="91798-136">Открыт список воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="91798-136">Playlist is open.</span></span>                                                                                                                                      |
| <span data-ttu-id="91798-137">7</span><span class="sxs-lookup"><span data-stu-id="91798-137">7</span></span>     | <span data-ttu-id="91798-138">плайлистчанжед</span><span class="sxs-lookup"><span data-stu-id="91798-138">PlaylistChanged</span></span>         | <span data-ttu-id="91798-139">В **куррентплайлист** был назначен новый список воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="91798-139">A new playlist has been assigned to **currentPlaylist**.</span></span>                                                                                               |
| <span data-ttu-id="91798-140">8</span><span class="sxs-lookup"><span data-stu-id="91798-140">8</span></span>     | <span data-ttu-id="91798-141">медиачангинг</span><span class="sxs-lookup"><span data-stu-id="91798-141">MediaChanging</span></span>           | <span data-ttu-id="91798-142">Будет загружен новый элемент мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="91798-142">A new media item is about to be loaded.</span></span>                                                                                                                |
| <span data-ttu-id="91798-143">9</span><span class="sxs-lookup"><span data-stu-id="91798-143">9</span></span>     | <span data-ttu-id="91798-144">медиалокатинг</span><span class="sxs-lookup"><span data-stu-id="91798-144">MediaLocating</span></span>           | <span data-ttu-id="91798-145">Проигрыватель Windows Media нахождение элемента мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="91798-145">Windows Media Player is locating the media item.</span></span> <span data-ttu-id="91798-146">Файл может быть локальным или удаленным.</span><span class="sxs-lookup"><span data-stu-id="91798-146">The file can be local or remote.</span></span>                                                                      |
| <span data-ttu-id="91798-147">10</span><span class="sxs-lookup"><span data-stu-id="91798-147">10</span></span>    | <span data-ttu-id="91798-148">медиаконнектинг</span><span class="sxs-lookup"><span data-stu-id="91798-148">MediaConnecting</span></span>         | <span data-ttu-id="91798-149">Подключение к серверу, на котором находится элемент мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="91798-149">Connecting to the server that holds the media item.</span></span>                                                                                                    |
| <span data-ttu-id="91798-150">11</span><span class="sxs-lookup"><span data-stu-id="91798-150">11</span></span>    | <span data-ttu-id="91798-151">медиалоадинг</span><span class="sxs-lookup"><span data-stu-id="91798-151">MediaLoading</span></span>            | <span data-ttu-id="91798-152">Элемент мультимедиа найден и теперь извлекается.</span><span class="sxs-lookup"><span data-stu-id="91798-152">Media item has been located and is now being retrieved.</span></span>                                                                                                |
| <span data-ttu-id="91798-153">12</span><span class="sxs-lookup"><span data-stu-id="91798-153">12</span></span>    | <span data-ttu-id="91798-154">медиаопенинг</span><span class="sxs-lookup"><span data-stu-id="91798-154">MediaOpening</span></span>            | <span data-ttu-id="91798-155">Элемент мультимедиа был извлечен и теперь открыт.</span><span class="sxs-lookup"><span data-stu-id="91798-155">Media item has been retrieved and is now being opened.</span></span>                                                                                                 |
| <span data-ttu-id="91798-156">13</span><span class="sxs-lookup"><span data-stu-id="91798-156">13</span></span>    | <span data-ttu-id="91798-157">медиаопен</span><span class="sxs-lookup"><span data-stu-id="91798-157">MediaOpen</span></span>               | <span data-ttu-id="91798-158">Теперь элемент мультимедиа открыт.</span><span class="sxs-lookup"><span data-stu-id="91798-158">Media item is now open.</span></span>                                                                                                                                |
| <span data-ttu-id="91798-159">14</span><span class="sxs-lookup"><span data-stu-id="91798-159">14</span></span>    | <span data-ttu-id="91798-160">бегинкодекаккуиситион</span><span class="sxs-lookup"><span data-stu-id="91798-160">BeginCodecAcquisition</span></span>   | <span data-ttu-id="91798-161">Начинается получение кодека.</span><span class="sxs-lookup"><span data-stu-id="91798-161">Starting codec acquisition.</span></span>                                                                                                                            |
| <span data-ttu-id="91798-162">15</span><span class="sxs-lookup"><span data-stu-id="91798-162">15</span></span>    | <span data-ttu-id="91798-163">ендкодекаккуиситион</span><span class="sxs-lookup"><span data-stu-id="91798-163">EndCodecAcquisition</span></span>     | <span data-ttu-id="91798-164">Получение кодека завершено.</span><span class="sxs-lookup"><span data-stu-id="91798-164">Codec acquisition is complete.</span></span>                                                                                                                         |
| <span data-ttu-id="91798-165">16</span><span class="sxs-lookup"><span data-stu-id="91798-165">16</span></span>    | <span data-ttu-id="91798-166">бегинлиценсеаккуиситион</span><span class="sxs-lookup"><span data-stu-id="91798-166">BeginLicenseAcquisition</span></span> | <span data-ttu-id="91798-167">Получение лицензии для воспроизведения содержимого, защищенного DRM.</span><span class="sxs-lookup"><span data-stu-id="91798-167">Acquiring a license to play DRM protected content.</span></span>                                                                                                     |
| <span data-ttu-id="91798-168">17</span><span class="sxs-lookup"><span data-stu-id="91798-168">17</span></span>    | <span data-ttu-id="91798-169">ендлиценсеаккуиситион</span><span class="sxs-lookup"><span data-stu-id="91798-169">EndLicenseAcquisition</span></span>   | <span data-ttu-id="91798-170">Получена лицензия на воспроизведение защищенного содержимого DRM.</span><span class="sxs-lookup"><span data-stu-id="91798-170">License to play DRM protected content has been acquired.</span></span>                                                                                               |
| <span data-ttu-id="91798-171">18</span><span class="sxs-lookup"><span data-stu-id="91798-171">18</span></span>    | <span data-ttu-id="91798-172">бегининдивидуализатион</span><span class="sxs-lookup"><span data-stu-id="91798-172">BeginIndividualization</span></span>  | <span data-ttu-id="91798-173">Начало индивидуализации DRM.</span><span class="sxs-lookup"><span data-stu-id="91798-173">Begin DRM Individualization.</span></span>                                                                                                                           |
| <span data-ttu-id="91798-174">19</span><span class="sxs-lookup"><span data-stu-id="91798-174">19</span></span>    | <span data-ttu-id="91798-175">ендиндивидуализатион</span><span class="sxs-lookup"><span data-stu-id="91798-175">EndIndividualization</span></span>    | <span data-ttu-id="91798-176">Индивидуальное управление DRM завершено.</span><span class="sxs-lookup"><span data-stu-id="91798-176">DRM individualization has been completed.</span></span>                                                                                                              |
| <span data-ttu-id="91798-177">20</span><span class="sxs-lookup"><span data-stu-id="91798-177">20</span></span>    | <span data-ttu-id="91798-178">медиаваитинг</span><span class="sxs-lookup"><span data-stu-id="91798-178">MediaWaiting</span></span>            | <span data-ttu-id="91798-179">Ожидание элемента мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="91798-179">Waiting for media item.</span></span>                                                                                                                                |
| <span data-ttu-id="91798-180">21</span><span class="sxs-lookup"><span data-stu-id="91798-180">21</span></span>    | <span data-ttu-id="91798-181">опенингункновнурл</span><span class="sxs-lookup"><span data-stu-id="91798-181">OpeningUnknownURL</span></span>       | <span data-ttu-id="91798-182">Открытие URL-адреса неизвестного типа.</span><span class="sxs-lookup"><span data-stu-id="91798-182">Opening a URL with an unknown type.</span></span>                                                                                                                    |



 

## <a name="remarks"></a><span data-ttu-id="91798-183">Комментарии</span><span class="sxs-lookup"><span data-stu-id="91798-183">Remarks</span></span>

<span data-ttu-id="91798-184">Состояния проигрывателя Windows Media не гарантированно выполняются в определенном порядке.</span><span class="sxs-lookup"><span data-stu-id="91798-184">Windows Media Player states are not guaranteed to occur in any particular order.</span></span> <span data-ttu-id="91798-185">Кроме того, не все состояния должны происходить во время последовательности событий.</span><span class="sxs-lookup"><span data-stu-id="91798-185">Furthermore, not every state necessarily occurs during a sequence of events.</span></span> <span data-ttu-id="91798-186">Не следует писать код, зависящий от порядка состояний.</span><span class="sxs-lookup"><span data-stu-id="91798-186">You should not write code that relies upon state order.</span></span>

## <a name="requirements"></a><span data-ttu-id="91798-187">Требования</span><span class="sxs-lookup"><span data-stu-id="91798-187">Requirements</span></span>



| <span data-ttu-id="91798-188">Требование</span><span class="sxs-lookup"><span data-stu-id="91798-188">Requirement</span></span> | <span data-ttu-id="91798-189">Значение</span><span class="sxs-lookup"><span data-stu-id="91798-189">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="91798-190">Версия</span><span class="sxs-lookup"><span data-stu-id="91798-190">Version</span></span><br/> | <span data-ttu-id="91798-191">Проигрыватель Windows Media версии 7,0 или более поздней.</span><span class="sxs-lookup"><span data-stu-id="91798-191">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="91798-192">DLL</span><span class="sxs-lookup"><span data-stu-id="91798-192">DLL</span></span><br/>     | <dl> <span data-ttu-id="91798-193"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="91798-193"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="91798-194">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="91798-194">See also</span></span>

<dl> <dt>

[<span data-ttu-id="91798-195">**Объект Player**</span><span class="sxs-lookup"><span data-stu-id="91798-195">**Player Object**</span></span>](player-object.md)
</dt> <dt>

[<span data-ttu-id="91798-196">**Событие Player. Опенстатечанже**</span><span class="sxs-lookup"><span data-stu-id="91798-196">**Player.OpenStateChange Event**</span></span>](player-player-openstatechange.md)
</dt> </dl>

 

 





