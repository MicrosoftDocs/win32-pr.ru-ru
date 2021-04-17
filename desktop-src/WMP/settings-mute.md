---
title: Параметры. выкл.
description: Свойство выкл. указывает и получает значение, указывающее, отключено ли звуковое сопровождение.
ms.assetid: d6d4b46d-5631-4af7-bd99-21674f067121
keywords:
- Параметры. выключение проигрывателя Windows Media
topic_type:
- apiref
api_name:
- Settings.mute
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7061439e9e091b2ad1cf6be49873d7e3895132b0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105704381"
---
# <a name="settingsmute"></a><span data-ttu-id="22792-104">Параметры. выкл.</span><span class="sxs-lookup"><span data-stu-id="22792-104">Settings.mute</span></span>

<span data-ttu-id="22792-105">Свойство **выкл** . указывает и получает значение, указывающее, отключено ли звуковое сопровождение.</span><span class="sxs-lookup"><span data-stu-id="22792-105">The **mute** property specifies and retrieves a value indicating whether audio is muted.</span></span>

## <a name="syntax"></a><span data-ttu-id="22792-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="22792-106">Syntax</span></span>

<span data-ttu-id="22792-107">Player. Settings. выкл.</span><span class="sxs-lookup"><span data-stu-id="22792-107">player.settings.mute</span></span>

## <a name="possible-values"></a><span data-ttu-id="22792-108">Возможные значения</span><span class="sxs-lookup"><span data-stu-id="22792-108">Possible Values</span></span>

<span data-ttu-id="22792-109">Это свойство является **логическим значением** для чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="22792-109">This property is a read/write **Boolean**.</span></span>



| <span data-ttu-id="22792-110">Значение</span><span class="sxs-lookup"><span data-stu-id="22792-110">Value</span></span> | <span data-ttu-id="22792-111">Описание</span><span class="sxs-lookup"><span data-stu-id="22792-111">Description</span></span>                  |
|-------|------------------------------|
| <span data-ttu-id="22792-112">true</span><span class="sxs-lookup"><span data-stu-id="22792-112">true</span></span>  | <span data-ttu-id="22792-113">Звук отключен.</span><span class="sxs-lookup"><span data-stu-id="22792-113">Audio is muted.</span></span>              |
| <span data-ttu-id="22792-114">false</span><span class="sxs-lookup"><span data-stu-id="22792-114">false</span></span> | <span data-ttu-id="22792-115">По умолчанию.</span><span class="sxs-lookup"><span data-stu-id="22792-115">Default.</span></span> <span data-ttu-id="22792-116">Звук не отключен.</span><span class="sxs-lookup"><span data-stu-id="22792-116">Audio is not muted.</span></span> |



 

## <a name="examples"></a><span data-ttu-id="22792-117">Примеры</span><span class="sxs-lookup"><span data-stu-id="22792-117">Examples</span></span>

<span data-ttu-id="22792-118">В следующем примере создается элемент CHECKBOX HTML, позволяющий пользователю отключить звук и снять с него микрофон.</span><span class="sxs-lookup"><span data-stu-id="22792-118">The following example creates an HTML CHECKBOX element that allows the user to mute and un-mute audio.</span></span> <span data-ttu-id="22792-119">Объект **Player** создан с идентификатором "Player".</span><span class="sxs-lookup"><span data-stu-id="22792-119">The **Player** object was created with ID = "Player".</span></span>


```
<!-- Create an HTML CHECKBOX control. -->
<INPUT  TYPE = "CHECKBOX"  ID = MUTE  
             onClick = "
                        /* Use the CHECKBOX state to set 
                           the mute property. */
                        Player.settings.mute = MUTE.checked;
">
```



## <a name="requirements"></a><span data-ttu-id="22792-120">Требования</span><span class="sxs-lookup"><span data-stu-id="22792-120">Requirements</span></span>



| <span data-ttu-id="22792-121">Требование</span><span class="sxs-lookup"><span data-stu-id="22792-121">Requirement</span></span> | <span data-ttu-id="22792-122">Значение</span><span class="sxs-lookup"><span data-stu-id="22792-122">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="22792-123">Версия</span><span class="sxs-lookup"><span data-stu-id="22792-123">Version</span></span><br/> | <span data-ttu-id="22792-124">Проигрыватель Windows Media версии 7,0 или более поздней.</span><span class="sxs-lookup"><span data-stu-id="22792-124">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="22792-125">DLL</span><span class="sxs-lookup"><span data-stu-id="22792-125">DLL</span></span><br/>     | <dl> <span data-ttu-id="22792-126"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="22792-126"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="22792-127">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="22792-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="22792-128">**Объект параметров**</span><span class="sxs-lookup"><span data-stu-id="22792-128">**Settings Object**</span></span>](settings-object.md)
</dt> </dl>

 

 





