---
description: Указывает среднюю скорость кодирования в битах в секунду. Это свойство применяется только к режимам кодирования с постоянным битом (CBR) и переменной скоростью с переменным битом (VBR).
ms.assetid: 8519685a-4f5b-44af-ad46-09eba7a198c6
title: Свойство Авенккоммонмеанбитрате (Кодекапи. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d4eaec7fc6578e6e69a45616ee6de059bb7a378b
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "104538006"
---
# <a name="avenccommonmeanbitrate-property"></a><span data-ttu-id="d6122-104">Авенккоммонмеанбитрате, свойство</span><span class="sxs-lookup"><span data-stu-id="d6122-104">AVEncCommonMeanBitRate property</span></span>

<span data-ttu-id="d6122-105">Указывает среднюю скорость кодирования в битах в секунду.</span><span class="sxs-lookup"><span data-stu-id="d6122-105">Specifies the average encoded bit rate, in bits per second.</span></span> <span data-ttu-id="d6122-106">Это свойство применяется только к режимам кодирования с постоянным битом (CBR) и переменной скоростью с переменным битом (VBR).</span><span class="sxs-lookup"><span data-stu-id="d6122-106">This property applies only to constant bit rate (CBR) and variable bit rate (VBR) encoding modes.</span></span>

<span data-ttu-id="d6122-107">Это свойство доступно для чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="d6122-107">This property is read/write.</span></span>

## <a name="data-type"></a><span data-ttu-id="d6122-108">Тип данных</span><span class="sxs-lookup"><span data-stu-id="d6122-108">Data type</span></span>

<span data-ttu-id="d6122-109">**UINT32** (**VT \_ UI4**)</span><span class="sxs-lookup"><span data-stu-id="d6122-109">**UINT32** (**VT\_UI4**)</span></span>

## <a name="property-guid"></a><span data-ttu-id="d6122-110">GUID свойства</span><span class="sxs-lookup"><span data-stu-id="d6122-110">Property GUID</span></span>

<span data-ttu-id="d6122-111">**КОДЕКАПИ \_ авенккоммонмеанбитрате**</span><span class="sxs-lookup"><span data-stu-id="d6122-111">**CODECAPI\_AVEncCommonMeanBitRate**</span></span>

## <a name="property-value"></a><span data-ttu-id="d6122-112">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="d6122-112">Property value</span></span>

<span data-ttu-id="d6122-113">Кодировщики могут реализовывать это свойство как перечислимый набор или как линейный Диапазон.</span><span class="sxs-lookup"><span data-stu-id="d6122-113">Encoders can implement this property as an enumerated set or as a linear range.</span></span>

## <a name="remarks"></a><span data-ttu-id="d6122-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="d6122-114">Remarks</span></span>

<span data-ttu-id="d6122-115">Это свойство также используется с [кодировщиками камер H. 264 увк 1,5](/windows/desktop/medfound/camera-encoder-h264-uvc-1-5).</span><span class="sxs-lookup"><span data-stu-id="d6122-115">This property is also used with [H.264 UVC 1.5 camera encoders](/windows/desktop/medfound/camera-encoder-h264-uvc-1-5).</span></span>

## <a name="requirements"></a><span data-ttu-id="d6122-116">Требования</span><span class="sxs-lookup"><span data-stu-id="d6122-116">Requirements</span></span>



| <span data-ttu-id="d6122-117">Требование</span><span class="sxs-lookup"><span data-stu-id="d6122-117">Requirement</span></span> | <span data-ttu-id="d6122-118">Значение</span><span class="sxs-lookup"><span data-stu-id="d6122-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="d6122-119">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="d6122-119">Minimum supported client</span></span><br/> | <span data-ttu-id="d6122-120">Приложения Windows 2000 Professional \[ классические приложения \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="d6122-120">Windows 2000 Professional \[desktop apps \| UWP apps\]</span></span><br/>                     |
| <span data-ttu-id="d6122-121">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="d6122-121">Minimum supported server</span></span><br/> | <span data-ttu-id="d6122-122">\[Приложения UWP для классических приложений Windows 2000 \|\]</span><span class="sxs-lookup"><span data-stu-id="d6122-122">Windows 2000 Server \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="d6122-123">Header</span><span class="sxs-lookup"><span data-stu-id="d6122-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="d6122-124"><dt>Кодекапи. h</dt></span><span class="sxs-lookup"><span data-stu-id="d6122-124"><dt>Codecapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d6122-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="d6122-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d6122-126">Свойства кодека API</span><span class="sxs-lookup"><span data-stu-id="d6122-126">Codec API Properties</span></span>](codec-api-properties.md)
</dt> <dt>

[<span data-ttu-id="d6122-127">**Интерфейс Икодекапи**</span><span class="sxs-lookup"><span data-stu-id="d6122-127">**ICodecAPI Interface**</span></span>](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

