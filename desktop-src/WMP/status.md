---
title: Состояние (пакет SDK для проигрывателя Windows Media)
description: Состояние
ms.assetid: b8d6d026-819c-4889-a894-c82fe81ec922
keywords:
- Обложки мобильных устройств проигрывателя Windows Media, отображение состояния
- обложки, отображение состояния
- Справочник по обложкам, отображению состояния
- Отображение состояния в обложках, о
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6f6f1cd9e0df209d6a37ed880765fd607e939765
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/10/2020
ms.locfileid: "104070945"
---
# <a name="status-windows-media-player-sdk"></a><span data-ttu-id="51247-107">Состояние (пакет SDK для проигрывателя Windows Media)</span><span class="sxs-lookup"><span data-stu-id="51247-107">Status (Windows Media Player SDK)</span></span>

<span data-ttu-id="51247-108">Вы можете использовать отображение состояния в обложке.</span><span class="sxs-lookup"><span data-stu-id="51247-108">You may want to use a status display in your skin.</span></span> <span data-ttu-id="51247-109">Если это так, элемент Status должен быть определен в файле определения обложки.</span><span class="sxs-lookup"><span data-stu-id="51247-109">If so, the status element must be defined in the skin definition file.</span></span> <span data-ttu-id="51247-110">В качестве альтернативы можно также отобразить эти сведения с помощью атрибута Status в элементе text.</span><span class="sxs-lookup"><span data-stu-id="51247-110">As an alternative, you may also display this information by using the Status attribute in the Text element.</span></span>

<span data-ttu-id="51247-111">Раздел Status файла определения обложки начинается со следующей строки:</span><span class="sxs-lookup"><span data-stu-id="51247-111">The Status section of the skin definition file begins with this line:</span></span>


```C++
[ Status ]

```



<span data-ttu-id="51247-112">Затем необходимо добавить одну или несколько строк, содержащих сведения о состоянии, отображаемых в обложке.</span><span class="sxs-lookup"><span data-stu-id="51247-112">You then must add one or more lines that contain information about the status display in your skin.</span></span>


```C++
    On           45,193,120,13    Left    Tahoma,8,B        0,255,  0

```



<span data-ttu-id="51247-113">Для раздела Status в файле определения обложки можно использовать следующий шаблон:</span><span class="sxs-lookup"><span data-stu-id="51247-113">You can use the following template for the Status section of your skin definition file:</span></span>


```C++
//  <Item>       <Location>     <Align>  <Font>          <Color>
//  ------       ----------     -------  ------          -------

```



<span data-ttu-id="51247-114">Необходимо использовать порядок, показанный в предыдущем шаблоне, для отображения сведений о состоянии для каждой строки в разделе состояние.</span><span class="sxs-lookup"><span data-stu-id="51247-114">You must use the order shown in the preceding template for status display information for each line in the Status section.</span></span> <span data-ttu-id="51247-115">Каждая часть строки является обязательной.</span><span class="sxs-lookup"><span data-stu-id="51247-115">Each part of the line is required.</span></span> <span data-ttu-id="51247-116">В следующих разделах описываются все элементы.</span><span class="sxs-lookup"><span data-stu-id="51247-116">The following sections describe each item:</span></span>

-   [<span data-ttu-id="51247-117">Элемент состояния</span><span class="sxs-lookup"><span data-stu-id="51247-117">Status Item</span></span>](status-item.md)
-   [<span data-ttu-id="51247-118">Расположение состояния</span><span class="sxs-lookup"><span data-stu-id="51247-118">Status Location</span></span>](status-location.md)
-   [<span data-ttu-id="51247-119">Выравнивание состояния</span><span class="sxs-lookup"><span data-stu-id="51247-119">Status Alignment</span></span>](status-alignment.md)
-   [<span data-ttu-id="51247-120">Шрифт состояния</span><span class="sxs-lookup"><span data-stu-id="51247-120">Status Font</span></span>](status-font.md)
-   [<span data-ttu-id="51247-121">Цвет состояния</span><span class="sxs-lookup"><span data-stu-id="51247-121">Status Color</span></span>](status-color.md)

<span data-ttu-id="51247-122">Пример кода состояния см. в [разделе Sample Status](sample-status-section.md).</span><span class="sxs-lookup"><span data-stu-id="51247-122">For an example of Status code, see [Sample Status Section](sample-status-section.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="51247-123">См. также</span><span class="sxs-lookup"><span data-stu-id="51247-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="51247-124">**Справочник по обложкам**</span><span class="sxs-lookup"><span data-stu-id="51247-124">**Skin Reference**</span></span>](skin-reference.md)
</dt> </dl>

 

 




