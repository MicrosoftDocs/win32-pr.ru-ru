---
description: Метод Жетитемсфромуи объекта Item отображает диалоговое окно, позволяющее пользователю выбирать изображения и звук для передачи с устройства.
ms.assetid: 0ee9a248-20ed-4e1f-a8ce-615c4a6a2bce
title: Item. Жетитемсфромуи, метод
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Item.GetItemsFromUI
api_type:
- COM
api_location:
- Wiascr.dll
ms.openlocfilehash: 25bb24fd2b4c6b8d3d7f8cc08c23a42257399a14
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104154866"
---
# <a name="itemgetitemsfromui-method"></a><span data-ttu-id="69bf0-103">Item. Жетитемсфромуи, метод</span><span class="sxs-lookup"><span data-stu-id="69bf0-103">Item.GetItemsFromUI method</span></span>

<span data-ttu-id="69bf0-104">Метод **жетитемсфромуи** объекта [**Item**](-wia-item.md) отображает диалоговое окно, позволяющее пользователю выбирать изображения и звук для передачи с устройства.</span><span class="sxs-lookup"><span data-stu-id="69bf0-104">The **GetItemsFromUI** method of the [**Item**](-wia-item.md) object displays a dialog box that allows a user to select images and audio to transfer from a device.</span></span>

## <a name="syntax"></a><span data-ttu-id="69bf0-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="69bf0-105">Syntax</span></span>


```JScript
retVal = Item.GetItemsFromUI(
  Flags = 0,
  Intent = 0
)
```



## <a name="parameters"></a><span data-ttu-id="69bf0-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="69bf0-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="69bf0-107">*Флаги* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="69bf0-107">*Flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="69bf0-108">Тип: **[ **виафлаг**](-wia-wiaflag.md)**</span><span class="sxs-lookup"><span data-stu-id="69bf0-108">Type: **[**WiaFlag**](-wia-wiaflag.md)**</span></span>

<dt>



 <span data-ttu-id="69bf0-109"> (0)</span><span class="sxs-lookup"><span data-stu-id="69bf0-109">(0)</span></span>


</dt> <dd>

<span data-ttu-id="69bf0-110">По умолчанию.</span><span class="sxs-lookup"><span data-stu-id="69bf0-110">Default.</span></span> <span data-ttu-id="69bf0-111">\[в \] задает поведение диалогового окна.</span><span class="sxs-lookup"><span data-stu-id="69bf0-111">\[in\] Specifies dialog box behavior.</span></span> <span data-ttu-id="69bf0-112">Допустимые значения для этого параметра совпадают с параметрами параметра *лфлагс* метода [**девицедлг**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiaitem-devicedlg) .</span><span class="sxs-lookup"><span data-stu-id="69bf0-112">The valid values for this parameter are the same as for the *lFlags* parameter of the [**DeviceDlg**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiaitem-devicedlg) method.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="69bf0-113">*Намерение* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="69bf0-113">*Intent* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="69bf0-114">Тип: **виаинтент**</span><span class="sxs-lookup"><span data-stu-id="69bf0-114">Type: **WiaIntent**</span></span>

<dt>



 <span data-ttu-id="69bf0-115"> (0)</span><span class="sxs-lookup"><span data-stu-id="69bf0-115">(0)</span></span>


</dt> <dd>

<span data-ttu-id="69bf0-116">По умолчанию.</span><span class="sxs-lookup"><span data-stu-id="69bf0-116">Default.</span></span> <span data-ttu-id="69bf0-117">\[в \] указывает, какой тип данных должен представлять изображение.</span><span class="sxs-lookup"><span data-stu-id="69bf0-117">\[in\] Specifies what type of data the image is intended to represent.</span></span> <span data-ttu-id="69bf0-118">Список значений намерения образа см. в разделе [**константы намерения изображения**](-wia-imageintentconstants.md).</span><span class="sxs-lookup"><span data-stu-id="69bf0-118">For a list of image intent values, see [**Image Intent Constants**](-wia-imageintentconstants.md).</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="69bf0-119">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="69bf0-119">Return value</span></span>

<span data-ttu-id="69bf0-120">Тип: **ICollection**</span><span class="sxs-lookup"><span data-stu-id="69bf0-120">Type: **ICollection**</span></span>

