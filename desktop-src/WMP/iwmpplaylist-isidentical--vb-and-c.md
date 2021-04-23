---
title: Ивмпплайлист. одинаковы (VB и C)
description: Свойство «идентично» (метод Get \_ одинаковы в C \) возвращает значение, указывающее, идентичен ли указанный список воспроизведения текущему списку воспроизведения.
ms.assetid: 0e5520ee-3d41-4e36-98f4-7bc2ec45fcb8
keywords:
- Проигрыватель Windows Media Ивмпплайлист. одинаковы (VB и C)
topic_type:
- apiref
api_name:
- IWMPPlaylist.isIdentical (VB and C )
api_location:
- Interop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bee30441e8f0275bba06f71a01095c39da8eae9f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105685154"
---
# <a name="iwmpplaylistisidentical-vb-and-c"></a><span data-ttu-id="9631a-104">Ивмпплайлист. одинаковы (VB и C#)</span><span class="sxs-lookup"><span data-stu-id="9631a-104">IWMPPlaylist.isIdentical (VB and C#)</span></span>

<span data-ttu-id="9631a-105">Свойство « **идентично** » (метод **Get \_ одинаковы** в C#) возвращает значение, указывающее, идентичен ли указанный список воспроизведения текущему списку воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="9631a-105">The **isIdentical** property (the **get\_isIdentical** method in C#) gets a value indicating whether the specified playlist is identical to the current playlist.</span></span>


```
[Visual Basic]
ReadOnly Property isIdentical(
  pIWMPPlaylist As IWMPPlaylist
) As System.Boolean
```




```
[C#]
System.Boolean get_isIdentical (
  IWMPPlaylist pIWMPPlaylist
);
```



## <a name="parameters"></a><span data-ttu-id="9631a-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="9631a-106">Parameters</span></span>

<span data-ttu-id="9631a-107">*пивмпплайлист*</span><span class="sxs-lookup"><span data-stu-id="9631a-107">*pIWMPPlaylist*</span></span>

<span data-ttu-id="9631a-108">Интерфейс **вмплиб. ивмпплайлист** для списка воспроизведения, сравниваемый этим методом с текущим списком воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="9631a-108">A **WMPLib.IWMPPlaylist** Interface for the playlist that this method compares to the current playlist.</span></span>

## <a name="property-value"></a><span data-ttu-id="9631a-109">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="9631a-109">Property Value</span></span>

<span data-ttu-id="9631a-110">Значение **System. Boolean** , указывающее, идентичны ли сравниваемые списки воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="9631a-110">A **System.Boolean** that indicates whether the compared playlists are identical.</span></span>

## <a name="remarks"></a><span data-ttu-id="9631a-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="9631a-111">Remarks</span></span>

<span data-ttu-id="9631a-112">**Ивмпплайлист.** ивмпплайлист — это свойство в Visual Basic, которое принимает параметр, а в C# называется методом **. Get \_ одинаковы** .</span><span class="sxs-lookup"><span data-stu-id="9631a-112">**IWMPPlaylist.isIdentical** is a property in Visual Basic that takes a parameter, while in C# it is referred to as the **IWMPPlaylist.get\_isIdentical** method.</span></span>

## <a name="requirements"></a><span data-ttu-id="9631a-113">Требования</span><span class="sxs-lookup"><span data-stu-id="9631a-113">Requirements</span></span>



| <span data-ttu-id="9631a-114">Требование</span><span class="sxs-lookup"><span data-stu-id="9631a-114">Requirement</span></span> | <span data-ttu-id="9631a-115">Значение</span><span class="sxs-lookup"><span data-stu-id="9631a-115">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9631a-116">Версия</span><span class="sxs-lookup"><span data-stu-id="9631a-116">Version</span></span><br/>   | <span data-ttu-id="9631a-117">Проигрыватель Windows Media 9 Series или более поздней версии</span><span class="sxs-lookup"><span data-stu-id="9631a-117">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="9631a-118">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="9631a-118">Namespace</span></span><br/> | <span data-ttu-id="9631a-119">**вмплиб**</span><span class="sxs-lookup"><span data-stu-id="9631a-119">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="9631a-120">Сборка</span><span class="sxs-lookup"><span data-stu-id="9631a-120">Assembly</span></span><br/>  | <dl> <span data-ttu-id="9631a-121"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="9631a-121"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9631a-122">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="9631a-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9631a-123">**Интерфейс Ивмпплайлист (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="9631a-123">**IWMPPlaylist Interface (VB and C#)**</span></span>](iwmpplaylist--vb-and-c.md)
</dt> </dl>

 

 





