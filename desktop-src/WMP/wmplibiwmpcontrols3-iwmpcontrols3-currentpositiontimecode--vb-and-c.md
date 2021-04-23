---
title: IWMPControls3 Куррентпоситионтимекоде, свойство
description: Свойство Куррентпоситионтимекоде Возвращает или задает текущую позицию в текущем элементе мультимедиа, используя формат кода времени. Сейчас это свойство поддерживает код времени SMPTE.
ms.assetid: 035b812c-e976-4b4e-b4e5-820653257732
keywords:
- Проигрыватель Windows Media для свойства Куррентпоситионтимекоде
- Куррентпоситионтимекоде свойство проигрывателя Windows Media Player, интерфейс IWMPControls3
- Интерфейс IWMPControls3 Windows Media Player, свойство Куррентпоситионтимекоде
topic_type:
- apiref
api_name:
- IWMPControls3.currentPositionTimecode
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7660e6dc2690c310cf06f64e38190dc1cb3f24ab
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105649054"
---
# <a name="iwmpcontrols3currentpositiontimecode-property"></a><span data-ttu-id="6dc0b-107">Свойство IWMPControls3:: Куррентпоситионтимекоде</span><span class="sxs-lookup"><span data-stu-id="6dc0b-107">IWMPControls3::currentPositionTimecode property</span></span>

<span data-ttu-id="6dc0b-108">Свойство **куррентпоситионтимекоде** Возвращает или задает текущую позицию в текущем элементе мультимедиа, используя формат кода времени.</span><span class="sxs-lookup"><span data-stu-id="6dc0b-108">The **currentPositionTimecode** property gets or sets the current position in the current media item using a time code format.</span></span> <span data-ttu-id="6dc0b-109">Сейчас это свойство поддерживает код времени SMPTE.</span><span class="sxs-lookup"><span data-stu-id="6dc0b-109">This property currently supports SMPTE time code.</span></span>

## <a name="syntax"></a><span data-ttu-id="6dc0b-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="6dc0b-110">Syntax</span></span>


```CSharp
public System.String currentPositionTimecode {get; set;}
```


```VB

Public Property currentPositionTimecode As System.String
```





## <a name="property-value"></a><span data-ttu-id="6dc0b-111">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="6dc0b-111">Property value</span></span>

<span data-ttu-id="6dc0b-112">**Строка System. String** , которая является кодом времени SMPTE.</span><span class="sxs-lookup"><span data-stu-id="6dc0b-112">A **System.String** that is the SMPTE time code.</span></span>

## <a name="remarks"></a><span data-ttu-id="6dc0b-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="6dc0b-113">Remarks</span></span>

<span data-ttu-id="6dc0b-114">Код времени SMPTE предоставляет стандартный способ идентификации отдельного кадра видео, который полезен для синхронизации воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="6dc0b-114">SMPTE time code provides a standard way of identifying an individual video frame, which is useful for synchronizing playback.</span></span> <span data-ttu-id="6dc0b-115">Если файл цифрового мультимедиа поддерживает код времени SMPTE, проигрыватель Windows Media может получить сведения о текущем положении кода времени или найти кадр видео, определенный кодом времени.</span><span class="sxs-lookup"><span data-stu-id="6dc0b-115">If a digital media file supports SMPTE time code, Windows Media Player can retrieve the current time code position information or seek to a video frame identified by a particular time code.</span></span>

<span data-ttu-id="6dc0b-116">Код времени SMPTE определяет конкретный кадр по количеству часов, минут, секунд и кадров, разделяющих его от определенного кадра ссылок кадром, обозначенным как нулевое время.</span><span class="sxs-lookup"><span data-stu-id="6dc0b-116">SMPTE time code identifies a particular frame by the number of hours, minutes, seconds, and frames that separate it from a particular reference frame the frame designated as time zero.</span></span> <span data-ttu-id="6dc0b-117">Как правило, начальным кадром времени является начало файла, а определенное значение кода времени SMPTE представляет время, прошедшее с начала файла.</span><span class="sxs-lookup"><span data-stu-id="6dc0b-117">Usually the time zero frame is the start of the file and a particular SMPTE time code value represents the elapsed time since the start of the file.</span></span>

<span data-ttu-id="6dc0b-118">Код времени находится в формате \[  \] *чч*:*мм*:*СС*.*FF* , где \[ *Range* \] представляет диапазон, чч представляет часы, *mm* — минуты, *SS* — секунды, а *FF* — кадры.</span><span class="sxs-lookup"><span data-stu-id="6dc0b-118">The time code is in the format \[*range*\]*hh*:*mm*:*ss*.*ff* where \[*range*\] represents the range, hh represents hours, *mm* represents minutes, *ss* represents seconds, and *ff* represents frames.</span></span> <span data-ttu-id="6dc0b-119">При задании значения для **куррентпоситионтимекоде** необходимо включить все восемь цифр, используя нули в качестве заполнителей.</span><span class="sxs-lookup"><span data-stu-id="6dc0b-119">When setting a value for **currentPositionTimecode**, you must include all eight digits, using zeros as placeholders.</span></span>

