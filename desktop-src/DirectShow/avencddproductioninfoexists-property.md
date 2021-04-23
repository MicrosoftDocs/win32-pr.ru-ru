---
description: Указывает флаг сведений о звуковой рабочей информации в потоке цифрового звука Dolby. Это свойство применяется к кодировщикам цифрового аудио Dolby.
ms.assetid: 72f5f988-37c3-40d4-9c1c-07086e60ea51
title: Свойство Авенкддпродуктионинфоексистс (Кодекапи. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5069c8d30f0266b0727f735ede822be491c4a4a2
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "105682296"
---
# <a name="avencddproductioninfoexists-property"></a><span data-ttu-id="55eac-104">Авенкддпродуктионинфоексистс, свойство</span><span class="sxs-lookup"><span data-stu-id="55eac-104">AVEncDDProductionInfoExists property</span></span>

<span data-ttu-id="55eac-105">Указывает флаг сведений о звуковой рабочей информации в потоке цифрового звука Dolby.</span><span class="sxs-lookup"><span data-stu-id="55eac-105">Specifies the audio production information flag in a Dolby Digital audio stream.</span></span> <span data-ttu-id="55eac-106">Это свойство применяется к кодировщикам цифрового аудио Dolby.</span><span class="sxs-lookup"><span data-stu-id="55eac-106">This property applies to Dolby Digital audio encoders.</span></span>

<span data-ttu-id="55eac-107">Это свойство доступно для чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="55eac-107">This property is read/write.</span></span>

## <a name="data-type"></a><span data-ttu-id="55eac-108">Тип данных</span><span class="sxs-lookup"><span data-stu-id="55eac-108">Data type</span></span>

<span data-ttu-id="55eac-109">**Вариант \_ BOOL** (**\_ логическое значение VT**)</span><span class="sxs-lookup"><span data-stu-id="55eac-109">**VARIANT\_BOOL** (**VT\_BOOL**)</span></span>

## <a name="property-guid"></a><span data-ttu-id="55eac-110">GUID свойства</span><span class="sxs-lookup"><span data-stu-id="55eac-110">Property GUID</span></span>

<span data-ttu-id="55eac-111">**КОДЕКАПИ \_ авенкддпродуктионинфоексистс**</span><span class="sxs-lookup"><span data-stu-id="55eac-111">**CODECAPI\_AVEncDDProductionInfoExists**</span></span>

## <a name="remarks"></a><span data-ttu-id="55eac-112">Комментарии</span><span class="sxs-lookup"><span data-stu-id="55eac-112">Remarks</span></span>

<span data-ttu-id="55eac-113">Если значение является **вариантным \_ true**, настройки уровня смешения и типа комнаты являются допустимыми.</span><span class="sxs-lookup"><span data-stu-id="55eac-113">If the value is **VARIANT\_TRUE**, the mixing level and room type settings are valid.</span></span> <span data-ttu-id="55eac-114">Укажите эти параметры с помощью свойств [**авенкддпродуктионрумтипе**](avencddproductionroomtype-property.md) и [**авенкддпродуктионмикслевел**](avencddproductionmixlevel-property.md) .</span><span class="sxs-lookup"><span data-stu-id="55eac-114">Specify these settings with the [**AVEncDDProductionRoomType**](avencddproductionroomtype-property.md) and [**AVEncDDProductionMixLevel**](avencddproductionmixlevel-property.md) properties.</span></span>

## <a name="requirements"></a><span data-ttu-id="55eac-115">Требования</span><span class="sxs-lookup"><span data-stu-id="55eac-115">Requirements</span></span>



| <span data-ttu-id="55eac-116">Требование</span><span class="sxs-lookup"><span data-stu-id="55eac-116">Requirement</span></span> | <span data-ttu-id="55eac-117">Значение</span><span class="sxs-lookup"><span data-stu-id="55eac-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="55eac-118">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="55eac-118">Minimum supported client</span></span><br/> | <span data-ttu-id="55eac-119">Приложения Windows 2000 Professional \[ классические приложения \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="55eac-119">Windows 2000 Professional \[desktop apps \| UWP apps\]</span></span><br/>                     |
| <span data-ttu-id="55eac-120">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="55eac-120">Minimum supported server</span></span><br/> | <span data-ttu-id="55eac-121">\[Приложения UWP для классических приложений Windows 2000 \|\]</span><span class="sxs-lookup"><span data-stu-id="55eac-121">Windows 2000 Server \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="55eac-122">Header</span><span class="sxs-lookup"><span data-stu-id="55eac-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="55eac-123"><dt>Кодекапи. h</dt></span><span class="sxs-lookup"><span data-stu-id="55eac-123"><dt>Codecapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="55eac-124">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="55eac-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="55eac-125">Свойства кодека API</span><span class="sxs-lookup"><span data-stu-id="55eac-125">Codec API Properties</span></span>](codec-api-properties.md)
</dt> <dt>

[<span data-ttu-id="55eac-126">**Интерфейс Икодекапи**</span><span class="sxs-lookup"><span data-stu-id="55eac-126">**ICodecAPI Interface**</span></span>](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

 




