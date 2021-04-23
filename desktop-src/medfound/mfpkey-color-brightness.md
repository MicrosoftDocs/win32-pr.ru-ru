---
description: Корректирует яркость.
ms.assetid: 1b3f56eb-3f22-4120-ba6c-331eccd5d303
title: Свойство MFPKEY_COLOR_BRIGHTNESS (Вмкодекдсп. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 685ab934a91f1843183fcfa88bb94c83e602db27
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103909392"
---
# <a name="mfpkey_color_brightness-property"></a><span data-ttu-id="b7174-103">МФПКЭЙ \_ , \_ свойство яркости цвета</span><span class="sxs-lookup"><span data-stu-id="b7174-103">MFPKEY\_COLOR\_BRIGHTNESS Property</span></span>

<span data-ttu-id="b7174-104">Корректирует яркость.</span><span class="sxs-lookup"><span data-stu-id="b7174-104">Adjusts the brightness.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="b7174-105">Константа для Ипропертибаг</span><span class="sxs-lookup"><span data-stu-id="b7174-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="b7174-106">Доступно только с помощью [**ипропертисторе**](/windows/win32/api/propsys/nn-propsys-ipropertystore).</span><span class="sxs-lookup"><span data-stu-id="b7174-106">Available only by using [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).</span></span>

## <a name="data-type"></a><span data-ttu-id="b7174-107">Тип данных</span><span class="sxs-lookup"><span data-stu-id="b7174-107">Data Type</span></span>

<span data-ttu-id="b7174-108">VT \_ I4</span><span class="sxs-lookup"><span data-stu-id="b7174-108">VT\_I4</span></span>

## <a name="default-value"></a><span data-ttu-id="b7174-109">Значение по умолчанию</span><span class="sxs-lookup"><span data-stu-id="b7174-109">Default Value</span></span>

<span data-ttu-id="b7174-110">0</span><span class="sxs-lookup"><span data-stu-id="b7174-110">0</span></span>

## <a name="applies-to"></a><span data-ttu-id="b7174-111">Применение</span><span class="sxs-lookup"><span data-stu-id="b7174-111">Applies To</span></span>

-   [<span data-ttu-id="b7174-112">Преобразование элемента управления цветом DSP</span><span class="sxs-lookup"><span data-stu-id="b7174-112">Color Control Transform DSP</span></span>](colorcontroltransform.md)

## <a name="remarks"></a><span data-ttu-id="b7174-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="b7174-113">Remarks</span></span>

<span data-ttu-id="b7174-114">Корректировка яркости выполняется путем добавления значения в канал яркости.</span><span class="sxs-lookup"><span data-stu-id="b7174-114">Brightness adjustment is performed by adding a value to the luma channel.</span></span>

<span data-ttu-id="b7174-115">Это свойство имеет диапазон от-127 до 127.</span><span class="sxs-lookup"><span data-stu-id="b7174-115">This property has a range of -127 to 127.</span></span> <span data-ttu-id="b7174-116">Ноль означает отсутствие изменений в яркости.</span><span class="sxs-lookup"><span data-stu-id="b7174-116">Zero indicates no change in brightness.</span></span>

## <a name="requirements"></a><span data-ttu-id="b7174-117">Требования</span><span class="sxs-lookup"><span data-stu-id="b7174-117">Requirements</span></span>



| <span data-ttu-id="b7174-118">Требование</span><span class="sxs-lookup"><span data-stu-id="b7174-118">Requirement</span></span> | <span data-ttu-id="b7174-119">Значение</span><span class="sxs-lookup"><span data-stu-id="b7174-119">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b7174-120">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="b7174-120">Minimum supported client</span></span><br/> | <span data-ttu-id="b7174-121">Только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="b7174-121">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="b7174-122">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="b7174-122">Minimum supported server</span></span><br/> | <span data-ttu-id="b7174-123">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="b7174-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="b7174-124">Header</span><span class="sxs-lookup"><span data-stu-id="b7174-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="b7174-125"><dt>Вмкодекдсп. h</dt></span><span class="sxs-lookup"><span data-stu-id="b7174-125"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b7174-126">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="b7174-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b7174-127">Свойства Media Foundation</span><span class="sxs-lookup"><span data-stu-id="b7174-127">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 
