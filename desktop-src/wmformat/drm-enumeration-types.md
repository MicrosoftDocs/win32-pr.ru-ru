---
title: Типы перечислений клиента DRM Microsoft Windows Media
description: Типы перечисления
ms.assetid: 940f66e1-1dc1-414f-bba9-b91f4f0dfc45
keywords:
- Windows Media Format SDK, типы перечислений
- Управление цифровыми правами (DRM), типы перечислений
- DRM (Управление цифровыми правами), типы перечислений
- Расширенные API клиента DRM, типы перечислений
- Расширенные API клиента, типы перечислений
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c159342367035767d213d57987d93d23eb321a6c
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/10/2020
ms.locfileid: "104070985"
---
# <a name="microsoft-windows-media-drm-client-enumeration-types"></a><span data-ttu-id="ae71c-108">Типы перечислений клиента DRM Microsoft Windows Media</span><span class="sxs-lookup"><span data-stu-id="ae71c-108">Microsoft Windows Media DRM Client Enumeration Types</span></span>

<span data-ttu-id="ae71c-109">В следующей таблице описаны перечисления, поддерживаемые расширенными API-интерфейсами клиента DRM Microsoft Windows Media.</span><span class="sxs-lookup"><span data-stu-id="ae71c-109">The following table describes the enumerations that are supported by the Microsoft Windows Media DRM Client Extended APIs.</span></span>



| <span data-ttu-id="ae71c-110">Перечисление</span><span class="sxs-lookup"><span data-stu-id="ae71c-110">Enumeration</span></span>                                                                      | <span data-ttu-id="ae71c-111">Описание</span><span class="sxs-lookup"><span data-stu-id="ae71c-111">Description</span></span>                                                                                                                                                   |
|----------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="ae71c-112">**действие DRM. \_ \_ разрешенные \_ \_ результаты запроса**</span><span class="sxs-lookup"><span data-stu-id="ae71c-112">**DRM\_ACTION\_ALLOWED\_QUERY\_RESULTS**</span></span>](drm-action-allowed-query-results.md) | <span data-ttu-id="ae71c-113">Используется интерфейсом [**ивмдрмлиценсекуери:: куеряктионалловед**](iwmdrmlicensequery-queryactionallowed.md) для указания причины, по которой действие не разрешено.</span><span class="sxs-lookup"><span data-stu-id="ae71c-113">Used by the [**IWMDRMLicenseQuery::QueryActionAllowed**](iwmdrmlicensequery-queryactionallowed.md) interface to specify the reason an action is not allowed.</span></span> |
| [<span data-ttu-id="ae71c-114">**\_тип данных attr с атрибутом DRM \_**</span><span class="sxs-lookup"><span data-stu-id="ae71c-114">**DRM\_ATTR\_DATATYPE**</span></span>](drm-attr-datatype.md)                                 | <span data-ttu-id="ae71c-115">Определяет типы данных, используемые для атрибутов и свойств DRM.</span><span class="sxs-lookup"><span data-stu-id="ae71c-115">Defines the data types used for DRM attributes and properties.</span></span>                                                                                                |
| [<span data-ttu-id="ae71c-116">**\_тип шифрования \_ DRM**</span><span class="sxs-lookup"><span data-stu-id="ae71c-116">**DRM\_CRYPTO\_TYPE**</span></span>](drm-crypto-type.md)                                     | <span data-ttu-id="ae71c-117">Определяет типы алгоритмов шифрования, которые могут использоваться для шифрования содержимого.</span><span class="sxs-lookup"><span data-stu-id="ae71c-117">Defines the cryptographic algorithm types that can be used to encrypt content.</span></span>                                                                                |
| [<span data-ttu-id="ae71c-118">**\_состояние HTTP \_ DRM**</span><span class="sxs-lookup"><span data-stu-id="ae71c-118">**DRM\_HTTP\_STATUS**</span></span>](drmdrm-http-status.md)                                  | <span data-ttu-id="ae71c-119">Определяет диапазон состояний HTTP для запроса DRM.</span><span class="sxs-lookup"><span data-stu-id="ae71c-119">Defines a range of HTTP states for a DRM request.</span></span>                                                                                                             |
| [<span data-ttu-id="ae71c-120">**\_состояние ИНДИВИДУАЛИЗАЦИИ DRM \_**</span><span class="sxs-lookup"><span data-stu-id="ae71c-120">**DRM\_INDIVIDUALIZATION\_STATUS**</span></span>](drmdrm-individualization-status.md)        | <span data-ttu-id="ae71c-121">Определяет допустимые состояния для индивидуальной защиты DRM.</span><span class="sxs-lookup"><span data-stu-id="ae71c-121">Defines the valid states for DRM individualization.</span></span>                                                                                                           |
| [<span data-ttu-id="ae71c-122">**\_ \_ Категория состояния лицензии \_ DRM**</span><span class="sxs-lookup"><span data-stu-id="ae71c-122">**DRM\_LICENSE\_STATE\_CATEGORY**</span></span>](drmdrm-license-state-category.md)           | <span data-ttu-id="ae71c-123">Указывает тип ограничения лицензии, описываемого структурой [**\_ \_ \_ данных состояния лицензии DRM**](drmdrm-license-state-data.md) .</span><span class="sxs-lookup"><span data-stu-id="ae71c-123">Specifies the type of license restriction that is described by a [**DRM\_LICENSE\_STATE\_DATA**](drmdrm-license-state-data.md) structure.</span></span>                    |
| [<span data-ttu-id="ae71c-124">**\_состояние Msdrm**</span><span class="sxs-lookup"><span data-stu-id="ae71c-124">**MSDRM\_STATUS**</span></span>](msdrm-status.md)                                            | <span data-ttu-id="ae71c-125">Определяет условия состояния для подсистемы DRM.</span><span class="sxs-lookup"><span data-stu-id="ae71c-125">Defines status conditions for the DRM subsystem.</span></span>                                                                                                              |
| [<span data-ttu-id="ae71c-126">**\_тип политики \_ вмдрмнет**</span><span class="sxs-lookup"><span data-stu-id="ae71c-126">**WMDRMNET\_POLICY\_TYPE**</span></span>](wmdrmnet-policy-type.md)                           | <span data-ttu-id="ae71c-127">Список типов политик, доступных для операций с сетевыми устройствами Windows Media DRM.</span><span class="sxs-lookup"><span data-stu-id="ae71c-127">Lists the types of policies that are available for Windows Media DRM for Network Devices operations.</span></span>                                                          |
| [<span data-ttu-id="ae71c-128">**\_права ВМТ**</span><span class="sxs-lookup"><span data-stu-id="ae71c-128">**WMT\_RIGHTS**</span></span>](drm-wmt-rights.md)                                            | <span data-ttu-id="ae71c-129">Определяет права, которые могут быть указаны в лицензии DRM.</span><span class="sxs-lookup"><span data-stu-id="ae71c-129">Defines the rights that may be specified in a DRM license.</span></span>                                                                                                    |



 

## <a name="related-topics"></a><span data-ttu-id="ae71c-130">См. также</span><span class="sxs-lookup"><span data-stu-id="ae71c-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ae71c-131">**Справочник по программированию**</span><span class="sxs-lookup"><span data-stu-id="ae71c-131">**Programming Reference**</span></span>](drm-programming-reference.md)
</dt> </dl>

 

 




