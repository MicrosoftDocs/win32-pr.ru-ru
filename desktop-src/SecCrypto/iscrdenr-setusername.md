---
description: Указывает имя пользователя, от имени которого предназначена регистрация сертификата.
ms.assetid: e088af63-5064-4b1b-976f-047f52e56af8
title: 'Метод Искрденр:: Сетусернаме'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCrdEnr.setUserName
- SCrdEnr.setUserName
api_type:
- COM
api_location:
- Scrdenrl.dll
ms.openlocfilehash: cc2d3157e41fc7ffd9fc0bf7f607de137559e751
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105684580"
---
# <a name="iscrdenrsetusername-method"></a><span data-ttu-id="74b1a-103">Метод Искрденр:: Сетусернаме</span><span class="sxs-lookup"><span data-stu-id="74b1a-103">ISCrdEnr::setUserName method</span></span>

<span data-ttu-id="74b1a-104">Метод **сетусернаме** указывает имя пользователя, от имени которого предназначена регистрация сертификата.</span><span class="sxs-lookup"><span data-stu-id="74b1a-104">The **setUserName** method specifies the name of the user on whose behalf the certificate enrollment is intended.</span></span>

## <a name="syntax"></a><span data-ttu-id="74b1a-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="74b1a-105">Syntax</span></span>


```C++
HRESULT setUserName(
  [in] DWORD dwFlags,
  [in] BSTR bstrUserName
);
```


```VB

SCrdEnr.setUserName( _
  ByVal dwFlags, _
  ByVal bstrUserName _
)
```





## <a name="parameters"></a><span data-ttu-id="74b1a-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="74b1a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="74b1a-107">*dwFlags* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="74b1a-107">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="74b1a-108">Это значение должно быть либо бросить \_ Регистрация \_ \_ имени участника-пользователя (определяется как 1), либо бросить с \_ именем, \_ \_ совместимым \_ с SAM (определяется как 2).</span><span class="sxs-lookup"><span data-stu-id="74b1a-108">This value must be either SCARD\_ENROLL\_UPN\_NAME (defined as 1) or SCARD\_ENROLL\_SAM\_COMPATIBLE\_NAME (defined as 2).</span></span>

<span data-ttu-id="74b1a-109">Присвойте этому параметру значение бросить \_ Регистрация \_ \_ имени участника-пользователя, если имя, указанное в *бструсернаме* , является универсальным именем участника, например " someone@example.com ".</span><span class="sxs-lookup"><span data-stu-id="74b1a-109">Set this value to SCARD\_ENROLL\_UPN\_NAME, if the name specified in *bstrUserName* is the user's Universal Principal Name, such as "someone@example.com".</span></span> <span data-ttu-id="74b1a-110">Имя участника-пользователя должно соответствовать существующему имени диспетчера доступа безопасности (SAM).</span><span class="sxs-lookup"><span data-stu-id="74b1a-110">The user's UPN name must correspond to an existing security access manager (SAM) name.</span></span>

<span data-ttu-id="74b1a-111">Присвойте этому параметру значение бросить \_ \_ \_ , совместимое с SAM \_ , если имя пользователя, указанное в *бструсернаме* , является именем SAM в формате " \\ пользователь домена".</span><span class="sxs-lookup"><span data-stu-id="74b1a-111">Set this value to SCARD\_ENROLL\_SAM\_COMPATIBLE\_NAME, if the name specified in *bstrUserName* is the user's SAM name in the format of "DOMAIN\\USER".</span></span>

</dd> <dt>

<span data-ttu-id="74b1a-112">*бструсернаме* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="74b1a-112">*bstrUserName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="74b1a-113">Имя пользователя.</span><span class="sxs-lookup"><span data-stu-id="74b1a-113">Name of the user.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="74b1a-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="74b1a-114">Return value</span></span>

### <a name="vb"></a><span data-ttu-id="74b1a-115">VB</span><span class="sxs-lookup"><span data-stu-id="74b1a-115">VB</span></span>

<span data-ttu-id="74b1a-116">Если метод завершается успешно, метод возвращает значение S \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="74b1a-116">If the method succeeds, the method returns S\_OK.</span></span>

