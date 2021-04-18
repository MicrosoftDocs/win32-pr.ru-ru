---
title: Метод Ивмпкдромколлектион Item
description: Метод Item возвращает интерфейс Ивмпкдром по заданному индексу.
ms.assetid: 66e51aa9-39c8-4b79-9cc7-d7125516e87e
keywords:
- Метод Item проигрыватель Windows Media Player
- Метод Item проигрыватель Windows Media Player, интерфейс Ивмпкдромколлектион
- Интерфейс Ивмпкдромколлектион Windows Media Player, метод Item
topic_type:
- apiref
api_name:
- IWMPCdromCollection.Item
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bf0c4a0c79a17b1e6956ba640daec74f0cbb2825
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105717956"
---
# <a name="iwmpcdromcollectionitem-method"></a><span data-ttu-id="ed47e-106">Метод Ивмпкдромколлектион:: Item</span><span class="sxs-lookup"><span data-stu-id="ed47e-106">IWMPCdromCollection::Item method</span></span>

<span data-ttu-id="ed47e-107">Метод **Item** возвращает интерфейс **ивмпкдром** по заданному индексу.</span><span class="sxs-lookup"><span data-stu-id="ed47e-107">The **Item** method returns an **IWMPCdrom** interface at the given index.</span></span>

## <a name="syntax"></a><span data-ttu-id="ed47e-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="ed47e-108">Syntax</span></span>


```CSharp
public IWMPCdrom Item(
  System.Int32 lIndex
);
```


```VB

Public Function Item( _
  ByVal lIndex As System.Int32 _
) As IWMPCdrom
Implements IWMPCdromCollection.Item
```





## <a name="parameters"></a><span data-ttu-id="ed47e-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="ed47e-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ed47e-110">*Линдекс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="ed47e-110">*lIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ed47e-111">Объект **System. Int32** , который является индексом.</span><span class="sxs-lookup"><span data-stu-id="ed47e-111">A **System.Int32** that is the index.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ed47e-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="ed47e-112">Return value</span></span>

<span data-ttu-id="ed47e-113">Интерфейс **вмплиб. ивмпкдром** .</span><span class="sxs-lookup"><span data-stu-id="ed47e-113">A **WMPLib.IWMPCdrom** interface.</span></span>

## <a name="remarks"></a><span data-ttu-id="ed47e-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="ed47e-114">Remarks</span></span>

