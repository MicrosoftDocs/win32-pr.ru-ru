---
title: пеаквалуе
description: Атрибут Пеаквалуе содержит 16-битное значение амплитуды, обозначающее пиковый уровень громкости звукового содержимого.
ms.assetid: 885f6d4c-661a-4681-96b6-c1a282c8bf18
keywords:
- Формат Windows Media Пеаквалуе
topic_type:
- apiref
api_name:
- PeakValue
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 37ef933ec1b10555aa4c88a24261313abb261163
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/25/2019
ms.locfileid: "105700751"
---
# <a name="peakvalue"></a><span data-ttu-id="92e08-104">пеаквалуе</span><span class="sxs-lookup"><span data-stu-id="92e08-104">PeakValue</span></span>

<span data-ttu-id="92e08-105">Атрибут **пеаквалуе** содержит 16-битное значение амплитуды, обозначающее пиковый уровень громкости звукового содержимого.</span><span class="sxs-lookup"><span data-stu-id="92e08-105">The **PeakValue** attribute contains contains a 16-bit amplitude value designating the peak volume level of audio content.</span></span> <span data-ttu-id="92e08-106">При использовании [**аверажелевел**](averagelevel.md)этот атрибут используется для нормализации.</span><span class="sxs-lookup"><span data-stu-id="92e08-106">With [**AverageLevel**](averagelevel.md), this attribute is used for normalization.</span></span> <span data-ttu-id="92e08-107">Нормализация — это процесс настройки уровня громкости воспроизведения звуковых файлов таким образом, чтобы громкость файлов воспроизведена на одном и том же уровне, а средний объем для каждого из них одинаков.</span><span class="sxs-lookup"><span data-stu-id="92e08-107">Normalization is the process of adjusting the playback volume level of audio files so that the loudest parts of files playback at the same level and the average volume for each is the same..</span></span>

## <a name="global-constant"></a><span data-ttu-id="92e08-108">Глобальная константа</span><span class="sxs-lookup"><span data-stu-id="92e08-108">Global Constant</span></span>

<span data-ttu-id="92e08-109">g \_ всзпеаквалуе</span><span class="sxs-lookup"><span data-stu-id="92e08-109">g\_wszPeakValue</span></span>

## <a name="data-type"></a><span data-ttu-id="92e08-110">Тип данных</span><span class="sxs-lookup"><span data-stu-id="92e08-110">Data Type</span></span>

<span data-ttu-id="92e08-111">**ВМТ, \_ тип \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="92e08-111">**WMT\_TYPE\_DWORD**</span></span>

## <a name="remarks"></a><span data-ttu-id="92e08-112">Комментарии</span><span class="sxs-lookup"><span data-stu-id="92e08-112">Remarks</span></span>

<span data-ttu-id="92e08-113">Этот атрибут задается объектом модуля записи на основе информации из кодека.</span><span class="sxs-lookup"><span data-stu-id="92e08-113">This attribute is set by the writer object based on information from the codec.</span></span> <span data-ttu-id="92e08-114">Значение автоматически задается только для потоков, сжатых с помощью одного из аудиокодеков Windows Media Audio.</span><span class="sxs-lookup"><span data-stu-id="92e08-114">Only streams compressed with one of the Windows Media Audio codecs have an automatically set value.</span></span>

<span data-ttu-id="92e08-115">**Пеаквалуе** не предназначен только для чтения.</span><span class="sxs-lookup"><span data-stu-id="92e08-115">**PeakValue** is not read-only.</span></span> <span data-ttu-id="92e08-116">Однако если файл будет воспроизводиться проигрывателем Windows Media, это значение изменять не следует.</span><span class="sxs-lookup"><span data-stu-id="92e08-116">However, if the file will be played by the Windows Media Player, you should not alter this value.</span></span> <span data-ttu-id="92e08-117">Проигрыватель Windows Media использует его для нормализации уровней файлов в списке воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="92e08-117">The Windows Media Player uses this for normalizing the levels of files in a playlist.</span></span>

## <a name="see-also"></a><span data-ttu-id="92e08-118">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="92e08-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="92e08-119">**Список атрибутов**</span><span class="sxs-lookup"><span data-stu-id="92e08-119">**Attribute List**</span></span>](attribute-list.md)
</dt> </dl>

 

 




