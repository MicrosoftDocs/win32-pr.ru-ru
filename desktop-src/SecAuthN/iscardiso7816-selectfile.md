---
description: Метод Селектфиле конструирует команду блока данных протокола приложения (КАТЕГОРИЯХ APDU), которая задает текущий простейший файл в логическом канале. Последующие команды могут неявно ссылаться на текущий файл по логическому каналу.
ms.assetid: cb6231b3-fb1c-4350-8797-9efaa663c21b
title: 'Метод ISCardISO7816:: Селектфиле (Скардссп. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardISO7816.SelectFile
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 9bab499d32a65a2e6b4348458ec42328029760ce
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104264690"
---
# <a name="iscardiso7816selectfile-method"></a><span data-ttu-id="1c9e2-104">Метод ISCardISO7816:: Селектфиле</span><span class="sxs-lookup"><span data-stu-id="1c9e2-104">ISCardISO7816::SelectFile method</span></span>

<span data-ttu-id="1c9e2-105">\[Метод **селектфиле** доступен для использования в операционных системах, указанных в разделе требования.</span><span class="sxs-lookup"><span data-stu-id="1c9e2-105">\[The **SelectFile** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="1c9e2-106">Он недоступен для использования в Windows Server 2003 с пакетом обновления 1 (SP1) и более поздней версии, Windows Vista, Windows Server 2008 и последующих версиях операционной системы.</span><span class="sxs-lookup"><span data-stu-id="1c9e2-106">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="1c9e2-107">[Модули смарт-карт](/previous-versions/windows/desktop/secsmart/smart-card-modules) предоставляют аналогичные функции.\]</span><span class="sxs-lookup"><span data-stu-id="1c9e2-107">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="1c9e2-108">Метод **селектфиле** конструирует команду [*блока данных протокола приложения*](../secgloss/a-gly.md) (категориях APDU), которая задает текущий простейший файл в логическом канале.</span><span class="sxs-lookup"><span data-stu-id="1c9e2-108">The **SelectFile** method constructs an [*application protocol data unit*](../secgloss/a-gly.md) (APDU) command that sets a current elementary file within a logical channel.</span></span> <span data-ttu-id="1c9e2-109">Последующие команды могут неявно ссылаться на текущий файл по логическому каналу.</span><span class="sxs-lookup"><span data-stu-id="1c9e2-109">Subsequent commands may implicitly refer to the current file through the logical channel.</span></span>

<span data-ttu-id="1c9e2-110">Выбор каталога (DF) в хранилище в виде хранилища, который может быть корнем (MF) хранилища файлов, делает его текущей DF.</span><span class="sxs-lookup"><span data-stu-id="1c9e2-110">Selecting a directory (DF) within the card filestore — which may be the root (MF) of the filestore — makes it the current DF.</span></span> <span data-ttu-id="1c9e2-111">После такого выбора можно ссылаться на неявный простой файл с этим логическим каналом.</span><span class="sxs-lookup"><span data-stu-id="1c9e2-111">After such a selection, an implicit current elementary file may be referred to through that logical channel.</span></span>

<span data-ttu-id="1c9e2-112">При выборе простейшего файла выбранный файл и его родительский файл устанавливаются в качестве текущих файлов.</span><span class="sxs-lookup"><span data-stu-id="1c9e2-112">Selecting an elementary file sets the selected file and its parent as current files.</span></span>

<span data-ttu-id="1c9e2-113">После ответа на сброс протокол MF неявно выбирается через базовый логический канал, если не указано иное в исторических байтах или в исходной строке данных.</span><span class="sxs-lookup"><span data-stu-id="1c9e2-113">After the answer to reset, the MF is implicitly selected through the basic logical channel, unless specified differently in the historical bytes or in the initial data string.</span></span>

## <a name="syntax"></a><span data-ttu-id="1c9e2-114">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="1c9e2-114">Syntax</span></span>


```C++
HRESULT SelectFile(
  [in]      BYTE         byP1,
  [in]      BYTE         byP2,
  [in]      LPBYTEBUFFER pData,
  [in]      LONG         lBytesToRead,
  [in, out] LPSCARDCMD   *ppCmd
);
```



## <a name="parameters"></a><span data-ttu-id="1c9e2-115">Параметры</span><span class="sxs-lookup"><span data-stu-id="1c9e2-115">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1c9e2-116">*byP1* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="1c9e2-116">*byP1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1c9e2-117">Элемент управления Selection.</span><span class="sxs-lookup"><span data-stu-id="1c9e2-117">Selection control.</span></span>



| <span data-ttu-id="1c9e2-118">P1 (Верхний байт в Word): 8 7 6 5 4 3 2 1</span><span class="sxs-lookup"><span data-stu-id="1c9e2-118">P1 (upper byte in word): 8 7 6 5 4 3 2 1</span></span>                                                                                                                                                            | <span data-ttu-id="1c9e2-119">Значение</span><span class="sxs-lookup"><span data-stu-id="1c9e2-119">Meaning</span></span>                            |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------|
| <span id="000000xx"></span><span id="000000XX"></span><dl> <span data-ttu-id="1c9e2-120"><dt>**000000xx**</dt><dt></dt></span><span class="sxs-lookup"><span data-stu-id="1c9e2-120"><dt>**000000xx**</dt> <dt></dt></span></span> </dl> | <span data-ttu-id="1c9e2-121">Выберите идентификатор файла</span><span class="sxs-lookup"><span data-stu-id="1c9e2-121">Select File ID</span></span><br/>          |
| <span id="00000000"></span><dl> <span data-ttu-id="1c9e2-122"><dt>**00000000**</dt><dt></dt></span><span class="sxs-lookup"><span data-stu-id="1c9e2-122"><dt>**00000000**</dt> <dt></dt></span></span> </dl>                            | <span data-ttu-id="1c9e2-123">EF, DF или MF</span><span class="sxs-lookup"><span data-stu-id="1c9e2-123">EF, DF, or MF</span></span><br/>           |
| <span id="00000001"></span><dl> <span data-ttu-id="1c9e2-124"><dt>**00000001**</dt><dt></dt></span><span class="sxs-lookup"><span data-stu-id="1c9e2-124"><dt>**00000001**</dt> <dt></dt></span></span> </dl>                            | <span data-ttu-id="1c9e2-125">Дочерняя DF</span><span class="sxs-lookup"><span data-stu-id="1c9e2-125">Child DF</span></span><br/>                |
| <span id="00000010"></span><dl> <span data-ttu-id="1c9e2-126"><dt>**00000010**</dt><dt></dt></span><span class="sxs-lookup"><span data-stu-id="1c9e2-126"><dt>**00000010**</dt> <dt></dt></span></span> </dl>                            | <span data-ttu-id="1c9e2-127">EF в DF</span><span class="sxs-lookup"><span data-stu-id="1c9e2-127">EF under DF</span></span><br/>             |
| <span id="00000011"></span><dl> <span data-ttu-id="1c9e2-128"><dt>**00000011**</dt><dt></dt></span><span class="sxs-lookup"><span data-stu-id="1c9e2-128"><dt>**00000011**</dt> <dt></dt></span></span> </dl>                            | <span data-ttu-id="1c9e2-129">Родительская DF текущей DF</span><span class="sxs-lookup"><span data-stu-id="1c9e2-129">Parent DF of current DF</span></span><br/> |



 

<span data-ttu-id="1c9e2-130">Если P1 = 00, карточка известна либо из-за определенного кода идентификатора файла, либо из-за контекста выполнения команды, если файл для выбора — MF, DF или EF.</span><span class="sxs-lookup"><span data-stu-id="1c9e2-130">When P1=00, the card knows either because of a specific coding of the file ID or because of the context of execution of the command if the file to select is the MF, a DF, or an EF.</span></span>

<span data-ttu-id="1c9e2-131">Если P1-P2 = 0000, если указан идентификатор файла, он должен быть уникальным в следующих средах:</span><span class="sxs-lookup"><span data-stu-id="1c9e2-131">When P1-P2=0000, if a file ID is provided, then it shall be unique in the following environments:</span></span>

-   <span data-ttu-id="1c9e2-132">Непосредственные дочерние элементы текущей DF</span><span class="sxs-lookup"><span data-stu-id="1c9e2-132">Immediate children of the current DF</span></span>
-   <span data-ttu-id="1c9e2-133">Родительская DF</span><span class="sxs-lookup"><span data-stu-id="1c9e2-133">Parent DF</span></span>
-   <span data-ttu-id="1c9e2-134">Непосредственные дочерние элементы родительской DF</span><span class="sxs-lookup"><span data-stu-id="1c9e2-134">Immediate children of the parent DF</span></span>

<span data-ttu-id="1c9e2-135">Если P1-P2 = 0000 и если поле данных пустое или равно 3F00, то выберите MF.</span><span class="sxs-lookup"><span data-stu-id="1c9e2-135">If P1-P2=0000 and if the data field is empty or equal to 3F00, then select the MF.</span></span>

<span data-ttu-id="1c9e2-136">Если P1 = 04, то поле данных является именем DF, возможно, усеченным справа.</span><span class="sxs-lookup"><span data-stu-id="1c9e2-136">When P1=04, the data field is a DF name, possibly right truncated.</span></span>

<span data-ttu-id="1c9e2-137">Если поддерживается, последовательные команды с одним и тем же полем данных должны выбирать DFs, имена которых совпадают с полем данных (то есть начинаются с поля данных команды).</span><span class="sxs-lookup"><span data-stu-id="1c9e2-137">When supported, successive such commands with the same data field shall select DFs whose names match with the data field (that is, start with the command data field).</span></span> <span data-ttu-id="1c9e2-138">Если карта принимает команду с пустым полем данных, можно последовательно выбрать все или подмножество DFs.</span><span class="sxs-lookup"><span data-stu-id="1c9e2-138">If the card accepts the command with an empty data field, then all or a subset of the DFs can be successively selected.</span></span>

</dd> <dt>

<span data-ttu-id="1c9e2-139">*byP2* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="1c9e2-139">*byP2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1c9e2-140">Элемент управления Selection.</span><span class="sxs-lookup"><span data-stu-id="1c9e2-140">Selection control.</span></span>

</dd> <dt>

<span data-ttu-id="1c9e2-141">*pData* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="1c9e2-141">*pData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1c9e2-142">Данные для операции, если это необходимо; else, **null**.</span><span class="sxs-lookup"><span data-stu-id="1c9e2-142">Data for operation if needed; else, **NULL**.</span></span> <span data-ttu-id="1c9e2-143">Ниже перечислены типы данных, передаваемых в этом параметре.</span><span class="sxs-lookup"><span data-stu-id="1c9e2-143">Types of data that are passed in this parameter include:</span></span>

-   <span data-ttu-id="1c9e2-144">Идентификатор файла</span><span class="sxs-lookup"><span data-stu-id="1c9e2-144">file ID</span></span>
-   <span data-ttu-id="1c9e2-145">путь из MF</span><span class="sxs-lookup"><span data-stu-id="1c9e2-145">path from the MF</span></span>
-   <span data-ttu-id="1c9e2-146">путь из текущей DF</span><span class="sxs-lookup"><span data-stu-id="1c9e2-146">path from the current DF</span></span>
-   <span data-ttu-id="1c9e2-147">Имя DF</span><span class="sxs-lookup"><span data-stu-id="1c9e2-147">DF name</span></span>

</dd> <dt>

<span data-ttu-id="1c9e2-148">*лбитестореад* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="1c9e2-148">*lBytesToRead* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1c9e2-149">Пустой (т. е. 0) или максимальная длина ожидаемых данных в ответе.</span><span class="sxs-lookup"><span data-stu-id="1c9e2-149">Empty (that is, 0) or maximum length of data expected in response.</span></span>

</dd> <dt>

<span data-ttu-id="1c9e2-150">*ппкмд* \[ в, out\]</span><span class="sxs-lookup"><span data-stu-id="1c9e2-150">*ppCmd* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="1c9e2-151">На входе — указатель на объект интерфейса [**искардкмд**](iscardcmd.md) или **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="1c9e2-151">On input, a pointer to an [**ISCardCmd**](iscardcmd.md) interface object or **NULL**.</span></span>

<span data-ttu-id="1c9e2-152">При возвращении он заполняется командой КАТЕГОРИЯХ APDU, созданной этой операцией.</span><span class="sxs-lookup"><span data-stu-id="1c9e2-152">On return, it is filled with the APDU command constructed by this operation.</span></span> <span data-ttu-id="1c9e2-153">Если для *ппкмд* было задано **значение NULL**, то объект [*смарт-карты*](../secgloss/s-gly.md) [**искардкмд**](iscardcmd.md) создается внутренним образом и возвращается через указатель *ппкмд* .</span><span class="sxs-lookup"><span data-stu-id="1c9e2-153">If *ppCmd* was set to **NULL**, a [*smart card*](../secgloss/s-gly.md) [**ISCardCmd**](iscardcmd.md) object is internally created and returned via the *ppCmd* pointer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1c9e2-154">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="1c9e2-154">Return value</span></span>

<span data-ttu-id="1c9e2-155">Метод возвращает одно из следующих возможных значений.</span><span class="sxs-lookup"><span data-stu-id="1c9e2-155">The method returns one of the following possible values.</span></span>



| <span data-ttu-id="1c9e2-156">Код возврата</span><span class="sxs-lookup"><span data-stu-id="1c9e2-156">Return code</span></span>                                                                                   | <span data-ttu-id="1c9e2-157">Описание</span><span class="sxs-lookup"><span data-stu-id="1c9e2-157">Description</span></span>                                  |
|-----------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="1c9e2-158"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="1c9e2-158"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="1c9e2-159">Operation completed successfully (Операция выполнена успешно).</span><span class="sxs-lookup"><span data-stu-id="1c9e2-159">Operation completed successfully.</span></span><br/> |
| <dl> <span data-ttu-id="1c9e2-160"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="1c9e2-160"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="1c9e2-161">Недопустимый параметр.</span><span class="sxs-lookup"><span data-stu-id="1c9e2-161">Invalid parameter.</span></span><br/>                |
| <dl> <span data-ttu-id="1c9e2-162"><dt>**\_указатель E**</dt></span><span class="sxs-lookup"><span data-stu-id="1c9e2-162"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="1c9e2-163">Передан неверный указатель.</span><span class="sxs-lookup"><span data-stu-id="1c9e2-163">A bad pointer was passed in.</span></span><br/>      |
| <dl> <span data-ttu-id="1c9e2-164"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="1c9e2-164"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="1c9e2-165">Недостаточно памяти.</span><span class="sxs-lookup"><span data-stu-id="1c9e2-165">Out of memory.</span></span><br/>                    |



 

## <a name="remarks"></a><span data-ttu-id="1c9e2-166">Комментарии</span><span class="sxs-lookup"><span data-stu-id="1c9e2-166">Remarks</span></span>

<span data-ttu-id="1c9e2-167">Если не указано иное, правильное выполнение инкапсулированной команды изменяет состояние безопасности согласно следующим правилам.</span><span class="sxs-lookup"><span data-stu-id="1c9e2-167">Unless otherwise specified, the correct execution of the encapsulated command modifies the security status according to the following rules:</span></span>

-   <span data-ttu-id="1c9e2-168">При изменении текущего простейшего файла или при отсутствии текущего простейшего файла состояние безопасности, относящееся к предыдущему текущему простейшему файлу, теряется.</span><span class="sxs-lookup"><span data-stu-id="1c9e2-168">When the current elementary file is changed, or when there is no current elementary file, the security status specific to a former current elementary file is lost.</span></span>
-   <span data-ttu-id="1c9e2-169">Если текущий каталог хранилища файлов (DF) является потомком или идентичен бывшей текущей DF, состояние безопасности, относящееся к бывшей текущей DF, будет утрачено.</span><span class="sxs-lookup"><span data-stu-id="1c9e2-169">When the current filestore directory (DF) is descendant of, or identical to the former current DF, the security status specific to the former current DF is lost.</span></span> <span data-ttu-id="1c9e2-170">Сохраняется состояние безопасности, общее для всех распространенных предков предыдущей и новой текущей DF.</span><span class="sxs-lookup"><span data-stu-id="1c9e2-170">The security status common to all common ancestors of the previous and new current DF is maintained.</span></span>

<span data-ttu-id="1c9e2-171">Список всех методов, предоставляемых этим интерфейсом, см. в разделе [**ISCardISO7816**](iscardiso7816.md).</span><span class="sxs-lookup"><span data-stu-id="1c9e2-171">For a list of all the methods provided by this interface, see [**ISCardISO7816**](iscardiso7816.md).</span></span>

<span data-ttu-id="1c9e2-172">Кроме приведенных выше кодов ошибок COM, этот интерфейс может возвращать код ошибки смарт-карты, если для завершения запроса была вызвана функция смарт-карты.</span><span class="sxs-lookup"><span data-stu-id="1c9e2-172">In addition to the COM error codes listed above, this interface may return a smart card error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="1c9e2-173">Дополнительные сведения см. в статье [возвращаемые значения смарт-карты](authentication-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="1c9e2-173">For more information, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="1c9e2-174">Требования</span><span class="sxs-lookup"><span data-stu-id="1c9e2-174">Requirements</span></span>



| <span data-ttu-id="1c9e2-175">Требование</span><span class="sxs-lookup"><span data-stu-id="1c9e2-175">Requirement</span></span> | <span data-ttu-id="1c9e2-176">Значение</span><span class="sxs-lookup"><span data-stu-id="1c9e2-176">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="1c9e2-177">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="1c9e2-177">Minimum supported client</span></span><br/> | <span data-ttu-id="1c9e2-178">Только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="1c9e2-178">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="1c9e2-179">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="1c9e2-179">Minimum supported server</span></span><br/> | <span data-ttu-id="1c9e2-180">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="1c9e2-180">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="1c9e2-181">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="1c9e2-181">End of client support</span></span><br/>    | <span data-ttu-id="1c9e2-182">Windows XP</span><span class="sxs-lookup"><span data-stu-id="1c9e2-182">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="1c9e2-183">Поддержка конца сервера</span><span class="sxs-lookup"><span data-stu-id="1c9e2-183">End of server support</span></span><br/>    | <span data-ttu-id="1c9e2-184">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="1c9e2-184">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="1c9e2-185">Header</span><span class="sxs-lookup"><span data-stu-id="1c9e2-185">Header</span></span><br/>                   | <dl> <span data-ttu-id="1c9e2-186"><dt>Скардссп. h</dt></span><span class="sxs-lookup"><span data-stu-id="1c9e2-186"><dt>Scardssp.h</dt></span></span> </dl>   |
| <span data-ttu-id="1c9e2-187">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="1c9e2-187">Type library</span></span><br/>             | <dl> <span data-ttu-id="1c9e2-188"><dt>Скардсрв. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="1c9e2-188"><dt>Scardsrv.tlb</dt></span></span> </dl> |
| <span data-ttu-id="1c9e2-189">DLL</span><span class="sxs-lookup"><span data-stu-id="1c9e2-189">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1c9e2-190"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1c9e2-190"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="1c9e2-191">IID</span><span class="sxs-lookup"><span data-stu-id="1c9e2-191">IID</span></span><br/>                      | <span data-ttu-id="1c9e2-192">IID \_ ISCardISO7816 определен как 53B6AA68-3F56-11D0-916B-00AA00C18068</span><span class="sxs-lookup"><span data-stu-id="1c9e2-192">IID\_ISCardISO7816 is defined as 53B6AA68-3F56-11D0-916B-00AA00C18068</span></span><br/>        |



## <a name="see-also"></a><span data-ttu-id="1c9e2-193">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="1c9e2-193">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1c9e2-194">**ISCardISO7816**</span><span class="sxs-lookup"><span data-stu-id="1c9e2-194">**ISCardISO7816**</span></span>](iscardiso7816.md)
</dt> </dl>

 

 
