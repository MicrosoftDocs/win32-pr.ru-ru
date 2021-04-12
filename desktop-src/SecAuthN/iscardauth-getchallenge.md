---
description: Метод метода WebMethod возвращает запрос со смарт-карты.
ms.assetid: a114ebfd-831f-4c6b-8156-ce631a732c9b
title: 'Метод Искардаус:: Challenge'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardAuth.GetChallenge
api_type:
- COM
api_location: ''
ms.openlocfilehash: 9282c0a922a1f8c8daff07c31dcafa7e47e923a7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104263588"
---
# <a name="iscardauthgetchallenge-method"></a><span data-ttu-id="1a8dc-103">Метод Искардаус:: Challenge</span><span class="sxs-lookup"><span data-stu-id="1a8dc-103">ISCardAuth::GetChallenge method</span></span>

<span data-ttu-id="1a8dc-104">\[Метод **метода** WebMethod доступен для использования в операционных системах, указанных в разделе требования.</span><span class="sxs-lookup"><span data-stu-id="1a8dc-104">\[The **GetChallenge** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="1a8dc-105">Он недоступен для использования в Windows Server 2003 с пакетом обновления 1 (SP1) и более поздней версии, Windows Vista, Windows Server 2008 и последующих версиях операционной системы.</span><span class="sxs-lookup"><span data-stu-id="1a8dc-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="1a8dc-106">[Модули смарт-карт](/previous-versions/windows/desktop/secsmart/smart-card-modules) предоставляют аналогичные функции.\]</span><span class="sxs-lookup"><span data-stu-id="1a8dc-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="1a8dc-107">Метод **метода WebMethod возвращает запрос со** [*смарт-карты*](../secgloss/s-gly.md).</span><span class="sxs-lookup"><span data-stu-id="1a8dc-107">The **GetChallenge** method returns a challenge from the [*smart card*](../secgloss/s-gly.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="1a8dc-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="1a8dc-108">Syntax</span></span>


```C++
HRESULT GetChallenge(
  [in, optional] LONG         lAlgoID,
  [in]           LONG         lLengthOfChallenge,
  [in]           LPBYTEBUFFER pParam,
  [in, out]      LPBYTEBUFFER *pBuffer
);
```



## <a name="parameters"></a><span data-ttu-id="1a8dc-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="1a8dc-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1a8dc-110">*лалгоид* \[ в необязательное\]</span><span class="sxs-lookup"><span data-stu-id="1a8dc-110">*lAlgoID* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="1a8dc-111">Алгоритм, используемый в процессе проверки подлинности.</span><span class="sxs-lookup"><span data-stu-id="1a8dc-111">Algorithm to be used in the authentication process.</span></span>

</dd> <dt>

<span data-ttu-id="1a8dc-112">*лленгсофчалленже* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="1a8dc-112">*lLengthOfChallenge* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1a8dc-113">Максимальная длина ожидаемого ответа.</span><span class="sxs-lookup"><span data-stu-id="1a8dc-113">Maximum length of expected response.</span></span>

</dd> <dt>

<span data-ttu-id="1a8dc-114">*ппарам* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="1a8dc-114">*pParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1a8dc-115">Объект [**ибитебуффер**](ibytebuffer.md) , содержащий зависящие от поставщика параметры процесса проверки подлинности.</span><span class="sxs-lookup"><span data-stu-id="1a8dc-115">An [**IByteBuffer**](ibytebuffer.md) object containing vendor-specific parameters of the authentication process.</span></span>

</dd> <dt>

<span data-ttu-id="1a8dc-116">*pBuffer* \[ в, out\]</span><span class="sxs-lookup"><span data-stu-id="1a8dc-116">*pBuffer* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="1a8dc-117">На входе указывает на буфер.</span><span class="sxs-lookup"><span data-stu-id="1a8dc-117">On input, points to the buffer.</span></span>

<span data-ttu-id="1a8dc-118">На выходе содержит данные запроса из карточки.</span><span class="sxs-lookup"><span data-stu-id="1a8dc-118">On output, contains the challenge data from the card.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1a8dc-119">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="1a8dc-119">Return value</span></span>

<span data-ttu-id="1a8dc-120">Метод возвращает одно из следующих возможных значений.</span><span class="sxs-lookup"><span data-stu-id="1a8dc-120">The method returns one of the following possible values.</span></span>



| <span data-ttu-id="1a8dc-121">Код возврата</span><span class="sxs-lookup"><span data-stu-id="1a8dc-121">Return code</span></span>                                                                                   | <span data-ttu-id="1a8dc-122">Описание</span><span class="sxs-lookup"><span data-stu-id="1a8dc-122">Description</span></span>                                  |
|-----------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="1a8dc-123"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="1a8dc-123"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="1a8dc-124">Operation completed successfully (Операция выполнена успешно).</span><span class="sxs-lookup"><span data-stu-id="1a8dc-124">Operation completed successfully.</span></span><br/> |
| <dl> <span data-ttu-id="1a8dc-125"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="1a8dc-125"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="1a8dc-126">Недопустимый параметр.</span><span class="sxs-lookup"><span data-stu-id="1a8dc-126">Invalid parameter.</span></span><br/>                |
| <dl> <span data-ttu-id="1a8dc-127"><dt>**\_указатель E**</dt></span><span class="sxs-lookup"><span data-stu-id="1a8dc-127"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="1a8dc-128">Передан неверный указатель.</span><span class="sxs-lookup"><span data-stu-id="1a8dc-128">A bad pointer was passed in.</span></span><br/>      |
| <dl> <span data-ttu-id="1a8dc-129"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="1a8dc-129"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="1a8dc-130">Недостаточно памяти.</span><span class="sxs-lookup"><span data-stu-id="1a8dc-130">Out of memory.</span></span><br/>                    |



 

## <a name="remarks"></a><span data-ttu-id="1a8dc-131">Комментарии</span><span class="sxs-lookup"><span data-stu-id="1a8dc-131">Remarks</span></span>

<span data-ttu-id="1a8dc-132">Список всех методов, предоставляемых этим интерфейсом, см. в разделе [**искардаус**](iscardauth.md).</span><span class="sxs-lookup"><span data-stu-id="1a8dc-132">For a list of all the methods provided by this interface, see [**ISCardAuth**](iscardauth.md).</span></span>

<span data-ttu-id="1a8dc-133">Кроме приведенных выше кодов ошибок COM, этот интерфейс может возвращать код ошибки смарт-карты, если для завершения запроса была вызвана функция смарт-карты.</span><span class="sxs-lookup"><span data-stu-id="1a8dc-133">In addition to the COM error codes listed above, this interface may return a smart card error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="1a8dc-134">Дополнительные сведения см. в статье [возвращаемые значения смарт-карты](authentication-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="1a8dc-134">For more information, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="1a8dc-135">Требования</span><span class="sxs-lookup"><span data-stu-id="1a8dc-135">Requirements</span></span>



| <span data-ttu-id="1a8dc-136">Требование</span><span class="sxs-lookup"><span data-stu-id="1a8dc-136">Requirement</span></span> | <span data-ttu-id="1a8dc-137">Значение</span><span class="sxs-lookup"><span data-stu-id="1a8dc-137">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="1a8dc-138">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="1a8dc-138">Minimum supported client</span></span><br/> | <span data-ttu-id="1a8dc-139">Только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="1a8dc-139">Windows XP \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="1a8dc-140">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="1a8dc-140">Minimum supported server</span></span><br/> | <span data-ttu-id="1a8dc-141">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="1a8dc-141">Windows Server 2003 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="1a8dc-142">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="1a8dc-142">End of client support</span></span><br/>    | <span data-ttu-id="1a8dc-143">Windows XP</span><span class="sxs-lookup"><span data-stu-id="1a8dc-143">Windows XP</span></span><br/>                                |
| <span data-ttu-id="1a8dc-144">Поддержка конца сервера</span><span class="sxs-lookup"><span data-stu-id="1a8dc-144">End of server support</span></span><br/>    | <span data-ttu-id="1a8dc-145">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="1a8dc-145">Windows Server 2003</span></span><br/>                       |



## <a name="see-also"></a><span data-ttu-id="1a8dc-146">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="1a8dc-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1a8dc-147">**искардаус**</span><span class="sxs-lookup"><span data-stu-id="1a8dc-147">**ISCardAuth**</span></span>](iscardauth.md)
</dt> </dl>

 

 
