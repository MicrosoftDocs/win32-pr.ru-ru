---
title: WM/Вмадркаверажетаржет
description: Атрибут WM/Вмадркаверажетаржет содержит средний уровень громкости, запрошенный пользователем. Это значение используется проигрывателем Windows Media для динамического контроля диапазона.
ms.assetid: 8173b5ab-27e4-4af9-aea8-6c1310f065f5
keywords:
- Формат Windows Media WM/Вмадркаверажетаржет
topic_type:
- apiref
api_name:
- WM/WMADRCAverageTarget
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 387eed9112e8e0d79943b99bf326b07f42f425d1
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/25/2019
ms.locfileid: "105691420"
---
# <a name="wmwmadrcaveragetarget"></a><span data-ttu-id="9f917-105">WM/Вмадркаверажетаржет</span><span class="sxs-lookup"><span data-stu-id="9f917-105">WM/WMADRCAverageTarget</span></span>

<span data-ttu-id="9f917-106">Атрибут **WM/вмадркаверажетаржет** содержит средний уровень громкости, запрошенный пользователем.</span><span class="sxs-lookup"><span data-stu-id="9f917-106">The **WM/WMADRCAverageTarget** attribute contains the average volume level requested by the user.</span></span> <span data-ttu-id="9f917-107">Это значение используется проигрывателем Windows Media для динамического контроля диапазона.</span><span class="sxs-lookup"><span data-stu-id="9f917-107">This value is used by Windows Media Player for dynamic range control.</span></span>

## <a name="global-constant"></a><span data-ttu-id="9f917-108">Глобальная константа</span><span class="sxs-lookup"><span data-stu-id="9f917-108">Global Constant</span></span>

<span data-ttu-id="9f917-109">g \_ всзвмвмадркаверажетаржет</span><span class="sxs-lookup"><span data-stu-id="9f917-109">g\_wszWMWMADRCAverageTarget</span></span>

## <a name="data-type"></a><span data-ttu-id="9f917-110">Тип данных</span><span class="sxs-lookup"><span data-stu-id="9f917-110">Data Type</span></span>

<span data-ttu-id="9f917-111">**ВМТ, \_ тип \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="9f917-111">**WMT\_TYPE\_DWORD**</span></span>

## <a name="remarks"></a><span data-ttu-id="9f917-112">Комментарии</span><span class="sxs-lookup"><span data-stu-id="9f917-112">Remarks</span></span>

<span data-ttu-id="9f917-113">Проигрыватель Windows Media использует четыре атрибута для динамического управления диапазоном: **WM/вмадркаверажереференце**, **WM/вмадркпеакреференце**, **WM/вмадркаверажетаржет** и **WM/вмадркпеактаржет**.</span><span class="sxs-lookup"><span data-stu-id="9f917-113">There are four attributes used by Windows Media Player for dynamic range control: **WM/WMADRCAverageReference**, **WM/WMADRCPeakReference**, **WM/WMADRCAverageTarget**, and **WM/WMADRCPeakTarget**.</span></span> <span data-ttu-id="9f917-114">Все эти значения задаются модулем записи на основе информации из кодека при записи потоков с помощью кодека Windows Media Audio 9 или кодека Windows Media Audio 9 Professional.</span><span class="sxs-lookup"><span data-stu-id="9f917-114">All of these values are set by the writer based on information from the codec when writing streams with the Windows Media Audio 9 codec or Windows Media Audio 9 Professional codec.</span></span> <span data-ttu-id="9f917-115">Для средних значений устанавливается средний уровень громкости потока, а для пиковых значений — максимальный уровень громкости в потоке.</span><span class="sxs-lookup"><span data-stu-id="9f917-115">The average values are set to the average volume level of the stream, and the peak values are set to the maximum volume level in the stream.</span></span> <span data-ttu-id="9f917-116">Ссылочные значения доступны только для чтения.</span><span class="sxs-lookup"><span data-stu-id="9f917-116">The reference values are read-only.</span></span> <span data-ttu-id="9f917-117">Целевые значения задаются проигрывателем Windows Media при воспроизведении файла для записи параметров динамического управления диапазоном пользователя.</span><span class="sxs-lookup"><span data-stu-id="9f917-117">The target values are set by Windows Media Player when the file is being played to record the dynamic range control preferences of the user.</span></span>

## <a name="see-also"></a><span data-ttu-id="9f917-118">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="9f917-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9f917-119">**Список атрибутов**</span><span class="sxs-lookup"><span data-stu-id="9f917-119">**Attribute List**</span></span>](attribute-list.md)
</dt> <dt>

[<span data-ttu-id="9f917-120">**WM/Вмадркаверажереференце**</span><span class="sxs-lookup"><span data-stu-id="9f917-120">**WM/WMADRCAverageReference**</span></span>](wm-wmadrcaveragereference.md)
</dt> <dt>

[<span data-ttu-id="9f917-121">**WM/Вмадркпеакреференце**</span><span class="sxs-lookup"><span data-stu-id="9f917-121">**WM/WMADRCPeakReference**</span></span>](wm-wmadrcpeakreference.md)
</dt> <dt>

[<span data-ttu-id="9f917-122">**WM/Вмадркпеактаржет**</span><span class="sxs-lookup"><span data-stu-id="9f917-122">**WM/WMADRCPeakTarget**</span></span>](wm-wmadrcpeaktarget.md)
</dt> </dl>

 

 




