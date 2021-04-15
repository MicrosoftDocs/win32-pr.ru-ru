---
title: Ивмпплайлистколлектион Жеталл, метод
description: Метод Жеталл возвращает интерфейс Ивмпплайлистаррай, который предоставляет доступ ко всем спискам воспроизведения в библиотеке.
ms.assetid: d36dbc5c-ccb0-400a-ab5b-918598c218f1
keywords:
- Жеталл метод Windows Media Player
- Жеталл метод проигрывателя Windows Media Player, интерфейс Ивмпплайлистколлектион
- Интерфейс Ивмпплайлистколлектион Windows Media Player, метод Жеталл
topic_type:
- apiref
api_name:
- IWMPPlaylistCollection.getAll
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a4260f5c960650cf6c04a1dd8b39d887f711fb8a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105708350"
---
# <a name="iwmpplaylistcollectiongetall-method"></a><span data-ttu-id="79b12-106">Метод Ивмпплайлистколлектион:: Жеталл</span><span class="sxs-lookup"><span data-stu-id="79b12-106">IWMPPlaylistCollection::getAll method</span></span>

<span data-ttu-id="79b12-107">Метод **жеталл** возвращает интерфейс **ивмпплайлистаррай** , который предоставляет доступ ко всем спискам воспроизведения в библиотеке.</span><span class="sxs-lookup"><span data-stu-id="79b12-107">The **getAll** method returns an **IWMPPlaylistArray** interface that provides access to all of the playlists in the library.</span></span>

## <a name="syntax"></a><span data-ttu-id="79b12-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="79b12-108">Syntax</span></span>


```CSharp
public IWMPPlaylistArray getAll();
```


```VB

Public Function getAll() As IWMPPlaylistArray
Implements IWMPPlaylistCollection.getAll
```





## <a name="parameters"></a><span data-ttu-id="79b12-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="79b12-109">Parameters</span></span>

<span data-ttu-id="79b12-110">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="79b12-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="79b12-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="79b12-111">Return value</span></span>

<span data-ttu-id="79b12-112">Интерфейс **вмплиб. ивмпплайлистаррай** для извлеченного массива списков воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="79b12-112">A **WMPLib.IWMPPlaylistArray** interface for the retrieved array of playlists.</span></span>

## <a name="remarks"></a><span data-ttu-id="79b12-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="79b12-113">Remarks</span></span>

<span data-ttu-id="79b12-114">Перед вызовом этого метода необходимо иметь доступ на чтение к библиотеке.</span><span class="sxs-lookup"><span data-stu-id="79b12-114">Before calling this method, you must have read access to the library.</span></span> <span data-ttu-id="79b12-115">Дополнительные сведения см. в разделе [доступ к библиотеке](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="79b12-115">For more information, see [Library Access](library-access.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="79b12-116">Требования</span><span class="sxs-lookup"><span data-stu-id="79b12-116">Requirements</span></span>



| <span data-ttu-id="79b12-117">Требование</span><span class="sxs-lookup"><span data-stu-id="79b12-117">Requirement</span></span> | <span data-ttu-id="79b12-118">Значение</span><span class="sxs-lookup"><span data-stu-id="79b12-118">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="79b12-119">Версия</span><span class="sxs-lookup"><span data-stu-id="79b12-119">Version</span></span><br/>   | <span data-ttu-id="79b12-120">Проигрыватель Windows Media 9 Series или более поздней версии.</span><span class="sxs-lookup"><span data-stu-id="79b12-120">Windows Media Player 9 Series or later.</span></span><br/>                                                                     |
| <span data-ttu-id="79b12-121">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="79b12-121">Namespace</span></span><br/> | <span data-ttu-id="79b12-122">**вмплиб**</span><span class="sxs-lookup"><span data-stu-id="79b12-122">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="79b12-123">Сборка</span><span class="sxs-lookup"><span data-stu-id="79b12-123">Assembly</span></span><br/>  | <dl> <span data-ttu-id="79b12-124"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="79b12-124"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="79b12-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="79b12-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="79b12-126">**Интерфейс Ивмпплайлистаррай (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="79b12-126">**IWMPPlaylistArray Interface (VB and C#)**</span></span>](iwmpplaylistarray--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="79b12-127">**Интерфейс Ивмпплайлистколлектион (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="79b12-127">**IWMPPlaylistCollection Interface (VB and C#)**</span></span>](iwmpplaylistcollection--vb-and-c.md)
</dt> </dl>

 

 





