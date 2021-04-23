---
title: Ивмпмедиа Аттрибутекаунт, свойство
description: Свойство Аттрибутекаунт возвращает количество атрибутов, которые можно запрашивать или задавать для элемента мультимедиа.
ms.assetid: 527298ff-365d-41b0-90dd-e236d6adf6fa
keywords:
- Проигрыватель Windows Media для свойства Аттрибутекаунт
- Аттрибутекаунт свойство проигрывателя Windows Media Player, интерфейс Ивмпмедиа
- Интерфейс Ивмпмедиа Windows Media Player, свойство Аттрибутекаунт
topic_type:
- apiref
api_name:
- IWMPMedia.attributeCount
- IWMPMedia.get_attributeCount
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ec5a56d06a54590afd315f04a90aa582f3a364db
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105669262"
---
# <a name="iwmpmediaattributecount-property"></a><span data-ttu-id="cb037-106">Свойство Ивмпмедиа:: Аттрибутекаунт</span><span class="sxs-lookup"><span data-stu-id="cb037-106">IWMPMedia::attributeCount property</span></span>

<span data-ttu-id="cb037-107">Свойство **аттрибутекаунт** возвращает количество атрибутов, которые можно запрашивать или задавать для элемента мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="cb037-107">The **attributeCount** property gets the number of attributes that can be queried and/or set for the media item.</span></span>

<span data-ttu-id="cb037-108">Это свойство доступно только для чтения.</span><span class="sxs-lookup"><span data-stu-id="cb037-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="cb037-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="cb037-109">Syntax</span></span>


```CSharp
public System.Int32 attributeCount {get;}
```


```VB

Public ReadOnly Property attributeCount As System.Int32
```





## <a name="property-value"></a><span data-ttu-id="cb037-110">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="cb037-110">Property value</span></span>

<span data-ttu-id="cb037-111">Значение **System. Int32** , которое является счетчиком.</span><span class="sxs-lookup"><span data-stu-id="cb037-111">A **System.Int32** that is the count.</span></span>

## <a name="remarks"></a><span data-ttu-id="cb037-112">Комментарии</span><span class="sxs-lookup"><span data-stu-id="cb037-112">Remarks</span></span>

<span data-ttu-id="cb037-113">Перед использованием этого свойства необходимо иметь доступ на чтение к библиотеке.</span><span class="sxs-lookup"><span data-stu-id="cb037-113">Before using this property, you must have read access to the library.</span></span> <span data-ttu-id="cb037-114">Дополнительные сведения см. в разделе [доступ к библиотеке](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="cb037-114">For more information, see [Library Access](library-access.md).</span></span>

<span data-ttu-id="cb037-115">Сведения об атрибутах, поддерживаемых проигрывателем Windows Media, см. в [справочнике по атрибутам](attribute-reference.md).</span><span class="sxs-lookup"><span data-stu-id="cb037-115">For information about the attributes supported by Windows Media Player, see the [Attribute Reference](attribute-reference.md).</span></span>

## <a name="examples"></a><span data-ttu-id="cb037-116">Примеры</span><span class="sxs-lookup"><span data-stu-id="cb037-116">Examples</span></span>

<span data-ttu-id="cb037-117">В следующем примере используется **аттрибутекаунт** для определения количества атрибутов, доступных в текущем элементе мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="cb037-117">The following example uses **attributeCount** to determine the number of attributes available in the current media item.</span></span> <span data-ttu-id="cb037-118">Код использует это значение для вывода списка имен и значений атрибутов в текстовом поле.</span><span class="sxs-lookup"><span data-stu-id="cb037-118">The code uses that value to display a list of attribute names and values in a text box.</span></span> <span data-ttu-id="cb037-119">Объект **аксвмплиб. аксвиндовсмедиаплайер** представлен переменной с именем Player.</span><span class="sxs-lookup"><span data-stu-id="cb037-119">The **AxWMPLib.AxWindowsMediaPlayer** object is represented by the variable named player.</span></span>


```CSharp
// Store an IWMPMedia3 interface to the current media item. 
WMPLib.IWMPMedia3 cm = (WMPLib.IWMPMedia3)player.currentMedia;

// Store the number of attributes in the current media item using attributeCount.
int numAttributes = cm.attributeCount;

// Create strings to hold each attribute name and value.
string atName;
string atValue;

// Create an array to hold the attribute list.
string [] atList = new string[numAttributes];

// Loop through the attribute list.   
for (int i = 0; i < numAttributes; i++)
{
    // Fill the strings with the attribute information.
    atName = cm.getAttributeName(i);
    atValue = cm.getItemInfo(atName);

    // Store the attribute information in an array.
    atList[i] = (atName + ": " + atValue);
}

// Display the attribute information in the text box.
attributeList.Lines = atList;
```


```VB

' Store an IWMPMedia3 interface to the current media item. 
Dim cm As WMPLib.IWMPMedia3 = player.currentMedia

&#39; Store the number of attributes in the current media item using attributeCount.
Dim numAttributes As Integer = cm.attributeCount

&#39; Create strings to hold each attribute name and value.
Dim atName As String
Dim atValue As String

&#39; Create an array to hold the attribute list.
Dim atList(numAttributes) As String

&#39; Loop through the attribute list.   
For i As Integer = 0 To (numAttributes - 1)

    &#39; Fill the strings with the attribute information.
    atName = cm.getAttributeName(i)
    atValue = cm.getItemInfo(atName)

    &#39; Store the attribute information in an array.
    atList(i) = (atName + &quot;: &quot; + atValue)

Next i

&#39; Display the attribute information in the text box.
attributeList.Lines = atList
```





## <a name="requirements"></a><span data-ttu-id="cb037-120">Требования</span><span class="sxs-lookup"><span data-stu-id="cb037-120">Requirements</span></span>



| <span data-ttu-id="cb037-121">Требование</span><span class="sxs-lookup"><span data-stu-id="cb037-121">Requirement</span></span> | <span data-ttu-id="cb037-122">Значение</span><span class="sxs-lookup"><span data-stu-id="cb037-122">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cb037-123">Версия</span><span class="sxs-lookup"><span data-stu-id="cb037-123">Version</span></span><br/>   | <span data-ttu-id="cb037-124">Проигрыватель Windows Media 9 Series или более поздней версии</span><span class="sxs-lookup"><span data-stu-id="cb037-124">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="cb037-125">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="cb037-125">Namespace</span></span><br/> | <span data-ttu-id="cb037-126">**вмплиб**</span><span class="sxs-lookup"><span data-stu-id="cb037-126">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="cb037-127">Сборка</span><span class="sxs-lookup"><span data-stu-id="cb037-127">Assembly</span></span><br/>  | <dl> <span data-ttu-id="cb037-128"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="cb037-128"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cb037-129">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="cb037-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cb037-130">**Интерфейс Ивмпмедиа (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="cb037-130">**IWMPMedia Interface (VB and C#)**</span></span>](iwmpmedia--vb-and-c.md)
</dt> </dl>

 

 





