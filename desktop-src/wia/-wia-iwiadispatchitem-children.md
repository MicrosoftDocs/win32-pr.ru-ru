---
description: Свойство Children объекта Item извлекает коллекцию объектов Item. Элементы в этой коллекции представляют элементы, которые являются прямыми дочерними элементами данного элемента в иерархическом дереве. Только для чтения.
ms.assetid: 94ad3385-9ce9-4a44-87bb-1d7170c8d45c
title: Свойство Item. Children
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Item.Children
api_type:
- COM
api_location:
- Wiascr.dll
ms.openlocfilehash: 144b60f1c8e9b500d49b53dfe290565c23023220
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105719367"
---
# <a name="itemchildren-property"></a><span data-ttu-id="4d5f1-105">Свойство Item. Children</span><span class="sxs-lookup"><span data-stu-id="4d5f1-105">Item.Children property</span></span>

<span data-ttu-id="4d5f1-106">Свойство **Children** объекта [**Item**](-wia-item.md) извлекает коллекцию объектов **Item** .</span><span class="sxs-lookup"><span data-stu-id="4d5f1-106">The **Children** property of the [**Item**](-wia-item.md) object retrieves a collection of **Item** objects.</span></span> <span data-ttu-id="4d5f1-107">Элементы в этой коллекции представляют элементы, которые являются прямыми дочерними элементами данного элемента в иерархическом дереве.</span><span class="sxs-lookup"><span data-stu-id="4d5f1-107">The items in this collection represent items that are direct children of this item in the hierarchical tree.</span></span> <span data-ttu-id="4d5f1-108">Только для чтения.</span><span class="sxs-lookup"><span data-stu-id="4d5f1-108">Read-only.</span></span>

<span data-ttu-id="4d5f1-109">Это свойство доступно только для чтения.</span><span class="sxs-lookup"><span data-stu-id="4d5f1-109">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="4d5f1-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="4d5f1-110">Syntax</span></span>


```JScript
propVal = Item.Children
```



## <a name="property-value"></a><span data-ttu-id="4d5f1-111">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="4d5f1-111">Property value</span></span>

<span data-ttu-id="4d5f1-112">Переменная, которая получает объекты.</span><span class="sxs-lookup"><span data-stu-id="4d5f1-112">Variable that receives the objects.</span></span>

## <a name="remarks"></a><span data-ttu-id="4d5f1-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="4d5f1-113">Remarks</span></span>

<span data-ttu-id="4d5f1-114">Это свойство используется для навигации по иерархическому дереву объектов [**элементов**](-wia-item.md) , представляющих устройство, папки и файлы, которые находятся на устройстве.</span><span class="sxs-lookup"><span data-stu-id="4d5f1-114">Use this property to navigate the hierarchical tree of [**Item**](-wia-item.md) objects that represent a device, the folders and the files that reside on the device.</span></span>

<span data-ttu-id="4d5f1-115">Свойство **Children** — это коллекция объектов [**элементов**](-wia-item.md) только из уровня, расположенного непосредственно под этим объектом **Item** в дереве.</span><span class="sxs-lookup"><span data-stu-id="4d5f1-115">The **Children** property is a collection of [**Item**](-wia-item.md) objects only from the level directly beneath this **Item** object in the tree.</span></span> <span data-ttu-id="4d5f1-116">Чтобы перейти к более подробному уровню вниз по дереву, используйте это свойство рекурсивно.</span><span class="sxs-lookup"><span data-stu-id="4d5f1-116">To navigate further levels down the tree, use this property recursively.</span></span>

<span data-ttu-id="4d5f1-117">Если элемент не может или не имеет дочерних элементов, это свойство возвращает пустую коллекцию.</span><span class="sxs-lookup"><span data-stu-id="4d5f1-117">If the item cannot or does not have any child items, this property returns an empty collection.</span></span>

> [!Note]  
> <span data-ttu-id="4d5f1-118">Эта коллекция основана на 0.</span><span class="sxs-lookup"><span data-stu-id="4d5f1-118">This collection is 0-based.</span></span>

 

## <a name="examples"></a><span data-ttu-id="4d5f1-119">Примеры</span><span class="sxs-lookup"><span data-stu-id="4d5f1-119">Examples</span></span>

<span data-ttu-id="4d5f1-120">В следующем примере показано использование свойства **Children** для извлечения и перечисления коллекции дочерних элементов устройства.</span><span class="sxs-lookup"><span data-stu-id="4d5f1-120">The following example demonstrates the use of the **Children** property to retrieve and enumerate a collection of the child items of a device.</span></span> <span data-ttu-id="4d5f1-121">Если устройство является цифровой камерой, коллекция обычно содержит элементы папки и изображения.</span><span class="sxs-lookup"><span data-stu-id="4d5f1-121">If the device is a digital camera, the collection typically contains folder and image items.</span></span> <span data-ttu-id="4d5f1-122">Если устройство является сканером, коллекция обычно содержит элементы, представляющие сканирование кроватях.</span><span class="sxs-lookup"><span data-stu-id="4d5f1-122">If the device is a scanner, the collection typically contains items that represent scanning beds.</span></span>


```JScript
<SCRIPT LANGUAGE="VBScript">
Dim objWia
Dim objDeviceInfoCollection
Dim objDeviceInfo
Dim objRootItem
Dim objItemCollection
Dim objItem
 
Set objWIA = CreateObject("Wia.Script")
 
Set objDeviceInfoCollection = objWia.Devices
 
For Each objDeviceInfo In objDeviceInfoCollection
    Set objRootItem = objWia.Create(objDeviceInfo)
    objItemCollection = objRootItem.Children
    For Each objItem In objItemCollection
        ' Do something with the child item
    Next
Next
</SCRIPT>
```



## <a name="requirements"></a><span data-ttu-id="4d5f1-123">Требования</span><span class="sxs-lookup"><span data-stu-id="4d5f1-123">Requirements</span></span>



| <span data-ttu-id="4d5f1-124">Требование</span><span class="sxs-lookup"><span data-stu-id="4d5f1-124">Requirement</span></span> | <span data-ttu-id="4d5f1-125">Значение</span><span class="sxs-lookup"><span data-stu-id="4d5f1-125">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4d5f1-126">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="4d5f1-126">Minimum supported client</span></span><br/> | <span data-ttu-id="4d5f1-127">Windows 2000 Professional, только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="4d5f1-127">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="4d5f1-128">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="4d5f1-128">Minimum supported server</span></span><br/> | <span data-ttu-id="4d5f1-129">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="4d5f1-129">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="4d5f1-130">DLL</span><span class="sxs-lookup"><span data-stu-id="4d5f1-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4d5f1-131"><dt>Wiascr.dll (версия 4,90 или более поздняя)</dt></span><span class="sxs-lookup"><span data-stu-id="4d5f1-131"><dt>Wiascr.dll (version 4.90 or later)</dt></span></span> </dl> |



 

 




