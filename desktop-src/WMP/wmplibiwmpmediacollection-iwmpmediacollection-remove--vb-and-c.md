---
title: Ивмпмедиаколлектион Remove, метод
description: Метод Remove удаляет указанный элемент из коллекции носителей.
ms.assetid: 2ed45159-0a92-4353-8bf1-1d20de404bf7
keywords:
- метод Remove Windows Media Player
- метод Remove Windows Media Player, интерфейс Ивмпмедиаколлектион
- Интерфейс Ивмпмедиаколлектион Windows Media Player, Remove, метод
topic_type:
- apiref
api_name:
- IWMPMediaCollection.remove
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d341f8974255dab5e3cdce356a9b221eddff193c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105699197"
---
# <a name="iwmpmediacollectionremove-method"></a><span data-ttu-id="84389-106">Метод Ивмпмедиаколлектион:: Remove</span><span class="sxs-lookup"><span data-stu-id="84389-106">IWMPMediaCollection::remove method</span></span>

<span data-ttu-id="84389-107">`remove`Метод удаляет указанный элемент из коллекции носителей.</span><span class="sxs-lookup"><span data-stu-id="84389-107">The `remove` method removes a specified item from the media collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="84389-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="84389-108">Syntax</span></span>


```CSharp
public void remove(
  IWMPMedia pItem,
  System.Boolean varfDeleteFile
);
```


```VB

Public Sub remove( _
  ByVal pItem As IWMPMedia, _
  ByVal varfDeleteFile As System.Boolean _
)
Implements IWMPMediaCollection.remove
```





## <a name="parameters"></a><span data-ttu-id="84389-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="84389-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="84389-110">*питем* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="84389-110">*pItem* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="84389-111">Интерфейс **вмплиб. ивмпмедиа** , определяющий удаляемый элемент.</span><span class="sxs-lookup"><span data-stu-id="84389-111">A **WMPLib.IWMPMedia** interface that identifies the item to remove.</span></span>

</dd> <dt>

<span data-ttu-id="84389-112">*варфделетефиле* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="84389-112">*varfDeleteFile* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="84389-113">Значение **System. Boolean** , указывающее, должен ли метод удалить указанный элемент из библиотеки.</span><span class="sxs-lookup"><span data-stu-id="84389-113">A **System.Boolean** value that specifies whether the method should remove the specified item from the library.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="84389-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="84389-114">Return value</span></span>

<span data-ttu-id="84389-115">Этот метод не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="84389-115">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="84389-116">Комментарии</span><span class="sxs-lookup"><span data-stu-id="84389-116">Remarks</span></span>

<span data-ttu-id="84389-117">Этот метод удаляет элемент из библиотеки.</span><span class="sxs-lookup"><span data-stu-id="84389-117">This method deletes an item from the library.</span></span> <span data-ttu-id="84389-118">Этот метод не удаляет файлы с компьютера пользователя.</span><span class="sxs-lookup"><span data-stu-id="84389-118">This method does not delete files from the user's computer.</span></span>

