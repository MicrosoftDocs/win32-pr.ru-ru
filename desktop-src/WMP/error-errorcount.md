---
title: Ошибка. Ерроркаунт
description: Свойство Ерроркаунт извлекает количество ошибок в очереди ошибок.
ms.assetid: 64d9bb0a-fcc4-401b-a7bd-529e1a517f3b
keywords:
- Ошибка. Ерроркаунт Windows Media Player
topic_type:
- apiref
api_name:
- Error.errorCount
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 94848023d2cd331545f97d3bea6d92f2fcd4b49c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105694515"
---
# <a name="errorerrorcount"></a><span data-ttu-id="feb17-104">Ошибка. Ерроркаунт</span><span class="sxs-lookup"><span data-stu-id="feb17-104">Error.errorCount</span></span>

<span data-ttu-id="feb17-105">Свойство **ерроркаунт** извлекает количество ошибок в очереди ошибок.</span><span class="sxs-lookup"><span data-stu-id="feb17-105">The **errorCount** property retrieves the number of errors in the error queue.</span></span>

``` syntax
player.error.errorCount
      
```

## <a name="possible-values"></a><span data-ttu-id="feb17-106">Возможные значения</span><span class="sxs-lookup"><span data-stu-id="feb17-106">Possible Values</span></span>

<span data-ttu-id="feb17-107">Это свойство является **числом** только для чтения (**длинное целое**).</span><span class="sxs-lookup"><span data-stu-id="feb17-107">This property is a read-only **Number** (**long**).</span></span>

## <a name="remarks"></a><span data-ttu-id="feb17-108">Комментарии</span><span class="sxs-lookup"><span data-stu-id="feb17-108">Remarks</span></span>

<span data-ttu-id="feb17-109">Необходимо задать *Параметры*. **енаблиррордиалогс** значение false, если выбрано отображение настраиваемых сообщений об ошибках.</span><span class="sxs-lookup"><span data-stu-id="feb17-109">You should set *Settings*.**enableErrorDialogs** to false if you choose to display custom error messages.</span></span>

## <a name="examples"></a><span data-ttu-id="feb17-110">Примеры</span><span class="sxs-lookup"><span data-stu-id="feb17-110">Examples</span></span>

<span data-ttu-id="feb17-111">В следующем примере JScript используется *Ошибка*. **ерроркаунт** в обработчике событий, чтобы предупредить пользователя о последней ошибке в очереди ошибок.</span><span class="sxs-lookup"><span data-stu-id="feb17-111">The following JScript example uses *Error*.**errorCount** in an event handler to alert the user about the most recent error in the error queue.</span></span> <span data-ttu-id="feb17-112">Объект **Player** создан с идентификатором "Player".</span><span class="sxs-lookup"><span data-stu-id="feb17-112">The **Player** object was created with ID = "Player".</span></span>


```JScript
<SCRIPT LANGUAGE = "JScript"  FOR = Player  EVENT = error()>

// Store the number of errors in the queue.
var max = Player.error.errorCount;

// Get the description of the last error. Error items start at zero,
// so the item index will always be one less than the error count.
var errDesc = Player.error.item(max-1).errorDescription;

// Display the error description.
alert(errDesc);

</SCRIPT>

```



## <a name="requirements"></a><span data-ttu-id="feb17-113">Требования</span><span class="sxs-lookup"><span data-stu-id="feb17-113">Requirements</span></span>



| <span data-ttu-id="feb17-114">Требование</span><span class="sxs-lookup"><span data-stu-id="feb17-114">Requirement</span></span> | <span data-ttu-id="feb17-115">Значение</span><span class="sxs-lookup"><span data-stu-id="feb17-115">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="feb17-116">Версия</span><span class="sxs-lookup"><span data-stu-id="feb17-116">Version</span></span><br/> | <span data-ttu-id="feb17-117">Проигрыватель Windows Media версии 7,0 или более поздней.</span><span class="sxs-lookup"><span data-stu-id="feb17-117">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="feb17-118">DLL</span><span class="sxs-lookup"><span data-stu-id="feb17-118">DLL</span></span><br/>     | <dl> <span data-ttu-id="feb17-119"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="feb17-119"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="feb17-120">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="feb17-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="feb17-121">**Объект Error**</span><span class="sxs-lookup"><span data-stu-id="feb17-121">**Error Object**</span></span>](error-object.md)
</dt> </dl>

 

 





