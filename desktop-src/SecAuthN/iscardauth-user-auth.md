---
description: '\_Метод проверки подлинности пользователя обеспечивает доступ к службам аутентификации пользователей.'
ms.assetid: 110da052-c581-46bc-8e81-5be112ee9b43
title: 'Метод Искардаус:: User_Auth'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardAuth.User_Auth
api_type:
- COM
api_location: ''
ms.openlocfilehash: ae810f93c322449109576b37f01afa4f277fc32f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103897174"
---
# <a name="iscardauthuser_auth-method"></a><span data-ttu-id="5a57d-103">\_Метод проверки подлинности искардаус:: User</span><span class="sxs-lookup"><span data-stu-id="5a57d-103">ISCardAuth::User\_Auth method</span></span>

<span data-ttu-id="5a57d-104">\[Метод **\_ проверки подлинности пользователя** доступен для использования в операционных системах, указанных в разделе требования.</span><span class="sxs-lookup"><span data-stu-id="5a57d-104">\[The **User\_Auth** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="5a57d-105">Он недоступен для использования в Windows Server 2003 с пакетом обновления 1 (SP1) и более поздней версии, Windows Vista, Windows Server 2008 и последующих версиях операционной системы.</span><span class="sxs-lookup"><span data-stu-id="5a57d-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="5a57d-106">[Модули смарт-карт](/previous-versions/windows/desktop/secsmart/smart-card-modules) предоставляют аналогичные функции.\]</span><span class="sxs-lookup"><span data-stu-id="5a57d-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="5a57d-107">Метод **\_ проверки** подлинности пользователя обеспечивает доступ к службам аутентификации пользователей.</span><span class="sxs-lookup"><span data-stu-id="5a57d-107">The **User\_Auth** method allows access to user authentication services.</span></span>

## <a name="syntax"></a><span data-ttu-id="5a57d-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="5a57d-108">Syntax</span></span>


```C++
HRESULT User_Auth(
  [in] LONG         lAlgorID,
  [in] LPBYTEBUFFER pParam,
  [in] LPBYTEBUFFER pBuffer
);
```



## <a name="parameters"></a><span data-ttu-id="5a57d-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="5a57d-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5a57d-110">*лалгорид* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="5a57d-110">*lAlgorID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5a57d-111">Алгоритм, используемый в процессе проверки подлинности.</span><span class="sxs-lookup"><span data-stu-id="5a57d-111">Algorithm to be used in the authentication process.</span></span>

</dd> <dt>

<span data-ttu-id="5a57d-112">*ппарам* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="5a57d-112">*pParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5a57d-113">Объект [**ибитебуффер**](ibytebuffer.md) , содержащий зависящие от поставщика параметры процесса проверки подлинности.</span><span class="sxs-lookup"><span data-stu-id="5a57d-113">An [**IByteBuffer**](ibytebuffer.md) object containing vendor-specific parameters of the authentication process.</span></span>

</dd> <dt>

<span data-ttu-id="5a57d-114">*pBuffer* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="5a57d-114">*pBuffer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5a57d-115">Данные, которые будут использоваться в процессе проверки подлинности.</span><span class="sxs-lookup"><span data-stu-id="5a57d-115">Data to be used in the authentication process.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5a57d-116">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="5a57d-116">Return value</span></span>

<span data-ttu-id="5a57d-117">Метод возвращает одно из следующих возможных значений.</span><span class="sxs-lookup"><span data-stu-id="5a57d-117">The method returns one of the following possible values.</span></span>



| <span data-ttu-id="5a57d-118">Код возврата</span><span class="sxs-lookup"><span data-stu-id="5a57d-118">Return code</span></span>                                                                                   | <span data-ttu-id="5a57d-119">Описание</span><span class="sxs-lookup"><span data-stu-id="5a57d-119">Description</span></span>                                  |
|-----------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="5a57d-120"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="5a57d-120"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="5a57d-121">Operation completed successfully (Операция выполнена успешно).</span><span class="sxs-lookup"><span data-stu-id="5a57d-121">Operation completed successfully.</span></span><br/> |
| <dl> <span data-ttu-id="5a57d-122"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="5a57d-122"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="5a57d-123">Недопустимый параметр.</span><span class="sxs-lookup"><span data-stu-id="5a57d-123">Invalid parameter.</span></span><br/>                |
| <dl> <span data-ttu-id="5a57d-124"><dt>**\_указатель E**</dt></span><span class="sxs-lookup"><span data-stu-id="5a57d-124"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="5a57d-125">Передан неверный указатель.</span><span class="sxs-lookup"><span data-stu-id="5a57d-125">A bad pointer was passed in.</span></span><br/>      |
| <dl> <span data-ttu-id="5a57d-126"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="5a57d-126"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="5a57d-127">Недостаточно памяти.</span><span class="sxs-lookup"><span data-stu-id="5a57d-127">Out of memory.</span></span><br/>                    |



 

## <a name="remarks"></a><span data-ttu-id="5a57d-128">Комментарии</span><span class="sxs-lookup"><span data-stu-id="5a57d-128">Remarks</span></span>

<span data-ttu-id="5a57d-129">Список всех методов, предоставляемых этим интерфейсом, см. в разделе [**искардаус**](iscardauth.md).</span><span class="sxs-lookup"><span data-stu-id="5a57d-129">For a list of all the methods provided by this interface, see [**ISCardAuth**](iscardauth.md).</span></span>

<span data-ttu-id="5a57d-130">Кроме приведенных выше кодов ошибок COM, этот интерфейс может возвращать код ошибки [*смарт-карты*](../secgloss/s-gly.md) , если для завершения запроса была вызвана функция смарт-карты.</span><span class="sxs-lookup"><span data-stu-id="5a57d-130">In addition to the COM error codes listed above, this interface may return a [*smart card*](../secgloss/s-gly.md) error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="5a57d-131">Дополнительные сведения см. в статье [возвращаемые значения смарт-карты](authentication-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="5a57d-131">For more information, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="5a57d-132">Требования</span><span class="sxs-lookup"><span data-stu-id="5a57d-132">Requirements</span></span>



| <span data-ttu-id="5a57d-133">Требование</span><span class="sxs-lookup"><span data-stu-id="5a57d-133">Requirement</span></span> | <span data-ttu-id="5a57d-134">Значение</span><span class="sxs-lookup"><span data-stu-id="5a57d-134">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="5a57d-135">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="5a57d-135">Minimum supported client</span></span><br/> | <span data-ttu-id="5a57d-136">Только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="5a57d-136">Windows XP \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="5a57d-137">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="5a57d-137">Minimum supported server</span></span><br/> | <span data-ttu-id="5a57d-138">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="5a57d-138">Windows Server 2003 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="5a57d-139">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="5a57d-139">End of client support</span></span><br/>    | <span data-ttu-id="5a57d-140">Windows XP</span><span class="sxs-lookup"><span data-stu-id="5a57d-140">Windows XP</span></span><br/>                                |
| <span data-ttu-id="5a57d-141">Поддержка конца сервера</span><span class="sxs-lookup"><span data-stu-id="5a57d-141">End of server support</span></span><br/>    | <span data-ttu-id="5a57d-142">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="5a57d-142">Windows Server 2003</span></span><br/>                       |



## <a name="see-also"></a><span data-ttu-id="5a57d-143">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="5a57d-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5a57d-144">**искардаус**</span><span class="sxs-lookup"><span data-stu-id="5a57d-144">**ISCardAuth**</span></span>](iscardauth.md)
</dt> <dt>

[<span data-ttu-id="5a57d-145">**ибитебуффер**</span><span class="sxs-lookup"><span data-stu-id="5a57d-145">**IByteBuffer**</span></span>](ibytebuffer.md)
</dt> </dl>

 

 
