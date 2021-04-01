---
description: Метод Аттачбиреадер открывает смарт-карту в именованном модуле чтения.
ms.assetid: a92f3281-5018-4e90-bfa0-f03eb9373bb1
title: Метод Аттачбиреадер (Скардмгр. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCard.AttachByReader
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 2607ea2e13be2dcccc3c1b6beebd40c86822d0a5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103999300"
---
# <a name="iscardattachbyreader-method"></a><span data-ttu-id="eaafc-103">Метод Аттачбиреадер::</span><span class="sxs-lookup"><span data-stu-id="eaafc-103">ISCard::AttachByReader method</span></span>

<span data-ttu-id="eaafc-104">\[Метод **аттачбиреадер** доступен для использования в операционных системах, указанных в разделе требования.</span><span class="sxs-lookup"><span data-stu-id="eaafc-104">\[The **AttachByReader** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="eaafc-105">Он недоступен для использования в Windows Server 2003 с пакетом обновления 1 (SP1) и более поздней версии, Windows Vista, Windows Server 2008 и последующих версиях операционной системы.</span><span class="sxs-lookup"><span data-stu-id="eaafc-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="eaafc-106">[Модули смарт-карт](/previous-versions/windows/desktop/secsmart/smart-card-modules) предоставляют аналогичные функции.\]</span><span class="sxs-lookup"><span data-stu-id="eaafc-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="eaafc-107">Метод **аттачбиреадер** открывает [*смарт-карту*](../secgloss/s-gly.md) в именованном [*модуле чтения*](../secgloss/r-gly.md).</span><span class="sxs-lookup"><span data-stu-id="eaafc-107">The **AttachByReader** method opens the [*smart card*](../secgloss/s-gly.md) in the named [*reader*](../secgloss/r-gly.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="eaafc-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="eaafc-108">Syntax</span></span>


```C++
HRESULT AttachByReader(
  [in] BSTR              bstrReaderName,
  [in] SCARD_SHARE_MODES ShareMode,
  [in] SCARD_PROTOCOLS   PrefProtocol
);
```



## <a name="parameters"></a><span data-ttu-id="eaafc-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="eaafc-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="eaafc-110">*бстрреадернаме* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="eaafc-110">*bstrReaderName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="eaafc-111">Значение типа **BSTR** , содержащее имя устройства чтения смарт-карт.</span><span class="sxs-lookup"><span data-stu-id="eaafc-111">A **BSTR** that contains the name of the smart card reader.</span></span>

</dd> <dt>

<span data-ttu-id="eaafc-112">*Шаремоде* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="eaafc-112">*ShareMode* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="eaafc-113">Режим, в котором запрашивать доступ к смарт-карте.</span><span class="sxs-lookup"><span data-stu-id="eaafc-113">Mode in which to claim access to the smart card.</span></span>



| <span data-ttu-id="eaafc-114">Значение</span><span class="sxs-lookup"><span data-stu-id="eaafc-114">Value</span></span>                                                                                                                                            | <span data-ttu-id="eaafc-115">Значение</span><span class="sxs-lookup"><span data-stu-id="eaafc-115">Meaning</span></span>                                                       |
|--------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------|
| <span id="EXCLUSIVE"></span><span id="exclusive"></span><dl> <span data-ttu-id="eaafc-116"><dt>**ВЗАИМОИСКЛЮЧАЮЩИМ**</dt></span><span class="sxs-lookup"><span data-stu-id="eaafc-116"><dt>**EXCLUSIVE**</dt></span></span> </dl> | <span data-ttu-id="eaafc-117">Никто больше не использует это подключение к смарт-карте.</span><span class="sxs-lookup"><span data-stu-id="eaafc-117">No one else use this connection to the smart card.</span></span><br/> |
| <span id="SHARED"></span><span id="shared"></span><dl> <span data-ttu-id="eaafc-118"><dt>**ИСПОЛЬЗУЕМЫЙ**</dt></span><span class="sxs-lookup"><span data-stu-id="eaafc-118"><dt>**SHARED**</dt></span></span> </dl>          | <span data-ttu-id="eaafc-119">Это подключение могут использовать другие приложения.</span><span class="sxs-lookup"><span data-stu-id="eaafc-119">Other applications can use this connection.</span></span><br/>        |



 

</dd> <dt>

<span data-ttu-id="eaafc-120">*Префпротокол* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="eaafc-120">*PrefProtocol* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="eaafc-121">Предпочтительное значение протокола.</span><span class="sxs-lookup"><span data-stu-id="eaafc-121">Preferred protocol value.</span></span>

<dl><span id="T0"></span><span id="t0"></span><dt>

<span data-ttu-id="eaafc-122">**T0**</span><span class="sxs-lookup"><span data-stu-id="eaafc-122">**T0**</span></span>
</dt><span id="T1"></span><span id="t1"></span><dt>

<span data-ttu-id="eaafc-123">**T1**</span><span class="sxs-lookup"><span data-stu-id="eaafc-123">**T1**</span></span>
</dt><span id="RAW"></span><span id="raw"></span><dt>

<span data-ttu-id="eaafc-124">**RAW**</span><span class="sxs-lookup"><span data-stu-id="eaafc-124">**RAW**</span></span>
</dt><span id="T0_T1"></span><span id="t0_t1"></span><dt>

<span data-ttu-id="eaafc-125">**T0 \| T1**</span><span class="sxs-lookup"><span data-stu-id="eaafc-125">**T0\|T1**</span></span>
</dt> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="eaafc-126">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="eaafc-126">Return value</span></span>

<span data-ttu-id="eaafc-127">Метод возвращает одно из следующих возможных значений.</span><span class="sxs-lookup"><span data-stu-id="eaafc-127">The method returns one of the following possible values.</span></span>



| <span data-ttu-id="eaafc-128">Код возврата</span><span class="sxs-lookup"><span data-stu-id="eaafc-128">Return code</span></span>                                                                                  | <span data-ttu-id="eaafc-129">Описание</span><span class="sxs-lookup"><span data-stu-id="eaafc-129">Description</span></span>                                                                                      |
|----------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="eaafc-130"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="eaafc-130"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="eaafc-131">Открытие на смарт-карте в именованном модуле чтения успешно завершено.</span><span class="sxs-lookup"><span data-stu-id="eaafc-131">Open on the smart card in the named reader has been completed successfully.</span></span><br/>           |
| <dl> <span data-ttu-id="eaafc-132"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="eaafc-132"><dt>**E\_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="eaafc-133">Возникла проблема с одним или несколькими параметрами, передаваемыми в функцию.</span><span class="sxs-lookup"><span data-stu-id="eaafc-133">There is something wrong with one or more of the parameters passed into the function.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="eaafc-134">Комментарии</span><span class="sxs-lookup"><span data-stu-id="eaafc-134">Remarks</span></span>

<span data-ttu-id="eaafc-135">Кроме приведенных выше кодов ошибок COM, этот интерфейс может возвращать код ошибки [*смарт-карты*](../secgloss/s-gly.md) , если для завершения запроса была вызвана функция смарт-карты.</span><span class="sxs-lookup"><span data-stu-id="eaafc-135">In addition to the COM error codes listed above, this interface may return a [*smart card*](../secgloss/s-gly.md) error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="eaafc-136">Дополнительные сведения см. в статье [возвращаемые значения смарт-карты](authentication-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="eaafc-136">For more information, see [Smart Card Return Values](authentication-return-values.md).</span></span>

<span data-ttu-id="eaafc-137">После завершения использования модуля чтения отпустите вложение, вызвав метод [**етач::D**](iscard-detach.md) .</span><span class="sxs-lookup"><span data-stu-id="eaafc-137">When you have finished using the reader, release the attachment by calling the [**ISCard::Detach**](iscard-detach.md) method.</span></span>

## <a name="examples"></a><span data-ttu-id="eaafc-138">Примеры</span><span class="sxs-lookup"><span data-stu-id="eaafc-138">Examples</span></span>

<span data-ttu-id="eaafc-139">В следующем примере показано подключение к смарт-карте в указанном модуле чтения смарт-карт.</span><span class="sxs-lookup"><span data-stu-id="eaafc-139">The following example shows attaching to a smart card in a specified smart card reader.</span></span>


```C++
#include <windows.h>
#include <stdio.h>
#include <Scardmgr.h>

// The reader name is vendor specific; change as needed.
#define READER_NAME L"Vendor Reader 0"

void main()
{
    BSTR     bstrReader = NULL;
    HRESULT  hr;

    bstrReader = SysAllocString(READER_NAME);
    if (NULL == bstrReader)
    {
        // Error encountered.
        exit(1);
    }

    // Connect to the reader.
    hr = pISCard->AttachByReader(bstrReader, SHARED, T0);
    if (FAILED(hr))
    {
        printf("Failed AttachByReader\n");
        // Take other error handling action.
        // ...
    }

    // Detach reader by calling ISCard::Detach (not shown).
    // ...

    // When done, free BSTR.
    if (NULL != bstrReader)
        SysFreeString(bstrReader);
}
```



## <a name="requirements"></a><span data-ttu-id="eaafc-140">Требования</span><span class="sxs-lookup"><span data-stu-id="eaafc-140">Requirements</span></span>



| <span data-ttu-id="eaafc-141">Требование</span><span class="sxs-lookup"><span data-stu-id="eaafc-141">Requirement</span></span> | <span data-ttu-id="eaafc-142">Значение</span><span class="sxs-lookup"><span data-stu-id="eaafc-142">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="eaafc-143">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="eaafc-143">Minimum supported client</span></span><br/> | <span data-ttu-id="eaafc-144">Только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="eaafc-144">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="eaafc-145">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="eaafc-145">Minimum supported server</span></span><br/> | <span data-ttu-id="eaafc-146">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="eaafc-146">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="eaafc-147">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="eaafc-147">End of client support</span></span><br/>    | <span data-ttu-id="eaafc-148">Windows XP</span><span class="sxs-lookup"><span data-stu-id="eaafc-148">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="eaafc-149">Поддержка конца сервера</span><span class="sxs-lookup"><span data-stu-id="eaafc-149">End of server support</span></span><br/>    | <span data-ttu-id="eaafc-150">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="eaafc-150">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="eaafc-151">Header</span><span class="sxs-lookup"><span data-stu-id="eaafc-151">Header</span></span><br/>                   | <dl> <span data-ttu-id="eaafc-152"><dt>Скардмгр. h</dt></span><span class="sxs-lookup"><span data-stu-id="eaafc-152"><dt>Scardmgr.h</dt></span></span> </dl>   |
| <span data-ttu-id="eaafc-153">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="eaafc-153">Type library</span></span><br/>             | <dl> <span data-ttu-id="eaafc-154"><dt>Скардмгр. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="eaafc-154"><dt>Scardmgr.tlb</dt></span></span> </dl> |
| <span data-ttu-id="eaafc-155">DLL</span><span class="sxs-lookup"><span data-stu-id="eaafc-155">DLL</span></span><br/>                      | <dl> <span data-ttu-id="eaafc-156"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="eaafc-156"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="eaafc-157">IID</span><span class="sxs-lookup"><span data-stu-id="eaafc-157">IID</span></span><br/>                      | <span data-ttu-id="eaafc-158">Идентификатор IID \_ -карты определен как 1461AAC3-6810-11D0-918F-00AA00C18068</span><span class="sxs-lookup"><span data-stu-id="eaafc-158">IID\_ISCard is defined as 1461AAC3-6810-11D0-918F-00AA00C18068</span></span><br/>               |



## <a name="see-also"></a><span data-ttu-id="eaafc-159">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="eaafc-159">See also</span></span>

<dl> <dt>

[<span data-ttu-id="eaafc-160">**аттачбихандле**</span><span class="sxs-lookup"><span data-stu-id="eaafc-160">**AttachByHandle**</span></span>](iscard-attachbyhandle.md)
</dt> <dt>

[<span data-ttu-id="eaafc-161">**Соединил**</span><span class="sxs-lookup"><span data-stu-id="eaafc-161">**Detach**</span></span>](iscard-detach.md)
</dt> <dt>

[<span data-ttu-id="eaafc-162">**Карточка**</span><span class="sxs-lookup"><span data-stu-id="eaafc-162">**ISCard**</span></span>](iscard.md)
</dt> <dt>

[<span data-ttu-id="eaafc-163">**Повторно подключиться**</span><span class="sxs-lookup"><span data-stu-id="eaafc-163">**ReAttach**</span></span>](iscard-reattach.md)
</dt> </dl>

 

 
