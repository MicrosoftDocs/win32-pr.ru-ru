---
description: Извлекает поле данных из блока данных протокола приложения (КАТЕГОРИЯХ APDU), помещая его в объект байтового буфера.
ms.assetid: fbffeeeb-56e5-4484-b294-8b6f59c919eb
title: 'Метод Искардкмд:: get_Data (Скарддат. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardCmd.get_Data
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: feb6a8c28316bd4fd08160063606d3e15054fd87
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104546986"
---
# <a name="iscardcmdget_data-method"></a><span data-ttu-id="fbd24-103">Метод Искардкмд:: Get \_ Data</span><span class="sxs-lookup"><span data-stu-id="fbd24-103">ISCardCmd::get\_Data method</span></span>

<span data-ttu-id="fbd24-104">\[Метод **Get \_ Data** доступен для использования в операционных системах, указанных в разделе требования.</span><span class="sxs-lookup"><span data-stu-id="fbd24-104">\[The **get\_Data** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="fbd24-105">Он недоступен для использования в Windows Server 2003 с пакетом обновления 1 (SP1) и более поздней версии, Windows Vista, Windows Server 2008 и последующих версиях операционной системы.</span><span class="sxs-lookup"><span data-stu-id="fbd24-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="fbd24-106">[Модули смарт-карт](/previous-versions/windows/desktop/secsmart/smart-card-modules) предоставляют аналогичные функции.\]</span><span class="sxs-lookup"><span data-stu-id="fbd24-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="fbd24-107">Метод **Get \_ Data** извлекает поле данных из [*блока данных протокола приложения*](../secgloss/a-gly.md) (категориях APDU), помещая его в объект байтового буфера.</span><span class="sxs-lookup"><span data-stu-id="fbd24-107">The **get\_Data** method retrieves the data field from the [*application protocol data unit*](../secgloss/a-gly.md) (APDU), placing it in a byte buffer object.</span></span>

## <a name="syntax"></a><span data-ttu-id="fbd24-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="fbd24-108">Syntax</span></span>


```C++
HRESULT get_Data(
  [out] LPBYTEBUFFER *ppData
);
```



## <a name="parameters"></a><span data-ttu-id="fbd24-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="fbd24-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fbd24-110">*ппдата* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="fbd24-110">*ppData* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="fbd24-111">Указатель на объект буфера байтов (**IStream**), содержащий поле данных категориях APDU при возврате.</span><span class="sxs-lookup"><span data-stu-id="fbd24-111">Pointer to the byte buffer object (**IStream**) that holds the APDU data field on return.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fbd24-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="fbd24-112">Return value</span></span>

<span data-ttu-id="fbd24-113">Метод возвращает одно из следующих возможных значений.</span><span class="sxs-lookup"><span data-stu-id="fbd24-113">The method returns one of the following possible values.</span></span>



| <span data-ttu-id="fbd24-114">Код возврата</span><span class="sxs-lookup"><span data-stu-id="fbd24-114">Return code</span></span>                                                                                   | <span data-ttu-id="fbd24-115">Описание</span><span class="sxs-lookup"><span data-stu-id="fbd24-115">Description</span></span>                                      |
|-----------------------------------------------------------------------------------------------|--------------------------------------------------|
| <dl> <span data-ttu-id="fbd24-116"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="fbd24-116"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="fbd24-117">Operation completed successfully (Операция выполнена успешно).</span><span class="sxs-lookup"><span data-stu-id="fbd24-117">Operation completed successfully.</span></span><br/>     |
| <dl> <span data-ttu-id="fbd24-118"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="fbd24-118"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="fbd24-119">Недопустимый параметр *ппдата* .</span><span class="sxs-lookup"><span data-stu-id="fbd24-119">The *ppData* parameter is not valid.</span></span><br/>  |
| <dl> <span data-ttu-id="fbd24-120"><dt>**\_указатель E**</dt></span><span class="sxs-lookup"><span data-stu-id="fbd24-120"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="fbd24-121">В *ппдата* был передан неверный указатель.</span><span class="sxs-lookup"><span data-stu-id="fbd24-121">A bad pointer was passed in *ppData*.</span></span><br/> |
| <dl> <span data-ttu-id="fbd24-122"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="fbd24-122"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="fbd24-123">Недостаточно памяти.</span><span class="sxs-lookup"><span data-stu-id="fbd24-123">Out of memory.</span></span><br/>                        |



 

## <a name="remarks"></a><span data-ttu-id="fbd24-124">Комментарии</span><span class="sxs-lookup"><span data-stu-id="fbd24-124">Remarks</span></span>

<span data-ttu-id="fbd24-125">Чтобы задать поле данных КАТЕГОРИЯХ APDU, вызовите метод Set [**\_ Data**](iscardcmd-put-data.md).</span><span class="sxs-lookup"><span data-stu-id="fbd24-125">To set the data field of the APDU, call [**put\_Data**](iscardcmd-put-data.md).</span></span>

<span data-ttu-id="fbd24-126">Список всех методов, предоставляемых этим интерфейсом, см. в разделе [**искардкмд**](iscardcmd.md).</span><span class="sxs-lookup"><span data-stu-id="fbd24-126">For a list of all the methods provided by this interface, see [**ISCardCmd**](iscardcmd.md).</span></span>

<span data-ttu-id="fbd24-127">Кроме приведенных выше кодов ошибок COM, этот интерфейс может возвращать код ошибки [*смарт-карты*](../secgloss/s-gly.md) , если для завершения запроса была вызвана функция смарт-карты.</span><span class="sxs-lookup"><span data-stu-id="fbd24-127">In addition to the COM error codes listed above, this interface may return a [*smart card*](../secgloss/s-gly.md) error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="fbd24-128">Дополнительные сведения см. в статье [возвращаемые значения смарт-карты](authentication-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="fbd24-128">For more information, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="examples"></a><span data-ttu-id="fbd24-129">Примеры</span><span class="sxs-lookup"><span data-stu-id="fbd24-129">Examples</span></span>

<span data-ttu-id="fbd24-130">В следующем примере показано, как получить поле данных в [*блоке данных протокола приложения*](../secgloss/a-gly.md) (категориях APDU).</span><span class="sxs-lookup"><span data-stu-id="fbd24-130">The following example shows how to retrieve the data field of the [*application protocol data unit*](../secgloss/a-gly.md) (APDU).</span></span> <span data-ttu-id="fbd24-131">В примере предполагается, что Пибитедата является допустимым указателем на экземпляр интерфейса [**ибитебуффер**](ibytebuffer.md) , а пискардкмд является допустимым указателем на экземпляр интерфейса [**искардкмд**](iscardcmd.md) .</span><span class="sxs-lookup"><span data-stu-id="fbd24-131">The example assumes that pIByteData is a valid pointer to an instance of the [**IByteBuffer**](ibytebuffer.md) interface, and that pISCardCmd is a valid pointer to an instance of the [**ISCardCmd**](iscardcmd.md) interface.</span></span>


```C++
HRESULT    hr;

// pIByteData is a pointer to an instance of IByteBuffer.
// Retrieve the data.
hr = pISCardCmd->get_Data(&pIByteData);
if (FAILED(hr)) 
{
    printf("Failed get_Data.\n");
    // Take other error handling action as needed.
}
```



## <a name="requirements"></a><span data-ttu-id="fbd24-132">Требования</span><span class="sxs-lookup"><span data-stu-id="fbd24-132">Requirements</span></span>



| <span data-ttu-id="fbd24-133">Требование</span><span class="sxs-lookup"><span data-stu-id="fbd24-133">Requirement</span></span> | <span data-ttu-id="fbd24-134">Значение</span><span class="sxs-lookup"><span data-stu-id="fbd24-134">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="fbd24-135">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="fbd24-135">Minimum supported client</span></span><br/> | <span data-ttu-id="fbd24-136">Только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="fbd24-136">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="fbd24-137">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="fbd24-137">Minimum supported server</span></span><br/> | <span data-ttu-id="fbd24-138">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="fbd24-138">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="fbd24-139">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="fbd24-139">End of client support</span></span><br/>    | <span data-ttu-id="fbd24-140">Windows XP</span><span class="sxs-lookup"><span data-stu-id="fbd24-140">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="fbd24-141">Поддержка конца сервера</span><span class="sxs-lookup"><span data-stu-id="fbd24-141">End of server support</span></span><br/>    | <span data-ttu-id="fbd24-142">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="fbd24-142">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="fbd24-143">Header</span><span class="sxs-lookup"><span data-stu-id="fbd24-143">Header</span></span><br/>                   | <dl> <span data-ttu-id="fbd24-144"><dt>Скарддат. h</dt></span><span class="sxs-lookup"><span data-stu-id="fbd24-144"><dt>Scarddat.h</dt></span></span> </dl>   |
| <span data-ttu-id="fbd24-145">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="fbd24-145">Type library</span></span><br/>             | <dl> <span data-ttu-id="fbd24-146"><dt>Скарддат. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="fbd24-146"><dt>Scarddat.tlb</dt></span></span> </dl> |
| <span data-ttu-id="fbd24-147">DLL</span><span class="sxs-lookup"><span data-stu-id="fbd24-147">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fbd24-148"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fbd24-148"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="fbd24-149">IID</span><span class="sxs-lookup"><span data-stu-id="fbd24-149">IID</span></span><br/>                      | <span data-ttu-id="fbd24-150">IID \_ искардкмд определен как D5778AE3-43DE-11D0-9171-00AA00C18068</span><span class="sxs-lookup"><span data-stu-id="fbd24-150">IID\_ISCardCmd is defined as D5778AE3-43DE-11D0-9171-00AA00C18068</span></span><br/>            |



## <a name="see-also"></a><span data-ttu-id="fbd24-151">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="fbd24-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fbd24-152">**искардкмд**</span><span class="sxs-lookup"><span data-stu-id="fbd24-152">**ISCardCmd**</span></span>](iscardcmd.md)
</dt> <dt>

[<span data-ttu-id="fbd24-153">**Размещение \_ данных**</span><span class="sxs-lookup"><span data-stu-id="fbd24-153">**put\_Data**</span></span>](iscardcmd-put-data.md)
</dt> </dl>

 

 
