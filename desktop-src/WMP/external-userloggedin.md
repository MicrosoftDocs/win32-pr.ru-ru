---
title: External. Усерлогжедин
description: Обратите внимание, что в этом разделе описываются функции, предназначенные для использования в Интернет-магазинах. | External. Усерлогжедин
ms.assetid: d02d9486-c692-4f46-bc29-f0aaa45cad0f
keywords:
- Внешний Усерлогжедин проигрыватель Windows Media
topic_type:
- apiref
api_name:
- External.userLoggedIn
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9a5454dd9d2fa2d771005448a4157c33b5634a30
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105695058"
---
# <a name="externaluserloggedin"></a><span data-ttu-id="89972-105">External. Усерлогжедин</span><span class="sxs-lookup"><span data-stu-id="89972-105">External.userLoggedIn</span></span>

> [!Note]  
> <span data-ttu-id="89972-106">В этом разделе описываются функции, предназначенные для использования в Интернет-магазинах.</span><span class="sxs-lookup"><span data-stu-id="89972-106">This topic describes functionality designed for use by online stores.</span></span> <span data-ttu-id="89972-107">Использование этой функции вне контекста Интернет-магазина не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="89972-107">Use of this functionality outside the context of an online store is not supported.</span></span>

 

<span data-ttu-id="89972-108">Свойство **усерлогжедин** извлекает значение, указывающее, вошел ли пользователь в Интернет-магазин.</span><span class="sxs-lookup"><span data-stu-id="89972-108">The **userLoggedIn** property retrieves a value indicating whether the user is logged in to the online store.</span></span>

## <a name="syntax"></a><span data-ttu-id="89972-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="89972-109">Syntax</span></span>

``` syntax
window.external.userLoggedIn
```

## <a name="possible-values"></a><span data-ttu-id="89972-110">Возможные значения</span><span class="sxs-lookup"><span data-stu-id="89972-110">Possible Values</span></span>

<span data-ttu-id="89972-111">Это свойство является **логическим значением**, доступным только для чтения.</span><span class="sxs-lookup"><span data-stu-id="89972-111">This property is a read-only **Boolean**.</span></span> <span data-ttu-id="89972-112">**Значение true** указывает, что пользователь вошел в систему, а **значение false** указывает, что пользователь вышел из систему.</span><span class="sxs-lookup"><span data-stu-id="89972-112">**TRUE** indicates that the user is logged in, and **FALSE** indicates that the user is logged out.</span></span>

## <a name="requirements"></a><span data-ttu-id="89972-113">Требования</span><span class="sxs-lookup"><span data-stu-id="89972-113">Requirements</span></span>



| <span data-ttu-id="89972-114">Требование</span><span class="sxs-lookup"><span data-stu-id="89972-114">Requirement</span></span> | <span data-ttu-id="89972-115">Значение</span><span class="sxs-lookup"><span data-stu-id="89972-115">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="89972-116">Версия</span><span class="sxs-lookup"><span data-stu-id="89972-116">Version</span></span><br/> | <span data-ttu-id="89972-117">Проигрыватель Windows Media 11.</span><span class="sxs-lookup"><span data-stu-id="89972-117">Windows Media Player 11.</span></span><br/>                                                |
| <span data-ttu-id="89972-118">DLL</span><span class="sxs-lookup"><span data-stu-id="89972-118">DLL</span></span><br/>     | <dl> <span data-ttu-id="89972-119"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="89972-119"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="89972-120">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="89972-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="89972-121">**Внешний объект для Интернет-магазинов типа 1**</span><span class="sxs-lookup"><span data-stu-id="89972-121">**External Object for Type 1 Online Stores**</span></span>](external-object-for-type-1-online-stores.md)
</dt> <dt>

[<span data-ttu-id="89972-122">**External. Аттемптлогин**</span><span class="sxs-lookup"><span data-stu-id="89972-122">**External.attemptLogin**</span></span>](external-attemptlogin.md)
</dt> <dt>

[<span data-ttu-id="89972-123">**Внешнее событие Онлогинчанже**</span><span class="sxs-lookup"><span data-stu-id="89972-123">**External.OnLoginChange Event**</span></span>](external-onloginchange-event.md)
</dt> </dl>

 

 





