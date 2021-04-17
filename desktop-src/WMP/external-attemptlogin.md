---
title: External. Аттемптлогин, метод
description: Метод Аттемптлогин отображает диалоговое окно, чтобы пользователь мог попытаться войти в Интернет-магазин.
ms.assetid: 04fe476f-6d0e-4faa-9e4a-f87bed782205
keywords:
- Аттемптлогин метод Windows Media Player
- Аттемптлогин метод Windows Media Player, внешний класс
- Внешний класс проигрыватель Windows Media Player, метод Аттемптлогин
topic_type:
- apiref
api_name:
- External.attemptLogin
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 86958c241f2399efbe342371b8cd4cfd376ff628
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105695065"
---
# <a name="externalattemptlogin-method"></a><span data-ttu-id="514a9-106">External. Аттемптлогин, метод</span><span class="sxs-lookup"><span data-stu-id="514a9-106">External.attemptLogin method</span></span>

<span data-ttu-id="514a9-107">Метод **аттемптлогин** отображает диалоговое окно, чтобы пользователь мог попытаться войти в Интернет-магазин.</span><span class="sxs-lookup"><span data-stu-id="514a9-107">The **attemptLogin** method displays a dialog box so the user can attempt to log in to the online store.</span></span>

## <a name="syntax"></a><span data-ttu-id="514a9-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="514a9-108">Syntax</span></span>


```JScript
External.attemptLogin()
```



## <a name="parameters"></a><span data-ttu-id="514a9-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="514a9-109">Parameters</span></span>

<span data-ttu-id="514a9-110">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="514a9-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="514a9-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="514a9-111">Return value</span></span>

<span data-ttu-id="514a9-112">Этот метод не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="514a9-112">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="514a9-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="514a9-113">Remarks</span></span>

<span data-ttu-id="514a9-114">Если при входе в систему возникает изменение состояния входа, проигрыватель Windows Media вызывает событие [онлогинчанже](external-onloginchange-event.md) .</span><span class="sxs-lookup"><span data-stu-id="514a9-114">If the log-in attempt results in a change of log-in status, Windows Media Player raises the [OnLoginChange](external-onloginchange-event.md) event.</span></span>

## <a name="requirements"></a><span data-ttu-id="514a9-115">Требования</span><span class="sxs-lookup"><span data-stu-id="514a9-115">Requirements</span></span>



| <span data-ttu-id="514a9-116">Требование</span><span class="sxs-lookup"><span data-stu-id="514a9-116">Requirement</span></span> | <span data-ttu-id="514a9-117">Значение</span><span class="sxs-lookup"><span data-stu-id="514a9-117">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="514a9-118">Версия</span><span class="sxs-lookup"><span data-stu-id="514a9-118">Version</span></span><br/> | <span data-ttu-id="514a9-119">Проигрыватель Windows Media 11.</span><span class="sxs-lookup"><span data-stu-id="514a9-119">Windows Media Player 11.</span></span><br/>                                                |
| <span data-ttu-id="514a9-120">DLL</span><span class="sxs-lookup"><span data-stu-id="514a9-120">DLL</span></span><br/>     | <dl> <span data-ttu-id="514a9-121"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="514a9-121"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="514a9-122">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="514a9-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="514a9-123">**Внешний объект для Интернет-магазинов типа 1**</span><span class="sxs-lookup"><span data-stu-id="514a9-123">**External Object for Type 1 Online Stores**</span></span>](external-object-for-type-1-online-stores.md)
</dt> <dt>

[<span data-ttu-id="514a9-124">**Внешнее событие Онлогинчанже**</span><span class="sxs-lookup"><span data-stu-id="514a9-124">**External.OnLoginChange Event**</span></span>](external-onloginchange-event.md)
</dt> <dt>

[<span data-ttu-id="514a9-125">**External. Усерлогжедин**</span><span class="sxs-lookup"><span data-stu-id="514a9-125">**External.userLoggedIn**</span></span>](external-userloggedin.md)
</dt> <dt>

[<span data-ttu-id="514a9-126">**Ивмпконтентпартнер:: login**</span><span class="sxs-lookup"><span data-stu-id="514a9-126">**IWMPContentPartner::Login**</span></span>](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-login)
</dt> <dt>

[<span data-ttu-id="514a9-127">**Управление именем входа**</span><span class="sxs-lookup"><span data-stu-id="514a9-127">**Managing Login**</span></span>](managing-login.md)
</dt> </dl>

 

 





