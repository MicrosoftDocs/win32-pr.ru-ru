---
title: WM/Вмадркаверажереференце
description: Атрибут WM/Вмадркаверажереференце содержит средний уровень громкости файла в кодировке.
ms.assetid: 994614e3-06e2-48f0-bdac-6de5ab0c0eff
keywords:
- Формат Windows Media WM/Вмадркаверажереференце
topic_type:
- apiref
api_name:
- WM/WMADRCAverageReference
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d7059b68658d070ca71a738a5e20658474139558
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/25/2019
ms.locfileid: "105700765"
---
# <a name="wmwmadrcaveragereference"></a><span data-ttu-id="0a051-104">WM/Вмадркаверажереференце</span><span class="sxs-lookup"><span data-stu-id="0a051-104">WM/WMADRCAverageReference</span></span>

<span data-ttu-id="0a051-105">Атрибут **WM/вмадркаверажереференце** содержит средний уровень громкости файла в кодировке.</span><span class="sxs-lookup"><span data-stu-id="0a051-105">The **WM/WMADRCAverageReference** attribute contains the average volume level of the file as encoded.</span></span>

## <a name="global-constant"></a><span data-ttu-id="0a051-106">Глобальная константа</span><span class="sxs-lookup"><span data-stu-id="0a051-106">Global Constant</span></span>

<span data-ttu-id="0a051-107">g \_ всзвмвмадркаверажереференце</span><span class="sxs-lookup"><span data-stu-id="0a051-107">g\_wszWMWMADRCAverageReference</span></span>

## <a name="data-type"></a><span data-ttu-id="0a051-108">Тип данных</span><span class="sxs-lookup"><span data-stu-id="0a051-108">Data Type</span></span>

<span data-ttu-id="0a051-109">**ВМТ, \_ тип \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="0a051-109">**WMT\_TYPE\_DWORD**</span></span>

## <a name="remarks"></a><span data-ttu-id="0a051-110">Комментарии</span><span class="sxs-lookup"><span data-stu-id="0a051-110">Remarks</span></span>

<span data-ttu-id="0a051-111">Проигрыватель Windows Media использует четыре атрибута для динамического управления диапазоном: **WM/вмадркаверажереференце**, **WM/вмадркпеакреференце**, **WM/вмадркаверажетаржет** и **WM/вмадркпеактаржет**.</span><span class="sxs-lookup"><span data-stu-id="0a051-111">There are four attributes used by Windows Media Player for dynamic range control: **WM/WMADRCAverageReference**, **WM/WMADRCPeakReference**, **WM/WMADRCAverageTarget**, and **WM/WMADRCPeakTarget**.</span></span> <span data-ttu-id="0a051-112">Все эти значения задаются модулем записи на основе информации из кодека при записи потоков с помощью кодека Windows Media Audio 9 или кодека Windows Media Audio 9 Professional.</span><span class="sxs-lookup"><span data-stu-id="0a051-112">All of these values are set by the writer based on information from the codec when writing streams with the Windows Media Audio 9 codec or Windows Media Audio 9 Professional codec.</span></span> <span data-ttu-id="0a051-113">Для средних значений устанавливается средний уровень громкости потока, а для пиковых значений — максимальный уровень громкости в потоке.</span><span class="sxs-lookup"><span data-stu-id="0a051-113">The average values are set to the average volume level of the stream, and the peak values are set to the maximum volume level in the stream.</span></span> <span data-ttu-id="0a051-114">Ссылочные значения доступны только для чтения.</span><span class="sxs-lookup"><span data-stu-id="0a051-114">The reference values are read-only.</span></span> <span data-ttu-id="0a051-115">Целевые значения задаются проигрывателем Windows Media при воспроизведении файла для записи параметров динамического управления диапазоном пользователя.</span><span class="sxs-lookup"><span data-stu-id="0a051-115">The target values are set by Windows Media Player when the file is being played to record the dynamic range control preferences of the user.</span></span>

## <a name="see-also"></a><span data-ttu-id="0a051-116">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="0a051-116">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0a051-117">**Список атрибутов**</span><span class="sxs-lookup"><span data-stu-id="0a051-117">**Attribute List**</span></span>](attribute-list.md)
</dt> <dt>

[<span data-ttu-id="0a051-118">**WM/Вмадркаверажетаржет**</span><span class="sxs-lookup"><span data-stu-id="0a051-118">**WM/WMADRCAverageTarget**</span></span>](wm-wmadrcaveragetarget.md)
</dt> <dt>

[<span data-ttu-id="0a051-119">**WM/Вмадркпеакреференце**</span><span class="sxs-lookup"><span data-stu-id="0a051-119">**WM/WMADRCPeakReference**</span></span>](wm-wmadrcpeakreference.md)
</dt> <dt>

[<span data-ttu-id="0a051-120">**WM/Вмадркпеактаржет**</span><span class="sxs-lookup"><span data-stu-id="0a051-120">**WM/WMADRCPeakTarget**</span></span>](wm-wmadrcpeaktarget.md)
</dt> </dl>

 

 