<span data-ttu-id="6dc0b-120">\[*диапазон значений* \] соответствует члену **вранже** структуры **\_ \_ \_ данных расширения** времени в формате Windows Media ВМТ.</span><span class="sxs-lookup"><span data-stu-id="6dc0b-120">\[*range*\] corresponds to the **wRange** member of the Windows Media Format **WMT\_TIMECODE\_EXTENSION\_DATA** structure.</span></span> <span data-ttu-id="6dc0b-121">Дополнительные сведения о диапазонах кодов времени см. в разделе Windows Media Format SDK.</span><span class="sxs-lookup"><span data-stu-id="6dc0b-121">For more information about time code ranges, see the Windows Media Format SDK.</span></span>

<span data-ttu-id="6dc0b-122">Установка и получение **куррентпоситионтимекоде** поддерживаются только для файлов, содержащих сведения о коде времени SMPTE.</span><span class="sxs-lookup"><span data-stu-id="6dc0b-122">Setting and getting **currentPositionTimecode** is supported only for files that contain SMPTE time code information.</span></span>

## <a name="examples"></a><span data-ttu-id="6dc0b-123">Примеры</span><span class="sxs-lookup"><span data-stu-id="6dc0b-123">Examples</span></span>

<span data-ttu-id="6dc0b-124">В следующем примере кода указывается **куррентпоситионтимекоде** в виде 1 часа, 0 минут, 30 секунд и 5 кадров.</span><span class="sxs-lookup"><span data-stu-id="6dc0b-124">The following code example specifies **currentPositionTimecode** as 1 hour, zero minutes, 30 seconds, and 5 frames.</span></span> <span data-ttu-id="6dc0b-125">Объект **аксвмплиб. аксвиндовсмедиаплайер** представлен переменной с именем Player.</span><span class="sxs-lookup"><span data-stu-id="6dc0b-125">The **AxWMPLib.AxWindowsMediaPlayer** object is represented by the variable named player.</span></span>


```CSharp
// Cast the interface returned by player.Ctlcontrols to an IWMPControls3 interface
// so that you can use the currentPositionTimecode property.
WMPLib.IWMPControls3 controls = (WMPLib.IWMPControls3)player.Ctlcontrols;

// Seek to a frame using SMPTE time code.
controls.currentPositionTimecode = "[00000]01:00:30.05";
```


```VB

' Cast the interface returned by player.Ctlcontrols to an IWMPControls3 interface
&#39; so that you can use the currentPositionTimecode property.
Dim controls As WMPLib.IWMPControls3 = player.Ctlcontrols

&#39; Seek to a frame using SMPTE time code.
Controls.currentPositionTimecode = &quot;[00000]01:00:30.05&quot;
```





## <a name="requirements"></a><span data-ttu-id="6dc0b-126">Требования</span><span class="sxs-lookup"><span data-stu-id="6dc0b-126">Requirements</span></span>



| <span data-ttu-id="6dc0b-127">Требование</span><span class="sxs-lookup"><span data-stu-id="6dc0b-127">Requirement</span></span> | <span data-ttu-id="6dc0b-128">Значение</span><span class="sxs-lookup"><span data-stu-id="6dc0b-128">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6dc0b-129">Версия</span><span class="sxs-lookup"><span data-stu-id="6dc0b-129">Version</span></span><br/>   | <span data-ttu-id="6dc0b-130">Проигрыватель Windows Media 9 Series или более поздней версии</span><span class="sxs-lookup"><span data-stu-id="6dc0b-130">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="6dc0b-131">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="6dc0b-131">Namespace</span></span><br/> | <span data-ttu-id="6dc0b-132">**вмплиб**</span><span class="sxs-lookup"><span data-stu-id="6dc0b-132">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="6dc0b-133">Сборка</span><span class="sxs-lookup"><span data-stu-id="6dc0b-133">Assembly</span></span><br/>  | <dl> <span data-ttu-id="6dc0b-134"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="6dc0b-134"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6dc0b-135">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="6dc0b-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6dc0b-136">**Интерфейс IWMPControls3 (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="6dc0b-136">**IWMPControls3 Interface (VB and C#)**</span></span>](iwmpcontrols3--vb-and-c.md)
</dt> </dl>

 

 





