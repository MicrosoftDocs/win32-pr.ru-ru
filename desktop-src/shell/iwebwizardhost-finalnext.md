---
description: Переход к странице мастера на стороне клиента, расположенной после страницы, на которой размещены HTML-страницы на стороне сервера, или завершение работы мастера при отсутствии дополнительных страниц на стороне клиента.
title: Вебвизардхост. Финалнекст, метод (Шлдисп. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WebWizardHost.FinalNext
api_type:
- COM
api_location:
- Shldisp.h
ms.assetid: 0699eb16-d6ef-46e3-bd02-d35512536275
ms.openlocfilehash: fa59a70c04e7f78a315955aeabb9477c6f28c80d
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/12/2021
ms.locfileid: "109841845"
---
# <a name="webwizardhostfinalnext-method"></a><span data-ttu-id="d935d-103">Вебвизардхост. Финалнекст, метод</span><span class="sxs-lookup"><span data-stu-id="d935d-103">WebWizardHost.FinalNext method</span></span>

<span data-ttu-id="d935d-104">Переход к странице мастера на стороне клиента, расположенной после страницы, на которой размещены HTML-страницы на стороне сервера, или завершение работы мастера при отсутствии дополнительных страниц на стороне клиента.</span><span class="sxs-lookup"><span data-stu-id="d935d-104">Navigates to the client-side wizard page that follows the page that hosts the server-side HTML pages, or finishes the wizard if there are no further client-side pages.</span></span>

## <a name="syntax"></a><span data-ttu-id="d935d-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="d935d-105">Syntax</span></span>


```JScript
iRetVal = WebWizardHost.FinalNext()
```



## <a name="parameters"></a><span data-ttu-id="d935d-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="d935d-106">Parameters</span></span>

<span data-ttu-id="d935d-107">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="d935d-107">This method has no parameters.</span></span>

## <a name="remarks"></a><span data-ttu-id="d935d-108">Remarks</span><span class="sxs-lookup"><span data-stu-id="d935d-108">Remarks</span></span>

<span data-ttu-id="d935d-109">Когда мастер отображает последнюю HTML-страницу на стороне сервера и пользователь нажимает кнопку " **Далее** " или **"Готово** ", сервер вызывает **финалнекст** в обработчике событий этой кнопки.</span><span class="sxs-lookup"><span data-stu-id="d935d-109">When the wizard is displaying the last server-side HTML page and the user clicks the **Next** or **Finish** button, the server invokes **FinalNext** in that button's event handler.</span></span>

## <a name="requirements"></a><span data-ttu-id="d935d-110">Requirements (Требования)</span><span class="sxs-lookup"><span data-stu-id="d935d-110">Requirements</span></span>



| <span data-ttu-id="d935d-111">Требование</span><span class="sxs-lookup"><span data-stu-id="d935d-111">Requirement</span></span> | <span data-ttu-id="d935d-112">Значение</span><span class="sxs-lookup"><span data-stu-id="d935d-112">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="d935d-113">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="d935d-113">Minimum supported client</span></span><br/> | <span data-ttu-id="d935d-114">Только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="d935d-114">Windows XP \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="d935d-115">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="d935d-115">Minimum supported server</span></span><br/> | <span data-ttu-id="d935d-116">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="d935d-116">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="d935d-117">Заголовок</span><span class="sxs-lookup"><span data-stu-id="d935d-117">Header</span></span><br/>                   | <dl> <span data-ttu-id="d935d-118"><dt>Шлдисп. h</dt></span><span class="sxs-lookup"><span data-stu-id="d935d-118"><dt>Shldisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="d935d-119">IDL</span><span class="sxs-lookup"><span data-stu-id="d935d-119">IDL</span></span><br/>                      | <dl> <span data-ttu-id="d935d-120"><dt>Шлдисп. idl</dt></span><span class="sxs-lookup"><span data-stu-id="d935d-120"><dt>Shldisp.idl</dt></span></span> </dl> |



 

 




