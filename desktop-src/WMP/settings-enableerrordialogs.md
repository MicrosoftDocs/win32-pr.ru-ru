---
title: Settings. Енаблиррордиалогс
description: Свойство Енаблиррордиалогс указывает или получает значение, указывающее, отображаются ли диалоговые окна ошибок автоматически.
ms.assetid: 16b10bea-4b3e-469f-a903-02f19ffcdf31
keywords:
- Проигрыватель Windows Media Settings. Енаблиррордиалогс
topic_type:
- apiref
api_name:
- Settings.enableErrorDialogs
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c5746bb68da71ca827da3923e4956b613eabdb50
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105647987"
---
# <a name="settingsenableerrordialogs"></a><span data-ttu-id="2a4f3-104">Settings. Енаблиррордиалогс</span><span class="sxs-lookup"><span data-stu-id="2a4f3-104">Settings.enableErrorDialogs</span></span>

<span data-ttu-id="2a4f3-105">Свойство **енаблиррордиалогс** указывает или получает значение, указывающее, отображаются ли диалоговые окна ошибок автоматически.</span><span class="sxs-lookup"><span data-stu-id="2a4f3-105">The **enableErrorDialogs** property specifies or retrieves a value indicating whether error dialog boxes are shown automatically.</span></span>

## <a name="syntax"></a><span data-ttu-id="2a4f3-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="2a4f3-106">Syntax</span></span>

<span data-ttu-id="2a4f3-107">Player. Settings. Енаблиррордиалогс</span><span class="sxs-lookup"><span data-stu-id="2a4f3-107">player.settings.enableErrorDialogs</span></span>

## <a name="possible-values"></a><span data-ttu-id="2a4f3-108">Возможные значения</span><span class="sxs-lookup"><span data-stu-id="2a4f3-108">Possible Values</span></span>

<span data-ttu-id="2a4f3-109">Это свойство является **логическим значением** для чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="2a4f3-109">This property is a read/write **Boolean**.</span></span>



| <span data-ttu-id="2a4f3-110">Значение</span><span class="sxs-lookup"><span data-stu-id="2a4f3-110">Value</span></span> | <span data-ttu-id="2a4f3-111">Описание</span><span class="sxs-lookup"><span data-stu-id="2a4f3-111">Description</span></span>                                     |
|-------|-------------------------------------------------|
| <span data-ttu-id="2a4f3-112">true</span><span class="sxs-lookup"><span data-stu-id="2a4f3-112">true</span></span>  | <span data-ttu-id="2a4f3-113">По умолчанию.</span><span class="sxs-lookup"><span data-stu-id="2a4f3-113">Default.</span></span> <span data-ttu-id="2a4f3-114">Диалоговые окна ошибок отображаются автоматически.</span><span class="sxs-lookup"><span data-stu-id="2a4f3-114">Error dialogs are shown automatically.</span></span> |
| <span data-ttu-id="2a4f3-115">false</span><span class="sxs-lookup"><span data-stu-id="2a4f3-115">false</span></span> | <span data-ttu-id="2a4f3-116">Диалоговые окна ошибок не отображаются автоматически.</span><span class="sxs-lookup"><span data-stu-id="2a4f3-116">Error dialogs are not shown automatically.</span></span>      |



 

## <a name="remarks"></a><span data-ttu-id="2a4f3-117">Комментарии</span><span class="sxs-lookup"><span data-stu-id="2a4f3-117">Remarks</span></span>

<span data-ttu-id="2a4f3-118">Это свойство характерно для удаленных экземпляров элемента управления проигрывателя.</span><span class="sxs-lookup"><span data-stu-id="2a4f3-118">This property exhibits specific behavior for remoted instances of the Player control.</span></span> <span data-ttu-id="2a4f3-119">Дополнительные сведения см. [в разделе Удаленное взаимодействие с элементом управления проигрывателя Windows Media](remoting-the-windows-media-player-control.md).</span><span class="sxs-lookup"><span data-stu-id="2a4f3-119">For more information, see [Remoting the Windows Media Player Control](remoting-the-windows-media-player-control.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="2a4f3-120">Требования</span><span class="sxs-lookup"><span data-stu-id="2a4f3-120">Requirements</span></span>



| <span data-ttu-id="2a4f3-121">Требование</span><span class="sxs-lookup"><span data-stu-id="2a4f3-121">Requirement</span></span> | <span data-ttu-id="2a4f3-122">Значение</span><span class="sxs-lookup"><span data-stu-id="2a4f3-122">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="2a4f3-123">Версия</span><span class="sxs-lookup"><span data-stu-id="2a4f3-123">Version</span></span><br/> | <span data-ttu-id="2a4f3-124">Проигрыватель Windows Media версии 7,0 или более поздней.</span><span class="sxs-lookup"><span data-stu-id="2a4f3-124">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="2a4f3-125">DLL</span><span class="sxs-lookup"><span data-stu-id="2a4f3-125">DLL</span></span><br/>     | <dl> <span data-ttu-id="2a4f3-126"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2a4f3-126"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2a4f3-127">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="2a4f3-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2a4f3-128">**Объект параметров**</span><span class="sxs-lookup"><span data-stu-id="2a4f3-128">**Settings Object**</span></span>](settings-object.md)
</dt> </dl>

 

 