<span data-ttu-id="74b1a-117">Если метод завершается с ошибкой, возвращается значение **HRESULT** , указывающее на ошибку.</span><span class="sxs-lookup"><span data-stu-id="74b1a-117">If the method fails, it returns an **HRESULT** value that indicates the error.</span></span> <span data-ttu-id="74b1a-118">Список распространенных кодов ошибок см. в разделе [Общие значения HRESULT](common-hresult-values.md).</span><span class="sxs-lookup"><span data-stu-id="74b1a-118">For a list of common error codes, see [Common HRESULT Values](common-hresult-values.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="74b1a-119">Комментарии</span><span class="sxs-lookup"><span data-stu-id="74b1a-119">Remarks</span></span>

<span data-ttu-id="74b1a-120">Вызовите этот метод, чтобы указать имя пользователя для выдачи [*смарт-карты*](../secgloss/s-gly.md).</span><span class="sxs-lookup"><span data-stu-id="74b1a-120">Call this method to specify the user name to be issued the [*smart card*](../secgloss/s-gly.md).</span></span> <span data-ttu-id="74b1a-121">Альтернативой для **сетусернаме** является [**Искрденр:: селектусернаме**](iscrdenr-selectusername.md).</span><span class="sxs-lookup"><span data-stu-id="74b1a-121">An alternative to **setUserName** is [**ISCrdEnr::selectUserName**](iscrdenr-selectusername.md).</span></span>

<span data-ttu-id="74b1a-122">После указания имени пользователя его значение можно получить, вызвав метод [**суперпользователя.**](iscrdenr-getusername.md)</span><span class="sxs-lookup"><span data-stu-id="74b1a-122">After a user name has been specified, its value can be retrieved by calling [**getUserName**](iscrdenr-getusername.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="74b1a-123">Требования</span><span class="sxs-lookup"><span data-stu-id="74b1a-123">Requirements</span></span>



| <span data-ttu-id="74b1a-124">Требование</span><span class="sxs-lookup"><span data-stu-id="74b1a-124">Requirement</span></span> | <span data-ttu-id="74b1a-125">Значение</span><span class="sxs-lookup"><span data-stu-id="74b1a-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="74b1a-126">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="74b1a-126">Minimum supported client</span></span><br/> | <span data-ttu-id="74b1a-127">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="74b1a-127">None supported</span></span><br/>                                                               |
| <span data-ttu-id="74b1a-128">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="74b1a-128">Minimum supported server</span></span><br/> | <span data-ttu-id="74b1a-129">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="74b1a-129">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="74b1a-130">DLL</span><span class="sxs-lookup"><span data-stu-id="74b1a-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="74b1a-131"><dt>Scrdenrl.dll</dt></span><span class="sxs-lookup"><span data-stu-id="74b1a-131"><dt>Scrdenrl.dll</dt></span></span> </dl> |
| <span data-ttu-id="74b1a-132">IID</span><span class="sxs-lookup"><span data-stu-id="74b1a-132">IID</span></span><br/>                      | <span data-ttu-id="74b1a-133">IID \_ искрденр определен как 753988a1-1357-436d-9cf5-f089bdd67d64</span><span class="sxs-lookup"><span data-stu-id="74b1a-133">IID\_ISCrdEnr is defined as 753988a1-1357-436d-9cf5-f089bdd67d64</span></span><br/>             |



## <a name="see-also"></a><span data-ttu-id="74b1a-134">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="74b1a-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="74b1a-135">**искрденр**</span><span class="sxs-lookup"><span data-stu-id="74b1a-135">**ISCrdEnr**</span></span>](iscrdenr.md)
</dt> <dt>

[<span data-ttu-id="74b1a-136">**Искрденр:: имя пользователя**</span><span class="sxs-lookup"><span data-stu-id="74b1a-136">**ISCrdEnr::getUserName**</span></span>](iscrdenr-getusername.md)
</dt> <dt>

[<span data-ttu-id="74b1a-137">**Искрденр:: Ресетусер**</span><span class="sxs-lookup"><span data-stu-id="74b1a-137">**ISCrdEnr::resetUser**</span></span>](iscrdenr-resetuser.md)
</dt> <dt>

[<span data-ttu-id="74b1a-138">**Искрденр:: Селектусернаме**</span><span class="sxs-lookup"><span data-stu-id="74b1a-138">**ISCrdEnr::selectUserName**</span></span>](iscrdenr-selectusername.md)
</dt> </dl>

 

 
