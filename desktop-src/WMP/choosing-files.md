---
title: Выбор файлов
description: Выбор файлов
ms.assetid: dfa44a32-7d72-47f7-a872-33b823a34798
keywords:
- Создание обложек, выбор файлов
- Обложки проигрывателя Windows Media, выбор файлов
- обложки, выбор файлов
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0098a37635c52ba3e48fb77f07a5868ceb957239
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104258861"
---
# <a name="choosing-files"></a><span data-ttu-id="51ff8-106">Выбор файлов</span><span class="sxs-lookup"><span data-stu-id="51ff8-106">Choosing Files</span></span>

<span data-ttu-id="51ff8-107">Если вы хотите выбрать файл, можно использовать код, похожий на пример списка воспроизведения, но заменить следующие сведения в разделе ПЛАЙЕЛЕМЕНТ:</span><span class="sxs-lookup"><span data-stu-id="51ff8-107">If you want to choose a file, you can use code similar to the Playlist example, but substitute the following for the PLAYELEMENT section:</span></span>


```C++
<PLAYELEMENT
  mappingColor = "#00FF00"
  onClick = "JScript:player.URL=theme.openDialog('FILE_OPEN','FILES_ALL');"
  />

```



<span data-ttu-id="51ff8-108">Эта строка будет использовать метод **Опендиалог** **темы** для определения **URL-адреса** проигрывателя.</span><span class="sxs-lookup"><span data-stu-id="51ff8-108">This line will use the **openDialog** method of **THEME** to define a **URL** for the player.</span></span> <span data-ttu-id="51ff8-109">Его можно использовать для выбора файлов, отсутствующих в списках воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="51ff8-109">You can use this to choose files that are not in playlists.</span></span>

<span data-ttu-id="51ff8-110">Аналогичный пример рабочего **опендиалог** см. в разделе примера пакета SDK.</span><span class="sxs-lookup"><span data-stu-id="51ff8-110">You can see a similar working **openDialog** example in the sample section of the SDK.</span></span>

## <a name="related-topics"></a><span data-ttu-id="51ff8-111">См. также</span><span class="sxs-lookup"><span data-stu-id="51ff8-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="51ff8-112">**Руководством по созданию обложки**</span><span class="sxs-lookup"><span data-stu-id="51ff8-112">**Skin Creation Guide**</span></span>](skin-creation-guide.md)
</dt> </dl>

 

 




