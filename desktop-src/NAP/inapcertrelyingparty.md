---
title: Интерфейс Инапцертрелингпарти (Напцертрелингпарти. h)
description: Проверяющие стороны сертификатов должны использовать для связи с Напажент.
ms.assetid: e5ae0f4d-24fa-4049-82d9-1c9baeb34e32
keywords:
- Инапцертрелингпарти интерфейса NAP
- Инапцертрелингпарти интерфейс NAP, описание
topic_type:
- apiref
api_name:
- INapCertRelyingParty
api_location:
- NapCertRelyingParty.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 85b4439389c6ee65076f710bb6ea752c73a51ecd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104071795"
---
# <a name="inapcertrelyingparty-interface"></a><span data-ttu-id="be9a5-105">Интерфейс Инапцертрелингпарти</span><span class="sxs-lookup"><span data-stu-id="be9a5-105">INapCertRelyingParty interface</span></span>

> [!Note]  
> <span data-ttu-id="be9a5-106">Платформа защиты доступа к сети недоступна начиная с Windows 10</span><span class="sxs-lookup"><span data-stu-id="be9a5-106">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="be9a5-107">Интерфейс **инапцертрелингпарти** предоставляет методы, которые проверяющие стороны сертификатов должны использовать для взаимодействия с напажент.</span><span class="sxs-lookup"><span data-stu-id="be9a5-107">The **INapCertRelyingParty** interface provides methods that certificate-relying parties must use to communicate with the NapAgent.</span></span>

## <a name="members"></a><span data-ttu-id="be9a5-108">Элементы</span><span class="sxs-lookup"><span data-stu-id="be9a5-108">Members</span></span>

<span data-ttu-id="be9a5-109">Интерфейс **инапцертрелингпарти** наследует от интерфейса [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="be9a5-109">The **INapCertRelyingParty** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="be9a5-110">**Инапцертрелингпарти** также имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="be9a5-110">**INapCertRelyingParty** also has these types of members:</span></span>

-   [<span data-ttu-id="be9a5-111">Методы</span><span class="sxs-lookup"><span data-stu-id="be9a5-111">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="be9a5-112">Методы</span><span class="sxs-lookup"><span data-stu-id="be9a5-112">Methods</span></span>

<span data-ttu-id="be9a5-113">Интерфейс **инапцертрелингпарти** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="be9a5-113">The **INapCertRelyingParty** interface has these methods.</span></span>



| <span data-ttu-id="be9a5-114">Метод</span><span class="sxs-lookup"><span data-stu-id="be9a5-114">Method</span></span>                                                                                                        | <span data-ttu-id="be9a5-115">Описание</span><span class="sxs-lookup"><span data-stu-id="be9a5-115">Description</span></span>                                                                     |
|:--------------------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------|
| [<span data-ttu-id="be9a5-116">**Инапцертрелингпарти:: Жетсубскрибедрелингпартиес**</span><span class="sxs-lookup"><span data-stu-id="be9a5-116">**INapCertRelyingParty::GetSubscribedRelyingParties**</span></span>](inapcertrelyingparty-getsubscribedrelyingparties.md) | <span data-ttu-id="be9a5-117">Возвращает список проверяющих сторон, на которые оформлена подписка.</span><span class="sxs-lookup"><span data-stu-id="be9a5-117">Gets a list of relying parties that have subscribed.</span></span><br/>                 |
| [<span data-ttu-id="be9a5-118">**Инапцертрелингпарти:: Субскрибецертбиграуп**</span><span class="sxs-lookup"><span data-stu-id="be9a5-118">**INapCertRelyingParty::SubscribeCertByGroup**</span></span>](inapcertrelyingparty-subscribecertbygroup.md)               | <span data-ttu-id="be9a5-119">Подписывается на уже зарегистрированный сервер сертификатов работоспособности (HCS).</span><span class="sxs-lookup"><span data-stu-id="be9a5-119">Subscribes to an already-registered health certificate server (HCS).</span></span><br/> |
| [<span data-ttu-id="be9a5-120">**Инапцертрелингпарти:: Унсубскрибецертбиграуп**</span><span class="sxs-lookup"><span data-stu-id="be9a5-120">**INapCertRelyingParty::UnSubscribeCertByGroup**</span></span>](inapcertrelyingparty-unsubscribecertbygroup.md)           | <span data-ttu-id="be9a5-121">Отменяет Подписывание сервера HCS.</span><span class="sxs-lookup"><span data-stu-id="be9a5-121">Unsubscribes from an HCS server.</span></span><br/>                                     |



 

## <a name="requirements"></a><span data-ttu-id="be9a5-122">Требования</span><span class="sxs-lookup"><span data-stu-id="be9a5-122">Requirements</span></span>



| <span data-ttu-id="be9a5-123">Требование</span><span class="sxs-lookup"><span data-stu-id="be9a5-123">Requirement</span></span> | <span data-ttu-id="be9a5-124">Значение</span><span class="sxs-lookup"><span data-stu-id="be9a5-124">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="be9a5-125">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="be9a5-125">Minimum supported client</span></span><br/> | <span data-ttu-id="be9a5-126">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="be9a5-126">Windows Vista \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="be9a5-127">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="be9a5-127">Minimum supported server</span></span><br/> | <span data-ttu-id="be9a5-128">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="be9a5-128">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="be9a5-129">Header</span><span class="sxs-lookup"><span data-stu-id="be9a5-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="be9a5-130"><dt>Напцертрелингпарти. h</dt></span><span class="sxs-lookup"><span data-stu-id="be9a5-130"><dt>NapCertRelyingParty.h</dt></span></span> </dl>   |
| <span data-ttu-id="be9a5-131">IDL</span><span class="sxs-lookup"><span data-stu-id="be9a5-131">IDL</span></span><br/>                      | <dl> <span data-ttu-id="be9a5-132"><dt>Напцертрелингпарти. idl</dt></span><span class="sxs-lookup"><span data-stu-id="be9a5-132"><dt>NapCertRelyingParty.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="be9a5-133">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="be9a5-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="be9a5-134">Интерфейсы NAP</span><span class="sxs-lookup"><span data-stu-id="be9a5-134">NAP Interfaces</span></span>](nap-interfaces.md)
</dt> <dt>

[<span data-ttu-id="be9a5-135">Справочник по NAP</span><span class="sxs-lookup"><span data-stu-id="be9a5-135">NAP Reference</span></span>](nap-reference.md)
</dt> </dl>

 

