---
title: Controls. Куррентпоситионтимекоде
description: Свойство Куррентпоситионтимекоде указывает или получает текущую позицию в текущем элементе мультимедиа, используя формат кода времени. Сейчас это свойство поддерживает код времени SMPTE.
ms.assetid: 98d79756-c6cf-4dbc-936a-58229452451c
keywords:
- Проигрыватель Windows Media Controls. Куррентпоситионтимекоде
topic_type:
- apiref
api_name:
- Controls.currentPositionTimecode
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2e2a4ddeb0849a829ff7a16fd80ff4891cfe56c8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105694559"
---
# <a name="controlscurrentpositiontimecode"></a><span data-ttu-id="0459f-105">Controls. Куррентпоситионтимекоде</span><span class="sxs-lookup"><span data-stu-id="0459f-105">Controls.currentPositionTimecode</span></span>

<span data-ttu-id="0459f-106">Свойство **куррентпоситионтимекоде** указывает или получает текущую позицию в текущем элементе мультимедиа, используя формат кода времени.</span><span class="sxs-lookup"><span data-stu-id="0459f-106">The **currentPositionTimecode** property specifies or retrieves the current position in the current media item using a time code format.</span></span> <span data-ttu-id="0459f-107">Сейчас это свойство поддерживает код времени SMPTE.</span><span class="sxs-lookup"><span data-stu-id="0459f-107">This property currently supports SMPTE time code.</span></span>

``` syntax
player.controls.currentPositionTimecode
      
```

## <a name="possible-values"></a><span data-ttu-id="0459f-108">Возможные значения</span><span class="sxs-lookup"><span data-stu-id="0459f-108">Possible Values</span></span>

<span data-ttu-id="0459f-109">Это свойство является **строкой** для чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="0459f-109">This property is a read/write **String**.</span></span>

## <a name="remarks"></a><span data-ttu-id="0459f-110">Комментарии</span><span class="sxs-lookup"><span data-stu-id="0459f-110">Remarks</span></span>

<span data-ttu-id="0459f-111">Код времени SMPTE предоставляет стандартный способ идентификации отдельного кадра видео, который полезен для синхронизации воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="0459f-111">SMPTE time code provides a standard way of identifying an individual video frame, which is useful for synchronizing playback.</span></span> <span data-ttu-id="0459f-112">Если файл цифрового мультимедиа поддерживает код времени SMPTE, проигрыватель Windows Media может получить сведения о текущем положении кода времени или найти кадр видео, определенный **строкой** кода времени.</span><span class="sxs-lookup"><span data-stu-id="0459f-112">If a digital media file supports SMPTE time code, Windows Media Player can retrieve the current time code position information or seek to a video frame identified by a particular time code **String**.</span></span>

<span data-ttu-id="0459f-113">Код времени SMPTE определяет конкретный кадр по количеству часов, минут, секунд и кадров, разделяющих его от определенного кадра ссылок кадром, обозначенным как нулевое время.</span><span class="sxs-lookup"><span data-stu-id="0459f-113">SMPTE time code identifies a particular frame by the number of hours, minutes, seconds, and frames that separate it from a particular reference frame the frame designated as time zero.</span></span> <span data-ttu-id="0459f-114">Как правило, начальным кадром времени является начало файла, а определенное значение кода времени SMPTE представляет время, прошедшее с начала файла.</span><span class="sxs-lookup"><span data-stu-id="0459f-114">Usually the time zero frame is the start of the file and a particular SMPTE time code value represents the elapsed time since the start of the file.</span></span>

<span data-ttu-id="0459f-115">**Строка** кода времени находится в формате \[  \] *чч*:*мм*:*СС*.*FF* , где \[ *Range* \] представляет диапазон, *чч* представляет часы, *mm* — минуты, *SS* — секунды, а *FF* — кадры.</span><span class="sxs-lookup"><span data-stu-id="0459f-115">The time code **String** is in the format \[*range*\]*hh*:*mm*:*ss*.*ff* where \[*range*\] represents the range, *hh* represents hours, *mm* represents minutes, *ss* represents seconds, and *ff* represents frames.</span></span> <span data-ttu-id="0459f-116">При указании значения с помощью **куррентпоситионтимекоде** необходимо включить все восемь цифр, используя нули в качестве заполнителей.</span><span class="sxs-lookup"><span data-stu-id="0459f-116">When specifying a value using **currentPositionTimecode**, you must include all eight digits using zeros as placeholders.</span></span>

<span data-ttu-id="0459f-117">Спецификатор \[ *диапазона* \] соответствует элементу **вранже** в структуре **\_ \_ \_ данных расширения** периода времени формата Windows Media ВМТ.</span><span class="sxs-lookup"><span data-stu-id="0459f-117">The \[*range*\] specifier corresponds to the **wRange** member of the Windows Media Format **WMT\_TIMECODE\_EXTENSION\_DATA** structure.</span></span> <span data-ttu-id="0459f-118">Дополнительные сведения о диапазонах кодов времени см. в разделе Windows Media Format SDK.</span><span class="sxs-lookup"><span data-stu-id="0459f-118">For more information about time code ranges, see the Windows Media Format SDK.</span></span>

<span data-ttu-id="0459f-119">Указание и извлечение **куррентпоситионтимекоде** поддерживается только для файлов, содержащих сведения о коде времени SMPTE.</span><span class="sxs-lookup"><span data-stu-id="0459f-119">Specifying and retrieving **currentPositionTimecode** is only supported for files that contain SMPTE time code information.</span></span>

## <a name="examples"></a><span data-ttu-id="0459f-120">Примеры</span><span class="sxs-lookup"><span data-stu-id="0459f-120">Examples</span></span>

<span data-ttu-id="0459f-121">В следующем примере кода указывается **куррентпоситионтимекоде** в виде 1 часа, 0 минут, 30 секунд и 5 кадров.</span><span class="sxs-lookup"><span data-stu-id="0459f-121">The following code example specifies **currentPositionTimecode** as 1 hour, zero minutes, 30 seconds, and 5 frames.</span></span> <span data-ttu-id="0459f-122">Объект **Player** создан с идентификатором "Player".</span><span class="sxs-lookup"><span data-stu-id="0459f-122">The **Player** object was created with ID = "Player".</span></span>


```
// Seek to a frame using SMPTE time code.
Player.controls.currentPositionTimecode = "[00000]01:00:30.05";

```



## <a name="requirements"></a><span data-ttu-id="0459f-123">Требования</span><span class="sxs-lookup"><span data-stu-id="0459f-123">Requirements</span></span>



| <span data-ttu-id="0459f-124">Требование</span><span class="sxs-lookup"><span data-stu-id="0459f-124">Requirement</span></span> | <span data-ttu-id="0459f-125">Значение</span><span class="sxs-lookup"><span data-stu-id="0459f-125">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="0459f-126">Версия</span><span class="sxs-lookup"><span data-stu-id="0459f-126">Version</span></span><br/> | <span data-ttu-id="0459f-127">Проигрыватель Windows Media 9 Series или более поздней версии.</span><span class="sxs-lookup"><span data-stu-id="0459f-127">Windows Media Player 9 Series or later.</span></span><br/>                                 |
| <span data-ttu-id="0459f-128">DLL</span><span class="sxs-lookup"><span data-stu-id="0459f-128">DLL</span></span><br/>     | <dl> <span data-ttu-id="0459f-129"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0459f-129"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0459f-130">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="0459f-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0459f-131">**Объект Controls**</span><span class="sxs-lookup"><span data-stu-id="0459f-131">**Controls Object**</span></span>](controls-object.md)
</dt> </dl>

 

 





