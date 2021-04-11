---
title: буфферавераже
description: Атрибут Буфферавераже содержит средний размер буфера, необходимый для потока с переменной скоростью (VBR).
ms.assetid: 5fd69534-6655-4c98-bf07-a694585fc9ae
keywords:
- Формат Windows Media Буфферавераже
topic_type:
- apiref
api_name:
- BufferAverage
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ce5767ed329fde43cc1022af54d937fc99e0e323
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/25/2019
ms.locfileid: "104133219"
---
# <a name="bufferaverage"></a><span data-ttu-id="aa9d7-104">буфферавераже</span><span class="sxs-lookup"><span data-stu-id="aa9d7-104">BufferAverage</span></span>

<span data-ttu-id="aa9d7-105">Атрибут **буфферавераже** содержит средний размер буфера, необходимый для потока с переменной СКОРОСТЬЮ (VBR).</span><span class="sxs-lookup"><span data-stu-id="aa9d7-105">The **BufferAverage** attribute contains the average buffer size needed for a variable bit rate (VBR) stream.</span></span>

## <a name="global-constant"></a><span data-ttu-id="aa9d7-106">Глобальная константа</span><span class="sxs-lookup"><span data-stu-id="aa9d7-106">Global Constant</span></span>

<span data-ttu-id="aa9d7-107">g \_ всзбуфферавераже</span><span class="sxs-lookup"><span data-stu-id="aa9d7-107">g\_wszBufferAverage</span></span>

## <a name="data-type"></a><span data-ttu-id="aa9d7-108">Тип данных</span><span class="sxs-lookup"><span data-stu-id="aa9d7-108">Data Type</span></span>

<span data-ttu-id="aa9d7-109">**ВМТ, \_ тип \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="aa9d7-109">**WMT\_TYPE\_DWORD**</span></span>

## <a name="remarks"></a><span data-ttu-id="aa9d7-110">Комментарии</span><span class="sxs-lookup"><span data-stu-id="aa9d7-110">Remarks</span></span>

<span data-ttu-id="aa9d7-111">При доступе к интерфейсу **IWMHeaderInfo3** объекта Writer можно добавить или изменить это значение.</span><span class="sxs-lookup"><span data-stu-id="aa9d7-111">When accessing the **IWMHeaderInfo3** interface of the writer object, you can add or change this value.</span></span> <span data-ttu-id="aa9d7-112">В других объектах (редактор метаданных, читатель и синхронное средство чтения) это значение доступно только для чтения.</span><span class="sxs-lookup"><span data-stu-id="aa9d7-112">In other objects (metadata editor, reader, and synchronous reader), this value is read-only.</span></span>

<span data-ttu-id="aa9d7-113">Модуль записи автоматически записывает значение **буфферавераже** для каждого потока VBR.</span><span class="sxs-lookup"><span data-stu-id="aa9d7-113">The writer automatically writes a **BufferAverage** value for each VBR stream.</span></span>

## <a name="see-also"></a><span data-ttu-id="aa9d7-114">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="aa9d7-114">See also</span></span>

<dl> <dt>

[<span data-ttu-id="aa9d7-115">**Список атрибутов**</span><span class="sxs-lookup"><span data-stu-id="aa9d7-115">**Attribute List**</span></span>](attribute-list.md)
</dt> </dl>

 

 




