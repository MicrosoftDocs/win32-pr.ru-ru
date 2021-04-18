---
title: Ивмпплайлист. attributeName (VB и C)
description: Свойство attributeName ( \_ метод Get AttributeName в C \) возвращает имя атрибута списка воспроизведения, указанного индексом.
ms.assetid: bb436657-5156-437e-af58-6497ad3b311b
keywords:
- Проигрыватель Windows Media Ивмпплайлист. attributeName (VB и C)
topic_type:
- apiref
api_name:
- IWMPPlaylist.attributeName (VB and C )
api_location:
- Interop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 727d58a0cf875ed29efe9235448c1d597e81656a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105685075"
---
# <a name="iwmpplaylistattributename-vb-and-c"></a><span data-ttu-id="37be9-104">Ивмпплайлист. attributeName (VB и C#)</span><span class="sxs-lookup"><span data-stu-id="37be9-104">IWMPPlaylist.attributeName (VB and C#)</span></span>

<span data-ttu-id="37be9-105">Свойство **attributeName** (метод **Get \_ attributeName** в C#) возвращает имя атрибута списка воспроизведения, указанного индексом.</span><span class="sxs-lookup"><span data-stu-id="37be9-105">The **attributeName** property (the **get\_attributeName** method in C#) gets the name of a playlist attribute specified by an index.</span></span>


```
[Visual Basic]
ReadOnly Property attributeName(
  lIndex As System.Int32
) As System.String
```




```
[C#]
System.String get_attributeName(
  System.Int32 lIndex
);
```



## <a name="parameters"></a><span data-ttu-id="37be9-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="37be9-106">Parameters</span></span>

<span data-ttu-id="37be9-107">*линдекс*</span><span class="sxs-lookup"><span data-stu-id="37be9-107">*lIndex*</span></span>

<span data-ttu-id="37be9-108">Объект **System. Int32** , который является индексом атрибута списка воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="37be9-108">A **System.Int32** that is the index of the playlist attribute.</span></span>

## <a name="return-value"></a><span data-ttu-id="37be9-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="37be9-109">Return Value</span></span>

<span data-ttu-id="37be9-110">**Строка System. String** , которая является именем атрибута списка воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="37be9-110">A **System.String** that is the name of the playlist attribute.</span></span>

## <a name="remarks"></a><span data-ttu-id="37be9-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="37be9-111">Remarks</span></span>

<span data-ttu-id="37be9-112">**Ивмпплайлист. AttributeName** — это свойство, доступное только для чтения, в Visual Basic, которое принимает параметр, тогда как в C# он называется методом **ивмпплайлист. Get \_ attributeName** .</span><span class="sxs-lookup"><span data-stu-id="37be9-112">**IWMPPlaylist.attributeName** is a read-only property in Visual Basic that takes a parameter, while in C# it is referred to as the **IWMPPlaylist.get\_attributeName** method.</span></span>

<span data-ttu-id="37be9-113">Число атрибутов, связанных с списком воспроизведения, возвращается свойством **ивмпплайлист. аттрибутекаунт** .</span><span class="sxs-lookup"><span data-stu-id="37be9-113">The number of attributes associated with a playlist is returned by the **IWMPPlaylist.attributeCount** property.</span></span>

<span data-ttu-id="37be9-114">Имя, возвращаемое этим свойством, может быть предоставлено методам **сетитеминфо** или **getItemInfo** для указания или получения значения для именованного атрибута.</span><span class="sxs-lookup"><span data-stu-id="37be9-114">The name returned by this property can be supplied to the **setItemInfo** or **getItemInfo** methods to specify or retrieve a value for the named attribute.</span></span>

<span data-ttu-id="37be9-115">Перед использованием этого свойства необходимо иметь доступ на чтение к библиотеке.</span><span class="sxs-lookup"><span data-stu-id="37be9-115">Before using this property, you must have read access to the library.</span></span> <span data-ttu-id="37be9-116">Дополнительные сведения см. в разделе [доступ к библиотеке](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="37be9-116">For more information, see [Library Access](library-access.md).</span></span>

<span data-ttu-id="37be9-117">Дополнительные сведения об атрибутах, поддерживаемых проигрывателем Windows Media, см. в [справочнике по атрибутам](attribute-reference.md).</span><span class="sxs-lookup"><span data-stu-id="37be9-117">For more information about attributes supported by Windows Media Player, see the [Attribute Reference](attribute-reference.md).</span></span>

## <a name="examples"></a><span data-ttu-id="37be9-118">Примеры</span><span class="sxs-lookup"><span data-stu-id="37be9-118">Examples</span></span>

<span data-ttu-id="37be9-119">Пример кода, в котором используется это свойство, см. в свойстве [аттрибутекаунт](wmplibiwmpplaylist-iwmpplaylist-attributecount--vb-and-c.md) .</span><span class="sxs-lookup"><span data-stu-id="37be9-119">See the [attributeCount](wmplibiwmpplaylist-iwmpplaylist-attributecount--vb-and-c.md) property for example code that uses this property.</span></span>

## <a name="requirements"></a><span data-ttu-id="37be9-120">Требования</span><span class="sxs-lookup"><span data-stu-id="37be9-120">Requirements</span></span>



| <span data-ttu-id="37be9-121">Требование</span><span class="sxs-lookup"><span data-stu-id="37be9-121">Requirement</span></span> | <span data-ttu-id="37be9-122">Значение</span><span class="sxs-lookup"><span data-stu-id="37be9-122">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="37be9-123">Версия</span><span class="sxs-lookup"><span data-stu-id="37be9-123">Version</span></span><br/>   | <span data-ttu-id="37be9-124">Проигрыватель Windows Media 9 Series или более поздней версии</span><span class="sxs-lookup"><span data-stu-id="37be9-124">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="37be9-125">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="37be9-125">Namespace</span></span><br/> | <span data-ttu-id="37be9-126">**вмплиб**</span><span class="sxs-lookup"><span data-stu-id="37be9-126">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="37be9-127">Сборка</span><span class="sxs-lookup"><span data-stu-id="37be9-127">Assembly</span></span><br/>  | <dl> <span data-ttu-id="37be9-128"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="37be9-128"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="37be9-129">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="37be9-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="37be9-130">**Интерфейс Ивмпплайлист (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="37be9-130">**IWMPPlaylist Interface (VB and C#)**</span></span>](iwmpplaylist--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="37be9-131">**Ивмпплайлист. Аттрибутекаунт (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="37be9-131">**IWMPPlaylist.attributeCount (VB and C#)**</span></span>](wmplibiwmpplaylist-iwmpplaylist-attributecount--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="37be9-132">**Ивмпплайлист. getItemInfo (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="37be9-132">**IWMPPlaylist.getItemInfo (VB and C#)**</span></span>](wmplibiwmpplaylist-iwmpplaylist-getiteminfo--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="37be9-133">**Ивмпплайлист. Сетитеминфо (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="37be9-133">**IWMPPlaylist.setItemInfo (VB and C#)**</span></span>](wmplibiwmpplaylist-iwmpplaylist-setiteminfo--vb-and-c.md)
</dt> </dl>

 

 





