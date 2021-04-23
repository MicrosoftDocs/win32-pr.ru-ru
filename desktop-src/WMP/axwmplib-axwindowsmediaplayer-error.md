---
title: Событие Error объекта Аксвиндовсмедиаплайер
description: Событие Error возникает, когда элемент управления проигрывателя Windows Media имеет условие ошибки.
ms.assetid: d28c18a9-c650-4169-989b-8727b7a5a831
keywords:
- Событие ошибки в проигрывателе Windows Media объекта Аксвиндовсмедиаплайер
topic_type:
- apiref
api_name:
- Error Event of the AxWindowsMediaPlayer Object
api_location:
- AxInterop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6cfd3571538aa2cdd263a9f5d57e479e73818806
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105694452"
---
# <a name="error-event-of-the-axwindowsmediaplayer-object"></a><span data-ttu-id="8a7e0-104">Событие Error объекта Аксвиндовсмедиаплайер</span><span class="sxs-lookup"><span data-stu-id="8a7e0-104">Error Event of the AxWindowsMediaPlayer Object</span></span>

<span data-ttu-id="8a7e0-105">Событие Error возникает, когда элемент управления проигрывателя Windows Media имеет условие ошибки.</span><span class="sxs-lookup"><span data-stu-id="8a7e0-105">The Error event occurs when the Windows Media Player control has an error condition.</span></span>

``` syntax
[C#]
private void player_ErrorEvent(
  object sender,
  System.EventArgs e
)

[Visual Basic]
Private Sub player_ErrorEvent(  
  sender As Object,  
  e As System.EventArgs
) Handles player.ErrorEvent
```

## <a name="event-data"></a><span data-ttu-id="8a7e0-106">Данные о событиях</span><span class="sxs-lookup"><span data-stu-id="8a7e0-106">Event Data</span></span>

<span data-ttu-id="8a7e0-107">Это событие не содержит данных.</span><span class="sxs-lookup"><span data-stu-id="8a7e0-107">This event does not contain data.</span></span>

## <a name="examples"></a><span data-ttu-id="8a7e0-108">Примеры</span><span class="sxs-lookup"><span data-stu-id="8a7e0-108">Examples</span></span>

<span data-ttu-id="8a7e0-109">В следующем примере создается обработчик событий для события Error для вывода текста описания первой ошибки в очереди ошибок.</span><span class="sxs-lookup"><span data-stu-id="8a7e0-109">The following example creates an event handler for the Error event to display the description text for the first error in the error queue.</span></span> <span data-ttu-id="8a7e0-110">Объект Аксвмплиб. Аксвиндовсмедиаплайер представлен переменной с именем Player.</span><span class="sxs-lookup"><span data-stu-id="8a7e0-110">The AxWMPLib.AxWindowsMediaPlayer object is represented by the variable named player.</span></span>


```CSharp
// Add a delegate for the Error event.
player.ErrorEvent += new EventHandler(player_ErrorEvent);

private void player_ErrorEvent(object sender, System.EventArgs e)
{
    // Get the description of the first error. 
    string errDesc = player.Error.get_Item(0).errorDescription;

    // Display the error description.
    System.Windows.Forms.MessageBox.Show(errDesc);
}
```


```VB

Public Sub player_ErrorEvent(ByVal sender As Object, ByVal e As System.EventArgs) Handles player.ErrorEvent

    &#39; Get the description of the first error. 
    Dim errDesc As String = player.Error.Item(0).errorDescription

    &#39; Display the error description.
    System.Windows.Forms.MessageBox.Show(errDesc)

End Sub
```





## <a name="requirements"></a><span data-ttu-id="8a7e0-111">Требования</span><span class="sxs-lookup"><span data-stu-id="8a7e0-111">Requirements</span></span>



| <span data-ttu-id="8a7e0-112">Требование</span><span class="sxs-lookup"><span data-stu-id="8a7e0-112">Requirement</span></span> | <span data-ttu-id="8a7e0-113">Значение</span><span class="sxs-lookup"><span data-stu-id="8a7e0-113">Value</span></span> |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8a7e0-114">Версия</span><span class="sxs-lookup"><span data-stu-id="8a7e0-114">Version</span></span><br/>   | <span data-ttu-id="8a7e0-115">Проигрыватель Windows Media 9 Series или более поздней версии</span><span class="sxs-lookup"><span data-stu-id="8a7e0-115">Windows Media Player 9 Series or later</span></span><br/>                                                                          |
| <span data-ttu-id="8a7e0-116">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="8a7e0-116">Namespace</span></span><br/> | <span data-ttu-id="8a7e0-117">**аксвмплиб**</span><span class="sxs-lookup"><span data-stu-id="8a7e0-117">**AxWMPLib**</span></span><br/>                                                                                                    |
| <span data-ttu-id="8a7e0-118">Сборка</span><span class="sxs-lookup"><span data-stu-id="8a7e0-118">Assembly</span></span><br/>  | <dl> <span data-ttu-id="8a7e0-119"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="8a7e0-119"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8a7e0-120">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="8a7e0-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8a7e0-121">**Объект Аксвиндовсмедиаплайер (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="8a7e0-121">**AxWindowsMediaPlayer Object (VB and C#)**</span></span>](axwindowsmediaplayer-object--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="8a7e0-122">**Ивмперрор. Item (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="8a7e0-122">**IWMPError.Item (VB and C#)**</span></span>](iwmperror-item--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="8a7e0-123">**Ивмперроритем. errorDescription (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="8a7e0-123">**IWMPErrorItem.errorDescription (VB and C#)**</span></span>](wmplibiwmperroritem-iwmperroritem-errordescription--vb-and-c.md)
</dt> </dl>

 

 





