---
description: Удаляет учетные данные пользователя, используемые для подключенного удостоверения.
ms.assetid: EB32832D-9A8C-4CEB-897A-7E9D24FF84DD
title: Функция Делетеконнектедидентити (Индентитисторе. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DeleteConnectedIdentity
api_type:
- HeaderDef
api_location:
- Indentitystore.h
ms.openlocfilehash: 8079985f916e996a56b4203ad6ad065c1b7664e3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104072626"
---
# <a name="deleteconnectedidentity-function"></a><span data-ttu-id="e05f0-103">Функция Делетеконнектедидентити</span><span class="sxs-lookup"><span data-stu-id="e05f0-103">DeleteConnectedIdentity function</span></span>

<span data-ttu-id="e05f0-104">Удаляет учетные данные пользователя, используемые для подключенного удостоверения.</span><span class="sxs-lookup"><span data-stu-id="e05f0-104">Deletes the user credential used for the connected identity.</span></span>

## <a name="syntax"></a><span data-ttu-id="e05f0-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="e05f0-105">Syntax</span></span>


```C++
SEC_ENTRY DeleteConnectedIdentity(
  _In_     PVOID  ProviderHandle,
  _In_opt_ HANDLE UserToken,
  _In_     PSID   UserSid,
  _In_     PWSTR  IdentityUserName
);
```



## <a name="parameters"></a><span data-ttu-id="e05f0-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="e05f0-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e05f0-107">*Провидерхандле* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="e05f0-107">*ProviderHandle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e05f0-108">Маркер поставщика удостоверений.</span><span class="sxs-lookup"><span data-stu-id="e05f0-108">Identity provider handle.</span></span>

</dd> <dt>

<span data-ttu-id="e05f0-109">*UserToken* \[ в необязательное\]</span><span class="sxs-lookup"><span data-stu-id="e05f0-109">*UserToken* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="e05f0-110">Токен подключенного пользователя, учетная запись которого будет преобразована в локальную учетную запись.</span><span class="sxs-lookup"><span data-stu-id="e05f0-110">Token of the connected user whose account is going to be converted to a local account.</span></span> <span data-ttu-id="e05f0-111">Если параметр *UserToken* не **равен null**, поставщик удостоверений использует этот токен для загрузки профиля пользователя и очистки подключенных состояний.</span><span class="sxs-lookup"><span data-stu-id="e05f0-111">If *UserToken* is not **NULL**, the identity provider uses this token to load the user profile and clean up connected states.</span></span> <span data-ttu-id="e05f0-112">Если параметр *UserToken* имеет **значение NULL**, LSA принудительно отменяет соединение.</span><span class="sxs-lookup"><span data-stu-id="e05f0-112">If *UserToken* is **NULL**, LSA is forcing the disconnection.</span></span> <span data-ttu-id="e05f0-113">Поставщик удостоверений должен очистить все глобальные подключенные состояния этого пользователя, но поставщику не нужно очищать подключенные состояния в профиле пользователя.</span><span class="sxs-lookup"><span data-stu-id="e05f0-113">The identity provider should clean up any global connected states on this user, but the provider does not have to clean up connected states in the user profile.</span></span>

</dd> <dt>

<span data-ttu-id="e05f0-114">О.  \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="e05f0-114">*UserSid* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e05f0-115">Основной идентификатор безопасности подключенного пользователя.</span><span class="sxs-lookup"><span data-stu-id="e05f0-115">The primary SID of the connected user.</span></span> <span data-ttu-id="e05f0-116">Если параметр *UserToken* имеет **значение, не равное NULL**, это идентификатор безопасности маркера.</span><span class="sxs-lookup"><span data-stu-id="e05f0-116">If *UserToken* is not **NULL**, this parameter is the user SID of the token.</span></span> <span data-ttu-id="e05f0-117">Если параметр *UserToken* имеет **значение NULL**, он используется для задания подключенного пользователя и очистки глобальных подключенных состояний этого пользователя.</span><span class="sxs-lookup"><span data-stu-id="e05f0-117">If *UserToken* is **NULL**, this parameter is used to identify the connected user and clean up global connected states of that user.</span></span>

</dd> <dt>

<span data-ttu-id="e05f0-118">*Идентитюсернаме* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="e05f0-118">*IdentityUserName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e05f0-119">Имя пользователя удостоверения.</span><span class="sxs-lookup"><span data-stu-id="e05f0-119">The user name of the identity.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e05f0-120">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="e05f0-120">Return value</span></span>

<span data-ttu-id="e05f0-121">Если функция завершается успешно, функция возвращает значение секунды \_ E \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="e05f0-121">If the function succeeds, the function returns SEC\_E\_OK.</span></span>

<span data-ttu-id="e05f0-122">Если функция завершается ошибкой, функция может вернуть один из следующих кодов ошибок.</span><span class="sxs-lookup"><span data-stu-id="e05f0-122">If the function fails, the function may return one of the following error codes.</span></span>



| <span data-ttu-id="e05f0-123">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="e05f0-123">Return value</span></span>                                                                                               | <span data-ttu-id="e05f0-124">Описание</span><span class="sxs-lookup"><span data-stu-id="e05f0-124">Description</span></span>                                                                                                                                                 |
|------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="e05f0-125"><dt>\_Недопустимый \_ параметр Status</dt></span><span class="sxs-lookup"><span data-stu-id="e05f0-125"><dt>STATUS\_INVALID\_PARAMETER</dt></span></span> </dl>      | <span data-ttu-id="e05f0-126">Недействительный параметр.</span><span class="sxs-lookup"><span data-stu-id="e05f0-126">A parameter is not valid.</span></span><br/>                                                                                                                        |
| <dl> <span data-ttu-id="e05f0-127"><dt>СОСТОЯНИЕ \_ нет \_ такого \_ пользователя</dt></span><span class="sxs-lookup"><span data-stu-id="e05f0-127"><dt>STATUS\_NO\_SUCH\_USER</dt></span></span> </dl>          | <span data-ttu-id="e05f0-128">Пользователь *, идентифицированный с помощью* ключа, не существует, не подключен, или отсутствует удостоверение, имя пользователя которого соответствует *идентитюсернаме*.</span><span class="sxs-lookup"><span data-stu-id="e05f0-128">The user identified by *UserSid* does not exist, is not currently connected, or there is no identity whose user name matches *IdentityUserName*.</span></span><br/> |
| <dl> <span data-ttu-id="e05f0-129"><dt>СОСТОЯНИЕ " \_ недостаточно \_ ресурсов"</dt></span><span class="sxs-lookup"><span data-stu-id="e05f0-129"><dt>STATUS\_INSUFFICIENT\_RESOURCES</dt></span></span> </dl> | <span data-ttu-id="e05f0-130">Недостаточно памяти для обработки запроса.</span><span class="sxs-lookup"><span data-stu-id="e05f0-130">There is not enough memory to process the request.</span></span><br/>                                                                                               |



 

## <a name="requirements"></a><span data-ttu-id="e05f0-131">Требования</span><span class="sxs-lookup"><span data-stu-id="e05f0-131">Requirements</span></span>



| <span data-ttu-id="e05f0-132">Требование</span><span class="sxs-lookup"><span data-stu-id="e05f0-132">Requirement</span></span> | <span data-ttu-id="e05f0-133">Значение</span><span class="sxs-lookup"><span data-stu-id="e05f0-133">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="e05f0-134">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="e05f0-134">Minimum supported client</span></span><br/> | <span data-ttu-id="e05f0-135">\[Только классические приложения Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="e05f0-135">Windows 8 \[desktop apps only\]</span></span><br/>                                                  |
| <span data-ttu-id="e05f0-136">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="e05f0-136">Minimum supported server</span></span><br/> | <span data-ttu-id="e05f0-137">\[Только для настольных приложений Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="e05f0-137">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="e05f0-138">Header</span><span class="sxs-lookup"><span data-stu-id="e05f0-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="e05f0-139"><dt>Индентитисторе. h</dt></span><span class="sxs-lookup"><span data-stu-id="e05f0-139"><dt>Indentitystore.h</dt></span></span> </dl> |



 

 




