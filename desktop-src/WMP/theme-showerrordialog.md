---
title: THEME. Шоверрордиалог
description: Метод Шоверрордиалог отображает стандартное диалоговое окно ошибки.
ms.assetid: cec9ecfd-6665-4b0a-a09c-49120d557a80
keywords:
- Проигрыватель Windows Media THEME. Шоверрордиалог
topic_type:
- apiref
api_name:
- THEME.showErrorDialog
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 0cdc1f9df13ec460ce780507e1bde38a2996f915
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105688872"
---
# <a name="themeshowerrordialog"></a><span data-ttu-id="24730-104">THEME. Шоверрордиалог</span><span class="sxs-lookup"><span data-stu-id="24730-104">THEME.showErrorDialog</span></span>

<span data-ttu-id="24730-105">Метод **шоверрордиалог** отображает стандартное диалоговое окно ошибки.</span><span class="sxs-lookup"><span data-stu-id="24730-105">The **showErrorDialog** method displays the standard error dialog box.</span></span>

``` syntax
        theme.showErrorDialog()
```

## <a name="parameters"></a><span data-ttu-id="24730-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="24730-106">Parameters</span></span>

<span data-ttu-id="24730-107">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="24730-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="24730-108">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="24730-108">Return Value</span></span>

<span data-ttu-id="24730-109">Этот метод не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="24730-109">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="24730-110">Комментарии</span><span class="sxs-lookup"><span data-stu-id="24730-110">Remarks</span></span>

<span data-ttu-id="24730-111">Если **Settings. енаблиррордиалогс** имеет значение false, этот метод можно использовать для программного вывода диалогового окна об ошибке.</span><span class="sxs-lookup"><span data-stu-id="24730-111">If **Settings.enableErrorDialogs** is false, this method can be used to programmatically display the error dialog.</span></span> <span data-ttu-id="24730-112">Если в очереди ошибок нет ошибок, диалоговое окно ошибки не отображается.</span><span class="sxs-lookup"><span data-stu-id="24730-112">If there are no errors in the error queue, the error dialog box is not shown.</span></span>

<span data-ttu-id="24730-113">Для Windows Media Player 9 Series или более поздней версии этот метод должен вызываться из обработчика событий Error.</span><span class="sxs-lookup"><span data-stu-id="24730-113">For Windows Media Player 9 Series or later, this method must be called from the error event handler.</span></span> <span data-ttu-id="24730-114">Проигрыватель Windows Media 9 Series или более поздней версии очищает очередь ошибок для обложек после запуска события ошибки.</span><span class="sxs-lookup"><span data-stu-id="24730-114">Windows Media Player 9 Series or later clears the error queue for skins after the error event has been fired.</span></span>

## <a name="requirements"></a><span data-ttu-id="24730-115">Требования</span><span class="sxs-lookup"><span data-stu-id="24730-115">Requirements</span></span>



| <span data-ttu-id="24730-116">Требование</span><span class="sxs-lookup"><span data-stu-id="24730-116">Requirement</span></span> | <span data-ttu-id="24730-117">Значение</span><span class="sxs-lookup"><span data-stu-id="24730-117">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="24730-118">Версия</span><span class="sxs-lookup"><span data-stu-id="24730-118">Version</span></span><br/> | <span data-ttu-id="24730-119">Проигрыватель Windows Media версии 7,0 или более поздней</span><span class="sxs-lookup"><span data-stu-id="24730-119">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="24730-120">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="24730-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="24730-121">**Элемент THEME**</span><span class="sxs-lookup"><span data-stu-id="24730-121">**THEME Element**</span></span>](theme-element.md)
</dt> <dt>

[<span data-ttu-id="24730-122">**Settings. Енаблиррордиалогс**</span><span class="sxs-lookup"><span data-stu-id="24730-122">**Settings.enableErrorDialogs**</span></span>](settings-enableerrordialogs.md)
</dt> </dl>

 

 





