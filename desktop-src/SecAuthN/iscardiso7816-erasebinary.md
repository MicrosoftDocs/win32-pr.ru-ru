---
description: Конструирует команду блока данных протокола приложения (КАТЕГОРИЯХ APDU), которая последовательно устанавливает часть содержимого простейшего файла в логическое состояние стирания, начиная с заданного смещения.
ms.assetid: 89e2371e-e27d-475b-9427-bbf6d614c473
title: 'Метод ISCardISO7816:: Ерасебинари (Скардссп. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardISO7816.EraseBinary
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: a9bad21bbb35b7ac16209ac0075267ef7300fe21
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105651126"
---
# <a name="iscardiso7816erasebinary-method"></a><span data-ttu-id="ec873-103">Метод ISCardISO7816:: Ерасебинари</span><span class="sxs-lookup"><span data-stu-id="ec873-103">ISCardISO7816::EraseBinary method</span></span>

<span data-ttu-id="ec873-104">\[Метод **ерасебинари** доступен для использования в операционных системах, указанных в разделе требования.</span><span class="sxs-lookup"><span data-stu-id="ec873-104">\[The **EraseBinary** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="ec873-105">Он недоступен для использования в Windows Server 2003 с пакетом обновления 1 (SP1) и более поздней версии, Windows Vista, Windows Server 2008 и последующих версиях операционной системы.</span><span class="sxs-lookup"><span data-stu-id="ec873-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="ec873-106">[Модули смарт-карт](/previous-versions/windows/desktop/secsmart/smart-card-modules) предоставляют аналогичные функции.\]</span><span class="sxs-lookup"><span data-stu-id="ec873-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="ec873-107">Метод **ерасебинари** конструирует команду [*блока данных протокола приложения*](../secgloss/a-gly.md) (категориях APDU), которая последовательно устанавливает часть содержимого простейшего файла в логическое состояние стирания, начиная с заданного смещения.</span><span class="sxs-lookup"><span data-stu-id="ec873-107">The **EraseBinary** method constructs an [*application protocol data unit*](../secgloss/a-gly.md) (APDU) command that sequentially sets part of the content of an elementary file to its logical erased state, starting from a given offset.</span></span>

## <a name="syntax"></a><span data-ttu-id="ec873-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="ec873-108">Syntax</span></span>


```C++
HRESULT EraseBinary(
  [in]      BYTE         byP1,
  [in]      BYTE         byP2,
  [in]      LPBYTEBUFFER pData,
  [in, out] LPSCARDCMD   *ppCmd
);
```



## <a name="parameters"></a><span data-ttu-id="ec873-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="ec873-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ec873-110">*byP1* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="ec873-110">*byP1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ec873-111">РФУ.</span><span class="sxs-lookup"><span data-stu-id="ec873-111">RFU position.</span></span>

<span data-ttu-id="ec873-112">Если B8 = 1 в P1, то значения B7 и B6 для P1 задаются равными нулю (РФУ биты), B5 — B1 of P1 — короткий идентификатор EF, а P2 — смещение первого байта, который необходимо стереть (в единицах данных) с начала файла.</span><span class="sxs-lookup"><span data-stu-id="ec873-112">If b8=1 in P1, then b7 and b6 of P1 are set to zero (RFU bits), b5 to b1 of P1 are a short EF identifier and P2 is the offset of the first byte to be erased (in data units) from the beginning of the file.</span></span>

<span data-ttu-id="ec873-113">Если B8 = 0 в P1, то P1 \| \| P2 — это смещение первого байта, который необходимо стереть (в единицах данных) с начала файла.</span><span class="sxs-lookup"><span data-stu-id="ec873-113">If b8=0 in P1, then P1 \|\| P2 is the offset of the first byte to be erased (in data units) from the beginning of the file.</span></span>

<span data-ttu-id="ec873-114">Если поле данных имеется, то оно кодирует смещение первой единицы данных, которую не нужно стирать.</span><span class="sxs-lookup"><span data-stu-id="ec873-114">If the data field is present, it codes the offset of the first data unit not to be erased.</span></span> <span data-ttu-id="ec873-115">Это смещение должно быть выше, чем запрограммировано в P1-P2.</span><span class="sxs-lookup"><span data-stu-id="ec873-115">This offset shall be higher than the one coded in P1-P2.</span></span> <span data-ttu-id="ec873-116">Если поле данных пустое, команда удаляет до конца файла.</span><span class="sxs-lookup"><span data-stu-id="ec873-116">When the data field is empty, the command erases up to the end of the file.</span></span>

</dd> <dt>

<span data-ttu-id="ec873-117">*byP2* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="ec873-117">*byP2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ec873-118">РФУ.</span><span class="sxs-lookup"><span data-stu-id="ec873-118">RFU position.</span></span>

<span data-ttu-id="ec873-119">Если B8 = 1 в P1, то значения B7 и B6 для P1 задаются равными нулю (РФУ биты), B5 — B1 of P1 — короткий идентификатор EF, а P2 — смещение первого байта, который необходимо стереть (в единицах данных) с начала файла.</span><span class="sxs-lookup"><span data-stu-id="ec873-119">If b8=1 in P1, then b7 and b6 of P1 are set to zero (RFU bits), b5 to b1 of P1 are a short EF identifier and P2 is the offset of the first byte to be erased (in data units) from the beginning of the file.</span></span>

<span data-ttu-id="ec873-120">Если B8 = 0 в P1, то P1 \| \| P2 — это смещение первого байта, который необходимо стереть (в единицах данных) с начала файла.</span><span class="sxs-lookup"><span data-stu-id="ec873-120">If b8=0 in P1, then P1 \|\| P2 is the offset of the first byte to be erased (in data units) from the beginning of the file.</span></span>

<span data-ttu-id="ec873-121">Если поле данных имеется, то оно кодирует смещение первой единицы данных, которую не нужно стирать.</span><span class="sxs-lookup"><span data-stu-id="ec873-121">If the data field is present, it codes the offset of the first data unit not to be erased.</span></span> <span data-ttu-id="ec873-122">Это смещение должно быть выше, чем запрограммировано в P1-P2.</span><span class="sxs-lookup"><span data-stu-id="ec873-122">This offset shall be higher than the one coded in P1-P2.</span></span> <span data-ttu-id="ec873-123">Если поле данных пустое, команда удаляет до конца файла.</span><span class="sxs-lookup"><span data-stu-id="ec873-123">When the data field is empty, the command erases up to the end of the file.</span></span>

</dd> <dt>

<span data-ttu-id="ec873-124">*pData* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="ec873-124">*pData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ec873-125">Указатель на данные, указывающие диапазон стирания.</span><span class="sxs-lookup"><span data-stu-id="ec873-125">A pointer to the data that specifies the erase range.</span></span> <span data-ttu-id="ec873-126">Этот параметр может иметь **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="ec873-126">This parameter may be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="ec873-127">*ппкмд* \[ в, out\]</span><span class="sxs-lookup"><span data-stu-id="ec873-127">*ppCmd* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="ec873-128">На входе — указатель на объект интерфейса [**искардкмд**](iscardcmd.md) или **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="ec873-128">On input, a pointer to an [**ISCardCmd**](iscardcmd.md) interface object or **NULL**.</span></span>

<span data-ttu-id="ec873-129">При возвращении он заполняется командой КАТЕГОРИЯХ APDU, созданной этой операцией.</span><span class="sxs-lookup"><span data-stu-id="ec873-129">On return, it is filled with the APDU command constructed by this operation.</span></span> <span data-ttu-id="ec873-130">Если для *ппкмд* было задано **значение NULL**, то объект [*смарт-карты*](../secgloss/s-gly.md) [**искардкмд**](iscardcmd.md) создается внутренне и возвращается с помощью указателя *ппкмд* .</span><span class="sxs-lookup"><span data-stu-id="ec873-130">If *ppCmd* was set to **NULL**, a [*smart card*](../secgloss/s-gly.md) [**ISCardCmd**](iscardcmd.md) object is internally created and returned by using the *ppCmd* pointer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ec873-131">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="ec873-131">Return value</span></span>

<span data-ttu-id="ec873-132">Метод возвращает одно из следующих возможных значений.</span><span class="sxs-lookup"><span data-stu-id="ec873-132">The method returns one of the following possible values.</span></span>



| <span data-ttu-id="ec873-133">Код возврата</span><span class="sxs-lookup"><span data-stu-id="ec873-133">Return code</span></span>                                                                                   | <span data-ttu-id="ec873-134">Описание</span><span class="sxs-lookup"><span data-stu-id="ec873-134">Description</span></span>                                          |
|-----------------------------------------------------------------------------------------------|------------------------------------------------------|
| <dl> <span data-ttu-id="ec873-135"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="ec873-135"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="ec873-136">Операция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="ec873-136">The operation completed successfully.</span></span><br/>     |
| <dl> <span data-ttu-id="ec873-137"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="ec873-137"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="ec873-138">Передан недопустимый параметр.</span><span class="sxs-lookup"><span data-stu-id="ec873-138">A parameter that is not valid was passed.</span></span><br/> |
| <dl> <span data-ttu-id="ec873-139"><dt>**\_указатель E**</dt></span><span class="sxs-lookup"><span data-stu-id="ec873-139"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="ec873-140">Передан неверный указатель.</span><span class="sxs-lookup"><span data-stu-id="ec873-140">A bad pointer was passed in.</span></span><br/>              |
| <dl> <span data-ttu-id="ec873-141"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="ec873-141"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="ec873-142">Недостаточно памяти.</span><span class="sxs-lookup"><span data-stu-id="ec873-142">Out of memory.</span></span><br/>                            |



 

## <a name="remarks"></a><span data-ttu-id="ec873-143">Комментарии</span><span class="sxs-lookup"><span data-stu-id="ec873-143">Remarks</span></span>

<span data-ttu-id="ec873-144">Инкапсулированная команда может быть выполнена только в том случае, если состояние безопасности [*смарт-карты*](../secgloss/s-gly.md) соответствует атрибутам безопасности для обрабатываемого простейшего файла.</span><span class="sxs-lookup"><span data-stu-id="ec873-144">The encapsulated command can only be performed if the security status of the [*smart card*](../secgloss/s-gly.md) satisfies the security attributes of the elementary file being processed.</span></span>

<span data-ttu-id="ec873-145">Если команда содержит допустимый краткий простой идентификатор, она устанавливает файл в качестве текущего простейшего файла.</span><span class="sxs-lookup"><span data-stu-id="ec873-145">When the command contains a valid short elementary identifier, it sets the file as current elementary file.</span></span>

<span data-ttu-id="ec873-146">Простые файлы без прозрачной структуры не могут быть удалены.</span><span class="sxs-lookup"><span data-stu-id="ec873-146">Elementary files without a transparent structure cannot be erased.</span></span> <span data-ttu-id="ec873-147">Инкапсулированная команда прерывается, если применяется к простейшему файлу без прозрачной структуры.</span><span class="sxs-lookup"><span data-stu-id="ec873-147">The encapsulated command aborts if applied to an elementary file without a transparent structure.</span></span>

<span data-ttu-id="ec873-148">Список всех методов, предоставляемых этим интерфейсом, см. в разделе [**ISCardISO7816**](iscardiso7816.md).</span><span class="sxs-lookup"><span data-stu-id="ec873-148">For a list of all the methods provided by this interface, see [**ISCardISO7816**](iscardiso7816.md).</span></span>

<span data-ttu-id="ec873-149">Кроме приведенных выше кодов ошибок COM, этот интерфейс может возвращать код ошибки смарт-карты, если для завершения запроса была вызвана функция смарт-карты.</span><span class="sxs-lookup"><span data-stu-id="ec873-149">In addition to the COM error codes listed above, this interface may return a smart card error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="ec873-150">Дополнительные сведения см. в статье [возвращаемые значения смарт-карты](authentication-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="ec873-150">For more information, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="ec873-151">Требования</span><span class="sxs-lookup"><span data-stu-id="ec873-151">Requirements</span></span>



| <span data-ttu-id="ec873-152">Требование</span><span class="sxs-lookup"><span data-stu-id="ec873-152">Requirement</span></span> | <span data-ttu-id="ec873-153">Значение</span><span class="sxs-lookup"><span data-stu-id="ec873-153">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="ec873-154">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="ec873-154">Minimum supported client</span></span><br/> | <span data-ttu-id="ec873-155">Только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="ec873-155">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="ec873-156">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="ec873-156">Minimum supported server</span></span><br/> | <span data-ttu-id="ec873-157">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="ec873-157">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="ec873-158">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="ec873-158">End of client support</span></span><br/>    | <span data-ttu-id="ec873-159">Windows XP</span><span class="sxs-lookup"><span data-stu-id="ec873-159">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="ec873-160">Поддержка конца сервера</span><span class="sxs-lookup"><span data-stu-id="ec873-160">End of server support</span></span><br/>    | <span data-ttu-id="ec873-161">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="ec873-161">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="ec873-162">Header</span><span class="sxs-lookup"><span data-stu-id="ec873-162">Header</span></span><br/>                   | <dl> <span data-ttu-id="ec873-163"><dt>Скардссп. h</dt></span><span class="sxs-lookup"><span data-stu-id="ec873-163"><dt>Scardssp.h</dt></span></span> </dl>   |
| <span data-ttu-id="ec873-164">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="ec873-164">Type library</span></span><br/>             | <dl> <span data-ttu-id="ec873-165"><dt>Скардсрв. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="ec873-165"><dt>Scardsrv.tlb</dt></span></span> </dl> |
| <span data-ttu-id="ec873-166">DLL</span><span class="sxs-lookup"><span data-stu-id="ec873-166">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ec873-167"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ec873-167"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="ec873-168">IID</span><span class="sxs-lookup"><span data-stu-id="ec873-168">IID</span></span><br/>                      | <span data-ttu-id="ec873-169">IID \_ ISCardISO7816 определен как 53B6AA68-3F56-11D0-916B-00AA00C18068</span><span class="sxs-lookup"><span data-stu-id="ec873-169">IID\_ISCardISO7816 is defined as 53B6AA68-3F56-11D0-916B-00AA00C18068</span></span><br/>        |



## <a name="see-also"></a><span data-ttu-id="ec873-170">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="ec873-170">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ec873-171">**ISCardISO7816**</span><span class="sxs-lookup"><span data-stu-id="ec873-171">**ISCardISO7816**</span></span>](iscardiso7816.md)
</dt> <dt>

[<span data-ttu-id="ec873-172">**реадбинари**</span><span class="sxs-lookup"><span data-stu-id="ec873-172">**ReadBinary**</span></span>](iscardiso7816-readbinary.md)
</dt> <dt>

[<span data-ttu-id="ec873-173">**упдатебинари**</span><span class="sxs-lookup"><span data-stu-id="ec873-173">**UpdateBinary**</span></span>](iscardiso7816-updatebinary.md)
</dt> <dt>

[<span data-ttu-id="ec873-174">**вритебинари**</span><span class="sxs-lookup"><span data-stu-id="ec873-174">**WriteBinary**</span></span>](iscardiso7816-writebinary.md)
</dt> </dl>

 

 
