---
description: Определяет, готова ли панель ввода к отображению списка автозавершения.
ms.assetid: 1e0d4bc6-e6a3-4123-a381-00a41ed9c848
title: 'Метод Итипаутокомплетеклиент:: Рекуестшовуи (Типаутокомплете. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITipAutocompleteClient.RequestShowUI
api_type:
- COM
api_location:
- tiptsf.dll
ms.openlocfilehash: e547376bf2e9c50c224d1917e00329e8d9555e6d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104264886"
---
# <a name="itipautocompleteclientrequestshowui-method"></a><span data-ttu-id="27ec7-103">Метод Итипаутокомплетеклиент:: Рекуестшовуи</span><span class="sxs-lookup"><span data-stu-id="27ec7-103">ITipAutocompleteClient::RequestShowUI method</span></span>

<span data-ttu-id="27ec7-104">Определяет, готова ли панель ввода к отображению списка автозавершения.</span><span class="sxs-lookup"><span data-stu-id="27ec7-104">Determines whether Input Panel is ready to have the auto complete list shown.</span></span>

## <a name="syntax"></a><span data-ttu-id="27ec7-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="27ec7-105">Syntax</span></span>


```C++
HRESULT RequestShowUI(
  [in]  HWND hWndACList,
  [out] BOOL *pfAllowShowing
);
```



## <a name="parameters"></a><span data-ttu-id="27ec7-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="27ec7-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="27ec7-107">*хвндаклист* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="27ec7-107">*hWndACList* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="27ec7-108">Описатель окна пользовательского интерфейса списка автозавершения.</span><span class="sxs-lookup"><span data-stu-id="27ec7-108">Window handle of the auto complete list user interface.</span></span>

</dd> <dt>

<span data-ttu-id="27ec7-109">*пфалловшовинг* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="27ec7-109">*pfAllowShowing* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="27ec7-110">**Значение false** , если клиент рекомендует не отображать пользовательский интерфейс списка автозавершения.</span><span class="sxs-lookup"><span data-stu-id="27ec7-110">**FALSE** if client recommends to not show the auto complete list user interface.</span></span> <span data-ttu-id="27ec7-111">**Значение true** , если поставщик автоматической полноты может отображать пользовательский интерфейс списка.</span><span class="sxs-lookup"><span data-stu-id="27ec7-111">**TRUE** if the auto complete provider can show the list user interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="27ec7-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="27ec7-112">Return value</span></span>

<span data-ttu-id="27ec7-113">Этот метод может возвращать одно из этих значений.</span><span class="sxs-lookup"><span data-stu-id="27ec7-113">This method can return one of these values.</span></span>



| <span data-ttu-id="27ec7-114">Код возврата</span><span class="sxs-lookup"><span data-stu-id="27ec7-114">Return code</span></span>                                                                            | <span data-ttu-id="27ec7-115">Описание</span><span class="sxs-lookup"><span data-stu-id="27ec7-115">Description</span></span>                               |
|----------------------------------------------------------------------------------------|-------------------------------------------|
| <dl> <span data-ttu-id="27ec7-116"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="27ec7-116"><dt>**S\_OK**</dt></span></span> </dl>   | <span data-ttu-id="27ec7-117">Успешно.</span><span class="sxs-lookup"><span data-stu-id="27ec7-117">Success.</span></span><br/>                       |
| <dl> <span data-ttu-id="27ec7-118"><dt>**\_Ошибка E**</dt></span><span class="sxs-lookup"><span data-stu-id="27ec7-118"><dt>**E\_FAIL**</dt></span></span> </dl> | <span data-ttu-id="27ec7-119">Произошла неизвестная ошибка.</span><span class="sxs-lookup"><span data-stu-id="27ec7-119">An unspecified error occurred.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="27ec7-120">Комментарии</span><span class="sxs-lookup"><span data-stu-id="27ec7-120">Remarks</span></span>

