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
ms.openlocfilehash: 704efbd4aae5a98ec01d8bd900e226144d25833d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103910459"
---
# <a name="webwizardhostfinalback-method"></a><span data-ttu-id="351b5-103">Вебвизардхост. Финалбакк, метод</span><span class="sxs-lookup"><span data-stu-id="351b5-103">WebWizardHost.FinalBack method</span></span>

<span data-ttu-id="351b5-104">Переход к странице на стороне клиента, непосредственно предшествующей странице, на которой размещены HTML-страницы на стороне сервера.</span><span class="sxs-lookup"><span data-stu-id="351b5-104">Navigates to the client-side page immediately preceding the page hosting the server-side HTML pages.</span></span>

## <a name="syntax"></a><span data-ttu-id="351b5-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="351b5-105">Syntax</span></span>


```JScript
iRetVal = WebWizardHost.FinalBack()
```



## <a name="parameters"></a><span data-ttu-id="351b5-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="351b5-106">Parameters</span></span>

<span data-ttu-id="351b5-107">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="351b5-107">This method has no parameters.</span></span>

## <a name="remarks"></a><span data-ttu-id="351b5-108">Примечания</span><span class="sxs-lookup"><span data-stu-id="351b5-108">Remarks</span></span>

<span data-ttu-id="351b5-109">Когда мастер отображает первую страницу на стороне сервера и пользователь нажимает кнопку « **назад** », сервер вызывает **финалбакк** при уведомлении этого события обработчиком событий клиента.</span><span class="sxs-lookup"><span data-stu-id="351b5-109">When the wizard displays the first server-side page and the user clicks the **Back** button, the server invokes **FinalBack** when notified of that event by the client's event handler.</span></span>

## <a name="requirements"></a><span data-ttu-id="351b5-110">Требования</span><span class="sxs-lookup"><span data-stu-id="351b5-110">Requirements</span></span>



| <span data-ttu-id="351b5-111">Требование</span><span class="sxs-lookup"><span data-stu-id="351b5-111">Requirement</span></span> | <span data-ttu-id="351b5-112">Значение</span><span class="sxs-lookup"><span data-stu-id="351b5-112">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="351b5-113">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="351b5-113">Minimum supported client</span></span><br/> | <span data-ttu-id="351b5-114">Только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="351b5-114">Windows XP \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="351b5-115">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="351b5-115">Minimum supported server</span></span><br/> | <span data-ttu-id="351b5-116">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="351b5-116">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="351b5-117">Header</span><span class="sxs-lookup"><span data-stu-id="351b5-117">Header</span></span><br/>                   | <dl> <span data-ttu-id="351b5-118"><dt>Шлдисп. h</dt></span><span class="sxs-lookup"><span data-stu-id="351b5-118"><dt>Shldisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="351b5-119">IDL</span><span class="sxs-lookup"><span data-stu-id="351b5-119">IDL</span></span><br/>                      | <dl> <span data-ttu-id="351b5-120"><dt>Шлдисп. idl</dt></span><span class="sxs-lookup"><span data-stu-id="351b5-120"><dt>Shldisp.idl</dt></span></span> </dl> |



 

 




