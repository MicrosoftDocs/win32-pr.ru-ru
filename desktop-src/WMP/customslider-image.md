---
title: КУСТОМСЛИДЕР. Image
description: Атрибут Image указывает или получает имя файла, содержащего изображения, соответствующие различным состояниям настраиваемого ползунка.
ms.assetid: 7db4f924-76af-4451-831c-1ed8ab1315ee
keywords:
- Проигрыватель Windows Media КУСТОМСЛИДЕР. Image
topic_type:
- apiref
api_name:
- CUSTOMSLIDER.image
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f425ce138b2a11d2be834f39603ecc295c52c706
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105694378"
---
# <a name="customsliderimage"></a><span data-ttu-id="d315c-104">КУСТОМСЛИДЕР. Image</span><span class="sxs-lookup"><span data-stu-id="d315c-104">CUSTOMSLIDER.image</span></span>

<span data-ttu-id="d315c-105">Атрибут **Image** указывает или получает имя файла, содержащего изображения, соответствующие различным состояниям настраиваемого ползунка.</span><span class="sxs-lookup"><span data-stu-id="d315c-105">The **image** attribute specifies or retrieves the name of the file containing the images corresponding to the various states of the custom slider.</span></span>

``` syntax
        elementID.image
```

## <a name="possible-values"></a><span data-ttu-id="d315c-106">Возможные значения</span><span class="sxs-lookup"><span data-stu-id="d315c-106">Possible Values</span></span>

<span data-ttu-id="d315c-107">Этот атрибут является **строкой** для чтения и записи, содержащей имя файла изображения.</span><span class="sxs-lookup"><span data-stu-id="d315c-107">This attribute is a read/write **String** containing the name of an image file.</span></span>

## <a name="remarks"></a><span data-ttu-id="d315c-108">Комментарии</span><span class="sxs-lookup"><span data-stu-id="d315c-108">Remarks</span></span>

<span data-ttu-id="d315c-109">Атрибут **Image** является обязательным.</span><span class="sxs-lookup"><span data-stu-id="d315c-109">The **image** attribute is required.</span></span> <span data-ttu-id="d315c-110">Он задает файл изображения, состоящий из одного или нескольких подизображений, упорядоченных горизонтально или вертикально, представляющих различные состояния настраиваемого ползунка.</span><span class="sxs-lookup"><span data-stu-id="d315c-110">It specifies an image file that consists of one or more sub-images, arranged either horizontally or vertically, representing the various states of the custom slider.</span></span> <span data-ttu-id="d315c-111">Каждый подобраз должен иметь те же размеры, что и **поситионимаже** , или пользовательский ползунок будет работать неправильно.</span><span class="sxs-lookup"><span data-stu-id="d315c-111">Each sub-image must have the same dimensions as the **positionImage** or the custom slider will not work correctly.</span></span> <span data-ttu-id="d315c-112">Следовательно, высота или ширина общего изображения должна быть кратной высоте или ширине **поситионимаже**.</span><span class="sxs-lookup"><span data-stu-id="d315c-112">The height or width of the overall image must therefore be an even multiple of the height or width of the **positionImage**.</span></span>

<span data-ttu-id="d315c-113">Поддерживаются следующие типы файлов изображений: BMP, JPG, PNG и GIF (не включая анимированные GIF).</span><span class="sxs-lookup"><span data-stu-id="d315c-113">The supported image file types are BMP, JPG, PNG, and GIF (not including animated GIFs).</span></span>

## <a name="examples"></a><span data-ttu-id="d315c-114">Примеры</span><span class="sxs-lookup"><span data-stu-id="d315c-114">Examples</span></span>

<span data-ttu-id="d315c-115">Ниже приведен пример настраиваемого изображения ползунка.</span><span class="sxs-lookup"><span data-stu-id="d315c-115">The following is an example of a custom slider image.</span></span> <span data-ttu-id="d315c-116">Соответствующий **поситионимаже** показан в разделе "пример" свойства **поситионимаже** .</span><span class="sxs-lookup"><span data-stu-id="d315c-116">The corresponding **positionImage** is shown in the example section of the **positionImage** property.</span></span>

![Пример образа кустомслидер](images/dial.png)

<span data-ttu-id="d315c-118">Атрибут **поситионимаже** также содержит образец кода, иллюстрирующий использование атрибутов элемента **кустомслидер** .</span><span class="sxs-lookup"><span data-stu-id="d315c-118">The **positionImage** attribute also contains a code sample illustrating how the attributes of the **CUSTOMSLIDER** element are used.</span></span>

## <a name="requirements"></a><span data-ttu-id="d315c-119">Требования</span><span class="sxs-lookup"><span data-stu-id="d315c-119">Requirements</span></span>



| <span data-ttu-id="d315c-120">Требование</span><span class="sxs-lookup"><span data-stu-id="d315c-120">Requirement</span></span> | <span data-ttu-id="d315c-121">Значение</span><span class="sxs-lookup"><span data-stu-id="d315c-121">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="d315c-122">Версия</span><span class="sxs-lookup"><span data-stu-id="d315c-122">Version</span></span><br/> | <span data-ttu-id="d315c-123">Проигрыватель Windows Media версии 7,0 или более поздней</span><span class="sxs-lookup"><span data-stu-id="d315c-123">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="d315c-124">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="d315c-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d315c-125">**КУСТОМСЛИДЕР, элемент**</span><span class="sxs-lookup"><span data-stu-id="d315c-125">**CUSTOMSLIDER Element**</span></span>](customslider-element.md)
</dt> <dt>

[<span data-ttu-id="d315c-126">**КУСТОМСЛИДЕР. Поситионимаже**</span><span class="sxs-lookup"><span data-stu-id="d315c-126">**CUSTOMSLIDER.positionImage**</span></span>](customslider-positionimage.md)
</dt> </dl>

 

 