<span data-ttu-id="69bf0-121">Этот метод возвращает коллекцию объектов [**Item**](-wia-item.md) , представляющих элементы, выбранные пользователем.</span><span class="sxs-lookup"><span data-stu-id="69bf0-121">This method returns a collection of [**Item**](-wia-item.md) objects that represent the items selected by the user.</span></span> <span data-ttu-id="69bf0-122">Если элементы не выбраны, коллекция будет пустой.</span><span class="sxs-lookup"><span data-stu-id="69bf0-122">If no items are selected, the collection is empty.</span></span>

## <a name="remarks"></a><span data-ttu-id="69bf0-123">Комментарии</span><span class="sxs-lookup"><span data-stu-id="69bf0-123">Remarks</span></span>

<span data-ttu-id="69bf0-124">Для приложений Microsoft Visual Basic добавьте ссылку на "Библиотека типов приобретения образа Windows 1,01".</span><span class="sxs-lookup"><span data-stu-id="69bf0-124">For Microsoft Visual Basic applications, add a reference to "Windows Image Acquisition 1.01 Type Library".</span></span>

<span data-ttu-id="69bf0-125">Этот метод применяется только к устройствам (корневым элементам).</span><span class="sxs-lookup"><span data-stu-id="69bf0-125">This method applies only to devices (root items).</span></span> <span data-ttu-id="69bf0-126">Метод возвращает коллекцию объектов [**Item**](-wia-item.md) , представляющих изображения или аудиоклипы, выбранные пользователем.</span><span class="sxs-lookup"><span data-stu-id="69bf0-126">The method returns a collection of [**Item**](-wia-item.md) objects that represent the images or audio clips selected by the user.</span></span>

<span data-ttu-id="69bf0-127">Если пользователь не выбрал ни одного элемента, метод возвращает пустую коллекцию.</span><span class="sxs-lookup"><span data-stu-id="69bf0-127">If no items are selected by the user, the method returns an empty collection.</span></span>

## <a name="examples"></a><span data-ttu-id="69bf0-128">Примеры</span><span class="sxs-lookup"><span data-stu-id="69bf0-128">Examples</span></span>

<span data-ttu-id="69bf0-129">В следующем примере показано использование метода **жетитемсфромуи** , позволяющего пользователю выбирать изображения из диалогового окна.</span><span class="sxs-lookup"><span data-stu-id="69bf0-129">The following example demonstrates the use of the **GetItemsFromUI** method to allow a user to select images from a dialog box.</span></span>


```JScript
<SCRIPT LANGUAGE="VBScript">
Dim objWia
Dim objDeviceInfoCollection
Dim objDeviceInfo
Dim objRootItem
Dim objSelectedItems
 
Set objWIA = CreateObject("Wia.Script")
 
Set objDeviceInfoCollection = objWia.Devices
 
For Each objDeviceInfo In objDeviceInfoCollection
    Set objRootItem = objWia.Create(objDeviceInfo)
    Set objSelectedItems = objRootItem.GetItemsFromUI(0, 0)
    ' Do something with selected items.
Next
</SCRIPT>
```



## <a name="requirements"></a><span data-ttu-id="69bf0-130">Требования</span><span class="sxs-lookup"><span data-stu-id="69bf0-130">Requirements</span></span>



| <span data-ttu-id="69bf0-131">Требование</span><span class="sxs-lookup"><span data-stu-id="69bf0-131">Requirement</span></span> | <span data-ttu-id="69bf0-132">Значение</span><span class="sxs-lookup"><span data-stu-id="69bf0-132">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="69bf0-133">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="69bf0-133">Minimum supported client</span></span><br/> | <span data-ttu-id="69bf0-134">Windows 2000 Professional, только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="69bf0-134">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="69bf0-135">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="69bf0-135">Minimum supported server</span></span><br/> | <span data-ttu-id="69bf0-136">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="69bf0-136">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="69bf0-137">DLL</span><span class="sxs-lookup"><span data-stu-id="69bf0-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="69bf0-138"><dt>Wiascr.dll (версия 4,90 или более поздняя)</dt></span><span class="sxs-lookup"><span data-stu-id="69bf0-138"><dt>Wiascr.dll (version 4.90 or later)</dt></span></span> </dl> |



 

 




