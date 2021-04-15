---
title: Media.name
description: Свойство Name указывает или получает имя элемента мультимедиа.
ms.assetid: 68aba78a-86fd-4411-9ac4-58f38d915e2c
keywords:
- Media.name Windows Media Player
topic_type:
- apiref
api_name:
- Media.name
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9de8095d88c3ddec9049e0b43461adcf5553ec74
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105695150"
---
# <a name="medianame"></a><span data-ttu-id="3aa9e-104">Media.name</span><span class="sxs-lookup"><span data-stu-id="3aa9e-104">Media.name</span></span>

<span data-ttu-id="3aa9e-105">Свойство **Name** указывает или получает имя элемента мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="3aa9e-105">The **name** property specifies or retrieves the name of the media item.</span></span>

## <a name="syntax"></a><span data-ttu-id="3aa9e-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="3aa9e-106">Syntax</span></span>

<span data-ttu-id="3aa9e-107">*проигрыватель*. *куррентмедиа*. **имя**</span><span class="sxs-lookup"><span data-stu-id="3aa9e-107">*player*.*currentMedia*.**name**</span></span>

## <a name="possible-values"></a><span data-ttu-id="3aa9e-108">Возможные значения</span><span class="sxs-lookup"><span data-stu-id="3aa9e-108">Possible Values</span></span>

<span data-ttu-id="3aa9e-109">Это свойство является **строкой** для чтения и записи, содержащей имя элемента мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="3aa9e-109">This property is a read/write **String** containing the name of the media item.</span></span>

## <a name="remarks"></a><span data-ttu-id="3aa9e-110">Комментарии</span><span class="sxs-lookup"><span data-stu-id="3aa9e-110">Remarks</span></span>

<span data-ttu-id="3aa9e-111">Чтобы получить значение этого свойства, требуется доступ на чтение к библиотеке.</span><span class="sxs-lookup"><span data-stu-id="3aa9e-111">To retrieve the value of this property, read access to the library is required.</span></span> <span data-ttu-id="3aa9e-112">Чтобы указать значение этого свойства, требуется полный доступ к библиотеке.</span><span class="sxs-lookup"><span data-stu-id="3aa9e-112">To specify the value of this property, full access to the library is required.</span></span> <span data-ttu-id="3aa9e-113">Дополнительные сведения см. в разделе [доступ к библиотеке](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="3aa9e-113">For more information, see [Library Access](library-access.md).</span></span>

<span data-ttu-id="3aa9e-114">Перед использованием этого метода для указания имени элемента мультимедиа используйте **исреадонлитем** , чтобы определить, можно ли задать имя.</span><span class="sxs-lookup"><span data-stu-id="3aa9e-114">Before using this method to specify the name of a media item, use **isReadOnlyItem** to determine whether the name can be set.</span></span>

<span data-ttu-id="3aa9e-115">**Проигрыватель Windows Media 10 Mobile:** Это свойство доступно только для чтения.</span><span class="sxs-lookup"><span data-stu-id="3aa9e-115">**Windows Media Player 10 Mobile:** This property is read-only.</span></span>

## <a name="examples"></a><span data-ttu-id="3aa9e-116">Примеры</span><span class="sxs-lookup"><span data-stu-id="3aa9e-116">Examples</span></span>

<span data-ttu-id="3aa9e-117">В следующем примере JScript используется *носитель*. **имя** для изменения имени текущего элемента мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="3aa9e-117">The following JScript example uses *Media*.**name** to change the name of the current media item.</span></span> <span data-ttu-id="3aa9e-118">HTML-элемент ввода текста с именем Наметекст позволяет пользователю ввести текстовую строку для нового имени.</span><span class="sxs-lookup"><span data-stu-id="3aa9e-118">An HTML TEXT input element named NameText allows the user to enter a text string for the new name.</span></span> <span data-ttu-id="3aa9e-119">Объект **Player** создан с идентификатором "Player".</span><span class="sxs-lookup"><span data-stu-id="3aa9e-119">The **Player** object was created with ID = "Player".</span></span>


```JScript
<!<entity type="mdash"/>-Create an HTML BUTTON element to execute the name change. -->
<INPUT type = "BUTTON"  id = "NewName"  name = "NewName"  value = "Change Name" 
    onClick = "

        /* Store the current media item. */
        var cm = Player.currentMedia;

        /* Change the name. */
        cm.name = NameText.value;
">

```



## <a name="requirements"></a><span data-ttu-id="3aa9e-120">Требования</span><span class="sxs-lookup"><span data-stu-id="3aa9e-120">Requirements</span></span>



| <span data-ttu-id="3aa9e-121">Требование</span><span class="sxs-lookup"><span data-stu-id="3aa9e-121">Requirement</span></span> | <span data-ttu-id="3aa9e-122">Значение</span><span class="sxs-lookup"><span data-stu-id="3aa9e-122">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="3aa9e-123">Версия</span><span class="sxs-lookup"><span data-stu-id="3aa9e-123">Version</span></span><br/> | <span data-ttu-id="3aa9e-124">Проигрыватель Windows Media версии 7,0 или более поздней.</span><span class="sxs-lookup"><span data-stu-id="3aa9e-124">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="3aa9e-125">DLL</span><span class="sxs-lookup"><span data-stu-id="3aa9e-125">DLL</span></span><br/>     | <dl> <span data-ttu-id="3aa9e-126"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3aa9e-126"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3aa9e-127">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="3aa9e-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3aa9e-128">**Объект мультимедиа**</span><span class="sxs-lookup"><span data-stu-id="3aa9e-128">**Media Object**</span></span>](media-object.md)
</dt> <dt>

[<span data-ttu-id="3aa9e-129">**Settings. Медиаакцессригхтс**</span><span class="sxs-lookup"><span data-stu-id="3aa9e-129">**Settings.mediaAccessRights**</span></span>](settings-mediaaccessrights.md)
</dt> <dt>

[<span data-ttu-id="3aa9e-130">**Settings. Рекуестмедиаакцессригхтс**</span><span class="sxs-lookup"><span data-stu-id="3aa9e-130">**Settings.requestMediaAccessRights**</span></span>](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





