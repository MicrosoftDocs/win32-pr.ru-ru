---
title: Ивмпмедиаколлектион Жетаттрибутестрингколлектион, метод
description: Метод Жетаттрибутестрингколлектион возвращает интерфейс Ивмпстрингколлектион, представляющий набор всех значений для указанного атрибута в типе мультимедиа.
ms.assetid: 5ac19c04-75db-4618-9c4e-b20e2f709024
keywords:
- Жетаттрибутестрингколлектион метод Windows Media Player
- Жетаттрибутестрингколлектион метод проигрывателя Windows Media Player, интерфейс Ивмпмедиаколлектион
- Интерфейс Ивмпмедиаколлектион Windows Media Player, метод Жетаттрибутестрингколлектион
topic_type:
- apiref
api_name:
- IWMPMediaCollection.getAttributeStringCollection
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bef25cd811890e82273fd5d634633e25e7ec460c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105669484"
---
# <a name="iwmpmediacollectiongetattributestringcollection-method"></a><span data-ttu-id="7edb5-106">Метод Ивмпмедиаколлектион:: Жетаттрибутестрингколлектион</span><span class="sxs-lookup"><span data-stu-id="7edb5-106">IWMPMediaCollection::getAttributeStringCollection method</span></span>

<span data-ttu-id="7edb5-107">Метод **жетаттрибутестрингколлектион** возвращает интерфейс **ивмпстрингколлектион** , представляющий набор всех значений для указанного атрибута в типе мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="7edb5-107">The **getAttributeStringCollection** method returns an **IWMPStringCollection** interface that represents the set of all values for a specified attribute within a media type.</span></span>

## <a name="syntax"></a><span data-ttu-id="7edb5-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="7edb5-108">Syntax</span></span>


```CSharp
public IWMPStringCollection getAttributeStringCollection(
  System.String bstrAttribute,
  System.String bstrMediaType
);
```


```VB

Public Function getAttributeStringCollection( _
  ByVal bstrAttribute As System.String, _
  ByVal bstrMediaType As System.String _
) As IWMPStringCollection
Implements IWMPMediaCollection.getAttributeStringCollection
```





## <a name="parameters"></a><span data-ttu-id="7edb5-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="7edb5-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7edb5-110">*бстраттрибуте* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="7edb5-110">*bstrAttribute* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7edb5-111">**Строка System. String** , которая является атрибутом, для которого извлекаются значения.</span><span class="sxs-lookup"><span data-stu-id="7edb5-111">A **System.String** that is the attribute for which the values are retrieved.</span></span>

</dd> <dt>

<span data-ttu-id="7edb5-112">*бстрмедиатипе* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="7edb5-112">*bstrMediaType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7edb5-113">**Строка System. String** , представляющая тип носителя, для которого извлекаются значения.</span><span class="sxs-lookup"><span data-stu-id="7edb5-113">A **System.String** that is the media type for which the values are retrieved.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7edb5-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="7edb5-114">Return value</span></span>

<span data-ttu-id="7edb5-115">Интерфейс **вмплиб. ивмпстрингколлектион** для извлеченных значений.</span><span class="sxs-lookup"><span data-stu-id="7edb5-115">A **WMPLib.IWMPStringCollection** interface for the retrieved values.</span></span>

## <a name="remarks"></a><span data-ttu-id="7edb5-116">Комментарии</span><span class="sxs-lookup"><span data-stu-id="7edb5-116">Remarks</span></span>

