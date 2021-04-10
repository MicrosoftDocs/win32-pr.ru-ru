---
description: Указывает тип комнаты для потока цифрового аудио Dolby. Это свойство применяется к кодировщикам цифрового аудио Dolby.
ms.assetid: d19b6b9d-9606-48a8-ac8e-cdbf15588a8f
title: Свойство Авенкддпродуктионрумтипе (Кодекапи. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2dc2eed0bb491fc982a5102507e5b55bf610880a
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "104140451"
---
# <a name="avencddproductionroomtype-property"></a><span data-ttu-id="d38b2-104">Авенкддпродуктионрумтипе, свойство</span><span class="sxs-lookup"><span data-stu-id="d38b2-104">AVEncDDProductionRoomType property</span></span>

<span data-ttu-id="d38b2-105">Указывает тип комнаты для потока цифрового аудио Dolby.</span><span class="sxs-lookup"><span data-stu-id="d38b2-105">Specifies the room type for a Dolby Digital audio stream.</span></span> <span data-ttu-id="d38b2-106">Это свойство применяется к кодировщикам цифрового аудио Dolby.</span><span class="sxs-lookup"><span data-stu-id="d38b2-106">This property applies to Dolby Digital audio encoders.</span></span>

<span data-ttu-id="d38b2-107">Это свойство доступно для чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="d38b2-107">This property is read/write.</span></span>

## <a name="data-type"></a><span data-ttu-id="d38b2-108">Тип данных</span><span class="sxs-lookup"><span data-stu-id="d38b2-108">Data type</span></span>

<span data-ttu-id="d38b2-109">**UINT32** (**VT \_ UI4**)</span><span class="sxs-lookup"><span data-stu-id="d38b2-109">**UINT32** (**VT\_UI4**)</span></span>

## <a name="property-guid"></a><span data-ttu-id="d38b2-110">GUID свойства</span><span class="sxs-lookup"><span data-stu-id="d38b2-110">Property GUID</span></span>

<span data-ttu-id="d38b2-111">**КОДЕКАПИ \_ авенкддпродуктионрумтипе**</span><span class="sxs-lookup"><span data-stu-id="d38b2-111">**CODECAPI\_AVEncDDProductionRoomType**</span></span>

## <a name="property-value"></a><span data-ttu-id="d38b2-112">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="d38b2-112">Property value</span></span>

<span data-ttu-id="d38b2-113">Значение этого свойства является членом перечисления [**еавенкддпродуктионрумтипе**](/windows/win32/api/codecapi/ne-codecapi-eavencddproductionroomtype) .</span><span class="sxs-lookup"><span data-stu-id="d38b2-113">The value of this property is a member of the [**eAVEncDDProductionRoomType**](/windows/win32/api/codecapi/ne-codecapi-eavencddproductionroomtype) enumeration.</span></span>

## <a name="remarks"></a><span data-ttu-id="d38b2-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="d38b2-114">Remarks</span></span>

<span data-ttu-id="d38b2-115">*Тип комнаты* относится к размеру комнаты, используемой в рабочей среде.</span><span class="sxs-lookup"><span data-stu-id="d38b2-115">*Room type* refers to the size of the room used during production.</span></span> <span data-ttu-id="d38b2-116">Если это свойство задано, задайте для свойства [**авенкддпродуктионинфоексистс**](avencddproductioninfoexists-property.md) значение **true**.</span><span class="sxs-lookup"><span data-stu-id="d38b2-116">If you set this property, set the [**AVEncDDProductionInfoExists**](avencddproductioninfoexists-property.md) property to **TRUE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="d38b2-117">Требования</span><span class="sxs-lookup"><span data-stu-id="d38b2-117">Requirements</span></span>



| <span data-ttu-id="d38b2-118">Требование</span><span class="sxs-lookup"><span data-stu-id="d38b2-118">Requirement</span></span> | <span data-ttu-id="d38b2-119">Значение</span><span class="sxs-lookup"><span data-stu-id="d38b2-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="d38b2-120">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="d38b2-120">Minimum supported client</span></span><br/> | <span data-ttu-id="d38b2-121">Приложения Windows 2000 Professional \[ классические приложения \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="d38b2-121">Windows 2000 Professional \[desktop apps \| UWP apps\]</span></span><br/>                     |
| <span data-ttu-id="d38b2-122">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="d38b2-122">Minimum supported server</span></span><br/> | <span data-ttu-id="d38b2-123">\[Приложения UWP для классических приложений Windows 2000 \|\]</span><span class="sxs-lookup"><span data-stu-id="d38b2-123">Windows 2000 Server \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="d38b2-124">Header</span><span class="sxs-lookup"><span data-stu-id="d38b2-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="d38b2-125"><dt>Кодекапи. h</dt></span><span class="sxs-lookup"><span data-stu-id="d38b2-125"><dt>Codecapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d38b2-126">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="d38b2-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d38b2-127">Свойства кодека API</span><span class="sxs-lookup"><span data-stu-id="d38b2-127">Codec API Properties</span></span>](codec-api-properties.md)
</dt> <dt>

[<span data-ttu-id="d38b2-128">**Интерфейс Икодекапи**</span><span class="sxs-lookup"><span data-stu-id="d38b2-128">**ICodecAPI Interface**</span></span>](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

