---
description: Возвращает имя пользователя, от имени которого предназначена регистрация сертификата.
ms.assetid: 7bd71944-f7dd-4c92-a71c-ecc5c0afd5b2
title: 'Метод Искрденр::'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCrdEnr.getUserName
- SCrdEnr.getUserName
api_type:
- COM
api_location:
- Scrdenrl.dll
ms.openlocfilehash: 51f551a704f3a98b932e646c95810f928e73bac7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104348505"
---
# <a name="iscrdenrgetusername-method"></a><span data-ttu-id="adb21-103">Метод Искрденр::</span><span class="sxs-lookup"><span data-stu-id="adb21-103">ISCrdEnr::getUserName method</span></span>

<span data-ttu-id="adb21-104">Метод **суперпользователя** извлекает имя пользователя, от имени которого предназначена регистрация сертификата.</span><span class="sxs-lookup"><span data-stu-id="adb21-104">The **getUserName** method retrieves the name of the user on whose behalf the certificate enrollment is intended.</span></span>

<span data-ttu-id="adb21-105">Перед вызовом этого метода необходимо указать имя пользователя в вызове [**искрденр:: селектусернаме**](iscrdenr-selectusername.md) или [**Искрденр:: сетусернаме**](iscrdenr-setusername.md).</span><span class="sxs-lookup"><span data-stu-id="adb21-105">Before calling this method, you must specify the user name in a call to [**ISCrdEnr::selectUserName**](iscrdenr-selectusername.md) or [**ISCrdEnr::setUserName**](iscrdenr-setusername.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="adb21-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="adb21-106">Syntax</span></span>


```C++
HRESULT getUserName(
  [in]  DWORD     dwFlags,
  [out] BSTR *pbstrUserName
);
```


```VB

SCrdEnr.getUserName( _
  ByVal dwFlags, _
  ByRef pbstrUserName _
)
```





## <a name="parameters"></a><span data-ttu-id="adb21-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="adb21-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="adb21-108">*dwFlags* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="adb21-108">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="adb21-109">Это значение должно быть либо нулевым (0), бросить \_ регистрацией \_ имени участника-пользователя \_ , либо бросить с \_ \_ \_ именем, совместимым с SAM \_ .</span><span class="sxs-lookup"><span data-stu-id="adb21-109">This value must be either zero (0), SCARD\_ENROLL\_UPN\_NAME, or SCARD\_ENROLL\_SAM\_COMPATIBLE\_NAME.</span></span>

<span data-ttu-id="adb21-110">Если это значение — бросить \_ Регистрация имени участника-пользователя, то функция @ \_ \_ **username** возвращает имя пользователя (UPN), например " someone@example.com ".</span><span class="sxs-lookup"><span data-stu-id="adb21-110">If this value is SCARD\_ENROLL\_UPN\_NAME, **getUserName** returns the user's Universal Principal Name (UPN), such as "someone@example.com".</span></span>

<span data-ttu-id="adb21-111">Если это значение равно бросить \_ зарегистрировать \_ SAM \_ \_ , метод возвращает имя ДИСПЕТЧЕРА доступа пользователя (SAM) в формате " \\ пользователь домена".</span><span class="sxs-lookup"><span data-stu-id="adb21-111">If this value is SCARD\_ENROLL\_SAM\_COMPATIBLE\_NAME, the method returns the user's security access manager (SAM) name in the format "DOMAIN\\USER".</span></span>

<span data-ttu-id="adb21-112">Если это значение равно нулю, метод возвращает имя UPN пользователя, если оно существует.</span><span class="sxs-lookup"><span data-stu-id="adb21-112">If this value is zero, the method returns the user's UPN name if it exists.</span></span> <span data-ttu-id="adb21-113">Если у пользователя нет имени UPN, метод возвращает имя пользователя SAM.</span><span class="sxs-lookup"><span data-stu-id="adb21-113">If the user does not have a UPN name, the method returns the user's SAM name.</span></span>

</dd> <dt>

<span data-ttu-id="adb21-114">*пбструсернаме* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="adb21-114">*pbstrUserName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="adb21-115">Указатель на строку, которая возвращает имя пользователя.</span><span class="sxs-lookup"><span data-stu-id="adb21-115">A pointer to a string that returns the name of the user.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="adb21-116">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="adb21-116">Return value</span></span>

### <a name="c"></a><span data-ttu-id="adb21-117">C++</span><span class="sxs-lookup"><span data-stu-id="adb21-117">C++</span></span>

<span data-ttu-id="adb21-118">Если метод завершается успешно, метод возвращает значение S \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="adb21-118">If the method succeeds, the method returns S\_OK.</span></span>

<span data-ttu-id="adb21-119">Если метод завершается с ошибкой, возвращается значение **HRESULT** , указывающее на ошибку.</span><span class="sxs-lookup"><span data-stu-id="adb21-119">If the method fails, it returns an **HRESULT** value that indicates the error.</span></span> <span data-ttu-id="adb21-120">Список распространенных кодов ошибок см. в разделе [Общие значения HRESULT](common-hresult-values.md).</span><span class="sxs-lookup"><span data-stu-id="adb21-120">For a list of common error codes, see [Common HRESULT Values](common-hresult-values.md).</span></span>

### <a name="vb"></a><span data-ttu-id="adb21-121">VB</span><span class="sxs-lookup"><span data-stu-id="adb21-121">VB</span></span>

<span data-ttu-id="adb21-122">Строка, представляющая имя пользователя.</span><span class="sxs-lookup"><span data-stu-id="adb21-122">String that represents the name of the user.</span></span>

## <a name="remarks"></a><span data-ttu-id="adb21-123">Комментарии</span><span class="sxs-lookup"><span data-stu-id="adb21-123">Remarks</span></span>

<span data-ttu-id="adb21-124">Можно указать имя пользователя, которому выдается [*смарт-карта*](../secgloss/s-gly.md) , вызвав либо [**Искрденр:: Сетусернаме**](iscrdenr-setusername.md) , либо [**искрденр:: селектусернаме**](iscrdenr-selectusername.md).</span><span class="sxs-lookup"><span data-stu-id="adb21-124">You can specify the name of the user to whom the [*smart card*](../secgloss/s-gly.md) is issued by calling either [**ISCrdEnr::setUserName**](iscrdenr-setusername.md) or [**ISCrdEnr::selectUserName**](iscrdenr-selectusername.md).</span></span> <span data-ttu-id="adb21-125">После указания имени пользователя его значение можно получить, вызвав метод **суперпользователя.**</span><span class="sxs-lookup"><span data-stu-id="adb21-125">After a user name has been specified, its value can be retrieved by calling **getUserName**.</span></span>

## <a name="requirements"></a><span data-ttu-id="adb21-126">Требования</span><span class="sxs-lookup"><span data-stu-id="adb21-126">Requirements</span></span>



| <span data-ttu-id="adb21-127">Требование</span><span class="sxs-lookup"><span data-stu-id="adb21-127">Requirement</span></span> | <span data-ttu-id="adb21-128">Значение</span><span class="sxs-lookup"><span data-stu-id="adb21-128">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="adb21-129">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="adb21-129">Minimum supported client</span></span><br/> | <span data-ttu-id="adb21-130">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="adb21-130">None supported</span></span><br/>                                                               |
| <span data-ttu-id="adb21-131">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="adb21-131">Minimum supported server</span></span><br/> | <span data-ttu-id="adb21-132">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="adb21-132">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="adb21-133">DLL</span><span class="sxs-lookup"><span data-stu-id="adb21-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="adb21-134"><dt>Scrdenrl.dll</dt></span><span class="sxs-lookup"><span data-stu-id="adb21-134"><dt>Scrdenrl.dll</dt></span></span> </dl> |
| <span data-ttu-id="adb21-135">IID</span><span class="sxs-lookup"><span data-stu-id="adb21-135">IID</span></span><br/>                      | <span data-ttu-id="adb21-136">IID \_ искрденр определен как 753988a1-1357-436d-9cf5-f089bdd67d64</span><span class="sxs-lookup"><span data-stu-id="adb21-136">IID\_ISCrdEnr is defined as 753988a1-1357-436d-9cf5-f089bdd67d64</span></span><br/>             |



## <a name="see-also"></a><span data-ttu-id="adb21-137">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="adb21-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="adb21-138">**искрденр**</span><span class="sxs-lookup"><span data-stu-id="adb21-138">**ISCrdEnr**</span></span>](iscrdenr.md)
</dt> <dt>

[<span data-ttu-id="adb21-139">**Искрденр:: Ресетусер**</span><span class="sxs-lookup"><span data-stu-id="adb21-139">**ISCrdEnr::resetUser**</span></span>](iscrdenr-resetuser.md)
</dt> <dt>

[<span data-ttu-id="adb21-140">**Искрденр:: Селектусернаме**</span><span class="sxs-lookup"><span data-stu-id="adb21-140">**ISCrdEnr::selectUserName**</span></span>](iscrdenr-selectusername.md)
</dt> <dt>

[<span data-ttu-id="adb21-141">**Искрденр:: Сетусернаме**</span><span class="sxs-lookup"><span data-stu-id="adb21-141">**ISCrdEnr::setUserName**</span></span>](iscrdenr-setusername.md)
</dt> </dl>

 

 
