---
title: Довнлоадитем. Cancel, метод
description: Обратите внимание, что в этом разделе описываются функции, предназначенные для использования Интернет-магазинами. Использование этой функции вне контекста Интернет-магазина не поддерживается. Метод Cancel отменяет скачивание.
ms.assetid: b3715fde-6a83-45fa-92ea-1cbffbee7274
keywords:
- метод Cancel проигрыватель Windows Media Player
- метод Cancel проигрыватель Windows Media Player, класс Довнлоадитем
- Класс Довнлоадитем Windows Media Player, метод Cancel
topic_type:
- apiref
api_name:
- DownloadItem.cancel
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c14d538e85d0930a43db883e226c007bea70de24
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105698946"
---
# <a name="downloaditemcancel-method"></a><span data-ttu-id="4e3e9-108">Довнлоадитем. Cancel, метод</span><span class="sxs-lookup"><span data-stu-id="4e3e9-108">DownloadItem.cancel method</span></span>

> [!Note]  
> <span data-ttu-id="4e3e9-109">В этом разделе описываются функции, предназначенные для использования в Интернет-магазинах.</span><span class="sxs-lookup"><span data-stu-id="4e3e9-109">This section describes functionality designed for use by online stores.</span></span> <span data-ttu-id="4e3e9-110">Использование этой функции вне контекста Интернет-магазина не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="4e3e9-110">Use of this functionality outside the context of an online store is not supported.</span></span>

 

<span data-ttu-id="4e3e9-111">Метод **Cancel** отменяет скачивание.</span><span class="sxs-lookup"><span data-stu-id="4e3e9-111">The **cancel** method cancels the download.</span></span>

## <a name="syntax"></a><span data-ttu-id="4e3e9-112">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="4e3e9-112">Syntax</span></span>


```JScript
DownloadItem.cancel()
```



## <a name="parameters"></a><span data-ttu-id="4e3e9-113">Параметры</span><span class="sxs-lookup"><span data-stu-id="4e3e9-113">Parameters</span></span>

<span data-ttu-id="4e3e9-114">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="4e3e9-114">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="4e3e9-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="4e3e9-115">Return value</span></span>

<span data-ttu-id="4e3e9-116">Этот метод не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="4e3e9-116">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="4e3e9-117">Комментарии</span><span class="sxs-lookup"><span data-stu-id="4e3e9-117">Remarks</span></span>

<span data-ttu-id="4e3e9-118">Отмененные элементы не удаляются из коллекции загрузки.</span><span class="sxs-lookup"><span data-stu-id="4e3e9-118">Cancelled items are not removed from the download collection.</span></span> <span data-ttu-id="4e3e9-119">Отмененные элементы возвращают **довнлоадстате** значение 4 (отменено).</span><span class="sxs-lookup"><span data-stu-id="4e3e9-119">Cancelled items return a **downloadState** value of 4 (canceled).</span></span>

## <a name="requirements"></a><span data-ttu-id="4e3e9-120">Требования</span><span class="sxs-lookup"><span data-stu-id="4e3e9-120">Requirements</span></span>



| <span data-ttu-id="4e3e9-121">Требование</span><span class="sxs-lookup"><span data-stu-id="4e3e9-121">Requirement</span></span> | <span data-ttu-id="4e3e9-122">Значение</span><span class="sxs-lookup"><span data-stu-id="4e3e9-122">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="4e3e9-123">Версия</span><span class="sxs-lookup"><span data-stu-id="4e3e9-123">Version</span></span><br/> | <span data-ttu-id="4e3e9-124">Проигрыватель Windows Media 9 Series или более поздней версии.</span><span class="sxs-lookup"><span data-stu-id="4e3e9-124">Windows Media Player 9 Series or later.</span></span><br/>                                 |
| <span data-ttu-id="4e3e9-125">DLL</span><span class="sxs-lookup"><span data-stu-id="4e3e9-125">DLL</span></span><br/>     | <dl> <span data-ttu-id="4e3e9-126"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4e3e9-126"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4e3e9-127">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="4e3e9-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4e3e9-128">**Объект Довнлоадитем**</span><span class="sxs-lookup"><span data-stu-id="4e3e9-128">**DownloadItem Object**</span></span>](downloaditem-object.md)
</dt> <dt>

[<span data-ttu-id="4e3e9-129">**Довнлоадитем. Довнлоадстате**</span><span class="sxs-lookup"><span data-stu-id="4e3e9-129">**DownloadItem.downloadState**</span></span>](downloaditem-downloadstate.md)
</dt> </dl>

 

 





