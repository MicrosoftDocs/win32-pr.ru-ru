---
description: Метод Реадбинари создает команду блока данных протокола приложения (КАТЕГОРИЯХ APDU), которая получает ответное сообщение, которое дает часть содержимого простейшего файла с прозрачным структурированием.
ms.assetid: 15394c21-1e07-4ea1-8f11-817e07b31f9b
title: 'Метод ISCardISO7816:: Реадбинари (Скардссп. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardISO7816.ReadBinary
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: a29093d8725a3390df9837f4e2f395cfcf2eef29
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103912464"
---
# <a name="iscardiso7816readbinary-method"></a><span data-ttu-id="1b6fb-103">Метод ISCardISO7816:: Реадбинари</span><span class="sxs-lookup"><span data-stu-id="1b6fb-103">ISCardISO7816::ReadBinary method</span></span>

<span data-ttu-id="1b6fb-104">\[Метод **реадбинари** доступен для использования в операционных системах, указанных в разделе требования.</span><span class="sxs-lookup"><span data-stu-id="1b6fb-104">\[The **ReadBinary** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="1b6fb-105">Он недоступен для использования в Windows Server 2003 с пакетом обновления 1 (SP1) и более поздней версии, Windows Vista, Windows Server 2008 и последующих версиях операционной системы.</span><span class="sxs-lookup"><span data-stu-id="1b6fb-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="1b6fb-106">[Модули смарт-карт](/previous-versions/windows/desktop/secsmart/smart-card-modules) предоставляют аналогичные функции.\]</span><span class="sxs-lookup"><span data-stu-id="1b6fb-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="1b6fb-107">Метод **реадбинари** создает команду [*блока данных протокола приложения*](../secgloss/a-gly.md) (категориях APDU), которая получает ответное сообщение, которое дает часть содержимого простейшего файла с прозрачным структурированием.</span><span class="sxs-lookup"><span data-stu-id="1b6fb-107">The **ReadBinary** method constructs an [*application protocol data unit*](../secgloss/a-gly.md) (APDU) command that acquires a response message that gives that part of the contents of a transparent-structured elementary file.</span></span>

## <a name="syntax"></a><span data-ttu-id="1b6fb-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="1b6fb-108">Syntax</span></span>


```C++
HRESULT ReadBinary(
  [in]      BYTE       byP1,
  [in]      BYTE       byP2,
  [in]      LONG       lBytesToRead,
  [in, out] LPSCARDCMD *ppCmd
);
```



## <a name="parameters"></a><span data-ttu-id="1b6fb-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="1b6fb-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1b6fb-110">*byP1* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="1b6fb-110">*byP1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1b6fb-111">Поле P1-P2 смещается на первый байт, который считывается с начала файла.</span><span class="sxs-lookup"><span data-stu-id="1b6fb-111">The P1-P2 field, offset to the first byte to be read from the beginning of the file.</span></span> <span data-ttu-id="1b6fb-112">Если B8 = 1 в P1, то значения B7 и B6 для P1 задаются равными нулю (РФУ биты), B5 – B1 of P1 — короткий идентификатор EF, а P2 — смещение первого байта, которое считывается в единицах данных с начала файла.</span><span class="sxs-lookup"><span data-stu-id="1b6fb-112">If b8=1 in P1, then b7 and b6 of P1 are set to zero (RFU bits), b5 to b1 of P1 are a short EF identifier and P2 is the offset of the first byte to be read in data units from the beginning of the file.</span></span> <span data-ttu-id="1b6fb-113">Если B8 = 0 в P1, то P1 \| \| P2 является смещением первого байта, который считывается в единицах данных с начала файла.</span><span class="sxs-lookup"><span data-stu-id="1b6fb-113">If b8=0 in P1, then P1\|\|P2 is the offset of the first byte to be read in data units from the beginning of the file.</span></span>

</dd> <dt>

<span data-ttu-id="1b6fb-114">*byP2* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="1b6fb-114">*byP2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1b6fb-115">Поле P1-P2 смещается на первый байт, который считывается с начала файла.</span><span class="sxs-lookup"><span data-stu-id="1b6fb-115">The P1-P2 field, offset to the first byte to be read from the beginning of the file.</span></span> <span data-ttu-id="1b6fb-116">Если B8 = 1 в P1, то значения B7 и B6 для P1 задаются равными нулю (РФУ биты), B5 – B1 of P1 — короткий идентификатор EF, а P2 — смещение первого байта, которое считывается в единицах данных с начала файла.</span><span class="sxs-lookup"><span data-stu-id="1b6fb-116">If b8=1 in P1, then b7 and b6 of P1 are set to zero (RFU bits), b5 to b1 of P1 are a short EF identifier and P2 is the offset of the first byte to be read in data units from the beginning of the file.</span></span> <span data-ttu-id="1b6fb-117">Если B8 = 0 в P1, то P1 \| \| P2 является смещением первого байта, который считывается в единицах данных с начала файла.</span><span class="sxs-lookup"><span data-stu-id="1b6fb-117">If b8=0 in P1, then P1\|\|P2 is the offset of the first byte to be read in data units from the beginning of the file.</span></span>

</dd> <dt>

<span data-ttu-id="1b6fb-118">*лбитестореад* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="1b6fb-118">*lBytesToRead* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1b6fb-119">Число байтов для чтения из прозрачной EF.</span><span class="sxs-lookup"><span data-stu-id="1b6fb-119">Number of bytes to read from the transparent EF.</span></span>

<span data-ttu-id="1b6fb-120">Если поле Le содержит только нули, то в пределах ограничения 256 для короткой длины или 65536 для расширенной длины все байты до конца файла должны быть считаны.</span><span class="sxs-lookup"><span data-stu-id="1b6fb-120">If the Le field contains only zeros, then within the limit of 256 for short length or 65536 for extended length, all the bytes until the end of the file should be read.</span></span>

</dd> <dt>

<span data-ttu-id="1b6fb-121">*ппкмд* \[ в, out\]</span><span class="sxs-lookup"><span data-stu-id="1b6fb-121">*ppCmd* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="1b6fb-122">На входе — указатель на объект интерфейса [**искардкмд**](iscardcmd.md) или **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="1b6fb-122">On input, a pointer to an [**ISCardCmd**](iscardcmd.md) interface object or **NULL**.</span></span>

<span data-ttu-id="1b6fb-123">При возвращении он заполняется командой КАТЕГОРИЯХ APDU, созданной этой операцией.</span><span class="sxs-lookup"><span data-stu-id="1b6fb-123">On return, it is filled with the APDU command constructed by this operation.</span></span> <span data-ttu-id="1b6fb-124">Если для *ппкмд* было задано **значение NULL**, то объект [*смарт-карты*](../secgloss/s-gly.md) [**искардкмд**](iscardcmd.md) создается внутренним образом и возвращается с помощью указателя *ппкмд* .</span><span class="sxs-lookup"><span data-stu-id="1b6fb-124">If *ppCmd* was set to **NULL**, a [*smart card*](../secgloss/s-gly.md) [**ISCardCmd**](iscardcmd.md) object is internally created and returned using the *ppCmd* pointer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1b6fb-125">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="1b6fb-125">Return value</span></span>

<span data-ttu-id="1b6fb-126">Метод возвращает одно из следующих возможных значений.</span><span class="sxs-lookup"><span data-stu-id="1b6fb-126">The method returns one of the following possible values.</span></span>



| <span data-ttu-id="1b6fb-127">Код возврата</span><span class="sxs-lookup"><span data-stu-id="1b6fb-127">Return code</span></span>                                                                                   | <span data-ttu-id="1b6fb-128">Описание</span><span class="sxs-lookup"><span data-stu-id="1b6fb-128">Description</span></span>                                  |
|-----------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="1b6fb-129"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="1b6fb-129"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="1b6fb-130">Operation completed successfully (Операция выполнена успешно).</span><span class="sxs-lookup"><span data-stu-id="1b6fb-130">Operation completed successfully.</span></span><br/> |
| <dl> <span data-ttu-id="1b6fb-131"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="1b6fb-131"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="1b6fb-132">Недопустимый параметр.</span><span class="sxs-lookup"><span data-stu-id="1b6fb-132">Invalid parameter.</span></span><br/>                |
| <dl> <span data-ttu-id="1b6fb-133"><dt>**\_указатель E**</dt></span><span class="sxs-lookup"><span data-stu-id="1b6fb-133"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="1b6fb-134">Передан неверный указатель.</span><span class="sxs-lookup"><span data-stu-id="1b6fb-134">A bad pointer was passed in.</span></span><br/>      |
| <dl> <span data-ttu-id="1b6fb-135"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="1b6fb-135"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="1b6fb-136">Недостаточно памяти.</span><span class="sxs-lookup"><span data-stu-id="1b6fb-136">Out of memory.</span></span><br/>                    |



 

## <a name="remarks"></a><span data-ttu-id="1b6fb-137">Комментарии</span><span class="sxs-lookup"><span data-stu-id="1b6fb-137">Remarks</span></span>

<span data-ttu-id="1b6fb-138">Инкапсулированная команда может быть выполнена только в том случае, если состояние безопасности [*смарт-карты*](../secgloss/s-gly.md) соответствует атрибутам безопасности для обрабатываемого простейшего файла.</span><span class="sxs-lookup"><span data-stu-id="1b6fb-138">The encapsulated command can only be performed if the security status of the [*smart card*](../secgloss/s-gly.md) satisfies the security attributes of the elementary file being processed.</span></span>

<span data-ttu-id="1b6fb-139">Если команда содержит допустимый краткий простой идентификатор, она устанавливает файл в качестве текущего простейшего файла.</span><span class="sxs-lookup"><span data-stu-id="1b6fb-139">When the command contains a valid short elementary identifier, it sets the file as current elementary file.</span></span>

<span data-ttu-id="1b6fb-140">Простые файлы без прозрачной структуры не могут быть удалены.</span><span class="sxs-lookup"><span data-stu-id="1b6fb-140">Elementary files without a transparent structure cannot be erased.</span></span> <span data-ttu-id="1b6fb-141">Инкапсулированная команда прерывается, если применяется к простейшему файлу без прозрачной структуры.</span><span class="sxs-lookup"><span data-stu-id="1b6fb-141">The encapsulated command aborts if applied to an elementary file without a transparent structure.</span></span>

<span data-ttu-id="1b6fb-142">Список всех методов, предоставляемых этим интерфейсом, см. в разделе [**ISCardISO7816**](iscardiso7816.md).</span><span class="sxs-lookup"><span data-stu-id="1b6fb-142">For a list of all the methods provided by this interface, see [**ISCardISO7816**](iscardiso7816.md).</span></span>

<span data-ttu-id="1b6fb-143">Кроме приведенных выше кодов ошибок COM, этот интерфейс может возвращать код ошибки смарт-карты, если для завершения запроса была вызвана функция смарт-карты.</span><span class="sxs-lookup"><span data-stu-id="1b6fb-143">In addition to the COM error codes listed above, this interface may return a smart card error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="1b6fb-144">Дополнительные сведения см. в статье [возвращаемые значения смарт-карты](authentication-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="1b6fb-144">For more information, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="1b6fb-145">Требования</span><span class="sxs-lookup"><span data-stu-id="1b6fb-145">Requirements</span></span>



| <span data-ttu-id="1b6fb-146">Требование</span><span class="sxs-lookup"><span data-stu-id="1b6fb-146">Requirement</span></span> | <span data-ttu-id="1b6fb-147">Значение</span><span class="sxs-lookup"><span data-stu-id="1b6fb-147">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="1b6fb-148">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="1b6fb-148">Minimum supported client</span></span><br/> | <span data-ttu-id="1b6fb-149">Только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="1b6fb-149">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="1b6fb-150">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="1b6fb-150">Minimum supported server</span></span><br/> | <span data-ttu-id="1b6fb-151">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="1b6fb-151">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="1b6fb-152">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="1b6fb-152">End of client support</span></span><br/>    | <span data-ttu-id="1b6fb-153">Windows XP</span><span class="sxs-lookup"><span data-stu-id="1b6fb-153">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="1b6fb-154">Поддержка конца сервера</span><span class="sxs-lookup"><span data-stu-id="1b6fb-154">End of server support</span></span><br/>    | <span data-ttu-id="1b6fb-155">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="1b6fb-155">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="1b6fb-156">Header</span><span class="sxs-lookup"><span data-stu-id="1b6fb-156">Header</span></span><br/>                   | <dl> <span data-ttu-id="1b6fb-157"><dt>Скардссп. h</dt></span><span class="sxs-lookup"><span data-stu-id="1b6fb-157"><dt>Scardssp.h</dt></span></span> </dl>   |
| <span data-ttu-id="1b6fb-158">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="1b6fb-158">Type library</span></span><br/>             | <dl> <span data-ttu-id="1b6fb-159"><dt>Скардсрв. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="1b6fb-159"><dt>Scardsrv.tlb</dt></span></span> </dl> |
| <span data-ttu-id="1b6fb-160">DLL</span><span class="sxs-lookup"><span data-stu-id="1b6fb-160">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1b6fb-161"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1b6fb-161"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="1b6fb-162">IID</span><span class="sxs-lookup"><span data-stu-id="1b6fb-162">IID</span></span><br/>                      | <span data-ttu-id="1b6fb-163">IID \_ ISCardISO7816 определен как 53B6AA68-3F56-11D0-916B-00AA00C18068</span><span class="sxs-lookup"><span data-stu-id="1b6fb-163">IID\_ISCardISO7816 is defined as 53B6AA68-3F56-11D0-916B-00AA00C18068</span></span><br/>        |



## <a name="see-also"></a><span data-ttu-id="1b6fb-164">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="1b6fb-164">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1b6fb-165">**ерасебинари**</span><span class="sxs-lookup"><span data-stu-id="1b6fb-165">**EraseBinary**</span></span>](iscardiso7816-erasebinary.md)
</dt> <dt>

[<span data-ttu-id="1b6fb-166">**ISCardISO7816**</span><span class="sxs-lookup"><span data-stu-id="1b6fb-166">**ISCardISO7816**</span></span>](iscardiso7816.md)
</dt> <dt>

[<span data-ttu-id="1b6fb-167">**упдатебинари**</span><span class="sxs-lookup"><span data-stu-id="1b6fb-167">**UpdateBinary**</span></span>](iscardiso7816-updatebinary.md)
</dt> <dt>

[<span data-ttu-id="1b6fb-168">**вритебинари**</span><span class="sxs-lookup"><span data-stu-id="1b6fb-168">**WriteBinary**</span></span>](iscardiso7816-writebinary.md)
</dt> </dl>

 

 