<span data-ttu-id="27ec7-121">Этот метод вызывается поставщиком автозавершения, когда он собирается отобразить пользовательский интерфейс автоматического завершения.</span><span class="sxs-lookup"><span data-stu-id="27ec7-121">This method is called by the auto complete provider when it is about to show the auto complete user interface.</span></span> <span data-ttu-id="27ec7-122">Если внутреннее состояние клиента не позволяет поставщику отображать пользовательский интерфейс, *пфалловшовинг* будет иметь значение **false**.</span><span class="sxs-lookup"><span data-stu-id="27ec7-122">If the client's internal state doesn't allow the provider to show the user interface, *pfAllowShowing* will be set to **FALSE**.</span></span> <span data-ttu-id="27ec7-123">Например, когда текст отправляется в поле из обложки рукописного ввода на панели ввода Tablet PC и пользователь сразу же начинает ввод рукописного ввода, клиент не рекомендует отображать пользовательский интерфейс автоматического завершения, чтобы избежать деструктуры рукописного ввода пользователя, установив для *Пфалловшовинг* **значение false**.</span><span class="sxs-lookup"><span data-stu-id="27ec7-123">For example, when the text gets sent to the field from the handwriting skin on the Tablet PC Input Panel and the user immediately starts inking, the client will recommend to not show the auto complete user interface, in order to avoid destructing the user's inking, by setting *pfAllowShowing* to **FALSE**.</span></span>

<span data-ttu-id="27ec7-124">Вызовите **рекуестшовуи** , чтобы задать обработчик окна списка автозаполнения всплывающих окон перед вызовом [**метода Итипаутокомплетеклиент::P реферредректс**](itipautocompleteclient-preferredrects.md).</span><span class="sxs-lookup"><span data-stu-id="27ec7-124">Call **RequestShowUI** to set the popup auto complete list window handle before you call the [**ITipAutocompleteClient::PreferredRects Method**](itipautocompleteclient-preferredrects.md).</span></span> <span data-ttu-id="27ec7-125">Несоблюдение этого действия приведет к ошибке **E \_ INVALIDARG** при вызове **преферредректс**.</span><span class="sxs-lookup"><span data-stu-id="27ec7-125">Failure to do so will cause an **E\_INVALIDARG** error when calling **PreferredRects**.</span></span>

## <a name="requirements"></a><span data-ttu-id="27ec7-126">Требования</span><span class="sxs-lookup"><span data-stu-id="27ec7-126">Requirements</span></span>



| <span data-ttu-id="27ec7-127">Требование</span><span class="sxs-lookup"><span data-stu-id="27ec7-127">Requirement</span></span> | <span data-ttu-id="27ec7-128">Значение</span><span class="sxs-lookup"><span data-stu-id="27ec7-128">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="27ec7-129">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="27ec7-129">Minimum supported client</span></span><br/> | <span data-ttu-id="27ec7-130">Только классические приложения Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="27ec7-130">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                                   |
| <span data-ttu-id="27ec7-131">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="27ec7-131">Minimum supported server</span></span><br/> | <span data-ttu-id="27ec7-132">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="27ec7-132">None supported</span></span><br/>                                                                                                       |
| <span data-ttu-id="27ec7-133">Header</span><span class="sxs-lookup"><span data-stu-id="27ec7-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="27ec7-134"><dt>Типаутокомплете. h (также требуется Пенинпутпанел \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="27ec7-134"><dt>TipAutoComplete.h (also requires Peninputpanel\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="27ec7-135">DLL</span><span class="sxs-lookup"><span data-stu-id="27ec7-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="27ec7-136"><dt>Tiptsf.dll</dt></span><span class="sxs-lookup"><span data-stu-id="27ec7-136"><dt>Tiptsf.dll</dt></span></span> </dl>                                           |



## <a name="see-also"></a><span data-ttu-id="27ec7-137">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="27ec7-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="27ec7-138">**Интерфейс Итипаутокомплетеклиент**</span><span class="sxs-lookup"><span data-stu-id="27ec7-138">**ITipAutocompleteClient Interface**</span></span>](itipautocompleteclient.md)
</dt> <dt>

[<span data-ttu-id="27ec7-139">**Итипаутокомплетеклиент: метод:P Реферредректс**</span><span class="sxs-lookup"><span data-stu-id="27ec7-139">**ITipAutocompleteClient::PreferredRects Method**</span></span>](itipautocompleteclient-preferredrects.md)
</dt> <dt>

[<span data-ttu-id="27ec7-140">Справочник по панели ввода текста</span><span class="sxs-lookup"><span data-stu-id="27ec7-140">Text Input Panel Reference</span></span>](text-input-panel-reference.md)
</dt> </dl>

 

 




