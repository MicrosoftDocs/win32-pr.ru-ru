---
title: Добавление списка воспроизведения
description: Добавление списка воспроизведения
ms.assetid: be0c2cac-245d-4435-87d9-4f17076e005a
keywords:
- Создание обложек, списков воспроизведения
- Обложки проигрывателя Windows Media, списки воспроизведения
- обложки, списки воспроизведения
- списки воспроизведения, обложки
- списки воспроизведения метафайлов, обложки
- Списки воспроизведения метафайлов Windows Media, обложки
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c42a4bc253d4b1a3ba9b8fe0f31ca16b0d522956
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "105691310"
---
# <a name="adding-a-playlist"></a><span data-ttu-id="712f6-109">Добавление списка воспроизведения</span><span class="sxs-lookup"><span data-stu-id="712f6-109">Adding a Playlist</span></span>

<span data-ttu-id="712f6-110">Списки воспроизведения можно использовать для выбора из коллекций аудио и видео.</span><span class="sxs-lookup"><span data-stu-id="712f6-110">You can use playlists to choose from collections of your audio and video.</span></span>

<span data-ttu-id="712f6-111">Используя иллюстрацию из первой обложки, можно внести несколько изменений в файл определения обложки.</span><span class="sxs-lookup"><span data-stu-id="712f6-111">Using the artwork from your first skin, you can make a few changes to the skin definition file.</span></span>

<span data-ttu-id="712f6-112">Первым шагом является использование оболочки, которая будет использоваться для большинства обложек:</span><span class="sxs-lookup"><span data-stu-id="712f6-112">The first step is to use the shell you will use for most skins:</span></span>


```C++
<THEME>
    <VIEW
        clippingColor = "#CCCC00"
        backgroundImage = "background.bmp"
        titleBar = "false">

        <BUTTONGROUP
            mappingImage = "map.bmp"
            hoverImage = "hover.bmp"> 
                
    </VIEW>


</THEME>

```



<span data-ttu-id="712f6-113">Теперь добавьте второе **представление**, содержащее список воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="712f6-113">Now add a second **VIEW**, which contains a playlist.</span></span> <span data-ttu-id="712f6-114">Поместите следующий код после </VIEW> кода оболочки.</span><span class="sxs-lookup"><span data-stu-id="712f6-114">Place the following code after the </VIEW> of the shell code.</span></span>


```C++
     <VIEW 
          id = "playview">
          <PLAYLIST/>
     </VIEW>

```



<span data-ttu-id="712f6-115">Необходимо присвоить второму просмотру идентификатор, чтобы вы могли обращаться к нему позже.</span><span class="sxs-lookup"><span data-stu-id="712f6-115">You will need to give this second view an ID so you can refer to it later.</span></span> <span data-ttu-id="712f6-116">Добавьте ПЛАЙЕЛЕМЕНТ и СТОПЕЛЕМЕНТ.</span><span class="sxs-lookup"><span data-stu-id="712f6-116">Add a PLAYELEMENT and a STOPELEMENT.</span></span> <span data-ttu-id="712f6-117">Эти стандартные кнопки упрощают жизнь.</span><span class="sxs-lookup"><span data-stu-id="712f6-117">These predefined buttons make life easier.</span></span>


```C++
        <PLAYELEMENT
            mappingColor = "#00FF00" />
                          
        <STOPELEMENT
            mappingColor = "#FF0000" />

```



<span data-ttu-id="712f6-118">Наконец, добавьте событие OnClick в ПЛАЙЕЛЕМЕНТ для отображения списка воспроизведения во втором представлении:</span><span class="sxs-lookup"><span data-stu-id="712f6-118">Finally, add an onClick event to the PLAYELEMENT to display a playlist in the second view:</span></span>


```C++
            onClick = "JScript: theme.openView('playview');" />

```



<span data-ttu-id="712f6-119">Аналогичные обложки рабочего списка можно просмотреть в разделе с примерами пакета SDK.</span><span class="sxs-lookup"><span data-stu-id="712f6-119">You can see a similar working playlist skin in the sample section of the SDK.</span></span>

## <a name="related-topics"></a><span data-ttu-id="712f6-120">См. также</span><span class="sxs-lookup"><span data-stu-id="712f6-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="712f6-121">**Руководством по созданию обложки**</span><span class="sxs-lookup"><span data-stu-id="712f6-121">**Skin Creation Guide**</span></span>](skin-creation-guide.md)
</dt> </dl>

 

 




