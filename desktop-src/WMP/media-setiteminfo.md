---
title: Метод Media. Сетитеминфо
description: Метод Сетитеминфо задает значение указанного атрибута для текущего элемента мультимедиа.
ms.assetid: 8c4ce954-45cb-4a67-9660-1a013ecd64c3
keywords:
- Сетитеминфо метод Windows Media Player
- Сетитеминфо метод Windows Media Player, класс мультимедиа
- Класс мультимедиа проигрыватель Windows Media Player, метод Сетитеминфо
topic_type:
- apiref
api_name:
- Media.setItemInfo
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b918e6a388cab750cc379611f5f55c6a1b1d256c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105698817"
---
# <a name="mediasetiteminfo-method"></a><span data-ttu-id="f9a9d-106">Метод Media. Сетитеминфо</span><span class="sxs-lookup"><span data-stu-id="f9a9d-106">Media.setItemInfo method</span></span>

<span data-ttu-id="f9a9d-107">Метод **сетитеминфо** задает значение указанного атрибута для текущего элемента мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="f9a9d-107">The **setItemInfo** method sets the value of the specified attribute for the current media item.</span></span>

## <a name="syntax"></a><span data-ttu-id="f9a9d-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="f9a9d-108">Syntax</span></span>


```JScript
Media.setItemInfo(
  attribute,
  value
)
```



## <a name="parameters"></a><span data-ttu-id="f9a9d-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="f9a9d-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f9a9d-110">*атрибут* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="f9a9d-110">*attribute* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f9a9d-111">**Строка** , содержащая имя атрибута.</span><span class="sxs-lookup"><span data-stu-id="f9a9d-111">**String** containing the attribute name.</span></span> <span data-ttu-id="f9a9d-112">Сведения об атрибутах, поддерживаемых проигрывателем Windows Media, см. в [справочнике по атрибутам](attribute-reference.md)проигрывателя Windows Media.</span><span class="sxs-lookup"><span data-stu-id="f9a9d-112">For information about the attributes supported by Windows Media Player, see the Windows Media Player [Attribute Reference](attribute-reference.md).</span></span>

</dd> <dt>

<span data-ttu-id="f9a9d-113">*значение* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="f9a9d-113">*value* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f9a9d-114">**Строка** , содержащая новое значение.</span><span class="sxs-lookup"><span data-stu-id="f9a9d-114">**String** containing the new value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f9a9d-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="f9a9d-115">Return value</span></span>

<span data-ttu-id="f9a9d-116">Этот метод не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="f9a9d-116">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="f9a9d-117">Комментарии</span><span class="sxs-lookup"><span data-stu-id="f9a9d-117">Remarks</span></span>

<span data-ttu-id="f9a9d-118">Свойство **аттрибутекаунт** содержит количество атрибутов, доступных для данного объекта **мультимедиа** .</span><span class="sxs-lookup"><span data-stu-id="f9a9d-118">The **attributeCount** property contains the number of attributes available for a given **Media** object.</span></span> <span data-ttu-id="f9a9d-119">Номера индексов можно использовать с методом **жетаттрибутенаме** для определения имен встроенных атрибутов, которые могут использоваться с этим методом.</span><span class="sxs-lookup"><span data-stu-id="f9a9d-119">Index numbers can then be used with the **getAttributeName** method to determine the names of the built-in attributes that can be used with this method.</span></span>

<span data-ttu-id="f9a9d-120">Перед использованием этого метода используйте метод **исреадонлитем** , чтобы определить, можно ли задать определенный атрибут.</span><span class="sxs-lookup"><span data-stu-id="f9a9d-120">Before using this method, use the **isReadOnlyItem** method to determine whether a particular attribute can be set.</span></span>

