---
title: Ивмперрор. Item (VB и C)
description: Свойство Item ( \_ метод Get Item в C \) получает интерфейс ивмперроритем по указанному индексу в очереди ошибок.
ms.assetid: acfaaaa5-eb13-4ba0-8417-4229adc62c5d
keywords:
- Проигрыватель Windows Media Ивмперрор. Item (VB и C)
topic_type:
- apiref
api_name:
- IWMPError.Item (VB and C )
api_location:
- Interop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e9217ec772512171c828dd0dad06ec8fe3704dba
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105688919"
---
# <a name="iwmperroritem-vb-and-c"></a><span data-ttu-id="4d254-104">Ивмперрор. Item (VB и C#)</span><span class="sxs-lookup"><span data-stu-id="4d254-104">IWMPError.Item (VB and C#)</span></span>

<span data-ttu-id="4d254-105">Свойство **Item** (метод **Get \_ Item** в C#) получает интерфейс **ивмперроритем** по указанному индексу в очереди ошибок.</span><span class="sxs-lookup"><span data-stu-id="4d254-105">The **Item** property (the **get\_Item** method in C#) gets an **IWMPErrorItem** interface at the specified index in the error queue.</span></span>


```
[Visual Basic]
ReadOnly Property Item(
  dwIndex As System.Integer
) As IWMPErrorItem
```




```
[C#]
IWMPErrorItem get_Item (
  System.Int32 dwIndex
);
```



## <a name="parameters"></a><span data-ttu-id="4d254-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="4d254-106">Parameters</span></span>

<span data-ttu-id="4d254-107">*двиндекс*</span><span class="sxs-lookup"><span data-stu-id="4d254-107">*dwIndex*</span></span>

<span data-ttu-id="4d254-108">Объект **System. Int32** , который является начинающимся с нуля индексом интерфейса **ивмперроритем** в очереди ошибок.</span><span class="sxs-lookup"><span data-stu-id="4d254-108">A **System.Int32** that is the zero-based index of an **IWMPErrorItem** interface in the error queue.</span></span>

## <a name="property-value"></a><span data-ttu-id="4d254-109">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="4d254-109">Property Value</span></span>

<span data-ttu-id="4d254-110">Интерфейс **вмплиб. ивмперроритем** .</span><span class="sxs-lookup"><span data-stu-id="4d254-110">A **WMPLib.IWMPErrorItem** interface.</span></span>

## <a name="remarks"></a><span data-ttu-id="4d254-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="4d254-111">Remarks</span></span>

<span data-ttu-id="4d254-112">Проигрыватель Windows Media может создавать ряд ошибок в ответ на состояние ошибки.</span><span class="sxs-lookup"><span data-stu-id="4d254-112">Windows Media Player can generate a number of errors in response to an error condition.</span></span> <span data-ttu-id="4d254-113">Это свойство возвращает определенную ошибку в очереди с помощью номера индекса.</span><span class="sxs-lookup"><span data-stu-id="4d254-113">This property gets a specific error in the queue by using an index number.</span></span> <span data-ttu-id="4d254-114">Номера индексов для очереди ошибок начинаются с нуля.</span><span class="sxs-lookup"><span data-stu-id="4d254-114">The index numbers for the error queue begin with zero.</span></span>

<span data-ttu-id="4d254-115">Если выбрано отображение настраиваемых сообщений об ошибках, следует задать для **ивмпсеттингс. енаблиррордиалогс** **значение false** .</span><span class="sxs-lookup"><span data-stu-id="4d254-115">You should set **IWMPSettings.enableErrorDialogs** to **false** if you choose to display custom error messages.</span></span>

## <a name="examples"></a><span data-ttu-id="4d254-116">Примеры</span><span class="sxs-lookup"><span data-stu-id="4d254-116">Examples</span></span>

<span data-ttu-id="4d254-117">В следующем примере свойство **Item** (метод **Get \_ Item** в C#) используется в обработчике событий ошибок для получения и вывода сведений о последней ошибке в очереди ошибок.</span><span class="sxs-lookup"><span data-stu-id="4d254-117">The following example uses the **Item** property (the **get\_Item** method in C#) in an Error event handler to retrieve and display information about the most recent error in the error queue.</span></span> <span data-ttu-id="4d254-118">Объект **аксвмплиб. аксвиндовсмедиаплайер** представлен переменной с именем Player.</span><span class="sxs-lookup"><span data-stu-id="4d254-118">The **AxWMPLib.AxWindowsMediaPlayer** object is represented by the variable named player.</span></span>


```CSharp
private void player_ErrorEvent_get_Item(object sender, System.EventArgs e)
{
    // Store the index of the most recent error.
    int max = (player.Error.errorCount - 1);

    // Get an interface for the most recent error item. Cast it to
    // a WMPLib.IWMPErrorItem2 interface to get all of the available functionality.
    WMPLib.IWMPErrorItem2 errItem = (WMPLib.IWMPErrorItem2)player.Error.get_Item(max);

    // Use the interface to access and store the error info.
    int errNum = errItem.errorCode;
    string errDesc = errItem.errorDescription;

    // Display the error info.
    System.Windows.Forms.MessageBox.Show(errNum.ToString() + ":  " + errDesc);
}
```


```VB

Public Sub player_ErrorEvent_get_Item(ByVal sender As Object, ByVal e As System.EventArgs) Handles player.ErrorEvent

    &#39; Store the index of the most recent error.
    Dim max As Integer = (player.Error.errorCount - 1)

    &#39; Get an interface for the most recent error item. 
    Dim errItem As WMPLib.IWMPErrorItem2 = player.Error.Item(max)

    &#39; Use the interface to access and store the error info.
    Dim errNum As Integer = errItem.errorCode
    Dim errDesc As String = errItem.errorDescription

    &#39; Display the error info.
    System.Windows.Forms.MessageBox.Show(errNum.ToString() + &quot;:  &quot; + errDesc)

End Sub
```





## <a name="requirements"></a><span data-ttu-id="4d254-119">Требования</span><span class="sxs-lookup"><span data-stu-id="4d254-119">Requirements</span></span>



| <span data-ttu-id="4d254-120">Требование</span><span class="sxs-lookup"><span data-stu-id="4d254-120">Requirement</span></span> | <span data-ttu-id="4d254-121">Значение</span><span class="sxs-lookup"><span data-stu-id="4d254-121">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4d254-122">Версия</span><span class="sxs-lookup"><span data-stu-id="4d254-122">Version</span></span><br/>   | <span data-ttu-id="4d254-123">Проигрыватель Windows Media 9 Series или более поздней версии</span><span class="sxs-lookup"><span data-stu-id="4d254-123">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="4d254-124">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="4d254-124">Namespace</span></span><br/> | <span data-ttu-id="4d254-125">**вмплиб**</span><span class="sxs-lookup"><span data-stu-id="4d254-125">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="4d254-126">Сборка</span><span class="sxs-lookup"><span data-stu-id="4d254-126">Assembly</span></span><br/>  | <dl> <span data-ttu-id="4d254-127"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="4d254-127"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4d254-128">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="4d254-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4d254-129">**Интерфейс Ивмперрор (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="4d254-129">**IWMPError Interface (VB and C#)**</span></span>](iwmperror--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="4d254-130">**Интерфейс Ивмперроритем (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="4d254-130">**IWMPErrorItem Interface (VB and C#)**</span></span>](iwmperroritem--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="4d254-131">**Ивмпсеттингс. Енаблиррордиалогс (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="4d254-131">**IWMPSettings.enableErrorDialogs (VB and C#)**</span></span>](wmplibiwmpsettings-iwmpsettings-enableerrordialogs--vb-and-c.md)
</dt> </dl>

 

 





