---
title: Ерроритем. Еррорконтекст
description: Свойство Еррорконтекст извлекает значение, указывающее контекст ошибки.
ms.assetid: 700d2bf0-dd3b-4211-99ea-58f952cf24b0
keywords:
- Проигрыватель Windows Media Ерроритем. Еррорконтекст
topic_type:
- apiref
api_name:
- ErrorItem.errorContext
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e9b9ed91d34645f08e7d3d28860ced9ca51420dc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105694535"
---
# <a name="erroritemerrorcontext"></a><span data-ttu-id="dec69-104">Ерроритем. Еррорконтекст</span><span class="sxs-lookup"><span data-stu-id="dec69-104">ErrorItem.errorContext</span></span>

<span data-ttu-id="dec69-105">Свойство **еррорконтекст** извлекает значение, указывающее контекст ошибки.</span><span class="sxs-lookup"><span data-stu-id="dec69-105">The **errorContext** property retrieves a value indicating the context of the error.</span></span>

``` syntax
player.error.item(
        index
        ).errorContext
```

## <a name="possible-values"></a><span data-ttu-id="dec69-106">Возможные значения</span><span class="sxs-lookup"><span data-stu-id="dec69-106">Possible Values</span></span>

<span data-ttu-id="dec69-107">Это свойство является **строкой** только для чтения, которая представляет код контекста ошибки.</span><span class="sxs-lookup"><span data-stu-id="dec69-107">This property is a read-only **String** that represents the error context code.</span></span>

## <a name="remarks"></a><span data-ttu-id="dec69-108">Комментарии</span><span class="sxs-lookup"><span data-stu-id="dec69-108">Remarks</span></span>

<span data-ttu-id="dec69-109">Контекст ошибки — это информация, используемая корпорацией Майкрософт для предоставления дополнительных сведений сотрудникам службы технической поддержки.</span><span class="sxs-lookup"><span data-stu-id="dec69-109">The error context is information that is used by Microsoft to provide additional information for technical support personnel.</span></span>

<span data-ttu-id="dec69-110">**Проигрыватель Windows Media 10 Mobile:** Это свойство всегда возвращает пустую строку.</span><span class="sxs-lookup"><span data-stu-id="dec69-110">**Windows Media Player 10 Mobile:** This property always returns an empty string.</span></span>

## <a name="requirements"></a><span data-ttu-id="dec69-111">Требования</span><span class="sxs-lookup"><span data-stu-id="dec69-111">Requirements</span></span>



| <span data-ttu-id="dec69-112">Требование</span><span class="sxs-lookup"><span data-stu-id="dec69-112">Requirement</span></span> | <span data-ttu-id="dec69-113">Значение</span><span class="sxs-lookup"><span data-stu-id="dec69-113">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="dec69-114">Версия</span><span class="sxs-lookup"><span data-stu-id="dec69-114">Version</span></span><br/> | <span data-ttu-id="dec69-115">Проигрыватель Windows Media версии 7,0 или более поздней</span><span class="sxs-lookup"><span data-stu-id="dec69-115">Windows Media Player version 7.0 or later</span></span><br/>                               |
| <span data-ttu-id="dec69-116">DLL</span><span class="sxs-lookup"><span data-stu-id="dec69-116">DLL</span></span><br/>     | <dl> <span data-ttu-id="dec69-117"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="dec69-117"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dec69-118">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="dec69-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dec69-119">**Объект Ерроритем**</span><span class="sxs-lookup"><span data-stu-id="dec69-119">**ErrorItem Object**</span></span>](erroritem-object.md)
</dt> </dl>

 

 





