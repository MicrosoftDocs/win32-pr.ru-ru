---
title: Ивмпмедиа Сетитеминфо, метод
description: Метод Сетитеминфо задает значение указанного атрибута для элемента мультимедиа.
ms.assetid: 247bbba5-7d9b-489d-8e41-ae8ec6e266fd
keywords:
- Сетитеминфо метод Windows Media Player
- Сетитеминфо метод проигрывателя Windows Media Player, интерфейс Ивмпмедиа
- Интерфейс Ивмпмедиа Windows Media Player, метод Сетитеминфо
topic_type:
- apiref
api_name:
- IWMPMedia.setItemInfo
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6702c80c13090a370e2922ccecade49bc06645de
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105668586"
---
# <a name="iwmpmediasetiteminfo-method"></a><span data-ttu-id="f3cb2-106">Метод Ивмпмедиа:: Сетитеминфо</span><span class="sxs-lookup"><span data-stu-id="f3cb2-106">IWMPMedia::setItemInfo method</span></span>

<span data-ttu-id="f3cb2-107">Метод **сетитеминфо** задает значение указанного атрибута для элемента мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="f3cb2-107">The **setItemInfo** method sets the value of the specified attribute for the media item.</span></span>

## <a name="syntax"></a><span data-ttu-id="f3cb2-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="f3cb2-108">Syntax</span></span>


```CSharp
public void setItemInfo(
  System.String bstrItemName,
  System.String bstrVal
);
```


```VB

Public Sub setItemInfo( _
  ByVal bstrItemName As System.String, _
  ByVal bstrVal As System.String _
)
Implements IWMPMedia.setItemInfo
```





## <a name="parameters"></a><span data-ttu-id="f3cb2-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="f3cb2-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f3cb2-110">*бстритемнаме* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="f3cb2-110">*bstrItemName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f3cb2-111">**Строка System. String** , которая является именем атрибута.</span><span class="sxs-lookup"><span data-stu-id="f3cb2-111">A **System.String** that is the attribute name.</span></span>

</dd> <dt>

<span data-ttu-id="f3cb2-112">*бстрвал* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="f3cb2-112">*bstrVal* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f3cb2-113">Значение **System. String** , которое является новым значением.</span><span class="sxs-lookup"><span data-stu-id="f3cb2-113">A **System.String** that is the new value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f3cb2-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="f3cb2-114">Return value</span></span>

<span data-ttu-id="f3cb2-115">Этот метод не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="f3cb2-115">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="f3cb2-116">Комментарии</span><span class="sxs-lookup"><span data-stu-id="f3cb2-116">Remarks</span></span>

<span data-ttu-id="f3cb2-117">Свойство **аттрибутекаунт** возвращает количество атрибутов, доступных для данного элемента мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="f3cb2-117">The **attributeCount** property gets the number of attributes available for a given media item.</span></span> <span data-ttu-id="f3cb2-118">Номера индексов можно использовать с методом **жетаттрибутенаме** для определения имен встроенных атрибутов, которые могут использоваться с этим методом.</span><span class="sxs-lookup"><span data-stu-id="f3cb2-118">Index numbers can then be used with the **getAttributeName** method to determine the names of the built-in attributes that can be used with this method.</span></span>

<span data-ttu-id="f3cb2-119">Перед использованием этого метода используйте метод **исреадонлитем** , чтобы определить, можно ли задать определенный атрибут.</span><span class="sxs-lookup"><span data-stu-id="f3cb2-119">Before using this method, use the **isReadOnlyItem** method to discover whether a particular attribute can be set.</span></span>

