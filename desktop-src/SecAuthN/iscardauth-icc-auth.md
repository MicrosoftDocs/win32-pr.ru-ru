---
description: Метод ICC \_ AUTH позволяет приложению проверить подлинность смарт-карты.
ms.assetid: 98aea241-6bdc-4f47-b56c-a90f69fcd9a4
title: 'Метод Искардаус:: ICC_Auth'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardAuth.ICC_Auth
api_type:
- COM
api_location: ''
ms.openlocfilehash: 015b5c395f025abea4ab2dc756c03691bbc27e72
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103991063"
---
# <a name="iscardauthicc_auth-method"></a><span data-ttu-id="a252d-103">Метод Искардаус:: ICC \_ AUTH</span><span class="sxs-lookup"><span data-stu-id="a252d-103">ISCardAuth::ICC\_Auth method</span></span>

<span data-ttu-id="a252d-104">\[Метод **ICC \_ AUTH** доступен для использования в операционных системах, указанных в разделе требования.</span><span class="sxs-lookup"><span data-stu-id="a252d-104">\[The **ICC\_Auth** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="a252d-105">Он недоступен для использования в Windows Server 2003 с пакетом обновления 1 (SP1) и более поздней версии, Windows Vista, Windows Server 2008 и последующих версиях операционной системы.</span><span class="sxs-lookup"><span data-stu-id="a252d-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="a252d-106">[Модули смарт-карт](/previous-versions/windows/desktop/secsmart/smart-card-modules) предоставляют аналогичные функции.\]</span><span class="sxs-lookup"><span data-stu-id="a252d-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="a252d-107">Метод **ICC \_ AUTH** позволяет приложению проверить подлинность смарт-карты.</span><span class="sxs-lookup"><span data-stu-id="a252d-107">The **ICC\_Auth** method allows an application to authenticate the smart card.</span></span>

## <a name="syntax"></a><span data-ttu-id="a252d-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="a252d-108">Syntax</span></span>


```C++
HRESULT ICC_Auth(
  [in]      LONG         lAlgoID,
  [in]      LPBYTEBUFFER pParam,
  [in, out] LPBYTEBUFFER *pBuffer
);
```



## <a name="parameters"></a><span data-ttu-id="a252d-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="a252d-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a252d-110">*лалгоид* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="a252d-110">*lAlgoID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a252d-111">Алгоритм, используемый в процессе проверки подлинности.</span><span class="sxs-lookup"><span data-stu-id="a252d-111">Algorithm to be used in the authentication process.</span></span>

</dd> <dt>

<span data-ttu-id="a252d-112">*ппарам* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="a252d-112">*pParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a252d-113">Объект [**ибитебуффер**](ibytebuffer.md) , содержащий зависящие от поставщика параметры процесса проверки подлинности.</span><span class="sxs-lookup"><span data-stu-id="a252d-113">An [**IByteBuffer**](ibytebuffer.md) object containing vendor-specific parameters of the authentication process.</span></span>

</dd> <dt>

<span data-ttu-id="a252d-114">*pBuffer* \[ в, out\]</span><span class="sxs-lookup"><span data-stu-id="a252d-114">*pBuffer* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="a252d-115">На входе содержит данные, которые будут использоваться в процессе проверки подлинности.</span><span class="sxs-lookup"><span data-stu-id="a252d-115">On input, contains data to be used in the authentication process.</span></span>

<span data-ttu-id="a252d-116">В выходных данных содержит результат процесса проверки подлинности.</span><span class="sxs-lookup"><span data-stu-id="a252d-116">On output, contains the result of the authentication process.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a252d-117">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="a252d-117">Return value</span></span>

<span data-ttu-id="a252d-118">Метод возвращает одно из следующих возможных значений.</span><span class="sxs-lookup"><span data-stu-id="a252d-118">The method returns one of the following possible values.</span></span>



| <span data-ttu-id="a252d-119">Код возврата</span><span class="sxs-lookup"><span data-stu-id="a252d-119">Return code</span></span>                                                                                   | <span data-ttu-id="a252d-120">Описание</span><span class="sxs-lookup"><span data-stu-id="a252d-120">Description</span></span>                                  |
|-----------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="a252d-121"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="a252d-121"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="a252d-122">Operation completed successfully (Операция выполнена успешно).</span><span class="sxs-lookup"><span data-stu-id="a252d-122">Operation completed successfully.</span></span><br/> |
| <dl> <span data-ttu-id="a252d-123"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="a252d-123"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="a252d-124">Недопустимый параметр.</span><span class="sxs-lookup"><span data-stu-id="a252d-124">Invalid parameter.</span></span><br/>                |
| <dl> <span data-ttu-id="a252d-125"><dt>**\_указатель E**</dt></span><span class="sxs-lookup"><span data-stu-id="a252d-125"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="a252d-126">Передан неверный указатель.</span><span class="sxs-lookup"><span data-stu-id="a252d-126">A bad pointer was passed in.</span></span><br/>      |
| <dl> <span data-ttu-id="a252d-127"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="a252d-127"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="a252d-128">Недостаточно памяти.</span><span class="sxs-lookup"><span data-stu-id="a252d-128">Out of memory.</span></span><br/>                    |



 

## <a name="remarks"></a><span data-ttu-id="a252d-129">Комментарии</span><span class="sxs-lookup"><span data-stu-id="a252d-129">Remarks</span></span>

<span data-ttu-id="a252d-130">Список всех методов, предоставляемых этим интерфейсом, см. в разделе [**искардаус**](iscardauth.md).</span><span class="sxs-lookup"><span data-stu-id="a252d-130">For a list of all the methods provided by this interface, see [**ISCardAuth**](iscardauth.md).</span></span>

<span data-ttu-id="a252d-131">Кроме приведенных выше кодов ошибок COM, этот интерфейс может возвращать код ошибки смарт-карты, если для завершения запроса была вызвана функция смарт-карты.</span><span class="sxs-lookup"><span data-stu-id="a252d-131">In addition to the COM error codes listed above, this interface may return a smart card error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="a252d-132">Дополнительные сведения см. в статье [возвращаемые значения смарт-карты](authentication-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="a252d-132">For more information, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="a252d-133">Требования</span><span class="sxs-lookup"><span data-stu-id="a252d-133">Requirements</span></span>



| <span data-ttu-id="a252d-134">Требование</span><span class="sxs-lookup"><span data-stu-id="a252d-134">Requirement</span></span> | <span data-ttu-id="a252d-135">Значение</span><span class="sxs-lookup"><span data-stu-id="a252d-135">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="a252d-136">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="a252d-136">Minimum supported client</span></span><br/> | <span data-ttu-id="a252d-137">Только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="a252d-137">Windows XP \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="a252d-138">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="a252d-138">Minimum supported server</span></span><br/> | <span data-ttu-id="a252d-139">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="a252d-139">Windows Server 2003 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="a252d-140">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="a252d-140">End of client support</span></span><br/>    | <span data-ttu-id="a252d-141">Windows XP</span><span class="sxs-lookup"><span data-stu-id="a252d-141">Windows XP</span></span><br/>                                |
| <span data-ttu-id="a252d-142">Поддержка конца сервера</span><span class="sxs-lookup"><span data-stu-id="a252d-142">End of server support</span></span><br/>    | <span data-ttu-id="a252d-143">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="a252d-143">Windows Server 2003</span></span><br/>                       |



## <a name="see-also"></a><span data-ttu-id="a252d-144">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="a252d-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a252d-145">**искардаус**</span><span class="sxs-lookup"><span data-stu-id="a252d-145">**ISCardAuth**</span></span>](iscardauth.md)
</dt> </dl>

 

 
