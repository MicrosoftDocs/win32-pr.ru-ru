---
title: куррентбитрате
description: Атрибут Куррентбитрате содержит текущую общую скорость потока активных потоков в файле.
ms.assetid: 961f36d5-a408-40d9-9ca1-0ed7c484858f
keywords:
- Формат Windows Media Куррентбитрате
topic_type:
- apiref
api_name:
- CurrentBitrate
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bdcd8db7d60c65bcb7ceedcac4498ac650f90d9a
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/25/2019
ms.locfileid: "105710207"
---
# <a name="currentbitrate"></a><span data-ttu-id="a7854-104">куррентбитрате</span><span class="sxs-lookup"><span data-stu-id="a7854-104">CurrentBitrate</span></span>

<span data-ttu-id="a7854-105">Атрибут Куррентбитрате содержит текущую общую скорость потока активных потоков в файле.</span><span class="sxs-lookup"><span data-stu-id="a7854-105">The CurrentBitrate attribute contains the current total bit rate of the active streams in the file.</span></span>

## <a name="global-constant"></a><span data-ttu-id="a7854-106">Глобальная константа</span><span class="sxs-lookup"><span data-stu-id="a7854-106">Global Constant</span></span>

<span data-ttu-id="a7854-107">g \_ всзвмкуррентбитрате</span><span class="sxs-lookup"><span data-stu-id="a7854-107">g\_wszWMCurrentBitrate</span></span>

## <a name="data-type"></a><span data-ttu-id="a7854-108">Тип данных</span><span class="sxs-lookup"><span data-stu-id="a7854-108">Data Type</span></span>

<span data-ttu-id="a7854-109">**ВМТ, \_ тип \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="a7854-109">**WMT\_TYPE\_DWORD**</span></span>

## <a name="remarks"></a><span data-ttu-id="a7854-110">Комментарии</span><span class="sxs-lookup"><span data-stu-id="a7854-110">Remarks</span></span>

<span data-ttu-id="a7854-111">Это закодированный атрибут.</span><span class="sxs-lookup"><span data-stu-id="a7854-111">This is a coded attribute.</span></span>

<span data-ttu-id="a7854-112">Значение, полученное для **куррентбитрате** , отличается в зависимости от используемого объекта.</span><span class="sxs-lookup"><span data-stu-id="a7854-112">The value retrieved for **CurrentBitrate** is different depending upon the object used.</span></span> <span data-ttu-id="a7854-113">В объекте чтения или синхронном модуле чтения значение представляет собой реальную скорость потока во время вызова.</span><span class="sxs-lookup"><span data-stu-id="a7854-113">In the reader or synchronous reader object, the value is the actual bit rate at the time of the call.</span></span> <span data-ttu-id="a7854-114">В объекте редактора метаданных значение является средней скоростью потока файла.</span><span class="sxs-lookup"><span data-stu-id="a7854-114">In the metadata editor object, the value is the average bit rate of the file.</span></span>

<span data-ttu-id="a7854-115">Фактическая скорость потока в файле равна скорости потока всех активных потоков плюс некоторые издержки.</span><span class="sxs-lookup"><span data-stu-id="a7854-115">The actual bit rate of a file is equal to the bit rates of all active streams plus some overhead.</span></span> <span data-ttu-id="a7854-116">Это значение, например, отображаемое при воспроизведении файла с помощью проигрывателя Windows Media.</span><span class="sxs-lookup"><span data-stu-id="a7854-116">This is the value that is, for example, displayed when playing a file with the Windows Media Player.</span></span>

<span data-ttu-id="a7854-117">Этот атрибут не может дублироваться на уровне файла.</span><span class="sxs-lookup"><span data-stu-id="a7854-117">This attribute cannot be duplicated at the file level.</span></span> <span data-ttu-id="a7854-118">Если этот атрибут используется для отдельного потока, он будет рассматриваться как пользовательские метаданные и не будет передавать его нормальные значения объектам пакета SDK Windows Media Format.</span><span class="sxs-lookup"><span data-stu-id="a7854-118">If this attribute is used for an individual stream, it will be treated as custom metadata and will not convey its normal meaning to the objects of the Windows Media Format SDK.</span></span>

## <a name="see-also"></a><span data-ttu-id="a7854-119">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="a7854-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a7854-120">**Список атрибутов**</span><span class="sxs-lookup"><span data-stu-id="a7854-120">**Attribute List**</span></span>](attribute-list.md)
</dt> </dl>

 

 




