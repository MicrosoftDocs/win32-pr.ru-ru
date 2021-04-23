---
title: WM/Track
description: Атрибут WM/Track содержит номер записи для содержимого. Этот атрибут отсчитывается от нуля и поддерживается для обеспечения обратной совместимости. В новом содержимом вместо него следует использовать атрибут WM/Траккнумбер.
ms.assetid: c763d7b0-9d12-4a4e-8c9f-9cf67bd2a02b
keywords:
- WM/Track Windows Media Format
topic_type:
- apiref
api_name:
- WM/Track
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 244426175ea74bc0281f8822964c2fc0bfa37aa7
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/25/2019
ms.locfileid: "104411541"
---
# <a name="wmtrack"></a><span data-ttu-id="ddb30-106">WM/Track</span><span class="sxs-lookup"><span data-stu-id="ddb30-106">WM/Track</span></span>

<span data-ttu-id="ddb30-107">Атрибут **WM/Track** содержит номер записи для содержимого.</span><span class="sxs-lookup"><span data-stu-id="ddb30-107">The **WM/Track** attribute contains the track number of the content.</span></span> <span data-ttu-id="ddb30-108">Этот атрибут отсчитывается от нуля и поддерживается для обеспечения обратной совместимости.</span><span class="sxs-lookup"><span data-stu-id="ddb30-108">This attribute is zero-based and is supported for backward compatibility.</span></span> <span data-ttu-id="ddb30-109">В новом содержимом вместо него следует использовать атрибут [**WM/траккнумбер**](wm-tracknumber.md) .</span><span class="sxs-lookup"><span data-stu-id="ddb30-109">New content should use the [**WM/TrackNumber**](wm-tracknumber.md) attribute instead.</span></span>

## <a name="global-constant"></a><span data-ttu-id="ddb30-110">Глобальная константа</span><span class="sxs-lookup"><span data-stu-id="ddb30-110">Global Constant</span></span>

<span data-ttu-id="ddb30-111">g \_ всзвмтракк</span><span class="sxs-lookup"><span data-stu-id="ddb30-111">g\_wszWMTrack</span></span>

## <a name="data-type"></a><span data-ttu-id="ddb30-112">Тип данных</span><span class="sxs-lookup"><span data-stu-id="ddb30-112">Data Type</span></span>

<span data-ttu-id="ddb30-113">**\_Строка типа \_ ВМТ**</span><span class="sxs-lookup"><span data-stu-id="ddb30-113">**WMT\_TYPE\_STRING**</span></span>

## <a name="remarks"></a><span data-ttu-id="ddb30-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="ddb30-114">Remarks</span></span>

<span data-ttu-id="ddb30-115">Многие существующие приложения записывают значение для **WM/Track** как **DWORD**.</span><span class="sxs-lookup"><span data-stu-id="ddb30-115">Many existing applications write the value for **WM/Track** as a **DWORD**.</span></span> <span data-ttu-id="ddb30-116">При создании приложения, которое воспроизводит файлы из неизвестных источников, необходимо включить код, обрабатывающий значения String и **DWORD** .</span><span class="sxs-lookup"><span data-stu-id="ddb30-116">If you create an application that plays files from unknown sources, you should include code to handle both string and **DWORD** values.</span></span>

## <a name="see-also"></a><span data-ttu-id="ddb30-117">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="ddb30-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ddb30-118">**Список атрибутов**</span><span class="sxs-lookup"><span data-stu-id="ddb30-118">**Attribute List**</span></span>](attribute-list.md)
</dt> </dl>

 

 




