---
description: Переход к странице на стороне клиента, непосредственно предшествующей странице, на которой размещены HTML-страницы на стороне сервера.
title: Вебвизардхост. Финалбакк, метод (Шлдисп. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WebWizardHost.FinalBack
api_type:
- COM
api_location:
- Shldisp.h
ms.assetid: a0616388-cf94-4433-ae52-24f02f1d15ac
ms.openlocfilehash: f131050bb5dd4cfc4b8533857c306f566f12ec2d
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/12/2021
ms.locfileid: "109841875"
---
# <a name="webwizardhostfinalback-method"></a><span data-ttu-id="92173-103">Вебвизардхост. Финалбакк, метод</span><span class="sxs-lookup"><span data-stu-id="92173-103">WebWizardHost.FinalBack method</span></span>

<span data-ttu-id="92173-104">Переход к странице на стороне клиента, непосредственно предшествующей странице, на которой размещены HTML-страницы на стороне сервера.</span><span class="sxs-lookup"><span data-stu-id="92173-104">Navigates to the client-side page immediately preceding the page hosting the server-side HTML pages.</span></span>

## <a name="syntax"></a><span data-ttu-id="92173-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="92173-105">Syntax</span></span>


```JScript
iRetVal = WebWizardHost.FinalBack()
```



## <a name="parameters"></a><span data-ttu-id="92173-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="92173-106">Parameters</span></span>

<span data-ttu-id="92173-107">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="92173-107">This method has no parameters.</span></span>

## <a name="remarks"></a><span data-ttu-id="92173-108">Remarks</span><span class="sxs-lookup"><span data-stu-id="92173-108">Remarks</span></span>

<span data-ttu-id="92173-109">Когда мастер отображает первую страницу на стороне сервера и пользователь нажимает кнопку « **назад** », сервер вызывает **финалбакк** при уведомлении этого события обработчиком событий клиента.</span><span class="sxs-lookup"><span data-stu-id="92173-109">When the wizard displays the first server-side page and the user clicks the **Back** button, the server invokes **FinalBack** when notified of that event by the client's event handler.</span></span>

## <a name="requirements"></a><span data-ttu-id="92173-110">Requirements (Требования)</span><span class="sxs-lookup"><span data-stu-id="92173-110">Requirements</span></span>



| <span data-ttu-id="92173-111">Требование</span><span class="sxs-lookup"><span data-stu-id="92173-111">Requirement</span></span> | <span data-ttu-id="92173-112">Значение</span><span class="sxs-lookup"><span data-stu-id="92173-112">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="92173-113">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="92173-113">Minimum supported client</span></span><br/> | <span data-ttu-id="92173-114">Только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="92173-114">Windows XP \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="92173-115">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="92173-115">Minimum supported server</span></span><br/> | <span data-ttu-id="92173-116">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="92173-116">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="92173-117">Заголовок</span><span class="sxs-lookup"><span data-stu-id="92173-117">Header</span></span><br/>                   | <dl> <span data-ttu-id="92173-118"><dt>Шлдисп. h</dt></span><span class="sxs-lookup"><span data-stu-id="92173-118"><dt>Shldisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="92173-119">IDL</span><span class="sxs-lookup"><span data-stu-id="92173-119">IDL</span></span><br/>                      | <dl> <span data-ttu-id="92173-120"><dt>Шлдисп. idl</dt></span><span class="sxs-lookup"><span data-stu-id="92173-120"><dt>Shldisp.idl</dt></span></span> </dl> |



 

 




