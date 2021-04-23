---
title: IWMPStringCollection2 Жетитеминфобитипе, метод
description: Метод Жетитеминфобитипе возвращает значение, соответствующее указанному индексу элемента коллекции строк, имени, языку и индексу атрибута.
ms.assetid: 51035fed-51ce-4cd2-a936-4c99802128f2
keywords:
- Жетитеминфобитипе метод Windows Media Player
- Жетитеминфобитипе метод проигрывателя Windows Media Player, интерфейс IWMPStringCollection2
- Интерфейс IWMPStringCollection2 Windows Media Player, метод Жетитеминфобитипе
topic_type:
- apiref
api_name:
- IWMPStringCollection2.getItemInfobyType
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e227d6471ecf41c8f48420ded61c6f4e7eaac8cf
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105708466"
---
# <a name="iwmpstringcollection2getiteminfobytype-method"></a><span data-ttu-id="519b2-106">Метод IWMPStringCollection2:: Жетитеминфобитипе</span><span class="sxs-lookup"><span data-stu-id="519b2-106">IWMPStringCollection2::getItemInfobyType method</span></span>

<span data-ttu-id="519b2-107">Метод **жетитеминфобитипе** возвращает значение, соответствующее указанному индексу элемента коллекции строк, имени, языку и индексу атрибута.</span><span class="sxs-lookup"><span data-stu-id="519b2-107">The **getItemInfoByType** method returns the value corresponding to the specified string collection item index, name, language, and attribute index.</span></span>

## <a name="syntax"></a><span data-ttu-id="519b2-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="519b2-108">Syntax</span></span>


```CSharp
public System.Object getItemInfobyType(
  System.Int32 lCollectionIndex,
  System.String bstrType,
  System.String bstrLanguage,
  System.Int32 lAttributeIndex
);
```


```VB

Public Function getItemInfobyType( _
  ByVal lCollectionIndex As System.Int32, _
  ByVal bstrType As System.String, _
  ByVal bstrLanguage As System.String, _
  ByVal lAttributeIndex As System.Int32 _
) As System.Object
Implements IWMPStringCollection2.getItemInfobyType
```





## <a name="parameters"></a><span data-ttu-id="519b2-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="519b2-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="519b2-110">*лколлектиониндекс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="519b2-110">*lCollectionIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="519b2-111">Объект **System. Int32** , являющийся начинающимся с нуля индексом элемента коллекции строк, из которого необходимо получить атрибут.</span><span class="sxs-lookup"><span data-stu-id="519b2-111">The **System.Int32** that is the zero-based index of the string collection item from which to get the attribute.</span></span>

</dd> <dt>

<span data-ttu-id="519b2-112">*бстртипе* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="519b2-112">*bstrType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="519b2-113">**Строка System. String** , которая является именем атрибута.</span><span class="sxs-lookup"><span data-stu-id="519b2-113">The **System.String** that is the attribute name.</span></span>

</dd> <dt>

<span data-ttu-id="519b2-114">*бстрлангуаже* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="519b2-114">*bstrLanguage* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="519b2-115">**Строка System. String** , указывающая язык.</span><span class="sxs-lookup"><span data-stu-id="519b2-115">The **System.String** that indicates the language.</span></span> <span data-ttu-id="519b2-116">Если задано значение null или строка нулевой длины (""), используется текущая строка языкового стандарта.</span><span class="sxs-lookup"><span data-stu-id="519b2-116">If the value is set to null or to a zero-length string (""), the current locale string is used.</span></span> <span data-ttu-id="519b2-117">В противном случае значение должно быть допустимой строкой языка RFC 1766, например "en-US".</span><span class="sxs-lookup"><span data-stu-id="519b2-117">Otherwise, the value must be a valid RFC 1766 language string such as "en-us".</span></span>

</dd> <dt>

<span data-ttu-id="519b2-118">*латтрибутеиндекс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="519b2-118">*lAttributeIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="519b2-119">Объект **System. Int32** , который является индексом атрибута (начинающийся с нуля).</span><span class="sxs-lookup"><span data-stu-id="519b2-119">A **System.Int32** that is the zero-based index of the attribute.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="519b2-120">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="519b2-120">Return value</span></span>

<span data-ttu-id="519b2-121">Объект **System. Object** , являющийся элементом коллекции строк.</span><span class="sxs-lookup"><span data-stu-id="519b2-121">A **System.Object** that is the string collection item.</span></span>

## <a name="remarks"></a><span data-ttu-id="519b2-122">Комментарии</span><span class="sxs-lookup"><span data-stu-id="519b2-122">Remarks</span></span>

<span data-ttu-id="519b2-123">Этот метод поддерживает атрибуты с несколькими значениями и атрибутами со сложными значениями.</span><span class="sxs-lookup"><span data-stu-id="519b2-123">This method supports attributes with multiple values and attributes with complex values.</span></span> <span data-ttu-id="519b2-124">Метод **getItemInfo** не поддерживает атрибуты с несколькими значениями или атрибутами со сложными значениями.</span><span class="sxs-lookup"><span data-stu-id="519b2-124">The **getItemInfo** method does not support attributes with multiple values or attributes with complex values.</span></span>

