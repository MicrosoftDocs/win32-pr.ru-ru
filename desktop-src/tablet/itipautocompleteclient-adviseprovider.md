---
description: Регистрирует поставщик в клиенте, чтобы позволить клиенту вызывать объект поставщика автозавершения приложения.
ms.assetid: 7b761b30-66f7-454a-9e0d-f45c8099f19f
title: 'Метод Итипаутокомплетеклиент:: Адвисепровидер (Типаутокомплете. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITipAutocompleteClient.AdviseProvider
api_type:
- COM
api_location:
- tiptsf.dll
ms.openlocfilehash: 9ef35ac730089403ac47c14421de96e75a022192
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105712133"
---
# <a name="itipautocompleteclientadviseprovider-method"></a><span data-ttu-id="e863c-103">Метод Итипаутокомплетеклиент:: Адвисепровидер</span><span class="sxs-lookup"><span data-stu-id="e863c-103">ITipAutocompleteClient::AdviseProvider method</span></span>

<span data-ttu-id="e863c-104">Регистрирует поставщик в клиенте, чтобы позволить клиенту вызывать объект поставщика автозавершения приложения.</span><span class="sxs-lookup"><span data-stu-id="e863c-104">Registers the provider with the client to enable the client to call the application's auto complete provider object.</span></span>

## <a name="syntax"></a><span data-ttu-id="e863c-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="e863c-105">Syntax</span></span>


```C++
HRESULT AdviseProvider(
  [in] HWND                     hWndField,
  [in] ITipAutocompleteProvider *pIACProvider
);
```



## <a name="parameters"></a><span data-ttu-id="e863c-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="e863c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e863c-107">*хвндфиелд* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="e863c-107">*hWndField* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e863c-108">Описатель окна поля, предоставляющего функцию автозавершения.</span><span class="sxs-lookup"><span data-stu-id="e863c-108">The window handle of the field which provide the auto complete feature.</span></span>

</dd> <dt>

<span data-ttu-id="e863c-109">*пиакпровидер* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="e863c-109">*pIACProvider* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e863c-110">Указатель интерфейса на интерфейс автоматического завершения поставщика.</span><span class="sxs-lookup"><span data-stu-id="e863c-110">The interface pointer to the auto complete provider interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e863c-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="e863c-111">Return value</span></span>

<span data-ttu-id="e863c-112">Этот метод может возвращать одно из этих значений.</span><span class="sxs-lookup"><span data-stu-id="e863c-112">This method can return one of these values.</span></span>



| <span data-ttu-id="e863c-113">Код возврата</span><span class="sxs-lookup"><span data-stu-id="e863c-113">Return code</span></span>                                                                            | <span data-ttu-id="e863c-114">Описание</span><span class="sxs-lookup"><span data-stu-id="e863c-114">Description</span></span>                               |
|----------------------------------------------------------------------------------------|-------------------------------------------|
| <dl> <span data-ttu-id="e863c-115"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="e863c-115"><dt>**S\_OK**</dt></span></span> </dl>   | <span data-ttu-id="e863c-116">Успешно.</span><span class="sxs-lookup"><span data-stu-id="e863c-116">Success.</span></span><br/>                       |
| <dl> <span data-ttu-id="e863c-117"><dt>**\_Ошибка E**</dt></span><span class="sxs-lookup"><span data-stu-id="e863c-117"><dt>**E\_FAIL**</dt></span></span> </dl> | <span data-ttu-id="e863c-118">Произошла неизвестная ошибка.</span><span class="sxs-lookup"><span data-stu-id="e863c-118">An unspecified error occurred.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="e863c-119">Требования</span><span class="sxs-lookup"><span data-stu-id="e863c-119">Requirements</span></span>



| <span data-ttu-id="e863c-120">Требование</span><span class="sxs-lookup"><span data-stu-id="e863c-120">Requirement</span></span> | <span data-ttu-id="e863c-121">Значение</span><span class="sxs-lookup"><span data-stu-id="e863c-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e863c-122">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="e863c-122">Minimum supported client</span></span><br/> | <span data-ttu-id="e863c-123">Только классические приложения Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="e863c-123">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                                   |
| <span data-ttu-id="e863c-124">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="e863c-124">Minimum supported server</span></span><br/> | <span data-ttu-id="e863c-125">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="e863c-125">None supported</span></span><br/>                                                                                                       |
| <span data-ttu-id="e863c-126">Header</span><span class="sxs-lookup"><span data-stu-id="e863c-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="e863c-127"><dt>Типаутокомплете. h (также требуется Пенинпутпанел \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="e863c-127"><dt>TipAutoComplete.h (also requires Peninputpanel\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="e863c-128">DLL</span><span class="sxs-lookup"><span data-stu-id="e863c-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e863c-129"><dt>Tiptsf.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e863c-129"><dt>Tiptsf.dll</dt></span></span> </dl>                                           |



## <a name="see-also"></a><span data-ttu-id="e863c-130">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="e863c-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e863c-131">**Интерфейс Итипаутокомплетеклиент**</span><span class="sxs-lookup"><span data-stu-id="e863c-131">**ITipAutocompleteClient Interface**</span></span>](itipautocompleteclient.md)
</dt> <dt>

[<span data-ttu-id="e863c-132">**Метод Итипаутокомплетеклиент:: Унадвисепровидер**</span><span class="sxs-lookup"><span data-stu-id="e863c-132">**ITipAutocompleteClient::UnadviseProvider Method**</span></span>](itipautocompleteclient-unadviseprovider.md)
</dt> <dt>

[<span data-ttu-id="e863c-133">Справочник по панели ввода текста</span><span class="sxs-lookup"><span data-stu-id="e863c-133">Text Input Panel Reference</span></span>](text-input-panel-reference.md)
</dt> </dl>

 

 




