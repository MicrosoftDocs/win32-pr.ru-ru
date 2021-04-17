---
title: Ерроритем. Condition
description: Свойство Condition извлекает значение, указывающее условие для ошибки.
ms.assetid: efb54b48-cfaa-479f-9ee6-ce6724dca24c
keywords:
- Проигрыватель Windows Media Ерроритем. Condition
topic_type:
- apiref
api_name:
- ErrorItem.condition
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c498e7479a7a3e067dea2d8a562800351effd672
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105698968"
---
# <a name="erroritemcondition"></a><span data-ttu-id="f03d5-104">Ерроритем. Condition</span><span class="sxs-lookup"><span data-stu-id="f03d5-104">ErrorItem.condition</span></span>

<span data-ttu-id="f03d5-105">Свойство **Condition** извлекает значение, указывающее условие для ошибки.</span><span class="sxs-lookup"><span data-stu-id="f03d5-105">The **condition** property retrieves a value indicating the condition for the error.</span></span>

``` syntax
player.error.item(
        index
        ).condition
      
```

## <a name="possible-values"></a><span data-ttu-id="f03d5-106">Возможные значения</span><span class="sxs-lookup"><span data-stu-id="f03d5-106">Possible Values</span></span>

<span data-ttu-id="f03d5-107">Это свойство является **числом** только для чтения (**длинное**), представляющим код условия.</span><span class="sxs-lookup"><span data-stu-id="f03d5-107">This property is a read-only **Number** (**long**) that represents the condition code.</span></span>

## <a name="remarks"></a><span data-ttu-id="f03d5-108">Комментарии</span><span class="sxs-lookup"><span data-stu-id="f03d5-108">Remarks</span></span>

<span data-ttu-id="f03d5-109">Код условия — это значение, которое используется корпорацией Майкрософт для предоставления дополнительных сведений сотрудникам службы технической поддержки.</span><span class="sxs-lookup"><span data-stu-id="f03d5-109">The condition code is a value that is used by Microsoft to provide additional information for technical support personnel.</span></span>

<span data-ttu-id="f03d5-110">**Проигрыватель Windows Media 10 Mobile:** Это свойство всегда возвращает значение 0.</span><span class="sxs-lookup"><span data-stu-id="f03d5-110">**Windows Media Player 10 Mobile:** This property always returns 0.</span></span>

## <a name="requirements"></a><span data-ttu-id="f03d5-111">Требования</span><span class="sxs-lookup"><span data-stu-id="f03d5-111">Requirements</span></span>



| <span data-ttu-id="f03d5-112">Требование</span><span class="sxs-lookup"><span data-stu-id="f03d5-112">Requirement</span></span> | <span data-ttu-id="f03d5-113">Значение</span><span class="sxs-lookup"><span data-stu-id="f03d5-113">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="f03d5-114">Версия</span><span class="sxs-lookup"><span data-stu-id="f03d5-114">Version</span></span><br/> | <span data-ttu-id="f03d5-115">Проигрыватель Windows Media 9 Series или более поздней версии.</span><span class="sxs-lookup"><span data-stu-id="f03d5-115">Windows Media Player 9 Series or later.</span></span><br/>                                 |
| <span data-ttu-id="f03d5-116">DLL</span><span class="sxs-lookup"><span data-stu-id="f03d5-116">DLL</span></span><br/>     | <dl> <span data-ttu-id="f03d5-117"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f03d5-117"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f03d5-118">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="f03d5-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f03d5-119">**Объект Ерроритем**</span><span class="sxs-lookup"><span data-stu-id="f03d5-119">**ErrorItem Object**</span></span>](erroritem-object.md)
</dt> </dl>

 

 





