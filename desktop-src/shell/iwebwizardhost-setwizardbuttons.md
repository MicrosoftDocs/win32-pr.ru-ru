---
description: Обновляет кнопки назад, далее и готово в кадре мастера клиента.
title: Вебвизардхост. Сетвизардбуттонс, метод (Шлдисп. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WebWizardHost.SetWizardButtons
api_type:
- COM
api_location:
- Shldisp.h
ms.assetid: 863aa667-454c-40cd-8091-9bb456047b6c
ms.openlocfilehash: a1b2a79c7ea323c36371e08d3519e71e4c537935
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/12/2021
ms.locfileid: "109842625"
---
# <a name="webwizardhostsetwizardbuttons-method"></a><span data-ttu-id="a3fab-103">Вебвизардхост. Сетвизардбуттонс, метод</span><span class="sxs-lookup"><span data-stu-id="a3fab-103">WebWizardHost.SetWizardButtons method</span></span>

<span data-ttu-id="a3fab-104">Обновляет кнопки **назад**, **Далее** и **Готово** в кадре мастера клиента.</span><span class="sxs-lookup"><span data-stu-id="a3fab-104">Updates the **Back**, **Next**, and **Finish** buttons in the client's wizard frame.</span></span>

## <a name="syntax"></a><span data-ttu-id="a3fab-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="a3fab-105">Syntax</span></span>


```JScript
iRetVal = WebWizardHost.SetWizardButtons(
  vbEnableBack,
  vbEnableNext,
  vbLastPage
)
```



## <a name="parameters"></a><span data-ttu-id="a3fab-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="a3fab-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a3fab-107">*вбенаблебакк* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="a3fab-107">*vbEnableBack* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a3fab-108">Тип: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="a3fab-108">Type: **Boolean**</span></span>

<span data-ttu-id="a3fab-109">Включает кнопку " **назад** ".</span><span class="sxs-lookup"><span data-stu-id="a3fab-109">Enables the **Back** button.</span></span>

</dd> <dt>

<span data-ttu-id="a3fab-110">*вбенабленекст* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="a3fab-110">*vbEnableNext* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a3fab-111">Тип: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="a3fab-111">Type: **Boolean**</span></span>

<span data-ttu-id="a3fab-112">Становится активной кнопка **Далее**.</span><span class="sxs-lookup"><span data-stu-id="a3fab-112">Enables the **Next** button.</span></span>

</dd> <dt>

<span data-ttu-id="a3fab-113">*вбластпаже* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="a3fab-113">*vbLastPage* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a3fab-114">Тип: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="a3fab-114">Type: **Boolean**</span></span>

<span data-ttu-id="a3fab-115">Включает кнопку **Готово** .</span><span class="sxs-lookup"><span data-stu-id="a3fab-115">Enables the **Finish** button.</span></span> <span data-ttu-id="a3fab-116">Указывает, что это последняя страница на стороне сервера.</span><span class="sxs-lookup"><span data-stu-id="a3fab-116">States that this is the last server-side page.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="a3fab-117">Remarks</span><span class="sxs-lookup"><span data-stu-id="a3fab-117">Remarks</span></span>

<span data-ttu-id="a3fab-118">Не забудьте реализовать функции обработчика на каждой странице на стороне сервера для функций onback () и onback (), соответствующих кнопкам мастера **назад** и **Далее**.</span><span class="sxs-lookup"><span data-stu-id="a3fab-118">Be sure to implement handler functions in each server-side page for OnBack() and OnNext(), corresponding to the wizard buttons **Back** and **Next**.</span></span> <span data-ttu-id="a3fab-119">Функции onback () и onback () отвечают на **сетвизардбуттонс**.</span><span class="sxs-lookup"><span data-stu-id="a3fab-119">The OnBack() and OnNext() functions respond to **SetWizardButtons**.</span></span> <span data-ttu-id="a3fab-120">В соответствующее время функция OnNext () вызывает **сетвизардбуттонс** с *вбластпаже* = **true**, что может включить кнопку **Готово** .</span><span class="sxs-lookup"><span data-stu-id="a3fab-120">At the appropriate time, the OnNext() function calls **SetWizardButtons** with *vbLastPage*=**true**, which can enable a **Finish** button.</span></span> <span data-ttu-id="a3fab-121">OnNext () также вызывает [**финалнекст**](iwebwizardhost-finalnext.md) , когда пользователь нажимает кнопку **Готово** .</span><span class="sxs-lookup"><span data-stu-id="a3fab-121">OnNext() also calls [**FinalNext**](iwebwizardhost-finalnext.md) when a user clicks the **Finish** button.</span></span>

## <a name="requirements"></a><span data-ttu-id="a3fab-122">Requirements (Требования)</span><span class="sxs-lookup"><span data-stu-id="a3fab-122">Requirements</span></span>



| <span data-ttu-id="a3fab-123">Требование</span><span class="sxs-lookup"><span data-stu-id="a3fab-123">Requirement</span></span> | <span data-ttu-id="a3fab-124">Значение</span><span class="sxs-lookup"><span data-stu-id="a3fab-124">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="a3fab-125">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="a3fab-125">Minimum supported client</span></span><br/> | <span data-ttu-id="a3fab-126">Только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="a3fab-126">Windows XP \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="a3fab-127">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="a3fab-127">Minimum supported server</span></span><br/> | <span data-ttu-id="a3fab-128">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="a3fab-128">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="a3fab-129">Заголовок</span><span class="sxs-lookup"><span data-stu-id="a3fab-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="a3fab-130"><dt>Шлдисп. h</dt></span><span class="sxs-lookup"><span data-stu-id="a3fab-130"><dt>Shldisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="a3fab-131">IDL</span><span class="sxs-lookup"><span data-stu-id="a3fab-131">IDL</span></span><br/>                      | <dl> <span data-ttu-id="a3fab-132"><dt>Шлдисп. idl</dt></span><span class="sxs-lookup"><span data-stu-id="a3fab-132"><dt>Shldisp.idl</dt></span></span> </dl> |



 

 




