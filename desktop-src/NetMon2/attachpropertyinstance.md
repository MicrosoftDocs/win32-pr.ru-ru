---
description: Функция Аттачпропертинстанце сопоставляет существующее свойство с конкретным расположением в распознанных данных.
ms.assetid: b44cf8d1-939b-45da-8a9a-b4bdcf9faf43
title: Функция Аттачпропертинстанце (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AttachPropertyInstance
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 50ab07967605f8a24ba330a3cb13f80c833cf542
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103911648"
---
# <a name="attachpropertyinstance-function"></a><span data-ttu-id="5473d-103">Функция Аттачпропертинстанце</span><span class="sxs-lookup"><span data-stu-id="5473d-103">AttachPropertyInstance function</span></span>

<span data-ttu-id="5473d-104">Функция **аттачпропертинстанце** сопоставляет существующее свойство с конкретным расположением в распознанных данных.</span><span class="sxs-lookup"><span data-stu-id="5473d-104">The **AttachPropertyInstance** function maps an existing property to a specific location in the recognized data.</span></span>

## <a name="syntax"></a><span data-ttu-id="5473d-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="5473d-105">Syntax</span></span>


```C++
BOOL WINAPI AttachPropertyInstance(
  _In_ HFRAME    hFrame,
  _In_ HPROPERTY hProperty,
  _In_ DWORD     Length,
  _In_ ULPVOID   lpData,
  _In_ DWORD     HelpID,
  _In_ DWORD     IndentLevel,
  _In_ DWORD     IFlags
);
```



## <a name="parameters"></a><span data-ttu-id="5473d-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="5473d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5473d-107">*хфраме* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="5473d-107">*hFrame* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5473d-108">Обработчик для анализируемого кадра.</span><span class="sxs-lookup"><span data-stu-id="5473d-108">Handle to the frame that is being parsed.</span></span> <span data-ttu-id="5473d-109">Используйте маркер, передаваемый в библиотеку DLL средства синтаксического анализа, в параметре *хфраме* функции [**аттачпропертиес**](attachproperties.md) .</span><span class="sxs-lookup"><span data-stu-id="5473d-109">Use the handle passed to the parser DLL in the *hFrame* parameter of the [**AttachProperties**](attachproperties.md) function.</span></span>

</dd> <dt>

<span data-ttu-id="5473d-110">*хпроперти* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="5473d-110">*hProperty* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5473d-111">Обработчик для структуры [**PROPERTYINFO**](propertyinfo.md) , определяющей свойство.</span><span class="sxs-lookup"><span data-stu-id="5473d-111">Handle to a [**PROPERTYINFO**](propertyinfo.md) structure that defines the property.</span></span> <span data-ttu-id="5473d-112">При реализации функции [**регистрации**](register-parser.md) экспорта указывается структура **PROPERTYINFO** , определяющая свойство.</span><span class="sxs-lookup"><span data-stu-id="5473d-112">When you implement the [**Register**](register-parser.md) export function you specify the **PROPERTYINFO** structure that defines the property.</span></span>

</dd> <dt>

<span data-ttu-id="5473d-113">*Длина* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="5473d-113">*Length* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5473d-114">Длина данных для этого экземпляра свойства.</span><span class="sxs-lookup"><span data-stu-id="5473d-114">Length of the data for this instance of the property.</span></span>

</dd> <dt>

<span data-ttu-id="5473d-115">*лпдата* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="5473d-115">*lpData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5473d-116">Указатель на расположение в распознанных данных, где находится значение свойства.</span><span class="sxs-lookup"><span data-stu-id="5473d-116">Pointer to the location in the recognized data where the property value is located.</span></span> <span data-ttu-id="5473d-117">Используйте указатель, передаваемый в библиотеку DLL средства синтаксического анализа, в параметре *лппротокол* функции [**аттачпропертиес**](attachproperties.md) .</span><span class="sxs-lookup"><span data-stu-id="5473d-117">Use the pointer passed to the parser DLL in the *lpProtocol* parameter of the [**AttachProperties**](attachproperties.md) function.</span></span>

</dd> <dt>

<span data-ttu-id="5473d-118">*Идентификатор справки* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="5473d-118">*HelpID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5473d-119">Идентификатор (от 0 до 2047), используемый для установки контекстно-зависимой справки для свойства.</span><span class="sxs-lookup"><span data-stu-id="5473d-119">Identifier (from 0 to 2047) used to set context-sensitive Help for the property.</span></span>

<span data-ttu-id="5473d-120">Номер идентификатора указывается относительно файла справки, связанного с [*базой данных свойств*](p.md)протокола.</span><span class="sxs-lookup"><span data-stu-id="5473d-120">The identifier number is relative to the Help file associated with the protocol [*property database*](p.md).</span></span>

</dd> <dt>

<span data-ttu-id="5473d-121">*Индентлевел* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="5473d-121">*IndentLevel* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5473d-122">Уровень отступа (от 0 до 15), используемый для иерархического вывода свойства.</span><span class="sxs-lookup"><span data-stu-id="5473d-122">Indentation level (from 0 to 15) used to display a property hierarchically.</span></span>

<span data-ttu-id="5473d-123">Сетевой монитор использует уровни от 0 до 14 для отступа свойств.</span><span class="sxs-lookup"><span data-stu-id="5473d-123">Network Monitor uses levels 0 through 14 to indent properties.</span></span> <span data-ttu-id="5473d-124">Уровень 15 — это специальное значение, которое позволяет средству синтаксического анализа присоединить скрытое свойство, которое не является видимым.</span><span class="sxs-lookup"><span data-stu-id="5473d-124">Level 15 is a special value that allows a parser to attach a hidden property that is not visible.</span></span>

</dd> <dt>

<span data-ttu-id="5473d-125">*Ифлагс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="5473d-125">*IFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5473d-126">Значение БИТОВого поля, указывающее порядок битов в свойстве.</span><span class="sxs-lookup"><span data-stu-id="5473d-126">A BIT field value that indicates the order of the BITs within a property.</span></span> <span data-ttu-id="5473d-127">Предыдущие синтаксические анализаторы, устанавливающие *fError* в значение 0 или 1, теперь должны установить *fError* в ифлаг \_ Error.</span><span class="sxs-lookup"><span data-stu-id="5473d-127">Previous parsers that set *fError* to 0 or 1, should now set *fError* to IFLAG\_ERROR.</span></span> <span data-ttu-id="5473d-128">Присвойте этому параметру одно из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="5473d-128">Set this parameter to one of the following values.</span></span>



| <span data-ttu-id="5473d-129">Значение</span><span class="sxs-lookup"><span data-stu-id="5473d-129">Value</span></span>                                                                                                                                                         | <span data-ttu-id="5473d-130">Значение</span><span class="sxs-lookup"><span data-stu-id="5473d-130">Meaning</span></span>                                                         |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <span id="IFLAG_ERROR"></span><span id="iflag_error"></span><dl> <span data-ttu-id="5473d-131"><dt>**ИФЛАГ, \_ Ошибка**</dt></span><span class="sxs-lookup"><span data-stu-id="5473d-131"><dt>**IFLAG\_ERROR**</dt></span></span> </dl>       | <span data-ttu-id="5473d-132">Данные в кадре имеют ошибку.</span><span class="sxs-lookup"><span data-stu-id="5473d-132">Data in the frame has an error.</span></span><br/>                      |
| <span id="IFLAG_SWAPPED"></span><span id="iflag_swapped"></span><dl> <span data-ttu-id="5473d-133"><dt>**ИФЛАГ \_ переключенный**</dt></span><span class="sxs-lookup"><span data-stu-id="5473d-133"><dt>**IFLAG\_SWAPPED**</dt></span></span> </dl> | <span data-ttu-id="5473d-134">Во время присоединения **слово** Byte имеет формат, отличный от Intel.</span><span class="sxs-lookup"><span data-stu-id="5473d-134">At attach time, **WORD** byte is a non-Intel format.</span></span><br/> |
| <span id="IFLAG_UNICODE"></span><span id="iflag_unicode"></span><dl> <span data-ttu-id="5473d-135"><dt>**ИФЛАГ \_ Юникод**</dt></span><span class="sxs-lookup"><span data-stu-id="5473d-135"><dt>**IFLAG\_UNICODE**</dt></span></span> </dl> | <span data-ttu-id="5473d-136">Во время подключения **строка** имеет кодировку Unicode.</span><span class="sxs-lookup"><span data-stu-id="5473d-136">At attach time, **STRING** is Unicode.</span></span><br/>               |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5473d-137">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="5473d-137">Return value</span></span>

<span data-ttu-id="5473d-138">Если функция выполнена успешно, возвращается значение **true**.</span><span class="sxs-lookup"><span data-stu-id="5473d-138">If the function is successful, the return value is **TRUE**.</span></span>

<span data-ttu-id="5473d-139">Если функция завершается неудачно, возвращается значение **false**.</span><span class="sxs-lookup"><span data-stu-id="5473d-139">If the function is unsuccessful, the return value is **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="5473d-140">Комментарии</span><span class="sxs-lookup"><span data-stu-id="5473d-140">Remarks</span></span>

<span data-ttu-id="5473d-141">Функция **аттачпропертинстанце** вызывается во время реализации функции экспорта [**аттачпропертиес**](attachproperties.md) .</span><span class="sxs-lookup"><span data-stu-id="5473d-141">The **AttachPropertyInstance** function is called during the implementation of the [**AttachProperties**](attachproperties.md) export function.</span></span> <span data-ttu-id="5473d-142">При присоединении к данным свойства сетевой монитор создает структуру [**пропертинст**](propertyinst.md) , определяющую экземпляр присоединенного свойства.</span><span class="sxs-lookup"><span data-stu-id="5473d-142">When a property is attached to the data, Network Monitor creates a [**PROPERTYINST**](propertyinst.md) structure that defines the instance of the attached property.</span></span>

<span data-ttu-id="5473d-143">Во время реализации [**аттачпропертиес**](attachproperties.md)вызовите **аттачпропертинстанце** , чтобы использовать данные в том виде, в котором они существуют в записи.</span><span class="sxs-lookup"><span data-stu-id="5473d-143">During the implementation of [**AttachProperties**](attachproperties.md), call **AttachPropertyInstance** to use the data as it exists in the capture.</span></span> <span data-ttu-id="5473d-144">Можно также вызвать функцию [**аттачпропертинстанцеекс**](attachpropertyinstanceex.md) для изменения данных свойства.</span><span class="sxs-lookup"><span data-stu-id="5473d-144">You can also call [**AttachPropertyInstanceEx**](attachpropertyinstanceex.md) function to modify the property data.</span></span> <span data-ttu-id="5473d-145">Однако рекомендуется использовать данные в том виде, в котором они существуют в записи.</span><span class="sxs-lookup"><span data-stu-id="5473d-145">However, it is advised that you use the data as it exists in the capture.</span></span>



| <span data-ttu-id="5473d-146">Дополнительные сведения о</span><span class="sxs-lookup"><span data-stu-id="5473d-146">For Information on</span></span>                                        | <span data-ttu-id="5473d-147">См.</span><span class="sxs-lookup"><span data-stu-id="5473d-147">See</span></span>                                                                |
|-----------------------------------------------------------|--------------------------------------------------------------------|
| <span data-ttu-id="5473d-148">Какие анализаторы и как они работают с сетевой монитор.</span><span class="sxs-lookup"><span data-stu-id="5473d-148">What parsers are, and how they work with Network Monitor.</span></span> | [<span data-ttu-id="5473d-149">**Анализаторы**</span><span class="sxs-lookup"><span data-stu-id="5473d-149">**Parsers**</span></span>](parsers.md)                                         |
| <span data-ttu-id="5473d-150">Как вызвать **аттачпропертинстанце**.</span><span class="sxs-lookup"><span data-stu-id="5473d-150">How to call **AttachPropertyInstance**.</span></span>                   | [<span data-ttu-id="5473d-151">Реализация Аттачпропертиес</span><span class="sxs-lookup"><span data-stu-id="5473d-151">Implementing AttachProperties</span></span>](implementing-attachproperties.md) |



 

## <a name="requirements"></a><span data-ttu-id="5473d-152">Требования</span><span class="sxs-lookup"><span data-stu-id="5473d-152">Requirements</span></span>



| <span data-ttu-id="5473d-153">Требование</span><span class="sxs-lookup"><span data-stu-id="5473d-153">Requirement</span></span> | <span data-ttu-id="5473d-154">Значение</span><span class="sxs-lookup"><span data-stu-id="5473d-154">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="5473d-155">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="5473d-155">Minimum supported client</span></span><br/> | <span data-ttu-id="5473d-156">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="5473d-156">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="5473d-157">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="5473d-157">Minimum supported server</span></span><br/> | <span data-ttu-id="5473d-158">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="5473d-158">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="5473d-159">Заголовок</span><span class="sxs-lookup"><span data-stu-id="5473d-159">Header</span></span><br/>                   | <dl> <span data-ttu-id="5473d-160"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="5473d-160"><dt>Netmon.h</dt></span></span> </dl>  |
| <span data-ttu-id="5473d-161">Библиотека</span><span class="sxs-lookup"><span data-stu-id="5473d-161">Library</span></span><br/>                  | <dl> <span data-ttu-id="5473d-162"><dt>Нмапи. lib</dt></span><span class="sxs-lookup"><span data-stu-id="5473d-162"><dt>Nmapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="5473d-163">DLL</span><span class="sxs-lookup"><span data-stu-id="5473d-163">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5473d-164"><dt>Nmapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5473d-164"><dt>Nmapi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5473d-165">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="5473d-165">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5473d-166">**аттачпропертиес**</span><span class="sxs-lookup"><span data-stu-id="5473d-166">**AttachProperties**</span></span>](attachproperties.md)
</dt> <dt>

[<span data-ttu-id="5473d-167">**аттачпропертинстанцеекс**</span><span class="sxs-lookup"><span data-stu-id="5473d-167">**AttachPropertyInstanceEx**</span></span>](attachpropertyinstanceex.md)
</dt> <dt>

[<span data-ttu-id="5473d-168">**пропертинст**</span><span class="sxs-lookup"><span data-stu-id="5473d-168">**PROPERTYINST**</span></span>](propertyinst.md)
</dt> </dl>

 

 




