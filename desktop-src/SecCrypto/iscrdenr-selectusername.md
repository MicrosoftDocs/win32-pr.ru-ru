---
description: Отображает пользовательский интерфейс выбора, позволяющий выбрать имя пользователя.
ms.assetid: 0a02d9e5-b2cf-4818-a2e1-89e6019e53d4
title: 'Метод Искрденр:: Селектусернаме'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCrdEnr.selectUserName
- SCrdEnr.selectUserName
api_type:
- COM
api_location:
- Scrdenrl.dll
ms.openlocfilehash: 13059775abc8520c39a0ad3dea2d604fc8d65455
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105664238"
---
# <a name="iscrdenrselectusername-method"></a><span data-ttu-id="3317a-103">Метод Искрденр:: Селектусернаме</span><span class="sxs-lookup"><span data-stu-id="3317a-103">ISCrdEnr::selectUserName method</span></span>

<span data-ttu-id="3317a-104">Метод **селектусернаме** отображает пользовательский интерфейс **выбора** , позволяющий выбрать имя пользователя.</span><span class="sxs-lookup"><span data-stu-id="3317a-104">The **selectUserName** method displays a **Select User** interface, allowing a user name to be selected.</span></span>

<span data-ttu-id="3317a-105">Имя пользователя применяется к пользователю, от имени которого предназначена регистрация сертификата.</span><span class="sxs-lookup"><span data-stu-id="3317a-105">The user name applies to the user on whose behalf the certificate enrollment is intended.</span></span>

## <a name="syntax"></a><span data-ttu-id="3317a-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="3317a-106">Syntax</span></span>


```C++
HRESULT selectUserName(
  [in] DWORD dwFlags
);
```


```VB

SCrdEnr.selectUserName( _
  ByVal dwFlags _
)
```





## <a name="parameters"></a><span data-ttu-id="3317a-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="3317a-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3317a-108">*dwFlags* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="3317a-108">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3317a-109">Зарезервировано для последующего использования.</span><span class="sxs-lookup"><span data-stu-id="3317a-109">Reserved for future use.</span></span> <span data-ttu-id="3317a-110">Присвойте этому параметру значение 0.</span><span class="sxs-lookup"><span data-stu-id="3317a-110">Set this value to zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3317a-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="3317a-111">Return value</span></span>

### <a name="vb"></a><span data-ttu-id="3317a-112">VB</span><span class="sxs-lookup"><span data-stu-id="3317a-112">VB</span></span>

<span data-ttu-id="3317a-113">Если метод завершается успешно, метод возвращает значение S \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="3317a-113">If the method succeeds, the method returns S\_OK.</span></span>

<span data-ttu-id="3317a-114">Если метод завершается с ошибкой, возвращается значение **HRESULT** , указывающее на ошибку.</span><span class="sxs-lookup"><span data-stu-id="3317a-114">If the method fails, it returns an **HRESULT** value that indicates the error.</span></span> <span data-ttu-id="3317a-115">Список распространенных кодов ошибок см. в разделе [Общие значения HRESULT](common-hresult-values.md).</span><span class="sxs-lookup"><span data-stu-id="3317a-115">For a list of common error codes, see [Common HRESULT Values](common-hresult-values.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="3317a-116">Комментарии</span><span class="sxs-lookup"><span data-stu-id="3317a-116">Remarks</span></span>

<span data-ttu-id="3317a-117">Используйте этот метод, чтобы выбрать имя пользователя.</span><span class="sxs-lookup"><span data-stu-id="3317a-117">Use this method to select the name of the user.</span></span> <span data-ttu-id="3317a-118">После выбора имени пользователя его значение можно получить, вызвав метод [**искрденр::-username**](iscrdenr-getusername.md) .</span><span class="sxs-lookup"><span data-stu-id="3317a-118">After a user name has been selected, its value can be retrieved by calling the [**ISCrdEnr::getUserName**](iscrdenr-getusername.md) method.</span></span>

<span data-ttu-id="3317a-119">Альтернативой использованию интерфейса "Выбор пользователя" является указание пользователя путем вызова метода [**искрденр:: сетусернаме**](iscrdenr-setusername.md) .</span><span class="sxs-lookup"><span data-stu-id="3317a-119">An alternative to using the 'Select User' interface is to specify a user by calling the [**ISCrdEnr::setUserName**](iscrdenr-setusername.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="3317a-120">Требования</span><span class="sxs-lookup"><span data-stu-id="3317a-120">Requirements</span></span>



| <span data-ttu-id="3317a-121">Требование</span><span class="sxs-lookup"><span data-stu-id="3317a-121">Requirement</span></span> | <span data-ttu-id="3317a-122">Значение</span><span class="sxs-lookup"><span data-stu-id="3317a-122">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="3317a-123">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="3317a-123">Minimum supported client</span></span><br/> | <span data-ttu-id="3317a-124">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="3317a-124">None supported</span></span><br/>                                                               |
| <span data-ttu-id="3317a-125">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="3317a-125">Minimum supported server</span></span><br/> | <span data-ttu-id="3317a-126">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="3317a-126">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="3317a-127">DLL</span><span class="sxs-lookup"><span data-stu-id="3317a-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3317a-128"><dt>Scrdenrl.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3317a-128"><dt>Scrdenrl.dll</dt></span></span> </dl> |
| <span data-ttu-id="3317a-129">IID</span><span class="sxs-lookup"><span data-stu-id="3317a-129">IID</span></span><br/>                      | <span data-ttu-id="3317a-130">IID \_ искрденр определен как 753988a1-1357-436d-9cf5-f089bdd67d64</span><span class="sxs-lookup"><span data-stu-id="3317a-130">IID\_ISCrdEnr is defined as 753988a1-1357-436d-9cf5-f089bdd67d64</span></span><br/>             |



## <a name="see-also"></a><span data-ttu-id="3317a-131">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="3317a-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3317a-132">**искрденр**</span><span class="sxs-lookup"><span data-stu-id="3317a-132">**ISCrdEnr**</span></span>](iscrdenr.md)
</dt> <dt>

[<span data-ttu-id="3317a-133">**Искрденр:: имя пользователя**</span><span class="sxs-lookup"><span data-stu-id="3317a-133">**ISCrdEnr::getUserName**</span></span>](iscrdenr-getusername.md)
</dt> <dt>

[<span data-ttu-id="3317a-134">**Искрденр:: Ресетусер**</span><span class="sxs-lookup"><span data-stu-id="3317a-134">**ISCrdEnr::resetUser**</span></span>](iscrdenr-resetuser.md)
</dt> <dt>

[<span data-ttu-id="3317a-135">**Искрденр:: Сетусернаме**</span><span class="sxs-lookup"><span data-stu-id="3317a-135">**ISCrdEnr::setUserName**</span></span>](iscrdenr-setusername.md)
</dt> </dl>

 

 




