---
description: Указывает, ограничена ли сложность алгоритма кодирования звука.
ms.assetid: a50b840f-9fe8-4291-b93f-f09c241fe802
title: Свойство MFPKEY_CONSTRAINENCOMPLEXITY (Вмкодекдсп. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bdc6e3d5a7077c72e5933ecbc235092174e263fe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105692861"
---
# <a name="mfpkey_constrainencomplexity-property"></a><span data-ttu-id="9ac4a-103">МФПКЭЙ \_ констраиненкомплексити, свойство</span><span class="sxs-lookup"><span data-stu-id="9ac4a-103">MFPKEY\_CONSTRAINENCOMPLEXITY Property</span></span>

<span data-ttu-id="9ac4a-104">Указывает, ограничена ли сложность алгоритма кодирования звука.</span><span class="sxs-lookup"><span data-stu-id="9ac4a-104">Specifies whether the complexity of the audio encoding algorithm is constrained.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="9ac4a-105">Константа для Ипропертибаг</span><span class="sxs-lookup"><span data-stu-id="9ac4a-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="9ac4a-106">Доступно только с помощью [**ипропертисторе**](/windows/win32/api/propsys/nn-propsys-ipropertystore).</span><span class="sxs-lookup"><span data-stu-id="9ac4a-106">Available only by using [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).</span></span>

## <a name="data-type"></a><span data-ttu-id="9ac4a-107">Тип данных</span><span class="sxs-lookup"><span data-stu-id="9ac4a-107">Data Type</span></span>

<span data-ttu-id="9ac4a-108">**Логическое значение VT \_**</span><span class="sxs-lookup"><span data-stu-id="9ac4a-108">**VT\_BOOL**</span></span>

## <a name="default-value"></a><span data-ttu-id="9ac4a-109">Значение по умолчанию</span><span class="sxs-lookup"><span data-stu-id="9ac4a-109">Default Value</span></span>

<span data-ttu-id="9ac4a-110">**ВАРИАНТ \_ false**</span><span class="sxs-lookup"><span data-stu-id="9ac4a-110">**VARIANT\_FALSE**</span></span>

## <a name="remarks"></a><span data-ttu-id="9ac4a-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="9ac4a-111">Remarks</span></span>

<span data-ttu-id="9ac4a-112">Если оставить это свойство по умолчанию со значением **Variant \_ false**, кодировщик использует алгоритм по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="9ac4a-112">If you leave this property at its default value of **VARIANT\_FALSE**, the audio encoder uses its default algorithm.</span></span> <span data-ttu-id="9ac4a-113">Алгоритм по умолчанию зависит от типа выходных данных и версии операционной системы Windows.</span><span class="sxs-lookup"><span data-stu-id="9ac4a-113">The default algorithm depends on the output type and which version of Windows is running.</span></span> <span data-ttu-id="9ac4a-114">В следующей таблице описывается поведение по умолчанию для различных сочетаний.</span><span class="sxs-lookup"><span data-stu-id="9ac4a-114">The following table describes the default behavior for the different combinations.</span></span>



| <span data-ttu-id="9ac4a-115">Операционная система</span><span class="sxs-lookup"><span data-stu-id="9ac4a-115">Operating system</span></span> | <span data-ttu-id="9ac4a-116">Поведение по умолчанию</span><span class="sxs-lookup"><span data-stu-id="9ac4a-116">Default behavior</span></span>                                                                                                                                                                                    |
|------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9ac4a-117">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="9ac4a-117">Windows Vista</span></span>    | <span data-ttu-id="9ac4a-118">Для всех типов выходных данных кодировщик по умолчанию использует самый сложный алгоритм.</span><span class="sxs-lookup"><span data-stu-id="9ac4a-118">For all output types, the audio encoder uses the most complex algorithm by default.</span></span>                                                                                                                 |
| <span data-ttu-id="9ac4a-119">Windows 7</span><span class="sxs-lookup"><span data-stu-id="9ac4a-119">Windows 7</span></span>        | <span data-ttu-id="9ac4a-120">Для стандартных и профессиональных типов выходных данных кодировщик по умолчанию использует самый сложный алгоритм.</span><span class="sxs-lookup"><span data-stu-id="9ac4a-120">For Standard and Professional output types, the audio encoder uses the most complex algorithm by default.</span></span> <span data-ttu-id="9ac4a-121">Для типов выходных данных без потерь в кодировщике используется по умолчанию наименьший сложный алгоритм.</span><span class="sxs-lookup"><span data-stu-id="9ac4a-121">For Lossless output types, the audio encoder uses the least complex algorithm by default.</span></span> |



 

<span data-ttu-id="9ac4a-122">Если для этого свойства задано **значение \_ true**, необходимо также указать значение сложности, задав свойство [**мфпкэй \_ енккомплексити**](mfpkey-enccomplexityproperty.md) .</span><span class="sxs-lookup"><span data-stu-id="9ac4a-122">If you set this property to **VARIANT\_TRUE**, you must also specify a complexity value by setting the [**MFPKEY\_ENCCOMPLEXITY**](mfpkey-enccomplexityproperty.md) property.</span></span>

## <a name="requirements"></a><span data-ttu-id="9ac4a-123">Требования</span><span class="sxs-lookup"><span data-stu-id="9ac4a-123">Requirements</span></span>



| <span data-ttu-id="9ac4a-124">Требование</span><span class="sxs-lookup"><span data-stu-id="9ac4a-124">Requirement</span></span> | <span data-ttu-id="9ac4a-125">Значение</span><span class="sxs-lookup"><span data-stu-id="9ac4a-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="9ac4a-126">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="9ac4a-126">Minimum supported client</span></span><br/> | <span data-ttu-id="9ac4a-127">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="9ac4a-127">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="9ac4a-128">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="9ac4a-128">Minimum supported server</span></span><br/> | <span data-ttu-id="9ac4a-129">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="9ac4a-129">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="9ac4a-130">Header</span><span class="sxs-lookup"><span data-stu-id="9ac4a-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="9ac4a-131"><dt>Вмкодекдсп. h</dt></span><span class="sxs-lookup"><span data-stu-id="9ac4a-131"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9ac4a-132">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="9ac4a-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9ac4a-133">Свойства Media Foundation</span><span class="sxs-lookup"><span data-stu-id="9ac4a-133">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 
