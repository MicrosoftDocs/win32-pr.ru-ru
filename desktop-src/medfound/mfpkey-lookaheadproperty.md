---
description: Указывает число кадров после текущего кадра, которое будет вычислено кодеком перед кодированием текущего кадра.
ms.assetid: e5cdd066-e25a-4107-9523-5611bd792372
title: Свойство MFPKEY_LOOKAHEAD (Вмкодекдсп. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e1a024c4d0be6ef7ab16c4bf51f290b01de3282b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105692849"
---
# <a name="mfpkey_lookahead-property"></a><span data-ttu-id="8affe-103">Свойство МФПКЭЙного \_ просмотра вперед</span><span class="sxs-lookup"><span data-stu-id="8affe-103">MFPKEY\_LOOKAHEAD Property</span></span>

<span data-ttu-id="8affe-104">Указывает число кадров после текущего кадра, которое будет вычислено кодеком перед кодированием текущего кадра.</span><span class="sxs-lookup"><span data-stu-id="8affe-104">Specifies the number of frames after the current frame that the codec will evaluate before encoding the current frame.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="8affe-105">Константа для Ипропертибаг</span><span class="sxs-lookup"><span data-stu-id="8affe-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="8affe-106">g \_ всзвмвклукахеад</span><span class="sxs-lookup"><span data-stu-id="8affe-106">g\_wszWMVCLookAhead</span></span>

## <a name="data-type"></a><span data-ttu-id="8affe-107">Тип данных</span><span class="sxs-lookup"><span data-stu-id="8affe-107">Data Type</span></span>

<span data-ttu-id="8affe-108">VT \_ I4</span><span class="sxs-lookup"><span data-stu-id="8affe-108">VT\_I4</span></span>

## <a name="default-value"></a><span data-ttu-id="8affe-109">Значение по умолчанию</span><span class="sxs-lookup"><span data-stu-id="8affe-109">Default Value</span></span>

<span data-ttu-id="8affe-110">0</span><span class="sxs-lookup"><span data-stu-id="8affe-110">0</span></span>

## <a name="remarks"></a><span data-ttu-id="8affe-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="8affe-111">Remarks</span></span>

<span data-ttu-id="8affe-112">Когда кодек использует поиск вперед, он может более эффективно кодировать видео.</span><span class="sxs-lookup"><span data-stu-id="8affe-112">When the codec uses lookahead, it can encode the video more efficiently.</span></span>

<span data-ttu-id="8affe-113">Объект модуля записи пакета SDK Windows Media Format предполагают, что кодек будет кодировать каждый пример немедленно.</span><span class="sxs-lookup"><span data-stu-id="8affe-113">The writer object of the Windows Media Format SDK expects the codec to encode each sample immediately.</span></span> <span data-ttu-id="8affe-114">В результате эта функция не работает должным образом в программном обеспечении, использующем объект модуля записи (включая кодировщик Windows Media и проигрыватель Windows Media).</span><span class="sxs-lookup"><span data-stu-id="8affe-114">As a result, this feature does not work properly in software that uses the writer object (including Windows Media Encoder and Windows Media Player).</span></span> <span data-ttu-id="8affe-115">Все расширения модулей данных, связанные с видеокадрами, будут присоединены к неправильному выходному кадру.</span><span class="sxs-lookup"><span data-stu-id="8affe-115">Any data unit extensions associated with video frames will be attached to the wrong output frame.</span></span> <span data-ttu-id="8affe-116">Число кадров, по которым происходит размещение модулей обработки данных, равно количеству используемых кадров вперед.</span><span class="sxs-lookup"><span data-stu-id="8affe-116">The number of frames by which the data unit extensions are misplaced is equal to the number of frames of lookahead that are used.</span></span>

<span data-ttu-id="8affe-117">Допустимые значения для просмотра вперед в диапазоне от 0 до 16 кадров.</span><span class="sxs-lookup"><span data-stu-id="8affe-117">Valid lookahead values range from 0 to 16 frames.</span></span> <span data-ttu-id="8affe-118">Рекомендуемое значение — 16.</span><span class="sxs-lookup"><span data-stu-id="8affe-118">The recommended value is 16.</span></span>

## <a name="requirements"></a><span data-ttu-id="8affe-119">Требования</span><span class="sxs-lookup"><span data-stu-id="8affe-119">Requirements</span></span>



| <span data-ttu-id="8affe-120">Требование</span><span class="sxs-lookup"><span data-stu-id="8affe-120">Requirement</span></span> | <span data-ttu-id="8affe-121">Значение</span><span class="sxs-lookup"><span data-stu-id="8affe-121">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="8affe-122">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="8affe-122">Minimum supported client</span></span><br/> | <span data-ttu-id="8affe-123">Только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="8affe-123">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="8affe-124">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="8affe-124">Minimum supported server</span></span><br/> | <span data-ttu-id="8affe-125">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="8affe-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="8affe-126">Header</span><span class="sxs-lookup"><span data-stu-id="8affe-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="8affe-127"><dt>Вмкодекдсп. h</dt></span><span class="sxs-lookup"><span data-stu-id="8affe-127"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8affe-128">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="8affe-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8affe-129">Свойства Media Foundation</span><span class="sxs-lookup"><span data-stu-id="8affe-129">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 