<span data-ttu-id="f3cb2-120">Перед вызовом этого метода необходимо иметь полный доступ к библиотеке.</span><span class="sxs-lookup"><span data-stu-id="f3cb2-120">Before calling this method, you must have full access to the library.</span></span> <span data-ttu-id="f3cb2-121">Дополнительные сведения см. в разделе [доступ к библиотеке](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="f3cb2-121">For more information, see [Library Access](library-access.md).</span></span>

<span data-ttu-id="f3cb2-122">Примечание</span><span class="sxs-lookup"><span data-stu-id="f3cb2-122">Note</span></span>

<span data-ttu-id="f3cb2-123">При внедрении элемента управления проигрывателя Windows Media в приложение измененные атрибуты файла не будут записываться в файл мультимедиа до тех пор, пока пользователь не запустит проигрыватель Windows Media.</span><span class="sxs-lookup"><span data-stu-id="f3cb2-123">If you embed the Windows Media Player control in your application, file attributes that you change will not be written to the digital media file until the user runs Windows Media Player.</span></span>

## <a name="examples"></a><span data-ttu-id="f3cb2-124">Примеры</span><span class="sxs-lookup"><span data-stu-id="f3cb2-124">Examples</span></span>

<span data-ttu-id="f3cb2-125">В следующем примере **сетитеминфо** используется для изменения значения атрибута жанра для текущего элемента мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="f3cb2-125">The following example uses **setItemInfo** to change the value of the Genre attribute for the current media item.</span></span> <span data-ttu-id="f3cb2-126">Текстовое поле позволяет пользователю ввести строку, которая затем используется для изменения сведений об атрибуте в ответ на событие щелчка кнопки.</span><span class="sxs-lookup"><span data-stu-id="f3cb2-126">A text box allows the user to enter a string, which is then used to change the attribute information in response to the Click event of a button.</span></span> <span data-ttu-id="f3cb2-127">Объект **аксвмплиб. аксвиндовсмедиаплайер** представлен переменной с именем Player.</span><span class="sxs-lookup"><span data-stu-id="f3cb2-127">The **AxWMPLib.AxWindowsMediaPlayer** object is represented by the variable named player.</span></span>


```CSharp
private void setNewGenre_Click(object sender, System.EventArgs e)
{
    // Store a WMPLib.IWMPMedia3 interface to the current media item. 
    WMPLib.IWMPMedia3 cm = (WMPLib.IWMPMedia3)player.currentMedia;

    // Get the user input from the TextBox. 
    string atValue = genText.Text;

    // Test for read-only status of the attribute. 
    if( cm.isReadOnlyItem("Genre") == false )
    {
        // Change the attribute value. 
        cm.setItemInfo("Genre", atValue);
    } 
}
```


```VB

Public Sub setNewGenre_Click(ByVal sender As Object, ByVal e As System.EventArgs) Handles setNewGenre.Click

    &#39; Store a WMPLib.IWMPMedia3 interface to the current media item. 
    Dim cm As WMPLib.IWMPMedia3 = player.currentMedia

    &#39; Get the user input from the TextBox. 
    Dim atValue = genText.Text

    &#39; Test for read-only status of the attribute. 
    If (cm.isReadOnlyItem(&quot;Genre&quot;) = False) Then

        &#39; Change the attribute value. 
        cm.setItemInfo(&quot;Genre&quot;, atValue)

    End If

End Sub
```





## <a name="requirements"></a><span data-ttu-id="f3cb2-128">Требования</span><span class="sxs-lookup"><span data-stu-id="f3cb2-128">Requirements</span></span>



| <span data-ttu-id="f3cb2-129">Требование</span><span class="sxs-lookup"><span data-stu-id="f3cb2-129">Requirement</span></span> | <span data-ttu-id="f3cb2-130">Значение</span><span class="sxs-lookup"><span data-stu-id="f3cb2-130">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f3cb2-131">Версия</span><span class="sxs-lookup"><span data-stu-id="f3cb2-131">Version</span></span><br/>   | <span data-ttu-id="f3cb2-132">Проигрыватель Windows Media 9 Series или более поздней версии</span><span class="sxs-lookup"><span data-stu-id="f3cb2-132">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="f3cb2-133">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="f3cb2-133">Namespace</span></span><br/> | <span data-ttu-id="f3cb2-134">**вмплиб**</span><span class="sxs-lookup"><span data-stu-id="f3cb2-134">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="f3cb2-135">Сборка</span><span class="sxs-lookup"><span data-stu-id="f3cb2-135">Assembly</span></span><br/>  | <dl> <span data-ttu-id="f3cb2-136"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="f3cb2-136"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f3cb2-137">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="f3cb2-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f3cb2-138">**Интерфейс Ивмпмедиа (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="f3cb2-138">**IWMPMedia Interface (VB and C#)**</span></span>](iwmpmedia--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="f3cb2-139">**Ивмпмедиа. Аттрибутекаунт (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="f3cb2-139">**IWMPMedia.attributeCount (VB and C#)**</span></span>](wmplibiwmpmedia-iwmpmedia-attributecount--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="f3cb2-140">**Ивмпмедиа. Жетаттрибутенаме (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="f3cb2-140">**IWMPMedia.getAttributeName (VB and C#)**</span></span>](wmplibiwmpmedia-iwmpmedia-getattributename--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="f3cb2-141">**Ивмпмедиа. Исреадонлитем (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="f3cb2-141">**IWMPMedia.isReadOnlyItem (VB and C#)**</span></span>](wmplibiwmpmedia-iwmpmedia-isreadonlyitem--vb-and-c.md)
</dt> </dl>

 

 





