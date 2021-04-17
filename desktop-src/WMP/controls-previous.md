---
title: Метод Controls. Previous
description: Предыдущий метод устанавливает текущий элемент на предыдущий элемент в списке воспроизведения.
ms.assetid: 09f83306-5e82-4384-ad28-38e406a401d8
keywords:
- Предыдущий метод проигрывателя Windows Media
- Предыдущий метод проигрыватель Windows Media, класс Controls
- Класс элементов управления проигрыватель Windows Media Player, предыдущий метод
topic_type:
- apiref
api_name:
- Controls.previous
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8b8fcfacd93412f467e6ef1def5afa6305a6bc0c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105698761"
---
# <a name="controlsprevious-method"></a><span data-ttu-id="bd123-106">Метод Controls. Previous</span><span class="sxs-lookup"><span data-stu-id="bd123-106">Controls.previous method</span></span>

<span data-ttu-id="bd123-107">**Предыдущий** метод устанавливает текущий элемент на предыдущий элемент в списке воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="bd123-107">The **previous** method sets the current item to the previous item in the playlist.</span></span>

## <a name="syntax"></a><span data-ttu-id="bd123-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="bd123-108">Syntax</span></span>


```JScript
Controls.previous()
```



## <a name="parameters"></a><span data-ttu-id="bd123-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="bd123-109">Parameters</span></span>

<span data-ttu-id="bd123-110">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="bd123-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="bd123-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="bd123-111">Return value</span></span>

<span data-ttu-id="bd123-112">Этот метод не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="bd123-112">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="bd123-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="bd123-113">Remarks</span></span>

<span data-ttu-id="bd123-114">Если список воспроизведения находится в первой записи при вызове **предыдущего** , последняя запись списка воспроизведения станет текущей.</span><span class="sxs-lookup"><span data-stu-id="bd123-114">If the playlist is on the first entry when **previous** is invoked, the last entry in the playlist will become the current one.</span></span>

## <a name="examples"></a><span data-ttu-id="bd123-115">Примеры</span><span class="sxs-lookup"><span data-stu-id="bd123-115">Examples</span></span>

<span data-ttu-id="bd123-116">В следующем примере создается HTML-элемент BUTTON, который использует **Previous** для перехода к предыдущему элементу в текущем списке воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="bd123-116">The following example creates an HTML BUTTON element that uses **previous** to move to the preceding item in the current playlist.</span></span> <span data-ttu-id="bd123-117">Объект **Player** создан с идентификатором "Player".</span><span class="sxs-lookup"><span data-stu-id="bd123-117">The **Player** object was created with ID = "Player".</span></span>


```JScript
<INPUT TYPE = "BUTTON"  ID = "PREV"  NAME = "PREV"  VALUE = "|<<"
    onClick = "

        /* Check first to be sure the operation is valid. */
        if (Player.controls.isAvailable('Previous'))

            /* Move to the preceding item in the playlist. */
            Player.controls.previous();
">

```



## <a name="requirements"></a><span data-ttu-id="bd123-118">Требования</span><span class="sxs-lookup"><span data-stu-id="bd123-118">Requirements</span></span>



| <span data-ttu-id="bd123-119">Требование</span><span class="sxs-lookup"><span data-stu-id="bd123-119">Requirement</span></span> | <span data-ttu-id="bd123-120">Значение</span><span class="sxs-lookup"><span data-stu-id="bd123-120">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="bd123-121">Версия</span><span class="sxs-lookup"><span data-stu-id="bd123-121">Version</span></span><br/> | <span data-ttu-id="bd123-122">Проигрыватель Windows Media версии 7,0 или более поздней.</span><span class="sxs-lookup"><span data-stu-id="bd123-122">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="bd123-123">DLL</span><span class="sxs-lookup"><span data-stu-id="bd123-123">DLL</span></span><br/>     | <dl> <span data-ttu-id="bd123-124"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bd123-124"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bd123-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="bd123-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bd123-126">**Объект Controls**</span><span class="sxs-lookup"><span data-stu-id="bd123-126">**Controls Object**</span></span>](controls-object.md)
</dt> <dt>

[<span data-ttu-id="bd123-127">**Controls. Next**</span><span class="sxs-lookup"><span data-stu-id="bd123-127">**Controls.next**</span></span>](controls-next.md)
</dt> <dt>

[<span data-ttu-id="bd123-128">**Controls. останавливаться**</span><span class="sxs-lookup"><span data-stu-id="bd123-128">**Controls.stop**</span></span>](controls-stop.md)
</dt> </dl>

 

 





