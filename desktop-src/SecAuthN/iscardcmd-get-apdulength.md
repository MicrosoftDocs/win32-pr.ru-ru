---
description: Определяет длину (в байтах) f в блоке данных протокола приложения (КАТЕГОРИЯХ APDU).
ms.assetid: 005345d0-afdd-4534-9926-12378546d0ef
title: 'Метод Искардкмд:: get_ApduLength (Скарддат. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardCmd.get_ApduLength
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 1535d2b4b67861b42719506ebd48cca4c49d5c38
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103818512"
---
# <a name="iscardcmdget_apdulength-method"></a><span data-ttu-id="d1aa3-103">Метод Искардкмд:: Get \_ апдуленгс</span><span class="sxs-lookup"><span data-stu-id="d1aa3-103">ISCardCmd::get\_ApduLength method</span></span>

<span data-ttu-id="d1aa3-104">\[Метод **Get \_ апдуленгс** доступен для использования в операционных системах, указанных в разделе требования.</span><span class="sxs-lookup"><span data-stu-id="d1aa3-104">\[The **get\_ApduLength** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="d1aa3-105">Он недоступен для использования в Windows Server 2003 с пакетом обновления 1 (SP1) и более поздней версии, Windows Vista, Windows Server 2008 и последующих версиях операционной системы.</span><span class="sxs-lookup"><span data-stu-id="d1aa3-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="d1aa3-106">[Модули смарт-карт](/previous-versions/windows/desktop/secsmart/smart-card-modules) предоставляют аналогичные функции.\]</span><span class="sxs-lookup"><span data-stu-id="d1aa3-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="d1aa3-107">Метод **Get \_ апдуленгс** определяет длину (в байтах) f в [*блоке данных протокола приложения*](../secgloss/a-gly.md) (категориях APDU).</span><span class="sxs-lookup"><span data-stu-id="d1aa3-107">The **get\_ApduLength** method determines the length, in bytes, f the [*application protocol data unit*](../secgloss/a-gly.md) (APDU).</span></span>

## <a name="syntax"></a><span data-ttu-id="d1aa3-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="d1aa3-108">Syntax</span></span>


```C++
HRESULT get_ApduLength(
  [out] LONG *plSize
);
```



## <a name="parameters"></a><span data-ttu-id="d1aa3-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="d1aa3-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d1aa3-110">*плсизе* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="d1aa3-110">*plSize* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d1aa3-111">Указатель на длину КАТЕГОРИЯХ APDU.</span><span class="sxs-lookup"><span data-stu-id="d1aa3-111">Pointer to the length of the APDU.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d1aa3-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="d1aa3-112">Return value</span></span>

<span data-ttu-id="d1aa3-113">Метод возвращает одно из следующих возможных значений.</span><span class="sxs-lookup"><span data-stu-id="d1aa3-113">The method returns one of the following possible values.</span></span>



| <span data-ttu-id="d1aa3-114">Код возврата</span><span class="sxs-lookup"><span data-stu-id="d1aa3-114">Return code</span></span>                                                                                   | <span data-ttu-id="d1aa3-115">Описание</span><span class="sxs-lookup"><span data-stu-id="d1aa3-115">Description</span></span>                                      |
|-----------------------------------------------------------------------------------------------|--------------------------------------------------|
| <dl> <span data-ttu-id="d1aa3-116"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="d1aa3-116"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="d1aa3-117">Operation completed successfully (Операция выполнена успешно).</span><span class="sxs-lookup"><span data-stu-id="d1aa3-117">Operation completed successfully.</span></span><br/>     |
| <dl> <span data-ttu-id="d1aa3-118"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="d1aa3-118"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="d1aa3-119">Недопустимый параметр *плсизе* .</span><span class="sxs-lookup"><span data-stu-id="d1aa3-119">The *plSize* parameter is not valid.</span></span><br/>  |
| <dl> <span data-ttu-id="d1aa3-120"><dt>**\_указатель E**</dt></span><span class="sxs-lookup"><span data-stu-id="d1aa3-120"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="d1aa3-121">В *плсизе* был передан неверный указатель.</span><span class="sxs-lookup"><span data-stu-id="d1aa3-121">A bad pointer was passed in *plSize*.</span></span><br/> |
| <dl> <span data-ttu-id="d1aa3-122"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="d1aa3-122"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="d1aa3-123">Недостаточно памяти.</span><span class="sxs-lookup"><span data-stu-id="d1aa3-123">Out of memory.</span></span><br/>                        |



 

## <a name="remarks"></a><span data-ttu-id="d1aa3-124">Комментарии</span><span class="sxs-lookup"><span data-stu-id="d1aa3-124">Remarks</span></span>

<span data-ttu-id="d1aa3-125">Чтобы получить необработанную [*единицу данных протокола приложения*](../secgloss/a-gly.md) (категориях APDU) из буфера байтов, сопоставленного с помощью **IStream** , содержащего сообщение категориях APDU, вызовите [**Get \_ категориях APDU**](iscardcmd-get-apdu.md).</span><span class="sxs-lookup"><span data-stu-id="d1aa3-125">To retrieve the raw [*application protocol data unit*](../secgloss/a-gly.md) (APDU) from the byte buffer mapped through an **IStream** that contains the APDU message, call [**get\_Apdu**](iscardcmd-get-apdu.md).</span></span>

<span data-ttu-id="d1aa3-126">Список всех методов, предоставляемых этим интерфейсом, см. в разделе [**искардкмд**](iscardcmd.md).</span><span class="sxs-lookup"><span data-stu-id="d1aa3-126">For a list of all the methods provided by this interface, see [**ISCardCmd**](iscardcmd.md).</span></span>

<span data-ttu-id="d1aa3-127">Кроме приведенных выше кодов ошибок COM, этот интерфейс может возвращать код ошибки смарт-карты, если для завершения запроса была вызвана функция смарт-карты.</span><span class="sxs-lookup"><span data-stu-id="d1aa3-127">In addition to the COM error codes listed above, this interface may return a smart card error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="d1aa3-128">Дополнительные сведения см. в статье [возвращаемые значения смарт-карты](authentication-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="d1aa3-128">For more information, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="examples"></a><span data-ttu-id="d1aa3-129">Примеры</span><span class="sxs-lookup"><span data-stu-id="d1aa3-129">Examples</span></span>

<span data-ttu-id="d1aa3-130">В следующем примере показано, как получить длину [*единицы данных протокола приложения*](../secgloss/a-gly.md) (категориях APDU).</span><span class="sxs-lookup"><span data-stu-id="d1aa3-130">The following example shows how to retrieve the [*application protocol data unit*](../secgloss/a-gly.md) (APDU) length.</span></span> <span data-ttu-id="d1aa3-131">В примере предполагается, что Пискардкмд является допустимым указателем на экземпляр интерфейса [**искардкмд**](iscardcmd.md) .</span><span class="sxs-lookup"><span data-stu-id="d1aa3-131">The example assumes that pISCardCmd is a valid pointer to an instance of the [**ISCardCmd**](iscardcmd.md) interface.</span></span>


```C++
LONG    lLen;
HRESULT hr;

// Retrieve the APDU length.
hr = pISCardCmd->get_ApduLength(&lLen);
if (FAILED(hr))
{
    printf("Failed get_ApduLength\n");
    // Take other error handling action.
}
else
    printf("Length returned is %d\n", lLen);
```



## <a name="requirements"></a><span data-ttu-id="d1aa3-132">Требования</span><span class="sxs-lookup"><span data-stu-id="d1aa3-132">Requirements</span></span>



| <span data-ttu-id="d1aa3-133">Требование</span><span class="sxs-lookup"><span data-stu-id="d1aa3-133">Requirement</span></span> | <span data-ttu-id="d1aa3-134">Значение</span><span class="sxs-lookup"><span data-stu-id="d1aa3-134">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d1aa3-135">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="d1aa3-135">Minimum supported client</span></span><br/> | <span data-ttu-id="d1aa3-136">Только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="d1aa3-136">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="d1aa3-137">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="d1aa3-137">Minimum supported server</span></span><br/> | <span data-ttu-id="d1aa3-138">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="d1aa3-138">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="d1aa3-139">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="d1aa3-139">End of client support</span></span><br/>    | <span data-ttu-id="d1aa3-140">Windows XP</span><span class="sxs-lookup"><span data-stu-id="d1aa3-140">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="d1aa3-141">Поддержка конца сервера</span><span class="sxs-lookup"><span data-stu-id="d1aa3-141">End of server support</span></span><br/>    | <span data-ttu-id="d1aa3-142">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="d1aa3-142">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="d1aa3-143">Header</span><span class="sxs-lookup"><span data-stu-id="d1aa3-143">Header</span></span><br/>                   | <dl> <span data-ttu-id="d1aa3-144"><dt>Скарддат. h</dt></span><span class="sxs-lookup"><span data-stu-id="d1aa3-144"><dt>Scarddat.h</dt></span></span> </dl>   |
| <span data-ttu-id="d1aa3-145">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="d1aa3-145">Type library</span></span><br/>             | <dl> <span data-ttu-id="d1aa3-146"><dt>Скарддат. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="d1aa3-146"><dt>Scarddat.tlb</dt></span></span> </dl> |
| <span data-ttu-id="d1aa3-147">DLL</span><span class="sxs-lookup"><span data-stu-id="d1aa3-147">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d1aa3-148"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d1aa3-148"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="d1aa3-149">IID</span><span class="sxs-lookup"><span data-stu-id="d1aa3-149">IID</span></span><br/>                      | <span data-ttu-id="d1aa3-150">IID \_ искардкмд определен как D5778AE3-43DE-11D0-9171-00AA00C18068</span><span class="sxs-lookup"><span data-stu-id="d1aa3-150">IID\_ISCardCmd is defined as D5778AE3-43DE-11D0-9171-00AA00C18068</span></span><br/>            |



## <a name="see-also"></a><span data-ttu-id="d1aa3-151">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="d1aa3-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d1aa3-152">**получить \_ категориях APDU**</span><span class="sxs-lookup"><span data-stu-id="d1aa3-152">**get\_Apdu**</span></span>](iscardcmd-get-apdu.md)
</dt> <dt>

[<span data-ttu-id="d1aa3-153">**искардкмд**</span><span class="sxs-lookup"><span data-stu-id="d1aa3-153">**ISCardCmd**</span></span>](iscardcmd.md)
</dt> </dl>

 

 
