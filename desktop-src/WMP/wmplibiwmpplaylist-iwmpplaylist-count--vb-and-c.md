---
title: Ивмпплайлист Count, свойство
description: Свойство Count возвращает количество элементов мультимедиа в списке воспроизведения.
ms.assetid: dbff3c86-2d42-4d47-a5cb-b8199efac728
keywords:
- Свойство Count проигрывателя Windows Media Player
- Свойство Count проигрывателя Windows Media Player, интерфейс Ивмпплайлист
- Интерфейс Ивмпплайлист Windows Media Player, свойство Count
topic_type:
- apiref
api_name:
- IWMPPlaylist.count
- IWMPPlaylist.get_count
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 56d988fefc436b65652d2b0765320ca289417c9c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105708402"
---
# <a name="iwmpplaylistcount-property"></a><span data-ttu-id="7a35e-106">Свойство Ивмпплайлист:: count</span><span class="sxs-lookup"><span data-stu-id="7a35e-106">IWMPPlaylist::count property</span></span>

<span data-ttu-id="7a35e-107">Свойство **Count** возвращает количество элементов мультимедиа в списке воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="7a35e-107">The **count** property gets the number of media items in a playlist.</span></span>

<span data-ttu-id="7a35e-108">Это свойство доступно только для чтения.</span><span class="sxs-lookup"><span data-stu-id="7a35e-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="7a35e-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="7a35e-109">Syntax</span></span>


```CSharp
public System.Int32 count {get;}
```


```VB

Public ReadOnly Property count As System.Int32
```





## <a name="property-value"></a><span data-ttu-id="7a35e-110">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="7a35e-110">Property value</span></span>

<span data-ttu-id="7a35e-111">Объект **System. Int32** , который является числом элементов мультимедиа в списке воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="7a35e-111">A **System.Int32** that is the number of media items in the playlist.</span></span>

## <a name="remarks"></a><span data-ttu-id="7a35e-112">Комментарии</span><span class="sxs-lookup"><span data-stu-id="7a35e-112">Remarks</span></span>

<span data-ttu-id="7a35e-113">Перед использованием этого свойства необходимо иметь доступ на чтение к библиотеке.</span><span class="sxs-lookup"><span data-stu-id="7a35e-113">Before using this property, you must have read access to the library.</span></span> <span data-ttu-id="7a35e-114">Дополнительные сведения см. в разделе [доступ к библиотеке](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="7a35e-114">For more information, see [Library Access](library-access.md).</span></span>

<span data-ttu-id="7a35e-115">Пример кода, в котором используется это свойство, см. в свойстве [аттрибутекаунт](wmplibiwmpplaylist-iwmpplaylist-attributecount--vb-and-c.md) .</span><span class="sxs-lookup"><span data-stu-id="7a35e-115">See the [attributeCount](wmplibiwmpplaylist-iwmpplaylist-attributecount--vb-and-c.md) property for example code that uses this property.</span></span>

## <a name="requirements"></a><span data-ttu-id="7a35e-116">Требования</span><span class="sxs-lookup"><span data-stu-id="7a35e-116">Requirements</span></span>



| <span data-ttu-id="7a35e-117">Требование</span><span class="sxs-lookup"><span data-stu-id="7a35e-117">Requirement</span></span> | <span data-ttu-id="7a35e-118">Значение</span><span class="sxs-lookup"><span data-stu-id="7a35e-118">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7a35e-119">Версия</span><span class="sxs-lookup"><span data-stu-id="7a35e-119">Version</span></span><br/>   | <span data-ttu-id="7a35e-120">Проигрыватель Windows Media 9 Series или более поздней версии</span><span class="sxs-lookup"><span data-stu-id="7a35e-120">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="7a35e-121">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="7a35e-121">Namespace</span></span><br/> | <span data-ttu-id="7a35e-122">**вмплиб**</span><span class="sxs-lookup"><span data-stu-id="7a35e-122">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="7a35e-123">Сборка</span><span class="sxs-lookup"><span data-stu-id="7a35e-123">Assembly</span></span><br/>  | <dl> <span data-ttu-id="7a35e-124"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="7a35e-124"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7a35e-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="7a35e-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7a35e-126">**Интерфейс Ивмпплайлист (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="7a35e-126">**IWMPPlaylist Interface (VB and C#)**</span></span>](iwmpplaylist--vb-and-c.md)
</dt> </dl>

 

 





