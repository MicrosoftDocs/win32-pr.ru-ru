---
title: Ивмпплайлистколлектион Remove, метод
description: Метод Remove удаляет список воспроизведения из библиотеки. | Ивмпплайлистколлектион Remove, метод
ms.assetid: 40c8ee1d-13fa-40d9-9532-4dc8383c4eb3
keywords:
- метод Remove Windows Media Player
- метод Remove Windows Media Player, интерфейс Ивмпплайлистколлектион
- Интерфейс Ивмпплайлистколлектион Windows Media Player, Remove, метод
topic_type:
- apiref
api_name:
- IWMPPlaylistCollection.remove
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c99fbaa2f60c769599bd6173b8e38f4d99e9f42d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105718178"
---
# <a name="iwmpplaylistcollectionremove-method"></a><span data-ttu-id="1b738-107">Метод Ивмпплайлистколлектион:: Remove</span><span class="sxs-lookup"><span data-stu-id="1b738-107">IWMPPlaylistCollection::remove method</span></span>

<span data-ttu-id="1b738-108">Метод **Remove** удаляет список воспроизведения из библиотеки.</span><span class="sxs-lookup"><span data-stu-id="1b738-108">The **remove** method removes a playlist from the library.</span></span>

## <a name="syntax"></a><span data-ttu-id="1b738-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="1b738-109">Syntax</span></span>


```CSharp
public void remove(
  IWMPPlaylist pItem
);
```


```VB

Public Sub remove( _
  ByVal pItem As IWMPPlaylist _
)
Implements IWMPPlaylistCollection.remove
```





## <a name="parameters"></a><span data-ttu-id="1b738-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="1b738-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1b738-111">*питем* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="1b738-111">*pItem* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1b738-112">Интерфейс **вмплиб. ивмпплайлист** для списка воспроизведения, который будет удален этим методом.</span><span class="sxs-lookup"><span data-stu-id="1b738-112">A **WMPLib.IWMPPlaylist** interface for the playlist that this method will remove.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1b738-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="1b738-113">Return value</span></span>

<span data-ttu-id="1b738-114">Этот метод не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="1b738-114">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="1b738-115">Комментарии</span><span class="sxs-lookup"><span data-stu-id="1b738-115">Remarks</span></span>

<span data-ttu-id="1b738-116">Перед вызовом этого метода необходимо иметь полный доступ к библиотеке.</span><span class="sxs-lookup"><span data-stu-id="1b738-116">Before calling this method, you must have full access to the library.</span></span> <span data-ttu-id="1b738-117">Дополнительные сведения см. в разделе [доступ к библиотеке](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="1b738-117">For more information, see [Library Access](library-access.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="1b738-118">Требования</span><span class="sxs-lookup"><span data-stu-id="1b738-118">Requirements</span></span>



| <span data-ttu-id="1b738-119">Требование</span><span class="sxs-lookup"><span data-stu-id="1b738-119">Requirement</span></span> | <span data-ttu-id="1b738-120">Значение</span><span class="sxs-lookup"><span data-stu-id="1b738-120">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1b738-121">Версия</span><span class="sxs-lookup"><span data-stu-id="1b738-121">Version</span></span><br/>   | <span data-ttu-id="1b738-122">Проигрыватель Windows Media 9 Series или более поздней версии.</span><span class="sxs-lookup"><span data-stu-id="1b738-122">Windows Media Player 9 Series or later.</span></span><br/>                                                                     |
| <span data-ttu-id="1b738-123">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="1b738-123">Namespace</span></span><br/> | <span data-ttu-id="1b738-124">**вмплиб**</span><span class="sxs-lookup"><span data-stu-id="1b738-124">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="1b738-125">Сборка</span><span class="sxs-lookup"><span data-stu-id="1b738-125">Assembly</span></span><br/>  | <dl> <span data-ttu-id="1b738-126"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="1b738-126"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1b738-127">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="1b738-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1b738-128">**Интерфейс Ивмпплайлист (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="1b738-128">**IWMPPlaylist Interface (VB and C#)**</span></span>](iwmpplaylist--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="1b738-129">**Интерфейс Ивмпплайлистколлектион (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="1b738-129">**IWMPPlaylistCollection Interface (VB and C#)**</span></span>](iwmpplaylistcollection--vb-and-c.md)
</dt> </dl>

 

 





