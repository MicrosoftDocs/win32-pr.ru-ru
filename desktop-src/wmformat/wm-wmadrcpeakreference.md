---
title: WM/Вмадркпеакреференце
description: Атрибут WM/Вмадркпеакреференце содержит максимальный уровень громкости файла в кодировке. Это значение используется проигрывателем Windows Media для динамического контроля диапазона. Это значение задается кодеком и доступно только для чтения.
ms.assetid: c732ee88-437b-4970-8f17-61aed2d91022
keywords:
- Формат Windows Media WM/Вмадркпеакреференце
topic_type:
- apiref
api_name:
- WM/WMADRCPeakReference
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 59660f950c748c45a1affccee10ae86e38998f23
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/25/2019
ms.locfileid: "104411856"
---
# <a name="wmwmadrcpeakreference"></a><span data-ttu-id="9da75-106">WM/Вмадркпеакреференце</span><span class="sxs-lookup"><span data-stu-id="9da75-106">WM/WMADRCPeakReference</span></span>

<span data-ttu-id="9da75-107">Атрибут **WM/вмадркпеакреференце** содержит максимальный уровень громкости файла в кодировке.</span><span class="sxs-lookup"><span data-stu-id="9da75-107">The **WM/WMADRCPeakReference** attribute contains the maximum volume level of the file as encoded.</span></span> <span data-ttu-id="9da75-108">Это значение используется проигрывателем Windows Media для динамического контроля диапазона.</span><span class="sxs-lookup"><span data-stu-id="9da75-108">This value is used by Windows Media Player for dynamic range control.</span></span> <span data-ttu-id="9da75-109">Это значение задается кодеком и доступно только для чтения.</span><span class="sxs-lookup"><span data-stu-id="9da75-109">This value is set by the codec and is read-only.</span></span>

## <a name="global-constant"></a><span data-ttu-id="9da75-110">Глобальная константа</span><span class="sxs-lookup"><span data-stu-id="9da75-110">Global Constant</span></span>

<span data-ttu-id="9da75-111">g \_ всзвмвмадркпеакреференце</span><span class="sxs-lookup"><span data-stu-id="9da75-111">g\_wszWMWMADRCPeakReference</span></span>

## <a name="data-type"></a><span data-ttu-id="9da75-112">Тип данных</span><span class="sxs-lookup"><span data-stu-id="9da75-112">Data Type</span></span>

<span data-ttu-id="9da75-113">**ВМТ, \_ тип \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="9da75-113">**WMT\_TYPE\_DWORD**</span></span>

## <a name="remarks"></a><span data-ttu-id="9da75-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="9da75-114">Remarks</span></span>

<span data-ttu-id="9da75-115">Проигрыватель Windows Media использует четыре атрибута для динамического управления диапазоном: **WM/вмадркаверажереференце**, **WM/вмадркпеакреференце**, **WM/вмадркаверажетаржет** и **WM/вмадркпеактаржет**.</span><span class="sxs-lookup"><span data-stu-id="9da75-115">There are four attributes used by Windows Media Player for dynamic range control: **WM/WMADRCAverageReference**, **WM/WMADRCPeakReference**, **WM/WMADRCAverageTarget**, and **WM/WMADRCPeakTarget**.</span></span> <span data-ttu-id="9da75-116">Все эти значения задаются модулем записи на основе информации из кодека при записи потоков с помощью кодека Windows Media Audio 9 или кодека Windows Media Audio 9 Professional.</span><span class="sxs-lookup"><span data-stu-id="9da75-116">All of these values are set by the writer based on information from the codec when writing streams with the Windows Media Audio 9 codec or Windows Media Audio 9 Professional codec.</span></span> <span data-ttu-id="9da75-117">Для средних значений устанавливается средний уровень громкости потока, а для пиковых значений — максимальный уровень громкости в потоке.</span><span class="sxs-lookup"><span data-stu-id="9da75-117">The average values are set to the average volume level of the stream, and the peak values are set to the maximum volume level in the stream.</span></span> <span data-ttu-id="9da75-118">Ссылочные значения доступны только для чтения.</span><span class="sxs-lookup"><span data-stu-id="9da75-118">The reference values are read-only.</span></span> <span data-ttu-id="9da75-119">Целевые значения задаются проигрывателем Windows Media при воспроизведении файла для записи параметров динамического управления диапазоном пользователя.</span><span class="sxs-lookup"><span data-stu-id="9da75-119">The target values are set by Windows Media Player when the file is being played to record the dynamic range control preferences of the user.</span></span>

## <a name="see-also"></a><span data-ttu-id="9da75-120">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="9da75-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9da75-121">**Список атрибутов**</span><span class="sxs-lookup"><span data-stu-id="9da75-121">**Attribute List**</span></span>](attribute-list.md)
</dt> <dt>

[<span data-ttu-id="9da75-122">**WM/Вмадркаверажереференце**</span><span class="sxs-lookup"><span data-stu-id="9da75-122">**WM/WMADRCAverageReference**</span></span>](wm-wmadrcaveragereference.md)
</dt> <dt>

[<span data-ttu-id="9da75-123">**WM/Вмадркаверажетаржет**</span><span class="sxs-lookup"><span data-stu-id="9da75-123">**WM/WMADRCAverageTarget**</span></span>](wm-wmadrcaveragetarget.md)
</dt> <dt>

[<span data-ttu-id="9da75-124">**WM/Вмадркпеактаржет**</span><span class="sxs-lookup"><span data-stu-id="9da75-124">**WM/WMADRCPeakTarget**</span></span>](wm-wmadrcpeaktarget.md)
</dt> </dl>

 

 




