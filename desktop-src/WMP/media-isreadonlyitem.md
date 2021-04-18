---
title: Метод Media. Исреадонлитем
description: Метод Исреадонлитем возвращает значение, указывающее, можно ли изменять указанный атрибут элемента мультимедиа.
ms.assetid: 5e398e76-f64a-45b5-9b4f-679c65e5a0d1
keywords:
- Исреадонлитем метод Windows Media Player
- Исреадонлитем метод Windows Media Player, класс мультимедиа
- Класс мультимедиа проигрыватель Windows Media Player, метод Исреадонлитем
topic_type:
- apiref
api_name:
- Media.isReadOnlyItem
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f0ac5bb8d445c3ba6418be4ee5c0c5e7a96f507d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105694376"
---
# <a name="mediaisreadonlyitem-method"></a><span data-ttu-id="d4b2f-106">Метод Media. Исреадонлитем</span><span class="sxs-lookup"><span data-stu-id="d4b2f-106">Media.isReadOnlyItem method</span></span>

<span data-ttu-id="d4b2f-107">Метод **исреадонлитем** возвращает значение, указывающее, можно ли изменять указанный атрибут элемента мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="d4b2f-107">The **isReadOnlyItem** method returns a value indicating whether the specified attribute of the media item can be edited.</span></span>

## <a name="syntax"></a><span data-ttu-id="d4b2f-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="d4b2f-108">Syntax</span></span>


```JScript
bRetVal = Media.isReadOnlyItem(
  attribute
)
```



## <a name="parameters"></a><span data-ttu-id="d4b2f-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="d4b2f-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d4b2f-110">*атрибут* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="d4b2f-110">*attribute* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d4b2f-111">**Строка** , указывающая имя атрибута для проверки.</span><span class="sxs-lookup"><span data-stu-id="d4b2f-111">**String** indicating the name of the attribute to test.</span></span> <span data-ttu-id="d4b2f-112">Сведения об атрибутах, поддерживаемых проигрывателем Windows Media, см. в [справочнике по атрибутам](attribute-reference.md)проигрывателя Windows Media.</span><span class="sxs-lookup"><span data-stu-id="d4b2f-112">For information about the attributes supported by Windows Media Player, see the Windows Media Player [Attribute Reference](attribute-reference.md)..</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d4b2f-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="d4b2f-113">Return value</span></span>

<span data-ttu-id="d4b2f-114">Этот метод возвращает **логическое значение**.</span><span class="sxs-lookup"><span data-stu-id="d4b2f-114">This method returns a **Boolean**.</span></span>

## <a name="remarks"></a><span data-ttu-id="d4b2f-115">Комментарии</span><span class="sxs-lookup"><span data-stu-id="d4b2f-115">Remarks</span></span>

<span data-ttu-id="d4b2f-116">Если атрибут доступен только для чтения, то он не может быть задан с помощью метода **сетитеминфо** .</span><span class="sxs-lookup"><span data-stu-id="d4b2f-116">If an attribute is read-only, then it cannot be set with the **setItemInfo** method.</span></span> <span data-ttu-id="d4b2f-117">Обратите внимание, что этот метод может возвращать различные значения для определенного атрибута при использовании с разными версиями проигрывателя Windows Media.</span><span class="sxs-lookup"><span data-stu-id="d4b2f-117">Note that this method may return different values for a particular attribute when used with different versions of Windows Media Player.</span></span>

