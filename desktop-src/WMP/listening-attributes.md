---
title: Атрибуты прослушивания
description: Атрибуты прослушивания
ms.assetid: 51b10507-5c2e-49ca-b560-6db6a1a7ee87
keywords:
- Обложки проигрывателя Windows Media, атрибуты прослушивания
- обложки, атрибуты прослушивания
- Справочник по обобложкам, атрибутам прослушивания
- атрибуты прослушивания
- атрибуты, прослушивание
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 349a549966f7fba5ea152f8f0bb002a92f6dfb8e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104532060"
---
# <a name="listening-attributes"></a><span data-ttu-id="42b4b-108">Атрибуты прослушивания</span><span class="sxs-lookup"><span data-stu-id="42b4b-108">Listening Attributes</span></span>

<span data-ttu-id="42b4b-109">Атрибут прослушивания используется для соединения одного атрибута с другим, чтобы его значение изменялось при каждом изменении значения другого атрибута.</span><span class="sxs-lookup"><span data-stu-id="42b4b-109">A listening attribute is used to connect one attribute to another so that its value changes every time the value of the other attribute changes.</span></span>

<span data-ttu-id="42b4b-110">Атрибут прослушивания **вмппроп:** является наиболее полезным.</span><span class="sxs-lookup"><span data-stu-id="42b4b-110">The listening attribute **wmpprop:** is the most useful.</span></span> <span data-ttu-id="42b4b-111">Если значение одного атрибута задано как **вмппроп:** для второго атрибута, первое значение будет автоматически обновлено, чтобы отразить второе значение при каждом изменении второго значения.</span><span class="sxs-lookup"><span data-stu-id="42b4b-111">If the value of one attribute is specified to be the **wmpprop:** of a second attribute, the first value will be automatically updated to reflect the second value each time the second value changes.</span></span>

<span data-ttu-id="42b4b-112">**Пример**.</span><span class="sxs-lookup"><span data-stu-id="42b4b-112">**Example:**</span></span>


```C++
<TEXT
  value="wmpprop:mySlider.value"
/>

```



<span data-ttu-id="42b4b-113">Таким образом, значение Мислидер, отображаемое положением ползунка, также может отображаться в виде числа в текстовом поле.</span><span class="sxs-lookup"><span data-stu-id="42b4b-113">In this way, the value of mySlider, shown by the position of the slider control, can also be shown as a number within a text box.</span></span>

<span data-ttu-id="42b4b-114">Два других атрибута прослушивания, **вмпенаблед:** и **вмпдисаблед:**, могут быть использованы, чтобы изменить атрибут **Enabled** элемента управления в зависимости от того, доступны ли его функциональные возможности в данный момент в проигрывателе.</span><span class="sxs-lookup"><span data-stu-id="42b4b-114">The two other listening attributes, **wmpenabled:** and **wmpdisabled:**, can be used to change the **enabled** attribute of a control depending on whether its functionality is currently available in the player.</span></span> <span data-ttu-id="42b4b-115">Эти атрибуты могут прослушивать только методы объекта **Controls** .</span><span class="sxs-lookup"><span data-stu-id="42b4b-115">These attributes can listen only to methods of the **Controls** object.</span></span>

<span data-ttu-id="42b4b-116">**Пример**.</span><span class="sxs-lookup"><span data-stu-id="42b4b-116">**Example:**</span></span>


```C++
<BUTTON 
  id="play" 
  enabled="wmpenabled:player.controls.play"
/>

```



## <a name="related-topics"></a><span data-ttu-id="42b4b-117">См. также</span><span class="sxs-lookup"><span data-stu-id="42b4b-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="42b4b-118">**Прочее**</span><span class="sxs-lookup"><span data-stu-id="42b4b-118">**Miscellaneous**</span></span>](miscellaneous.md)
</dt> </dl>

 

 




