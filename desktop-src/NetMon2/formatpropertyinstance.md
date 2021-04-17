---
description: Форматирует данные экземпляра свойства с помощью универсального модуля форматирования, который сетевой монитор предоставляет.
ms.assetid: 36206601-7519-45c8-a14e-707b318c539d
title: Функция Форматпропертинстанце (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FormatPropertyInstance
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 39d51df93a04efa8631fcfbd583075d7e3500bff
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105673199"
---
# <a name="formatpropertyinstance-function"></a><span data-ttu-id="6d374-103">Функция Форматпропертинстанце</span><span class="sxs-lookup"><span data-stu-id="6d374-103">FormatPropertyInstance function</span></span>

<span data-ttu-id="6d374-104">Функция **форматпропертинстанце** форматирует данные экземпляра свойства с помощью универсального модуля форматирования, который сетевой монитор предоставляет.</span><span class="sxs-lookup"><span data-stu-id="6d374-104">The **FormatPropertyInstance** function formats the property instance data using the generic formatter that Network Monitor provides.</span></span>

## <a name="syntax"></a><span data-ttu-id="6d374-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="6d374-105">Syntax</span></span>


```C++
DWORD WINAPIV FormatPropertyInstance(
  _Inout_ LPPROPERTYINST lpPropertyInst
);
```



## <a name="parameters"></a><span data-ttu-id="6d374-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="6d374-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6d374-107">*лппропертинст* \[ в, out\]</span><span class="sxs-lookup"><span data-stu-id="6d374-107">*lpPropertyInst* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="6d374-108">Указатель на структуру [пропертинст](propertyinst.md) , содержащую данные экземпляра.</span><span class="sxs-lookup"><span data-stu-id="6d374-108">A pointer to a [PROPERTYINST](propertyinst.md) structure that contains the instance data.</span></span>

<span data-ttu-id="6d374-109">На входе универсальный модуль форматирования принимает данные экземпляра из одного из членов объединения **пропертинст** и преобразует эти данные в стандартную отформатированную строку.</span><span class="sxs-lookup"><span data-stu-id="6d374-109">On input, the generic formatter takes the instance data from one of the **PROPERTYINST** union members and converts that data to a predefined formatted string.</span></span>

<span data-ttu-id="6d374-110">В выходных данных универсальный модуль форматирования устанавливает элемент **сзпропертитекст** структуры **пропертинст** в указатель на отформатированную строку.</span><span class="sxs-lookup"><span data-stu-id="6d374-110">On output, the generic formatter sets the **szPropertyText** member of the **PROPERTYINST** structure to a pointer to the formatted string.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6d374-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="6d374-111">Return value</span></span>

<span data-ttu-id="6d374-112">Если функция выполнена успешно, возвращается значение НМЕРР \_ Success.</span><span class="sxs-lookup"><span data-stu-id="6d374-112">If the function is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="6d374-113">Если функция не выполнена, возвращаемое значение является кодом ошибки из Нмерр. h.</span><span class="sxs-lookup"><span data-stu-id="6d374-113">If the function is unsuccessful, the return value is an error code from NMerr.h.</span></span>

## <a name="remarks"></a><span data-ttu-id="6d374-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="6d374-114">Remarks</span></span>

<span data-ttu-id="6d374-115">Библиотека DLL средства синтаксического анализа косвенно вызывает функцию **форматпропертинстанце** , если универсальный модуль форматирования требуется для форматирования данных, отображаемых в области сведений пользовательского интерфейса сетевой монитор.</span><span class="sxs-lookup"><span data-stu-id="6d374-115">The parser DLL indirectly calls the **FormatPropertyInstance** function when the generic formatter is required to format data for display in the details pane of the Network Monitor UI.</span></span> <span data-ttu-id="6d374-116">Чтобы вызвать **форматпропертинстанце** , укажите его в элементе **инстанцедата** структуры [PROPERTYINFO](propertyinfo.md) при определении свойства.</span><span class="sxs-lookup"><span data-stu-id="6d374-116">To call **FormatPropertyInstance** specify it in the **InstanceData** member of the [PROPERTYINFO](propertyinfo.md) structure when you define the property.</span></span>

> [!Note]  
> <span data-ttu-id="6d374-117">Средство синтаксического анализа не распознает, какая функция вызывается, когда необходимо отформатировать экземпляр свойства.</span><span class="sxs-lookup"><span data-stu-id="6d374-117">The parser does not recognize which function is called when it must format an instance of a property.</span></span> <span data-ttu-id="6d374-118">Функция может быть **форматпропертинстанце** или пользовательской функцией форматирования, определенной средством синтаксического анализа.</span><span class="sxs-lookup"><span data-stu-id="6d374-118">The function can be **FormatPropertyInstance** or a custom format function defined by the parser.</span></span> <span data-ttu-id="6d374-119">Средство синтаксического анализа вызывает любую функцию формата, указанную элементом **инстанцедата** структуры **PROPERTYINFO** для свойства.</span><span class="sxs-lookup"><span data-stu-id="6d374-119">The parser calls whatever format function is specified by the **InstanceData** member of the **PROPERTYINFO** structure for the property.</span></span>

 

<span data-ttu-id="6d374-120">Дополнительные сведения и пример реализации [форматпропертиес](formatproperties.md)см. в разделе [Реализация форматпропертиес](implementing-formatproperties.md).</span><span class="sxs-lookup"><span data-stu-id="6d374-120">For more information and an example of how to implement [formatproperties](formatproperties.md), see [Implementing FormatProperties](implementing-formatproperties.md).</span></span> <span data-ttu-id="6d374-121">Дополнительные сведения о форматировании универсального модуля форматирования для различных типов данных см. в разделе [Общие выходные данные модуля форматирования](generic-formatter-output.md).</span><span class="sxs-lookup"><span data-stu-id="6d374-121">For more information about how the generic formatter formats different types of data, see [Generic Formatter Output](generic-formatter-output.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="6d374-122">Требования</span><span class="sxs-lookup"><span data-stu-id="6d374-122">Requirements</span></span>



| <span data-ttu-id="6d374-123">Требование</span><span class="sxs-lookup"><span data-stu-id="6d374-123">Requirement</span></span> | <span data-ttu-id="6d374-124">Значение</span><span class="sxs-lookup"><span data-stu-id="6d374-124">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="6d374-125">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="6d374-125">Minimum supported client</span></span><br/> | <span data-ttu-id="6d374-126">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="6d374-126">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="6d374-127">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="6d374-127">Minimum supported server</span></span><br/> | <span data-ttu-id="6d374-128">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="6d374-128">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="6d374-129">Заголовок</span><span class="sxs-lookup"><span data-stu-id="6d374-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="6d374-130"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="6d374-130"><dt>Netmon.h</dt></span></span> </dl>  |
| <span data-ttu-id="6d374-131">Библиотека</span><span class="sxs-lookup"><span data-stu-id="6d374-131">Library</span></span><br/>                  | <dl> <span data-ttu-id="6d374-132"><dt>Нмапи. lib</dt></span><span class="sxs-lookup"><span data-stu-id="6d374-132"><dt>Nmapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="6d374-133">DLL</span><span class="sxs-lookup"><span data-stu-id="6d374-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6d374-134"><dt>Nmapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6d374-134"><dt>Nmapi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6d374-135">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="6d374-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6d374-136">PROPERTYINFO</span><span class="sxs-lookup"><span data-stu-id="6d374-136">PROPERTYINFO</span></span>](propertyinfo.md)
</dt> <dt>

[<span data-ttu-id="6d374-137">пропертинст</span><span class="sxs-lookup"><span data-stu-id="6d374-137">PROPERTYINST</span></span>](propertyinst.md)
</dt> </dl>

 

 