<span data-ttu-id="84389-119">Перед вызовом этого метода необходимо иметь доступ на чтение к библиотеке.</span><span class="sxs-lookup"><span data-stu-id="84389-119">Before calling this method, you must have read access to the library.</span></span> <span data-ttu-id="84389-120">Дополнительные сведения см. в разделе [доступ к библиотеке](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="84389-120">For more information, see [Library Access](library-access.md).</span></span>

## <a name="examples"></a><span data-ttu-id="84389-121">Примеры</span><span class="sxs-lookup"><span data-stu-id="84389-121">Examples</span></span>

<span data-ttu-id="84389-122">В следующем примере после запроса пользователя окончательно удаляется первый элемент мультимедиа из коллекции мультимедиа с помощью `remove` .</span><span class="sxs-lookup"><span data-stu-id="84389-122">The following example, after prompting the user, permanently deletes the first media item in the media collection by using `remove`.</span></span> <span data-ttu-id="84389-123">Объект Аксвмплиб. Аксвиндовсмедиаплайер представлен переменной с именем Player.</span><span class="sxs-lookup"><span data-stu-id="84389-123">The AxWMPLib.AxWindowsMediaPlayer object is represented by the variable named player.</span></span>


```CSharp
// Get an interface to the first item from the media collection. 
WMPLib.IWMPMedia3 media = (WMPLib.IWMPMedia3)player.mediaCollection.getAll().get_Item(0);

// Store the name of the retrieved media item.
string mediaName = media.name;

// Prepare a message, a caption and buttons for the user prompt.
string message = ("OK to permanently delete " + mediaName + "?");
string caption = "Confirm deletion";
System.Windows.Forms.MessageBoxButtons buttons = System.Windows.Forms.MessageBoxButtons.OKCancel;

// Prompt the user for permission to delete the object.
System.Windows.Forms.DialogResult result = System.Windows.Forms.MessageBox.Show(message, caption, buttons);

// Check the user response.
if (result == System.Windows.Forms.DialogResult.OK)
{
    // Permanently delete the item.
    player.mediaCollection.remove(media, true);

    // Report that the item was deleted.
    System.Windows.Forms.MessageBox.Show("Deleted item " + mediaName);
}
```


```VB

' Get an interface to the first item from the media collection. 
Dim media As WMPLib.IWMPMedia3 = player.mediaCollection.getAll().Item(0)

&#39; Store the name of the retrieved media item.
Dim mediaName As String = media.name

&#39; Prepare a message, a caption and buttons for the user prompt.
Dim message As String = (&quot;OK to permanently delete &quot; + mediaName + &quot;?&quot;)
Dim caption As String = &quot;Confirm deletion&quot;
Dim buttons As System.Windows.Forms.MessageBoxButtons = System.Windows.Forms.MessageBoxButtons.OKCancel

&#39; Prompt the user for permission to delete the object.
Dim result As System.Windows.Forms.DialogResult = System.Windows.Forms.MessageBox.Show(message, caption, buttons)

&#39; Check the user response.
If (result = System.Windows.Forms.DialogResult.OK) Then

    &#39; Permanently delete the item.
    player.mediaCollection.remove(media, True)

    &#39; Report that the item was deleted.
    System.Windows.Forms.MessageBox.Show(&quot;Deleted item &quot; + mediaName)

End If
```





## <a name="requirements"></a><span data-ttu-id="84389-124">Требования</span><span class="sxs-lookup"><span data-stu-id="84389-124">Requirements</span></span>



| <span data-ttu-id="84389-125">Требование</span><span class="sxs-lookup"><span data-stu-id="84389-125">Requirement</span></span> | <span data-ttu-id="84389-126">Значение</span><span class="sxs-lookup"><span data-stu-id="84389-126">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="84389-127">Версия</span><span class="sxs-lookup"><span data-stu-id="84389-127">Version</span></span><br/>   | <span data-ttu-id="84389-128">Проигрыватель Windows Media 9 Series или более поздней версии</span><span class="sxs-lookup"><span data-stu-id="84389-128">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="84389-129">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="84389-129">Namespace</span></span><br/> | <span data-ttu-id="84389-130">**вмплиб**</span><span class="sxs-lookup"><span data-stu-id="84389-130">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="84389-131">Сборка</span><span class="sxs-lookup"><span data-stu-id="84389-131">Assembly</span></span><br/>  | <dl> <span data-ttu-id="84389-132"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="84389-132"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="84389-133">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="84389-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="84389-134">**Интерфейс Ивмпмедиа (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="84389-134">**IWMPMedia Interface (VB and C#)**</span></span>](iwmpmedia--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="84389-135">**Интерфейс Ивмпмедиаколлектион (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="84389-135">**IWMPMediaCollection Interface (VB and C#)**</span></span>](iwmpmediacollection--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="84389-136">**Ивмпмедиаколлектион. Add (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="84389-136">**IWMPMediaCollection.add (VB and C#)**</span></span>](wmplibiwmpmediacollection-iwmpmediacollection-add--vb-and-c.md)
</dt> </dl>

 

 





