---
title: Ерроритем. errorDescription
description: Свойство errorDescription Извлекает описание ошибки.
ms.assetid: 7fd16c3d-1460-41b5-81ca-2636d7a1d0d1
keywords:
- Проигрыватель Windows Media Ерроритем. errorDescription
topic_type:
- apiref
api_name:
- ErrorItem.errorDescription
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f0de19bb67a5846a82e87d091f95a18cd12c5c2b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105694534"
---
# <a name="erroritemerrordescription"></a><span data-ttu-id="c7501-104">Ерроритем. errorDescription</span><span class="sxs-lookup"><span data-stu-id="c7501-104">ErrorItem.errorDescription</span></span>

<span data-ttu-id="c7501-105">Свойство **errorDescription** Извлекает описание ошибки.</span><span class="sxs-lookup"><span data-stu-id="c7501-105">The **errorDescription** property retrieves a description of the error.</span></span>

``` syntax
player.error.item(
        index
        ).errorDescription
```

## <a name="possible-values"></a><span data-ttu-id="c7501-106">Возможные значения</span><span class="sxs-lookup"><span data-stu-id="c7501-106">Possible Values</span></span>

<span data-ttu-id="c7501-107">Это свойство является **строкой**, доступная только для чтения.</span><span class="sxs-lookup"><span data-stu-id="c7501-107">This property is a read-only **String**.</span></span>

## <a name="remarks"></a><span data-ttu-id="c7501-108">Комментарии</span><span class="sxs-lookup"><span data-stu-id="c7501-108">Remarks</span></span>

<span data-ttu-id="c7501-109">Необходимо задать *Параметры*. **енаблиррордиалогс** значение false, если выбрано отображение настраиваемых сообщений об ошибках.</span><span class="sxs-lookup"><span data-stu-id="c7501-109">You should set *Settings*.**enableErrorDialogs** to false if you choose to display custom error messages.</span></span>

## <a name="examples"></a><span data-ttu-id="c7501-110">Примеры</span><span class="sxs-lookup"><span data-stu-id="c7501-110">Examples</span></span>

<span data-ttu-id="c7501-111">В следующем примере JScript используется *ерроритем*. **errorDescription** в обработчике событий для вывода сообщения об ошибке пользователю.</span><span class="sxs-lookup"><span data-stu-id="c7501-111">The following JScript example uses *ErrorItem*.**errorDescription** in an event handler to display the error message to the user.</span></span> <span data-ttu-id="c7501-112">Объект **Player** создан с идентификатором "Player".</span><span class="sxs-lookup"><span data-stu-id="c7501-112">The **Player** object was created with ID = "Player".</span></span>


```JScript
<SCRIPT LANGUAGE = "JScript"  FOR = Player  EVENT = error()>

// Get the error description for the first error item.
errDesc = Player.error.item(0).errorDescription;

// Display the error code.
var message = "Error: " + errDesc";
message += "<BR>";
message += "Use your BACK button to return ";
message += "to the previous page.";
document.write(message);

</SCRIPT>

```



## <a name="requirements"></a><span data-ttu-id="c7501-113">Требования</span><span class="sxs-lookup"><span data-stu-id="c7501-113">Requirements</span></span>



| <span data-ttu-id="c7501-114">Требование</span><span class="sxs-lookup"><span data-stu-id="c7501-114">Requirement</span></span> | <span data-ttu-id="c7501-115">Значение</span><span class="sxs-lookup"><span data-stu-id="c7501-115">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="c7501-116">Версия</span><span class="sxs-lookup"><span data-stu-id="c7501-116">Version</span></span><br/> | <span data-ttu-id="c7501-117">Проигрыватель Windows Media версии 7,0 или более поздней</span><span class="sxs-lookup"><span data-stu-id="c7501-117">Windows Media Player version 7.0 or later</span></span><br/>                               |
| <span data-ttu-id="c7501-118">DLL</span><span class="sxs-lookup"><span data-stu-id="c7501-118">DLL</span></span><br/>     | <dl> <span data-ttu-id="c7501-119"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c7501-119"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c7501-120">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="c7501-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c7501-121">**Объект Ерроритем**</span><span class="sxs-lookup"><span data-stu-id="c7501-121">**ErrorItem Object**</span></span>](erroritem-object.md)
</dt> </dl>

 

 





