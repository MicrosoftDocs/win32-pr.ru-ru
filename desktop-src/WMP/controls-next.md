---
title: Метод Controls. Next
description: Следующий метод задает текущий элемент для следующего элемента списка воспроизведения.
ms.assetid: 67436c76-8fb9-4350-86f3-67f5e9e6dca1
keywords:
- Следующий метод проигрывателя Windows Media
- 'Следующий метод: проигрыватель Windows Media, класс Controls'
- Класс управляет проигрывателем Windows Media Player, метод Next
topic_type:
- apiref
api_name:
- Controls.next
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8f58e6d11eafe38b4ab26e0275bd5c986cd4e4a4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105699217"
---
# <a name="controlsnext-method"></a><span data-ttu-id="04720-106">Метод Controls. Next</span><span class="sxs-lookup"><span data-stu-id="04720-106">Controls.next method</span></span>

<span data-ttu-id="04720-107">**Следующий** метод задает текущий элемент для следующего элемента списка воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="04720-107">The **next** method sets the current item to the next item in the playlist.</span></span>

## <a name="syntax"></a><span data-ttu-id="04720-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="04720-108">Syntax</span></span>


```JScript
Controls.next()
```



## <a name="parameters"></a><span data-ttu-id="04720-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="04720-109">Parameters</span></span>

<span data-ttu-id="04720-110">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="04720-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="04720-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="04720-111">Return value</span></span>

<span data-ttu-id="04720-112">Этот метод не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="04720-112">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="04720-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="04720-113">Remarks</span></span>

<span data-ttu-id="04720-114">Если список воспроизведения находится в последней записи при вызове **Next** , первая запись списка воспроизведения станет текущей.</span><span class="sxs-lookup"><span data-stu-id="04720-114">If the playlist is on the last entry when **next** is invoked, the first entry in the playlist will become the current one.</span></span>

<span data-ttu-id="04720-115">Для списков воспроизведения на стороне сервера этот метод пропускает следующий элемент в списке воспроизведения на стороне сервера, а не в списке воспроизведения клиента.</span><span class="sxs-lookup"><span data-stu-id="04720-115">For server-side playlists, this method skips to the next item in the server-side playlist, not the client playlist.</span></span>

<span data-ttu-id="04720-116">При воспроизведении DVD этот метод пропускает следующую логическую главу в последовательности воспроизведения, которая может не быть следующей главой в списке воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="04720-116">When playing a DVD, this method skips to the next logical chapter in the playback sequence, which may not be the next chapter in the playlist.</span></span> <span data-ttu-id="04720-117">При каждом воспроизведении DVD-диска этот метод пропускается до следующего.</span><span class="sxs-lookup"><span data-stu-id="04720-117">When playing DVD stills, this method skips to the next still.</span></span>

## <a name="examples"></a><span data-ttu-id="04720-118">Примеры</span><span class="sxs-lookup"><span data-stu-id="04720-118">Examples</span></span>

<span data-ttu-id="04720-119">В следующем примере создается HTML-элемент BUTTON, который использует **Next** для перехода к следующему элементу в текущем списке воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="04720-119">The following example creates an HTML BUTTON element that uses **next** to move to the next item in the current playlist.</span></span> <span data-ttu-id="04720-120">Объект **Player** создан с идентификатором "Player".</span><span class="sxs-lookup"><span data-stu-id="04720-120">The **Player** object was created with ID = "Player".</span></span>


```JScript
<INPUT TYPE = "BUTTON"  ID = "NEXT"  NAME = "NEXT"  VALUE = ">>|"
    onClick = "

        /* Check first to be sure the operation is valid. */
        if (Player.controls.isAvailable('Next'))

            /* Move to the next item in the playlist. */
            Player.controls.next();
">

```



## <a name="requirements"></a><span data-ttu-id="04720-121">Требования</span><span class="sxs-lookup"><span data-stu-id="04720-121">Requirements</span></span>



| <span data-ttu-id="04720-122">Требование</span><span class="sxs-lookup"><span data-stu-id="04720-122">Requirement</span></span> | <span data-ttu-id="04720-123">Значение</span><span class="sxs-lookup"><span data-stu-id="04720-123">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="04720-124">Версия</span><span class="sxs-lookup"><span data-stu-id="04720-124">Version</span></span><br/> | <span data-ttu-id="04720-125">Проигрыватель Windows Media версии 7,0 или более поздней.</span><span class="sxs-lookup"><span data-stu-id="04720-125">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="04720-126">DLL</span><span class="sxs-lookup"><span data-stu-id="04720-126">DLL</span></span><br/>     | <dl> <span data-ttu-id="04720-127"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="04720-127"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="04720-128">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="04720-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="04720-129">**Объект Controls**</span><span class="sxs-lookup"><span data-stu-id="04720-129">**Controls Object**</span></span>](controls-object.md)
</dt> <dt>

[<span data-ttu-id="04720-130">**Controls. Previous**</span><span class="sxs-lookup"><span data-stu-id="04720-130">**Controls.previous**</span></span>](controls-previous.md)
</dt> <dt>

[<span data-ttu-id="04720-131">**Controls. останавливаться**</span><span class="sxs-lookup"><span data-stu-id="04720-131">**Controls.stop**</span></span>](controls-stop.md)
</dt> </dl>

 

 





