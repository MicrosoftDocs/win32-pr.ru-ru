---
title: Свойство Image. Source
description: Представляет путь к каталогу образа.
ms.assetid: 174a518a-e9a3-4461-a9a3-d61b62d2b718
keywords:
- Свойство Image. Source ленты Windows
topic_type:
- apiref
api_name:
- Image.Source
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3ace2a907280a11c54452b54bfb6172539980e38
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103801900"
---
# <a name="imagesource-property"></a><span data-ttu-id="c7993-104">Свойство Image. Source</span><span class="sxs-lookup"><span data-stu-id="c7993-104">Image.Source property</span></span>

<span data-ttu-id="c7993-105">Представляет путь к каталогу образа.</span><span class="sxs-lookup"><span data-stu-id="c7993-105">Represents the directory path of an image.</span></span>

## <a name="usage"></a><span data-ttu-id="c7993-106">Использование</span><span class="sxs-lookup"><span data-stu-id="c7993-106">Usage</span></span>

``` syntax
<Image.Source/>
```

## <a name="attributes"></a><span data-ttu-id="c7993-107">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="c7993-107">Attributes</span></span>

<span data-ttu-id="c7993-108">Атрибуты отсутствуют.</span><span class="sxs-lookup"><span data-stu-id="c7993-108">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="c7993-109">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="c7993-109">Child elements</span></span>

<span data-ttu-id="c7993-110">Нет дочерних элементов.</span><span class="sxs-lookup"><span data-stu-id="c7993-110">There are no child elements.</span></span>

## <a name="parent-elements"></a><span data-ttu-id="c7993-111">Родительские элементы</span><span class="sxs-lookup"><span data-stu-id="c7993-111">Parent elements</span></span>



| <span data-ttu-id="c7993-112">Элемент</span><span class="sxs-lookup"><span data-stu-id="c7993-112">Element</span></span>                                                 |
|---------------------------------------------------------|
| [<span data-ttu-id="c7993-113">**Образ**</span><span class="sxs-lookup"><span data-stu-id="c7993-113">**Image**</span></span>](windowsribbon-element-image.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="c7993-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="c7993-114">Remarks</span></span>

<span data-ttu-id="c7993-115">Необязательный элемент.</span><span class="sxs-lookup"><span data-stu-id="c7993-115">Optional.</span></span>

<span data-ttu-id="c7993-116">Для каждого [**образа**](windowsribbon-element-image.md)может использоваться не более одного раза.</span><span class="sxs-lookup"><span data-stu-id="c7993-116">May occur at most once for each [**Image**](windowsribbon-element-image.md).</span></span>

<span data-ttu-id="c7993-117">Этот элемент содержит значение типа *xs: anyURI* или любую последовательность символов, представляющих универсальный код ресурса (URI).</span><span class="sxs-lookup"><span data-stu-id="c7993-117">This element contains a value of type *xs:anyURI* or any sequence of characters that represents a Uniform Resource Identifier (URI).</span></span> <span data-ttu-id="c7993-118">Значение URI является абсолютным или относительным (для файла разметки ленты) путем к каталогу ресурса изображения типа Bitmap (BMP).</span><span class="sxs-lookup"><span data-stu-id="c7993-118">The URI value is an absolute or relative (to the Ribbon markup file) directory path of an image resource of type bitmap (BMP).</span></span>

## <a name="examples"></a><span data-ttu-id="c7993-119">Примеры</span><span class="sxs-lookup"><span data-stu-id="c7993-119">Examples</span></span>

<span data-ttu-id="c7993-120">В следующем примере кода показана разметка, необходимая для объявления, с помощью набора элементов [**Image**](windowsribbon-element-image.md) — коллекция ресурсов изображений, предназначенных для поддержки четырех параметров dpi на экране.</span><span class="sxs-lookup"><span data-stu-id="c7993-120">The following code example shows the markup required to declare, through a set of [**Image**](windowsribbon-element-image.md) elements, a collection of image resources that are designed to support four specific screen dpi settings.</span></span> <span data-ttu-id="c7993-121">Свойство **Image. Source** используется для указания пути к ресурсу изображения.</span><span class="sxs-lookup"><span data-stu-id="c7993-121">The **Image.Source** property is used to specify the path to the image resource.</span></span>


```C++
<Command Name="cmdSizeAndColor" Symbol="IDR_CMD_SIZEANDCOLOR">
  <Command.LabelTitle>
    <String Id="250">Size and Color</String>
  </Command.LabelTitle>
  <Command.LargeImages>
    <Image Id="251" MinDPI="96">
      <Image.Source>res/sizeAndColor_96.bmp</Image.Source>
    </Image>
    <Image Id="252" MinDPI="120">
      <Image.Source>res/sizeAndColor_120.bmp</Image.Source>
    </Image>
    <Image Id="253" MinDPI="144">
      <Image.Source>res/sizeAndColor_144.bmp</Image.Source>
    </Image>
    <Image Id="254" MinDPI="192">
      <Image.Source>res/sizeAndColor_192.bmp</Image.Source>
    </Image>
  </Command.LargeImages>
</Command>
```



## <a name="requirements"></a><span data-ttu-id="c7993-122">Требования</span><span class="sxs-lookup"><span data-stu-id="c7993-122">Requirements</span></span>



| <span data-ttu-id="c7993-123">Требование</span><span class="sxs-lookup"><span data-stu-id="c7993-123">Requirement</span></span> | <span data-ttu-id="c7993-124">Значение</span><span class="sxs-lookup"><span data-stu-id="c7993-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="c7993-125">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="c7993-125">Minimum supported client</span></span><br/> | <span data-ttu-id="c7993-126">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="c7993-126">Windows 7 \[desktop apps only\]</span></span><br/>              |
| <span data-ttu-id="c7993-127">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="c7993-127">Minimum supported server</span></span><br/> | <span data-ttu-id="c7993-128">Только классические приложения Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="c7993-128">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/> |



 

 





