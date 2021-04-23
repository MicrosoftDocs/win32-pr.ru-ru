---
title: Ивмпстрингколлектион Count, свойство
description: Свойство Count возвращает количество элементов в коллекции строк.
ms.assetid: 0ba2d158-fa54-46a8-9124-8a412e71bd09
keywords:
- Свойство Count проигрывателя Windows Media Player
- Свойство Count проигрывателя Windows Media Player, интерфейс Ивмпстрингколлектион
- Интерфейс Ивмпстрингколлектион Windows Media Player, свойство Count
topic_type:
- apiref
api_name:
- IWMPStringCollection.count
- IWMPStringCollection.get_count
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 00c520ab346737d1599d79d80ea3acd36c9b84fe
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105689430"
---
# <a name="iwmpstringcollectioncount-property"></a><span data-ttu-id="d2735-106">Свойство Ивмпстрингколлектион:: count</span><span class="sxs-lookup"><span data-stu-id="d2735-106">IWMPStringCollection::count property</span></span>

<span data-ttu-id="d2735-107">Свойство **Count** возвращает количество элементов в коллекции строк.</span><span class="sxs-lookup"><span data-stu-id="d2735-107">The **count** property gets the number of items in the string collection.</span></span>

<span data-ttu-id="d2735-108">Это свойство доступно только для чтения.</span><span class="sxs-lookup"><span data-stu-id="d2735-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="d2735-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="d2735-109">Syntax</span></span>


```CSharp
public System.Int32 count {get;}
```


```VB

Public ReadOnly Property count As System.Int32
```





## <a name="property-value"></a><span data-ttu-id="d2735-110">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="d2735-110">Property value</span></span>

<span data-ttu-id="d2735-111">Объект **System. Int32** , который является числом элементов в коллекции строк.</span><span class="sxs-lookup"><span data-stu-id="d2735-111">A **System.Int32** that is the number of items in the string collection.</span></span>

## <a name="remarks"></a><span data-ttu-id="d2735-112">Комментарии</span><span class="sxs-lookup"><span data-stu-id="d2735-112">Remarks</span></span>

<span data-ttu-id="d2735-113">Перед использованием этого свойства необходимо иметь доступ на чтение к библиотеке.</span><span class="sxs-lookup"><span data-stu-id="d2735-113">Before using this property, you must have read access to the library.</span></span> <span data-ttu-id="d2735-114">Дополнительные сведения см. в разделе [доступ к библиотеке](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="d2735-114">For more information, see [Library Access](library-access.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="d2735-115">Требования</span><span class="sxs-lookup"><span data-stu-id="d2735-115">Requirements</span></span>



| <span data-ttu-id="d2735-116">Требование</span><span class="sxs-lookup"><span data-stu-id="d2735-116">Requirement</span></span> | <span data-ttu-id="d2735-117">Значение</span><span class="sxs-lookup"><span data-stu-id="d2735-117">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d2735-118">Версия</span><span class="sxs-lookup"><span data-stu-id="d2735-118">Version</span></span><br/>   | <span data-ttu-id="d2735-119">Проигрыватель Windows Media 9 Series или более поздней версии</span><span class="sxs-lookup"><span data-stu-id="d2735-119">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="d2735-120">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="d2735-120">Namespace</span></span><br/> | <span data-ttu-id="d2735-121">**вмплиб**</span><span class="sxs-lookup"><span data-stu-id="d2735-121">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="d2735-122">Сборка</span><span class="sxs-lookup"><span data-stu-id="d2735-122">Assembly</span></span><br/>  | <dl> <span data-ttu-id="d2735-123"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="d2735-123"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d2735-124">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="d2735-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d2735-125">**IWMPSettings2. Медиаакцессригхтс (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="d2735-125">**IWMPSettings2.mediaAccessRights (VB and C#)**</span></span>](wmplibiwmpsettings2-iwmpsettings2-mediaaccessrights--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="d2735-126">**IWMPSettings2. Рекуестмедиаакцессригхтс (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="d2735-126">**IWMPSettings2.requestMediaAccessRights (VB and C#)**</span></span>](wmplibiwmpsettings2-iwmpsettings2-requestmediaaccessrights--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="d2735-127">**Интерфейс Ивмпстрингколлектион (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="d2735-127">**IWMPStringCollection Interface (VB and C#)**</span></span>](iwmpstringcollection--vb-and-c.md)
</dt> </dl>

 

 





