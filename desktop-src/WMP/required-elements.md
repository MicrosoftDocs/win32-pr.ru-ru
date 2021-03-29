---
title: Обязательные элементы
description: Обязательные элементы
ms.assetid: 6aabbdcc-f834-4908-b25a-1dfce038132a
keywords:
- Обложки мобильных устройств проигрывателя Windows Media, элементы
- обложки, элементы
- файлы определения обложки, элементы
- элементы, файлы определения обложки
- элементы, проигрыватель Windows Media Mobile
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9e1f05ba51b83fad6585d24c3ad19830598b8975
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103776412"
---
# <a name="required-elements"></a><span data-ttu-id="f4005-108">Обязательные элементы</span><span class="sxs-lookup"><span data-stu-id="f4005-108">Required Elements</span></span>

<span data-ttu-id="f4005-109">В файле определения обложки необходимо указать следующие элементы:</span><span class="sxs-lookup"><span data-stu-id="f4005-109">You must provide the following elements in your skin definition file:</span></span>

-   <span data-ttu-id="f4005-110">**Заголовок.**</span><span class="sxs-lookup"><span data-stu-id="f4005-110">**Header.**</span></span> <span data-ttu-id="f4005-111">Требуется основной заголовок файла определения обложки.</span><span class="sxs-lookup"><span data-stu-id="f4005-111">The main skin definition file header is required.</span></span> <span data-ttu-id="f4005-112">Сведения о версии заголовка см. в таблице в разделе [Создание файла определения обложки](creating-a-skin-definition-file.md) .</span><span class="sxs-lookup"><span data-stu-id="f4005-112">For header version information, see the table in the [Creating a Skin Definition File](creating-a-skin-definition-file.md) section.</span></span>
-   <span data-ttu-id="f4005-113">**Раздел описания.**</span><span class="sxs-lookup"><span data-stu-id="f4005-113">**Description section.**</span></span> <span data-ttu-id="f4005-114">Раздел Description (описание) необходим при создании обложек для Windows Media 9 Series для Windows Mobile.</span><span class="sxs-lookup"><span data-stu-id="f4005-114">The Description section is required when creating skins for Windows Media Player 9 Series for Windows Mobile.</span></span> <span data-ttu-id="f4005-115">Он должен быть первым разделом в файле определения обложки и должен указывать допустимые значения для измерений.</span><span class="sxs-lookup"><span data-stu-id="f4005-115">It must be the first section in the skin definition file, and it must specify valid values for Dimensions.</span></span> <span data-ttu-id="f4005-116">Указывать значение параметра Orientation необязательно.</span><span class="sxs-lookup"><span data-stu-id="f4005-116">Specifying a value for Orientation is optional.</span></span>
-   <span data-ttu-id="f4005-117">**Раздел точечных рисунков.**</span><span class="sxs-lookup"><span data-stu-id="f4005-117">**Bitmaps section.**</span></span> <span data-ttu-id="f4005-118">Необходимо указать раздел точечных рисунков.</span><span class="sxs-lookup"><span data-stu-id="f4005-118">The Bitmaps section is required.</span></span> <span data-ttu-id="f4005-119">Кроме того, раздел растровых изображений должен указывать допустимые имена для фоновых, отключенных, отправленных, регионов и файлов Super Image.</span><span class="sxs-lookup"><span data-stu-id="f4005-119">Additionally, the Bitmaps section must specify valid names for Background, Disabled, Pushed, Region, and Super image files.</span></span>
-   <span data-ttu-id="f4005-120">**файлы изображений.**</span><span class="sxs-lookup"><span data-stu-id="f4005-120">**Image files.**</span></span> <span data-ttu-id="f4005-121">В рамках обложки необходимо предоставить фоновые, отключенные, отправленные, регионы и файлы суперпользователя.</span><span class="sxs-lookup"><span data-stu-id="f4005-121">You must provide Background, Disabled, Pushed, Region, and Super image files as part of your skin.</span></span> <span data-ttu-id="f4005-122">Если вы создаете обложки для проигрывателя Windows Media 10 Mobile или более поздней версии, вам не нужно включать файлы регионов или Super Image.</span><span class="sxs-lookup"><span data-stu-id="f4005-122">If you are creating skins for Windows Media Player 10 Mobile or later, you do not need to include Region or Super image files.</span></span>

<span data-ttu-id="f4005-123">При создании обложки только с определенными изображениями Обложка будет видима, но не будет предоставлять пользователю никаких осмысленных функциональных возможностей.</span><span class="sxs-lookup"><span data-stu-id="f4005-123">If you create a skin with only images defined, the skin will be visible, but will not offer any meaningful functionality to the user.</span></span> <span data-ttu-id="f4005-124">Если вы решили создать обложку без кнопок, возможно, чтобы предотвратить пропуску определенного содержимого пользователем, имейте в виду, что для аппаратных кнопок на устройстве все равно может быть возможно соответствие функциональных возможностей.</span><span class="sxs-lookup"><span data-stu-id="f4005-124">If you decide to create a skin without buttons, perhaps to prevent the user from skipping over certain content, be aware that it may still be possible to map functionality to the hardware buttons on the device.</span></span>

<span data-ttu-id="f4005-125">Файлы Thumb являются обязательными, и линейки не могут использоваться без бегунка.</span><span class="sxs-lookup"><span data-stu-id="f4005-125">Thumb files are required and your trackbars cannot be used without thumbs.</span></span>

## <a name="related-topics"></a><span data-ttu-id="f4005-126">См. также</span><span class="sxs-lookup"><span data-stu-id="f4005-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f4005-127">**Файл определения обложки**</span><span class="sxs-lookup"><span data-stu-id="f4005-127">**Skin Definition File**</span></span>](skin-definition-file-mobile.md)
</dt> </dl>

 

 




