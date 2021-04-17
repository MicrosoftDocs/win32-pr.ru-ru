---
description: Портативные устройства Windows поддерживают следующие атрибуты ресурсов.
ms.assetid: 0cbf8777-5cea-4839-a4c3-366bb9e18488
title: Атрибуты ресурсов (Портабледевице. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Resource
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: 300add64d332dbc509bef6ec5bb2ad124f7a6b3e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105718102"
---
# <a name="resource-attributes"></a><span data-ttu-id="d0f27-103">Атрибуты ресурсов</span><span class="sxs-lookup"><span data-stu-id="d0f27-103">Resource Attributes</span></span>

<span data-ttu-id="d0f27-104">Портативные устройства Windows поддерживают следующие атрибуты ресурсов.</span><span class="sxs-lookup"><span data-stu-id="d0f27-104">Windows Portable Devices supports the following resource attributes.</span></span> <span data-ttu-id="d0f27-105">Эти атрибуты возвращаются следующими методами.</span><span class="sxs-lookup"><span data-stu-id="d0f27-105">These attributes are returned by the following methods:</span></span>

-   [<span data-ttu-id="d0f27-106">**Ипортабледевицересаурцес:: Жетресаурцеаттрибутес**</span><span class="sxs-lookup"><span data-stu-id="d0f27-106">**IPortableDeviceResources::GetResourceAttributes**</span></span>](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevicecapabilities-getfixedpropertyattributes)



| <span data-ttu-id="d0f27-107">attribute</span><span class="sxs-lookup"><span data-stu-id="d0f27-107">Attribute</span></span>                                                  | <span data-ttu-id="d0f27-108">VarType</span><span class="sxs-lookup"><span data-stu-id="d0f27-108">VarType</span></span>      | <span data-ttu-id="d0f27-109">Описание</span><span class="sxs-lookup"><span data-stu-id="d0f27-109">Description</span></span>                                                                                                                                 |
|------------------------------------------------------------|--------------|---------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d0f27-110">**\_атрибут ресурса \_ WPD \_ может быть \_ удален**</span><span class="sxs-lookup"><span data-stu-id="d0f27-110">**WPD\_RESOURCE\_ATTRIBUTE\_CAN\_DELETE**</span></span>                  | <span data-ttu-id="d0f27-111">**Логическое значение VT \_**</span><span class="sxs-lookup"><span data-stu-id="d0f27-111">**VT\_BOOL**</span></span> | <span data-ttu-id="d0f27-112">Логическое значение, указывающее, имеет ли клиент разрешение на удаление ресурса.</span><span class="sxs-lookup"><span data-stu-id="d0f27-112">A Boolean value that specifies whether a client has permission to delete the resource.</span></span> <span data-ttu-id="d0f27-113">Если он отсутствует, предполагается, что он имеет значение false.</span><span class="sxs-lookup"><span data-stu-id="d0f27-113">If absent, it is assumed to be false.</span></span>                |
| <span data-ttu-id="d0f27-114">**\_атрибут ресурса \_ WPD \_ может \_ читать**</span><span class="sxs-lookup"><span data-stu-id="d0f27-114">**WPD\_RESOURCE\_ATTRIBUTE\_CAN\_READ**</span></span>                    | <span data-ttu-id="d0f27-115">**Логическое значение VT \_**</span><span class="sxs-lookup"><span data-stu-id="d0f27-115">**VT\_BOOL**</span></span> | <span data-ttu-id="d0f27-116">Логическое значение, указывающее, имеет ли клиент разрешение на открытие ресурса для доступа на чтение.</span><span class="sxs-lookup"><span data-stu-id="d0f27-116">A Boolean value that specifies whether a client has permission to open the resource for Read access.</span></span> <span data-ttu-id="d0f27-117">Если он отсутствует, предполагается, что он имеет значение false.</span><span class="sxs-lookup"><span data-stu-id="d0f27-117">If absent, it is assumed to be False.</span></span>  |
| <span data-ttu-id="d0f27-118">**\_атрибут ресурса \_ WPD \_ может \_ записывать**</span><span class="sxs-lookup"><span data-stu-id="d0f27-118">**WPD\_RESOURCE\_ATTRIBUTE\_CAN\_WRITE**</span></span>                   | <span data-ttu-id="d0f27-119">**Логическое значение VT \_**</span><span class="sxs-lookup"><span data-stu-id="d0f27-119">**VT\_BOOL**</span></span> | <span data-ttu-id="d0f27-120">Логическое значение, указывающее, имеет ли клиент разрешение на открытие ресурса для доступа на запись.</span><span class="sxs-lookup"><span data-stu-id="d0f27-120">A Boolean value that specifies whether a client has permission to open the resource for Write access.</span></span> <span data-ttu-id="d0f27-121">Если он отсутствует, предполагается, что он имеет значение false.</span><span class="sxs-lookup"><span data-stu-id="d0f27-121">If absent, it is assumed to be false.</span></span> |
| <span data-ttu-id="d0f27-122">**\_ \_ \_ Размер неоптимального \_ \_ буфера чтения \_ для атрибута ресурса WPD**</span><span class="sxs-lookup"><span data-stu-id="d0f27-122">**WPD\_RESOURCE\_ATTRIBUTE\_OPTIMAL\_READ\_BUFFER\_SIZE**</span></span>  | <span data-ttu-id="d0f27-123">**VT \_ UI4**</span><span class="sxs-lookup"><span data-stu-id="d0f27-123">**VT\_UI4**</span></span>  | <span data-ttu-id="d0f27-124">Рекомендуемый размер буфера, который вызывающий объект должен использовать для буферизованного чтения из ресурса.</span><span class="sxs-lookup"><span data-stu-id="d0f27-124">The recommended buffer size that a caller should use for buffered reads from the resource.</span></span>                                                  |
| <span data-ttu-id="d0f27-125">**\_атрибут ресурса WPD — \_ \_ оптимальный \_ \_ Размер буфера записи \_**</span><span class="sxs-lookup"><span data-stu-id="d0f27-125">**WPD\_RESOURCE\_ATTRIBUTE\_OPTIMAL\_WRITE\_BUFFER\_SIZE**</span></span> | <span data-ttu-id="d0f27-126">**VT \_ UI4**</span><span class="sxs-lookup"><span data-stu-id="d0f27-126">**VT\_UI4**</span></span>  | <span data-ttu-id="d0f27-127">Рекомендуемый размер буфера, который вызывающий объект должен использовать для буферизованной записи ресурса.</span><span class="sxs-lookup"><span data-stu-id="d0f27-127">The recommended buffer size that a caller should use for buffered writes on the resource.</span></span>                                                   |
| <span data-ttu-id="d0f27-128">**\_ \_ \_ Общий \_ Размер атрибута ресурса WPD**</span><span class="sxs-lookup"><span data-stu-id="d0f27-128">**WPD\_RESOURCE\_ATTRIBUTE\_TOTAL\_SIZE**</span></span>                  | <span data-ttu-id="d0f27-129">**VT \_ UI8**</span><span class="sxs-lookup"><span data-stu-id="d0f27-129">**VT\_UI8**</span></span>  | <span data-ttu-id="d0f27-130">Общий размер данных ресурса в байтах.</span><span class="sxs-lookup"><span data-stu-id="d0f27-130">The total size of the resource data, in bytes.</span></span>                                                                                              |



 

## <a name="requirements"></a><span data-ttu-id="d0f27-131">Требования</span><span class="sxs-lookup"><span data-stu-id="d0f27-131">Requirements</span></span>



| <span data-ttu-id="d0f27-132">Требование</span><span class="sxs-lookup"><span data-stu-id="d0f27-132">Requirement</span></span> | <span data-ttu-id="d0f27-133">Значение</span><span class="sxs-lookup"><span data-stu-id="d0f27-133">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="d0f27-134">Header</span><span class="sxs-lookup"><span data-stu-id="d0f27-134">Header</span></span><br/> | <dl> <span data-ttu-id="d0f27-135"><dt>Портабледевице. h</dt></span><span class="sxs-lookup"><span data-stu-id="d0f27-135"><dt>PortableDevice.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d0f27-136">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="d0f27-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d0f27-137">**Свойства**</span><span class="sxs-lookup"><span data-stu-id="d0f27-137">**Properties**</span></span>](properties-and-attributes.md)
</dt> </dl>

 

 




