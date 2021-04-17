---
description: Функция Аттачпропертинстанцеекс сопоставляет существующее свойство с конкретным расположением в распознанных данных и изменяет значение данных свойства.
ms.assetid: 08bd1959-5ce8-4cb8-af8b-abbf4839c484
title: Функция Аттачпропертинстанцеекс (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AttachPropertyInstanceEx
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 1e0841c49e54d10d38a56d6206bc255b0aa7c49a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105673647"
---
# <a name="attachpropertyinstanceex-function"></a><span data-ttu-id="80c27-103">Функция Аттачпропертинстанцеекс</span><span class="sxs-lookup"><span data-stu-id="80c27-103">AttachPropertyInstanceEx function</span></span>

<span data-ttu-id="80c27-104">Функция **аттачпропертинстанцеекс** сопоставляет существующее свойство с конкретным расположением в распознанных данных и изменяет значение данных свойства.</span><span class="sxs-lookup"><span data-stu-id="80c27-104">The **AttachPropertyInstanceEx** function maps an existing property to a specific location in the recognized data, and modifies the value of the property data.</span></span>

## <a name="syntax"></a><span data-ttu-id="80c27-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="80c27-105">Syntax</span></span>


```C++
BOOL WINAPI AttachPropertyInstanceEx(
  _In_ HFRAME    hFrame,
  _In_ HPROPERTY hProperty,
  _In_ DWORD     Length,
  _In_ ULPVOID   lpData,
  _In_ DWORD     LengthEx,
  _In_ ULPVOID   lpDataEx,
  _In_ DWORD     HelpID,
  _In_ DWORD     IndentLevel,
  _In_ DWORD     IFlags
);
```



## <a name="parameters"></a><span data-ttu-id="80c27-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="80c27-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="80c27-107">*хфраме* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="80c27-107">*hFrame* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="80c27-108">Обработчик для анализируемого кадра.</span><span class="sxs-lookup"><span data-stu-id="80c27-108">Handle to the frame that is being parsed.</span></span> <span data-ttu-id="80c27-109">Используйте маркер, передаваемый в библиотеку DLL средства синтаксического анализа, в параметре *хфраме* функции [**аттачпропертиес**](attachproperties.md) .</span><span class="sxs-lookup"><span data-stu-id="80c27-109">Use the handle passed to the parser DLL in the *hFrame* parameter of the [**AttachProperties**](attachproperties.md) function.</span></span>

</dd> <dt>

<span data-ttu-id="80c27-110">*хпроперти* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="80c27-110">*hProperty* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="80c27-111">Обработчик для структуры [**PROPERTYINFO**](propertyinfo.md) , определяющей свойство.</span><span class="sxs-lookup"><span data-stu-id="80c27-111">Handle to a [**PROPERTYINFO**](propertyinfo.md) structure that defines the property.</span></span> <span data-ttu-id="80c27-112">При реализации функции [**регистрации**](register-parser.md) экспорта указывается структура **PROPERTYINFO** , определяющая свойство.</span><span class="sxs-lookup"><span data-stu-id="80c27-112">When you implement the [**Register**](register-parser.md) export function you specify the **PROPERTYINFO** structure that defines the property.</span></span>

</dd> <dt>

<span data-ttu-id="80c27-113">*Длина* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="80c27-113">*Length* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="80c27-114">Длина данных для этого экземпляра свойства.</span><span class="sxs-lookup"><span data-stu-id="80c27-114">Length of the data for this instance of the property.</span></span>

</dd> <dt>

<span data-ttu-id="80c27-115">*лпдата* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="80c27-115">*lpData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="80c27-116">Указатель на расположение в распознанных данных, где находится значение свойства.</span><span class="sxs-lookup"><span data-stu-id="80c27-116">Pointer to the location in the recognized data where the property value is located.</span></span> <span data-ttu-id="80c27-117">Используйте указатель, передаваемый в библиотеку DLL средства синтаксического анализа, в параметре *лппротокол* функции [**аттачпропертиес**](attachproperties.md) .</span><span class="sxs-lookup"><span data-stu-id="80c27-117">Use the pointer passed to the parser DLL in the *lpProtocol* parameter of the [**AttachProperties**](attachproperties.md) function.</span></span>

</dd> <dt>

<span data-ttu-id="80c27-118">*Ленгсекс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="80c27-118">*LengthEx* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="80c27-119">Длина расширенной длины данных в байтах.</span><span class="sxs-lookup"><span data-stu-id="80c27-119">Length of the extended data   length in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="80c27-120">*лпдатаекс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="80c27-120">*lpDataEx* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="80c27-121">Указатель на Расширенные данные, которые обычно представляют собой переменную стека, которая содержит данные расширения.</span><span class="sxs-lookup"><span data-stu-id="80c27-121">Pointer to the extended data, which is typically a stack variable that contains the extend data.</span></span>

</dd> <dt>

<span data-ttu-id="80c27-122">*Идентификатор справки* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="80c27-122">*HelpID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="80c27-123">Идентификатор (от 0 до 2047), используемый для установки контекстно-зависимой справки для свойства.</span><span class="sxs-lookup"><span data-stu-id="80c27-123">Identifier (from 0 to 2047) used to set context-sensitive Help for a property.</span></span>

<span data-ttu-id="80c27-124">Номер *идентификатор справки* относится к файлу справки, связанному с [*базой данных свойств*](p.md)протокола.</span><span class="sxs-lookup"><span data-stu-id="80c27-124">The *HelpID* number is relative to the Help file associated with the protocol [*property database*](p.md).</span></span>

</dd> <dt>

<span data-ttu-id="80c27-125">*Индентлевел* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="80c27-125">*IndentLevel* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="80c27-126">Уровень отступа (от 0 до 15), используемый для иерархического вывода свойства.</span><span class="sxs-lookup"><span data-stu-id="80c27-126">Indentation level (from 0 to 15) used to display a property hierarchically.</span></span>

<span data-ttu-id="80c27-127">Сетевой монитор использует уровни от 0 до 9.</span><span class="sxs-lookup"><span data-stu-id="80c27-127">Network Monitor uses levels 0 through 9.</span></span> <span data-ttu-id="80c27-128">Уровень 15 — это специальное значение, которое позволяет средству синтаксического анализа присоединить скрытое свойство, которое не является видимым.</span><span class="sxs-lookup"><span data-stu-id="80c27-128">Level 15 is a special value that allows the parser to attach a hidden property that is not visible.</span></span>

</dd> <dt>

<span data-ttu-id="80c27-129">*Ифлагс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="80c27-129">*IFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="80c27-130">Значение БИТОВого поля, указывающее порядок битов в свойстве.</span><span class="sxs-lookup"><span data-stu-id="80c27-130">A BIT field value that indicates the order of the BITs within a property.</span></span> <span data-ttu-id="80c27-131">Предыдущие синтаксические анализаторы, устанавливающие *fError* в значение 0 или 1, теперь должны установить *fError* в ифлаг \_ Error.</span><span class="sxs-lookup"><span data-stu-id="80c27-131">Previous parsers that set *fError* to 0 or 1, should now set *fError* to IFLAG\_ERROR.</span></span> <span data-ttu-id="80c27-132">Присвойте этому параметру одно из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="80c27-132">Set this parameter to one of the following values.</span></span>



| <span data-ttu-id="80c27-133">Значение</span><span class="sxs-lookup"><span data-stu-id="80c27-133">Value</span></span>                                                                                                                                                         | <span data-ttu-id="80c27-134">Значение</span><span class="sxs-lookup"><span data-stu-id="80c27-134">Meaning</span></span>                                                         |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <span id="IFLAG_ERROR"></span><span id="iflag_error"></span><dl> <span data-ttu-id="80c27-135"><dt>**ИФЛАГ, \_ Ошибка**</dt></span><span class="sxs-lookup"><span data-stu-id="80c27-135"><dt>**IFLAG\_ERROR**</dt></span></span> </dl>       | <span data-ttu-id="80c27-136">Данные в кадре имеют ошибку.</span><span class="sxs-lookup"><span data-stu-id="80c27-136">Data in the frame has an error.</span></span><br/>                      |
| <span id="IFLAG_SWAPPED"></span><span id="iflag_swapped"></span><dl> <span data-ttu-id="80c27-137"><dt>**ИФЛАГ \_ переключенный**</dt></span><span class="sxs-lookup"><span data-stu-id="80c27-137"><dt>**IFLAG\_SWAPPED**</dt></span></span> </dl> | <span data-ttu-id="80c27-138">Во время присоединения **слово** Byte имеет формат, отличный от Intel.</span><span class="sxs-lookup"><span data-stu-id="80c27-138">At attach time, **WORD** byte is a non-Intel format.</span></span><br/> |
| <span id="IFLAG_UNICODE"></span><span id="iflag_unicode"></span><dl> <span data-ttu-id="80c27-139"><dt>**ИФЛАГ \_ Юникод**</dt></span><span class="sxs-lookup"><span data-stu-id="80c27-139"><dt>**IFLAG\_UNICODE**</dt></span></span> </dl> | <span data-ttu-id="80c27-140">Во время подключения **строка** имеет кодировку Unicode.</span><span class="sxs-lookup"><span data-stu-id="80c27-140">At attach time, **STRING** is Unicode.</span></span><br/>               |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="80c27-141">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="80c27-141">Return value</span></span>

<span data-ttu-id="80c27-142">Если функция выполнена успешно, возвращается значение **true**.</span><span class="sxs-lookup"><span data-stu-id="80c27-142">If the function is successful, the return value is **TRUE**.</span></span>

<span data-ttu-id="80c27-143">Если функция завершается неудачно, возвращается значение **false**.</span><span class="sxs-lookup"><span data-stu-id="80c27-143">If the function is unsuccessful, the return value is **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="80c27-144">Комментарии</span><span class="sxs-lookup"><span data-stu-id="80c27-144">Remarks</span></span>

<span data-ttu-id="80c27-145">Функция **аттачпропертинстанцеекс** вызывается во время реализации функции экспорта [**аттачпропертиес**](attachproperties.md) .</span><span class="sxs-lookup"><span data-stu-id="80c27-145">The **AttachPropertyInstanceEx** function is called during the implementation of the [**AttachProperties**](attachproperties.md) export function.</span></span> <span data-ttu-id="80c27-146">При присоединении свойства к данным с помощью Аттачпропертинстанцеекс сетевой монитор создает структуру [**пропертинст**](propertyinst.md) , которая определяет экземпляр присоединенного свойства и структуру [**пропертинстекс**](propertyinstex.md) , определяющую Расширенные данные.</span><span class="sxs-lookup"><span data-stu-id="80c27-146">When a property is attached to the data using AttachPropertyInstanceEx, Network Monitor creates a [**PROPERTYINST**](propertyinst.md) structure that defines the instance of the attached property and a [**PROPERTYINSTEX**](propertyinstex.md) structure that defines the extended data.</span></span>

<span data-ttu-id="80c27-147">Если вызывается **аттачпропертинстанцеекс** и не предоставлены расширенные данные, параметр *Лпдатаекс* имеет **значение NULL** или параметр *ленгсекс* равен 0, вызов **аттачпропертинстанцеекс** функционально эквивалентен вызову [**аттачпропертинстанце**](attachpropertyinstance.md) .</span><span class="sxs-lookup"><span data-stu-id="80c27-147">If **AttachPropertyInstanceEx** is called and no extended data is provided, the *lpDataEx* parameter is **NULL** or the *LengthEx* parameter is 0, the **AttachPropertyInstanceEx** call is functionally equivalent to an [**AttachPropertyInstance**](attachpropertyinstance.md) call.</span></span>

<span data-ttu-id="80c27-148">Во время реализации [**аттачпропертиес**](attachproperties.md)вызовите [**аттачпропертинстанце**](attachpropertyinstance.md) , чтобы использовать данные в том виде, в котором они существуют в записи.</span><span class="sxs-lookup"><span data-stu-id="80c27-148">During the implementation of [**AttachProperties**](attachproperties.md), call [**AttachPropertyInstance**](attachpropertyinstance.md) to use the data as it exists in the capture.</span></span> <span data-ttu-id="80c27-149">Можно также вызвать функцию **аттачпропертинстанцеекс** для изменения данных свойства.</span><span class="sxs-lookup"><span data-stu-id="80c27-149">You can also call **AttachPropertyInstanceEx** function to modify the property data.</span></span> <span data-ttu-id="80c27-150">Однако рекомендуется использовать данные в том виде, в котором они существуют в записи.</span><span class="sxs-lookup"><span data-stu-id="80c27-150">However, it is advised that you use the data as it exists in the capture.</span></span>

## <a name="requirements"></a><span data-ttu-id="80c27-151">Требования</span><span class="sxs-lookup"><span data-stu-id="80c27-151">Requirements</span></span>



| <span data-ttu-id="80c27-152">Требование</span><span class="sxs-lookup"><span data-stu-id="80c27-152">Requirement</span></span> | <span data-ttu-id="80c27-153">Значение</span><span class="sxs-lookup"><span data-stu-id="80c27-153">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="80c27-154">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="80c27-154">Minimum supported client</span></span><br/> | <span data-ttu-id="80c27-155">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="80c27-155">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="80c27-156">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="80c27-156">Minimum supported server</span></span><br/> | <span data-ttu-id="80c27-157">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="80c27-157">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="80c27-158">Заголовок</span><span class="sxs-lookup"><span data-stu-id="80c27-158">Header</span></span><br/>                   | <dl> <span data-ttu-id="80c27-159"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="80c27-159"><dt>Netmon.h</dt></span></span> </dl>  |
| <span data-ttu-id="80c27-160">Библиотека</span><span class="sxs-lookup"><span data-stu-id="80c27-160">Library</span></span><br/>                  | <dl> <span data-ttu-id="80c27-161"><dt>Нмапи. lib</dt></span><span class="sxs-lookup"><span data-stu-id="80c27-161"><dt>Nmapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="80c27-162">DLL</span><span class="sxs-lookup"><span data-stu-id="80c27-162">DLL</span></span><br/>                      | <dl> <span data-ttu-id="80c27-163"><dt>Nmapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="80c27-163"><dt>Nmapi.dll</dt></span></span> </dl> |



 

 




