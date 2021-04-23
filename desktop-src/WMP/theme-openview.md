---
title: THEME. openView
description: Метод openView открывает представление в новом окне.
ms.assetid: 2aa63c29-dafe-4942-a010-076f1503862b
keywords:
- Проигрыватель Windows Media THEME. openView
topic_type:
- apiref
api_name:
- THEME.openView
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: d66ff2cf47004c7687a37f1f22a87bdeb534d344
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105675560"
---
# <a name="themeopenview"></a><span data-ttu-id="92fee-104">THEME. openView</span><span class="sxs-lookup"><span data-stu-id="92fee-104">THEME.openView</span></span>

<span data-ttu-id="92fee-105">Метод **openView** открывает **представление** в новом окне.</span><span class="sxs-lookup"><span data-stu-id="92fee-105">The **openView** method opens a **VIEW** in a new window.</span></span>

``` syntax
        theme.openView(view)
```

## <a name="parameters"></a><span data-ttu-id="92fee-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="92fee-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="92fee-107"><span id="view"></span><span id="VIEW"></span>*режиме*</span><span class="sxs-lookup"><span data-stu-id="92fee-107"><span id="view"></span><span id="VIEW"></span>*view*</span></span>
</dt> <dd>

<span data-ttu-id="92fee-108">**Строка** , указывающая **идентификатор** открываемого **представления** .</span><span class="sxs-lookup"><span data-stu-id="92fee-108">A **String** specifying the **id** of the **VIEW** to open.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="92fee-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="92fee-109">Return Value</span></span>

<span data-ttu-id="92fee-110">Этот метод не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="92fee-110">This method does not return a value.</span></span>

## <a name="examples"></a><span data-ttu-id="92fee-111">Примеры</span><span class="sxs-lookup"><span data-stu-id="92fee-111">Examples</span></span>


```JScript
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



## <a name="requirements"></a><span data-ttu-id="92fee-112">Требования</span><span class="sxs-lookup"><span data-stu-id="92fee-112">Requirements</span></span>



| <span data-ttu-id="92fee-113">Требование</span><span class="sxs-lookup"><span data-stu-id="92fee-113">Requirement</span></span> | <span data-ttu-id="92fee-114">Значение</span><span class="sxs-lookup"><span data-stu-id="92fee-114">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="92fee-115">Версия</span><span class="sxs-lookup"><span data-stu-id="92fee-115">Version</span></span><br/> | <span data-ttu-id="92fee-116">Проигрыватель Windows Media версии 7,0 или более поздней</span><span class="sxs-lookup"><span data-stu-id="92fee-116">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="92fee-117">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="92fee-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="92fee-118">**Элемент THEME**</span><span class="sxs-lookup"><span data-stu-id="92fee-118">**THEME Element**</span></span>](theme-element.md)
</dt> <dt>

[<span data-ttu-id="92fee-119">**THEME. closeView**</span><span class="sxs-lookup"><span data-stu-id="92fee-119">**THEME.closeView**</span></span>](theme-closeview.md)
</dt> <dt>

[<span data-ttu-id="92fee-120">**THEME. Опенвиеврелативе**</span><span class="sxs-lookup"><span data-stu-id="92fee-120">**THEME.openViewRelative**</span></span>](theme-openviewrelative.md)
</dt> </dl>

 

 





