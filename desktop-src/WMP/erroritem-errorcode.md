---
title: Ерроритем. errorCode
description: Свойство errorCode извлекает текущий код ошибки.
ms.assetid: 1495ec34-0995-40c6-bfd0-f3695784e057
keywords:
- Ерроритем. errorCode проигрыватель Windows Media
topic_type:
- apiref
api_name:
- ErrorItem.errorCode
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8c934b83b28e510f29b84a45b48bde700968c97b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105694536"
---
# <a name="erroritemerrorcode"></a><span data-ttu-id="94d3f-104">Ерроритем. errorCode</span><span class="sxs-lookup"><span data-stu-id="94d3f-104">ErrorItem.errorCode</span></span>

<span data-ttu-id="94d3f-105">Свойство **ErrorCode** извлекает текущий код ошибки.</span><span class="sxs-lookup"><span data-stu-id="94d3f-105">The **errorCode** property retrieves the current error code.</span></span>

``` syntax
player.error.item(
        index
        ).errorCode
```

## <a name="possible-values"></a><span data-ttu-id="94d3f-106">Возможные значения</span><span class="sxs-lookup"><span data-stu-id="94d3f-106">Possible Values</span></span>

<span data-ttu-id="94d3f-107">Это свойство является **числом** только для чтения (**длинное целое**).</span><span class="sxs-lookup"><span data-stu-id="94d3f-107">This property is a read-only **Number** (**long**).</span></span>

## <a name="remarks"></a><span data-ttu-id="94d3f-108">Комментарии</span><span class="sxs-lookup"><span data-stu-id="94d3f-108">Remarks</span></span>

<span data-ttu-id="94d3f-109">Необходимо задать *Параметры*. **енаблиррордиалогс** значение false, если выбрано отображение настраиваемых сообщений об ошибках.</span><span class="sxs-lookup"><span data-stu-id="94d3f-109">You should set *Settings*.**enableErrorDialogs** to false if you choose to display custom error messages.</span></span>

## <a name="examples"></a><span data-ttu-id="94d3f-110">Примеры</span><span class="sxs-lookup"><span data-stu-id="94d3f-110">Examples</span></span>

<span data-ttu-id="94d3f-111">В следующем примере JScript используется *ерроритем*. **ErrorCode** в обработчике событий для вывода кода ошибки пользователю.</span><span class="sxs-lookup"><span data-stu-id="94d3f-111">The following JScript example uses *ErrorItem*.**errorCode** in an event handler to display the error code to the user.</span></span> <span data-ttu-id="94d3f-112">Объект **Player** создан с идентификатором "Player".</span><span class="sxs-lookup"><span data-stu-id="94d3f-112">The **Player** object was created with ID = "Player".</span></span>


```JScript
<SCRIPT LANGUAGE = "JScript"  FOR = Player  EVENT = error()>

// Get the error code for the first error item.
errNum = Player.error.item(0).errorCode;

// Display the error information.
var message = "Error number: " + errNum);
message += "<BR>";
message += "Use your BACK button to return ";
message += "to the previous page.";
document.write(message);

</SCRIPT>

```



## <a name="requirements"></a><span data-ttu-id="94d3f-113">Требования</span><span class="sxs-lookup"><span data-stu-id="94d3f-113">Requirements</span></span>



| <span data-ttu-id="94d3f-114">Требование</span><span class="sxs-lookup"><span data-stu-id="94d3f-114">Requirement</span></span> | <span data-ttu-id="94d3f-115">Значение</span><span class="sxs-lookup"><span data-stu-id="94d3f-115">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="94d3f-116">Версия</span><span class="sxs-lookup"><span data-stu-id="94d3f-116">Version</span></span><br/> | <span data-ttu-id="94d3f-117">Проигрыватель Windows Media версии 7,0 или более поздней.</span><span class="sxs-lookup"><span data-stu-id="94d3f-117">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="94d3f-118">DLL</span><span class="sxs-lookup"><span data-stu-id="94d3f-118">DLL</span></span><br/>     | <dl> <span data-ttu-id="94d3f-119"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="94d3f-119"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="94d3f-120">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="94d3f-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="94d3f-121">**Объект Ерроритем**</span><span class="sxs-lookup"><span data-stu-id="94d3f-121">**ErrorItem Object**</span></span>](erroritem-object.md)
</dt> <dt>

[<span data-ttu-id="94d3f-122">**Ерроритем. errorDescription**</span><span class="sxs-lookup"><span data-stu-id="94d3f-122">**ErrorItem.errorDescription**</span></span>](erroritem-errordescription.md)
</dt> </dl>

 

 





