---
description: Используется клиентом автоматического завершения для уведомления приложения о тексте, которое пользователь направит на панель ввода.
ms.assetid: 68413836-321a-4e75-8538-c5a8fc577c0f
title: 'Метод Итипаутокомплетепровидер:: Упдатепендингтекст (Типаутокомплете. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITipAutocompleteProvider.UpdatePendingText
api_type:
- COM
api_location:
- tiptsf.dll
ms.openlocfilehash: 5c66e625639aa7088b1b3934a2f984d0f4097536
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104081588"
---
# <a name="itipautocompleteproviderupdatependingtext-method"></a><span data-ttu-id="5ed4b-103">Метод Итипаутокомплетепровидер:: Упдатепендингтекст</span><span class="sxs-lookup"><span data-stu-id="5ed4b-103">ITipAutocompleteProvider::UpdatePendingText method</span></span>

<span data-ttu-id="5ed4b-104">Используется клиентом автоматического завершения для уведомления приложения о тексте, которое пользователь направит на панель ввода.</span><span class="sxs-lookup"><span data-stu-id="5ed4b-104">Used by the auto complete client to notify the application of the text a user has inked into Input Panel.</span></span>

## <a name="syntax"></a><span data-ttu-id="5ed4b-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="5ed4b-105">Syntax</span></span>


```C++
HRESULT UpdatePendingText(
  [in] BSTR bstrPendingText
);
```



## <a name="parameters"></a><span data-ttu-id="5ed4b-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="5ed4b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5ed4b-107">*бстрпендингтекст* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="5ed4b-107">*bstrPendingText* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5ed4b-108">Исходный текст, используемый для создания списка автозавершения.</span><span class="sxs-lookup"><span data-stu-id="5ed4b-108">Source text to be used to generate the auto complete list.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5ed4b-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="5ed4b-109">Return value</span></span>

<span data-ttu-id="5ed4b-110">Этот метод может возвращать одно из этих значений.</span><span class="sxs-lookup"><span data-stu-id="5ed4b-110">This method can return one of these values.</span></span>



| <span data-ttu-id="5ed4b-111">Код возврата</span><span class="sxs-lookup"><span data-stu-id="5ed4b-111">Return code</span></span>                                                                            | <span data-ttu-id="5ed4b-112">Описание</span><span class="sxs-lookup"><span data-stu-id="5ed4b-112">Description</span></span>                               |
|----------------------------------------------------------------------------------------|-------------------------------------------|
| <dl> <span data-ttu-id="5ed4b-113"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="5ed4b-113"><dt>**S\_OK**</dt></span></span> </dl>   | <span data-ttu-id="5ed4b-114">Успешно.</span><span class="sxs-lookup"><span data-stu-id="5ed4b-114">Success.</span></span><br/>                       |
| <dl> <span data-ttu-id="5ed4b-115"><dt>**\_Ошибка E**</dt></span><span class="sxs-lookup"><span data-stu-id="5ed4b-115"><dt>**E\_FAIL**</dt></span></span> </dl> | <span data-ttu-id="5ed4b-116">Произошла неизвестная ошибка.</span><span class="sxs-lookup"><span data-stu-id="5ed4b-116">An unspecified error occurred.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="5ed4b-117">Комментарии</span><span class="sxs-lookup"><span data-stu-id="5ed4b-117">Remarks</span></span>

<span data-ttu-id="5ed4b-118">Этот текст не будет содержать текст, уже вставленный в поле "поля ввода".</span><span class="sxs-lookup"><span data-stu-id="5ed4b-118">This text will not contain the text already inserted in the focused field.</span></span> <span data-ttu-id="5ed4b-119">Поставщик автозаполнения отвечает за принятие счета за текущий текст поля и выбор для создания списка автозавершения.</span><span class="sxs-lookup"><span data-stu-id="5ed4b-119">The auto complete provider is responsible for taking into account the current field text and the selection to generate the auto complete list.</span></span> <span data-ttu-id="5ed4b-120">Если *бстрпендингтекст* имеет **значение NULL**, то список автоматических завершений создается с текущим текстом слева от выделенного поля.</span><span class="sxs-lookup"><span data-stu-id="5ed4b-120">When *bstrPendingText* is **NULL**, the auto complete list is generated with the current text to the left of the selection in the field.</span></span>

## <a name="requirements"></a><span data-ttu-id="5ed4b-121">Требования</span><span class="sxs-lookup"><span data-stu-id="5ed4b-121">Requirements</span></span>



| <span data-ttu-id="5ed4b-122">Требование</span><span class="sxs-lookup"><span data-stu-id="5ed4b-122">Requirement</span></span> | <span data-ttu-id="5ed4b-123">Значение</span><span class="sxs-lookup"><span data-stu-id="5ed4b-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5ed4b-124">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="5ed4b-124">Minimum supported client</span></span><br/> | <span data-ttu-id="5ed4b-125">Только классические приложения Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="5ed4b-125">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                                   |
| <span data-ttu-id="5ed4b-126">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="5ed4b-126">Minimum supported server</span></span><br/> | <span data-ttu-id="5ed4b-127">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="5ed4b-127">None supported</span></span><br/>                                                                                                       |
| <span data-ttu-id="5ed4b-128">Header</span><span class="sxs-lookup"><span data-stu-id="5ed4b-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="5ed4b-129"><dt>Типаутокомплете. h (также требуется Пенинпутпанел \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="5ed4b-129"><dt>TipAutoComplete.h (also requires Peninputpanel\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="5ed4b-130">DLL</span><span class="sxs-lookup"><span data-stu-id="5ed4b-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5ed4b-131"><dt>Tiptsf.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5ed4b-131"><dt>Tiptsf.dll</dt></span></span> </dl>                                           |



## <a name="see-also"></a><span data-ttu-id="5ed4b-132">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="5ed4b-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5ed4b-133">**Интерфейс Итипаутокомплетепровидер**</span><span class="sxs-lookup"><span data-stu-id="5ed4b-133">**ITipAutocompleteProvider Interface**</span></span>](itipautocompleteprovider.md)
</dt> <dt>

[<span data-ttu-id="5ed4b-134">Справочник по панели ввода текста</span><span class="sxs-lookup"><span data-stu-id="5ed4b-134">Text Input Panel Reference</span></span>](text-input-panel-reference.md)
</dt> </dl>

 

 