<span data-ttu-id="f9a9d-121">Чтобы использовать этот метод, требуется полный доступ к библиотеке.</span><span class="sxs-lookup"><span data-stu-id="f9a9d-121">To use this method, full access to the library is required.</span></span> <span data-ttu-id="f9a9d-122">Дополнительные сведения см. в разделе [доступ к библиотеке](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="f9a9d-122">For more information, see [Library Access](library-access.md).</span></span>

<span data-ttu-id="f9a9d-123">**Примечание**</span><span class="sxs-lookup"><span data-stu-id="f9a9d-123">**Note**</span></span>

<span data-ttu-id="f9a9d-124">При внедрении элемента управления проигрывателя Windows Media в приложение измененные атрибуты файла не будут записываться в файл мультимедиа до тех пор, пока пользователь не запустит проигрыватель Windows Media.</span><span class="sxs-lookup"><span data-stu-id="f9a9d-124">If you embed the Windows Media Player control in your application, file attributes that you change will not be written to the digital media file until the user runs Windows Media Player.</span></span> <span data-ttu-id="f9a9d-125">При использовании элемента управления в удаленном приложении, написанном на языке C++, измененные атрибуты файла будут записаны в файл мультимедиа вскоре после внесения изменений.</span><span class="sxs-lookup"><span data-stu-id="f9a9d-125">If you use the control in a remoted application written in C++, file attributes that you change will be written to the digital media file shortly after you make the changes.</span></span> <span data-ttu-id="f9a9d-126">В любом случае изменения сразу же становятся доступными для кода через библиотеку.</span><span class="sxs-lookup"><span data-stu-id="f9a9d-126">In either case, the changes are immediately available to your code through the library.</span></span>

<span data-ttu-id="f9a9d-127">**Проигрыватель Windows Media 10 Mobile:** Этот метод не реализован.</span><span class="sxs-lookup"><span data-stu-id="f9a9d-127">**Windows Media Player 10 Mobile:** This method is not implemented.</span></span>

## <a name="examples"></a><span data-ttu-id="f9a9d-128">Примеры</span><span class="sxs-lookup"><span data-stu-id="f9a9d-128">Examples</span></span>

<span data-ttu-id="f9a9d-129">В следующем примере JScript используется *носитель*. **сетитеминфо** , чтобы изменить значение атрибута жанра для текущего элемента мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="f9a9d-129">The following JScript example uses *Media*.**setItemInfo** to change the value of the Genre attribute for the current media item.</span></span> <span data-ttu-id="f9a9d-130">HTML-элемент ввода текста с именем genText позволяет пользователю ввести текстовую строку, которая затем будет использоваться для изменения сведений об атрибуте.</span><span class="sxs-lookup"><span data-stu-id="f9a9d-130">An HTML TEXT input element named genText allows the user to enter a text string, which is then used to change the attribute information.</span></span> <span data-ttu-id="f9a9d-131">Объект **Player** создан с идентификатором "Player".</span><span class="sxs-lookup"><span data-stu-id="f9a9d-131">The **Player** object was created with ID = "Player".</span></span>


```JScript
<!-- Create the button element. -->
<INPUT type = "BUTTON"  id = "NEWGEN"  name = "NEWGEN"  value = "Change Genre" 
onClick = "
    /* Store the current media item. */
    var cm = Player.currentMedia;

    /* Get the user input from the text box. */
    var atValue = genText.value;

    /* Test for read-only status of the attribute. */
    if(cm.isReadOnlyItem('Genre') == false){

        /* Change the attribute value. */
        cm.setItemInfo('Genre' ,atValue);
    } 
">

```



## <a name="requirements"></a><span data-ttu-id="f9a9d-132">Требования</span><span class="sxs-lookup"><span data-stu-id="f9a9d-132">Requirements</span></span>



| <span data-ttu-id="f9a9d-133">Требование</span><span class="sxs-lookup"><span data-stu-id="f9a9d-133">Requirement</span></span> | <span data-ttu-id="f9a9d-134">Значение</span><span class="sxs-lookup"><span data-stu-id="f9a9d-134">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="f9a9d-135">Версия</span><span class="sxs-lookup"><span data-stu-id="f9a9d-135">Version</span></span><br/> | <span data-ttu-id="f9a9d-136">Проигрыватель Windows Media версии 7,0 или более поздней.</span><span class="sxs-lookup"><span data-stu-id="f9a9d-136">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="f9a9d-137">DLL</span><span class="sxs-lookup"><span data-stu-id="f9a9d-137">DLL</span></span><br/>     | <dl> <span data-ttu-id="f9a9d-138"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f9a9d-138"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f9a9d-139">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="f9a9d-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f9a9d-140">**Объект мультимедиа**</span><span class="sxs-lookup"><span data-stu-id="f9a9d-140">**Media Object**</span></span>](media-object.md)
</dt> <dt>

[<span data-ttu-id="f9a9d-141">**Media. getItemInfo**</span><span class="sxs-lookup"><span data-stu-id="f9a9d-141">**Media.getItemInfo**</span></span>](media-getiteminfo.md)
</dt> <dt>

[<span data-ttu-id="f9a9d-142">**Media. Исреадонлитем**</span><span class="sxs-lookup"><span data-stu-id="f9a9d-142">**Media.isReadOnlyItem**</span></span>](media-isreadonlyitem.md)
</dt> <dt>

[<span data-ttu-id="f9a9d-143">**Settings. Медиаакцессригхтс**</span><span class="sxs-lookup"><span data-stu-id="f9a9d-143">**Settings.mediaAccessRights**</span></span>](settings-mediaaccessrights.md)
</dt> <dt>

[<span data-ttu-id="f9a9d-144">**Settings. Рекуестмедиаакцессригхтс**</span><span class="sxs-lookup"><span data-stu-id="f9a9d-144">**Settings.requestMediaAccessRights**</span></span>](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





