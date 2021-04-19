---
title: Controls. currentPosition
description: Свойство currentPosition указывает или получает текущую позицию в элементе мультимедиа за считаные секунды с начала.
ms.assetid: 374ad144-3f74-4d1b-bec5-1cd0f03777b7
keywords:
- Проигрыватель Windows Media Controls. currentPosition
topic_type:
- apiref
api_name:
- Controls.currentPosition
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 12c690c102bb95c1a58785f18d727ffdae2a82c4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105698993"
---
# <a name="controlscurrentposition"></a><span data-ttu-id="5f501-104">Controls. currentPosition</span><span class="sxs-lookup"><span data-stu-id="5f501-104">Controls.currentPosition</span></span>

<span data-ttu-id="5f501-105">Свойство **CurrentPosition** указывает или получает текущую позицию в элементе мультимедиа за считаные секунды с начала.</span><span class="sxs-lookup"><span data-stu-id="5f501-105">The **currentPosition** property specifies or retrieves the current position in the media item in seconds from the beginning.</span></span>

``` syntax
player.controls.currentPosition
      
```

## <a name="possible-values"></a><span data-ttu-id="5f501-106">Возможные значения</span><span class="sxs-lookup"><span data-stu-id="5f501-106">Possible Values</span></span>

<span data-ttu-id="5f501-107">Это свойство является **числом** для чтения и записи (**Double**).</span><span class="sxs-lookup"><span data-stu-id="5f501-107">This property is a read/write **Number** (**double**).</span></span>

## <a name="examples"></a><span data-ttu-id="5f501-108">Примеры</span><span class="sxs-lookup"><span data-stu-id="5f501-108">Examples</span></span>

<span data-ttu-id="5f501-109">В следующем примере **CurrentPosition** используется для поиска расположения, предоставленного пользователем.</span><span class="sxs-lookup"><span data-stu-id="5f501-109">The following example uses **currentPosition** to seek to a position provided by the user.</span></span> <span data-ttu-id="5f501-110">Для выполнения кода JScript создается HTML-элемент BUTTON.</span><span class="sxs-lookup"><span data-stu-id="5f501-110">An HTML BUTTON element is created to execute the JScript code.</span></span> <span data-ttu-id="5f501-111">Элемент ввода текста HTML с именем setPosition был создан для принятия значения в секундах от пользователя.</span><span class="sxs-lookup"><span data-stu-id="5f501-111">An HTML TEXT input element, named setPosition, was created to accept a value, in seconds, from the user.</span></span> <span data-ttu-id="5f501-112">Объект **Player** создан с идентификатором "Player".</span><span class="sxs-lookup"><span data-stu-id="5f501-112">The **Player** object was created with ID = "Player".</span></span>


```JScript
<INPUT TYPE = "BUTTON"  ID = "Set"  NAME = "Set"  VALUE = "Set Position"

    /* Check to be sure the TEXT element contains a valid value. */
    if (!isNaN(setPosition.value) && (setPosition.value != '))

    /* Set the current position when the user clicks the button. */
    onClick = "Player.controls.currentPosition = setPosition.value;
">
```



## <a name="requirements"></a><span data-ttu-id="5f501-113">Требования</span><span class="sxs-lookup"><span data-stu-id="5f501-113">Requirements</span></span>



| <span data-ttu-id="5f501-114">Требование</span><span class="sxs-lookup"><span data-stu-id="5f501-114">Requirement</span></span> | <span data-ttu-id="5f501-115">Значение</span><span class="sxs-lookup"><span data-stu-id="5f501-115">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="5f501-116">Версия</span><span class="sxs-lookup"><span data-stu-id="5f501-116">Version</span></span><br/> | <span data-ttu-id="5f501-117">Проигрыватель Windows Media версии 7,0 или более поздней.</span><span class="sxs-lookup"><span data-stu-id="5f501-117">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="5f501-118">DLL</span><span class="sxs-lookup"><span data-stu-id="5f501-118">DLL</span></span><br/>     | <dl> <span data-ttu-id="5f501-119"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5f501-119"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5f501-120">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="5f501-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5f501-121">**Объект Controls**</span><span class="sxs-lookup"><span data-stu-id="5f501-121">**Controls Object**</span></span>](controls-object.md)
</dt> </dl>

 

 





