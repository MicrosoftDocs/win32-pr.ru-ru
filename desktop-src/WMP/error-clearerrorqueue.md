---
title: Ошибка. метод Клеарерроркуеуе
description: Метод Клеарерроркуеуе удаляет ошибки из очереди ошибок. | Ошибка. метод Клеарерроркуеуе
ms.assetid: 306f0700-88b1-4433-8abb-7d225e82060a
keywords:
- Клеарерроркуеуе метод Windows Media Player
- метод Клеарерроркуеуе Windows Media Player, класс Error
- Класс ошибок Windows Media Player, метод Клеарерроркуеуе
topic_type:
- apiref
api_name:
- Error.clearErrorQueue
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6b756708b8f0643f86489c26dd921e87c408be8f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105694925"
---
# <a name="errorclearerrorqueue-method"></a><span data-ttu-id="49a7b-107">Ошибка. метод Клеарерроркуеуе</span><span class="sxs-lookup"><span data-stu-id="49a7b-107">Error.clearErrorQueue method</span></span>

<span data-ttu-id="49a7b-108">Метод **клеарерроркуеуе** удаляет ошибки из очереди ошибок.</span><span class="sxs-lookup"><span data-stu-id="49a7b-108">The **clearErrorQueue** method clears the errors from the error queue.</span></span>

## <a name="syntax"></a><span data-ttu-id="49a7b-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="49a7b-109">Syntax</span></span>


```JScript
Error.clearErrorQueue()
```



## <a name="parameters"></a><span data-ttu-id="49a7b-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="49a7b-110">Parameters</span></span>

<span data-ttu-id="49a7b-111">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="49a7b-111">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="49a7b-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="49a7b-112">Return value</span></span>

<span data-ttu-id="49a7b-113">Этот метод не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="49a7b-113">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="49a7b-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="49a7b-114">Remarks</span></span>

<span data-ttu-id="49a7b-115">Этот метод полезен для очистки очереди ошибок после обработки ряда ошибок.</span><span class="sxs-lookup"><span data-stu-id="49a7b-115">This method is useful to clear the error queue after a series of errors has been processed.</span></span>

<span data-ttu-id="49a7b-116">Необходимо задать *Параметры*. **енаблиррордиалогс** значение false, если выбрано отображение настраиваемых сообщений об ошибках.</span><span class="sxs-lookup"><span data-stu-id="49a7b-116">You should set *Settings*.**enableErrorDialogs** to false if you choose to display custom error messages.</span></span>

## <a name="examples"></a><span data-ttu-id="49a7b-117">Примеры</span><span class="sxs-lookup"><span data-stu-id="49a7b-117">Examples</span></span>

<span data-ttu-id="49a7b-118">В следующем примере JScript используется *Ошибка*. **клеарерроркуеуе** в обработчике событий, чтобы очистить очередь ошибок после отображения всех описаний ошибок.</span><span class="sxs-lookup"><span data-stu-id="49a7b-118">The following JScript example uses *Error*.**clearErrorQueue** in an event handler to empty the error queue after all error descriptions are displayed.</span></span> <span data-ttu-id="49a7b-119">Объект **Player** создан с идентификатором "Player".</span><span class="sxs-lookup"><span data-stu-id="49a7b-119">The **Player** object was created with ID = "Player".</span></span>


```JScript
<SCRIPT LANGUAGE = "JScript"  FOR = Player  EVENT = error()>

// Store the number of errors in the queue.
var max = Player.error.errorCount 

// Loop through the list of errors.
for (var i = 0; i < max; i++){
    // Get the error description for this item.
    var errDesc = Player.error.item(i).errorDescription;
    
    // Display the error message.
    alert(errDesc);
}

// Clear the error queue to prepare for the next group of errors.
Player.error.clearErrorQueue();

</SCRIPT>

```



## <a name="requirements"></a><span data-ttu-id="49a7b-120">Требования</span><span class="sxs-lookup"><span data-stu-id="49a7b-120">Requirements</span></span>



| <span data-ttu-id="49a7b-121">Требование</span><span class="sxs-lookup"><span data-stu-id="49a7b-121">Requirement</span></span> | <span data-ttu-id="49a7b-122">Значение</span><span class="sxs-lookup"><span data-stu-id="49a7b-122">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="49a7b-123">Версия</span><span class="sxs-lookup"><span data-stu-id="49a7b-123">Version</span></span><br/> | <span data-ttu-id="49a7b-124">Проигрыватель Windows Media версии 7,0 или более поздней.</span><span class="sxs-lookup"><span data-stu-id="49a7b-124">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="49a7b-125">DLL</span><span class="sxs-lookup"><span data-stu-id="49a7b-125">DLL</span></span><br/>     | <dl> <span data-ttu-id="49a7b-126"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="49a7b-126"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="49a7b-127">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="49a7b-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="49a7b-128">**Объект Error**</span><span class="sxs-lookup"><span data-stu-id="49a7b-128">**Error Object**</span></span>](error-object.md)
</dt> </dl>

 

 





