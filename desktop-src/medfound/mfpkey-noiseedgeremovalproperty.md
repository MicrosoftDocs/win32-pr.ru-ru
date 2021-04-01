---
description: Указывает, должен ли кодек попытаться обнаружить шумы в кадрах и удалить их.
ms.assetid: fdb4f3a8-1447-4e1e-a208-0f9b717f7626
title: Свойство MFPKEY_NOISEEDGEREMOVAL (Вмкодекдсп. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 30acd92bae7693d0714e42d6b4f832a521557bf2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104263987"
---
# <a name="mfpkey_noiseedgeremoval-property"></a><span data-ttu-id="0aa4b-103">МФПКЭЙ \_ ноисиджеремовал, свойство</span><span class="sxs-lookup"><span data-stu-id="0aa4b-103">MFPKEY\_NOISEEDGEREMOVAL Property</span></span>

<span data-ttu-id="0aa4b-104">Указывает, должен ли кодек попытаться обнаружить шумы в кадрах и удалить их.</span><span class="sxs-lookup"><span data-stu-id="0aa4b-104">Specifies whether the codec should attempt to detect noisy frame edges and remove them.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="0aa4b-105">Константа для Ипропертибаг</span><span class="sxs-lookup"><span data-stu-id="0aa4b-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="0aa4b-106">g \_ всзвмвкноисиджеремовал</span><span class="sxs-lookup"><span data-stu-id="0aa4b-106">g\_wszWMVCNoiseEdgeRemoval</span></span>

## <a name="data-type"></a><span data-ttu-id="0aa4b-107">Тип данных</span><span class="sxs-lookup"><span data-stu-id="0aa4b-107">Data Type</span></span>

<span data-ttu-id="0aa4b-108">Логическое значение VT \_</span><span class="sxs-lookup"><span data-stu-id="0aa4b-108">VT\_BOOL</span></span>

## <a name="default-value"></a><span data-ttu-id="0aa4b-109">Значение по умолчанию</span><span class="sxs-lookup"><span data-stu-id="0aa4b-109">Default Value</span></span>

<span data-ttu-id="0aa4b-110">FALSE</span><span class="sxs-lookup"><span data-stu-id="0aa4b-110">FALSE</span></span>

## <a name="remarks"></a><span data-ttu-id="0aa4b-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="0aa4b-111">Remarks</span></span>

<span data-ttu-id="0aa4b-112">Шумы в кадре обычно являются вертикальными пустыми интервалами (ВБИ) из кадра телевизионных телепередач.</span><span class="sxs-lookup"><span data-stu-id="0aa4b-112">A noisy frame edge is usually the vertical blanking interval (VBI) data from a frame of broadcast television.</span></span> <span data-ttu-id="0aa4b-113">ВБИ — это первые 21 строки просмотра кадра телевизора.</span><span class="sxs-lookup"><span data-stu-id="0aa4b-113">The VBI is the first 21 scan lines of the television frame.</span></span> <span data-ttu-id="0aa4b-114">Эти строки просмотра не содержат данных видео — они содержат данные о широковещательной рассылке.</span><span class="sxs-lookup"><span data-stu-id="0aa4b-114">These scan lines do not contain video data—they contain data about the broadcast.</span></span> <span data-ttu-id="0aa4b-115">Когда на карте записи записывается ТВ-сигнал, ВБИ обычно удаляется из рамки.</span><span class="sxs-lookup"><span data-stu-id="0aa4b-115">When a television signal is recorded by a capture card, the VBI is usually removed from the frame.</span></span> <span data-ttu-id="0aa4b-116">Функция обнаружения и исправления шумового периметра, выполняемая кодеком, может исправить только ребро с тремя или менее строками шума.</span><span class="sxs-lookup"><span data-stu-id="0aa4b-116">The noisy edge detection and correction performed by the codec can only correct an edge that has three or fewer lines of noise.</span></span> <span data-ttu-id="0aa4b-117">Если записанное видео содержит более трех бесшумных линий, возникает проблема с оборудованием, используемым для записи видео.</span><span class="sxs-lookup"><span data-stu-id="0aa4b-117">If captured video contains more than three noisy lines, there is a problem with the hardware used to capture the video.</span></span>

<span data-ttu-id="0aa4b-118">Если кодек настроен на удаление шума, он дублирует строки, смежные с шумным ребром, для заполнения рамки.</span><span class="sxs-lookup"><span data-stu-id="0aa4b-118">If the codec is set to remove noisy edges, it duplicates lines adjacent to the noisy edge to fill in the frame.</span></span>

## <a name="requirements"></a><span data-ttu-id="0aa4b-119">Требования</span><span class="sxs-lookup"><span data-stu-id="0aa4b-119">Requirements</span></span>



| <span data-ttu-id="0aa4b-120">Требование</span><span class="sxs-lookup"><span data-stu-id="0aa4b-120">Requirement</span></span> | <span data-ttu-id="0aa4b-121">Значение</span><span class="sxs-lookup"><span data-stu-id="0aa4b-121">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="0aa4b-122">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="0aa4b-122">Minimum supported client</span></span><br/> | <span data-ttu-id="0aa4b-123">Только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="0aa4b-123">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="0aa4b-124">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="0aa4b-124">Minimum supported server</span></span><br/> | <span data-ttu-id="0aa4b-125">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="0aa4b-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="0aa4b-126">Header</span><span class="sxs-lookup"><span data-stu-id="0aa4b-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="0aa4b-127"><dt>Вмкодекдсп. h</dt></span><span class="sxs-lookup"><span data-stu-id="0aa4b-127"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0aa4b-128">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="0aa4b-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0aa4b-129">Свойства Media Foundation</span><span class="sxs-lookup"><span data-stu-id="0aa4b-129">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 




