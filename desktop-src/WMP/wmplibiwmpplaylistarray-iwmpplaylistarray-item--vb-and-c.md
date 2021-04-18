---
title: Метод Ивмпплайлистаррай Item
description: Метод Item возвращает интерфейс Ивмпплайлист, представляющий список воспроизведения по указанному индексу.
ms.assetid: 5cb4b89f-b679-4d92-a5f9-5d0fe686775d
keywords:
- Метод Item проигрыватель Windows Media Player
- Метод Item проигрыватель Windows Media Player, интерфейс Ивмпплайлистаррай
- Интерфейс Ивмпплайлистаррай Windows Media Player, метод Item
topic_type:
- apiref
api_name:
- IWMPPlaylistArray.Item
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 660e919ef51bbb9584971f25bdf92296d331de23
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105718021"
---
# <a name="iwmpplaylistarrayitem-method"></a><span data-ttu-id="af892-106">Метод Ивмпплайлистаррай:: Item</span><span class="sxs-lookup"><span data-stu-id="af892-106">IWMPPlaylistArray::Item method</span></span>

<span data-ttu-id="af892-107">Метод **Item** возвращает интерфейс **ивмпплайлист** , представляющий список воспроизведения по указанному индексу.</span><span class="sxs-lookup"><span data-stu-id="af892-107">The **Item** method returns an **IWMPPlaylist** interface representing the playlist at the specified index.</span></span>

## <a name="syntax"></a><span data-ttu-id="af892-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="af892-108">Syntax</span></span>


```CSharp
public IWMPPlaylist Item(
  System.Int32 lIndex
);
```


```VB

Public Function Item( _
  ByVal lIndex As System.Int32 _
) As IWMPPlaylist
Implements IWMPPlaylistArray.Item
```





## <a name="parameters"></a><span data-ttu-id="af892-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="af892-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="af892-110">*Линдекс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="af892-110">*lIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="af892-111">Объект **System. Int32** , содержащий индекс, определяющий список воспроизведения, который должен быть извлечен методом.</span><span class="sxs-lookup"><span data-stu-id="af892-111">A **System.Int32** containing the index that identifies the playlist that the method should retrieve.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="af892-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="af892-112">Return value</span></span>

<span data-ttu-id="af892-113">Интерфейс **вмплиб. ивмпплайлист** для полученного списка воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="af892-113">A **WMPLib.IWMPPlaylist** interface for the retrieved playlist.</span></span>

## <a name="remarks"></a><span data-ttu-id="af892-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="af892-114">Remarks</span></span>

<span data-ttu-id="af892-115">Перед вызовом этого метода необходимо иметь доступ на чтение к библиотеке.</span><span class="sxs-lookup"><span data-stu-id="af892-115">Before calling this method, you must have read access to the library.</span></span> <span data-ttu-id="af892-116">Дополнительные сведения см. в разделе [доступ к библиотеке](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="af892-116">For more information, see [Library Access](library-access.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="af892-117">Требования</span><span class="sxs-lookup"><span data-stu-id="af892-117">Requirements</span></span>



| <span data-ttu-id="af892-118">Требование</span><span class="sxs-lookup"><span data-stu-id="af892-118">Requirement</span></span> | <span data-ttu-id="af892-119">Значение</span><span class="sxs-lookup"><span data-stu-id="af892-119">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="af892-120">Версия</span><span class="sxs-lookup"><span data-stu-id="af892-120">Version</span></span><br/>   | <span data-ttu-id="af892-121">Проигрыватель Windows Media 9 Series или более поздней версии.</span><span class="sxs-lookup"><span data-stu-id="af892-121">Windows Media Player 9 Series or later.</span></span><br/>                                                                     |
| <span data-ttu-id="af892-122">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="af892-122">Namespace</span></span><br/> | <span data-ttu-id="af892-123">**вмплиб**</span><span class="sxs-lookup"><span data-stu-id="af892-123">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="af892-124">Сборка</span><span class="sxs-lookup"><span data-stu-id="af892-124">Assembly</span></span><br/>  | <dl> <span data-ttu-id="af892-125"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="af892-125"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="af892-126">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="af892-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="af892-127">**Интерфейс Ивмпплайлист (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="af892-127">**IWMPPlaylist Interface (VB and C#)**</span></span>](iwmpplaylist--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="af892-128">**Интерфейс Ивмпплайлистаррай (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="af892-128">**IWMPPlaylistArray Interface (VB and C#)**</span></span>](iwmpplaylistarray--vb-and-c.md)
</dt> </dl>

 

 





