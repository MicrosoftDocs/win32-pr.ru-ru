---
title: Settings. Volume
description: Свойство Volume указывает или получает текущий том.
ms.assetid: 60143eff-3a34-43eb-a86d-641c2a5cfc01
keywords:
- Проигрыватель Windows Media Settings. Volume
topic_type:
- apiref
api_name:
- Settings.volume
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e0f5ec4299bf33ed16143eec8570b65c548599e2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105651842"
---
# <a name="settingsvolume"></a><span data-ttu-id="51cc1-104">Settings. Volume</span><span class="sxs-lookup"><span data-stu-id="51cc1-104">Settings.volume</span></span>

<span data-ttu-id="51cc1-105">Свойство **Volume** указывает или получает текущий том.</span><span class="sxs-lookup"><span data-stu-id="51cc1-105">The **volume** property specifies or retrieves the current volume.</span></span>

## <a name="syntax"></a><span data-ttu-id="51cc1-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="51cc1-106">Syntax</span></span>

<span data-ttu-id="51cc1-107">проигрыватель. Settings. Volume</span><span class="sxs-lookup"><span data-stu-id="51cc1-107">player.settings.volume</span></span>

## <a name="possible-values"></a><span data-ttu-id="51cc1-108">Возможные значения</span><span class="sxs-lookup"><span data-stu-id="51cc1-108">Possible Values</span></span>

<span data-ttu-id="51cc1-109">Это свойство является **числом** для чтения и записи (**длинное**) в диапазоне от 0 до 100.</span><span class="sxs-lookup"><span data-stu-id="51cc1-109">This property is a read/write **Number** (**long**) ranging from 0 to 100.</span></span>

## <a name="remarks"></a><span data-ttu-id="51cc1-110">Комментарии</span><span class="sxs-lookup"><span data-stu-id="51cc1-110">Remarks</span></span>

<span data-ttu-id="51cc1-111">Ноль указывает на отсутствие тома и 100 указывает на полный том.</span><span class="sxs-lookup"><span data-stu-id="51cc1-111">Zero specifies no volume and 100 specifies full volume.</span></span> <span data-ttu-id="51cc1-112">Если для этого свойства не указано значение, по умолчанию используется последний параметр тома, установленный для проигрывателя.</span><span class="sxs-lookup"><span data-stu-id="51cc1-112">If no value is specified for this property, it defaults to the last volume setting established for the player.</span></span>

## <a name="requirements"></a><span data-ttu-id="51cc1-113">Требования</span><span class="sxs-lookup"><span data-stu-id="51cc1-113">Requirements</span></span>



| <span data-ttu-id="51cc1-114">Требование</span><span class="sxs-lookup"><span data-stu-id="51cc1-114">Requirement</span></span> | <span data-ttu-id="51cc1-115">Значение</span><span class="sxs-lookup"><span data-stu-id="51cc1-115">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="51cc1-116">Версия</span><span class="sxs-lookup"><span data-stu-id="51cc1-116">Version</span></span><br/> | <span data-ttu-id="51cc1-117">Проигрыватель Windows Media версии 7,0 или более поздней.</span><span class="sxs-lookup"><span data-stu-id="51cc1-117">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="51cc1-118">DLL</span><span class="sxs-lookup"><span data-stu-id="51cc1-118">DLL</span></span><br/>     | <dl> <span data-ttu-id="51cc1-119"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="51cc1-119"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="51cc1-120">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="51cc1-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="51cc1-121">**Объект параметров**</span><span class="sxs-lookup"><span data-stu-id="51cc1-121">**Settings Object**</span></span>](settings-object.md)
</dt> </dl>

 

 





