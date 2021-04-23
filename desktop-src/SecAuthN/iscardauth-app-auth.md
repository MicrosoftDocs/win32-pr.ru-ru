---
description: Метод проверки подлинности приложения \_ выполняет аутентификацию приложения. Это позволяет приложению пройти проверку подлинности (с помощью протокола вызова и подписи), когда на смарт-карте запрашивается проверка подлинности.
ms.assetid: 0b86ce09-ca17-4d74-bc14-46b17262e669
title: 'Метод Искардаус:: APP_Auth'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardAuth.APP_Auth
api_type:
- COM
api_location: ''
ms.openlocfilehash: 792cd1b43a43f020e62e87048741935a82da28dd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103898301"
---
# <a name="iscardauthapp_auth-method"></a><span data-ttu-id="0097c-104">\_Метод проверки подлинности искардаус:: App</span><span class="sxs-lookup"><span data-stu-id="0097c-104">ISCardAuth::APP\_Auth method</span></span>

<span data-ttu-id="0097c-105">\[Метод **\_ проверки подлинности приложения** доступен для использования в операционных системах, указанных в разделе требования.</span><span class="sxs-lookup"><span data-stu-id="0097c-105">\[The **APP\_Auth** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="0097c-106">Он недоступен для использования в Windows Server 2003 с пакетом обновления 1 (SP1) и более поздней версии, Windows Vista, Windows Server 2008 и последующих версиях операционной системы.</span><span class="sxs-lookup"><span data-stu-id="0097c-106">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="0097c-107">[Модули смарт-карт](/previous-versions/windows/desktop/secsmart/smart-card-modules) предоставляют аналогичные функции.\]</span><span class="sxs-lookup"><span data-stu-id="0097c-107">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="0097c-108">Метод **\_ проверки** подлинности приложения выполняет аутентификацию приложения.</span><span class="sxs-lookup"><span data-stu-id="0097c-108">The **APP\_Auth** method authenticates the application.</span></span> <span data-ttu-id="0097c-109">Это позволяет приложению пройти проверку подлинности (с помощью протокола вызова и подписи), когда на [*смарт-карте*](../secgloss/s-gly.md)запрашивается проверка подлинности.</span><span class="sxs-lookup"><span data-stu-id="0097c-109">It allows an application to authenticate itself (using a challenge/signature protocol) when authentication is requested by a [*smart card*](../secgloss/s-gly.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="0097c-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="0097c-110">Syntax</span></span>


```C++
HRESULT APP_Auth(
  [in] LONG         lAlgoID,
  [in] LPBYTEBUFFER pParam,
  [in] LPBYTEBUFFER pBuffer
);
```



## <a name="parameters"></a><span data-ttu-id="0097c-111">Параметры</span><span class="sxs-lookup"><span data-stu-id="0097c-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0097c-112">*лалгоид* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="0097c-112">*lAlgoID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0097c-113">Алгоритм, используемый в процессе проверки подлинности.</span><span class="sxs-lookup"><span data-stu-id="0097c-113">Algorithm to be used in the authentication process.</span></span>

</dd> <dt>

<span data-ttu-id="0097c-114">*ппарам* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="0097c-114">*pParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0097c-115">[**Ибитебуффер**](ibytebuffer.md) , содержащий параметры процесса проверки подлинности, зависящие от поставщика.</span><span class="sxs-lookup"><span data-stu-id="0097c-115">An [**IByteBuffer**](ibytebuffer.md) containing vendor-specific parameters of the authentication process.</span></span>

</dd> <dt>

<span data-ttu-id="0097c-116">*pBuffer* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="0097c-116">*pBuffer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0097c-117">Данные, необходимые для вычисления.</span><span class="sxs-lookup"><span data-stu-id="0097c-117">Data required for the calculation.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0097c-118">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="0097c-118">Return value</span></span>

<span data-ttu-id="0097c-119">Метод возвращает одно из следующих возможных значений.</span><span class="sxs-lookup"><span data-stu-id="0097c-119">The method returns one of the following possible values.</span></span>



| <span data-ttu-id="0097c-120">Код возврата</span><span class="sxs-lookup"><span data-stu-id="0097c-120">Return code</span></span>                                                                                   | <span data-ttu-id="0097c-121">Описание</span><span class="sxs-lookup"><span data-stu-id="0097c-121">Description</span></span>                                  |
|-----------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="0097c-122"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="0097c-122"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="0097c-123">Operation completed successfully (Операция выполнена успешно).</span><span class="sxs-lookup"><span data-stu-id="0097c-123">Operation completed successfully.</span></span><br/> |
| <dl> <span data-ttu-id="0097c-124"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="0097c-124"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="0097c-125">Недопустимый параметр.</span><span class="sxs-lookup"><span data-stu-id="0097c-125">Invalid parameter.</span></span><br/>                |
| <dl> <span data-ttu-id="0097c-126"><dt>**\_указатель E**</dt></span><span class="sxs-lookup"><span data-stu-id="0097c-126"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="0097c-127">Передан неверный указатель.</span><span class="sxs-lookup"><span data-stu-id="0097c-127">A bad pointer was passed in.</span></span><br/>      |
| <dl> <span data-ttu-id="0097c-128"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="0097c-128"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="0097c-129">Недостаточно памяти.</span><span class="sxs-lookup"><span data-stu-id="0097c-129">Out of memory.</span></span><br/>                    |



 

## <a name="remarks"></a><span data-ttu-id="0097c-130">Комментарии</span><span class="sxs-lookup"><span data-stu-id="0097c-130">Remarks</span></span>

<span data-ttu-id="0097c-131">Список всех методов, предоставляемых этим интерфейсом, см. в разделе [**искардаус**](iscardauth.md).</span><span class="sxs-lookup"><span data-stu-id="0097c-131">For a list of all the methods provided by this interface, see [**ISCardAuth**](iscardauth.md).</span></span>

<span data-ttu-id="0097c-132">Кроме приведенных выше кодов ошибок COM, этот интерфейс может возвращать код ошибки смарт-карты, если для завершения запроса была вызвана функция смарт-карты.</span><span class="sxs-lookup"><span data-stu-id="0097c-132">In addition to the COM error codes listed above, this interface may return a smart card error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="0097c-133">Дополнительные сведения см. в статье [возвращаемые значения смарт-карты](authentication-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="0097c-133">For more information, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="0097c-134">Требования</span><span class="sxs-lookup"><span data-stu-id="0097c-134">Requirements</span></span>



| <span data-ttu-id="0097c-135">Требование</span><span class="sxs-lookup"><span data-stu-id="0097c-135">Requirement</span></span> | <span data-ttu-id="0097c-136">Значение</span><span class="sxs-lookup"><span data-stu-id="0097c-136">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="0097c-137">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="0097c-137">Minimum supported client</span></span><br/> | <span data-ttu-id="0097c-138">Только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="0097c-138">Windows XP \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="0097c-139">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="0097c-139">Minimum supported server</span></span><br/> | <span data-ttu-id="0097c-140">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="0097c-140">Windows Server 2003 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="0097c-141">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="0097c-141">End of client support</span></span><br/>    | <span data-ttu-id="0097c-142">Windows XP</span><span class="sxs-lookup"><span data-stu-id="0097c-142">Windows XP</span></span><br/>                                |
| <span data-ttu-id="0097c-143">Поддержка конца сервера</span><span class="sxs-lookup"><span data-stu-id="0097c-143">End of server support</span></span><br/>    | <span data-ttu-id="0097c-144">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="0097c-144">Windows Server 2003</span></span><br/>                       |



## <a name="see-also"></a><span data-ttu-id="0097c-145">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="0097c-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0097c-146">**искардаус**</span><span class="sxs-lookup"><span data-stu-id="0097c-146">**ISCardAuth**</span></span>](iscardauth.md)
</dt> <dt>

[<span data-ttu-id="0097c-147">**ибитебуффер**</span><span class="sxs-lookup"><span data-stu-id="0097c-147">**IByteBuffer**</span></span>](ibytebuffer.md)
</dt> </dl>

 

 
