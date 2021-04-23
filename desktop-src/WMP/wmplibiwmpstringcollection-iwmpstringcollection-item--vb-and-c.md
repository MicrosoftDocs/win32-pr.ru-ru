---
title: Метод Ивмпстрингколлектион Item
description: Метод Item возвращает строку по указанному индексу.
ms.assetid: 77546cb2-eda5-4bb8-97b9-55270461815f
keywords:
- Метод Item проигрыватель Windows Media Player
- Метод Item проигрыватель Windows Media Player, интерфейс Ивмпстрингколлектион
- Интерфейс Ивмпстрингколлектион Windows Media Player, метод Item
topic_type:
- apiref
api_name:
- IWMPStringCollection.Item
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f69bdc63448699a595238b9907f4b1253209ad06
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105704360"
---
# <a name="iwmpstringcollectionitem-method"></a><span data-ttu-id="cfd76-106">Метод Ивмпстрингколлектион:: Item</span><span class="sxs-lookup"><span data-stu-id="cfd76-106">IWMPStringCollection::Item method</span></span>

<span data-ttu-id="cfd76-107">Метод **Item** возвращает строку по указанному индексу.</span><span class="sxs-lookup"><span data-stu-id="cfd76-107">The **Item** method returns the string at the specified index.</span></span>

## <a name="syntax"></a><span data-ttu-id="cfd76-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="cfd76-108">Syntax</span></span>


```CSharp
public System.String Item(
  System.Int32 lIndex
);
```


```VB

Public Function Item( _
  ByVal lIndex As System.Int32 _
) As System.String
Implements IWMPStringCollection.Item
```





## <a name="parameters"></a><span data-ttu-id="cfd76-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="cfd76-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cfd76-110">*Линдекс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="cfd76-110">*lIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cfd76-111">Объект **System. Int32** , который является индексом.</span><span class="sxs-lookup"><span data-stu-id="cfd76-111">A **System.Int32** that is the index.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cfd76-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="cfd76-112">Return value</span></span>

<span data-ttu-id="cfd76-113">Строка **System. String** , которая является строкой по указанному индексу.</span><span class="sxs-lookup"><span data-stu-id="cfd76-113">A **System.String** that is the string at the specified index.</span></span>

## <a name="remarks"></a><span data-ttu-id="cfd76-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="cfd76-114">Remarks</span></span>

<span data-ttu-id="cfd76-115">Интерфейс **ивмпстрингколлектион** используется для получения набора значений, доступных для атрибута.</span><span class="sxs-lookup"><span data-stu-id="cfd76-115">The **IWMPStringCollection** interface is used to retrieve the set of values available for an attribute.</span></span> <span data-ttu-id="cfd76-116">Например, метод **ивмпмедиаколлектион. жетаттрибутестрингколлектион** можно использовать для получения интерфейса **ивмпстрингколлектион** , представляющего все значения атрибута жанра в типе носителя Audio.</span><span class="sxs-lookup"><span data-stu-id="cfd76-116">For example, the **IWMPMediaCollection.getAttributeStringCollection** method can be used to retrieve an **IWMPStringCollection** interface representing all the values for the Genre attribute within the Audio media type.</span></span> <span data-ttu-id="cfd76-117">Затем метод **Item** можно использовать для итерации всех возможных значений атрибута жанра.</span><span class="sxs-lookup"><span data-stu-id="cfd76-117">The **Item** method can then be used to iterate through all of the possible values for the Genre attribute.</span></span>

<span data-ttu-id="cfd76-118">Чтобы использовать этот метод, требуется доступ на чтение к библиотеке.</span><span class="sxs-lookup"><span data-stu-id="cfd76-118">To use this method, read access to the library is required.</span></span> <span data-ttu-id="cfd76-119">Дополнительные сведения см. в разделе [доступ к библиотеке](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="cfd76-119">For more information, see [Library Access](library-access.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="cfd76-120">Требования</span><span class="sxs-lookup"><span data-stu-id="cfd76-120">Requirements</span></span>



| <span data-ttu-id="cfd76-121">Требование</span><span class="sxs-lookup"><span data-stu-id="cfd76-121">Requirement</span></span> | <span data-ttu-id="cfd76-122">Значение</span><span class="sxs-lookup"><span data-stu-id="cfd76-122">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cfd76-123">Версия</span><span class="sxs-lookup"><span data-stu-id="cfd76-123">Version</span></span><br/>   | <span data-ttu-id="cfd76-124">Проигрыватель Windows Media 9 Series или более поздней версии</span><span class="sxs-lookup"><span data-stu-id="cfd76-124">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="cfd76-125">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="cfd76-125">Namespace</span></span><br/> | <span data-ttu-id="cfd76-126">**вмплиб**</span><span class="sxs-lookup"><span data-stu-id="cfd76-126">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="cfd76-127">Сборка</span><span class="sxs-lookup"><span data-stu-id="cfd76-127">Assembly</span></span><br/>  | <dl> <span data-ttu-id="cfd76-128"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="cfd76-128"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cfd76-129">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="cfd76-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cfd76-130">**Ивмпмедиаколлектион. Жетаттрибутестрингколлектион (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="cfd76-130">**IWMPMediaCollection.getAttributeStringCollection (VB and C#)**</span></span>](wmplibiwmpmediacollection-iwmpmediacollection-getattributestringcollection--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="cfd76-131">**IWMPSettings2. Медиаакцессригхтс (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="cfd76-131">**IWMPSettings2.mediaAccessRights (VB and C#)**</span></span>](wmplibiwmpsettings2-iwmpsettings2-mediaaccessrights--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="cfd76-132">**IWMPSettings2. Рекуестмедиаакцессригхтс (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="cfd76-132">**IWMPSettings2.requestMediaAccessRights (VB and C#)**</span></span>](wmplibiwmpsettings2-iwmpsettings2-requestmediaaccessrights--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="cfd76-133">**Интерфейс Ивмпстрингколлектион (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="cfd76-133">**IWMPStringCollection Interface (VB and C#)**</span></span>](iwmpstringcollection--vb-and-c.md)
</dt> </dl>

 

 