<span data-ttu-id="519b2-125">Передав значение "Чилдлист" в параметре *бстртипе* , можно получить новую коллекцию строк, содержащую дочерние элементы одного из элементов в родительской коллекции строк.</span><span class="sxs-lookup"><span data-stu-id="519b2-125">By passing the value "ChildList" in the *bstrType* parameter, you can retrieve a new string collection that contains the children of one of the items in the parent string collection.</span></span> <span data-ttu-id="519b2-126">Например, если родительская коллекция содержит список Албумидс, этот метод можно использовать для получения коллекции дочерних строк, содержащей все дорожки для одного из альбомов.</span><span class="sxs-lookup"><span data-stu-id="519b2-126">For instance, if the parent collection contains a list of AlbumIDs, you can use this method to obtain a child string collection that contains all the tracks for one of the albums.</span></span> <span data-ttu-id="519b2-127">Этот подход быстрее и эффективнее, чем вызов метода **IWMPMediaCollection2. жетстрингколлектионбикуери** дважды; один раз для получения коллекции Албумидс и второй раз для получения коллекции дорожек для определенного Албумид.</span><span class="sxs-lookup"><span data-stu-id="519b2-127">This approach is faster and more efficient than calling the **IWMPMediaCollection2.getStringCollectionByQuery** method twice; once to get a collection of AlbumIDs, and a second time to get a collection of tracks for a particular AlbumID.</span></span> <span data-ttu-id="519b2-128">Чтобы использовать Чилдлист только что описанным способом, родительская коллекция строк должна быть получена из коллекции носителей через **ивмплибрарисервицес**, а не с помощью свойства **аксвиндовсмедиаплайер. медиаколлектион** .</span><span class="sxs-lookup"><span data-stu-id="519b2-128">To use ChildList in the way just described, the parent string collection must be obtained from a media collection through **IWMPLibraryServices**, and not by using the **AxWindowsMediaPlayer.mediaCollection** property.</span></span>

<span data-ttu-id="519b2-129">При использовании Чилдлист передайте значение "Чилдлист" в параметре *бстртипе* и значение 0 в параметре *латтрибутеиндекс* .</span><span class="sxs-lookup"><span data-stu-id="519b2-129">When using ChildList, pass the value "ChildList" in the *bstrType* parameter, and the value 0 in the *lAttributeIndex* parameter.</span></span> <span data-ttu-id="519b2-130">Затем можно привести объект, возвращаемый к интерфейсу **IWMPStringCollection2** , для доступа к дочернему списку.</span><span class="sxs-lookup"><span data-stu-id="519b2-130">You can then cast the object that is returned to an **IWMPStringCollection2** interface to access the child list.</span></span>

<span data-ttu-id="519b2-131">Чтобы использовать этот метод, необходимо иметь доступ на чтение к библиотеке.</span><span class="sxs-lookup"><span data-stu-id="519b2-131">To use this method, you must have read access to the library.</span></span> <span data-ttu-id="519b2-132">Дополнительные сведения см. в разделе [доступ к библиотеке](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="519b2-132">For more information, see [Library Access](library-access.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="519b2-133">Требования</span><span class="sxs-lookup"><span data-stu-id="519b2-133">Requirements</span></span>



| <span data-ttu-id="519b2-134">Требование</span><span class="sxs-lookup"><span data-stu-id="519b2-134">Requirement</span></span> | <span data-ttu-id="519b2-135">Значение</span><span class="sxs-lookup"><span data-stu-id="519b2-135">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="519b2-136">Версия</span><span class="sxs-lookup"><span data-stu-id="519b2-136">Version</span></span><br/>   | <span data-ttu-id="519b2-137">Проигрыватель Windows Media 11.</span><span class="sxs-lookup"><span data-stu-id="519b2-137">Windows Media Player 11.</span></span><br/>                                                                                    |
| <span data-ttu-id="519b2-138">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="519b2-138">Namespace</span></span><br/> | <span data-ttu-id="519b2-139">**вмплиб**</span><span class="sxs-lookup"><span data-stu-id="519b2-139">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="519b2-140">Сборка</span><span class="sxs-lookup"><span data-stu-id="519b2-140">Assembly</span></span><br/>  | <dl> <span data-ttu-id="519b2-141"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="519b2-141"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="519b2-142">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="519b2-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="519b2-143">**Атрибут Албумид**</span><span class="sxs-lookup"><span data-stu-id="519b2-143">**AlbumID Attribute**</span></span>](albumid-attribute.md)
</dt> <dt>

[<span data-ttu-id="519b2-144">**Интерфейс Ивмплибрарисервицес (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="519b2-144">**IWMPLibraryServices Interface (VB and C#)**</span></span>](iwmplibraryservices--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="519b2-145">**IWMPMediaCollection2. Жетстрингколлектионбикуери (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="519b2-145">**IWMPMediaCollection2.getStringCollectionByQuery (VB and C#)**</span></span>](wmplibiwmpmediacollection2-iwmpmediacollection2-getstringcollectionbyquery--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="519b2-146">**Интерфейс IWMPStringCollection2**</span><span class="sxs-lookup"><span data-stu-id="519b2-146">**IWMPStringCollection2 Interface**</span></span>](iwmpstringcollection2--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="519b2-147">**IWMPStringCollection2. getItemInfo (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="519b2-147">**IWMPStringCollection2.getItemInfo (VB and C#)**</span></span>](wmplibiwmpstringcollection2-iwmpstringcollection2-getiteminfo--vb-and-c.md)
</dt> </dl>

 

 





