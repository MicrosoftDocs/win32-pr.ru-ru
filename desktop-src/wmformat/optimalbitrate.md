---
title: оптималбитрате
description: Атрибут Оптималбитрате содержит битовую скорость, с которой файл лучше воспроизводить.
ms.assetid: cd13b9b5-34d2-4ebb-9f10-3bf42dd9de81
keywords:
- Формат Windows Media Оптималбитрате
topic_type:
- apiref
api_name:
- OptimalBitrate
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ff71c6b64cbc4bf4ccc4f346e62a5eae066e78ce
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/25/2019
ms.locfileid: "105700759"
---
# <a name="optimalbitrate"></a><span data-ttu-id="bca8b-104">оптималбитрате</span><span class="sxs-lookup"><span data-stu-id="bca8b-104">OptimalBitrate</span></span>

<span data-ttu-id="bca8b-105">Атрибут **оптималбитрате** содержит битовую скорость, с которой файл лучше воспроизводить.</span><span class="sxs-lookup"><span data-stu-id="bca8b-105">The **OptimalBitrate** attribute contains the bit rate at which the file is best played.</span></span>

## <a name="global-constant"></a><span data-ttu-id="bca8b-106">Глобальная константа</span><span class="sxs-lookup"><span data-stu-id="bca8b-106">Global Constant</span></span>

<span data-ttu-id="bca8b-107">g \_ всзвмоптималбитрате</span><span class="sxs-lookup"><span data-stu-id="bca8b-107">g\_wszWMOptimalBitrate</span></span>

## <a name="data-type"></a><span data-ttu-id="bca8b-108">Тип данных</span><span class="sxs-lookup"><span data-stu-id="bca8b-108">Data Type</span></span>

<span data-ttu-id="bca8b-109">**ВМТ, \_ тип \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="bca8b-109">**WMT\_TYPE\_DWORD**</span></span>

## <a name="remarks"></a><span data-ttu-id="bca8b-110">Комментарии</span><span class="sxs-lookup"><span data-stu-id="bca8b-110">Remarks</span></span>

<span data-ttu-id="bca8b-111">Это закодированный атрибут.</span><span class="sxs-lookup"><span data-stu-id="bca8b-111">This is a coded attribute.</span></span>

<span data-ttu-id="bca8b-112">Для файлов, содержащих потоки с переменной скоростью (VBR), это значение является пиковой скоростью потока в файле.</span><span class="sxs-lookup"><span data-stu-id="bca8b-112">For files that contain variable bit rate (VBR) streams, this value is the peak bit rate for the streams in the file.</span></span> <span data-ttu-id="bca8b-113">Для файлов без VBR это значение совпадает с [**скоростью**](bit-rate.md).</span><span class="sxs-lookup"><span data-stu-id="bca8b-113">For files without VBR, this value is the same as [**Bitrate**](bit-rate.md).</span></span>

<span data-ttu-id="bca8b-114">Этот атрибут не может дублироваться на уровне файла.</span><span class="sxs-lookup"><span data-stu-id="bca8b-114">This attribute cannot be duplicated at the file level.</span></span> <span data-ttu-id="bca8b-115">Если этот атрибут используется для отдельного потока, он будет рассматриваться как пользовательские метаданные и не будет передавать его нормальные значения объектам пакета SDK Windows Media Format.</span><span class="sxs-lookup"><span data-stu-id="bca8b-115">If this attribute is used for an individual stream, it will be treated as custom metadata and will not convey its normal meaning to the objects of the Windows Media Format SDK.</span></span>

## <a name="see-also"></a><span data-ttu-id="bca8b-116">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="bca8b-116">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bca8b-117">**Список атрибутов**</span><span class="sxs-lookup"><span data-stu-id="bca8b-117">**Attribute List**</span></span>](attribute-list.md)
</dt> </dl>

 

 




