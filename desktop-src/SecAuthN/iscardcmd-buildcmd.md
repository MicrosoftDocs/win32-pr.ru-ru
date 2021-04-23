---
description: Создание допустимой единицы данных протокола командного приложения (КАТЕГОРИЯХ APDU) для передачи на смарт-карту.
ms.assetid: d1003cc3-c235-4635-ad5a-8cea7363bf30
title: 'Метод Искардкмд:: Буилдкмд (Скарддат. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardCmd.BuildCmd
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: f44597ea087f7ccec191abc9dd03787780e88b2d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104265647"
---
# <a name="iscardcmdbuildcmd-method"></a><span data-ttu-id="08a72-103">Метод Искардкмд:: Буилдкмд</span><span class="sxs-lookup"><span data-stu-id="08a72-103">ISCardCmd::BuildCmd method</span></span>

<span data-ttu-id="08a72-104">\[Метод **буилдкмд** доступен для использования в операционных системах, указанных в разделе требования.</span><span class="sxs-lookup"><span data-stu-id="08a72-104">\[The **BuildCmd** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="08a72-105">Он недоступен для использования в Windows Server 2003 с пакетом обновления 1 (SP1) и более поздней версии, Windows Vista, Windows Server 2008 и последующих версиях операционной системы.</span><span class="sxs-lookup"><span data-stu-id="08a72-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="08a72-106">[Модули смарт-карт](/previous-versions/windows/desktop/secsmart/smart-card-modules) предоставляют аналогичные функции.\]</span><span class="sxs-lookup"><span data-stu-id="08a72-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="08a72-107">Метод **буилдкмд** конструирует допустимую [*единицу данных протокола приложения*](../secgloss/a-gly.md) (категориях APDU) для передачи на [*смарт-карту*](../secgloss/s-gly.md).</span><span class="sxs-lookup"><span data-stu-id="08a72-107">The **BuildCmd** method constructs a valid command [*application protocol data unit*](../secgloss/a-gly.md) (APDU) for transmission to a [*smart card*](../secgloss/s-gly.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="08a72-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="08a72-108">Syntax</span></span>


```C++
HRESULT BuildCmd(
  [in] BYTE         byClassId,
  [in] BYTE         byInsId,
  [in] BYTE         byP1,
  [in] BYTE         byP2,
  [in] LPBYTEBUFFER pbyData,
  [in] LONG         *p1Le
);
```



## <a name="parameters"></a><span data-ttu-id="08a72-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="08a72-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="08a72-110">*биклассид* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="08a72-110">*byClassId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="08a72-111">Идентификатор класса команд.</span><span class="sxs-lookup"><span data-stu-id="08a72-111">Command class identifier.</span></span>

</dd> <dt>

<span data-ttu-id="08a72-112">*бинсид* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="08a72-112">*byInsId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="08a72-113">Идентификатор инструкции команды.</span><span class="sxs-lookup"><span data-stu-id="08a72-113">Command instruction identifier.</span></span>

</dd> <dt>

<span data-ttu-id="08a72-114">*byP1* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="08a72-114">*byP1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="08a72-115">Первый параметр команды.</span><span class="sxs-lookup"><span data-stu-id="08a72-115">Command's first parameter.</span></span>

</dd> <dt>

<span data-ttu-id="08a72-116">*byP2* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="08a72-116">*byP2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="08a72-117">Второй параметр команды.</span><span class="sxs-lookup"><span data-stu-id="08a72-117">Command's second parameter.</span></span>

</dd> <dt>

<span data-ttu-id="08a72-118">*пбидата* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="08a72-118">*pbyData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="08a72-119">Указатель на часть данных команды.</span><span class="sxs-lookup"><span data-stu-id="08a72-119">Pointer to the data portion of the command.</span></span>

</dd> <dt>

<span data-ttu-id="08a72-120">*p1Le* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="08a72-120">*p1Le* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="08a72-121">Указатель на ДЛИННое целое число, содержащее ожидаемую длину возвращаемых данных.</span><span class="sxs-lookup"><span data-stu-id="08a72-121">Pointer to a LONG integer containing the expected length of the returned data.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="08a72-122">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="08a72-122">Return value</span></span>

<span data-ttu-id="08a72-123">Метод возвращает одно из следующих возможных значений.</span><span class="sxs-lookup"><span data-stu-id="08a72-123">The method returns one of the following possible values.</span></span>



| <span data-ttu-id="08a72-124">Код возврата</span><span class="sxs-lookup"><span data-stu-id="08a72-124">Return code</span></span>                                                                                   | <span data-ttu-id="08a72-125">Описание</span><span class="sxs-lookup"><span data-stu-id="08a72-125">Description</span></span>                                    |
|-----------------------------------------------------------------------------------------------|------------------------------------------------|
| <dl> <span data-ttu-id="08a72-126"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="08a72-126"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="08a72-127">Operation completed successfully (Операция выполнена успешно).</span><span class="sxs-lookup"><span data-stu-id="08a72-127">Operation completed successfully.</span></span><br/>   |
| <dl> <span data-ttu-id="08a72-128"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="08a72-128"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="08a72-129">Один из параметров недопустим.</span><span class="sxs-lookup"><span data-stu-id="08a72-129">One of the parameters is not valid.</span></span><br/> |
| <dl> <span data-ttu-id="08a72-130"><dt>**\_указатель E**</dt></span><span class="sxs-lookup"><span data-stu-id="08a72-130"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="08a72-131">Передан неверный указатель.</span><span class="sxs-lookup"><span data-stu-id="08a72-131">A bad pointer was passed in.</span></span><br/>        |
| <dl> <span data-ttu-id="08a72-132"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="08a72-132"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="08a72-133">Недостаточно памяти.</span><span class="sxs-lookup"><span data-stu-id="08a72-133">Out of memory.</span></span><br/>                      |



 

## <a name="remarks"></a><span data-ttu-id="08a72-134">Комментарии</span><span class="sxs-lookup"><span data-stu-id="08a72-134">Remarks</span></span>

<span data-ttu-id="08a72-135">Чтобы инкапсулировать команду в другую команду, вызовите функцию [**Инкапсуляция**](iscardcmd-encapsulate.md).</span><span class="sxs-lookup"><span data-stu-id="08a72-135">To encapsulate the command into another command, call [**Encapsulate**](iscardcmd-encapsulate.md).</span></span>

<span data-ttu-id="08a72-136">Список всех методов, предоставляемых этим интерфейсом, см. в разделе [**искардкмд**](iscardcmd.md).</span><span class="sxs-lookup"><span data-stu-id="08a72-136">For a list of all the methods provided by this interface, see [**ISCardCmd**](iscardcmd.md).</span></span>

<span data-ttu-id="08a72-137">Кроме приведенных выше кодов ошибок COM, этот интерфейс может возвращать код ошибки смарт-карты, если для завершения запроса была вызвана функция смарт-карты.</span><span class="sxs-lookup"><span data-stu-id="08a72-137">In addition to the COM error codes listed above, this interface may return a smart card error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="08a72-138">Дополнительные сведения см. в статье [возвращаемые значения смарт-карты](authentication-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="08a72-138">For more information, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="examples"></a><span data-ttu-id="08a72-139">Примеры</span><span class="sxs-lookup"><span data-stu-id="08a72-139">Examples</span></span>

<span data-ttu-id="08a72-140">В следующем примере показано, как создать команду КАТЕГОРИЯХ APDU.</span><span class="sxs-lookup"><span data-stu-id="08a72-140">The following example shows how to construct a command APDU.</span></span> <span data-ttu-id="08a72-141">В этом примере предполагается, что Пискардкмд является допустимым указателем на экземпляр интерфейса [**искардкмд**](iscardcmd.md) , а пибитерекуест является допустимым указателем на экземпляр интерфейса [**ибитебуффер**](ibytebuffer.md) , инициализированного предыдущим вызовом метода [**ибитебуффер:: Initialize**](ibytebuffer-initialize.md) .</span><span class="sxs-lookup"><span data-stu-id="08a72-141">The example assumes that pISCardCmd is a valid pointer to an instance of the [**ISCardCmd**](iscardcmd.md) interface and that pIByteRequest is a valid pointer to an instance of the [**IByteBuffer**](ibytebuffer.md) interface initialized with a previous call to the [**IByteBuffer::Initialize**](ibytebuffer-initialize.md) method.</span></span>


```C++
LONG       lLe = 0;
HRESULT    hr;

hr = pISCardCmd->BuildCmd(0x00,   // Some cards prefer 0xC0
                          0xa4,   // 'Select File'
                          0x00,
                          0x00,
                          pIByteRequest,
                          &lLe);
if (FAILED(hr))
{
    printf("Failed ISCardCmd::BuildCmd\n");
    // Take other error handling action as needed.
}
```



## <a name="requirements"></a><span data-ttu-id="08a72-142">Требования</span><span class="sxs-lookup"><span data-stu-id="08a72-142">Requirements</span></span>



| <span data-ttu-id="08a72-143">Требование</span><span class="sxs-lookup"><span data-stu-id="08a72-143">Requirement</span></span> | <span data-ttu-id="08a72-144">Значение</span><span class="sxs-lookup"><span data-stu-id="08a72-144">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="08a72-145">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="08a72-145">Minimum supported client</span></span><br/> | <span data-ttu-id="08a72-146">Только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="08a72-146">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="08a72-147">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="08a72-147">Minimum supported server</span></span><br/> | <span data-ttu-id="08a72-148">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="08a72-148">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="08a72-149">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="08a72-149">End of client support</span></span><br/>    | <span data-ttu-id="08a72-150">Windows XP</span><span class="sxs-lookup"><span data-stu-id="08a72-150">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="08a72-151">Поддержка конца сервера</span><span class="sxs-lookup"><span data-stu-id="08a72-151">End of server support</span></span><br/>    | <span data-ttu-id="08a72-152">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="08a72-152">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="08a72-153">Header</span><span class="sxs-lookup"><span data-stu-id="08a72-153">Header</span></span><br/>                   | <dl> <span data-ttu-id="08a72-154"><dt>Скарддат. h</dt></span><span class="sxs-lookup"><span data-stu-id="08a72-154"><dt>Scarddat.h</dt></span></span> </dl>   |
| <span data-ttu-id="08a72-155">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="08a72-155">Type library</span></span><br/>             | <dl> <span data-ttu-id="08a72-156"><dt>Скарддат. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="08a72-156"><dt>Scarddat.tlb</dt></span></span> </dl> |
| <span data-ttu-id="08a72-157">DLL</span><span class="sxs-lookup"><span data-stu-id="08a72-157">DLL</span></span><br/>                      | <dl> <span data-ttu-id="08a72-158"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="08a72-158"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="08a72-159">IID</span><span class="sxs-lookup"><span data-stu-id="08a72-159">IID</span></span><br/>                      | <span data-ttu-id="08a72-160">IID \_ искардкмд определен как D5778AE3-43DE-11D0-9171-00AA00C18068</span><span class="sxs-lookup"><span data-stu-id="08a72-160">IID\_ISCardCmd is defined as D5778AE3-43DE-11D0-9171-00AA00C18068</span></span><br/>            |



## <a name="see-also"></a><span data-ttu-id="08a72-161">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="08a72-161">See also</span></span>

<dl> <dt>

[<span data-ttu-id="08a72-162">**Инкапсулировать**</span><span class="sxs-lookup"><span data-stu-id="08a72-162">**Encapsulate**</span></span>](iscardcmd-encapsulate.md)
</dt> <dt>

[<span data-ttu-id="08a72-163">**искардкмд**</span><span class="sxs-lookup"><span data-stu-id="08a72-163">**ISCardCmd**</span></span>](iscardcmd.md)
</dt> </dl>

 

 
