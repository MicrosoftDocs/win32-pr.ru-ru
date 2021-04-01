---
title: WM/Picture
description: Атрибут WM/Picture содержит изображение, связанное с содержимым.
ms.assetid: ec82dfdf-7755-4758-9771-096aac114f78
keywords:
- Формат мультимедиа Windows WM/Picture
topic_type:
- apiref
api_name:
- WM/Picture
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 18ba3f74378112c8e3f58958db8b22c970e8e099
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/25/2019
ms.locfileid: "103986954"
---
# <a name="wmpicture"></a><span data-ttu-id="5a5f9-104">WM/Picture</span><span class="sxs-lookup"><span data-stu-id="5a5f9-104">WM/Picture</span></span>

<span data-ttu-id="5a5f9-105">Атрибут **WM/Picture** содержит изображение, связанное с содержимым.</span><span class="sxs-lookup"><span data-stu-id="5a5f9-105">The **WM/Picture** attribute contains a picture related to the content.</span></span>

## <a name="global-constant"></a><span data-ttu-id="5a5f9-106">Глобальная константа</span><span class="sxs-lookup"><span data-stu-id="5a5f9-106">Global Constant</span></span>

<span data-ttu-id="5a5f9-107">g \_ всзвмпиктуре</span><span class="sxs-lookup"><span data-stu-id="5a5f9-107">g\_wszWMPicture</span></span>

## <a name="data-type"></a><span data-ttu-id="5a5f9-108">Тип данных</span><span class="sxs-lookup"><span data-stu-id="5a5f9-108">Data Type</span></span>

<span data-ttu-id="5a5f9-109">[**WM \_ Рисунок**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_picture) (**\_ \_ двоичный тип ВМТ**)</span><span class="sxs-lookup"><span data-stu-id="5a5f9-109">[**WM\_PICTURE**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_picture) (**WMT\_TYPE\_BINARY**)</span></span>

## <a name="remarks"></a><span data-ttu-id="5a5f9-110">Комментарии</span><span class="sxs-lookup"><span data-stu-id="5a5f9-110">Remarks</span></span>

<span data-ttu-id="5a5f9-111">Этот атрибут совместим с кадром ID3, APIC.</span><span class="sxs-lookup"><span data-stu-id="5a5f9-111">This attribute is compatible with the ID3 frame, APIC.</span></span> <span data-ttu-id="5a5f9-112">Спецификация ID3 для кадра APIC подразумевает, что, хотя может существовать любое количество кадров APIC, связанных с файлом, только один из них может иметь тип 1, а только один может иметь тип 2.</span><span class="sxs-lookup"><span data-stu-id="5a5f9-112">The ID3 specification for the APIC frame stipulates that, while there may be any number of APIC frames associated with a file, only one may be of type 1 and only one may be of type 2.</span></span> <span data-ttu-id="5a5f9-113">В спецификации также указывается, что описание изображения не может содержать более 64 символов, но может быть пустым.</span><span class="sxs-lookup"><span data-stu-id="5a5f9-113">The specification also states that the description of the picture can be no longer than 64 characters, but can be empty.</span></span>

<span data-ttu-id="5a5f9-114">Атрибуты WM/Picture, добавленные с помощью объектов пакета SDK формата Windows Media, не проверяются автоматически в соответствии со спецификациями ID3.</span><span class="sxs-lookup"><span data-stu-id="5a5f9-114">WM/Picture attributes added with the objects of the Windows Media Format SDK are not automatically validated to conform to ID3 specifications.</span></span> <span data-ttu-id="5a5f9-115">Необходимо добавить код в приложение для выполнения проверок, если требуется обеспечить полную совместимость с ID3.</span><span class="sxs-lookup"><span data-stu-id="5a5f9-115">You must add code in your application to perform validations if you want to maintain complete compatibility with ID3.</span></span>

## <a name="see-also"></a><span data-ttu-id="5a5f9-116">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="5a5f9-116">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5a5f9-117">**Список атрибутов**</span><span class="sxs-lookup"><span data-stu-id="5a5f9-117">**Attribute List**</span></span>](attribute-list.md)
</dt> <dt>

[<span data-ttu-id="5a5f9-118">**\_изображение WM**</span><span class="sxs-lookup"><span data-stu-id="5a5f9-118">**WM\_PICTURE**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_picture)
</dt> </dl>

 

 




