---
title: THEME. closeView
description: Метод closeView закрывает открытое представление.
ms.assetid: 37b56a7d-8031-4055-95ad-0510105e1c1f
keywords:
- Проигрыватель Windows Media THEME. closeView
topic_type:
- apiref
api_name:
- THEME.closeView
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: b39083979809fc2e747c54569db8d03298a951c6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105648652"
---
# <a name="themecloseview"></a><span data-ttu-id="385fe-104">THEME. closeView</span><span class="sxs-lookup"><span data-stu-id="385fe-104">THEME.closeView</span></span>

<span data-ttu-id="385fe-105">Метод **closeView** закрывает открытое **представление**.</span><span class="sxs-lookup"><span data-stu-id="385fe-105">The **closeView** method closes an open **VIEW**.</span></span>

``` syntax
        theme.closeView(theView)
```

## <a name="parameters"></a><span data-ttu-id="385fe-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="385fe-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="385fe-107"><span id="theView"></span><span id="theview"></span><span id="THEVIEW"></span>*севиев*</span><span class="sxs-lookup"><span data-stu-id="385fe-107"><span id="theView"></span><span id="theview"></span><span id="THEVIEW"></span>*theView*</span></span>
</dt> <dd>

<span data-ttu-id="385fe-108">**Строка** , указывающая **идентификатор** закрытого **представления** .</span><span class="sxs-lookup"><span data-stu-id="385fe-108">A **String** specifying the **id** of the **VIEW** to close.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="385fe-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="385fe-109">Return Value</span></span>

<span data-ttu-id="385fe-110">Этот метод не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="385fe-110">This method does not return a value.</span></span>

## <a name="examples"></a><span data-ttu-id="385fe-111">Примеры</span><span class="sxs-lookup"><span data-stu-id="385fe-111">Examples</span></span>


```C++
<THEME>
  <VIEW>
    <TEXT value="open" 
        onclick="jscript:theme.openView('newView')"/>
    <TEXT top="30" value="close"
        onclick="jscript:theme.closeView('newView')"/>
  </VIEW>
  <VIEW id="newView"/>
</THEME>
```



## <a name="requirements"></a><span data-ttu-id="385fe-112">Требования</span><span class="sxs-lookup"><span data-stu-id="385fe-112">Requirements</span></span>



| <span data-ttu-id="385fe-113">Требование</span><span class="sxs-lookup"><span data-stu-id="385fe-113">Requirement</span></span> | <span data-ttu-id="385fe-114">Значение</span><span class="sxs-lookup"><span data-stu-id="385fe-114">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="385fe-115">Версия</span><span class="sxs-lookup"><span data-stu-id="385fe-115">Version</span></span><br/> | <span data-ttu-id="385fe-116">Проигрыватель Windows Media версии 7,0 или более поздней</span><span class="sxs-lookup"><span data-stu-id="385fe-116">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="385fe-117">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="385fe-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="385fe-118">**Элемент THEME**</span><span class="sxs-lookup"><span data-stu-id="385fe-118">**THEME Element**</span></span>](theme-element.md)
</dt> <dt>

[<span data-ttu-id="385fe-119">**THEME. openView**</span><span class="sxs-lookup"><span data-stu-id="385fe-119">**THEME.openView**</span></span>](theme-openview.md)
</dt> </dl>

 

 





