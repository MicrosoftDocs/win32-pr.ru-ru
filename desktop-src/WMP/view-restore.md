---
title: Просмотр. Восстановление
description: Метод Restore восстанавливает представление.
ms.assetid: 8005c14e-771b-4f20-8039-fc09869dc726
keywords:
- Просмотр. Восстановление проигрывателя Windows Media
topic_type:
- apiref
api_name:
- VIEW.restore
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: db92fc5e796acc55fe9c4faf93417d648652415e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105717943"
---
# <a name="viewrestore"></a><span data-ttu-id="a5dc5-104">Просмотр. Восстановление</span><span class="sxs-lookup"><span data-stu-id="a5dc5-104">VIEW.restore</span></span>

<span data-ttu-id="a5dc5-105">Метод **RESTORE** восстанавливает **представление**.</span><span class="sxs-lookup"><span data-stu-id="a5dc5-105">The **restore** method restores the **VIEW**.</span></span>

``` syntax
        elementID.restore()
```

## <a name="parameters"></a><span data-ttu-id="a5dc5-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="a5dc5-106">Parameters</span></span>

<span data-ttu-id="a5dc5-107">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="a5dc5-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="a5dc5-108">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="a5dc5-108">Return Value</span></span>

<span data-ttu-id="a5dc5-109">Этот метод не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="a5dc5-109">This method does not return a value.</span></span>

## <a name="examples"></a><span data-ttu-id="a5dc5-110">Примеры</span><span class="sxs-lookup"><span data-stu-id="a5dc5-110">Examples</span></span>


```JScript
<THEME>
  <VIEW id="View1">
    <BUTTON id="Open" image="Open.png" 
        onclick="jscript:View1.restore()">
    </BUTTON>
  </VIEW>
</THEME>
```



## <a name="requirements"></a><span data-ttu-id="a5dc5-111">Требования</span><span class="sxs-lookup"><span data-stu-id="a5dc5-111">Requirements</span></span>



| <span data-ttu-id="a5dc5-112">Требование</span><span class="sxs-lookup"><span data-stu-id="a5dc5-112">Requirement</span></span> | <span data-ttu-id="a5dc5-113">Значение</span><span class="sxs-lookup"><span data-stu-id="a5dc5-113">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="a5dc5-114">Версия</span><span class="sxs-lookup"><span data-stu-id="a5dc5-114">Version</span></span><br/> | <span data-ttu-id="a5dc5-115">Проигрыватель Windows Media версии 7,0 или более поздней</span><span class="sxs-lookup"><span data-stu-id="a5dc5-115">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="a5dc5-116">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="a5dc5-116">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a5dc5-117">**VIEW, элемент**</span><span class="sxs-lookup"><span data-stu-id="a5dc5-117">**VIEW Element**</span></span>](view-element.md)
</dt> </dl>

 

 





