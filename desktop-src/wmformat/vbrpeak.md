---
title: вбрпеак
description: Атрибут Вбрпеак содержит максимальную скорость потока в закодированном потоке переменной скорости (VBR).
ms.assetid: 7b735145-8235-4efb-986f-952989b739bc
keywords:
- Формат Windows Media Вбрпеак
topic_type:
- apiref
api_name:
- VBRPeak
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6e8aacb076c3e92cfa676e73e945506cc4942bf4
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/25/2019
ms.locfileid: "104069092"
---
# <a name="vbrpeak"></a><span data-ttu-id="a0e49-104">вбрпеак</span><span class="sxs-lookup"><span data-stu-id="a0e49-104">VBRPeak</span></span>

<span data-ttu-id="a0e49-105">Атрибут **вбрпеак** содержит максимальную скорость потока в закодированном потоке переменной скорости (VBR).</span><span class="sxs-lookup"><span data-stu-id="a0e49-105">The **VBRPeak** attribute contains the highest momentary bit rate in a variable bit rate (VBR) encoded stream.</span></span>

## <a name="global-constant"></a><span data-ttu-id="a0e49-106">Глобальная константа</span><span class="sxs-lookup"><span data-stu-id="a0e49-106">Global Constant</span></span>

<span data-ttu-id="a0e49-107">g \_ всзвбрпеак</span><span class="sxs-lookup"><span data-stu-id="a0e49-107">g\_wszVBRPeak</span></span>

## <a name="data-type"></a><span data-ttu-id="a0e49-108">Тип данных</span><span class="sxs-lookup"><span data-stu-id="a0e49-108">Data Type</span></span>

<span data-ttu-id="a0e49-109">**ВМТ, \_ тип \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="a0e49-109">**WMT\_TYPE\_DWORD**</span></span>

## <a name="remarks"></a><span data-ttu-id="a0e49-110">Комментарии</span><span class="sxs-lookup"><span data-stu-id="a0e49-110">Remarks</span></span>

<span data-ttu-id="a0e49-111">При доступе к интерфейсу **IWMHeaderInfo3** объекта Writer можно добавить или изменить это значение.</span><span class="sxs-lookup"><span data-stu-id="a0e49-111">When accessing the **IWMHeaderInfo3** interface of the writer object, you can add or change this value.</span></span> <span data-ttu-id="a0e49-112">В других объектах (редактор метаданных, читатель и синхронное средство чтения) это значение доступно только для чтения.</span><span class="sxs-lookup"><span data-stu-id="a0e49-112">In other objects (metadata editor, reader, and synchronous reader), this value is read-only.</span></span>

<span data-ttu-id="a0e49-113">Модуль записи автоматически записывает значение **вбрпеак** для каждого потока VBR.</span><span class="sxs-lookup"><span data-stu-id="a0e49-113">The writer automatically writes a **VBRPeak** value for each VBR stream.</span></span>

## <a name="see-also"></a><span data-ttu-id="a0e49-114">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="a0e49-114">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a0e49-115">**Список атрибутов**</span><span class="sxs-lookup"><span data-stu-id="a0e49-115">**Attribute List**</span></span>](attribute-list.md)
</dt> </dl>

 

 




