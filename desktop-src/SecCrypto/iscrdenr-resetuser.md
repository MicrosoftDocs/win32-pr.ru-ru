---
description: Удаляет имя пользователя из элемента управления смарт-картой.
ms.assetid: fff50db5-0610-4985-94c6-96d7ce990219
title: 'Метод Искрденр:: Ресетусер'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCrdEnr.resetUser
- SCrdEnr.resetUser
api_type:
- COM
api_location:
- Scrdenrl.dll
ms.openlocfilehash: e3b00721229890f82b00e7e7a41ccb8796a81b98
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105664396"
---
# <a name="iscrdenrresetuser-method"></a><span data-ttu-id="d29e3-103">Метод Искрденр:: Ресетусер</span><span class="sxs-lookup"><span data-stu-id="d29e3-103">ISCrdEnr::resetUser method</span></span>

<span data-ttu-id="d29e3-104">Метод **ресетусер** удаляет имя пользователя из элемента управления смарт-картой.</span><span class="sxs-lookup"><span data-stu-id="d29e3-104">The **resetUser** method clears the user name from the smart card control.</span></span>

## <a name="syntax"></a><span data-ttu-id="d29e3-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="d29e3-105">Syntax</span></span>


```C++
HRESULT resetUser();
```



## <a name="parameters"></a><span data-ttu-id="d29e3-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="d29e3-106">Parameters</span></span>

<span data-ttu-id="d29e3-107">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="d29e3-107">This method has no parameters.</span></span>

## <a name="remarks"></a><span data-ttu-id="d29e3-108">Комментарии</span><span class="sxs-lookup"><span data-stu-id="d29e3-108">Remarks</span></span>

<span data-ttu-id="d29e3-109">Этот метод очищает все существующие имя пользователя и ранее зарегистрированный сертификат из памяти.</span><span class="sxs-lookup"><span data-stu-id="d29e3-109">This method clears any existing user name and previously enrolled certificate from memory.</span></span> <span data-ttu-id="d29e3-110">Однако ранее зарегистрированный сертификат не удаляется со смарт-карты.</span><span class="sxs-lookup"><span data-stu-id="d29e3-110">The previously enrolled certificate is not removed from the smart card, however.</span></span>

## <a name="requirements"></a><span data-ttu-id="d29e3-111">Требования</span><span class="sxs-lookup"><span data-stu-id="d29e3-111">Requirements</span></span>



| <span data-ttu-id="d29e3-112">Требование</span><span class="sxs-lookup"><span data-stu-id="d29e3-112">Requirement</span></span> | <span data-ttu-id="d29e3-113">Значение</span><span class="sxs-lookup"><span data-stu-id="d29e3-113">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d29e3-114">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="d29e3-114">Minimum supported client</span></span><br/> | <span data-ttu-id="d29e3-115">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="d29e3-115">None supported</span></span><br/>                                                               |
| <span data-ttu-id="d29e3-116">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="d29e3-116">Minimum supported server</span></span><br/> | <span data-ttu-id="d29e3-117">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="d29e3-117">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="d29e3-118">DLL</span><span class="sxs-lookup"><span data-stu-id="d29e3-118">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d29e3-119"><dt>Scrdenrl.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d29e3-119"><dt>Scrdenrl.dll</dt></span></span> </dl> |
| <span data-ttu-id="d29e3-120">IID</span><span class="sxs-lookup"><span data-stu-id="d29e3-120">IID</span></span><br/>                      | <span data-ttu-id="d29e3-121">IID \_ искрденр определен как 753988a1-1357-436d-9cf5-f089bdd67d64</span><span class="sxs-lookup"><span data-stu-id="d29e3-121">IID\_ISCrdEnr is defined as 753988a1-1357-436d-9cf5-f089bdd67d64</span></span><br/>             |



## <a name="see-also"></a><span data-ttu-id="d29e3-122">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="d29e3-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d29e3-123">**искрденр**</span><span class="sxs-lookup"><span data-stu-id="d29e3-123">**ISCrdEnr**</span></span>](iscrdenr.md)
</dt> <dt>

[<span data-ttu-id="d29e3-124">**Искрденр:: имя пользователя**</span><span class="sxs-lookup"><span data-stu-id="d29e3-124">**ISCrdEnr::getUserName**</span></span>](iscrdenr-getusername.md)
</dt> <dt>

[<span data-ttu-id="d29e3-125">**Искрденр:: Селектусернаме**</span><span class="sxs-lookup"><span data-stu-id="d29e3-125">**ISCrdEnr::selectUserName**</span></span>](iscrdenr-selectusername.md)
</dt> <dt>

[<span data-ttu-id="d29e3-126">**Искрденр:: Сетусернаме**</span><span class="sxs-lookup"><span data-stu-id="d29e3-126">**ISCrdEnr::setUserName**</span></span>](iscrdenr-setusername.md)
</dt> </dl>

 

 




