---
title: Глобальные атрибуты (пакет SDK для проигрывателя Windows Media)
description: Глобальные атрибуты
ms.assetid: 2ed09506-990e-4da2-89d6-6ff77dc43eb2
keywords:
- Обложки проигрывателя Windows Media, глобальные атрибуты
- обложки, глобальные атрибуты
- Справочник по обложкам, глобальным атрибутам
- Глобальные атрибуты
- атрибуты, глобальные
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 19c3f7a605b5c277b3207cefbbeaaa641f81f026
ms.sourcegitcommit: 40a1246849dba8ececf54c716b2794b99c96ad50
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/12/2019
ms.locfileid: "104412115"
---
# <a name="global-attributes"></a><span data-ttu-id="3eae4-108">Глобальные атрибуты</span><span class="sxs-lookup"><span data-stu-id="3eae4-108">Global Attributes</span></span>

<span data-ttu-id="3eae4-109">Глобальные атрибуты — это атрибуты, обеспечивающие простой доступ к определенным элементам или объектам проигрывателя из любого места внутри обложки.</span><span class="sxs-lookup"><span data-stu-id="3eae4-109">Global attributes are attributes that provide easy access to certain player elements or objects from anywhere within a skin.</span></span>

<span data-ttu-id="3eae4-110">Глобальный атрибут **Player** является ссылкой на объект [Player](player-object.md) и используется для доступа к основным функциям проигрывателя Windows Media.</span><span class="sxs-lookup"><span data-stu-id="3eae4-110">The **player** global attribute is a reference to the [Player](player-object.md) object, and is used to access the primary functionality of Windows Media Player.</span></span> <span data-ttu-id="3eae4-111">В следующем примере **проигрыватель** используется для начала воспроизведения цифрового мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="3eae4-111">The following example uses **player** to begin digital media playback.</span></span>


```C++
<BUTTON
  onclick="jscript:player.controls.play();"
/>

```



<span data-ttu-id="3eae4-112">Глобальный атрибут **темы** является ссылкой на элемент [Theme](theme-element.md) .</span><span class="sxs-lookup"><span data-stu-id="3eae4-112">The **theme** global attribute is a reference to the [THEME](theme-element.md) element.</span></span> <span data-ttu-id="3eae4-113">Это правильный способ доступа к атрибутам **темы** , а не указания идентификатора в элементе **Theme** .</span><span class="sxs-lookup"><span data-stu-id="3eae4-113">This is the proper way to access **THEME** attributes, rather than by specifying an ID within the **THEME** element.</span></span> <span data-ttu-id="3eae4-114">В следующем примере для открытия нового представления используется **Тема** .</span><span class="sxs-lookup"><span data-stu-id="3eae4-114">The following example uses **theme** to open a new view.</span></span>


```C++
<TEXT 
  value="open" 
  onclick="jscript:theme.openView('newView');"
/>

```



<span data-ttu-id="3eae4-115">Глобальный атрибут **View** является ссылкой на текущее [представление](view-element.md).</span><span class="sxs-lookup"><span data-stu-id="3eae4-115">The **view** global attribute is a reference to the current [VIEW](view-element.md).</span></span> <span data-ttu-id="3eae4-116">Его можно использовать вместо идентификатора, указанного в различных элементах **представления** .</span><span class="sxs-lookup"><span data-stu-id="3eae4-116">This can be used instead of the ID specified within the various **VIEW** elements.</span></span> <span data-ttu-id="3eae4-117">В следующем примере **представление** используется для закрытия текущего представления.</span><span class="sxs-lookup"><span data-stu-id="3eae4-117">The following example uses **view** to close the current view.</span></span>


```C++
<BUTTON 
  id="quitbutton"
  onclick="jscript:view.close();"
/>

```



<span data-ttu-id="3eae4-118">Глобальный атрибут **event** используется для доступа к атрибутам внешних событий из обработчиков событий.</span><span class="sxs-lookup"><span data-stu-id="3eae4-118">The **event** global attribute is used to access ambient event attributes from within event handlers.</span></span> <span data-ttu-id="3eae4-119">В следующем примере **событие** используется для определения того, нажата ли клавиша ALT при нажатии на кнопку.</span><span class="sxs-lookup"><span data-stu-id="3eae4-119">The following example uses **event** to determine whether the ALT key is pressed when a button is clicked.</span></span>


```C++
<BUTTON
  onclick="jscript:if (event.altKey == true) myText.value='ALT';"
/>

```



<span data-ttu-id="3eae4-120">Глобальный атрибут **плайераппликатион** является ссылкой на объект [плайераппликатион](playerapplication-object.md) и используется файлами обложки, предоставляемыми в качестве настраиваемых пользовательских интерфейсов для удаленных элементов управления проигрывателем.</span><span class="sxs-lookup"><span data-stu-id="3eae4-120">The **playerApplication** global attribute is a reference to the [PlayerApplication](playerapplication-object.md) object, and is used by skin files provided as custom user interfaces for remoted Player controls.</span></span> <span data-ttu-id="3eae4-121">Элемент управления Player можно внедрять в удаленном режиме только в программах на C++, которые реализуют интерфейс **ивмпремотемедиасервицес** .</span><span class="sxs-lookup"><span data-stu-id="3eae4-121">The Player control can be embedded in remote mode only in C++ programs that implement the **IWMPRemoteMediaServices** interface.</span></span> <span data-ttu-id="3eae4-122">В следующем примере **плайераппликатион** используется для переключения в полный режим проигрывателя.</span><span class="sxs-lookup"><span data-stu-id="3eae4-122">The following example uses **playerApplication** to switch to the full mode of the Player.</span></span>


```C++
<BUTTON
  onclick="jscript:playerApplication.switchToPlayerApplication();"
/>

```



<span data-ttu-id="3eae4-123">Дополнительные сведения см. в разделе [атрибуты внешних событий](ambient-event-attributes.md).</span><span class="sxs-lookup"><span data-stu-id="3eae4-123">For more information, see [Ambient Event Attributes](ambient-event-attributes.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="3eae4-124">См. также</span><span class="sxs-lookup"><span data-stu-id="3eae4-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3eae4-125">**Прочее**</span><span class="sxs-lookup"><span data-stu-id="3eae4-125">**Miscellaneous**</span></span>](miscellaneous.md)
</dt> </dl>

 

 




