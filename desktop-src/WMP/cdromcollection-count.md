---
title: Кдромколлектион. Count
description: Свойство Count извлекает количество доступных компакт-дисков и DVD-дисководов в системе.
ms.assetid: 98d24713-6a55-409f-af9a-fc941ad6d8f5
keywords:
- Проигрыватель Windows Media Кдромколлектион. Count
topic_type:
- apiref
api_name:
- CdromCollection.count
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bf7150ca31caaf68fa51ae42fded223d24a8e59f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105699177"
---
# <a name="cdromcollectioncount"></a><span data-ttu-id="fc63e-104">Кдромколлектион. Count</span><span class="sxs-lookup"><span data-stu-id="fc63e-104">CdromCollection.count</span></span>

<span data-ttu-id="fc63e-105">Свойство **Count** извлекает количество доступных компакт-дисков и DVD-дисководов в системе.</span><span class="sxs-lookup"><span data-stu-id="fc63e-105">The **count** property retrieves the number of available CD and DVD drives on the system.</span></span>

``` syntax
player.cdromCollection.count
      
```

## <a name="possible-values"></a><span data-ttu-id="fc63e-106">Возможные значения</span><span class="sxs-lookup"><span data-stu-id="fc63e-106">Possible Values</span></span>

<span data-ttu-id="fc63e-107">Это свойство является **числом** только для чтения (**длинное целое**).</span><span class="sxs-lookup"><span data-stu-id="fc63e-107">This property is a read-only **Number** (**long**).</span></span>

## <a name="remarks"></a><span data-ttu-id="fc63e-108">Комментарии</span><span class="sxs-lookup"><span data-stu-id="fc63e-108">Remarks</span></span>

<span data-ttu-id="fc63e-109">Чтобы получить значение этого свойства, требуется доступ на чтение к библиотеке.</span><span class="sxs-lookup"><span data-stu-id="fc63e-109">To retrieve the value of this property, read access to the library is required.</span></span> <span data-ttu-id="fc63e-110">Дополнительные сведения см. в разделе [доступ к библиотеке](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="fc63e-110">For more information, see [Library Access](library-access.md).</span></span>

<span data-ttu-id="fc63e-111">Дисководы DVD-дисков подсчитываются точно так же, как и дисководы компакт-дисков.</span><span class="sxs-lookup"><span data-stu-id="fc63e-111">DVD-ROM drives are counted exactly like CD drives.</span></span> <span data-ttu-id="fc63e-112">Однако элемент управления проигрывателя Windows Media поддерживает только функции DVD для операционных систем Windows XP и более поздних версий.</span><span class="sxs-lookup"><span data-stu-id="fc63e-112">However, the Windows Media Player control only supports DVD functionality for Windows XP or later operating systems.</span></span> <span data-ttu-id="fc63e-113">Обычно дисководы DVD могут воспроизводить компакт-диски, но дисководы компакт-дисков не могут воспроизводить DVD-носители.</span><span class="sxs-lookup"><span data-stu-id="fc63e-113">Typically, DVD drives can play CD media, but CD drives cannot play DVD media.</span></span>

<span data-ttu-id="fc63e-114">**Проигрыватель Windows Media 10 Mobile:** Этот метод всегда возвращает значение 0.</span><span class="sxs-lookup"><span data-stu-id="fc63e-114">**Windows Media Player 10 Mobile:** This method always returns 0.</span></span>

## <a name="examples"></a><span data-ttu-id="fc63e-115">Примеры</span><span class="sxs-lookup"><span data-stu-id="fc63e-115">Examples</span></span>

<span data-ttu-id="fc63e-116">В следующем примере JScript используется *кдромколлектион*. **число** , которое показывает число дисков CD и DVD, доступных на компьютере пользователя.</span><span class="sxs-lookup"><span data-stu-id="fc63e-116">The following JScript example uses *CdromCollection*.**count** to display the number of CD and DVD drives available on the user's computer.</span></span> <span data-ttu-id="fc63e-117">Объект Player создан с ИДЕНТИФИКАТОРом "Player".</span><span class="sxs-lookup"><span data-stu-id="fc63e-117">The player object was created with ID = "Player".</span></span>


```JScript
// Store the count of drives found on the computer.
var numCDROMS = Player.cdromCollection.count;

// Build the string to display to the user.
var displayString = numCDROMS + " drive(s) found.";

// Show a message box with the count information.
alert(displayString);
```



## <a name="requirements"></a><span data-ttu-id="fc63e-118">Требования</span><span class="sxs-lookup"><span data-stu-id="fc63e-118">Requirements</span></span>



| <span data-ttu-id="fc63e-119">Требование</span><span class="sxs-lookup"><span data-stu-id="fc63e-119">Requirement</span></span> | <span data-ttu-id="fc63e-120">Значение</span><span class="sxs-lookup"><span data-stu-id="fc63e-120">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="fc63e-121">Версия</span><span class="sxs-lookup"><span data-stu-id="fc63e-121">Version</span></span><br/> | <span data-ttu-id="fc63e-122">Проигрыватель Windows Media версии 7,0 или более поздней</span><span class="sxs-lookup"><span data-stu-id="fc63e-122">Windows Media Player version 7.0 or later</span></span><br/>                               |
| <span data-ttu-id="fc63e-123">DLL</span><span class="sxs-lookup"><span data-stu-id="fc63e-123">DLL</span></span><br/>     | <dl> <span data-ttu-id="fc63e-124"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fc63e-124"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fc63e-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="fc63e-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fc63e-126">**Объект Кдромколлектион**</span><span class="sxs-lookup"><span data-stu-id="fc63e-126">**CdromCollection Object**</span></span>](cdromcollection-object.md)
</dt> <dt>

[<span data-ttu-id="fc63e-127">**Settings. Медиаакцессригхтс**</span><span class="sxs-lookup"><span data-stu-id="fc63e-127">**Settings.mediaAccessRights**</span></span>](settings-mediaaccessrights.md)
</dt> <dt>

[<span data-ttu-id="fc63e-128">**Settings. Рекуестмедиаакцессригхтс**</span><span class="sxs-lookup"><span data-stu-id="fc63e-128">**Settings.requestMediaAccessRights**</span></span>](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





