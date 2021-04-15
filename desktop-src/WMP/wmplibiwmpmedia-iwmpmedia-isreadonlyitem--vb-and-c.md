---
title: Ивмпмедиа Исреадонлитем, метод
description: Метод Исреадонлитем возвращает значение, указывающее, можно ли изменять атрибуты указанного элемента мультимедиа.
ms.assetid: c810c5c1-8cb9-4ac7-ac49-1ebdc86f5d7f
keywords:
- Исреадонлитем метод Windows Media Player
- Исреадонлитем метод проигрывателя Windows Media Player, интерфейс Ивмпмедиа
- Интерфейс Ивмпмедиа Windows Media Player, метод Исреадонлитем
topic_type:
- apiref
api_name:
- IWMPMedia.isReadOnlyItem
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f21d3dfefc1222832783e62962298da8bcb02b25
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105669243"
---
# <a name="iwmpmediaisreadonlyitem-method"></a><span data-ttu-id="50711-106">Метод Ивмпмедиа:: Исреадонлитем</span><span class="sxs-lookup"><span data-stu-id="50711-106">IWMPMedia::isReadOnlyItem method</span></span>

<span data-ttu-id="50711-107">Метод **исреадонлитем** возвращает значение, указывающее, можно ли изменять атрибуты указанного элемента мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="50711-107">The **isReadOnlyItem** method returns a value indicating whether the attributes of the specified media item can be edited.</span></span>

## <a name="syntax"></a><span data-ttu-id="50711-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="50711-108">Syntax</span></span>


```CSharp
public System.Boolean isReadOnlyItem(
  System.String bstrItemName
);
```


```VB

Public Function isReadOnlyItem( _
  ByVal bstrItemName As System.String _
) As System.Boolean
Implements IWMPMedia.isReadOnlyItem
```





## <a name="parameters"></a><span data-ttu-id="50711-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="50711-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="50711-110">*бстритемнаме* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="50711-110">*bstrItemName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="50711-111">**Строка System. String** , которая является именем элемента мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="50711-111">A **System.String** that is the name of the media item.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="50711-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="50711-112">Return value</span></span>

<span data-ttu-id="50711-113">Значение **System. Boolean** , указывающее, доступны ли атрибуты только для чтения.</span><span class="sxs-lookup"><span data-stu-id="50711-113">A **System.Boolean** value that indicates whether the attributes are read-only.</span></span>

## <a name="remarks"></a><span data-ttu-id="50711-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="50711-114">Remarks</span></span>

<span data-ttu-id="50711-115">Если атрибут доступен только для чтения, то он не может быть задан с помощью метода **сетитеминфо** .</span><span class="sxs-lookup"><span data-stu-id="50711-115">If an attribute is read-only, then it cannot be set with the **setItemInfo** method.</span></span> <span data-ttu-id="50711-116">Обратите внимание, что этот метод может возвращать различные значения для определенного атрибута при использовании с разными версиями проигрывателя Windows Media.</span><span class="sxs-lookup"><span data-stu-id="50711-116">Note that this method may return different values for a particular attribute when used with different versions of Windows Media Player.</span></span>

