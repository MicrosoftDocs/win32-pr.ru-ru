---
description: Извлекает строку ATR смарт-карты.
ms.assetid: 2021bd0c-6ef8-4679-be6c-9a9fd33d9fd6
title: Метод get_Atr. h.
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCard.get_Atr
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 4f2a5688ee85318003ea366bbce614e8250a131a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105651096"
---
# <a name="iscardget_atr-method"></a><span data-ttu-id="2c8f9-103">Метод "кредитной:: Get \_ ATR"</span><span class="sxs-lookup"><span data-stu-id="2c8f9-103">ISCard::get\_Atr method</span></span>

<span data-ttu-id="2c8f9-104">\[Метод **Get \_ ATR** доступен для использования в операционных системах, указанных в разделе требования.</span><span class="sxs-lookup"><span data-stu-id="2c8f9-104">\[The **get\_Atr** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="2c8f9-105">[Модули смарт-карт](/previous-versions/windows/desktop/secsmart/smart-card-modules) предоставляют аналогичные функции.\]</span><span class="sxs-lookup"><span data-stu-id="2c8f9-105">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="2c8f9-106">Метод **Get \_ ATR** извлекает [*строку ATR*](../secgloss/a-gly.md) [*смарт-карты*](../secgloss/s-gly.md).</span><span class="sxs-lookup"><span data-stu-id="2c8f9-106">The **get\_Atr** method retrieves an [*ATR string*](../secgloss/a-gly.md) of the [*smart card*](../secgloss/s-gly.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="2c8f9-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="2c8f9-107">Syntax</span></span>


```C++
HRESULT get_Atr(
  [out] LPBYTEBUFFER *ppAtr
);
```



## <a name="parameters"></a><span data-ttu-id="2c8f9-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="2c8f9-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2c8f9-109">*ппатр* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="2c8f9-109">*ppAtr* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="2c8f9-110">Указатель на байтовый буфер в форме [**IStream**](/windows/win32/api/objidl/nn-objidl-istream) , который будет содержать строку ATR при возврате.</span><span class="sxs-lookup"><span data-stu-id="2c8f9-110">Pointer to a byte buffer in the form of an [**IStream**](/windows/win32/api/objidl/nn-objidl-istream) that will contain the ATR string on return.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2c8f9-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="2c8f9-111">Return value</span></span>

<span data-ttu-id="2c8f9-112">Метод возвращает одно из следующих возможных значений.</span><span class="sxs-lookup"><span data-stu-id="2c8f9-112">The method returns one of the following possible values.</span></span>



| <span data-ttu-id="2c8f9-113">Код возврата</span><span class="sxs-lookup"><span data-stu-id="2c8f9-113">Return code</span></span>                                                                                   | <span data-ttu-id="2c8f9-114">Описание</span><span class="sxs-lookup"><span data-stu-id="2c8f9-114">Description</span></span>                                              |
|-----------------------------------------------------------------------------------------------|----------------------------------------------------------|
| <dl> <span data-ttu-id="2c8f9-115"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="2c8f9-115"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="2c8f9-116">Operation completed successfully (Операция выполнена успешно).</span><span class="sxs-lookup"><span data-stu-id="2c8f9-116">Operation completed successfully.</span></span><br/>             |
| <dl> <span data-ttu-id="2c8f9-117"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="2c8f9-117"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="2c8f9-118">Недопустимый параметр *ппатр* .</span><span class="sxs-lookup"><span data-stu-id="2c8f9-118">The *ppAtr* parameter is not valid.</span></span><br/>           |
| <dl> <span data-ttu-id="2c8f9-119"><dt>**\_указатель E**</dt></span><span class="sxs-lookup"><span data-stu-id="2c8f9-119"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="2c8f9-120">В *ппатр* был передан неверный указатель.</span><span class="sxs-lookup"><span data-stu-id="2c8f9-120">A bad pointer was passed in *ppAtr*.</span></span><br/>          |
| <dl> <span data-ttu-id="2c8f9-121"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="2c8f9-121"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="2c8f9-122">Память для удовлетворения запроса недоступна.</span><span class="sxs-lookup"><span data-stu-id="2c8f9-122">Memory to satisfy the request is unavailable.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="2c8f9-123">Комментарии</span><span class="sxs-lookup"><span data-stu-id="2c8f9-123">Remarks</span></span>

<span data-ttu-id="2c8f9-124">Кроме приведенных выше кодов ошибок COM, этот интерфейс может возвращать код ошибки смарт-карты, если для завершения запроса была вызвана функция смарт-карты.</span><span class="sxs-lookup"><span data-stu-id="2c8f9-124">In addition to the COM error codes listed above, this interface may return a smart card error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="2c8f9-125">Дополнительные сведения см. в статье [возвращаемые значения смарт-карты](authentication-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="2c8f9-125">For more information, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="examples"></a><span data-ttu-id="2c8f9-126">Примеры</span><span class="sxs-lookup"><span data-stu-id="2c8f9-126">Examples</span></span>

<span data-ttu-id="2c8f9-127">В следующем примере показано извлечение строки ATR из смарт-карты.</span><span class="sxs-lookup"><span data-stu-id="2c8f9-127">The following example shows retrieving the ATR string from the smart card.</span></span>


```C++
// Retrieve the ATR.
// pISCard is a pointer to a previously instantiated ISCard.
// pAtr is a pointer to a previously instantiated IByteBuffer.
hr = pISCard->get_Atr(&pAtr);
if (FAILED(hr))
{
    printf("Failed get_Atr\n");
    // Take other error handling action.
}
// Success, you can now use IByteBuffer::Read to access ATR bytes.
BYTE  byAtr[32];
   long  lBytesRead, i;
   // Read the ATR string into a byte array.
   hr = pAtr->Read(byAtr, 32, &lBytesRead);
   // Use the ATR value. (This example merely displays the bytes.)
   for ( i = 0; i < lBytesRead; i++)
       printf("%c", *(byAtr + i));
   printf("\n");
```



## <a name="requirements"></a><span data-ttu-id="2c8f9-128">Требования</span><span class="sxs-lookup"><span data-stu-id="2c8f9-128">Requirements</span></span>



| <span data-ttu-id="2c8f9-129">Требование</span><span class="sxs-lookup"><span data-stu-id="2c8f9-129">Requirement</span></span> | <span data-ttu-id="2c8f9-130">Значение</span><span class="sxs-lookup"><span data-stu-id="2c8f9-130">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="2c8f9-131">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="2c8f9-131">Minimum supported client</span></span><br/> | <span data-ttu-id="2c8f9-132">Только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="2c8f9-132">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="2c8f9-133">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="2c8f9-133">Minimum supported server</span></span><br/> | <span data-ttu-id="2c8f9-134">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="2c8f9-134">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="2c8f9-135">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="2c8f9-135">End of client support</span></span><br/>    | <span data-ttu-id="2c8f9-136">Windows XP</span><span class="sxs-lookup"><span data-stu-id="2c8f9-136">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="2c8f9-137">Поддержка конца сервера</span><span class="sxs-lookup"><span data-stu-id="2c8f9-137">End of server support</span></span><br/>    | <span data-ttu-id="2c8f9-138">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="2c8f9-138">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="2c8f9-139">Header</span><span class="sxs-lookup"><span data-stu-id="2c8f9-139">Header</span></span><br/>                   | <dl> <span data-ttu-id="2c8f9-140"><dt>Скардмгр. h</dt></span><span class="sxs-lookup"><span data-stu-id="2c8f9-140"><dt>Scardmgr.h</dt></span></span> </dl>   |
| <span data-ttu-id="2c8f9-141">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="2c8f9-141">Type library</span></span><br/>             | <dl> <span data-ttu-id="2c8f9-142"><dt>Скардмгр. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="2c8f9-142"><dt>Scardmgr.tlb</dt></span></span> </dl> |
| <span data-ttu-id="2c8f9-143">DLL</span><span class="sxs-lookup"><span data-stu-id="2c8f9-143">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2c8f9-144"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2c8f9-144"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="2c8f9-145">IID</span><span class="sxs-lookup"><span data-stu-id="2c8f9-145">IID</span></span><br/>                      | <span data-ttu-id="2c8f9-146">Идентификатор IID \_ -карты определен как 1461AAC3-6810-11D0-918F-00AA00C18068</span><span class="sxs-lookup"><span data-stu-id="2c8f9-146">IID\_ISCard is defined as 1461AAC3-6810-11D0-918F-00AA00C18068</span></span><br/>               |



## <a name="see-also"></a><span data-ttu-id="2c8f9-147">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="2c8f9-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2c8f9-148">**получить \_ кардхандле**</span><span class="sxs-lookup"><span data-stu-id="2c8f9-148">**get\_CardHandle**</span></span>](iscard-get-cardhandle.md)
</dt> <dt>

[<span data-ttu-id="2c8f9-149">**получить \_ контекст**</span><span class="sxs-lookup"><span data-stu-id="2c8f9-149">**get\_Context**</span></span>](iscard-get-context.md)
</dt> <dt>

[<span data-ttu-id="2c8f9-150">**получить \_ протокол**</span><span class="sxs-lookup"><span data-stu-id="2c8f9-150">**get\_Protocol**</span></span>](iscard-get-protocol.md)
</dt> <dt>

[<span data-ttu-id="2c8f9-151">**получение \_ состояния**</span><span class="sxs-lookup"><span data-stu-id="2c8f9-151">**get\_Status**</span></span>](iscard-get-status.md)
</dt> <dt>

[<span data-ttu-id="2c8f9-152">**Карточка**</span><span class="sxs-lookup"><span data-stu-id="2c8f9-152">**ISCard**</span></span>](iscard.md)
</dt> <dt>

[<span data-ttu-id="2c8f9-153">**Ибитебуффер:: Read**</span><span class="sxs-lookup"><span data-stu-id="2c8f9-153">**IByteBuffer::Read**</span></span>](ibytebuffer-read.md)
</dt> </dl>

 

 
