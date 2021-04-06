---
description: Копирует блок данных протокола приложения (КАТЕГОРИЯХ APDU) из объекта Ибитебуффер (IStream) в КАТЕГОРИЯХ APDU, упакованный в этот объект интерфейса.
ms.assetid: 28dac222-ee7a-40aa-903b-e9c0b7757c9c
title: 'Искардкмд: метод ut_Apdu:p (Скарддат. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardCmd.put_Apdu
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: ee615e7f2e8d7555cfed276658e8de1a97ddf73a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103991134"
---
# <a name="iscardcmdput_apdu-method"></a><span data-ttu-id="adb84-103">Искардкмд::p UT \_ категориях APDU метод</span><span class="sxs-lookup"><span data-stu-id="adb84-103">ISCardCmd::put\_Apdu method</span></span>

<span data-ttu-id="adb84-104">\[Метод **размещения \_ категориях APDU** доступен для использования в операционных системах, указанных в разделе требования.</span><span class="sxs-lookup"><span data-stu-id="adb84-104">\[The **put\_Apdu** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="adb84-105">Он недоступен для использования в Windows Server 2003 с пакетом обновления 1 (SP1) и более поздней версии, Windows Vista, Windows Server 2008 и последующих версиях операционной системы.</span><span class="sxs-lookup"><span data-stu-id="adb84-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="adb84-106">[Модули смарт-карт](/previous-versions/windows/desktop/secsmart/smart-card-modules) предоставляют аналогичные функции.\]</span><span class="sxs-lookup"><span data-stu-id="adb84-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="adb84-107">Метод **размещения \_ категориях APDU** копирует [*блок данных протокола приложения*](../secgloss/a-gly.md) (категориях APDU) из объекта [**ибитебуффер**](ibytebuffer.md) (**IStream**) в категориях APDU, упакованный в этот объект интерфейса.</span><span class="sxs-lookup"><span data-stu-id="adb84-107">The **put\_Apdu** method copies the [*application protocol data unit*](../secgloss/a-gly.md) (APDU) from the [**IByteBuffer**](ibytebuffer.md) (**IStream**) object into the APDU wrapped in this interface object.</span></span>

## <a name="syntax"></a><span data-ttu-id="adb84-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="adb84-108">Syntax</span></span>


```C++
HRESULT put_Apdu(
  [in] LPBYTEBUFFER pApdu
);
```



## <a name="parameters"></a><span data-ttu-id="adb84-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="adb84-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="adb84-110">*папду* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="adb84-110">*pApdu* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="adb84-111">Указатель на КАТЕГОРИЯХ APDU ISO 7816-4 для копирования.</span><span class="sxs-lookup"><span data-stu-id="adb84-111">Pointer to the ISO 7816-4 APDU to be copied in.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="adb84-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="adb84-112">Return value</span></span>

<span data-ttu-id="adb84-113">Метод возвращает одно из следующих возможных значений.</span><span class="sxs-lookup"><span data-stu-id="adb84-113">The method returns one of the following possible values.</span></span>



| <span data-ttu-id="adb84-114">Код возврата</span><span class="sxs-lookup"><span data-stu-id="adb84-114">Return code</span></span>                                                                                   | <span data-ttu-id="adb84-115">Описание</span><span class="sxs-lookup"><span data-stu-id="adb84-115">Description</span></span>                                     |
|-----------------------------------------------------------------------------------------------|-------------------------------------------------|
| <dl> <span data-ttu-id="adb84-116"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="adb84-116"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="adb84-117">Operation completed successfully (Операция выполнена успешно).</span><span class="sxs-lookup"><span data-stu-id="adb84-117">Operation completed successfully.</span></span><br/>    |
| <dl> <span data-ttu-id="adb84-118"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="adb84-118"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="adb84-119">Недопустимый параметр *папду* .</span><span class="sxs-lookup"><span data-stu-id="adb84-119">The *pApdu* parameter is not valid.</span></span><br/>  |
| <dl> <span data-ttu-id="adb84-120"><dt>**\_указатель E**</dt></span><span class="sxs-lookup"><span data-stu-id="adb84-120"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="adb84-121">В *папду* был передан неверный указатель.</span><span class="sxs-lookup"><span data-stu-id="adb84-121">A bad pointer was passed in *pApdu*.</span></span><br/> |
| <dl> <span data-ttu-id="adb84-122"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="adb84-122"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="adb84-123">Недостаточно памяти.</span><span class="sxs-lookup"><span data-stu-id="adb84-123">Out of memory.</span></span><br/>                       |



 

## <a name="remarks"></a><span data-ttu-id="adb84-124">Комментарии</span><span class="sxs-lookup"><span data-stu-id="adb84-124">Remarks</span></span>

<span data-ttu-id="adb84-125">Чтобы получить необработанные КАТЕГОРИЯХ APDU из буфера байтов, сопоставленного с помощью **IStream** , содержащего сообщение категориях APDU, вызовите [**Get \_ категориях APDU**](iscardcmd-get-apdu.md).</span><span class="sxs-lookup"><span data-stu-id="adb84-125">To retrieve the raw APDU from the byte buffer mapped through an **IStream** that contains the APDU message, call [**get\_Apdu**](iscardcmd-get-apdu.md).</span></span>

<span data-ttu-id="adb84-126">Список всех методов, предоставляемых этим интерфейсом, см. в разделе [**искардкмд**](iscardcmd.md).</span><span class="sxs-lookup"><span data-stu-id="adb84-126">For a list of all the methods provided by this interface, see [**ISCardCmd**](iscardcmd.md).</span></span>

<span data-ttu-id="adb84-127">Кроме приведенных выше кодов ошибок COM, этот интерфейс может возвращать код ошибки [*смарт-карты*](../secgloss/s-gly.md) , если для завершения запроса была вызвана функция смарт-карты.</span><span class="sxs-lookup"><span data-stu-id="adb84-127">In addition to the COM error codes listed above, this interface may return a [*smart card*](../secgloss/s-gly.md) error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="adb84-128">Дополнительные сведения см. в статье [возвращаемые значения смарт-карты](authentication-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="adb84-128">For more information, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="examples"></a><span data-ttu-id="adb84-129">Примеры</span><span class="sxs-lookup"><span data-stu-id="adb84-129">Examples</span></span>

<span data-ttu-id="adb84-130">В следующем примере показано, как скопировать КАТЕГОРИЯХ APDU из объекта [**ибитебуффер**](ibytebuffer.md) (**ISTREAM**) в категориях APDU, упакованный в объект Interface.</span><span class="sxs-lookup"><span data-stu-id="adb84-130">The following example shows how to copy an APDU from an [**IByteBuffer**](ibytebuffer.md) (**IStream**) object into the APDU wrapped in an interface object.</span></span> <span data-ttu-id="adb84-131">В этом примере предполагается, что Пибитеапду является допустимым указателем на экземпляр **ибитебуффер** , а пискардкмд является допустимым указателем на экземпляр интерфейса [**искардкмд**](iscardcmd.md) .</span><span class="sxs-lookup"><span data-stu-id="adb84-131">The example assumes that pIByteApdu is a valid pointer to an instance of **IByteBuffer** and that pISCardCmd is a valid pointer to an instance of the [**ISCardCmd**](iscardcmd.md) interface.</span></span>


```C++
HRESULT    hr;


// Set the APDU.
hr = pISCardCmd->put_Apdu(pIByteApdu);
if (FAILED(hr)) 
{
    printf("Failed put_Apdu.\n");
    // Take other error handling action as needed.
}
```



## <a name="requirements"></a><span data-ttu-id="adb84-132">Требования</span><span class="sxs-lookup"><span data-stu-id="adb84-132">Requirements</span></span>



| <span data-ttu-id="adb84-133">Требование</span><span class="sxs-lookup"><span data-stu-id="adb84-133">Requirement</span></span> | <span data-ttu-id="adb84-134">Значение</span><span class="sxs-lookup"><span data-stu-id="adb84-134">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="adb84-135">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="adb84-135">Minimum supported client</span></span><br/> | <span data-ttu-id="adb84-136">Только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="adb84-136">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="adb84-137">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="adb84-137">Minimum supported server</span></span><br/> | <span data-ttu-id="adb84-138">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="adb84-138">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="adb84-139">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="adb84-139">End of client support</span></span><br/>    | <span data-ttu-id="adb84-140">Windows XP</span><span class="sxs-lookup"><span data-stu-id="adb84-140">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="adb84-141">Поддержка конца сервера</span><span class="sxs-lookup"><span data-stu-id="adb84-141">End of server support</span></span><br/>    | <span data-ttu-id="adb84-142">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="adb84-142">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="adb84-143">Header</span><span class="sxs-lookup"><span data-stu-id="adb84-143">Header</span></span><br/>                   | <dl> <span data-ttu-id="adb84-144"><dt>Скарддат. h</dt></span><span class="sxs-lookup"><span data-stu-id="adb84-144"><dt>Scarddat.h</dt></span></span> </dl>   |
| <span data-ttu-id="adb84-145">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="adb84-145">Type library</span></span><br/>             | <dl> <span data-ttu-id="adb84-146"><dt>Скарддат. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="adb84-146"><dt>Scarddat.tlb</dt></span></span> </dl> |
| <span data-ttu-id="adb84-147">DLL</span><span class="sxs-lookup"><span data-stu-id="adb84-147">DLL</span></span><br/>                      | <dl> <span data-ttu-id="adb84-148"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="adb84-148"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="adb84-149">IID</span><span class="sxs-lookup"><span data-stu-id="adb84-149">IID</span></span><br/>                      | <span data-ttu-id="adb84-150">IID \_ искардкмд определен как D5778AE3-43DE-11D0-9171-00AA00C18068</span><span class="sxs-lookup"><span data-stu-id="adb84-150">IID\_ISCardCmd is defined as D5778AE3-43DE-11D0-9171-00AA00C18068</span></span><br/>            |



## <a name="see-also"></a><span data-ttu-id="adb84-151">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="adb84-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="adb84-152">**получить \_ категориях APDU**</span><span class="sxs-lookup"><span data-stu-id="adb84-152">**get\_Apdu**</span></span>](iscardcmd-get-apdu.md)
</dt> <dt>

[<span data-ttu-id="adb84-153">**искардкмд**</span><span class="sxs-lookup"><span data-stu-id="adb84-153">**ISCardCmd**</span></span>](iscardcmd.md)
</dt> </dl>

 

 
