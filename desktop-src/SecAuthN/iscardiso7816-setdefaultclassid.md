---
description: Метод Сетдефаултклассид присваивает байт идентификатора стандартного класса, который будет использоваться во всех операциях при создании блока данных протокола приложения ISO 7816-4 (КАТЕГОРИЯХ APDU). По умолчанию для идентификатора стандартного класса используется значение 0x00.
ms.assetid: 5a53d5f1-7986-4c4c-9512-f592cd398d1c
title: 'Метод ISCardISO7816:: Сетдефаултклассид (Скардссп. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardISO7816.SetDefaultClassId
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 29e8868f491f0b9a61554da008c4100622815dd4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105647438"
---
# <a name="iscardiso7816setdefaultclassid-method"></a><span data-ttu-id="7e7f8-104">Метод ISCardISO7816:: Сетдефаултклассид</span><span class="sxs-lookup"><span data-stu-id="7e7f8-104">ISCardISO7816::SetDefaultClassId method</span></span>

<span data-ttu-id="7e7f8-105">\[Метод **сетдефаултклассид** доступен для использования в операционных системах, указанных в разделе требования.</span><span class="sxs-lookup"><span data-stu-id="7e7f8-105">\[The **SetDefaultClassId** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="7e7f8-106">Он недоступен для использования в Windows Server 2003 с пакетом обновления 1 (SP1) и более поздней версии, Windows Vista, Windows Server 2008 и последующих версиях операционной системы.</span><span class="sxs-lookup"><span data-stu-id="7e7f8-106">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="7e7f8-107">[Модули смарт-карт](/previous-versions/windows/desktop/secsmart/smart-card-modules) предоставляют аналогичные функции.\]</span><span class="sxs-lookup"><span data-stu-id="7e7f8-107">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="7e7f8-108">Метод **сетдефаултклассид** присваивает байт идентификатора стандартного класса, который будет использоваться во всех операциях при создании [*блока данных протокола приложения*](../secgloss/a-gly.md) ISO 7816-4 (категориях APDU).</span><span class="sxs-lookup"><span data-stu-id="7e7f8-108">The **SetDefaultClassId** method assigns a standard class identifier byte that will be used in all operations when constructing an ISO 7816-4 command [*application protocol data unit*](../secgloss/a-gly.md) (APDU).</span></span> <span data-ttu-id="7e7f8-109">По умолчанию для идентификатора стандартного класса используется значение 0x00.</span><span class="sxs-lookup"><span data-stu-id="7e7f8-109">By default, the standard class identifier byte is 0x00.</span></span>

## <a name="syntax"></a><span data-ttu-id="7e7f8-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="7e7f8-110">Syntax</span></span>


```C++
HRESULT SetDefaultClassId(
  [in] BYTE byClass
);
```



## <a name="parameters"></a><span data-ttu-id="7e7f8-111">Параметры</span><span class="sxs-lookup"><span data-stu-id="7e7f8-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7e7f8-112">*бикласс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="7e7f8-112">*byClass* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7e7f8-113">Идентификатор класса, байт.</span><span class="sxs-lookup"><span data-stu-id="7e7f8-113">Class ID byte.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7e7f8-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="7e7f8-114">Return value</span></span>

<span data-ttu-id="7e7f8-115">Возможны следующие возвращаемые значения:</span><span class="sxs-lookup"><span data-stu-id="7e7f8-115">The possible return values are the following:</span></span>



| <span data-ttu-id="7e7f8-116">Код возврата</span><span class="sxs-lookup"><span data-stu-id="7e7f8-116">Return code</span></span>                                                                          | <span data-ttu-id="7e7f8-117">Описание</span><span class="sxs-lookup"><span data-stu-id="7e7f8-117">Description</span></span>                                  |
|--------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="7e7f8-118"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="7e7f8-118"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="7e7f8-119">Operation completed successfully (Операция выполнена успешно).</span><span class="sxs-lookup"><span data-stu-id="7e7f8-119">Operation completed successfully.</span></span><br/> |



 

<span data-ttu-id="7e7f8-120">Список всех методов, предоставляемых интерфейсом [**ISCardISO7816**](iscardiso7816.md) , см. в разделе **ISCardISO7816**.</span><span class="sxs-lookup"><span data-stu-id="7e7f8-120">For a list of all the methods provided by the [**ISCardISO7816**](iscardiso7816.md) interface, see **ISCardISO7816**.</span></span>

<span data-ttu-id="7e7f8-121">Кроме приведенных выше кодов ошибок COM, этот интерфейс может возвращать код ошибки [*смарт-карты*](../secgloss/s-gly.md) , если для завершения запроса была вызвана функция смарт-карты.</span><span class="sxs-lookup"><span data-stu-id="7e7f8-121">In addition to the COM error codes listed above, this interface may return a [*smart card*](../secgloss/s-gly.md) error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="7e7f8-122">Дополнительные сведения о кодах ошибок смарт-карт см. в статье [возвращаемые значения смарт-карты](authentication-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="7e7f8-122">For information about smart card error codes, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="7e7f8-123">Требования</span><span class="sxs-lookup"><span data-stu-id="7e7f8-123">Requirements</span></span>



| <span data-ttu-id="7e7f8-124">Требование</span><span class="sxs-lookup"><span data-stu-id="7e7f8-124">Requirement</span></span> | <span data-ttu-id="7e7f8-125">Значение</span><span class="sxs-lookup"><span data-stu-id="7e7f8-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="7e7f8-126">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="7e7f8-126">Minimum supported client</span></span><br/> | <span data-ttu-id="7e7f8-127">Только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="7e7f8-127">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="7e7f8-128">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="7e7f8-128">Minimum supported server</span></span><br/> | <span data-ttu-id="7e7f8-129">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="7e7f8-129">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="7e7f8-130">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="7e7f8-130">End of client support</span></span><br/>    | <span data-ttu-id="7e7f8-131">Windows XP</span><span class="sxs-lookup"><span data-stu-id="7e7f8-131">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="7e7f8-132">Поддержка конца сервера</span><span class="sxs-lookup"><span data-stu-id="7e7f8-132">End of server support</span></span><br/>    | <span data-ttu-id="7e7f8-133">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="7e7f8-133">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="7e7f8-134">Header</span><span class="sxs-lookup"><span data-stu-id="7e7f8-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="7e7f8-135"><dt>Скардссп. h</dt></span><span class="sxs-lookup"><span data-stu-id="7e7f8-135"><dt>Scardssp.h</dt></span></span> </dl>   |
| <span data-ttu-id="7e7f8-136">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="7e7f8-136">Type library</span></span><br/>             | <dl> <span data-ttu-id="7e7f8-137"><dt>Скардсрв. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="7e7f8-137"><dt>Scardsrv.tlb</dt></span></span> </dl> |
| <span data-ttu-id="7e7f8-138">DLL</span><span class="sxs-lookup"><span data-stu-id="7e7f8-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7e7f8-139"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7e7f8-139"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="7e7f8-140">IID</span><span class="sxs-lookup"><span data-stu-id="7e7f8-140">IID</span></span><br/>                      | <span data-ttu-id="7e7f8-141">IID \_ ISCardISO7816 определен как 53B6AA68-3F56-11D0-916B-00AA00C18068</span><span class="sxs-lookup"><span data-stu-id="7e7f8-141">IID\_ISCardISO7816 is defined as 53B6AA68-3F56-11D0-916B-00AA00C18068</span></span><br/>        |



## <a name="see-also"></a><span data-ttu-id="7e7f8-142">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="7e7f8-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7e7f8-143">**ISCardISO7816**</span><span class="sxs-lookup"><span data-stu-id="7e7f8-143">**ISCardISO7816**</span></span>](iscardiso7816.md)
</dt> </dl>

 

 
