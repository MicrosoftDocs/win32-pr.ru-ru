---
description: Отменяет регистрацию связанного поставщика.
ms.assetid: b5edc33d-dfd0-4350-b8cd-eaa30b726771
title: 'Метод Итипаутокомплетеклиент:: Унадвисепровидер (Типаутокомплете. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITipAutocompleteClient.UnadviseProvider
api_type:
- COM
api_location:
- tiptsf.dll
ms.openlocfilehash: 1100ebb700ef2fb769a13f9b62aacf5c1d007e0d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103910439"
---
# <a name="itipautocompleteclientunadviseprovider-method"></a><span data-ttu-id="34565-103">Метод Итипаутокомплетеклиент:: Унадвисепровидер</span><span class="sxs-lookup"><span data-stu-id="34565-103">ITipAutocompleteClient::UnadviseProvider method</span></span>

<span data-ttu-id="34565-104">Отменяет регистрацию связанного поставщика.</span><span class="sxs-lookup"><span data-stu-id="34565-104">Unregisters the associated provider.</span></span>

## <a name="syntax"></a><span data-ttu-id="34565-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="34565-105">Syntax</span></span>


```C++
HRESULT UnadviseProvider(
  [in] HWND                   hWndField,
  [in] ITipAutocompleProvider *pIACProvider
);
```



## <a name="parameters"></a><span data-ttu-id="34565-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="34565-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="34565-107">*хвндфиелд* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="34565-107">*hWndField* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="34565-108">Описатель окна поля, предоставляющего функцию автозавершения.</span><span class="sxs-lookup"><span data-stu-id="34565-108">Window handle of the field which provide the auto complete feature.</span></span>

</dd> <dt>

<span data-ttu-id="34565-109">*пиакпровидер* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="34565-109">*pIACProvider* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="34565-110">Указатель интерфейса на интерфейс поставщика автозавершения для отмены регистрации.</span><span class="sxs-lookup"><span data-stu-id="34565-110">Interface pointer to the auto complete provider interface to be unregistered.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="34565-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="34565-111">Return value</span></span>

<span data-ttu-id="34565-112">Этот метод может возвращать одно из этих значений.</span><span class="sxs-lookup"><span data-stu-id="34565-112">This method can return one of these values.</span></span>



| <span data-ttu-id="34565-113">Код возврата</span><span class="sxs-lookup"><span data-stu-id="34565-113">Return code</span></span>                                                                            | <span data-ttu-id="34565-114">Описание</span><span class="sxs-lookup"><span data-stu-id="34565-114">Description</span></span>                               |
|----------------------------------------------------------------------------------------|-------------------------------------------|
| <dl> <span data-ttu-id="34565-115"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="34565-115"><dt>**S\_OK**</dt></span></span> </dl>   | <span data-ttu-id="34565-116">Успешно.</span><span class="sxs-lookup"><span data-stu-id="34565-116">Success.</span></span><br/>                       |
| <dl> <span data-ttu-id="34565-117"><dt>**\_Ошибка E**</dt></span><span class="sxs-lookup"><span data-stu-id="34565-117"><dt>**E\_FAIL**</dt></span></span> </dl> | <span data-ttu-id="34565-118">Произошла неизвестная ошибка.</span><span class="sxs-lookup"><span data-stu-id="34565-118">An unspecified error occurred.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="34565-119">Требования</span><span class="sxs-lookup"><span data-stu-id="34565-119">Requirements</span></span>



| <span data-ttu-id="34565-120">Требование</span><span class="sxs-lookup"><span data-stu-id="34565-120">Requirement</span></span> | <span data-ttu-id="34565-121">Значение</span><span class="sxs-lookup"><span data-stu-id="34565-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="34565-122">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="34565-122">Minimum supported client</span></span><br/> | <span data-ttu-id="34565-123">Только классические приложения Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="34565-123">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                                   |
| <span data-ttu-id="34565-124">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="34565-124">Minimum supported server</span></span><br/> | <span data-ttu-id="34565-125">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="34565-125">None supported</span></span><br/>                                                                                                       |
| <span data-ttu-id="34565-126">Header</span><span class="sxs-lookup"><span data-stu-id="34565-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="34565-127"><dt>Типаутокомплете. h (также требуется Пенинпутпанел \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="34565-127"><dt>TipAutoComplete.h (also requires Peninputpanel\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="34565-128">DLL</span><span class="sxs-lookup"><span data-stu-id="34565-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="34565-129"><dt>Tiptsf.dll</dt></span><span class="sxs-lookup"><span data-stu-id="34565-129"><dt>Tiptsf.dll</dt></span></span> </dl>                                           |



## <a name="see-also"></a><span data-ttu-id="34565-130">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="34565-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="34565-131">**Интерфейс Итипаутокомплетеклиент**</span><span class="sxs-lookup"><span data-stu-id="34565-131">**ITipAutocompleteClient Interface**</span></span>](itipautocompleteclient.md)
</dt> <dt>

[<span data-ttu-id="34565-132">Справочник по панели ввода текста</span><span class="sxs-lookup"><span data-stu-id="34565-132">Text Input Panel Reference</span></span>](text-input-panel-reference.md)
</dt> </dl>

 

 




