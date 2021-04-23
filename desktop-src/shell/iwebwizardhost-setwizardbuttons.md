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
ms.openlocfilehash: 18af31eac1042e84a41e5651c517279869f03697
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104985785"
---
# <a name="webwizardhostsetwizardbuttons-method"></a><span data-ttu-id="609ef-103">Вебвизардхост. Сетвизардбуттонс, метод</span><span class="sxs-lookup"><span data-stu-id="609ef-103">WebWizardHost.SetWizardButtons method</span></span>

<span data-ttu-id="609ef-104">Обновляет кнопки **назад**, **Далее** и **Готово** в кадре мастера клиента.</span><span class="sxs-lookup"><span data-stu-id="609ef-104">Updates the **Back**, **Next**, and **Finish** buttons in the client's wizard frame.</span></span>

## <a name="syntax"></a><span data-ttu-id="609ef-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="609ef-105">Syntax</span></span>


```JScript
iRetVal = WebWizardHost.SetWizardButtons(
  vbEnableBack,
  vbEnableNext,
  vbLastPage
)
```



## <a name="parameters"></a><span data-ttu-id="609ef-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="609ef-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="609ef-107">*вбенаблебакк* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="609ef-107">*vbEnableBack* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="609ef-108">Тип: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="609ef-108">Type: **Boolean**</span></span>

<span data-ttu-id="609ef-109">Включает кнопку " **назад** ".</span><span class="sxs-lookup"><span data-stu-id="609ef-109">Enables the **Back** button.</span></span>

</dd> <dt>

<span data-ttu-id="609ef-110">*вбенабленекст* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="609ef-110">*vbEnableNext* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="609ef-111">Тип: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="609ef-111">Type: **Boolean**</span></span>

<span data-ttu-id="609ef-112">Становится активной кнопка **Далее**.</span><span class="sxs-lookup"><span data-stu-id="609ef-112">Enables the **Next** button.</span></span>

</dd> <dt>

<span data-ttu-id="609ef-113">*вбластпаже* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="609ef-113">*vbLastPage* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="609ef-114">Тип: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="609ef-114">Type: **Boolean**</span></span>

<span data-ttu-id="609ef-115">Включает кнопку **Готово** .</span><span class="sxs-lookup"><span data-stu-id="609ef-115">Enables the **Finish** button.</span></span> <span data-ttu-id="609ef-116">Указывает, что это последняя страница на стороне сервера.</span><span class="sxs-lookup"><span data-stu-id="609ef-116">States that this is the last server-side page.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="609ef-117">Примечания</span><span class="sxs-lookup"><span data-stu-id="609ef-117">Remarks</span></span>

<span data-ttu-id="609ef-118">Не забудьте реализовать функции обработчика на каждой странице на стороне сервера для функций onback () и onback (), соответствующих кнопкам мастера **назад** и **Далее**.</span><span class="sxs-lookup"><span data-stu-id="609ef-118">Be sure to implement handler functions in each server-side page for OnBack() and OnNext(), corresponding to the wizard buttons **Back** and **Next**.</span></span> <span data-ttu-id="609ef-119">Функции onback () и onback () отвечают на **сетвизардбуттонс**.</span><span class="sxs-lookup"><span data-stu-id="609ef-119">The OnBack() and OnNext() functions respond to **SetWizardButtons**.</span></span> <span data-ttu-id="609ef-120">В соответствующее время функция OnNext () вызывает **сетвизардбуттонс** с *вбластпаже* = **true**, что может включить кнопку **Готово** .</span><span class="sxs-lookup"><span data-stu-id="609ef-120">At the appropriate time, the OnNext() function calls **SetWizardButtons** with *vbLastPage*=**true**, which can enable a **Finish** button.</span></span> <span data-ttu-id="609ef-121">OnNext () также вызывает [**финалнекст**](iwebwizardhost-finalnext.md) , когда пользователь нажимает кнопку **Готово** .</span><span class="sxs-lookup"><span data-stu-id="609ef-121">OnNext() also calls [**FinalNext**](iwebwizardhost-finalnext.md) when a user clicks the **Finish** button.</span></span>

## <a name="requirements"></a><span data-ttu-id="609ef-122">Требования</span><span class="sxs-lookup"><span data-stu-id="609ef-122">Requirements</span></span>



| <span data-ttu-id="609ef-123">Требование</span><span class="sxs-lookup"><span data-stu-id="609ef-123">Requirement</span></span> | <span data-ttu-id="609ef-124">Значение</span><span class="sxs-lookup"><span data-stu-id="609ef-124">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="609ef-125">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="609ef-125">Minimum supported client</span></span><br/> | <span data-ttu-id="609ef-126">Только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="609ef-126">Windows XP \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="609ef-127">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="609ef-127">Minimum supported server</span></span><br/> | <span data-ttu-id="609ef-128">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="609ef-128">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="609ef-129">Header</span><span class="sxs-lookup"><span data-stu-id="609ef-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="609ef-130"><dt>Шлдисп. h</dt></span><span class="sxs-lookup"><span data-stu-id="609ef-130"><dt>Shldisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="609ef-131">IDL</span><span class="sxs-lookup"><span data-stu-id="609ef-131">IDL</span></span><br/>                      | <dl> <span data-ttu-id="609ef-132"><dt>Шлдисп. idl</dt></span><span class="sxs-lookup"><span data-stu-id="609ef-132"><dt>Shldisp.idl</dt></span></span> </dl> |



 

 




