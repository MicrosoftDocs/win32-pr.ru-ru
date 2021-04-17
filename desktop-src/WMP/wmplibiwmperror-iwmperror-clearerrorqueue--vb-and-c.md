---
title: Ивмперрор Клеарерроркуеуе, метод
description: Метод Клеарерроркуеуе удаляет ошибки из очереди ошибок. | Ивмперрор Клеарерроркуеуе, метод
ms.assetid: a8e8e666-56e4-4e75-9ed5-2714d272ce7c
keywords:
- Клеарерроркуеуе метод Windows Media Player
- Клеарерроркуеуе метод проигрывателя Windows Media Player, интерфейс Ивмперрор
- Интерфейс Ивмперрор Windows Media Player, метод Клеарерроркуеуе
topic_type:
- apiref
api_name:
- IWMPError.clearErrorQueue
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 98c3f422a9bc32049106d83c970bd8d2c9b2110f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105708544"
---
# <a name="iwmperrorclearerrorqueue-method"></a><span data-ttu-id="4d620-107">Метод Ивмперрор:: Клеарерроркуеуе</span><span class="sxs-lookup"><span data-stu-id="4d620-107">IWMPError::clearErrorQueue method</span></span>

<span data-ttu-id="4d620-108">Метод **клеарерроркуеуе** удаляет ошибки из очереди ошибок.</span><span class="sxs-lookup"><span data-stu-id="4d620-108">The **clearErrorQueue** method clears the errors from the error queue.</span></span>

## <a name="syntax"></a><span data-ttu-id="4d620-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="4d620-109">Syntax</span></span>


```CSharp
public void clearErrorQueue();
```


```VB

Public Sub clearErrorQueue()
Implements IWMPError.clearErrorQueue
```





## <a name="parameters"></a><span data-ttu-id="4d620-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="4d620-110">Parameters</span></span>

<span data-ttu-id="4d620-111">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="4d620-111">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="4d620-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="4d620-112">Return value</span></span>

<span data-ttu-id="4d620-113">Этот метод не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="4d620-113">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="4d620-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="4d620-114">Remarks</span></span>

<span data-ttu-id="4d620-115">Используйте этот метод, чтобы очистить очередь ошибок после обработки ряда ошибок.</span><span class="sxs-lookup"><span data-stu-id="4d620-115">Use this method to clear the error queue after a series of errors has been processed.</span></span>

<span data-ttu-id="4d620-116">Если выбрано отображение настраиваемых сообщений об ошибках, следует задать для **ивмпсеттингс. енаблиррордиалогс** **значение false** .</span><span class="sxs-lookup"><span data-stu-id="4d620-116">You should set **IWMPSettings.enableErrorDialogs** to **false** if you choose to display custom error messages.</span></span>

## <a name="examples"></a><span data-ttu-id="4d620-117">Примеры</span><span class="sxs-lookup"><span data-stu-id="4d620-117">Examples</span></span>

<span data-ttu-id="4d620-118">В следующем примере используется **клеарерроркуеуе** в обработчике событий ошибки для очистки очереди ошибок после отображения всех описаний ошибок.</span><span class="sxs-lookup"><span data-stu-id="4d620-118">The following example uses **clearErrorQueue** in an Error event handler to empty the error queue after all error descriptions have been displayed.</span></span> <span data-ttu-id="4d620-119">Объект **аксвмплиб. аксвиндовсмедиаплайер** представлен переменной с именем Player.</span><span class="sxs-lookup"><span data-stu-id="4d620-119">The **AxWMPLib.AxWindowsMediaPlayer** object is represented by the variable named player.</span></span>


```CSharp
private void player_ErrorEvent_clearErrorQueue(object sender, System.EventArgs e)
{
    // Store the number of errors in the queue.
    int max = player.Error.errorCount;

    // Loop through the list of errors.
    for (int i = 0; i < max; i++)
    {
        // Get the description for this error.
        string errDesc = player.Error.get_Item(i).errorDescription;

        // Display the error message.
        System.Windows.Forms.MessageBox.Show(errDesc);
    }

    // Clear the error queue to prepare for the next group of errors.
    player.Error.clearErrorQueue();
}
```


```VB

Public Sub player_ErrorEvent_clearErrorQueue(ByVal sender As Object, ByVal e As System.EventArgs) Handles player.ErrorEvent

    &#39; Store the number of errors in the queue.
    Dim max As Integer = player.Error.errorCount

    &#39; Loop through the list of errors.
    For i As Integer = 0 To (max - 1)

        &#39; Get the description for this error.
        Dim errDesc As String = player.Error.Item(i).errorDescription

        &#39; Display the error message.
        System.Windows.Forms.MessageBox.Show(errDesc)

    Next i

    &#39; Clear the error queue to prepare for the next group of errors.
    player.Error.clearErrorQueue()

End Sub
```





## <a name="requirements"></a><span data-ttu-id="4d620-120">Требования</span><span class="sxs-lookup"><span data-stu-id="4d620-120">Requirements</span></span>



| <span data-ttu-id="4d620-121">Требование</span><span class="sxs-lookup"><span data-stu-id="4d620-121">Requirement</span></span> | <span data-ttu-id="4d620-122">Значение</span><span class="sxs-lookup"><span data-stu-id="4d620-122">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4d620-123">Версия</span><span class="sxs-lookup"><span data-stu-id="4d620-123">Version</span></span><br/>   | <span data-ttu-id="4d620-124">Проигрыватель Windows Media 9 Series или более поздней версии</span><span class="sxs-lookup"><span data-stu-id="4d620-124">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="4d620-125">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="4d620-125">Namespace</span></span><br/> | <span data-ttu-id="4d620-126">**вмплиб**</span><span class="sxs-lookup"><span data-stu-id="4d620-126">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="4d620-127">Сборка</span><span class="sxs-lookup"><span data-stu-id="4d620-127">Assembly</span></span><br/>  | <dl> <span data-ttu-id="4d620-128"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="4d620-128"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4d620-129">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="4d620-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4d620-130">**Интерфейс Ивмперрор (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="4d620-130">**IWMPError Interface (VB and C#)**</span></span>](iwmperror--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="4d620-131">**Ивмпсеттингс. Енаблиррордиалогс (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="4d620-131">**IWMPSettings.enableErrorDialogs (VB and C#)**</span></span>](wmplibiwmpsettings-iwmpsettings-enableerrordialogs--vb-and-c.md)
</dt> </dl>

 

 





