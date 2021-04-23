---
title: Ивмпмедиаколлектион Сетделетед, метод
description: Метод Сетделетед перемещает указанный элемент мультимедиа в папку Удаленные элементы. | Ивмпмедиаколлектион Сетделетед, метод
ms.assetid: 3fa7989e-8b98-44e1-93ca-8136aba358ea
keywords:
- Сетделетед метод Windows Media Player
- Сетделетед метод проигрывателя Windows Media Player, интерфейс Ивмпмедиаколлектион
- Интерфейс Ивмпмедиаколлектион Windows Media Player, метод Сетделетед
topic_type:
- apiref
api_name:
- IWMPMediaCollection.setDeleted
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 57ccf8cf2d36ab7e4aaf76fdbe5c28582650fcda
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105699196"
---
# <a name="iwmpmediacollectionsetdeleted-method"></a><span data-ttu-id="7fd15-107">Метод Ивмпмедиаколлектион:: Сетделетед</span><span class="sxs-lookup"><span data-stu-id="7fd15-107">IWMPMediaCollection::setDeleted method</span></span>

<span data-ttu-id="7fd15-108">`setDeleted`Метод перемещает указанный элемент мультимедиа в папку Удаленные элементы.</span><span class="sxs-lookup"><span data-stu-id="7fd15-108">The `setDeleted` method moves the specified media item to the deleted items folder.</span></span>

## <a name="syntax"></a><span data-ttu-id="7fd15-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="7fd15-109">Syntax</span></span>


```CSharp
public void setDeleted(
  IWMPMedia pItem,
  System.Boolean varfIsDeleted
);
```


```VB

Public Sub setDeleted( _
  ByVal pItem As IWMPMedia, _
  ByVal varfIsDeleted As System.Boolean _
)
Implements IWMPMediaCollection.setDeleted
```





## <a name="parameters"></a><span data-ttu-id="7fd15-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="7fd15-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7fd15-111">*питем* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="7fd15-111">*pItem* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7fd15-112">Интерфейс **вмплиб. ивмпмедиа** для перемещаемого элемента.</span><span class="sxs-lookup"><span data-stu-id="7fd15-112">A **WMPLib.IWMPMedia** interface for the item to be moved.</span></span>

</dd> <dt>

<span data-ttu-id="7fd15-113">*варфисделетед* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="7fd15-113">*varfIsDeleted* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7fd15-114">Значение **System. Boolean** , указывающее, следует ли перемещать элемент в папку "удаленные элементы".</span><span class="sxs-lookup"><span data-stu-id="7fd15-114">A **System.Boolean** value that specifies whether the item should be moved to the deleted items folder.</span></span> <span data-ttu-id="7fd15-115">Это значение всегда должно быть **true**.</span><span class="sxs-lookup"><span data-stu-id="7fd15-115">This value must always be **true**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7fd15-116">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="7fd15-116">Return value</span></span>

<span data-ttu-id="7fd15-117">Этот метод не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="7fd15-117">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="7fd15-118">Комментарии</span><span class="sxs-lookup"><span data-stu-id="7fd15-118">Remarks</span></span>

<span data-ttu-id="7fd15-119">Этот метод не удаляет файлы с компьютера пользователя, а просто перемещает их в папку Удаленные элементы.</span><span class="sxs-lookup"><span data-stu-id="7fd15-119">This method does not remove files from the user's computer, it just moves them to the deleted items folder.</span></span>

<span data-ttu-id="7fd15-120">Перед вызовом этого метода необходимо иметь доступ на чтение к библиотеке.</span><span class="sxs-lookup"><span data-stu-id="7fd15-120">Before calling this method, you must have read access to the library.</span></span> <span data-ttu-id="7fd15-121">Дополнительные сведения см. в разделе [доступ к библиотеке](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="7fd15-121">For more information, see [Library Access](library-access.md).</span></span>

## <a name="examples"></a><span data-ttu-id="7fd15-122">Примеры</span><span class="sxs-lookup"><span data-stu-id="7fd15-122">Examples</span></span>

<span data-ttu-id="7fd15-123">В следующем примере используется `setDeleted` для перемещения определенного элемента мультимедиа в папку Удаленные элементы.</span><span class="sxs-lookup"><span data-stu-id="7fd15-123">The following example uses `setDeleted` to move a particular media item to the deleted items folder.</span></span> <span data-ttu-id="7fd15-124">Метод **IsDeleted** сначала проверяет, был ли уже удален элемент.</span><span class="sxs-lookup"><span data-stu-id="7fd15-124">The **isDeleted** method first tests whether the item has already been deleted.</span></span> <span data-ttu-id="7fd15-125">Объект **аксвмплиб. аксвиндовсмедиаплайер** представлен переменной с именем Player.</span><span class="sxs-lookup"><span data-stu-id="7fd15-125">The **AxWMPLib.AxWindowsMediaPlayer** object is represented by the variable named player.</span></span>


```CSharp
// Test whether the media item has already been deleted.
if (!player.mediaCollection.isDeleted(media))
{
    // The item is available to be deleted; move it to the deleted items folder.
    player.mediaCollection.setDeleted(media, true);

    // Inform the user that the operation succeeded.
    System.Windows.Forms.MessageBox.Show("Item moved to deleted items folder.");
}
else
{
    // Tell the user the operation is unnecessary.
    System.Windows.Forms.MessageBox.Show("Item is already deleted!");
}
```


```VB

' Test whether the media item has already been deleted.
If (Not player.mediaCollection.isDeleted(media)) Then

    &#39; The item is available to be deleted move it to the deleted items folder.
    player.mediaCollection.setDeleted(media, True)

    &#39; Inform the user that the operation succeeded.
    System.Windows.Forms.MessageBox.Show(&quot;Item moved to deleted items folder.&quot;)

Else

    &#39; Tell the user the operation is unnecessary.
    System.Windows.Forms.MessageBox.Show(&quot;Item is already deleted!&quot;)

End If
```





## <a name="requirements"></a><span data-ttu-id="7fd15-126">Требования</span><span class="sxs-lookup"><span data-stu-id="7fd15-126">Requirements</span></span>



| <span data-ttu-id="7fd15-127">Требование</span><span class="sxs-lookup"><span data-stu-id="7fd15-127">Requirement</span></span> | <span data-ttu-id="7fd15-128">Значение</span><span class="sxs-lookup"><span data-stu-id="7fd15-128">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7fd15-129">Версия</span><span class="sxs-lookup"><span data-stu-id="7fd15-129">Version</span></span><br/>   | <span data-ttu-id="7fd15-130">Проигрыватель Windows Media 9 Series или более поздней версии</span><span class="sxs-lookup"><span data-stu-id="7fd15-130">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="7fd15-131">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="7fd15-131">Namespace</span></span><br/> | <span data-ttu-id="7fd15-132">**вмплиб**</span><span class="sxs-lookup"><span data-stu-id="7fd15-132">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="7fd15-133">Сборка</span><span class="sxs-lookup"><span data-stu-id="7fd15-133">Assembly</span></span><br/>  | <dl> <span data-ttu-id="7fd15-134"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="7fd15-134"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7fd15-135">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="7fd15-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7fd15-136">**Интерфейс Ивмпмедиа (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="7fd15-136">**IWMPMedia Interface (VB and C#)**</span></span>](iwmpmedia--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="7fd15-137">**Интерфейс Ивмпмедиаколлектион (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="7fd15-137">**IWMPMediaCollection Interface (VB and C#)**</span></span>](iwmpmediacollection--vb-and-c.md)
</dt> </dl>

 

 





