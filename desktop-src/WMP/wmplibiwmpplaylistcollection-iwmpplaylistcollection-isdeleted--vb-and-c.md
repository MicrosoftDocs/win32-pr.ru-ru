---
title: Ивмпплайлистколлектион метод isDeleted
description: Метод IsDeleted возвращает значение, указывающее, находится ли указанный список воспроизведения в папке удаленных элементов.
ms.assetid: 02bc4b9f-6149-4fe2-8417-6484b22f2d74
keywords:
- метод IsDeleted Windows Media Player
- метод IsDeleted Windows Media Player, интерфейс Ивмпплайлистколлектион
- Интерфейс Ивмпплайлистколлектион Windows Media Player, метод isDeleted
topic_type:
- apiref
api_name:
- IWMPPlaylistCollection.isDeleted
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7d4ce4a314378c5a4a211a52b99ea1b36ae1fda8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105704052"
---
# <a name="iwmpplaylistcollectionisdeleted-method"></a><span data-ttu-id="283ad-106">Метод Ивмпплайлистколлектион:: isDeleted</span><span class="sxs-lookup"><span data-stu-id="283ad-106">IWMPPlaylistCollection::isDeleted method</span></span>

<span data-ttu-id="283ad-107">Метод **IsDeleted** возвращает значение, указывающее, находится ли указанный список воспроизведения в папке удаленных элементов.</span><span class="sxs-lookup"><span data-stu-id="283ad-107">The **isDeleted** method returns a value indicating whether the specified playlist is in the deleted items folder.</span></span>

## <a name="syntax"></a><span data-ttu-id="283ad-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="283ad-108">Syntax</span></span>


```CSharp
public System.Boolean isDeleted(
  IWMPPlaylist pItem
);
```


```VB

Public Function isDeleted( _
  ByVal pItem As IWMPPlaylist _
) As System.Boolean
Implements IWMPPlaylistCollection.isDeleted
```





## <a name="parameters"></a><span data-ttu-id="283ad-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="283ad-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="283ad-110">*питем* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="283ad-110">*pItem* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="283ad-111">Интерфейс **вмплиб. ивмпплайлист** для запрашиваемого списка воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="283ad-111">A **WMPLib.IWMPPlaylist** interface for the queried playlist.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="283ad-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="283ad-112">Return value</span></span>

<span data-ttu-id="283ad-113">Значение **System. Boolean** , указывающее, был ли удален список воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="283ad-113">A **System.Boolean** that specifies whether the playlist was deleted.</span></span>

## <a name="requirements"></a><span data-ttu-id="283ad-114">Требования</span><span class="sxs-lookup"><span data-stu-id="283ad-114">Requirements</span></span>



| <span data-ttu-id="283ad-115">Требование</span><span class="sxs-lookup"><span data-stu-id="283ad-115">Requirement</span></span> | <span data-ttu-id="283ad-116">Значение</span><span class="sxs-lookup"><span data-stu-id="283ad-116">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="283ad-117">Версия</span><span class="sxs-lookup"><span data-stu-id="283ad-117">Version</span></span><br/>   | <span data-ttu-id="283ad-118">Проигрыватель Windows Media 9 Series или более поздней версии.</span><span class="sxs-lookup"><span data-stu-id="283ad-118">Windows Media Player 9 Series or later.</span></span><br/>                                                                     |
| <span data-ttu-id="283ad-119">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="283ad-119">Namespace</span></span><br/> | <span data-ttu-id="283ad-120">**вмплиб**</span><span class="sxs-lookup"><span data-stu-id="283ad-120">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="283ad-121">Сборка</span><span class="sxs-lookup"><span data-stu-id="283ad-121">Assembly</span></span><br/>  | <dl> <span data-ttu-id="283ad-122"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="283ad-122"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="283ad-123">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="283ad-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="283ad-124">**Интерфейс Ивмпплайлист (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="283ad-124">**IWMPPlaylist Interface (VB and C#)**</span></span>](iwmpplaylist--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="283ad-125">**Интерфейс Ивмпплайлистколлектион (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="283ad-125">**IWMPPlaylistCollection Interface (VB and C#)**</span></span>](iwmpplaylistcollection--vb-and-c.md)
</dt> </dl>

 

 





