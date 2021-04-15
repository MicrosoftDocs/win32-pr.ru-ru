---
description: Указывает класс мультимедиа класса службы планировщика для декодирования потока.
ms.assetid: 77724879-62e4-439e-9dd0-3642cd7f75ca
title: Свойство Авдекммксс (UUIDs. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e0092ac516f9600929a9772d044f51e7e375548d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105669294"
---
# <a name="avdecmmcss-property"></a><span data-ttu-id="5d455-103">Авдекммксс, свойство</span><span class="sxs-lookup"><span data-stu-id="5d455-103">AVDecMmcss property</span></span>

<span data-ttu-id="5d455-104">Указывает класс мультимедиа класса службы планировщика для декодирования потока.</span><span class="sxs-lookup"><span data-stu-id="5d455-104">Specifies the Multimedia Class Scheduler Service (MMCSS) class for the decoding thread.</span></span>

<span data-ttu-id="5d455-105">Это свойство доступно для чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="5d455-105">This property is read/write.</span></span>

## <a name="data-type"></a><span data-ttu-id="5d455-106">Тип данных</span><span class="sxs-lookup"><span data-stu-id="5d455-106">Data type</span></span>

<span data-ttu-id="5d455-107">**BSTR** (**VT \_ BSTR**)</span><span class="sxs-lookup"><span data-stu-id="5d455-107">**BSTR** (**VT\_BSTR**)</span></span>

## <a name="property-guid"></a><span data-ttu-id="5d455-108">GUID свойства</span><span class="sxs-lookup"><span data-stu-id="5d455-108">Property GUID</span></span>

<span data-ttu-id="5d455-109">**КОДЕКАПИ \_ авдекммксскласс**</span><span class="sxs-lookup"><span data-stu-id="5d455-109">**CODECAPI\_AVDecMmcssClass**</span></span>

## <a name="property-value"></a><span data-ttu-id="5d455-110">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="5d455-110">Property value</span></span>

<span data-ttu-id="5d455-111">Значением этого свойства является имя класса MMCSS.</span><span class="sxs-lookup"><span data-stu-id="5d455-111">The value of this property is the name of the MMCSS class.</span></span>

## <a name="remarks"></a><span data-ttu-id="5d455-112">Комментарии</span><span class="sxs-lookup"><span data-stu-id="5d455-112">Remarks</span></span>

<span data-ttu-id="5d455-113">Служба MMCSS позволяет приложениям обеспечивать приоритетную обработку с учетом времени доступа к ресурсам ЦП.</span><span class="sxs-lookup"><span data-stu-id="5d455-113">MMCSS enables applications to ensure that time-sensitive processing has prioritized access to CPU resources.</span></span> <span data-ttu-id="5d455-114">Это работает путем повышения приоритета зарегистрированных потоков до большего количества потоков, в то же время периодически уменьшая их приоритеты для получения времени другим процессам.</span><span class="sxs-lookup"><span data-stu-id="5d455-114">It works by elevating registered threads to higher thread priorities while periodically decreasing their priorities to yield time to other processes.</span></span>

<span data-ttu-id="5d455-115">Рекомендуемое значение для звуковых декодеров — "аудио", а рекомендуемое значение для видеодекодеров — "Воспроизведение".</span><span class="sxs-lookup"><span data-stu-id="5d455-115">The recommended value for audio decoders is "Audio," and the recommended value for video decoders is "Playback."</span></span>

<span data-ttu-id="5d455-116">Если служба MMCSS недоступна или указанный класс MMCSS не существует, установка свойства не оказывает никакого влияния.</span><span class="sxs-lookup"><span data-stu-id="5d455-116">If the MMCSS service is not available or the specified MMCSS class does not exist, setting the property has no effect.</span></span>

## <a name="requirements"></a><span data-ttu-id="5d455-117">Требования</span><span class="sxs-lookup"><span data-stu-id="5d455-117">Requirements</span></span>



| <span data-ttu-id="5d455-118">Требование</span><span class="sxs-lookup"><span data-stu-id="5d455-118">Requirement</span></span> | <span data-ttu-id="5d455-119">Значение</span><span class="sxs-lookup"><span data-stu-id="5d455-119">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="5d455-120">Header</span><span class="sxs-lookup"><span data-stu-id="5d455-120">Header</span></span><br/> | <dl> <span data-ttu-id="5d455-121"><dt>UUID. h</dt></span><span class="sxs-lookup"><span data-stu-id="5d455-121"><dt>Uuids.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5d455-122">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="5d455-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5d455-123">Свойства кодека API</span><span class="sxs-lookup"><span data-stu-id="5d455-123">Codec API Properties</span></span>](codec-api-properties.md)
</dt> <dt>

[<span data-ttu-id="5d455-124">**Интерфейс Икодекапи**</span><span class="sxs-lookup"><span data-stu-id="5d455-124">**ICodecAPI Interface**</span></span>](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

 




