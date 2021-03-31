---
title: WM/Вмадркпеактаржет
description: Атрибут WM/Вмадркпеактаржет содержит максимальный уровень громкости, запрошенный пользователем. Это значение используется проигрывателем Windows Media для динамического контроля диапазона.
ms.assetid: 94ef5db1-34f4-4cf8-ac56-c85cca10536b
keywords:
- Формат Windows Media WM/Вмадркпеактаржет
topic_type:
- apiref
api_name:
- WM/WMADRCPeakTarget
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 55eac4ea68cd61e2cfa0b5c185dc1a4ad17e5ce8
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/25/2019
ms.locfileid: "103784146"
---
# <a name="wmwmadrcpeaktarget"></a><span data-ttu-id="97d14-105">WM/Вмадркпеактаржет</span><span class="sxs-lookup"><span data-stu-id="97d14-105">WM/WMADRCPeakTarget</span></span>

<span data-ttu-id="97d14-106">Атрибут **WM/вмадркпеактаржет** содержит максимальный уровень громкости, запрошенный пользователем.</span><span class="sxs-lookup"><span data-stu-id="97d14-106">The **WM/WMADRCPeakTarget** attribute contains the maximum volume level requested by the user.</span></span> <span data-ttu-id="97d14-107">Это значение используется проигрывателем Windows Media для динамического контроля диапазона.</span><span class="sxs-lookup"><span data-stu-id="97d14-107">This value is used by Windows Media Player for dynamic range control.</span></span>

## <a name="global-constant"></a><span data-ttu-id="97d14-108">Глобальная константа</span><span class="sxs-lookup"><span data-stu-id="97d14-108">Global Constant</span></span>

<span data-ttu-id="97d14-109">g \_ всзвмвмадркпеактаржет</span><span class="sxs-lookup"><span data-stu-id="97d14-109">g\_wszWMWMADRCPeakTarget</span></span>

## <a name="data-type"></a><span data-ttu-id="97d14-110">Тип данных</span><span class="sxs-lookup"><span data-stu-id="97d14-110">Data Type</span></span>

<span data-ttu-id="97d14-111">**ВМТ, \_ тип \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="97d14-111">**WMT\_TYPE\_DWORD**</span></span>

## <a name="remarks"></a><span data-ttu-id="97d14-112">Комментарии</span><span class="sxs-lookup"><span data-stu-id="97d14-112">Remarks</span></span>

<span data-ttu-id="97d14-113">Проигрыватель Windows Media использует четыре атрибута для динамического управления диапазоном: **WM/вмадркаверажереференце**, **WM/вмадркпеакреференце**, **WM/вмадркаверажетаржет** и **WM/вмадркпеактаржет**.</span><span class="sxs-lookup"><span data-stu-id="97d14-113">There are four attributes used by Windows Media Player for dynamic range control: **WM/WMADRCAverageReference**, **WM/WMADRCPeakReference**, **WM/WMADRCAverageTarget**, and **WM/WMADRCPeakTarget**.</span></span> <span data-ttu-id="97d14-114">Все эти значения задаются модулем записи на основе информации из кодека при записи потоков с помощью кодека Windows Media Audio 9 или кодека Windows Media Audio 9 Professional.</span><span class="sxs-lookup"><span data-stu-id="97d14-114">All of these values are set by the writer based on information from the codec when writing streams with the Windows Media Audio 9 codec or Windows Media Audio 9 Professional codec.</span></span> <span data-ttu-id="97d14-115">Для средних значений устанавливается средний уровень громкости потока, а для пиковых значений — максимальный уровень громкости в потоке.</span><span class="sxs-lookup"><span data-stu-id="97d14-115">The average values are set to the average volume level of the stream, and the peak values are set to the maximum volume level in the stream.</span></span> <span data-ttu-id="97d14-116">Ссылочные значения доступны только для чтения.</span><span class="sxs-lookup"><span data-stu-id="97d14-116">The reference values are read-only.</span></span> <span data-ttu-id="97d14-117">Целевые значения задаются проигрывателем Windows Media при воспроизведении файла для записи параметров динамического управления диапазоном пользователя.</span><span class="sxs-lookup"><span data-stu-id="97d14-117">The target values are set by Windows Media Player when the file is being played to record the dynamic range control preferences of the user.</span></span>

## <a name="see-also"></a><span data-ttu-id="97d14-118">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="97d14-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="97d14-119">**Список атрибутов**</span><span class="sxs-lookup"><span data-stu-id="97d14-119">**Attribute List**</span></span>](attribute-list.md)
</dt> <dt>

[<span data-ttu-id="97d14-120">**WM/Вмадркаверажереференце**</span><span class="sxs-lookup"><span data-stu-id="97d14-120">**WM/WMADRCAverageReference**</span></span>](wm-wmadrcaveragereference.md)
</dt> <dt>

[<span data-ttu-id="97d14-121">**WM/Вмадркаверажетаржет**</span><span class="sxs-lookup"><span data-stu-id="97d14-121">**WM/WMADRCAverageTarget**</span></span>](wm-wmadrcaveragetarget.md)
</dt> <dt>

[<span data-ttu-id="97d14-122">**WM/Вмадркпеакреференце**</span><span class="sxs-lookup"><span data-stu-id="97d14-122">**WM/WMADRCPeakReference**</span></span>](wm-wmadrcpeakreference.md)
</dt> </dl>

 

 




