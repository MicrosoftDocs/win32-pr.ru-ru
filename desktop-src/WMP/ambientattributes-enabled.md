---
title: Амбиентаттрибутес. Enabled
description: Атрибут Enabled указывает или получает значение, обозначающее включение или отключение элемента управления.
ms.assetid: cf96ab7c-8acd-42b6-b7ca-d084a89c97e2
keywords:
- Проигрыватель Windows Media Амбиентаттрибутес. Enabled
topic_type:
- apiref
api_name:
- AmbientAttributes.enabled
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7c34d24e86118a1cca0939d535b6da6e86c2df34
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105694542"
---
# <a name="ambientattributesenabled"></a><span data-ttu-id="40803-104">Амбиентаттрибутес. Enabled</span><span class="sxs-lookup"><span data-stu-id="40803-104">AmbientAttributes.enabled</span></span>

<span data-ttu-id="40803-105">Атрибут **Enabled** указывает или получает значение, обозначающее включение или отключение элемента управления.</span><span class="sxs-lookup"><span data-stu-id="40803-105">The **enabled** attribute specifies or retrieves a value indicating whether the control is enabled or disabled.</span></span>

``` syntax
        elementID.enabled
```

## <a name="possible-values"></a><span data-ttu-id="40803-106">Возможные значения</span><span class="sxs-lookup"><span data-stu-id="40803-106">Possible Values</span></span>

<span data-ttu-id="40803-107">Этот атрибут является **логическим значением** для чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="40803-107">This attribute is a read/write **Boolean**.</span></span>



| <span data-ttu-id="40803-108">Значение</span><span class="sxs-lookup"><span data-stu-id="40803-108">Value</span></span> | <span data-ttu-id="40803-109">Описание</span><span class="sxs-lookup"><span data-stu-id="40803-109">Description</span></span>               |
|-------|---------------------------|
| <span data-ttu-id="40803-110">true</span><span class="sxs-lookup"><span data-stu-id="40803-110">true</span></span>  | <span data-ttu-id="40803-111">По умолчанию.</span><span class="sxs-lookup"><span data-stu-id="40803-111">Default.</span></span> <span data-ttu-id="40803-112">Элемент управления включен.</span><span class="sxs-lookup"><span data-stu-id="40803-112">Control enabled.</span></span> |
| <span data-ttu-id="40803-113">false</span><span class="sxs-lookup"><span data-stu-id="40803-113">false</span></span> | <span data-ttu-id="40803-114">Элемент управления отключен.</span><span class="sxs-lookup"><span data-stu-id="40803-114">Control disabled.</span></span>         |



 

## <a name="remarks"></a><span data-ttu-id="40803-115">Комментарии</span><span class="sxs-lookup"><span data-stu-id="40803-115">Remarks</span></span>

<span data-ttu-id="40803-116">Если элемент управления включен, он может иметь позицию табуляции и получит все события окружения.</span><span class="sxs-lookup"><span data-stu-id="40803-116">If the control is enabled, it can have a tab stop, and will receive all ambient events.</span></span> <span data-ttu-id="40803-117">Если эта возможность отключена, элемент управления не имеет позиции табуляции и не получает никаких запущенных в него событий внешней мыши или клавиатуры.</span><span class="sxs-lookup"><span data-stu-id="40803-117">When disabled, the control does not have a tab stop, and does not receive any ambient mouse or keyboard events fired to it.</span></span> <span data-ttu-id="40803-118">(Однако он будет по-прежнему принимать все остальные события внешнего окружения.)</span><span class="sxs-lookup"><span data-stu-id="40803-118">(However, it will continue to receive all other ambient events fired to it.)</span></span>

<span data-ttu-id="40803-119">Этот атрибут не поддерживается для элемента вложенного **представления** .</span><span class="sxs-lookup"><span data-stu-id="40803-119">This attribute is not supported for the **SUBVIEW** element.</span></span>

## <a name="requirements"></a><span data-ttu-id="40803-120">Требования</span><span class="sxs-lookup"><span data-stu-id="40803-120">Requirements</span></span>



| <span data-ttu-id="40803-121">Требование</span><span class="sxs-lookup"><span data-stu-id="40803-121">Requirement</span></span> | <span data-ttu-id="40803-122">Значение</span><span class="sxs-lookup"><span data-stu-id="40803-122">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="40803-123">Версия</span><span class="sxs-lookup"><span data-stu-id="40803-123">Version</span></span><br/> | <span data-ttu-id="40803-124">Проигрыватель Windows Media версии 7,0 или более поздней</span><span class="sxs-lookup"><span data-stu-id="40803-124">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="40803-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="40803-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="40803-126">**Атрибуты окружения**</span><span class="sxs-lookup"><span data-stu-id="40803-126">**Ambient Attributes**</span></span>](ambient-attributes.md)
</dt> </dl>

 

 





