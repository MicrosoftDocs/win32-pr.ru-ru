---
description: Метод Упдатебинари конструирует команду блока данных протокола приложения (КАТЕГОРИЯХ APDU), которая обновляет биты в простейшем файле с битами, заданными в команде КАТЕГОРИЯХ APDU.
ms.assetid: 14ac6ad9-efcf-48ea-8712-19caeee47521
title: 'Метод ISCardISO7816:: Упдатебинари (Скардссп. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardISO7816.UpdateBinary
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: d9651189cab228eaa5dacc9c2f5963201bbc65c8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105650879"
---
# <a name="iscardiso7816updatebinary-method"></a><span data-ttu-id="ddcba-103">Метод ISCardISO7816:: Упдатебинари</span><span class="sxs-lookup"><span data-stu-id="ddcba-103">ISCardISO7816::UpdateBinary method</span></span>

<span data-ttu-id="ddcba-104">\[Метод **упдатебинари** доступен для использования в операционных системах, указанных в разделе требования.</span><span class="sxs-lookup"><span data-stu-id="ddcba-104">\[The **UpdateBinary** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="ddcba-105">Он недоступен для использования в Windows Server 2003 с пакетом обновления 1 (SP1) и более поздней версии, Windows Vista, Windows Server 2008 и последующих версиях операционной системы.</span><span class="sxs-lookup"><span data-stu-id="ddcba-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="ddcba-106">[Модули смарт-карт](/previous-versions/windows/desktop/secsmart/smart-card-modules) предоставляют аналогичные функции.\]</span><span class="sxs-lookup"><span data-stu-id="ddcba-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="ddcba-107">Метод **упдатебинари** конструирует команду [*блока данных протокола приложения*](../secgloss/a-gly.md) (категориях APDU), которая обновляет биты в простейшем файле с битами, заданными в команде категориях APDU.</span><span class="sxs-lookup"><span data-stu-id="ddcba-107">The **UpdateBinary** method constructs an [*application protocol data unit*](../secgloss/a-gly.md) (APDU) command that updates the bits present in an elementary file with the bits given in the APDU command.</span></span>

## <a name="syntax"></a><span data-ttu-id="ddcba-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="ddcba-108">Syntax</span></span>


```C++
HRESULT UpdateBinary(
  [in]      BYTE         byP1,
  [in]      BYTE         byP2,
  [in]      LPBYTEBUFFER pData,
  [in, out] LPSCARDCMD   *ppCmd
);
```



## <a name="parameters"></a><span data-ttu-id="ddcba-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="ddcba-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ddcba-110">*byP1* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="ddcba-110">*byP1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ddcba-111">Смещение к расположению записи (обновление) в двоичный файл с начала двоичного файла.</span><span class="sxs-lookup"><span data-stu-id="ddcba-111">Offset to the write (update) location into the binary from the start of the binary.</span></span> <span data-ttu-id="ddcba-112">Если B8 = 1 в P1, то значения B7 и B6 для P1 задаются равными нулю (РФУ биты), B5 – B1 of P1 — короткий идентификатор EF, а P2 — смещение первого байта, которое должно быть Обновлено в единицах данных с начала файла.</span><span class="sxs-lookup"><span data-stu-id="ddcba-112">If b8=1 in P1, then b7 and b6 of P1 are set to zero (RFU bits), b5 to b1 of P1 are a short EF identifier and P2 is the offset of the first byte to be updated in data units from the beginning of the file.</span></span> <span data-ttu-id="ddcba-113">Если B8 = 0 в P1, то P1 \| \| P2 — это смещение первого байта, обновляемого в единицах данных, с начала файла.</span><span class="sxs-lookup"><span data-stu-id="ddcba-113">If b8=0 in P1, then P1 \|\| P2 is the offset of the first byte to be updated in data units from the beginning of the file.</span></span>

</dd> <dt>

<span data-ttu-id="ddcba-114">*byP2* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="ddcba-114">*byP2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ddcba-115">Смещение к расположению записи (обновление) в двоичный файл с начала двоичного файла.</span><span class="sxs-lookup"><span data-stu-id="ddcba-115">Offset to the write (update) location into the binary from the start of the binary.</span></span> <span data-ttu-id="ddcba-116">Если B8 = 1 в P1, то значения B7 и B6 для P1 задаются равными нулю (РФУ биты), B5 – B1 of P1 — короткий идентификатор EF, а P2 — смещение первого байта, которое должно быть Обновлено в единицах данных с начала файла.</span><span class="sxs-lookup"><span data-stu-id="ddcba-116">If b8=1 in P1, then b7 and b6 of P1 are set to zero (RFU bits), b5 to b1 of P1 are a short EF identifier and P2 is the offset of the first byte to be updated in data units from the beginning of the file.</span></span> <span data-ttu-id="ddcba-117">Если B8 = 0 в P1, то P1 \| \| P2 — это смещение первого байта, обновляемого в единицах данных, с начала файла.</span><span class="sxs-lookup"><span data-stu-id="ddcba-117">If b8=0 in P1, then P1 \|\| P2 is the offset of the first byte to be updated in data units from the beginning of the file.</span></span>

</dd> <dt>

<span data-ttu-id="ddcba-118">*pData* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="ddcba-118">*pData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ddcba-119">Указатель на строку обновляемых единиц данных.</span><span class="sxs-lookup"><span data-stu-id="ddcba-119">Pointer to the string of data units to be updated.</span></span>

</dd> <dt>

<span data-ttu-id="ddcba-120">*ппкмд* \[ в, out\]</span><span class="sxs-lookup"><span data-stu-id="ddcba-120">*ppCmd* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="ddcba-121">На входе — указатель на объект интерфейса [**искардкмд**](iscardcmd.md) или **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="ddcba-121">On input, a pointer to an [**ISCardCmd**](iscardcmd.md) interface object or **NULL**.</span></span>

<span data-ttu-id="ddcba-122">При возвращении он заполняется командой КАТЕГОРИЯХ APDU, созданной этой операцией.</span><span class="sxs-lookup"><span data-stu-id="ddcba-122">On return, it is filled with the APDU command constructed by this operation.</span></span> <span data-ttu-id="ddcba-123">Если для *ппкмд* было задано **значение NULL**, то объект [*смарт-карты*](../secgloss/s-gly.md) [**искардкмд**](iscardcmd.md) создается внутренним образом и возвращается с помощью указателя *ппкмд* .</span><span class="sxs-lookup"><span data-stu-id="ddcba-123">If *ppCmd* was set to **NULL**, a [*smart card*](../secgloss/s-gly.md) [**ISCardCmd**](iscardcmd.md) object is internally created and returned using the *ppCmd* pointer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ddcba-124">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="ddcba-124">Return value</span></span>

<span data-ttu-id="ddcba-125">Метод возвращает одно из следующих возможных значений.</span><span class="sxs-lookup"><span data-stu-id="ddcba-125">The method returns one of the following possible values.</span></span>



| <span data-ttu-id="ddcba-126">Код возврата</span><span class="sxs-lookup"><span data-stu-id="ddcba-126">Return code</span></span>                                                                                   | <span data-ttu-id="ddcba-127">Описание</span><span class="sxs-lookup"><span data-stu-id="ddcba-127">Description</span></span>                                  |
|-----------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="ddcba-128"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="ddcba-128"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="ddcba-129">Operation completed successfully (Операция выполнена успешно).</span><span class="sxs-lookup"><span data-stu-id="ddcba-129">Operation completed successfully.</span></span><br/> |
| <dl> <span data-ttu-id="ddcba-130"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="ddcba-130"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="ddcba-131">Недопустимый параметр.</span><span class="sxs-lookup"><span data-stu-id="ddcba-131">Invalid parameter.</span></span><br/>                |
| <dl> <span data-ttu-id="ddcba-132"><dt>**\_указатель E**</dt></span><span class="sxs-lookup"><span data-stu-id="ddcba-132"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="ddcba-133">Передан неверный указатель.</span><span class="sxs-lookup"><span data-stu-id="ddcba-133">A bad pointer was passed in.</span></span><br/>      |
| <dl> <span data-ttu-id="ddcba-134"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="ddcba-134"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="ddcba-135">Недостаточно памяти.</span><span class="sxs-lookup"><span data-stu-id="ddcba-135">Out of memory.</span></span><br/>                    |



 

## <a name="remarks"></a><span data-ttu-id="ddcba-136">Комментарии</span><span class="sxs-lookup"><span data-stu-id="ddcba-136">Remarks</span></span>

<span data-ttu-id="ddcba-137">Инкапсулированная команда может быть выполнена только в том случае, если состояние безопасности смарт-карты соответствует атрибутам безопасности для обрабатываемого простейшего файла.</span><span class="sxs-lookup"><span data-stu-id="ddcba-137">The encapsulated command can only be performed if the security status of the smart card satisfies the security attributes of the elementary file being processed.</span></span>

<span data-ttu-id="ddcba-138">Если команда содержит допустимый краткий простой идентификатор, она устанавливает файл в качестве текущего простейшего файла.</span><span class="sxs-lookup"><span data-stu-id="ddcba-138">When the command contains a valid short elementary identifier, it sets the file as current elementary file.</span></span>

<span data-ttu-id="ddcba-139">Простые файлы без прозрачной структуры не могут быть удалены.</span><span class="sxs-lookup"><span data-stu-id="ddcba-139">Elementary files without a transparent structure cannot be erased.</span></span> <span data-ttu-id="ddcba-140">Инкапсулированная команда прерывается, если применяется к простейшему файлу без прозрачной структуры.</span><span class="sxs-lookup"><span data-stu-id="ddcba-140">The encapsulated command aborts if applied to an elementary file without a transparent structure.</span></span>

<span data-ttu-id="ddcba-141">Список всех методов, предоставляемых этим интерфейсом, см. в разделе [**ISCardISO7816**](iscardiso7816.md).</span><span class="sxs-lookup"><span data-stu-id="ddcba-141">For a list of all the methods provided by this interface, see [**ISCardISO7816**](iscardiso7816.md).</span></span>

<span data-ttu-id="ddcba-142">Кроме приведенных выше кодов ошибок COM, этот интерфейс может возвращать код ошибки смарт-карты, если для завершения запроса была вызвана функция смарт-карты.</span><span class="sxs-lookup"><span data-stu-id="ddcba-142">In addition to the COM error codes listed above, this interface may return a smart card error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="ddcba-143">Дополнительные сведения см. в статье [возвращаемые значения смарт-карты](authentication-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="ddcba-143">For more information, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="ddcba-144">Требования</span><span class="sxs-lookup"><span data-stu-id="ddcba-144">Requirements</span></span>



| <span data-ttu-id="ddcba-145">Требование</span><span class="sxs-lookup"><span data-stu-id="ddcba-145">Requirement</span></span> | <span data-ttu-id="ddcba-146">Значение</span><span class="sxs-lookup"><span data-stu-id="ddcba-146">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="ddcba-147">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="ddcba-147">Minimum supported client</span></span><br/> | <span data-ttu-id="ddcba-148">Только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="ddcba-148">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="ddcba-149">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="ddcba-149">Minimum supported server</span></span><br/> | <span data-ttu-id="ddcba-150">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="ddcba-150">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="ddcba-151">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="ddcba-151">End of client support</span></span><br/>    | <span data-ttu-id="ddcba-152">Windows XP</span><span class="sxs-lookup"><span data-stu-id="ddcba-152">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="ddcba-153">Поддержка конца сервера</span><span class="sxs-lookup"><span data-stu-id="ddcba-153">End of server support</span></span><br/>    | <span data-ttu-id="ddcba-154">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="ddcba-154">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="ddcba-155">Header</span><span class="sxs-lookup"><span data-stu-id="ddcba-155">Header</span></span><br/>                   | <dl> <span data-ttu-id="ddcba-156"><dt>Скардссп. h</dt></span><span class="sxs-lookup"><span data-stu-id="ddcba-156"><dt>Scardssp.h</dt></span></span> </dl>   |
| <span data-ttu-id="ddcba-157">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="ddcba-157">Type library</span></span><br/>             | <dl> <span data-ttu-id="ddcba-158"><dt>Скардсрв. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="ddcba-158"><dt>Scardsrv.tlb</dt></span></span> </dl> |
| <span data-ttu-id="ddcba-159">DLL</span><span class="sxs-lookup"><span data-stu-id="ddcba-159">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ddcba-160"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ddcba-160"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="ddcba-161">IID</span><span class="sxs-lookup"><span data-stu-id="ddcba-161">IID</span></span><br/>                      | <span data-ttu-id="ddcba-162">IID \_ ISCardISO7816 определен как 53B6AA68-3F56-11D0-916B-00AA00C18068</span><span class="sxs-lookup"><span data-stu-id="ddcba-162">IID\_ISCardISO7816 is defined as 53B6AA68-3F56-11D0-916B-00AA00C18068</span></span><br/>        |



## <a name="see-also"></a><span data-ttu-id="ddcba-163">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="ddcba-163">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ddcba-164">**ерасебинари**</span><span class="sxs-lookup"><span data-stu-id="ddcba-164">**EraseBinary**</span></span>](iscardiso7816-erasebinary.md)
</dt> <dt>

[<span data-ttu-id="ddcba-165">**ISCardISO7816**</span><span class="sxs-lookup"><span data-stu-id="ddcba-165">**ISCardISO7816**</span></span>](iscardiso7816.md)
</dt> <dt>

[<span data-ttu-id="ddcba-166">**реадбинари**</span><span class="sxs-lookup"><span data-stu-id="ddcba-166">**ReadBinary**</span></span>](iscardiso7816-readbinary.md)
</dt> <dt>

[<span data-ttu-id="ddcba-167">**вритебинари**</span><span class="sxs-lookup"><span data-stu-id="ddcba-167">**WriteBinary**</span></span>](iscardiso7816-writebinary.md)
</dt> </dl>

 

 
