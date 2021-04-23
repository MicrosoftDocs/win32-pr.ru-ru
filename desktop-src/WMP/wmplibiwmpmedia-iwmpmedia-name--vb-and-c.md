---
title: Ивмпмедиа имя свойства
description: Свойство Name возвращает или задает имя элемента мультимедиа.
ms.assetid: d1057871-bccf-4f84-9b1d-74c41a8f7f7c
keywords:
- свойство Name проигрыватель Windows Media Player
- свойство Name проигрыватель Windows Media Player, интерфейс Ивмпмедиа
- Интерфейс Ивмпмедиа Windows Media Player, свойство Name
topic_type:
- apiref
api_name:
- IWMPMedia.name
- IWMPMedia.get_name
- IWMPMedia.put_name
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5c526fc9847b06d0f7b6f4ebadf71761fd29a9d9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105669241"
---
# <a name="iwmpmedianame-property"></a><span data-ttu-id="f3685-106">Свойство Ивмпмедиа:: Name</span><span class="sxs-lookup"><span data-stu-id="f3685-106">IWMPMedia::name property</span></span>

<span data-ttu-id="f3685-107">Свойство **Name** Возвращает или задает имя элемента мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="f3685-107">The **name** property gets or sets the name of the media item.</span></span>

<span data-ttu-id="f3685-108">Это свойство доступно для чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="f3685-108">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="f3685-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="f3685-109">Syntax</span></span>


```CSharp
public System.String name {get; set;}
```


```VB

Public Property name As System.String
```





## <a name="property-value"></a><span data-ttu-id="f3685-110">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="f3685-110">Property value</span></span>

<span data-ttu-id="f3685-111">**Строка System. String** , которая является именем элемента мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="f3685-111">A **System.String** that is the name of the media item.</span></span>

## <a name="remarks"></a><span data-ttu-id="f3685-112">Комментарии</span><span class="sxs-lookup"><span data-stu-id="f3685-112">Remarks</span></span>

<span data-ttu-id="f3685-113">Перед использованием этого свойства необходимо иметь доступ на чтение к библиотеке.</span><span class="sxs-lookup"><span data-stu-id="f3685-113">Before using this property, you must have read access to the library.</span></span> <span data-ttu-id="f3685-114">Дополнительные сведения см. в разделе [доступ к библиотеке](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="f3685-114">For more information, see [Library Access](library-access.md).</span></span>

## <a name="examples"></a><span data-ttu-id="f3685-115">Примеры</span><span class="sxs-lookup"><span data-stu-id="f3685-115">Examples</span></span>

<span data-ttu-id="f3685-116">В следующем примере используется **имя** для изменения имени текущего элемента мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="f3685-116">The following example uses **name** to change the name of the current media item.</span></span> <span data-ttu-id="f3685-117">Текстовое поле позволяет пользователю ввести новое имя, а имя изменится в ответ на событие щелчка кнопки.</span><span class="sxs-lookup"><span data-stu-id="f3685-117">A text box allows the user to enter a new name, and the name is changed in response to the Click event of a button.</span></span> <span data-ttu-id="f3685-118">Объект **аксвмплиб. аксвиндовсмедиаплайер** представлен переменной с именем Player.</span><span class="sxs-lookup"><span data-stu-id="f3685-118">The **AxWMPLib.AxWindowsMediaPlayer** object is represented by the variable named player.</span></span>


```CSharp
private void setNewName_Click(object sender, System.EventArgs e)
{
    // ...Add code to ensure that the TextBox contains a valid value.

    // Store a WMPLib.IWMPMedia3 interface to the current media item. 
    WMPLib.IWMPMedia3 cm = (WMPLib.IWMPMedia3)player.currentMedia;

    // Change the name. 
    cm.name = nameText.Text;
}
```


```VB

Public Sub setNewName_Click(ByVal sender As Object, ByVal e As System.EventArgs) Handles setNewName.Click

    &#39; ...Add code to ensure that the TextBox contains a valid value.

    &#39; Store a WMPLib.IWMPMedia3 interface to the current media item. 
    Dim cm As WMPLib.IWMPMedia3 = player.currentMedia

    &#39; Change the name. 
    cm.name = nameText.Text

End Sub
```





## <a name="requirements"></a><span data-ttu-id="f3685-119">Требования</span><span class="sxs-lookup"><span data-stu-id="f3685-119">Requirements</span></span>



| <span data-ttu-id="f3685-120">Требование</span><span class="sxs-lookup"><span data-stu-id="f3685-120">Requirement</span></span> | <span data-ttu-id="f3685-121">Значение</span><span class="sxs-lookup"><span data-stu-id="f3685-121">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f3685-122">Версия</span><span class="sxs-lookup"><span data-stu-id="f3685-122">Version</span></span><br/>   | <span data-ttu-id="f3685-123">Проигрыватель Windows Media 9 Series или более поздней версии</span><span class="sxs-lookup"><span data-stu-id="f3685-123">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="f3685-124">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="f3685-124">Namespace</span></span><br/> | <span data-ttu-id="f3685-125">**вмплиб**</span><span class="sxs-lookup"><span data-stu-id="f3685-125">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="f3685-126">Сборка</span><span class="sxs-lookup"><span data-stu-id="f3685-126">Assembly</span></span><br/>  | <dl> <span data-ttu-id="f3685-127"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="f3685-127"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f3685-128">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="f3685-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f3685-129">**Интерфейс Ивмпмедиа (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="f3685-129">**IWMPMedia Interface (VB and C#)**</span></span>](iwmpmedia--vb-and-c.md)
</dt> </dl>

 

 