<span data-ttu-id="7edb5-117">Перед вызовом этого метода необходимо иметь доступ на чтение к библиотеке.</span><span class="sxs-lookup"><span data-stu-id="7edb5-117">Before calling this method, you must have read access to the library.</span></span> <span data-ttu-id="7edb5-118">Дополнительные сведения см. в разделе [доступ к библиотеке](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="7edb5-118">For more information, see [Library Access](library-access.md).</span></span>

<span data-ttu-id="7edb5-119">Сведения об атрибутах, поддерживаемых проигрывателем Windows Media, см. в [справочнике по атрибутам](attribute-reference.md).</span><span class="sxs-lookup"><span data-stu-id="7edb5-119">For information about the attributes supported by Windows Media Player, see the [Attribute Reference](attribute-reference.md).</span></span>

## <a name="examples"></a><span data-ttu-id="7edb5-120">Примеры</span><span class="sxs-lookup"><span data-stu-id="7edb5-120">Examples</span></span>

<span data-ttu-id="7edb5-121">В следующем примере **жетаттрибутестрингколлектион** используется для вывода списка значений, соответствующих определенному атрибуту для звуковых элементов в коллекции мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="7edb5-121">The following example uses **getAttributeStringCollection** to display a list of values that correspond to a particular attribute for audio items in the media collection.</span></span> <span data-ttu-id="7edb5-122">Поле со списком позволяет пользователю выбрать атрибут, например исполнитель, жанр или альбом, а также многострочное текстовое поле, в котором отображается результат.</span><span class="sxs-lookup"><span data-stu-id="7edb5-122">A list box allows the user to select an attribute, such as Artist, Genre, or Album and a multi-line text box displays the result.</span></span> <span data-ttu-id="7edb5-123">Объект **аксвмплиб. аксвиндовсмедиаплайер** представлен переменной с именем Player.</span><span class="sxs-lookup"><span data-stu-id="7edb5-123">The **AxWMPLib.AxWindowsMediaPlayer** object is represented by the variable named player.</span></span>


```CSharp
private void audioAttributes_OnSelectedIndexChanged(object sender, System.EventArgs e)
{
    // Retrieve the attribute type from the ListBox
    string attributeType = (string)((System.Windows.Forms.ListBox)sender).SelectedItem;

    // Get an interface to the mediaCollection.  
    WMPLib.IWMPMediaCollection2 library = (WMPLib.IWMPMediaCollection2)player.mediaCollection;

    // Get an interface to the string collection for the attribute type the user selects.
    WMPLib.IWMPStringCollection2 all = (WMPLib.IWMPStringCollection2)library.getAttributeStringCollection(attributeType, "Audio");

    // Clear the text box of previous results.
    attributeValues.Clear();

    // Create an array to hold the attribute values.
    string[] attributeArray = new string[all.count];
    
    // Loop through the string collection.
    for (int i = 0; i < all.count; i++)
    {
        // Store the items in the array.
        attributeArray[i] = all.Item(i);
    }

    // Display the items in the text box.
    attributeValues.Lines = attributeArray;
}
```


```VB

Public Sub audioAttributes_OnSelectedIndexChanged(ByVal sender As Object, ByVal e As System.EventArgs) Handles audioAttributes.SelectedIndexChanged

    &#39; Retrieve the attribute type from the ListBox
    Dim lb As System.Windows.Forms.ListBox = sender
    Dim attributeType As String = lb.SelectedItem

    &#39; Get an interface to the mediaCollection.  
    Dim library As WMPLib.IWMPMediaCollection2 = player.mediaCollection

    &#39; Get an interface to the string collection for the attribute type the user selects.
    Dim all As WMPLib.IWMPStringCollection2 = library.getAttributeStringCollection(attributeType, &quot;Audio&quot;)

    &#39; Clear the text box of previous results.
    attributeValues.Clear()

    &#39; Create an array to hold the attribute values.
    Dim attributeArray(all.count) As String

    &#39; Loop through the string collection.
    For i As Integer = 0 To (all.count - 1)

        &#39; Store the items in the array.
        attributeArray(i) = all.Item(i)

    Next i

    &#39; Display the items in the text box.
    attributeValues.Lines = attributeArray

End Sub
```





## <a name="requirements"></a><span data-ttu-id="7edb5-124">Требования</span><span class="sxs-lookup"><span data-stu-id="7edb5-124">Requirements</span></span>



| <span data-ttu-id="7edb5-125">Требование</span><span class="sxs-lookup"><span data-stu-id="7edb5-125">Requirement</span></span> | <span data-ttu-id="7edb5-126">Значение</span><span class="sxs-lookup"><span data-stu-id="7edb5-126">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7edb5-127">Версия</span><span class="sxs-lookup"><span data-stu-id="7edb5-127">Version</span></span><br/>   | <span data-ttu-id="7edb5-128">Проигрыватель Windows Media 9 Series или более поздней версии</span><span class="sxs-lookup"><span data-stu-id="7edb5-128">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="7edb5-129">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="7edb5-129">Namespace</span></span><br/> | <span data-ttu-id="7edb5-130">**вмплиб**</span><span class="sxs-lookup"><span data-stu-id="7edb5-130">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="7edb5-131">Сборка</span><span class="sxs-lookup"><span data-stu-id="7edb5-131">Assembly</span></span><br/>  | <dl> <span data-ttu-id="7edb5-132"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="7edb5-132"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7edb5-133">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="7edb5-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7edb5-134">**Интерфейс Ивмпмедиаколлектион (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="7edb5-134">**IWMPMediaCollection Interface (VB and C#)**</span></span>](iwmpmediacollection--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="7edb5-135">**Интерфейс Ивмпстрингколлектион (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="7edb5-135">**IWMPStringCollection Interface (VB and C#)**</span></span>](iwmpstringcollection--vb-and-c.md)
</dt> </dl>

 

 





