---
description: Отображает или скрывает список автозавершения.
ms.assetid: 756ffa3d-03ee-4753-a826-3bc22ab16f5f
title: 'Метод Итипаутокомплетепровидер:: reby (Типаутокомплете. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITipAutocompleteProvider.Show
api_type:
- COM
api_location:
- tiptsf.dll
ms.openlocfilehash: 950358ae28d1cb68af803ed6b7f520f1bbad8c03
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103818112"
---
# <a name="itipautocompleteprovidershow-method"></a><span data-ttu-id="d17ce-103">Метод Итипаутокомплетепровидер:: «показывать»</span><span class="sxs-lookup"><span data-stu-id="d17ce-103">ITipAutocompleteProvider::Show method</span></span>

<span data-ttu-id="d17ce-104">Отображает или скрывает список автозавершения.</span><span class="sxs-lookup"><span data-stu-id="d17ce-104">Displays or hides the auto complete list.</span></span>

## <a name="syntax"></a><span data-ttu-id="d17ce-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="d17ce-105">Syntax</span></span>


```C++
HRESULT Show(
  [in] BOOL fShow
);
```



## <a name="parameters"></a><span data-ttu-id="d17ce-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="d17ce-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d17ce-107">*фшов* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="d17ce-107">*fShow* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d17ce-108">**Значение true** , чтобы показать пользовательский интерфейс автоматического завершения, **значение false** , чтобы скрыть пользовательский интерфейс списка автозавершения.</span><span class="sxs-lookup"><span data-stu-id="d17ce-108">**TRUE** to show the auto complete user interface, **FALSE** to hide the auto complete list user interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d17ce-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="d17ce-109">Return value</span></span>

<span data-ttu-id="d17ce-110">Этот метод может возвращать одно из этих значений.</span><span class="sxs-lookup"><span data-stu-id="d17ce-110">This method can return one of these values.</span></span>



| <span data-ttu-id="d17ce-111">Код возврата</span><span class="sxs-lookup"><span data-stu-id="d17ce-111">Return code</span></span>                                                                            | <span data-ttu-id="d17ce-112">Описание</span><span class="sxs-lookup"><span data-stu-id="d17ce-112">Description</span></span>                               |
|----------------------------------------------------------------------------------------|-------------------------------------------|
| <dl> <span data-ttu-id="d17ce-113"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="d17ce-113"><dt>**S\_OK**</dt></span></span> </dl>   | <span data-ttu-id="d17ce-114">Успешно.</span><span class="sxs-lookup"><span data-stu-id="d17ce-114">Success.</span></span><br/>                       |
| <dl> <span data-ttu-id="d17ce-115"><dt>**\_Ошибка E**</dt></span><span class="sxs-lookup"><span data-stu-id="d17ce-115"><dt>**E\_FAIL**</dt></span></span> </dl> | <span data-ttu-id="d17ce-116">Произошла неизвестная ошибка.</span><span class="sxs-lookup"><span data-stu-id="d17ce-116">An unspecified error occurred.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="d17ce-117">Комментарии</span><span class="sxs-lookup"><span data-stu-id="d17ce-117">Remarks</span></span>

<span data-ttu-id="d17ce-118">Этот метод вызывается клиентом для отображения или скрытия списка автозавершения.</span><span class="sxs-lookup"><span data-stu-id="d17ce-118">This method is called by the client to show or hide the auto complete list.</span></span> <span data-ttu-id="d17ce-119">Если список автозавершения не отображается и *фшов* имеет **значение false**, этот метод не выполняет никаких действий.</span><span class="sxs-lookup"><span data-stu-id="d17ce-119">If the auto complete list is not displayed and *fShow* is **FALSE**, this method does nothing.</span></span> <span data-ttu-id="d17ce-120">Если отображается список автозавершения и *фшов* имеет **значение true**, этот метод ничего не делает.</span><span class="sxs-lookup"><span data-stu-id="d17ce-120">If the auto complete list is displayed and *fShow* is **TRUE**, this method does nothing.</span></span>

## <a name="requirements"></a><span data-ttu-id="d17ce-121">Требования</span><span class="sxs-lookup"><span data-stu-id="d17ce-121">Requirements</span></span>



| <span data-ttu-id="d17ce-122">Требование</span><span class="sxs-lookup"><span data-stu-id="d17ce-122">Requirement</span></span> | <span data-ttu-id="d17ce-123">Значение</span><span class="sxs-lookup"><span data-stu-id="d17ce-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d17ce-124">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="d17ce-124">Minimum supported client</span></span><br/> | <span data-ttu-id="d17ce-125">Только классические приложения Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="d17ce-125">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                                   |
| <span data-ttu-id="d17ce-126">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="d17ce-126">Minimum supported server</span></span><br/> | <span data-ttu-id="d17ce-127">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="d17ce-127">None supported</span></span><br/>                                                                                                       |
| <span data-ttu-id="d17ce-128">Header</span><span class="sxs-lookup"><span data-stu-id="d17ce-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="d17ce-129"><dt>Типаутокомплете. h (также требуется Пенинпутпанел \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="d17ce-129"><dt>TipAutoComplete.h (also requires Peninputpanel\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="d17ce-130">DLL</span><span class="sxs-lookup"><span data-stu-id="d17ce-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d17ce-131"><dt>Tiptsf.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d17ce-131"><dt>Tiptsf.dll</dt></span></span> </dl>                                           |



## <a name="see-also"></a><span data-ttu-id="d17ce-132">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="d17ce-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d17ce-133">**Интерфейс Итипаутокомплетепровидер**</span><span class="sxs-lookup"><span data-stu-id="d17ce-133">**ITipAutocompleteProvider Interface**</span></span>](itipautocompleteprovider.md)
</dt> <dt>

[<span data-ttu-id="d17ce-134">Справочник по панели ввода текста</span><span class="sxs-lookup"><span data-stu-id="d17ce-134">Text Input Panel Reference</span></span>](text-input-panel-reference.md)
</dt> </dl>

 

 




