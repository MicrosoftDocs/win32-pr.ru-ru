---
title: КУСТОМСЛИДЕР. Дисабледимаже
description: Атрибут Дисабледимаже указывает или получает изображение ползунка, используемого при отключенном ползунке.
ms.assetid: 91b1c2e3-6c92-4baa-b1f3-e44707157f4b
keywords:
- Проигрыватель Windows Media КУСТОМСЛИДЕР. Дисабледимаже
topic_type:
- apiref
api_name:
- CUSTOMSLIDER.disabledImage
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 169057d952170fb92c4e3a98617c7db22f5456b0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105698989"
---
# <a name="customsliderdisabledimage"></a><span data-ttu-id="16567-104">КУСТОМСЛИДЕР. Дисабледимаже</span><span class="sxs-lookup"><span data-stu-id="16567-104">CUSTOMSLIDER.disabledImage</span></span>

<span data-ttu-id="16567-105">Атрибут **дисабледимаже** указывает или получает изображение ползунка, используемого при отключенном ползунке.</span><span class="sxs-lookup"><span data-stu-id="16567-105">The **disabledImage** attribute specifies or retrieves the image of the slider used when the slider is disabled.</span></span>

``` syntax
        elementID.disabledImage
```

## <a name="possible-values"></a><span data-ttu-id="16567-106">Возможные значения</span><span class="sxs-lookup"><span data-stu-id="16567-106">Possible Values</span></span>

<span data-ttu-id="16567-107">Этот атрибут является **строкой** для чтения и записи, содержащей имя файла изображения.</span><span class="sxs-lookup"><span data-stu-id="16567-107">This attribute is a read/write **String** containing the name of an image file.</span></span>

## <a name="remarks"></a><span data-ttu-id="16567-108">Комментарии</span><span class="sxs-lookup"><span data-stu-id="16567-108">Remarks</span></span>

<span data-ttu-id="16567-109">Этот атрибут является необязательным.</span><span class="sxs-lookup"><span data-stu-id="16567-109">This attribute is optional.</span></span> <span data-ttu-id="16567-110">Если он не указан, будет использоваться файл, указанный в атрибуте **Image** .</span><span class="sxs-lookup"><span data-stu-id="16567-110">If it not specified, the file specified in the **image** attribute will be used.</span></span>

<span data-ttu-id="16567-111">**Дисабледимаже** представляет отключенное состояние элемента управления **кустомслидер** .</span><span class="sxs-lookup"><span data-stu-id="16567-111">The **disabledImage** represents the disabled state of the **CUSTOMSLIDER** control.</span></span> <span data-ttu-id="16567-112">Это может быть один образ или несколько изображений, представляющих различные состояния ползунка.</span><span class="sxs-lookup"><span data-stu-id="16567-112">It can be a single image or a series of images representing the various states of the slider.</span></span> <span data-ttu-id="16567-113">Если используется несколько образов, они упорядочиваются так же, как и файл **изображения** .</span><span class="sxs-lookup"><span data-stu-id="16567-113">If multiple images are used, they are arranged in the same way as the **image** file.</span></span>

<span data-ttu-id="16567-114">Поддерживаются следующие типы файлов изображений: BMP, JPG, PNG и GIF (не включая анимированные GIF).</span><span class="sxs-lookup"><span data-stu-id="16567-114">The supported image file types are BMP, JPG, PNG, and GIF (not including animated GIFs).</span></span>

## <a name="requirements"></a><span data-ttu-id="16567-115">Требования</span><span class="sxs-lookup"><span data-stu-id="16567-115">Requirements</span></span>



| <span data-ttu-id="16567-116">Требование</span><span class="sxs-lookup"><span data-stu-id="16567-116">Requirement</span></span> | <span data-ttu-id="16567-117">Значение</span><span class="sxs-lookup"><span data-stu-id="16567-117">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="16567-118">Версия</span><span class="sxs-lookup"><span data-stu-id="16567-118">Version</span></span><br/> | <span data-ttu-id="16567-119">Проигрыватель Windows Media версии 7,0 или более поздней</span><span class="sxs-lookup"><span data-stu-id="16567-119">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="16567-120">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="16567-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="16567-121">**КУСТОМСЛИДЕР, элемент**</span><span class="sxs-lookup"><span data-stu-id="16567-121">**CUSTOMSLIDER Element**</span></span>](customslider-element.md)
</dt> <dt>

[<span data-ttu-id="16567-122">**КУСТОМСЛИДЕР. Image**</span><span class="sxs-lookup"><span data-stu-id="16567-122">**CUSTOMSLIDER.image**</span></span>](customslider-image.md)
</dt> </dl>

 

 





