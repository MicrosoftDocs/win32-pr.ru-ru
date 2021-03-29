---
description: Функция экспорта Форматпропертиес форматирует данные, отображаемые в области сведений пользовательского интерфейса сетевой монитор. Если вы хотите отображать данные в области сведений, необходимо реализовать функцию экспорта Форматпропертиес во всех библиотеках DLL средства синтаксического анализа.
ms.assetid: 78e0b4b9-f19e-41cb-8504-635f3f9ac1ee
title: Функция обратного вызова Форматпропертиес (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FormatProperties
api_type:
- UserDefined
api_location:
- Netmon.h
ms.openlocfilehash: 61707b49fa88490e1aa22ac89f33dfd97ec20cbd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105662193"
---
# <a name="formatproperties-callback-function"></a><span data-ttu-id="e1fa7-104">Функция обратного вызова Форматпропертиес</span><span class="sxs-lookup"><span data-stu-id="e1fa7-104">FormatProperties callback function</span></span>

<span data-ttu-id="e1fa7-105">Функция экспорта **форматпропертиес** форматирует данные, отображаемые в области сведений пользовательского интерфейса сетевой монитор.</span><span class="sxs-lookup"><span data-stu-id="e1fa7-105">The **FormatProperties** export function formats the data that is displayed in the details pane of the Network Monitor UI.</span></span> <span data-ttu-id="e1fa7-106">Если вы хотите отображать данные в области сведений, необходимо реализовать функцию экспорта **форматпропертиес** во всех библиотеках DLL средства синтаксического анализа.</span><span class="sxs-lookup"><span data-stu-id="e1fa7-106">If you want to display data in the details pane, you must implement the **FormatProperties** export function in all parser DLLs.</span></span>

## <a name="syntax"></a><span data-ttu-id="e1fa7-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="e1fa7-107">Syntax</span></span>


```C++
DWORD FormatProperties(
  _In_ HFRAME         hFrame,
  _In_ LPBYTE         lpFrame,
  _In_ LPBYTE         lpProtocol,
  _In_ DWORD          nPropertyInsts,
  _In_ LPPROPERTYINST lpPropInst
);
```



## <a name="parameters"></a><span data-ttu-id="e1fa7-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="e1fa7-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e1fa7-109">*хфраме* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="e1fa7-109">*hFrame* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e1fa7-110">Обработчик для анализируемого кадра.</span><span class="sxs-lookup"><span data-stu-id="e1fa7-110">Handle to the frame that is being parsed.</span></span>

</dd> <dt>

<span data-ttu-id="e1fa7-111">*лпфраме* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="e1fa7-111">*lpFrame* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e1fa7-112">Указатель на первый байт кадра.</span><span class="sxs-lookup"><span data-stu-id="e1fa7-112">Pointer to the first byte of a frame.</span></span>

</dd> <dt>

<span data-ttu-id="e1fa7-113">*лппротокол* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="e1fa7-113">*lpProtocol* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e1fa7-114">Указатель на начало данных протокола в кадре.</span><span class="sxs-lookup"><span data-stu-id="e1fa7-114">Pointer to the beginning of the protocol data in a frame.</span></span>

</dd> <dt>

<span data-ttu-id="e1fa7-115">*нпропертинстс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="e1fa7-115">*nPropertyInsts* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e1fa7-116">Число структур [пропертинст](propertyinst.md) , предоставляемых *лппропинст*.</span><span class="sxs-lookup"><span data-stu-id="e1fa7-116">Number of [PROPERTYINST](propertyinst.md) structures provided by *lpPropInst*.</span></span>

</dd> <dt>

<span data-ttu-id="e1fa7-117">*лппропинст* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="e1fa7-117">*lpPropInst* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e1fa7-118">Указатель на массив структур [пропертинст](propertyinst.md) .</span><span class="sxs-lookup"><span data-stu-id="e1fa7-118">Pointer to an array of [PROPERTYINST](propertyinst.md) structures.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e1fa7-119">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="e1fa7-119">Return value</span></span>

<span data-ttu-id="e1fa7-120">Если функция выполнена успешно, возвращается значение **true**.</span><span class="sxs-lookup"><span data-stu-id="e1fa7-120">If the function is successful, the return value is **TRUE**.</span></span>

<span data-ttu-id="e1fa7-121">Если функция завершается неудачно, возвращается значение **false**.</span><span class="sxs-lookup"><span data-stu-id="e1fa7-121">If the function is unsuccessful, the return value is **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="e1fa7-122">Комментарии</span><span class="sxs-lookup"><span data-stu-id="e1fa7-122">Remarks</span></span>

<span data-ttu-id="e1fa7-123">Сетевой монитор вызывает функцию **форматпропертиес** для вывода данных в области сведений пользовательского интерфейса сетевой монитор.</span><span class="sxs-lookup"><span data-stu-id="e1fa7-123">Network Monitor calls the **FormatProperties** function to display data in the details pane of the Network Monitor UI.</span></span> <span data-ttu-id="e1fa7-124">Как правило, **форматпропертиес** вызывается для форматирования строки сводки по протоколу, а затем для форматирования всех экземпляров свойств протокола внутри фрейма.</span><span class="sxs-lookup"><span data-stu-id="e1fa7-124">Typically, **FormatProperties** is called to format the summary line for a protocol, and then to format all the property instances of the protocol within a frame.</span></span> <span data-ttu-id="e1fa7-125">Однако сетевой монитор не гарантирует, сколько раз он вызывает **форматпропертиес** для конкретного средства синтаксического анализа.</span><span class="sxs-lookup"><span data-stu-id="e1fa7-125">However, Network Monitor does not guarantee the number of times it calls **FormatProperties** for a specific parser.</span></span>

<span data-ttu-id="e1fa7-126">Во время реализации функции **форматпропертиес** средство синтаксического анализа косвенно вызывает функцию [форматпропертинстанце](formatpropertyinstance.md) для использования универсального модуля форматирования, который сетевой монитор предоставляет, или может вызвать пользовательскую процедуру форматирования, определенную средством синтаксического анализа.</span><span class="sxs-lookup"><span data-stu-id="e1fa7-126">During the implementation of the **FormatProperties** function, the parser indirectly calls the [FormatPropertyInstance](formatpropertyinstance.md) function to use the generic formatter that Network Monitor provides, or it can call a custom formatter procedure that is defined by the parser.</span></span> <span data-ttu-id="e1fa7-127">Один из модулей форматирования должен вызываться для каждой структуры [пропертинст](propertyinst.md) , передаваемой в библиотеку DLL средства синтаксического анализа в параметре *лппропинст* .</span><span class="sxs-lookup"><span data-stu-id="e1fa7-127">One of the formatters must be called for each [PROPERTYINST](propertyinst.md) structure passed to the parser DLL in the *lpPropInst* parameter.</span></span>



| <span data-ttu-id="e1fa7-128">Дополнительные сведения о</span><span class="sxs-lookup"><span data-stu-id="e1fa7-128">For Information on</span></span>                                          | <span data-ttu-id="e1fa7-129">См.</span><span class="sxs-lookup"><span data-stu-id="e1fa7-129">See</span></span>                                                                |
|-------------------------------------------------------------|--------------------------------------------------------------------|
| <span data-ttu-id="e1fa7-130">Какие анализаторы и как они работают с сетевой монитор.</span><span class="sxs-lookup"><span data-stu-id="e1fa7-130">What parsers are, and how they work with Network Monitor.</span></span>   | [<span data-ttu-id="e1fa7-131">Анализаторы</span><span class="sxs-lookup"><span data-stu-id="e1fa7-131">Parsers</span></span>](parsers.md)                                             |
| <span data-ttu-id="e1fa7-132">Какие точки входа включены в библиотеку DLL средства синтаксического анализа.</span><span class="sxs-lookup"><span data-stu-id="e1fa7-132">Which entry points are included in the parser DLL.</span></span>          | [<span data-ttu-id="e1fa7-133">Архитектура библиотеки DLL средства синтаксического анализа</span><span class="sxs-lookup"><span data-stu-id="e1fa7-133">Parser DLL Architecture</span></span>](parser-dll-architecture.md)             |
| <span data-ttu-id="e1fa7-134">Реализация **форматпропертиес**  включает пример.</span><span class="sxs-lookup"><span data-stu-id="e1fa7-134">How to implement **FormatProperties**  includes an example.</span></span> | [<span data-ttu-id="e1fa7-135">Реализация Форматпропертиес</span><span class="sxs-lookup"><span data-stu-id="e1fa7-135">Implementing FormatProperties</span></span>](implementing-formatproperties.md) |
| <span data-ttu-id="e1fa7-136">Как универсальный модуль форматирования форматирует различные типы данных.</span><span class="sxs-lookup"><span data-stu-id="e1fa7-136">How the generic formatter formats different types of data.</span></span>  | [<span data-ttu-id="e1fa7-137">Выходные данные универсального модуля форматирования</span><span class="sxs-lookup"><span data-stu-id="e1fa7-137">Generic Formatter Output</span></span>](generic-formatter-output.md)           |



 

## <a name="requirements"></a><span data-ttu-id="e1fa7-138">Требования</span><span class="sxs-lookup"><span data-stu-id="e1fa7-138">Requirements</span></span>



| <span data-ttu-id="e1fa7-139">Требование</span><span class="sxs-lookup"><span data-stu-id="e1fa7-139">Requirement</span></span> | <span data-ttu-id="e1fa7-140">Значение</span><span class="sxs-lookup"><span data-stu-id="e1fa7-140">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="e1fa7-141">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="e1fa7-141">Minimum supported client</span></span><br/> | <span data-ttu-id="e1fa7-142">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="e1fa7-142">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="e1fa7-143">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="e1fa7-143">Minimum supported server</span></span><br/> | <span data-ttu-id="e1fa7-144">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="e1fa7-144">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="e1fa7-145">Заголовок</span><span class="sxs-lookup"><span data-stu-id="e1fa7-145">Header</span></span><br/>                   | <dl> <span data-ttu-id="e1fa7-146"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="e1fa7-146"><dt>Netmon.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e1fa7-147">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="e1fa7-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e1fa7-148">форматпропертинстанце</span><span class="sxs-lookup"><span data-stu-id="e1fa7-148">FormatPropertyInstance</span></span>](formatpropertyinstance.md)
</dt> <dt>

[<span data-ttu-id="e1fa7-149">PROPERTYINFO</span><span class="sxs-lookup"><span data-stu-id="e1fa7-149">PROPERTYINFO</span></span>](propertyinfo.md)
</dt> <dt>

[<span data-ttu-id="e1fa7-150">пропертинст</span><span class="sxs-lookup"><span data-stu-id="e1fa7-150">PROPERTYINST</span></span>](propertyinst.md)
</dt> </dl>

 

 




