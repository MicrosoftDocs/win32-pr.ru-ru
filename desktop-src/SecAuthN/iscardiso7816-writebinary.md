---
description: Метод Вритебинари создает команду блока данных протокола приложения (КАТЕГОРИЯХ APDU), которая записывает двоичные значения в простейший файл.
ms.assetid: e38273d5-4eb0-4c0b-829a-c78e511a38bc
title: 'Метод ISCardISO7816:: Вритебинари (Скардссп. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardISO7816.WriteBinary
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 330e817bc501c451026589087991fb43c0b5ac57
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103990888"
---
# <a name="iscardiso7816writebinary-method"></a><span data-ttu-id="7cee5-103">Метод ISCardISO7816:: Вритебинари</span><span class="sxs-lookup"><span data-stu-id="7cee5-103">ISCardISO7816::WriteBinary method</span></span>

<span data-ttu-id="7cee5-104">\[Метод **вритебинари** доступен для использования в операционных системах, указанных в разделе требования.</span><span class="sxs-lookup"><span data-stu-id="7cee5-104">\[The **WriteBinary** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="7cee5-105">Он недоступен для использования в Windows Server 2003 с пакетом обновления 1 (SP1) и более поздней версии, Windows Vista, Windows Server 2008 и последующих версиях операционной системы.</span><span class="sxs-lookup"><span data-stu-id="7cee5-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="7cee5-106">[Модули смарт-карт](/previous-versions/windows/desktop/secsmart/smart-card-modules) предоставляют аналогичные функции.\]</span><span class="sxs-lookup"><span data-stu-id="7cee5-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="7cee5-107">Метод **вритебинари** создает команду [*блока данных протокола приложения*](../secgloss/a-gly.md) (категориях APDU), которая записывает двоичные значения в простейший файл.</span><span class="sxs-lookup"><span data-stu-id="7cee5-107">The **WriteBinary** method constructs an [*application protocol data unit*](../secgloss/a-gly.md) (APDU) command that writes binary values into an elementary file.</span></span>

<span data-ttu-id="7cee5-108">В зависимости от атрибутов файла команда выполняет одну из следующих операций:</span><span class="sxs-lookup"><span data-stu-id="7cee5-108">Depending upon the file attributes, the command performs one of the following operations:</span></span>

-   <span data-ttu-id="7cee5-109">Логическое значение или для битов, уже имеющихся в карточке с битами, заданными в команде КАТЕГОРИЯХ APDU (логическое стирание состояния битов файла — 0).</span><span class="sxs-lookup"><span data-stu-id="7cee5-109">The logical OR of the bits already present in the card with the bits given in the command APDU (logical erased state of the bits of the file is 0).</span></span>
-   <span data-ttu-id="7cee5-110">Логическое и для битов, уже имеющихся в карточке с битами, заданными в команде КАТЕГОРИЯХ APDU (логическое стирание состояния битов файла — 1).</span><span class="sxs-lookup"><span data-stu-id="7cee5-110">The logical AND of the bits already present in the card with the bits given in the command APDU (logical erased state of the bits of the file is 1).</span></span>
-   <span data-ttu-id="7cee5-111">Однократная запись в карточку битов, заданная в команде КАТЕГОРИЯХ APDU.</span><span class="sxs-lookup"><span data-stu-id="7cee5-111">The one-time write in the card of the bits given in the command APDU.</span></span>

<span data-ttu-id="7cee5-112">Если в байте кода данных не указаны никакие указания, применяется логическое поведение или.</span><span class="sxs-lookup"><span data-stu-id="7cee5-112">When no indication is given in the data coding byte, the logical OR behavior applies.</span></span>

## <a name="syntax"></a><span data-ttu-id="7cee5-113">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="7cee5-113">Syntax</span></span>


```C++
HRESULT WriteBinary(
  [in]      BYTE         byP1,
  [in]      BYTE         byP2,
  [in]      LPBYTEBUFFER pData,
  [in, out] LPSCARDCMD   *ppCmd
);
```



## <a name="parameters"></a><span data-ttu-id="7cee5-114">Параметры</span><span class="sxs-lookup"><span data-stu-id="7cee5-114">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7cee5-115">*byP1* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="7cee5-115">*byP1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7cee5-116">Смещение в расположении записи от начала двоичного файла (EF).</span><span class="sxs-lookup"><span data-stu-id="7cee5-116">Offset to the write location from the beginning of the binary file (EF).</span></span> <span data-ttu-id="7cee5-117">Если B8 = 1 в P1, то значения B7 и B6 для P1 задаются равными нулю (РФУ биты), B5 – B1 of P1 — короткий идентификатор EF, а P2 — смещение первого байта, записываемого в единицы данных с начала файла.</span><span class="sxs-lookup"><span data-stu-id="7cee5-117">If b8=1 in P1, then b7 and b6 of P1 are set to zero (RFU bits), b5 to b1 of P1 are a short EF identifier and P2 is the offset of the first byte to be written in data units from the beginning of the file.</span></span> <span data-ttu-id="7cee5-118">Если B8 = 0 в P1, то P1 \| \| P2 — это смещение первого байта, записываемого в единицы данных с начала файла.</span><span class="sxs-lookup"><span data-stu-id="7cee5-118">If b8=0 in P1, then P1\|\|P2 is the offset of the first byte to be written in data units from the beginning of the file.</span></span>

</dd> <dt>

<span data-ttu-id="7cee5-119">*byP2* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="7cee5-119">*byP2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7cee5-120">Смещение в расположении записи от начала двоичного файла (EF).</span><span class="sxs-lookup"><span data-stu-id="7cee5-120">Offset to the write location from the beginning of the binary file (EF).</span></span> <span data-ttu-id="7cee5-121">Если B8 = 1 в P1, то значения B7 и B6 для P1 задаются равными нулю (РФУ биты), B5 – B1 of P1 — короткий идентификатор EF, а P2 — смещение первого байта, записываемого в единицы данных с начала файла.</span><span class="sxs-lookup"><span data-stu-id="7cee5-121">If b8=1 in P1, then b7 and b6 of P1 are set to zero (RFU bits), b5 to b1 of P1 are a short EF identifier and P2 is the offset of the first byte to be written in data units from the beginning of the file.</span></span> <span data-ttu-id="7cee5-122">Если B8 = 0 в P1, то P1 \| \| P2 — это смещение первого байта, записываемого в единицы данных с начала файла.</span><span class="sxs-lookup"><span data-stu-id="7cee5-122">If b8=0 in P1, then P1\|\|P2 is the offset of the first byte to be written in data units from the beginning of the file.</span></span>

</dd> <dt>

<span data-ttu-id="7cee5-123">*pData* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="7cee5-123">*pData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7cee5-124">Указатель на строку записываемых единиц данных.</span><span class="sxs-lookup"><span data-stu-id="7cee5-124">Pointer to the string of data units to be written.</span></span>

</dd> <dt>

<span data-ttu-id="7cee5-125">*ппкмд* \[ в, out\]</span><span class="sxs-lookup"><span data-stu-id="7cee5-125">*ppCmd* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="7cee5-126">На входе — указатель на объект интерфейса [**искардкмд**](iscardcmd.md) или **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="7cee5-126">On input, a pointer to an [**ISCardCmd**](iscardcmd.md) interface object or **NULL**.</span></span>

<span data-ttu-id="7cee5-127">При возвращении он заполняется командой КАТЕГОРИЯХ APDU, созданной этой операцией.</span><span class="sxs-lookup"><span data-stu-id="7cee5-127">On return, it is filled with the APDU command constructed by this operation.</span></span> <span data-ttu-id="7cee5-128">Если для *ппкмд* было задано **значение NULL**, то объект [*смарт-карты*](../secgloss/s-gly.md) [**искардкмд**](iscardcmd.md) создается внутренним образом и возвращается через указатель *ппкмд* .</span><span class="sxs-lookup"><span data-stu-id="7cee5-128">If *ppCmd* was set to **NULL**, a [*smart card*](../secgloss/s-gly.md) [**ISCardCmd**](iscardcmd.md) object is internally created and returned via the *ppCmd* pointer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7cee5-129">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="7cee5-129">Return value</span></span>

<span data-ttu-id="7cee5-130">Метод возвращает одно из следующих возможных значений.</span><span class="sxs-lookup"><span data-stu-id="7cee5-130">The method returns one of the following possible values.</span></span>



| <span data-ttu-id="7cee5-131">Код возврата</span><span class="sxs-lookup"><span data-stu-id="7cee5-131">Return code</span></span>                                                                                   | <span data-ttu-id="7cee5-132">Описание</span><span class="sxs-lookup"><span data-stu-id="7cee5-132">Description</span></span>                                  |
|-----------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="7cee5-133"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="7cee5-133"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="7cee5-134">Operation completed successfully (Операция выполнена успешно).</span><span class="sxs-lookup"><span data-stu-id="7cee5-134">Operation completed successfully.</span></span><br/> |
| <dl> <span data-ttu-id="7cee5-135"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="7cee5-135"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="7cee5-136">Недопустимый параметр.</span><span class="sxs-lookup"><span data-stu-id="7cee5-136">Invalid parameter.</span></span><br/>                |
| <dl> <span data-ttu-id="7cee5-137"><dt>**\_указатель E**</dt></span><span class="sxs-lookup"><span data-stu-id="7cee5-137"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="7cee5-138">Передан неверный указатель.</span><span class="sxs-lookup"><span data-stu-id="7cee5-138">A bad pointer was passed in.</span></span><br/>      |
| <dl> <span data-ttu-id="7cee5-139"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="7cee5-139"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="7cee5-140">Недостаточно памяти.</span><span class="sxs-lookup"><span data-stu-id="7cee5-140">Out of memory.</span></span><br/>                    |



 

## <a name="remarks"></a><span data-ttu-id="7cee5-141">Комментарии</span><span class="sxs-lookup"><span data-stu-id="7cee5-141">Remarks</span></span>

<span data-ttu-id="7cee5-142">Инкапсулированная команда может быть выполнена только в том случае, если состояние безопасности [*смарт-карты*](../secgloss/s-gly.md) соответствует атрибутам безопасности для обрабатываемого простейшего файла.</span><span class="sxs-lookup"><span data-stu-id="7cee5-142">The encapsulated command can only be performed if the security status of the [*smart card*](../secgloss/s-gly.md) satisfies the security attributes of the elementary file being processed.</span></span>

<span data-ttu-id="7cee5-143">Если команда содержит допустимый краткий простой идентификатор, она устанавливает файл в качестве текущего простейшего файла.</span><span class="sxs-lookup"><span data-stu-id="7cee5-143">When the command contains a valid short elementary identifier, it sets the file as current elementary file.</span></span>

<span data-ttu-id="7cee5-144">Если операция записи в двоичный файл была применена к блоку данных одновременной записи EF, дальнейшая операция записи, ссылающаяся на эту единицу данных, будет прервана, если содержимое единицы данных или индикатор логического стирания состояния (если таковое имеется), прикрепленный к этой единице данных, отличается от логического состояния.</span><span class="sxs-lookup"><span data-stu-id="7cee5-144">When a write binary operation has been applied to a data unit of a one-time write EF, any further write operation referring to this data unit will be aborted if the content of the data unit or the logical erased state indicator (if any) attached to this data unit is different from the logical erased state.</span></span>

<span data-ttu-id="7cee5-145">Невозможно записать простые файлы без прозрачной структуры.</span><span class="sxs-lookup"><span data-stu-id="7cee5-145">Elementary files without a transparent structure cannot be written to.</span></span> <span data-ttu-id="7cee5-146">Инкапсулированная команда прерывается, если применяется к простейшему файлу без прозрачной структуры.</span><span class="sxs-lookup"><span data-stu-id="7cee5-146">The encapsulated command aborts if applied to an elementary file without a transparent structure.</span></span>

<span data-ttu-id="7cee5-147">Список всех методов, предоставляемых этим интерфейсом, см. в разделе [**ISCardISO7816**](iscardiso7816.md).</span><span class="sxs-lookup"><span data-stu-id="7cee5-147">For a list of all the methods provided by this interface, see [**ISCardISO7816**](iscardiso7816.md).</span></span>

<span data-ttu-id="7cee5-148">Кроме приведенных выше кодов ошибок COM, этот интерфейс может возвращать код ошибки смарт-карты, если для завершения запроса была вызвана функция смарт-карты.</span><span class="sxs-lookup"><span data-stu-id="7cee5-148">In addition to the COM error codes listed above, this interface may return a smart card error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="7cee5-149">Дополнительные сведения см. в статье [возвращаемые значения смарт-карты](authentication-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="7cee5-149">For more information, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="7cee5-150">Требования</span><span class="sxs-lookup"><span data-stu-id="7cee5-150">Requirements</span></span>



| <span data-ttu-id="7cee5-151">Требование</span><span class="sxs-lookup"><span data-stu-id="7cee5-151">Requirement</span></span> | <span data-ttu-id="7cee5-152">Значение</span><span class="sxs-lookup"><span data-stu-id="7cee5-152">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="7cee5-153">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="7cee5-153">Minimum supported client</span></span><br/> | <span data-ttu-id="7cee5-154">Только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="7cee5-154">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="7cee5-155">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="7cee5-155">Minimum supported server</span></span><br/> | <span data-ttu-id="7cee5-156">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="7cee5-156">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="7cee5-157">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="7cee5-157">End of client support</span></span><br/>    | <span data-ttu-id="7cee5-158">Windows XP</span><span class="sxs-lookup"><span data-stu-id="7cee5-158">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="7cee5-159">Поддержка конца сервера</span><span class="sxs-lookup"><span data-stu-id="7cee5-159">End of server support</span></span><br/>    | <span data-ttu-id="7cee5-160">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="7cee5-160">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="7cee5-161">Header</span><span class="sxs-lookup"><span data-stu-id="7cee5-161">Header</span></span><br/>                   | <dl> <span data-ttu-id="7cee5-162"><dt>Скардссп. h</dt></span><span class="sxs-lookup"><span data-stu-id="7cee5-162"><dt>Scardssp.h</dt></span></span> </dl>   |
| <span data-ttu-id="7cee5-163">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="7cee5-163">Type library</span></span><br/>             | <dl> <span data-ttu-id="7cee5-164"><dt>Скардсрв. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="7cee5-164"><dt>Scardsrv.tlb</dt></span></span> </dl> |
| <span data-ttu-id="7cee5-165">DLL</span><span class="sxs-lookup"><span data-stu-id="7cee5-165">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7cee5-166"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7cee5-166"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="7cee5-167">IID</span><span class="sxs-lookup"><span data-stu-id="7cee5-167">IID</span></span><br/>                      | <span data-ttu-id="7cee5-168">IID \_ ISCardISO7816 определен как 53B6AA68-3F56-11D0-916B-00AA00C18068</span><span class="sxs-lookup"><span data-stu-id="7cee5-168">IID\_ISCardISO7816 is defined as 53B6AA68-3F56-11D0-916B-00AA00C18068</span></span><br/>        |



## <a name="see-also"></a><span data-ttu-id="7cee5-169">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="7cee5-169">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7cee5-170">**ерасебинари**</span><span class="sxs-lookup"><span data-stu-id="7cee5-170">**EraseBinary**</span></span>](iscardiso7816-erasebinary.md)
</dt> <dt>

[<span data-ttu-id="7cee5-171">**ISCardISO7816**</span><span class="sxs-lookup"><span data-stu-id="7cee5-171">**ISCardISO7816**</span></span>](iscardiso7816.md)
</dt> <dt>

[<span data-ttu-id="7cee5-172">**реадбинари**</span><span class="sxs-lookup"><span data-stu-id="7cee5-172">**ReadBinary**</span></span>](iscardiso7816-readbinary.md)
</dt> <dt>

[<span data-ttu-id="7cee5-173">**упдатебинари**</span><span class="sxs-lookup"><span data-stu-id="7cee5-173">**UpdateBinary**</span></span>](iscardiso7816-updatebinary.md)
</dt> </dl>

 

 
