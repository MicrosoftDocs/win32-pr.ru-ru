---
title: аверажелевел
description: Атрибут Аверажелевел содержит 16-битное значение амплитуды, обозначающее средний уровень громкости звукового содержимого.
ms.assetid: e6270ac8-5de3-4dee-824c-ba25fdd272c8
keywords:
- Формат Windows Media Аверажелевел
topic_type:
- apiref
api_name:
- AverageLevel
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 632379e42fa6c64e44018173b9d40340add4ee61
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/25/2019
ms.locfileid: "104068975"
---
# <a name="averagelevel"></a><span data-ttu-id="fa65b-104">аверажелевел</span><span class="sxs-lookup"><span data-stu-id="fa65b-104">AverageLevel</span></span>

<span data-ttu-id="fa65b-105">Атрибут **аверажелевел** содержит 16-битное значение амплитуды, обозначающее средний уровень громкости звукового содержимого.</span><span class="sxs-lookup"><span data-stu-id="fa65b-105">The **AverageLevel** attribute contains a 16-bit amplitude value designating the average volume level of audio content.</span></span> <span data-ttu-id="fa65b-106">При использовании [**пеаквалуе**](peakvalue.md)этот атрибут используется для нормализации.</span><span class="sxs-lookup"><span data-stu-id="fa65b-106">With [**PeakValue**](peakvalue.md), this attribute is used for normalization.</span></span> <span data-ttu-id="fa65b-107">Нормализация — это процесс настройки уровня громкости воспроизведения звуковых файлов таким образом, чтобы воспроизводимые громкими частями файлов на одном уровне и средним объемом для каждого из них совпадали.</span><span class="sxs-lookup"><span data-stu-id="fa65b-107">Normalization is the process of adjusting the playback volume level of audio files so that the loudest parts of files playback at the same level and the average volume for each is the same.</span></span>

## <a name="global-constant"></a><span data-ttu-id="fa65b-108">Глобальная константа</span><span class="sxs-lookup"><span data-stu-id="fa65b-108">Global Constant</span></span>

<span data-ttu-id="fa65b-109">g \_ всзаверажелевел</span><span class="sxs-lookup"><span data-stu-id="fa65b-109">g\_wszAverageLevel</span></span>

## <a name="data-type"></a><span data-ttu-id="fa65b-110">Тип данных</span><span class="sxs-lookup"><span data-stu-id="fa65b-110">Data Type</span></span>

<span data-ttu-id="fa65b-111">**ВМТ, \_ тип \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="fa65b-111">**WMT\_TYPE\_DWORD**</span></span>

## <a name="remarks"></a><span data-ttu-id="fa65b-112">Комментарии</span><span class="sxs-lookup"><span data-stu-id="fa65b-112">Remarks</span></span>

<span data-ttu-id="fa65b-113">Этот атрибут задается объектом модуля записи на основе информации из кодека.</span><span class="sxs-lookup"><span data-stu-id="fa65b-113">This attribute is set by the writer object based on information from the codec.</span></span> <span data-ttu-id="fa65b-114">Значение автоматически задается только для потоков, сжатых с помощью одного из аудиокодеков Windows Media Audio.</span><span class="sxs-lookup"><span data-stu-id="fa65b-114">Only streams compressed with one of the Windows Media Audio codecs have an automatically set value.</span></span>

<span data-ttu-id="fa65b-115">**Аверажелевел** не предназначен только для чтения.</span><span class="sxs-lookup"><span data-stu-id="fa65b-115">**AverageLevel** is not read-only.</span></span> <span data-ttu-id="fa65b-116">Однако если файл будет воспроизводиться проигрывателем Windows Media, это значение изменять не следует.</span><span class="sxs-lookup"><span data-stu-id="fa65b-116">However, if the file will be played by the Windows Media Player, you should not alter this value.</span></span> <span data-ttu-id="fa65b-117">Проигрыватель Windows Media использует его для нормализации уровней файлов в списке воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="fa65b-117">The Windows Media Player uses this for normalizing the levels of files in a playlist.</span></span>

## <a name="see-also"></a><span data-ttu-id="fa65b-118">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="fa65b-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fa65b-119">**Список атрибутов**</span><span class="sxs-lookup"><span data-stu-id="fa65b-119">**Attribute List**</span></span>](attribute-list.md)
</dt> </dl>

 

 




