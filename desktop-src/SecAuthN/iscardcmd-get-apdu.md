---
description: Извлекает необработанную единицу данных протокола приложения (КАТЕГОРИЯХ APDU).
ms.assetid: d8b326db-de54-4ef8-becb-fd905414c45c
title: 'Метод Искардкмд:: get_Apdu (Скарддат. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardCmd.get_Apdu
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: fb943d7ade48f6684cdc10cb4b1ad7e48f87e65c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104072766"
---
# <a name="iscardcmdget_apdu-method"></a><span data-ttu-id="ec24d-103">Метод Искардкмд:: Get \_ категориях APDU</span><span class="sxs-lookup"><span data-stu-id="ec24d-103">ISCardCmd::get\_Apdu method</span></span>

<span data-ttu-id="ec24d-104">\[Метод **Get \_ категориях APDU** доступен для использования в операционных системах, указанных в разделе требования.</span><span class="sxs-lookup"><span data-stu-id="ec24d-104">\[The **get\_Apdu** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="ec24d-105">Он недоступен для использования в Windows Server 2003 с пакетом обновления 1 (SP1) и более поздней версии, Windows Vista, Windows Server 2008 и последующих версиях операционной системы.</span><span class="sxs-lookup"><span data-stu-id="ec24d-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="ec24d-106">[Модули смарт-карт](/previous-versions/windows/desktop/secsmart/smart-card-modules) предоставляют аналогичные функции.\]</span><span class="sxs-lookup"><span data-stu-id="ec24d-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="ec24d-107">Метод **Get \_ категориях APDU** извлекает необработанную [*единицу данных протокола приложения*](../secgloss/a-gly.md) (категориях APDU).</span><span class="sxs-lookup"><span data-stu-id="ec24d-107">The **get\_Apdu** method retrieves the raw [*application protocol data unit*](../secgloss/a-gly.md) (APDU).</span></span>

## <a name="syntax"></a><span data-ttu-id="ec24d-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="ec24d-108">Syntax</span></span>


```C++
HRESULT get_Apdu(
  [out] LPBYTEBUFFER *ppApdu
);
```



## <a name="parameters"></a><span data-ttu-id="ec24d-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="ec24d-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ec24d-110">*ппапду* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="ec24d-110">*ppApdu* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ec24d-111">Указатель на буфер байтов, сопоставленный через объект **IStream** , который содержит сообщение категориях APDU при возврате.</span><span class="sxs-lookup"><span data-stu-id="ec24d-111">Pointer to the byte buffer mapped through an **IStream** object that contains the APDU message on return.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ec24d-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="ec24d-112">Return value</span></span>

<span data-ttu-id="ec24d-113">Метод возвращает одно из следующих возможных значений.</span><span class="sxs-lookup"><span data-stu-id="ec24d-113">The method returns one of the following possible values.</span></span>



| <span data-ttu-id="ec24d-114">Код возврата</span><span class="sxs-lookup"><span data-stu-id="ec24d-114">Return code</span></span>                                                                                   | <span data-ttu-id="ec24d-115">Описание</span><span class="sxs-lookup"><span data-stu-id="ec24d-115">Description</span></span>                                      |
|-----------------------------------------------------------------------------------------------|--------------------------------------------------|
| <dl> <span data-ttu-id="ec24d-116"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="ec24d-116"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="ec24d-117">Operation completed successfully (Операция выполнена успешно).</span><span class="sxs-lookup"><span data-stu-id="ec24d-117">Operation completed successfully.</span></span><br/>     |
| <dl> <span data-ttu-id="ec24d-118"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="ec24d-118"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="ec24d-119">Недопустимый параметр *ппапду* .</span><span class="sxs-lookup"><span data-stu-id="ec24d-119">The *ppApdu* parameter is not valid.</span></span><br/>  |
| <dl> <span data-ttu-id="ec24d-120"><dt>**\_указатель E**</dt></span><span class="sxs-lookup"><span data-stu-id="ec24d-120"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="ec24d-121">В *ппапду* был передан неверный указатель.</span><span class="sxs-lookup"><span data-stu-id="ec24d-121">A bad pointer was passed in *ppApdu*.</span></span><br/> |
| <dl> <span data-ttu-id="ec24d-122"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="ec24d-122"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="ec24d-123">Недостаточно памяти.</span><span class="sxs-lookup"><span data-stu-id="ec24d-123">Out of memory.</span></span><br/>                        |



 

## <a name="remarks"></a><span data-ttu-id="ec24d-124">Комментарии</span><span class="sxs-lookup"><span data-stu-id="ec24d-124">Remarks</span></span>

<span data-ttu-id="ec24d-125">Чтобы скопировать КАТЕГОРИЯХ APDU из объекта [**ибитебуффер**](ibytebuffer.md) (**ISTREAM**) в категориях APDU, упакованный в этот объект интерфейса, вызовите [**метод \_ категориях APDU**](iscardcmd-put-apdu.md).</span><span class="sxs-lookup"><span data-stu-id="ec24d-125">To copy the APDU from an [**IByteBuffer**](ibytebuffer.md) (**IStream**) object into the APDU wrapped in this interface object, call [**put\_Apdu**](iscardcmd-put-apdu.md).</span></span>

<span data-ttu-id="ec24d-126">Чтобы определить длину КАТЕГОРИЯХ APDU, вызовите [**Get \_ апдуленгс**](iscardcmd-get-apdulength.md).</span><span class="sxs-lookup"><span data-stu-id="ec24d-126">To determine the length of the APDU, call [**get\_ApduLength**](iscardcmd-get-apdulength.md).</span></span>

<span data-ttu-id="ec24d-127">Список всех методов, предоставляемых интерфейсом [**искардкмд**](iscardcmd.md) , см. в разделе [**искардкмд**](iscardcmd.md).</span><span class="sxs-lookup"><span data-stu-id="ec24d-127">For a list of all the methods provided by the [**ISCardCmd**](iscardcmd.md) interface, see [**ISCardCmd**](iscardcmd.md).</span></span>

<span data-ttu-id="ec24d-128">Кроме приведенных выше кодов ошибок COM, этот интерфейс может возвращать код ошибки [*смарт-карты*](../secgloss/s-gly.md) , если для завершения запроса была вызвана функция смарт-карты.</span><span class="sxs-lookup"><span data-stu-id="ec24d-128">In addition to the COM error codes listed above, this interface may return a [*smart card*](../secgloss/s-gly.md) error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="ec24d-129">Дополнительные сведения о кодах ошибок смарт-карт см. в статье [возвращаемые значения смарт-карты](authentication-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="ec24d-129">For information about smart card error codes, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="examples"></a><span data-ttu-id="ec24d-130">Примеры</span><span class="sxs-lookup"><span data-stu-id="ec24d-130">Examples</span></span>

<span data-ttu-id="ec24d-131">В следующем примере показано, как получить необработанную [*единицу данных протокола приложения*](../secgloss/a-gly.md) (категориях APDU).</span><span class="sxs-lookup"><span data-stu-id="ec24d-131">The following example shows how to retrieve the raw [*application protocol data unit*](../secgloss/a-gly.md) (APDU).</span></span> <span data-ttu-id="ec24d-132">В примере предполагается, что Пискардкмд является допустимым указателем на интерфейс [**искардкмд**](iscardcmd.md) , а пибитеапду является допустимым указателем на экземпляр интерфейса [**ибитебуффер**](ibytebuffer.md) .</span><span class="sxs-lookup"><span data-stu-id="ec24d-132">The example assumes that pISCardCmd is a valid pointer to the [**ISCardCmd**](iscardcmd.md) interface, and that pIByteApdu is a valid pointer to an instance of the [**IByteBuffer**](ibytebuffer.md) interface.</span></span>


```C++
HRESULT    hr;

hr = pISCardCmd->get_Apdu(&pIByteApdu);
if (FAILED(hr)) 
{
    printf("Failed get_Apdu.\n");
    // Take other error handling action as needed.
}
```



## <a name="requirements"></a><span data-ttu-id="ec24d-133">Требования</span><span class="sxs-lookup"><span data-stu-id="ec24d-133">Requirements</span></span>



| <span data-ttu-id="ec24d-134">Требование</span><span class="sxs-lookup"><span data-stu-id="ec24d-134">Requirement</span></span> | <span data-ttu-id="ec24d-135">Значение</span><span class="sxs-lookup"><span data-stu-id="ec24d-135">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="ec24d-136">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="ec24d-136">Minimum supported client</span></span><br/> | <span data-ttu-id="ec24d-137">Только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="ec24d-137">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="ec24d-138">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="ec24d-138">Minimum supported server</span></span><br/> | <span data-ttu-id="ec24d-139">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="ec24d-139">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="ec24d-140">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="ec24d-140">End of client support</span></span><br/>    | <span data-ttu-id="ec24d-141">Windows XP</span><span class="sxs-lookup"><span data-stu-id="ec24d-141">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="ec24d-142">Поддержка конца сервера</span><span class="sxs-lookup"><span data-stu-id="ec24d-142">End of server support</span></span><br/>    | <span data-ttu-id="ec24d-143">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="ec24d-143">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="ec24d-144">Header</span><span class="sxs-lookup"><span data-stu-id="ec24d-144">Header</span></span><br/>                   | <dl> <span data-ttu-id="ec24d-145"><dt>Скарддат. h</dt></span><span class="sxs-lookup"><span data-stu-id="ec24d-145"><dt>Scarddat.h</dt></span></span> </dl>   |
| <span data-ttu-id="ec24d-146">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="ec24d-146">Type library</span></span><br/>             | <dl> <span data-ttu-id="ec24d-147"><dt>Скарддат. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="ec24d-147"><dt>Scarddat.tlb</dt></span></span> </dl> |
| <span data-ttu-id="ec24d-148">DLL</span><span class="sxs-lookup"><span data-stu-id="ec24d-148">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ec24d-149"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ec24d-149"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="ec24d-150">IID</span><span class="sxs-lookup"><span data-stu-id="ec24d-150">IID</span></span><br/>                      | <span data-ttu-id="ec24d-151">IID \_ искардкмд определен как D5778AE3-43DE-11D0-9171-00AA00C18068</span><span class="sxs-lookup"><span data-stu-id="ec24d-151">IID\_ISCardCmd is defined as D5778AE3-43DE-11D0-9171-00AA00C18068</span></span><br/>            |



## <a name="see-also"></a><span data-ttu-id="ec24d-152">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="ec24d-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ec24d-153">**получить \_ апдуленгс**</span><span class="sxs-lookup"><span data-stu-id="ec24d-153">**get\_ApduLength**</span></span>](iscardcmd-get-apdulength.md)
</dt> <dt>

[<span data-ttu-id="ec24d-154">**искардкмд**</span><span class="sxs-lookup"><span data-stu-id="ec24d-154">**ISCardCmd**</span></span>](iscardcmd.md)
</dt> <dt>

[<span data-ttu-id="ec24d-155">**разместить \_ категориях APDU**</span><span class="sxs-lookup"><span data-stu-id="ec24d-155">**put\_Apdu**</span></span>](iscardcmd-put-apdu.md)
</dt> </dl>

 

 
