---
title: Ивмпмедиа Жетаттрибутенаме, метод
description: Метод Жетаттрибутенаме возвращает имя атрибута, соответствующего указанному индексу.
ms.assetid: d2496484-34cc-4222-9bc3-1d3ebb9a4173
keywords:
- Жетаттрибутенаме метод Windows Media Player
- Жетаттрибутенаме метод проигрывателя Windows Media Player, интерфейс Ивмпмедиа
- Интерфейс Ивмпмедиа Windows Media Player, метод Жетаттрибутенаме
topic_type:
- apiref
api_name:
- IWMPMedia.getAttributeName
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fb40ef8c0c984258dc11dd00c80807db2f4eb64a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105669259"
---
# <a name="iwmpmediagetattributename-method"></a><span data-ttu-id="7f676-106">Метод Ивмпмедиа:: Жетаттрибутенаме</span><span class="sxs-lookup"><span data-stu-id="7f676-106">IWMPMedia::getAttributeName method</span></span>

<span data-ttu-id="7f676-107">Метод **жетаттрибутенаме** возвращает имя атрибута, соответствующего указанному индексу.</span><span class="sxs-lookup"><span data-stu-id="7f676-107">The **getAttributeName** method returns the name of the attribute corresponding to the specified index.</span></span>

## <a name="syntax"></a><span data-ttu-id="7f676-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="7f676-108">Syntax</span></span>


```CSharp
public System.String getAttributeName(
  System.Int32 lIndex
);
```


```VB

Public Function getAttributeName( _
  ByVal lIndex As System.Int32 _
) As System.String
Implements IWMPMedia.getAttributeName
```





## <a name="parameters"></a><span data-ttu-id="7f676-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="7f676-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7f676-110">*Линдекс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="7f676-110">*lIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7f676-111">Объект **System. Int32** , который является индексом.</span><span class="sxs-lookup"><span data-stu-id="7f676-111">A **System.Int32** that is the index.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7f676-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="7f676-112">Return value</span></span>

<span data-ttu-id="7f676-113">**Строка System. String** , которая является именем атрибута.</span><span class="sxs-lookup"><span data-stu-id="7f676-113">A **System.String** that is the attribute name.</span></span>

## <a name="remarks"></a><span data-ttu-id="7f676-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="7f676-114">Remarks</span></span>

<span data-ttu-id="7f676-115">Возвращаемое имя атрибута можно использовать в сочетании с **getItemInfo** для получения значения для определенного именованного атрибута.</span><span class="sxs-lookup"><span data-stu-id="7f676-115">The attribute name returned can be used in conjunction with **getItemInfo** to retrieve the value for a specific named attribute.</span></span>

<span data-ttu-id="7f676-116">Перед вызовом этого метода необходимо иметь доступ на чтение к библиотеке.</span><span class="sxs-lookup"><span data-stu-id="7f676-116">Before calling this method, you must have read access to the library.</span></span> <span data-ttu-id="7f676-117">Дополнительные сведения см. в разделе [доступ к библиотеке](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="7f676-117">For more information, see [Library Access](library-access.md).</span></span>

<span data-ttu-id="7f676-118">Сведения об атрибутах, поддерживаемых проигрывателем Windows Media, см. в [справочнике по атрибутам](attribute-reference.md).</span><span class="sxs-lookup"><span data-stu-id="7f676-118">For information about the attributes supported by Windows Media Player, see the [Attribute Reference](attribute-reference.md).</span></span>

## <a name="examples"></a><span data-ttu-id="7f676-119">Примеры</span><span class="sxs-lookup"><span data-stu-id="7f676-119">Examples</span></span>

<span data-ttu-id="7f676-120">В следующем примере **жетаттрибутенаме** используется для заполнения многострочного текстового поля с индексом и именем каждого атрибута для текущего элемента мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="7f676-120">The following example uses **getAttributeName** to fill a multi-line text box with the index and name of each attribute for the current media item.</span></span> <span data-ttu-id="7f676-121">Объект **аксвмплиб. аксвиндовсмедиаплайер** представлен переменной с именем Player.</span><span class="sxs-lookup"><span data-stu-id="7f676-121">The **AxWMPLib.AxWindowsMediaPlayer** object is represented by the variable named player.</span></span>


```CSharp
// Store an IWMPMedia3 interface for the current media item. 
WMPLib.IWMPMedia3 cm = (WMPLib.IWMPMedia3)player.currentMedia;

// Get the number of attributes for the current media item. 
int attCount = cm.attributeCount;

// Create an array of strings to hold the index and name for each attribute.
string[] attInfo = new string[attCount];

// Loop through the attribute list.
for (int i = 0; i < attCount; i++)
{
    // Store the attribute index and name in the array.
    attInfo[i] = ("Attribute " + i + ": " + cm.getAttributeName(i));
}

// Display the attribute information in the text box.
attributeNames.Lines = attInfo;
```


```VB

' Store an IWMPMedia3 interface for the current media item. 
Dim cm As WMPLib.IWMPMedia3 = player.currentMedia

&#39; Get the number of attributes for the current media. 
Dim attCount As Integer = cm.attributeCount

&#39; Create an array of strings to hold the index and name for each attribute.
Dim attInfo(attCount) As String

&#39; Loop through the attribute list.
For i As Integer = 0 To (attCount - 1)

    &#39; Store the attribute index and name in the array.
    attInfo(i) = (&quot;Attribute &quot; + i.ToString() + &quot;: &quot; + cm.getAttributeName(i))

Next i

&#39; Display the attribute information in the text box.
attributeNames.Lines = attInfo
```





## <a name="requirements"></a><span data-ttu-id="7f676-122">Требования</span><span class="sxs-lookup"><span data-stu-id="7f676-122">Requirements</span></span>



| <span data-ttu-id="7f676-123">Требование</span><span class="sxs-lookup"><span data-stu-id="7f676-123">Requirement</span></span> | <span data-ttu-id="7f676-124">Значение</span><span class="sxs-lookup"><span data-stu-id="7f676-124">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7f676-125">Версия</span><span class="sxs-lookup"><span data-stu-id="7f676-125">Version</span></span><br/>   | <span data-ttu-id="7f676-126">Проигрыватель Windows Media 9 Series или более поздней версии</span><span class="sxs-lookup"><span data-stu-id="7f676-126">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="7f676-127">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="7f676-127">Namespace</span></span><br/> | <span data-ttu-id="7f676-128">**вмплиб**</span><span class="sxs-lookup"><span data-stu-id="7f676-128">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="7f676-129">Сборка</span><span class="sxs-lookup"><span data-stu-id="7f676-129">Assembly</span></span><br/>  | <dl> <span data-ttu-id="7f676-130"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="7f676-130"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7f676-131">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="7f676-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7f676-132">**Интерфейс Ивмпмедиа (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="7f676-132">**IWMPMedia Interface (VB and C#)**</span></span>](iwmpmedia--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="7f676-133">**Ивмпмедиа. getItemInfo (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="7f676-133">**IWMPMedia.getItemInfo (VB and C#)**</span></span>](wmplibiwmpmedia-iwmpmedia-getiteminfo--vb-and-c.md)
</dt> </dl>

 

 





