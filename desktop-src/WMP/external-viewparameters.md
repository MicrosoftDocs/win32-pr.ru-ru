---
title: External. Виевпараметерс
description: Обратите внимание, что в этом разделе описываются функции, предназначенные для использования в Интернет-магазинах. | External. Виевпараметерс
ms.assetid: 0afabe35-2857-413a-a662-1a76d3fb75fe
keywords:
- Внешний Виевпараметерс проигрыватель Windows Media
topic_type:
- apiref
api_name:
- External.viewParameters
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ea0adec580a68bd3f6b92beef1de814729848179
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105695054"
---
# <a name="externalviewparameters"></a><span data-ttu-id="dcba4-105">External. Виевпараметерс</span><span class="sxs-lookup"><span data-stu-id="dcba4-105">External.viewParameters</span></span>

> [!Note]  
> <span data-ttu-id="dcba4-106">В этом разделе описываются функции, предназначенные для использования в Интернет-магазинах.</span><span class="sxs-lookup"><span data-stu-id="dcba4-106">This topic describes functionality designed for use by online stores.</span></span> <span data-ttu-id="dcba4-107">Использование этой функции вне контекста Интернет-магазина не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="dcba4-107">Use of this functionality outside the context of an online store is not supported.</span></span>

 

<span data-ttu-id="dcba4-108">Свойство **виевпараметерс** извлекает параметры, связанные с текущим представлением в проигрывателе Windows Media.</span><span class="sxs-lookup"><span data-stu-id="dcba4-108">The **viewParameters** property retrieves parameters associated with the current view in Windows Media Player.</span></span>

## <a name="syntax"></a><span data-ttu-id="dcba4-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="dcba4-109">Syntax</span></span>

<span data-ttu-id="dcba4-110">**Window. external. Виевпараметерс**</span><span class="sxs-lookup"><span data-stu-id="dcba4-110">**window.external.viewParameters**</span></span>

## <a name="possible-values"></a><span data-ttu-id="dcba4-111">Возможные значения</span><span class="sxs-lookup"><span data-stu-id="dcba4-111">Possible Values</span></span>

<span data-ttu-id="dcba4-112">Это свойство возвращает **строку**, доступную только для чтения.</span><span class="sxs-lookup"><span data-stu-id="dcba4-112">This property returns a read-only **String**.</span></span>

## <a name="remarks"></a><span data-ttu-id="dcba4-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="dcba4-113">Remarks</span></span>

<span data-ttu-id="dcba4-114">Это свойство извлекает параметры, которые ранее были заданы в Интернет-магазине.</span><span class="sxs-lookup"><span data-stu-id="dcba4-114">This property retrieves parameters that were previously set by the online store.</span></span> <span data-ttu-id="dcba4-115">Например, в Интернет-магазине можно указать параметры представления в параметре *виевпарамс* метода [Чанжевиев](external-changeview.md) или параметр *params* метода [чанжевиевонлинелист](external-changeviewonlinelist.md) .</span><span class="sxs-lookup"><span data-stu-id="dcba4-115">For example, the online store can specify view parameters in the *ViewParams* parameter of the [changeView](external-changeview.md) method or the *Params* parameter of the [changeViewOnlineList](external-changeviewonlinelist.md) method.</span></span>

<span data-ttu-id="dcba4-116">Параметры представления не обрабатываются проигрывателем Windows Media.</span><span class="sxs-lookup"><span data-stu-id="dcba4-116">View parameters are not interpreted by Windows Media Player.</span></span> <span data-ttu-id="dcba4-117">Они создаются Интернет-магазином и имеют значение только в Интернет-магазине.</span><span class="sxs-lookup"><span data-stu-id="dcba4-117">They are created by the online store and have meaning only to the online store.</span></span>

## <a name="requirements"></a><span data-ttu-id="dcba4-118">Требования</span><span class="sxs-lookup"><span data-stu-id="dcba4-118">Requirements</span></span>



| <span data-ttu-id="dcba4-119">Требование</span><span class="sxs-lookup"><span data-stu-id="dcba4-119">Requirement</span></span> | <span data-ttu-id="dcba4-120">Значение</span><span class="sxs-lookup"><span data-stu-id="dcba4-120">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="dcba4-121">Версия</span><span class="sxs-lookup"><span data-stu-id="dcba4-121">Version</span></span><br/> | <span data-ttu-id="dcba4-122">Проигрыватель Windows Media 11.</span><span class="sxs-lookup"><span data-stu-id="dcba4-122">Windows Media Player 11.</span></span><br/>                                                |
| <span data-ttu-id="dcba4-123">DLL</span><span class="sxs-lookup"><span data-stu-id="dcba4-123">DLL</span></span><br/>     | <dl> <span data-ttu-id="dcba4-124"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="dcba4-124"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dcba4-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="dcba4-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dcba4-126">**Внешний объект для Интернет-магазинов типа 1**</span><span class="sxs-lookup"><span data-stu-id="dcba4-126">**External Object for Type 1 Online Stores**</span></span>](external-object-for-type-1-online-stores.md)
</dt> </dl>

 

 





