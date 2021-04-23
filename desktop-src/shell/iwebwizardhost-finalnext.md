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
ms.openlocfilehash: 5693de342b03a9ee4b7ed04cf24d8cfa9ee8b784
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104265468"
---
# <a name="webwizardhostfinalnext-method"></a><span data-ttu-id="c86de-103">Вебвизардхост. Финалнекст, метод</span><span class="sxs-lookup"><span data-stu-id="c86de-103">WebWizardHost.FinalNext method</span></span>

<span data-ttu-id="c86de-104">Переход к странице мастера на стороне клиента, расположенной после страницы, на которой размещены HTML-страницы на стороне сервера, или завершение работы мастера при отсутствии дополнительных страниц на стороне клиента.</span><span class="sxs-lookup"><span data-stu-id="c86de-104">Navigates to the client-side wizard page that follows the page that hosts the server-side HTML pages, or finishes the wizard if there are no further client-side pages.</span></span>

## <a name="syntax"></a><span data-ttu-id="c86de-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="c86de-105">Syntax</span></span>


```JScript
iRetVal = WebWizardHost.FinalNext()
```



## <a name="parameters"></a><span data-ttu-id="c86de-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="c86de-106">Parameters</span></span>

<span data-ttu-id="c86de-107">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="c86de-107">This method has no parameters.</span></span>

## <a name="remarks"></a><span data-ttu-id="c86de-108">Примечания</span><span class="sxs-lookup"><span data-stu-id="c86de-108">Remarks</span></span>

<span data-ttu-id="c86de-109">Когда мастер отображает последнюю HTML-страницу на стороне сервера и пользователь нажимает кнопку " **Далее** " или **"Готово** ", сервер вызывает **финалнекст** в обработчике событий этой кнопки.</span><span class="sxs-lookup"><span data-stu-id="c86de-109">When the wizard is displaying the last server-side HTML page and the user clicks the **Next** or **Finish** button, the server invokes **FinalNext** in that button's event handler.</span></span>

## <a name="requirements"></a><span data-ttu-id="c86de-110">Требования</span><span class="sxs-lookup"><span data-stu-id="c86de-110">Requirements</span></span>



| <span data-ttu-id="c86de-111">Требование</span><span class="sxs-lookup"><span data-stu-id="c86de-111">Requirement</span></span> | <span data-ttu-id="c86de-112">Значение</span><span class="sxs-lookup"><span data-stu-id="c86de-112">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="c86de-113">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="c86de-113">Minimum supported client</span></span><br/> | <span data-ttu-id="c86de-114">Только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="c86de-114">Windows XP \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="c86de-115">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="c86de-115">Minimum supported server</span></span><br/> | <span data-ttu-id="c86de-116">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="c86de-116">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="c86de-117">Header</span><span class="sxs-lookup"><span data-stu-id="c86de-117">Header</span></span><br/>                   | <dl> <span data-ttu-id="c86de-118"><dt>Шлдисп. h</dt></span><span class="sxs-lookup"><span data-stu-id="c86de-118"><dt>Shldisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="c86de-119">IDL</span><span class="sxs-lookup"><span data-stu-id="c86de-119">IDL</span></span><br/>                      | <dl> <span data-ttu-id="c86de-120"><dt>Шлдисп. idl</dt></span><span class="sxs-lookup"><span data-stu-id="c86de-120"><dt>Shldisp.idl</dt></span></span> </dl> |



 

 




