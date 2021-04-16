---
description: Уведомляет панель ввода о том, что пользователь выбрал что-либо в списке автозавершения, и отбросить оставшийся текст, который еще не был вставлен.
ms.assetid: 2e6fabe1-7984-4908-bf90-0603d0dad268
title: 'Метод Итипаутокомплетеклиент:: Усерселектион (Типаутокомплете. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITipAutocompleteClient.UserSelection
api_type:
- COM
api_location:
- tiptsf.dll
ms.openlocfilehash: 1894db9da3b8e3a36e59eb45150b27facfe0291f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105712131"
---
# <a name="itipautocompleteclientuserselection-method"></a><span data-ttu-id="50e88-103">Метод Итипаутокомплетеклиент:: Усерселектион</span><span class="sxs-lookup"><span data-stu-id="50e88-103">ITipAutocompleteClient::UserSelection method</span></span>

<span data-ttu-id="50e88-104">Уведомляет панель ввода о том, что пользователь выбрал что-либо в списке автозавершения, и отбросить оставшийся текст, который еще не был вставлен.</span><span class="sxs-lookup"><span data-stu-id="50e88-104">Notifies the Input Panel that the user has selected something in the auto complete list and to discard all remaining text that has not yet been inserted.</span></span>

## <a name="syntax"></a><span data-ttu-id="50e88-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="50e88-105">Syntax</span></span>


```C++
HRESULT UserSelection();
```



## <a name="parameters"></a><span data-ttu-id="50e88-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="50e88-106">Parameters</span></span>

<span data-ttu-id="50e88-107">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="50e88-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="50e88-108">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="50e88-108">Return value</span></span>

<span data-ttu-id="50e88-109">Этот метод может возвращать одно из этих значений.</span><span class="sxs-lookup"><span data-stu-id="50e88-109">This method can return one of these values.</span></span>



| <span data-ttu-id="50e88-110">Код возврата</span><span class="sxs-lookup"><span data-stu-id="50e88-110">Return code</span></span>                                                                            | <span data-ttu-id="50e88-111">Описание</span><span class="sxs-lookup"><span data-stu-id="50e88-111">Description</span></span>                               |
|----------------------------------------------------------------------------------------|-------------------------------------------|
| <dl> <span data-ttu-id="50e88-112"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="50e88-112"><dt>**S\_OK**</dt></span></span> </dl>   | <span data-ttu-id="50e88-113">Успешно.</span><span class="sxs-lookup"><span data-stu-id="50e88-113">Success.</span></span><br/>                       |
| <dl> <span data-ttu-id="50e88-114"><dt>**\_Ошибка E**</dt></span><span class="sxs-lookup"><span data-stu-id="50e88-114"><dt>**E\_FAIL**</dt></span></span> </dl> | <span data-ttu-id="50e88-115">Произошла неизвестная ошибка.</span><span class="sxs-lookup"><span data-stu-id="50e88-115">An unspecified error occurred.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="50e88-116">Комментарии</span><span class="sxs-lookup"><span data-stu-id="50e88-116">Remarks</span></span>

<span data-ttu-id="50e88-117">Этот метод вызывается из поставщика для уведомления клиента о том, что выбор сделан пользователем.</span><span class="sxs-lookup"><span data-stu-id="50e88-117">This method is called from the provider to notify the client that a selection has been made by the user.</span></span>

## <a name="requirements"></a><span data-ttu-id="50e88-118">Требования</span><span class="sxs-lookup"><span data-stu-id="50e88-118">Requirements</span></span>



| <span data-ttu-id="50e88-119">Требование</span><span class="sxs-lookup"><span data-stu-id="50e88-119">Requirement</span></span> | <span data-ttu-id="50e88-120">Значение</span><span class="sxs-lookup"><span data-stu-id="50e88-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="50e88-121">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="50e88-121">Minimum supported client</span></span><br/> | <span data-ttu-id="50e88-122">Только классические приложения Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="50e88-122">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                                   |
| <span data-ttu-id="50e88-123">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="50e88-123">Minimum supported server</span></span><br/> | <span data-ttu-id="50e88-124">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="50e88-124">None supported</span></span><br/>                                                                                                       |
| <span data-ttu-id="50e88-125">Header</span><span class="sxs-lookup"><span data-stu-id="50e88-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="50e88-126"><dt>Типаутокомплете. h (также требуется Пенинпутпанел \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="50e88-126"><dt>TipAutoComplete.h (also requires Peninputpanel\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="50e88-127">DLL</span><span class="sxs-lookup"><span data-stu-id="50e88-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="50e88-128"><dt>Tiptsf.dll</dt></span><span class="sxs-lookup"><span data-stu-id="50e88-128"><dt>Tiptsf.dll</dt></span></span> </dl>                                           |



## <a name="see-also"></a><span data-ttu-id="50e88-129">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="50e88-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="50e88-130">**Интерфейс Итипаутокомплетеклиент**</span><span class="sxs-lookup"><span data-stu-id="50e88-130">**ITipAutocompleteClient Interface**</span></span>](itipautocompleteclient.md)
</dt> <dt>

[<span data-ttu-id="50e88-131">Справочник по панели ввода текста</span><span class="sxs-lookup"><span data-stu-id="50e88-131">Text Input Panel Reference</span></span>](text-input-panel-reference.md)
</dt> </dl>

 

 




