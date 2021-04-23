---
title: CDROM. ДривеспеЦифиер
description: Свойство ДривеспеЦифиер извлекает букву CD или DVD-дисковода.
ms.assetid: f592819e-61ba-4ae1-b748-b6f29df88067
keywords:
- Проигрыватель Windows Media CDROM. ДривеспеЦифиер
topic_type:
- apiref
api_name:
- Cdrom.driveSpecifier
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1fef04f56de87bb6aeb4843e5aedb6e5ed74418a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104533908"
---
# <a name="cdromdrivespecifier"></a><span data-ttu-id="6015d-104">CDROM. ДривеспеЦифиер</span><span class="sxs-lookup"><span data-stu-id="6015d-104">Cdrom.driveSpecifier</span></span>

<span data-ttu-id="6015d-105">Свойство **дривеспеЦифиер** извлекает букву CD или DVD-дисковода.</span><span class="sxs-lookup"><span data-stu-id="6015d-105">The **driveSpecifier** property retrieves the CD or DVD drive letter.</span></span>

``` syntax
player.cdromCollection.item(
        index
        ).driveSpecifier
      
```

## <a name="possible-values"></a><span data-ttu-id="6015d-106">Возможные значения</span><span class="sxs-lookup"><span data-stu-id="6015d-106">Possible Values</span></span>

<span data-ttu-id="6015d-107">Это свойство является **строкой**, доступная только для чтения.</span><span class="sxs-lookup"><span data-stu-id="6015d-107">This property is a read-only **String**.</span></span>

## <a name="remarks"></a><span data-ttu-id="6015d-108">Комментарии</span><span class="sxs-lookup"><span data-stu-id="6015d-108">Remarks</span></span>

<span data-ttu-id="6015d-109">Обычно дисководы DVD могут воспроизводить компакт-диски, но дисководы компакт-дисков не могут воспроизводить DVD-носители.</span><span class="sxs-lookup"><span data-stu-id="6015d-109">Typically, DVD drives can play CD media, but CD drives cannot play DVD media.</span></span> <span data-ttu-id="6015d-110">Это свойство получает описатель диска для индекса диска, начинающегося с нуля, в диапазоне, полученном с помощью *кдромколлектион*. **количество**.</span><span class="sxs-lookup"><span data-stu-id="6015d-110">This property retrieves a drive specifier for a zero-based drive index within the range retrieved using *CdromCollection*.**count**.</span></span> <span data-ttu-id="6015d-111">Полученное значение имеет вид *x*:, где *X* представляет букву диска.</span><span class="sxs-lookup"><span data-stu-id="6015d-111">The value retrieved takes the form *X*:, where *X* represents the drive letter.</span></span>

<span data-ttu-id="6015d-112">Чтобы получить значение этого свойства, требуется доступ на чтение к библиотеке.</span><span class="sxs-lookup"><span data-stu-id="6015d-112">To retrieve the value of this property, read access to the library is required.</span></span> <span data-ttu-id="6015d-113">Дополнительные сведения см. в разделе [доступ к библиотеке](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="6015d-113">For more information, see [Library Access](library-access.md).</span></span>

<span data-ttu-id="6015d-114">**Проигрыватель Windows Media 10 Mobile:** Это свойство не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="6015d-114">**Windows Media Player 10 Mobile:** This property is not supported.</span></span>

## <a name="examples"></a><span data-ttu-id="6015d-115">Примеры</span><span class="sxs-lookup"><span data-stu-id="6015d-115">Examples</span></span>

<span data-ttu-id="6015d-116">В следующем примере JScript используется *CDROM*. **дривеспеЦифиер** для заполнения текстовой области HTML с именем myText с разделенным запятыми списком доступных ДИСКОВОДов компакт-и DVD-дисков.</span><span class="sxs-lookup"><span data-stu-id="6015d-116">The following JScript example uses *Cdrom*.**driveSpecifier** to fill an HTML text area named myText with a comma-separated list of available CD and DVD drives.</span></span> <span data-ttu-id="6015d-117">Объект **Player** создан с идентификатором "Player".</span><span class="sxs-lookup"><span data-stu-id="6015d-117">The **Player** object was created with ID = "Player".</span></span>


```JScript
// Allocate an array to store the drive specifiers.
var MYdriveSpecifiers = new Array();

// Loop through the available drives using CdromCollection.count.
for (var i = 0; i < Player.cdRomCollection.count; i++){

// For each available drive, add a corresponding item 
// to the MYdriveSpecifiers array. 
    MYdriveSpecifiers[i] = Player.CDRomCollection.item(i).driveSpecifier;
}

// Write the array of drive letter specifiers to the text area.
myText.value = "Drive letters found: " + MYdriveSpecifiers;
```



## <a name="requirements"></a><span data-ttu-id="6015d-118">Требования</span><span class="sxs-lookup"><span data-stu-id="6015d-118">Requirements</span></span>



| <span data-ttu-id="6015d-119">Требование</span><span class="sxs-lookup"><span data-stu-id="6015d-119">Requirement</span></span> | <span data-ttu-id="6015d-120">Значение</span><span class="sxs-lookup"><span data-stu-id="6015d-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="6015d-121">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="6015d-121">Minimum supported client</span></span><br/> | <span data-ttu-id="6015d-122">Только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="6015d-122">Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="6015d-123">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="6015d-123">Minimum supported server</span></span><br/> | <span data-ttu-id="6015d-124">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="6015d-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="6015d-125">Версия</span><span class="sxs-lookup"><span data-stu-id="6015d-125">Version</span></span><br/>                  | <span data-ttu-id="6015d-126">Проигрыватель Windows Media версии 7,0 или более поздней</span><span class="sxs-lookup"><span data-stu-id="6015d-126">Windows Media Player version 7.0 or later</span></span><br/>                               |
| <span data-ttu-id="6015d-127">DLL</span><span class="sxs-lookup"><span data-stu-id="6015d-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6015d-128"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6015d-128"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6015d-129">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="6015d-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6015d-130">**Объект CDROM**</span><span class="sxs-lookup"><span data-stu-id="6015d-130">**Cdrom Object**</span></span>](cdrom-object.md)
</dt> <dt>

[<span data-ttu-id="6015d-131">**Кдромколлектион. Count**</span><span class="sxs-lookup"><span data-stu-id="6015d-131">**CdromCollection.count**</span></span>](cdromcollection-count.md)
</dt> <dt>

[<span data-ttu-id="6015d-132">**Settings. Медиаакцессригхтс**</span><span class="sxs-lookup"><span data-stu-id="6015d-132">**Settings.mediaAccessRights**</span></span>](settings-mediaaccessrights.md)
</dt> <dt>

[<span data-ttu-id="6015d-133">**Settings. Рекуестмедиаакцессригхтс**</span><span class="sxs-lookup"><span data-stu-id="6015d-133">**Settings.requestMediaAccessRights**</span></span>](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





