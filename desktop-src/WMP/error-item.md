---
title: Error. Item, метод
description: Метод Item извлекает объект Ерроритем из очереди ошибок.
ms.assetid: 3aca21ff-4c6b-4c24-a85d-3d015612a496
keywords:
- метод Item проигрыватель Windows Media Player
- метод Item проигрыватель Windows Media, класс Error
- Класс ошибок Windows Media Player, метод Item
topic_type:
- apiref
api_name:
- Error.item
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5545df50fce05ff5a10a5f870d1ec07648434fe9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105694512"
---
# <a name="erroritem-method"></a><span data-ttu-id="fd0d5-106">Error. Item, метод</span><span class="sxs-lookup"><span data-stu-id="fd0d5-106">Error.item method</span></span>

<span data-ttu-id="fd0d5-107">Метод **Item** извлекает объект **ерроритем** из очереди ошибок.</span><span class="sxs-lookup"><span data-stu-id="fd0d5-107">The **item** method retrieves an **ErrorItem** object from the error queue.</span></span>

## <a name="syntax"></a><span data-ttu-id="fd0d5-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="fd0d5-108">Syntax</span></span>


```JScript
retVal = Error.item(
  index
)
```



## <a name="parameters"></a><span data-ttu-id="fd0d5-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="fd0d5-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fd0d5-110">*индекс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="fd0d5-110">*index* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fd0d5-111">**Число** (**Long**), содержащее индекс объекта **ерроритем** , который требуется получить.</span><span class="sxs-lookup"><span data-stu-id="fd0d5-111">**Number** (**long**) containing the index of the **ErrorItem** object to be retrieved.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fd0d5-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="fd0d5-112">Return value</span></span>

<span data-ttu-id="fd0d5-113">Этот метод возвращает объект **ерроритем** .</span><span class="sxs-lookup"><span data-stu-id="fd0d5-113">This method returns an **ErrorItem** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="fd0d5-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="fd0d5-114">Remarks</span></span>

<span data-ttu-id="fd0d5-115">Проигрыватель Windows Media может создавать ряд ошибок в ответ на состояние ошибки.</span><span class="sxs-lookup"><span data-stu-id="fd0d5-115">Windows Media Player can generate a number of errors in response to an error condition.</span></span> <span data-ttu-id="fd0d5-116">Этот метод позволяет получить конкретную ошибку в очереди, используя номер индекса.</span><span class="sxs-lookup"><span data-stu-id="fd0d5-116">This method allows the retrieval of a specific error in the queue by using an index number.</span></span> <span data-ttu-id="fd0d5-117">Номера индексов для очереди ошибок начинаются с нуля.</span><span class="sxs-lookup"><span data-stu-id="fd0d5-117">The index numbers for the error queue begin with zero.</span></span>

<span data-ttu-id="fd0d5-118">Необходимо задать *Параметры*. **енаблиррордиалогс** значение false, если выбрано отображение настраиваемых сообщений об ошибках.</span><span class="sxs-lookup"><span data-stu-id="fd0d5-118">You should set *Settings*.**enableErrorDialogs** to false if you choose to display custom error messages.</span></span>

## <a name="examples"></a><span data-ttu-id="fd0d5-119">Примеры</span><span class="sxs-lookup"><span data-stu-id="fd0d5-119">Examples</span></span>

<span data-ttu-id="fd0d5-120">В следующем примере JScript используется *Ошибка*. Объект **Item** в обработчике событий для предупреждения пользователя о последней ошибке.</span><span class="sxs-lookup"><span data-stu-id="fd0d5-120">The following JScript example uses the *Error*.**item** object in an event handler to alert the user to the most recent error.</span></span> <span data-ttu-id="fd0d5-121">Объект **Player** создан с идентификатором "Player".</span><span class="sxs-lookup"><span data-stu-id="fd0d5-121">The **Player** object was created with ID = "Player".</span></span>


```JScript
<SCRIPT LANGUAGE="JScript"  FOR=Player EVENT=error()>

// Store the most recent error item number.
var max = Player.error.errorCount - 1 

// Store the most recent error in an error item object.
var errItem = Player.error.item(max);

// Use the error item object to store the error info.
errDesc = errItem.errorDescription;
errNum = errItem.errorCode;

// Display the error info.
alert(errNum + "\n" + errDesc);

</SCRIPT> 

```



## <a name="requirements"></a><span data-ttu-id="fd0d5-122">Требования</span><span class="sxs-lookup"><span data-stu-id="fd0d5-122">Requirements</span></span>



| <span data-ttu-id="fd0d5-123">Требование</span><span class="sxs-lookup"><span data-stu-id="fd0d5-123">Requirement</span></span> | <span data-ttu-id="fd0d5-124">Значение</span><span class="sxs-lookup"><span data-stu-id="fd0d5-124">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="fd0d5-125">Версия</span><span class="sxs-lookup"><span data-stu-id="fd0d5-125">Version</span></span><br/> | <span data-ttu-id="fd0d5-126">Проигрыватель Windows Media версии 7,0 или более поздней.</span><span class="sxs-lookup"><span data-stu-id="fd0d5-126">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="fd0d5-127">DLL</span><span class="sxs-lookup"><span data-stu-id="fd0d5-127">DLL</span></span><br/>     | <dl> <span data-ttu-id="fd0d5-128"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fd0d5-128"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fd0d5-129">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="fd0d5-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fd0d5-130">**Объект Error**</span><span class="sxs-lookup"><span data-stu-id="fd0d5-130">**Error Object**</span></span>](error-object.md)
</dt> <dt>

[<span data-ttu-id="fd0d5-131">**Объект Ерроритем**</span><span class="sxs-lookup"><span data-stu-id="fd0d5-131">**ErrorItem Object**</span></span>](erroritem-object.md)
</dt> </dl>

 

 





