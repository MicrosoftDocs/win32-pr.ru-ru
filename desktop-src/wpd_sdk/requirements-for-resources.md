---
description: Требования к ресурсам
ms.assetid: 6b654cd6-7e9f-4e12-a687-4110e600ba7b
title: Требования к ресурсам
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5702555704137f4280e527f0fc26f176435238ad
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104265668"
---
# <a name="requirements-for-resources"></a><span data-ttu-id="e9924-103">Требования к ресурсам</span><span class="sxs-lookup"><span data-stu-id="e9924-103">Requirements for Resources</span></span>

<span data-ttu-id="e9924-104">Портативные устройства Windows определяют следующие категории ресурсов в качестве значений **PROPERTYKEY** .</span><span class="sxs-lookup"><span data-stu-id="e9924-104">Windows Portable Devices defines the following resource categories as **PROPERTYKEY** values.</span></span> <span data-ttu-id="e9924-105">Эти значения используются для описания отдельных ресурсов в объекте.</span><span class="sxs-lookup"><span data-stu-id="e9924-105">These values are used to describe individual resources in an object.</span></span> <span data-ttu-id="e9924-106">Элемент *PID* ключа свойства может отличаться для описания различных ресурсов одного типа для всех типов, за исключением **\_ ресурсов WPD \_ по умолчанию**, которые могут описывать только один ресурс.</span><span class="sxs-lookup"><span data-stu-id="e9924-106">The *pid* member of the property key can be different to describe different resources of the same type for all types except **WPD\_RESOURCE\_DEFAULT**, which can only describe one resource.</span></span> <span data-ttu-id="e9924-107">На странице «связанное описание» для каждого типа ресурсов перечислены атрибуты, поддерживаемые этим ресурсом.</span><span class="sxs-lookup"><span data-stu-id="e9924-107">The linked description page for each resource type lists the attributes supported by that resource.</span></span>



| <span data-ttu-id="e9924-108">PROPERTYKEY ресурсов</span><span class="sxs-lookup"><span data-stu-id="e9924-108">Resource PROPERTYKEY</span></span>                                                | <span data-ttu-id="e9924-109">Описание</span><span class="sxs-lookup"><span data-stu-id="e9924-109">Description</span></span>                                                                                                    |
|---------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="e9924-110">**\_ресурс \_ по умолчанию для WPD**</span><span class="sxs-lookup"><span data-stu-id="e9924-110">**WPD\_RESOURCE\_DEFAULT**</span></span>](wpd-resource-default.md)              | <span data-ttu-id="e9924-111">Задает весь файл за объектом.</span><span class="sxs-lookup"><span data-stu-id="e9924-111">Specifies the whole file behind the object.</span></span> <span data-ttu-id="e9924-112">Это единственный необходимый ресурс для любого объекта с ресурсом.</span><span class="sxs-lookup"><span data-stu-id="e9924-112">This is the only required resource for any object with a resource.</span></span> |
| [<span data-ttu-id="e9924-113">**\_ \_ Обложка ресурсов \_ WPD**</span><span class="sxs-lookup"><span data-stu-id="e9924-113">**WPD\_RESOURCE\_ALBUM\_ART**</span></span>](wpd-resource-album-art.md)         | <span data-ttu-id="e9924-114">Задает изображение, представляющее иллюстрацию альбома для объекта.</span><span class="sxs-lookup"><span data-stu-id="e9924-114">Specifies an image that represents the album artwork for the object.</span></span>                                           |
| [<span data-ttu-id="e9924-115">**\_ \_ звуковой ролик ресурса \_ WPD**</span><span class="sxs-lookup"><span data-stu-id="e9924-115">**WPD\_RESOURCE\_AUDIO\_CLIP**</span></span>](wpd-resource-audio-clip.md)       | <span data-ttu-id="e9924-116">Указывает аудиоклип для объекта.</span><span class="sxs-lookup"><span data-stu-id="e9924-116">Specifies an audio clip for the object.</span></span>                                                                        |
| [<span data-ttu-id="e9924-117">**\_фотография контакта по ресурсу WPD \_ \_**</span><span class="sxs-lookup"><span data-stu-id="e9924-117">**WPD\_RESOURCE\_CONTACT\_PHOTO**</span></span>](wpd-resource-contact-photo.md) | <span data-ttu-id="e9924-118">Задает изображение, представляющее фотографию лица, на которое ссылается объект Contact.</span><span class="sxs-lookup"><span data-stu-id="e9924-118">Specifies an image that represents a photo of the individual referred to in the contact object.</span></span>                |
| [<span data-ttu-id="e9924-119">**\_универсальный ресурс \_ WPD**</span><span class="sxs-lookup"><span data-stu-id="e9924-119">**WPD\_RESOURCE\_GENERIC**</span></span>](wpd-resource-generic.md)              | <span data-ttu-id="e9924-120">Универсальный ресурс неопределенного типа данных.</span><span class="sxs-lookup"><span data-stu-id="e9924-120">A generic resource of undefined data type.</span></span> <span data-ttu-id="e9924-121">Он должен рассматриваться как массив байтов.</span><span class="sxs-lookup"><span data-stu-id="e9924-121">This should be treated as a byte array.</span></span>                             |
| [<span data-ttu-id="e9924-122">**\_значок ресурса \_ WPD**</span><span class="sxs-lookup"><span data-stu-id="e9924-122">**WPD\_RESOURCE\_ICON**</span></span>](wpd-resource-icon.md)                    | <span data-ttu-id="e9924-123">Значок.</span><span class="sxs-lookup"><span data-stu-id="e9924-123">An icon.</span></span>                                                                                                       |
| [<span data-ttu-id="e9924-124">**\_эскиз ресурса \_ WPD**</span><span class="sxs-lookup"><span data-stu-id="e9924-124">**WPD\_RESOURCE\_THUMBNAIL**</span></span>](wpd-resource-thumbnail.md)          | <span data-ttu-id="e9924-125">Эскиз изображения.</span><span class="sxs-lookup"><span data-stu-id="e9924-125">A thumbnail image.</span></span>                                                                                             |



 

## <a name="related-topics"></a><span data-ttu-id="e9924-126">См. также</span><span class="sxs-lookup"><span data-stu-id="e9924-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e9924-127">**Справочник по программированию**</span><span class="sxs-lookup"><span data-stu-id="e9924-127">**Programming Reference**</span></span>](programming-reference.md)
</dt> </dl>

 

 