<span data-ttu-id="d4b2f-118">Чтобы использовать этот метод, требуется доступ на чтение к библиотеке.</span><span class="sxs-lookup"><span data-stu-id="d4b2f-118">To use this method, read access to the library is required.</span></span> <span data-ttu-id="d4b2f-119">Дополнительные сведения см. в разделе [доступ к библиотеке](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="d4b2f-119">For more information, see [Library Access](library-access.md).</span></span>

<span data-ttu-id="d4b2f-120">**Проигрыватель Windows Media 10 Mobile:** Это свойство всегда возвращает **значение true**.</span><span class="sxs-lookup"><span data-stu-id="d4b2f-120">**Windows Media Player 10 Mobile:** This property always returns **true**.</span></span>

## <a name="examples"></a><span data-ttu-id="d4b2f-121">Примеры</span><span class="sxs-lookup"><span data-stu-id="d4b2f-121">Examples</span></span>

<span data-ttu-id="d4b2f-122">В следующем примере JScript используется *носитель*. **исреадонлитем** для заполнения HTML-элемента textarea с именем рвтекст сведениями о текущем элементе мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="d4b2f-122">The following JScript example uses *Media*.**isReadOnlyItem** to fill an HTML TEXTAREA element named rwText with information about the current media item.</span></span> <span data-ttu-id="d4b2f-123">Код выводит каждый атрибут текущего элемента мультимедиа вместе с текстом, указывающим, доступен ли атрибут только для чтения или для чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="d4b2f-123">The code outputs each attribute of the current media item, along with text indicating whether the attribute is read-only or read/write.</span></span> <span data-ttu-id="d4b2f-124">Объект **Player** создан с идентификатором "Player".</span><span class="sxs-lookup"><span data-stu-id="d4b2f-124">The **Player** object was created with ID = "Player".</span></span>


```JScript
// Store the current media item object.
var cm = Player.currentMedia;

// Create a variable to hold each attribute name.
var atName;

// Loop through the attribute list.
for(var i = 0; i < cm.attributeCount; i++){

   // Get the attribute name.
   atName = cm.getAttributeName(i);

   // Test whether the attribute is read-only.
   var test = ((cm.isReadOnlyItem(atName))?"Read-Only":"Read/Write");

// Print the attribute information to the text area.
   rwText.value += atName + " is " + test;
   rwText.value += "\n";
}

```



## <a name="requirements"></a><span data-ttu-id="d4b2f-125">Требования</span><span class="sxs-lookup"><span data-stu-id="d4b2f-125">Requirements</span></span>



| <span data-ttu-id="d4b2f-126">Требование</span><span class="sxs-lookup"><span data-stu-id="d4b2f-126">Requirement</span></span> | <span data-ttu-id="d4b2f-127">Значение</span><span class="sxs-lookup"><span data-stu-id="d4b2f-127">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="d4b2f-128">Версия</span><span class="sxs-lookup"><span data-stu-id="d4b2f-128">Version</span></span><br/> | <span data-ttu-id="d4b2f-129">Проигрыватель Windows Media версии 7,0 или более поздней.</span><span class="sxs-lookup"><span data-stu-id="d4b2f-129">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="d4b2f-130">DLL</span><span class="sxs-lookup"><span data-stu-id="d4b2f-130">DLL</span></span><br/>     | <dl> <span data-ttu-id="d4b2f-131"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d4b2f-131"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d4b2f-132">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="d4b2f-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d4b2f-133">**Объект мультимедиа**</span><span class="sxs-lookup"><span data-stu-id="d4b2f-133">**Media Object**</span></span>](media-object.md)
</dt> <dt>

[<span data-ttu-id="d4b2f-134">**Media. Сетитеминфо**</span><span class="sxs-lookup"><span data-stu-id="d4b2f-134">**Media.setItemInfo**</span></span>](media-setiteminfo.md)
</dt> <dt>

[<span data-ttu-id="d4b2f-135">**Settings. Медиаакцессригхтс**</span><span class="sxs-lookup"><span data-stu-id="d4b2f-135">**Settings.mediaAccessRights**</span></span>](settings-mediaaccessrights.md)
</dt> <dt>

[<span data-ttu-id="d4b2f-136">**Settings. Рекуестмедиаакцессригхтс**</span><span class="sxs-lookup"><span data-stu-id="d4b2f-136">**Settings.requestMediaAccessRights**</span></span>](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





