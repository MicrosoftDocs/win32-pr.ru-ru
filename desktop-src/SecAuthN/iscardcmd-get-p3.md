---
description: Извлекает третий байт параметра (P3) из блока данных протокола приложения (КАТЕГОРИЯХ APDU).
ms.assetid: 5fe90686-f542-42be-91ed-6600eaee3e7b
title: 'Метод Искардкмд:: get_P3 (Скарддат. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardCmd.get_P3
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: b1072fc9c4ca3b2a238cc8893104df1a831c99c9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104145286"
---
# <a name="iscardcmdget_p3-method"></a><span data-ttu-id="321b5-103">Метод Искардкмд:: Get \_ P3</span><span class="sxs-lookup"><span data-stu-id="321b5-103">ISCardCmd::get\_P3 method</span></span>

<span data-ttu-id="321b5-104">\[Метод **Get \_ P3** доступен для использования в операционных системах, указанных в разделе требования.</span><span class="sxs-lookup"><span data-stu-id="321b5-104">\[The **get\_P3** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="321b5-105">Он недоступен для использования в Windows Server 2003 с пакетом обновления 1 (SP1) и более поздней версии, Windows Vista, Windows Server 2008 и последующих версиях операционной системы.</span><span class="sxs-lookup"><span data-stu-id="321b5-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="321b5-106">[Модули смарт-карт](/previous-versions/windows/desktop/secsmart/smart-card-modules) предоставляют аналогичные функции.\]</span><span class="sxs-lookup"><span data-stu-id="321b5-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="321b5-107">Метод **Get \_ P3** извлекает третий байт параметра (P3) из [*блока данных протокола приложения*](../secgloss/a-gly.md) (категориях APDU).</span><span class="sxs-lookup"><span data-stu-id="321b5-107">The **get\_P3** method retrieves the third parameter (P3) byte from the [*application protocol data unit*](../secgloss/a-gly.md) (APDU).</span></span> <span data-ttu-id="321b5-108">Это значение байта только для чтения представляет размер части данных КАТЕГОРИЯХ APDU.</span><span class="sxs-lookup"><span data-stu-id="321b5-108">This read-only byte value represents the size of the data portion of the APDU.</span></span>

## <a name="syntax"></a><span data-ttu-id="321b5-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="321b5-109">Syntax</span></span>


```C++
HRESULT get_P3(
  [out] BYTE *pbyP3
);
```



## <a name="parameters"></a><span data-ttu-id="321b5-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="321b5-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="321b5-111">*pbyP3* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="321b5-111">*pbyP3* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="321b5-112">Указатель на байт, который является P3 из КАТЕГОРИЯХ APDU при возврате.</span><span class="sxs-lookup"><span data-stu-id="321b5-112">Pointer to the byte that is the P3 from the APDU on return.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="321b5-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="321b5-113">Return value</span></span>

<span data-ttu-id="321b5-114">Метод возвращает одно из следующих возможных значений.</span><span class="sxs-lookup"><span data-stu-id="321b5-114">The method returns one of the following possible values.</span></span>



| <span data-ttu-id="321b5-115">Код возврата</span><span class="sxs-lookup"><span data-stu-id="321b5-115">Return code</span></span>                                                                                   | <span data-ttu-id="321b5-116">Описание</span><span class="sxs-lookup"><span data-stu-id="321b5-116">Description</span></span>                                     |
|-----------------------------------------------------------------------------------------------|-------------------------------------------------|
| <dl> <span data-ttu-id="321b5-117"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="321b5-117"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="321b5-118">Operation completed successfully (Операция выполнена успешно).</span><span class="sxs-lookup"><span data-stu-id="321b5-118">Operation completed successfully.</span></span><br/>    |
| <dl> <span data-ttu-id="321b5-119"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="321b5-119"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="321b5-120">Недопустимый *pbyP3* .</span><span class="sxs-lookup"><span data-stu-id="321b5-120">The *pbyP3* is not valid.</span></span><br/>            |
| <dl> <span data-ttu-id="321b5-121"><dt>**\_указатель E**</dt></span><span class="sxs-lookup"><span data-stu-id="321b5-121"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="321b5-122">В *pbyP3* был передан неверный указатель.</span><span class="sxs-lookup"><span data-stu-id="321b5-122">A bad pointer was passed in *pbyP3*.</span></span><br/> |
| <dl> <span data-ttu-id="321b5-123"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="321b5-123"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="321b5-124">Недостаточно памяти.</span><span class="sxs-lookup"><span data-stu-id="321b5-124">Out of memory.</span></span><br/>                       |



 

## <a name="remarks"></a><span data-ttu-id="321b5-125">Комментарии</span><span class="sxs-lookup"><span data-stu-id="321b5-125">Remarks</span></span>

<span data-ttu-id="321b5-126">Параметр P3 доступен только для чтения и поэтому не может быть установлен.</span><span class="sxs-lookup"><span data-stu-id="321b5-126">The P3 parameter is read-only, and therefore cannot be set.</span></span>

<span data-ttu-id="321b5-127">Чтобы получить параметры P1 или P2, вызовите [**Get \_ P1**](iscardcmd-get-p1.md) и [**Get \_ P2**](iscardcmd-get-p2.md) соответственно.</span><span class="sxs-lookup"><span data-stu-id="321b5-127">To get the P1 or P2 parameters, call [**get\_P1**](iscardcmd-get-p1.md) and [**get\_P2**](iscardcmd-get-p2.md) respectively.</span></span>

<span data-ttu-id="321b5-128">Список всех методов, предоставляемых этим интерфейсом, см. в разделе [**искардкмд**](iscardcmd.md).</span><span class="sxs-lookup"><span data-stu-id="321b5-128">For a list of all the methods provided by this interface, see [**ISCardCmd**](iscardcmd.md).</span></span>

<span data-ttu-id="321b5-129">Кроме приведенных выше кодов ошибок COM, этот интерфейс может возвращать код ошибки [*смарт-карты*](../secgloss/s-gly.md) , если для завершения запроса была вызвана функция смарт-карты.</span><span class="sxs-lookup"><span data-stu-id="321b5-129">In addition to the COM error codes listed above, this interface may return a [*smart card*](../secgloss/s-gly.md) error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="321b5-130">Дополнительные сведения см. в статье [возвращаемые значения смарт-карты](authentication-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="321b5-130">For more information, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="examples"></a><span data-ttu-id="321b5-131">Примеры</span><span class="sxs-lookup"><span data-stu-id="321b5-131">Examples</span></span>

<span data-ttu-id="321b5-132">В следующем примере показано, как получить байт третьего параметра (P3) из [*блока данных протокола приложения*](../secgloss/a-gly.md) (категориях APDU).</span><span class="sxs-lookup"><span data-stu-id="321b5-132">The following example shows how to retrieve the third parameter (P3) byte from the [*application protocol data unit*](../secgloss/a-gly.md) (APDU).</span></span> <span data-ttu-id="321b5-133">В примере предполагается, что Пискардкмд является допустимым указателем на экземпляр интерфейса [**искардкмд**](iscardcmd.md) .</span><span class="sxs-lookup"><span data-stu-id="321b5-133">The example assumes that pISCardCmd is a valid pointer to an instance of the [**ISCardCmd**](iscardcmd.md) interface.</span></span>


```C++
BYTE  byP3;
HRESULT  hr;

// Retrieve the P3 byte.
hr = pISCardCmd->get_P3(&byP3);
if (FAILED(hr))
{
  printf("Failed get_P3\n");
  // Take other error handling action as needed.
}
```



## <a name="requirements"></a><span data-ttu-id="321b5-134">Требования</span><span class="sxs-lookup"><span data-stu-id="321b5-134">Requirements</span></span>



| <span data-ttu-id="321b5-135">Требование</span><span class="sxs-lookup"><span data-stu-id="321b5-135">Requirement</span></span> | <span data-ttu-id="321b5-136">Значение</span><span class="sxs-lookup"><span data-stu-id="321b5-136">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="321b5-137">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="321b5-137">Minimum supported client</span></span><br/> | <span data-ttu-id="321b5-138">Только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="321b5-138">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="321b5-139">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="321b5-139">Minimum supported server</span></span><br/> | <span data-ttu-id="321b5-140">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="321b5-140">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="321b5-141">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="321b5-141">End of client support</span></span><br/>    | <span data-ttu-id="321b5-142">Windows XP</span><span class="sxs-lookup"><span data-stu-id="321b5-142">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="321b5-143">Поддержка конца сервера</span><span class="sxs-lookup"><span data-stu-id="321b5-143">End of server support</span></span><br/>    | <span data-ttu-id="321b5-144">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="321b5-144">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="321b5-145">Header</span><span class="sxs-lookup"><span data-stu-id="321b5-145">Header</span></span><br/>                   | <dl> <span data-ttu-id="321b5-146"><dt>Скарддат. h</dt></span><span class="sxs-lookup"><span data-stu-id="321b5-146"><dt>Scarddat.h</dt></span></span> </dl>   |
| <span data-ttu-id="321b5-147">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="321b5-147">Type library</span></span><br/>             | <dl> <span data-ttu-id="321b5-148"><dt>Скарддат. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="321b5-148"><dt>Scarddat.tlb</dt></span></span> </dl> |
| <span data-ttu-id="321b5-149">DLL</span><span class="sxs-lookup"><span data-stu-id="321b5-149">DLL</span></span><br/>                      | <dl> <span data-ttu-id="321b5-150"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="321b5-150"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="321b5-151">IID</span><span class="sxs-lookup"><span data-stu-id="321b5-151">IID</span></span><br/>                      | <span data-ttu-id="321b5-152">IID \_ искардкмд определен как D5778AE3-43DE-11D0-9171-00AA00C18068</span><span class="sxs-lookup"><span data-stu-id="321b5-152">IID\_ISCardCmd is defined as D5778AE3-43DE-11D0-9171-00AA00C18068</span></span><br/>            |



## <a name="see-also"></a><span data-ttu-id="321b5-153">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="321b5-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="321b5-154">**получить \_ P1**</span><span class="sxs-lookup"><span data-stu-id="321b5-154">**get\_P1**</span></span>](iscardcmd-get-p1.md)
</dt> <dt>

[<span data-ttu-id="321b5-155">**получить \_ P2**</span><span class="sxs-lookup"><span data-stu-id="321b5-155">**get\_P2**</span></span>](iscardcmd-get-p2.md)
</dt> <dt>

[<span data-ttu-id="321b5-156">**искардкмд**</span><span class="sxs-lookup"><span data-stu-id="321b5-156">**ISCardCmd**</span></span>](iscardcmd.md)
</dt> </dl>

 

 