<span data-ttu-id="ed47e-115">Чтобы использовать этот метод, требуется доступ на чтение к библиотеке.</span><span class="sxs-lookup"><span data-stu-id="ed47e-115">To use this method, read access to the library is required.</span></span> <span data-ttu-id="ed47e-116">Дополнительные сведения см. в разделе [доступ к библиотеке](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="ed47e-116">For more information, see [Library Access](library-access.md).</span></span>

## <a name="examples"></a><span data-ttu-id="ed47e-117">Примеры</span><span class="sxs-lookup"><span data-stu-id="ed47e-117">Examples</span></span>

<span data-ttu-id="ed47e-118">В следующем примере **элемент** используется для вывода спецификатора диска и имени списка воспроизведения с каждого компакт-диска, доступного на компьютере в окне списка.</span><span class="sxs-lookup"><span data-stu-id="ed47e-118">The following example uses **Item** to display the drive specifier and playlist name from each CD available on the computer in a list box.</span></span> <span data-ttu-id="ed47e-119">Если на самом деле диск содержит содержимое DVD, требуется ОС Windows XP или более поздней версии.</span><span class="sxs-lookup"><span data-stu-id="ed47e-119">If the drive actually contains DVD content, Windows XP or later is required.</span></span> <span data-ttu-id="ed47e-120">Объект **аксвмплиб. аксвиндовсмедиаплайер** представлен переменной с именем Player.</span><span class="sxs-lookup"><span data-stu-id="ed47e-120">The **AxWMPLib.AxWindowsMediaPlayer** object is represented by the variable named player.</span></span>


```CSharp
// Store the number of available drives.
int numDrives = player.cdromCollection.count;

// Loop through the available drives.
for (int i = 0; i < numDrives; i++)
{
    // Store the drive specifier and playlist name for this drive in a string.
    string pl = player.cdromCollection.Item(i).driveSpecifier + " ";
    pl += player.cdromCollection.Item(i).Playlist.name;

    // Add the string to a list box.
    myPlaylists.Items.Add(pl);
}
```


```VB

' Store the number of available drives.
Dim numDrives As Integer = player.cdromCollection.count

&#39; Loop through the available drives.
For i As Integer = 0 To (numDrives - 1)

    &#39; Store the drive specifier and playlist name for this drive in a string.
    Dim pl As String = player.cdromCollection.Item(i).driveSpecifier + &quot; &quot;
    pl += player.cdromCollection.Item(i).Playlist.name

    &#39; Add the string to a list box.
    myPlaylists.Items.Add(pl)

Next i
```





## <a name="requirements"></a><span data-ttu-id="ed47e-121">Требования</span><span class="sxs-lookup"><span data-stu-id="ed47e-121">Requirements</span></span>



| <span data-ttu-id="ed47e-122">Требование</span><span class="sxs-lookup"><span data-stu-id="ed47e-122">Requirement</span></span> | <span data-ttu-id="ed47e-123">Значение</span><span class="sxs-lookup"><span data-stu-id="ed47e-123">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ed47e-124">Версия</span><span class="sxs-lookup"><span data-stu-id="ed47e-124">Version</span></span><br/>   | <span data-ttu-id="ed47e-125">Проигрыватель Windows Media 9 Series или более поздней версии</span><span class="sxs-lookup"><span data-stu-id="ed47e-125">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="ed47e-126">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="ed47e-126">Namespace</span></span><br/> | <span data-ttu-id="ed47e-127">**вмплиб**</span><span class="sxs-lookup"><span data-stu-id="ed47e-127">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="ed47e-128">Сборка</span><span class="sxs-lookup"><span data-stu-id="ed47e-128">Assembly</span></span><br/>  | <dl> <span data-ttu-id="ed47e-129"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="ed47e-129"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ed47e-130">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="ed47e-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ed47e-131">**Интерфейс Ивмпкдром (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="ed47e-131">**IWMPCdrom Interface (VB and C#)**</span></span>](iwmpcdrom--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="ed47e-132">**Интерфейс Ивмпкдромколлектион (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="ed47e-132">**IWMPCdromCollection Interface (VB and C#)**</span></span>](iwmpcdromcollection--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="ed47e-133">**Ивмпкдромколлектион. Count (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="ed47e-133">**IWMPCdromCollection.count (VB and C#)**</span></span>](wmplibiwmpcdromcollection-iwmpcdromcollection-count--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="ed47e-134">**Ивмпкдромколлектион. ЖетбидривеспеЦифиер (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="ed47e-134">**IWMPCdromCollection.getByDriveSpecifier (VB and C#)**</span></span>](wmplibiwmpcdromcollection-iwmpcdromcollection-getbydrivespecifier--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="ed47e-135">**IWMPPlaylist.name (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="ed47e-135">**IWMPPlaylist.name (VB and C#)**</span></span>](wmplibiwmpplaylist-iwmpplaylist-name--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="ed47e-136">**IWMPSettings2. Медиаакцессригхтс (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="ed47e-136">**IWMPSettings2.mediaAccessRights (VB and C#)**</span></span>](wmplibiwmpsettings2-iwmpsettings2-mediaaccessrights--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="ed47e-137">**IWMPSettings2. Рекуестмедиаакцессригхтс (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="ed47e-137">**IWMPSettings2.requestMediaAccessRights (VB and C#)**</span></span>](wmplibiwmpsettings2-iwmpsettings2-requestmediaaccessrights--vb-and-c.md)
</dt> </dl>

 

 