<span data-ttu-id="50711-117">Перед вызовом этого метода необходимо иметь доступ на чтение к библиотеке.</span><span class="sxs-lookup"><span data-stu-id="50711-117">Before calling this method, you must have read access to the library.</span></span> <span data-ttu-id="50711-118">Дополнительные сведения см. в разделе [доступ к библиотеке](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="50711-118">For more information, see [Library Access](library-access.md).</span></span>

## <a name="examples"></a><span data-ttu-id="50711-119">Примеры</span><span class="sxs-lookup"><span data-stu-id="50711-119">Examples</span></span>

<span data-ttu-id="50711-120">В следующем примере **исреадонлитем** используется для заполнения многострочного текстового поля сведениями о текущем элементе мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="50711-120">The following example uses **isReadOnlyItem** to fill a multi-line text box with information about the current media item.</span></span> <span data-ttu-id="50711-121">Код отображает каждый атрибут текущего элемента мультимедиа вместе с текстом, указывающим, доступен ли атрибут только для чтения или для чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="50711-121">The code displays each attribute of the current media item, along with text indicating whether the attribute is read-only or read/write.</span></span> <span data-ttu-id="50711-122">Объект **аксвмплиб. аксвиндовсмедиаплайер** представлен переменной с именем Player.</span><span class="sxs-lookup"><span data-stu-id="50711-122">The **AxWMPLib.AxWindowsMediaPlayer** object is represented by the variable named player.</span></span>


```CSharp
// Store a WMPLib.IWMPMedia3 interface to the current media item.
WMPLib.IWMPMedia3 cm = (WMPLib.IWMPMedia3)player.currentMedia;

// Get the number of attributes in the current media item.
int attCount = player.currentMedia.attributeCount;

// Create an array to store the list of attribute information.
string[] atInfo = new string[attCount];

// Create a variable to hold each attribute name.
string atName;

// Loop through the attribute list.
for (int i = 0; i < cm.attributeCount; i++)
{
    // Get the attribute name.
    atName = cm.getAttributeName(i);

    // Test whether the attribute is read-only.
    string test = ((cm.isReadOnlyItem(atName)) ? "Read-Only" : "Read/Write");

    // Store the attribute information in the array.
    atInfo[i] = (atName + " is " + test);
}

// Display the attribute information in the text box.
rwText.Lines = atInfo;
```


```VB

' Store a WMPLib.IWMPMedia3 interface to the current media item.
Dim cm As WMPLib.IWMPMedia3 = player.currentMedia

&#39; Get the number of attributes in the current media item.
Dim attCount As Integer = player.currentMedia.attributeCount

&#39; Create an array to store the list of attribute information.
Dim atInfo(attCount) As String

&#39; Create a variable to hold each attribute name.
Dim atName As String

&#39; Loop through the attribute list.
For i As Integer = 0 To (cm.attributeCount - 1)

    &#39; Get the attribute name.
    atName = cm.getAttributeName(i)

    &#39; Test whether the attribute is read-only.
    If (cm.isReadOnlyItem(atName)) Then

        atInfo(i) = (atName + &quot; is Read-Only&quot;)

    Else

        atInfo(i) = (atName + &quot; is Read/Write&quot;)

    End If

Next i

&#39; Display the attribute information in the text box.
rwText.Lines = atInfo
```





## <a name="requirements"></a><span data-ttu-id="50711-123">Требования</span><span class="sxs-lookup"><span data-stu-id="50711-123">Requirements</span></span>



| <span data-ttu-id="50711-124">Требование</span><span class="sxs-lookup"><span data-stu-id="50711-124">Requirement</span></span> | <span data-ttu-id="50711-125">Значение</span><span class="sxs-lookup"><span data-stu-id="50711-125">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="50711-126">Версия</span><span class="sxs-lookup"><span data-stu-id="50711-126">Version</span></span><br/>   | <span data-ttu-id="50711-127">Проигрыватель Windows Media 9 Series или более поздней версии</span><span class="sxs-lookup"><span data-stu-id="50711-127">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="50711-128">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="50711-128">Namespace</span></span><br/> | <span data-ttu-id="50711-129">**вмплиб**</span><span class="sxs-lookup"><span data-stu-id="50711-129">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="50711-130">Сборка</span><span class="sxs-lookup"><span data-stu-id="50711-130">Assembly</span></span><br/>  | <dl> <span data-ttu-id="50711-131"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="50711-131"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="50711-132">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="50711-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="50711-133">**Интерфейс Ивмпмедиа (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="50711-133">**IWMPMedia Interface (VB and C#)**</span></span>](iwmpmedia--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="50711-134">**Ивмпмедиа. Сетитеминфо (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="50711-134">**IWMPMedia.setItemInfo (VB and C#)**</span></span>](wmplibiwmpmedia-iwmpmedia-setiteminfo--vb-and-c.md)
</dt> </dl>

 

 





