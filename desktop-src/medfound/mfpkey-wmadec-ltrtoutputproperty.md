---
description: Указывает, следует ли выполнять декодер Lt-Rt свертывания.
ms.assetid: ce1dc4ea-4326-40ab-bb30-ff1a34f06d79
title: Свойство MFPKEY_WMADEC_LTRTOUTPUT (Вмкодекдсп. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d4f4a83d2529ce3b37282be35924b48288d4df45
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104155387"
---
# <a name="mfpkey_wmadec_ltrtoutput-property"></a><span data-ttu-id="309f0-103">МФПКЭЙ \_ вмадек \_ Лтртаутпут, свойство</span><span class="sxs-lookup"><span data-stu-id="309f0-103">MFPKEY\_WMADEC\_LTRTOUTPUT Property</span></span>

<span data-ttu-id="309f0-104">Указывает, следует ли выполнять декодер Lt-Rt свертывания.</span><span class="sxs-lookup"><span data-stu-id="309f0-104">Specifies whether the decoder should perform Lt-Rt fold down.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="309f0-105">Константа для Ипропертибаг</span><span class="sxs-lookup"><span data-stu-id="309f0-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="309f0-106">Доступно только с помощью [**ипропертисторе**](/windows/win32/api/propsys/nn-propsys-ipropertystore).</span><span class="sxs-lookup"><span data-stu-id="309f0-106">Available only by using [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).</span></span>

## <a name="data-type"></a><span data-ttu-id="309f0-107">Тип данных</span><span class="sxs-lookup"><span data-stu-id="309f0-107">Data Type</span></span>

<span data-ttu-id="309f0-108">**Логическое значение VT \_**</span><span class="sxs-lookup"><span data-stu-id="309f0-108">**VT\_BOOL**</span></span>

## <a name="default-value"></a><span data-ttu-id="309f0-109">Значение по умолчанию</span><span class="sxs-lookup"><span data-stu-id="309f0-109">Default Value</span></span>

<span data-ttu-id="309f0-110">**ВАРИАНТ \_ false**</span><span class="sxs-lookup"><span data-stu-id="309f0-110">**VARIANT\_FALSE**</span></span>

## <a name="remarks"></a><span data-ttu-id="309f0-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="309f0-111">Remarks</span></span>

<span data-ttu-id="309f0-112">Если это свойство имеет значение VARIANT \_ false, а выходные данные — стерео, то аудио-декодер использует простой канал.</span><span class="sxs-lookup"><span data-stu-id="309f0-112">If this property has a value of VARIANT\_FALSE and the output is stereo, the audio decoder uses simple channel fold down.</span></span> <span data-ttu-id="309f0-113">Если это свойство имеет значение \_ true, то аудио-декодер выполняет Lt-Rt (с матрицей) по вертикали до стерео, а затем любой окружающий декодер Dolby можно использовать для декодирования вокруг матрицы.</span><span class="sxs-lookup"><span data-stu-id="309f0-113">If this property has a value of VARIANT\_TRUE, the audio decoder performs Lt-Rt (matrixed) fold down to stereo, and then any Dolby Surround decoder can be used to decode the matrixed surround .</span></span> <span data-ttu-id="309f0-114">Например, звуковой декодер может выполнять Lt-Rt выгнуть содержимое 5,1 или 7,1.</span><span class="sxs-lookup"><span data-stu-id="309f0-114">For example, the audio decoder could perform Lt-Rt fold down on 5.1 or 7.1 content.</span></span>

<span data-ttu-id="309f0-115">Это свойство поддерживается только в том случае, если декодер выступает в качестве объекта мультимедиа DirectX (DMO).</span><span class="sxs-lookup"><span data-stu-id="309f0-115">This property is supported only when the decoder is acting as a DirectX Media Object (DMO).</span></span> <span data-ttu-id="309f0-116">Отсутствие какого-либо вида поддерживается, если декодер выступает в качестве Media Foundation преобразования (MFT).</span><span class="sxs-lookup"><span data-stu-id="309f0-116">No fold down of any kind is supported when the decoder is acting as a Media Foundation Transform (MFT).</span></span>

<span data-ttu-id="309f0-117">В Windows Vista, если вы получаете интерфейс **ипропертисторе** для звукового декодера, декодер выступает в качестве MFT.</span><span class="sxs-lookup"><span data-stu-id="309f0-117">On Windows Vista, if you obtain an **IPropertyStore** interface on an audio decoder, the decoder acts as an MFT.</span></span> <span data-ttu-id="309f0-118">Следовательно, это свойство нельзя использовать в Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="309f0-118">Consequently, this property cannot be used on Windows Vista.</span></span> <span data-ttu-id="309f0-119">Сведения о том, когда декодер выступает в качестве DMO или MFT, см. на страницах справочника по отдельным кодекам в разделе [объекты кодека](codecobjects.md).</span><span class="sxs-lookup"><span data-stu-id="309f0-119">For information on when a decoder acts as a DMO or an MFT, see the individual codec reference pages under [Codec Objects](codecobjects.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="309f0-120">Требования</span><span class="sxs-lookup"><span data-stu-id="309f0-120">Requirements</span></span>



| <span data-ttu-id="309f0-121">Требование</span><span class="sxs-lookup"><span data-stu-id="309f0-121">Requirement</span></span> | <span data-ttu-id="309f0-122">Значение</span><span class="sxs-lookup"><span data-stu-id="309f0-122">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="309f0-123">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="309f0-123">Minimum supported client</span></span><br/> | <span data-ttu-id="309f0-124">Только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="309f0-124">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="309f0-125">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="309f0-125">Minimum supported server</span></span><br/> | <span data-ttu-id="309f0-126">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="309f0-126">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="309f0-127">Header</span><span class="sxs-lookup"><span data-stu-id="309f0-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="309f0-128"><dt>Вмкодекдсп. h</dt></span><span class="sxs-lookup"><span data-stu-id="309f0-128"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="309f0-129">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="309f0-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="309f0-130">Свойства Media Foundation</span><span class="sxs-lookup"><span data-stu-id="309f0-130">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 
