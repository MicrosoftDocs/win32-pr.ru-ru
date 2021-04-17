---
title: Внешний метод проверки подлинности
description: Метод проверки подлинности инициирует попытку проверки подлинности пользователя.
ms.assetid: db4cd2c6-b735-40b1-af96-82a40bda9d97
keywords:
- метод проверки подлинности Windows Media Player
- метод проверки подлинности Windows Media Player, внешний класс
- Внешний класс проигрыватель Windows Media Player, метод проверки подлинности
topic_type:
- apiref
api_name:
- External.authenticate
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aa2bba0afb80c4285ad8fa8d2c20191321315d60
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105695064"
---
# <a name="externalauthenticate-method"></a><span data-ttu-id="0dd2a-106">Внешний метод проверки подлинности</span><span class="sxs-lookup"><span data-stu-id="0dd2a-106">External.authenticate method</span></span>

<span data-ttu-id="0dd2a-107">Метод **проверки подлинности** инициирует попытку проверки подлинности пользователя.</span><span class="sxs-lookup"><span data-stu-id="0dd2a-107">The **authenticate** method initiates an attempt to authenticate the user.</span></span>

## <a name="syntax"></a><span data-ttu-id="0dd2a-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="0dd2a-108">Syntax</span></span>


```JScript
External.authenticate(
  AuthenticationIndex
)
```



## <a name="parameters"></a><span data-ttu-id="0dd2a-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="0dd2a-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0dd2a-110">*Аусентикатиониндекс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="0dd2a-110">*AuthenticationIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0dd2a-111">**Число** (**Long**), указывающее индекс веб-страницы успешного выполнения проверки подлинности.</span><span class="sxs-lookup"><span data-stu-id="0dd2a-111">**Number** (**long**) that specifies the index of an authentication-success webpage.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0dd2a-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="0dd2a-112">Return value</span></span>

<span data-ttu-id="0dd2a-113">Этот метод не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="0dd2a-113">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="0dd2a-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="0dd2a-114">Remarks</span></span>

<span data-ttu-id="0dd2a-115">Некоторые ссылки на странице обнаружения имеют целевые объекты, которые должны отображаться только после проверки подлинности пользователя.</span><span class="sxs-lookup"><span data-stu-id="0dd2a-115">Certain links on a discovery page have targets that should be displayed only after the user has been authenticated.</span></span> <span data-ttu-id="0dd2a-116">На странице Обнаружение, проигрыватель Windows Media и подключаемый модуль интернет-магазина выполните следующие действия, чтобы проверить подлинность пользователя и отобразить целевую веб-страницу:</span><span class="sxs-lookup"><span data-stu-id="0dd2a-116">The discovery page, Windows Media Player, and the online store's plug-in use the following steps to authenticate the user and display the target webpage:</span></span>

1.  <span data-ttu-id="0dd2a-117">Скрипт на странице обнаружения вызывает *внешний* объект. метод **проверки подлинности** .</span><span class="sxs-lookup"><span data-stu-id="0dd2a-117">Script on a discovery page calls the *External*.**authenticate** method.</span></span>
2.  <span data-ttu-id="0dd2a-118">Проигрыватель Windows Media отображает диалоговое окно для получения имени пользователя и пароля.</span><span class="sxs-lookup"><span data-stu-id="0dd2a-118">Windows Media Player displays a dialog box to obtain a user name and password.</span></span>
3.  <span data-ttu-id="0dd2a-119">Проигрыватель Windows Media вызывает метод [ивмпконтентпартнер:: Authenticate](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-authenticate), который инициирует попытку проверки подлинности и немедленно возвращает результат.</span><span class="sxs-lookup"><span data-stu-id="0dd2a-119">Windows Media Player calls [IWMPContentPartner::Authenticate](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-authenticate), which initiates the authentication attempt and returns immediately.</span></span>
4.  <span data-ttu-id="0dd2a-120">По завершении проверки подлинности подключаемый модуль интернет-магазина вызывает [ивмпконтентпартнеркаллбакк:: notify](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartnercallback-notify), передает Вмпкнаусресулт и логическое значение, указывающее, была ли попытка успешной.</span><span class="sxs-lookup"><span data-stu-id="0dd2a-120">When the authentication attempt is complete, the online store's plug-in calls [IWMPContentPartnerCallback::Notify](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartnercallback-notify), passing wmpcnAuthResult and a Boolean value that indicates whether the attempt was successful.</span></span>
5.  <span data-ttu-id="0dd2a-121">Если попытка проверки подлинности прошла успешно, проигрыватель Windows Media вызывает [ивмпконтентпартнер:: GetItemInfo](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-getiteminfo), передавая g \_ сзитеминфо \_ аусентикатионсукцессурл, чтобы получить URL-адрес веб-страницы, которая успешно проходит проверку подлинности.</span><span class="sxs-lookup"><span data-stu-id="0dd2a-121">If the authentication attempt was successful, Windows Media Player calls [IWMPContentPartner::GetItemInfo](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-getiteminfo), passing g\_szItemInfo\_AuthenticationSuccessURL, to obtain the URL of an authentication-success webpage.</span></span> <span data-ttu-id="0dd2a-122">В этом вызове проигрыватель Windows Media передает тот же индекс, что и страница обнаружения, передаваемая *внешней*. метод **проверки подлинности** .</span><span class="sxs-lookup"><span data-stu-id="0dd2a-122">In this call, Windows Media Player passes the same index that the discovery page passed to the *External*.**authenticate** method.</span></span>
6.  <span data-ttu-id="0dd2a-123">Проигрыватель Windows Media отображает веб-страницу Проверка подлинности — успешно выполненная.</span><span class="sxs-lookup"><span data-stu-id="0dd2a-123">Windows Media Player displays the authentication-success webpage.</span></span>

## <a name="requirements"></a><span data-ttu-id="0dd2a-124">Требования</span><span class="sxs-lookup"><span data-stu-id="0dd2a-124">Requirements</span></span>



| <span data-ttu-id="0dd2a-125">Требование</span><span class="sxs-lookup"><span data-stu-id="0dd2a-125">Requirement</span></span> | <span data-ttu-id="0dd2a-126">Значение</span><span class="sxs-lookup"><span data-stu-id="0dd2a-126">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="0dd2a-127">Версия</span><span class="sxs-lookup"><span data-stu-id="0dd2a-127">Version</span></span><br/> | <span data-ttu-id="0dd2a-128">Проигрыватель Windows Media 11</span><span class="sxs-lookup"><span data-stu-id="0dd2a-128">Windows Media Player 11</span></span><br/>                                                 |
| <span data-ttu-id="0dd2a-129">DLL</span><span class="sxs-lookup"><span data-stu-id="0dd2a-129">DLL</span></span><br/>     | <dl> <span data-ttu-id="0dd2a-130"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0dd2a-130"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0dd2a-131">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="0dd2a-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0dd2a-132">**Внешний объект для Интернет-магазинов типа 1**</span><span class="sxs-lookup"><span data-stu-id="0dd2a-132">**External Object for Type 1 Online Stores**</span></span>](external-object-for-type-1-online-stores.md)
</dt> <dt>

[<span data-ttu-id="0dd2a-133">**External. Аттемптлогин**</span><span class="sxs-lookup"><span data-stu-id="0dd2a-133">**External.attemptLogin**</span></span>](external-attemptlogin.md)
</dt> <dt>

[<span data-ttu-id="0dd2a-134">**External. Усерлогжедин**</span><span class="sxs-lookup"><span data-stu-id="0dd2a-134">**External.userLoggedIn**</span></span>](external-userloggedin.md)
</dt> </dl>

 

 





