---
description: Функция экспорта Аттачпропертиес сопоставляет свойства с расположением в пределах части распознанных данных. Аттачпропертиес должен быть реализован для каждого средства синтаксического анализа, поддерживаемого библиотекой DLL средства синтаксического анализа.
ms.assetid: ef28f571-8364-47d0-841c-580e89333afd
title: Функция обратного вызова Аттачпропертиес (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AttachProperties
api_type:
- UserDefined
api_location:
- Netmon.h
ms.openlocfilehash: 3b3cb4be93b8d960b39f0f5c5cf2b5a4809573cf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105673646"
---
# <a name="attachproperties-callback-function"></a><span data-ttu-id="1daee-104">Функция обратного вызова Аттачпропертиес</span><span class="sxs-lookup"><span data-stu-id="1daee-104">AttachProperties callback function</span></span>

<span data-ttu-id="1daee-105">Функция экспорта **аттачпропертиес** сопоставляет свойства с расположением в пределах части распознанных данных.</span><span class="sxs-lookup"><span data-stu-id="1daee-105">The **AttachProperties** export function maps the properties to a location within a piece of recognized data.</span></span> <span data-ttu-id="1daee-106">**Аттачпропертиес** должен быть реализован для каждого средства синтаксического анализа, ПОДДЕРЖИВАЕМого библиотекой DLL средства синтаксического анализа.</span><span class="sxs-lookup"><span data-stu-id="1daee-106">**AttachProperties** must be implemented for each parser that the parser DLL supports.</span></span>

## <a name="syntax"></a><span data-ttu-id="1daee-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="1daee-107">Syntax</span></span>


```C++
DWORD AttachProperties(
  _In_ HFRAME    hFrame,
  _In_ LPBYTE    lpFrame,
  _In_ LPBYTE    lpProtocol,
  _In_ DWORD     MacType,
  _In_ DWORD     BytesLeft,
  _In_ HPROTOCOL hPreviousProtocol,
  _In_ DWORD     nPreviousProtocolOffset,
  _In_ DWORD     lpInstData
);
```



## <a name="parameters"></a><span data-ttu-id="1daee-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="1daee-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1daee-109">*хфраме* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="1daee-109">*hFrame* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1daee-110">Маркер анализируемого кадра.</span><span class="sxs-lookup"><span data-stu-id="1daee-110">Handle of the frame that is being parsed.</span></span>

</dd> <dt>

<span data-ttu-id="1daee-111">*лпфраме* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="1daee-111">*lpFrame* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1daee-112">Указатель на первый байт в кадре.</span><span class="sxs-lookup"><span data-stu-id="1daee-112">Pointer to the first byte in a frame.</span></span>

</dd> <dt>

<span data-ttu-id="1daee-113">*лппротокол* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="1daee-113">*lpProtocol* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1daee-114">Указатель на начало распознанных данных.</span><span class="sxs-lookup"><span data-stu-id="1daee-114">Pointer to the start of the recognized data.</span></span>

</dd> <dt>

<span data-ttu-id="1daee-115">*MacType* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="1daee-115">*MacType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1daee-116">Значение MAC первого протокола в кадре.</span><span class="sxs-lookup"><span data-stu-id="1daee-116">MAC value of the first protocol in a frame.</span></span> <span data-ttu-id="1daee-117">*MacType* может быть одним из следующих:</span><span class="sxs-lookup"><span data-stu-id="1daee-117">The *MacType* can be one of the following:</span></span>



| <span data-ttu-id="1daee-118">Значение</span><span class="sxs-lookup"><span data-stu-id="1daee-118">Value</span></span>                                                                                                                                                                         | <span data-ttu-id="1daee-119">Значение</span><span class="sxs-lookup"><span data-stu-id="1daee-119">Meaning</span></span>                 |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------|
| <span id="MAC_TYPE_ETHERNET"></span><span id="mac_type_ethernet"></span><dl> <span data-ttu-id="1daee-120"><dt>**\_тип Mac \_ Ethernet**</dt></span><span class="sxs-lookup"><span data-stu-id="1daee-120"><dt>**MAC\_TYPE\_ETHERNET**</dt></span></span> </dl>    | <span data-ttu-id="1daee-121">802.3</span><span class="sxs-lookup"><span data-stu-id="1daee-121">802.3</span></span> <br/>       |
| <span id="MAC_TYPE_TOKENRING"></span><span id="mac_type_tokenring"></span><dl> <span data-ttu-id="1daee-122"><dt>**\_тип Mac \_ токенринг**</dt></span><span class="sxs-lookup"><span data-stu-id="1daee-122"><dt>**MAC\_TYPE\_TOKENRING**</dt></span></span> </dl> | <span data-ttu-id="1daee-123">802.5</span><span class="sxs-lookup"><span data-stu-id="1daee-123">802.5</span></span> <br/>       |
| <span id="MAC_TYPE_FDDI"></span><span id="mac_type_fddi"></span><dl> <span data-ttu-id="1daee-124"><dt>**\_тип Mac \_ FDDI**</dt></span><span class="sxs-lookup"><span data-stu-id="1daee-124"><dt>**MAC\_TYPE\_FDDI**</dt></span></span> </dl>                | <span data-ttu-id="1daee-125">ANSI X3T 9,5</span><span class="sxs-lookup"><span data-stu-id="1daee-125">ANSI X3T9.5</span></span> <br/> |



 

</dd> <dt>

<span data-ttu-id="1daee-126">*Битеслефт* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="1daee-126">*BytesLeft* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1daee-127">Оставшееся число байтов в кадре, начиная с начала распознанных данных.</span><span class="sxs-lookup"><span data-stu-id="1daee-127">The remaining number of bytes in a frame   starting at the beginning of the recognized data.</span></span>

</dd> <dt>

<span data-ttu-id="1daee-128">*хпревиауспротокол* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="1daee-128">*hPreviousProtocol* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1daee-129">Обработчик предыдущего протокола.</span><span class="sxs-lookup"><span data-stu-id="1daee-129">Handle of the previous protocol.</span></span>

</dd> <dt>

<span data-ttu-id="1daee-130">*нпревиауспротоколоффсет* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="1daee-130">*nPreviousProtocolOffset* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1daee-131">Смещение предыдущего протокола, начиная с начала кадра.</span><span class="sxs-lookup"><span data-stu-id="1daee-131">Offset of the previous protocol   starting at the beginning of the frame.</span></span>

</dd> <dt>

<span data-ttu-id="1daee-132">*лпинстдата* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="1daee-132">*lpInstData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1daee-133">Указатель на данные экземпляра, которые предоставляет предыдущий протокол.</span><span class="sxs-lookup"><span data-stu-id="1daee-133">Pointer to the instance data that the previous protocol provides.</span></span> <span data-ttu-id="1daee-134">Длина данных экземпляра не может превышать значение типа DWORD \_ .</span><span class="sxs-lookup"><span data-stu-id="1daee-134">Instance data cannot be longer than a DWORD\_PTR in length.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1daee-135">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="1daee-135">Return value</span></span>

<span data-ttu-id="1daee-136">Если функция выполнена успешно, возвращаемое значение является указателем на первый байт после распознанных данных в кадре или **значение NULL** , если распознанные данные являются последним элементом данных в кадре.</span><span class="sxs-lookup"><span data-stu-id="1daee-136">If the function is successful, the return value is a pointer to the first byte after the recognized data in a frame or **NULL** if the recognized data is the last piece of data in a frame.</span></span>

<span data-ttu-id="1daee-137">Если функция завершается неудачно, возвращаемое значение является указателем на распознаваемые данные.</span><span class="sxs-lookup"><span data-stu-id="1daee-137">If the function is unsuccessful, the return value is a pointer to the recognized data.</span></span> <span data-ttu-id="1daee-138">Параметр *лппротокол* передает указатель на библиотеку DLL средства синтаксического анализа.</span><span class="sxs-lookup"><span data-stu-id="1daee-138">The *lpProtocol* parameter passes the pointer to the parser DLL.</span></span>

## <a name="remarks"></a><span data-ttu-id="1daee-139">Комментарии</span><span class="sxs-lookup"><span data-stu-id="1daee-139">Remarks</span></span>

<span data-ttu-id="1daee-140">Сетевой монитор вызывает функцию **аттачпропертиес** для каждого средства синтаксического анализа, распознающего фрагмент данных в кадре.</span><span class="sxs-lookup"><span data-stu-id="1daee-140">Network Monitor calls the **AttachProperties** function for each parser that recognizes a piece of data in a frame.</span></span> <span data-ttu-id="1daee-141">Обратите внимание, что средство синтаксического анализа определяет, какие свойства существуют в распознанных данных и где находится каждое свойство.</span><span class="sxs-lookup"><span data-stu-id="1daee-141">Note that the parser determines which properties exist in the recognized data, and where each property is located.</span></span>

<span data-ttu-id="1daee-142">Во время реализации **аттачпропертиес** вызовите [аттачпропертинстанце](attachpropertyinstance.md) , чтобы использовать данные в том виде, в котором они существуют в записи.</span><span class="sxs-lookup"><span data-stu-id="1daee-142">During the implementation of **AttachProperties**, call [AttachPropertyInstance](attachpropertyinstance.md) to use the data as it exists in the capture.</span></span> <span data-ttu-id="1daee-143">Можно также вызвать функцию [аттачпропертинстанцеекс](attachpropertyinstanceex.md) для изменения данных свойства.</span><span class="sxs-lookup"><span data-stu-id="1daee-143">You can also call [AttachPropertyInstanceEx](attachpropertyinstanceex.md) function to modify the property data.</span></span> <span data-ttu-id="1daee-144">Однако рекомендуется использовать данные в том виде, в котором они существуют в записи.</span><span class="sxs-lookup"><span data-stu-id="1daee-144">However, it is advised that you use the data as it exists in the capture.</span></span>

<span data-ttu-id="1daee-145">Функции **аттачпропертинстанцеекс** и **аттачпропертинстанце** вызываются только для свойств, существующих в распознанных данных.</span><span class="sxs-lookup"><span data-stu-id="1daee-145">The **AttachPropertyInstanceEx** and **AttachPropertyInstance** functions are called only for the properties that exist in the recognized data.</span></span> <span data-ttu-id="1daee-146">Обратите внимание, что сетевой монитор имеет [*базу данных свойств*](p.md) для средства синтаксического анализа, которая содержит описание всех свойств, поддерживаемых синтаксическим анализатором.</span><span class="sxs-lookup"><span data-stu-id="1daee-146">Note that Network Monitor has a [*property database*](p.md) for the parser that contains a description of all the properties that the parser supports.</span></span>

<span data-ttu-id="1daee-147">**Данные экземпляров**</span><span class="sxs-lookup"><span data-stu-id="1daee-147">**Instance data**</span></span>

<span data-ttu-id="1daee-148">Данные экземпляра — это сведения, передаваемые из одного средства синтаксического анализа в другое.</span><span class="sxs-lookup"><span data-stu-id="1daee-148">Instance data is information that is passed from one parser to another.</span></span> <span data-ttu-id="1daee-149">Данные экземпляра могут быть любыми данными, размер которых меньше или равен DWORD или \_ указателем на данные, например необработанные данные кадра, которые не должны выделяться или освобождаться анализатором.</span><span class="sxs-lookup"><span data-stu-id="1daee-149">Instance data can be any data that is less than or equal to a DWORD\_PTR in length, or a pointer to data, such as raw frame data, that does not need to be allocated by or freed by the parser.</span></span> <span data-ttu-id="1daee-150">В параметре *лпинстдата* функций **аттачпропертиес** и [рекогнизефраме](recognizeframe.md) сетевой монитор предоставляет указатель на данные экземпляра предыдущего протокола.</span><span class="sxs-lookup"><span data-stu-id="1daee-150">In the *lpInstData* parameter of the **AttachProperties** and [RecognizeFrame](recognizeframe.md) functions, Network Monitor provides a pointer to the instance data of the previous protocol.</span></span> <span data-ttu-id="1daee-151">Вы можете задать данные экземпляра для средства синтаксического анализа во время реализации **рекогнизефраме**.</span><span class="sxs-lookup"><span data-stu-id="1daee-151">You can set the instance data for your parser during your implementation of **RecognizeFrame**.</span></span>



| <span data-ttu-id="1daee-152">Для получения информации о</span><span class="sxs-lookup"><span data-stu-id="1daee-152">For information on</span></span>                                          | <span data-ttu-id="1daee-153">См.</span><span class="sxs-lookup"><span data-stu-id="1daee-153">See</span></span>                                                                |
|-------------------------------------------------------------|--------------------------------------------------------------------|
| <span data-ttu-id="1daee-154">Какие анализаторы и как они работают с сетевой монитор.</span><span class="sxs-lookup"><span data-stu-id="1daee-154">What parsers are, and how they work with Network Monitor.</span></span>   | [<span data-ttu-id="1daee-155">Анализаторы</span><span class="sxs-lookup"><span data-stu-id="1daee-155">Parsers</span></span>](parsers.md)                                             |
| <span data-ttu-id="1daee-156">Какие точки входа включены в библиотеку DLL средства синтаксического анализа.</span><span class="sxs-lookup"><span data-stu-id="1daee-156">What entry points are included in the parser DLL.</span></span>           | [<span data-ttu-id="1daee-157">Архитектура библиотеки DLL средства синтаксического анализа</span><span class="sxs-lookup"><span data-stu-id="1daee-157">Parser DLL Architecture</span></span>](parser-dll-architecture.md)             |
| <span data-ttu-id="1daee-158">Распознавание данных.</span><span class="sxs-lookup"><span data-stu-id="1daee-158">How to recognize data.</span></span>                                      | [<span data-ttu-id="1daee-159">Реализация Рекогнизефраме</span><span class="sxs-lookup"><span data-stu-id="1daee-159">Implementing RecognizeFrame</span></span>](implementing-recognizeframe.md)     |
| <span data-ttu-id="1daee-160">Создание базы данных свойств.</span><span class="sxs-lookup"><span data-stu-id="1daee-160">How to create a property database.</span></span>                          | [<span data-ttu-id="1daee-161">Реализация регистра</span><span class="sxs-lookup"><span data-stu-id="1daee-161">Implementing Register</span></span>](implementing-register.md)                 |
| <span data-ttu-id="1daee-162">Реализация **аттачпропертиес**  включает пример.</span><span class="sxs-lookup"><span data-stu-id="1daee-162">How to implement **AttachProperties**  includes an example.</span></span> | [<span data-ttu-id="1daee-163">Реализация Аттачпропертиес</span><span class="sxs-lookup"><span data-stu-id="1daee-163">Implementing AttachProperties</span></span>](implementing-attachproperties.md) |



 

## <a name="requirements"></a><span data-ttu-id="1daee-164">Требования</span><span class="sxs-lookup"><span data-stu-id="1daee-164">Requirements</span></span>



| <span data-ttu-id="1daee-165">Требование</span><span class="sxs-lookup"><span data-stu-id="1daee-165">Requirement</span></span> | <span data-ttu-id="1daee-166">Значение</span><span class="sxs-lookup"><span data-stu-id="1daee-166">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="1daee-167">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="1daee-167">Minimum supported client</span></span><br/> | <span data-ttu-id="1daee-168">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="1daee-168">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="1daee-169">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="1daee-169">Minimum supported server</span></span><br/> | <span data-ttu-id="1daee-170">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="1daee-170">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="1daee-171">Заголовок</span><span class="sxs-lookup"><span data-stu-id="1daee-171">Header</span></span><br/>                   | <dl> <span data-ttu-id="1daee-172"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="1daee-172"><dt>Netmon.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1daee-173">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="1daee-173">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1daee-174">аттачпропертинстанце</span><span class="sxs-lookup"><span data-stu-id="1daee-174">AttachPropertyInstance</span></span>](attachpropertyinstance.md)
</dt> <dt>

[<span data-ttu-id="1daee-175">аттачпропертинстанцеекс</span><span class="sxs-lookup"><span data-stu-id="1daee-175">AttachPropertyInstanceEx</span></span>](attachpropertyinstanceex.md)
</dt> <dt>

[<span data-ttu-id="1daee-176">рекогнизефраме</span><span class="sxs-lookup"><span data-stu-id="1daee-176">RecognizeFrame</span></span>](recognizeframe.md)
</dt> </dl>

 

 




