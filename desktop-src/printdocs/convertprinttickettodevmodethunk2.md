---
description: Преобразует билет печати в структуру DEVMODE.
ms.assetid: 3b0a6afd-fa9d-434e-a95f-b051296d4567
title: Функция ConvertPrintTicketToDevModeThunk2
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ConvertPrintTicketToDevModeThunk2
api_type:
- DllExport
api_location:
- prntvpt.dll
ms.openlocfilehash: cf05ab6739dad09332ebc6746a05f3c40ef32de6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104081163"
---
# <a name="convertprinttickettodevmodethunk2-function"></a><span data-ttu-id="aa722-103">Функция ConvertPrintTicketToDevModeThunk2</span><span class="sxs-lookup"><span data-stu-id="aa722-103">ConvertPrintTicketToDevModeThunk2 function</span></span>

<span data-ttu-id="aa722-104">\[Эта функция не поддерживается и может быть отключена или удалена в будущих версиях Windows.</span><span class="sxs-lookup"><span data-stu-id="aa722-104">\[This function is not supported and might be disabled or deleted in future versions of Windows.</span></span> <span data-ttu-id="aa722-105">[**Птконвертпринттиккеттодевмоде**](/windows/desktop/api/prntvpt/nf-prntvpt-ptconvertprinttickettodevmode) предоставляет эквивалентную функциональность, и вместо нее следует использовать.\]</span><span class="sxs-lookup"><span data-stu-id="aa722-105">[**PTConvertPrintTicketToDevMode**](/windows/desktop/api/prntvpt/nf-prntvpt-ptconvertprinttickettodevmode) provides equivalent functionality and should be used instead.\]</span></span>

<span data-ttu-id="aa722-106">Преобразует билет печати в структуру [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) .</span><span class="sxs-lookup"><span data-stu-id="aa722-106">Converts a print ticket to a [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="aa722-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="aa722-107">Syntax</span></span>


```C++
HRESULT ConvertPrintTicketToDevModeThunk2(
  _In_      HPTPROVIDER hProvider,
  _In_      BYTE        *pPrintTicket,
  _In_      ULONG       cbSize,
  _In_      INT         baseType,
  _In_      DWORD       scope,
  _Out_     BYTE        **ppDevmode,
  _Out_     ULONG       *pcbDevModeLength,
  _Out_opt_ BSTR        *errMsg
);
```



## <a name="parameters"></a><span data-ttu-id="aa722-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="aa722-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="aa722-109">*хпровидер* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="aa722-109">*hProvider* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="aa722-110">Маркер открытого поставщика билетов на печать.</span><span class="sxs-lookup"><span data-stu-id="aa722-110">A handle to an open print ticket provider.</span></span> <span data-ttu-id="aa722-111">Этот маркер возвращается функцией [**биндптпровидерсунк**](bindptproviderthunk.md) .</span><span class="sxs-lookup"><span data-stu-id="aa722-111">This handle is returned by the [**BindPTProviderThunk**](bindptproviderthunk.md) function.</span></span>

</dd> <dt>

<span data-ttu-id="aa722-112">*ппринттиккет* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="aa722-112">*pPrintTicket* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="aa722-113">Буфер, содержащий билет на печать для преобразования.</span><span class="sxs-lookup"><span data-stu-id="aa722-113">The buffer that contains the print ticket to convert.</span></span>

</dd> <dt>

<span data-ttu-id="aa722-114">*кбсизе* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="aa722-114">*cbSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="aa722-115">Размер буфера (в байтах), переданного в *ппринттиккет*.</span><span class="sxs-lookup"><span data-stu-id="aa722-115">The size, in bytes, of the buffer passed in *pPrintTicket*.</span></span>

</dd> <dt>

<span data-ttu-id="aa722-116">*тип BaseType* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="aa722-116">*baseType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="aa722-117">Значение, указывающее, используется ли по умолчанию [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) пользователя или очередь печати по **умолчанию** для предоставления значений для выходного **DEVMODE** , когда *Ппринттиккет* не указывает все возможные параметры для **DEVMODE**.</span><span class="sxs-lookup"><span data-stu-id="aa722-117">A value indicating whether the user's default [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) or the print queue's default **DEVMODE** is used to provide values to the output **DEVMODE** when *pPrintTicket* does not specify every possible setting for a **DEVMODE**.</span></span> <span data-ttu-id="aa722-118">Значение этого параметра должно быть членом перечисления [**едефаултдевмодетипе**](/windows/win32/api/prntvpt/ne-prntvpt-edefaultdevmodetype) , приведенным как **int**.</span><span class="sxs-lookup"><span data-stu-id="aa722-118">The value of this parameter must be a member of the [**EDefaultDevmodeType**](/windows/win32/api/prntvpt/ne-prntvpt-edefaultdevmodetype) enumeration, cast as an **INT**.</span></span>

</dd> <dt>

<span data-ttu-id="aa722-119">*область действия* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="aa722-119">*scope* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="aa722-120">Значение типа, указывающее область действия *ппринттиккет*.</span><span class="sxs-lookup"><span data-stu-id="aa722-120">A value that specifies the scope of *pPrintTicket*.</span></span> <span data-ttu-id="aa722-121">Это значение может указывать одну страницу, весь документ или все документы в задании печати.</span><span class="sxs-lookup"><span data-stu-id="aa722-121">This value can specify a single page, an entire document, or all documents in the print job.</span></span> <span data-ttu-id="aa722-122">Значение этого параметра должно быть членом перечисления [**епринттиккетскопе**](/windows/desktop/api/prntvpt/ne-prntvpt-eprintticketscope) , приведенным как **DWORD**.</span><span class="sxs-lookup"><span data-stu-id="aa722-122">The value of this parameter must be a member of the [**EPrintTicketScope**](/windows/desktop/api/prntvpt/ne-prntvpt-eprintticketscope) enumeration, cast as a **DWORD**.</span></span>

</dd> <dt>

<span data-ttu-id="aa722-123">*ппдевмоде* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="aa722-123">*ppDevmode* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="aa722-124">Адрес созданного [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea).</span><span class="sxs-lookup"><span data-stu-id="aa722-124">The address of the newly created [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea).</span></span> <span data-ttu-id="aa722-125">Эта функция вызывает функцию [**CoTaskMemAlloc**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemalloc) для выделения буфера.</span><span class="sxs-lookup"><span data-stu-id="aa722-125">This function calls [**CoTaskMemAlloc**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemalloc) to allocate this buffer.</span></span> <span data-ttu-id="aa722-126">Если буфер больше не нужен, вызывающий объект должен освободить его, вызвав [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree).</span><span class="sxs-lookup"><span data-stu-id="aa722-126">When the buffer is no longer needed, the caller must free it by calling [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree).</span></span>

</dd> <dt>

<span data-ttu-id="aa722-127">*пкбдевмоделенгс* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="aa722-127">*pcbDevModeLength* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="aa722-128">Размер [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) в байтах, возвращенный в *ппдевмоде*.</span><span class="sxs-lookup"><span data-stu-id="aa722-128">The size, in bytes, of the [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) returned in *ppDevmode*.</span></span>

</dd> <dt>

<span data-ttu-id="aa722-129">*еррмсг* \[ out, необязательно\]</span><span class="sxs-lookup"><span data-stu-id="aa722-129">*errMsg* \[out, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="aa722-130">Указатель на строку, указывающую, что, если что-либо, является недопустимым для билета печати в *ппринттиккет*.</span><span class="sxs-lookup"><span data-stu-id="aa722-130">A pointer to a string that specifies what, if anything, is invalid about the print ticket in *pPrintTicket*.</span></span> <span data-ttu-id="aa722-131">Если он является допустимым, это **значение равно NULL**.</span><span class="sxs-lookup"><span data-stu-id="aa722-131">If it is valid, this is **NULL**.</span></span> <span data-ttu-id="aa722-132">Если *еррмсг* не **равно NULL** , то при возврате функции вызывающий объект должен освободить строку с помощью [**сисфристринг**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring).</span><span class="sxs-lookup"><span data-stu-id="aa722-132">If *errMsg* is not **NULL** when the function returns, the caller must free the string with [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="aa722-133">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="aa722-133">Return value</span></span>

<span data-ttu-id="aa722-134">Если метод завершается успешно, возвращается значение **\_ ОК**. в противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="aa722-134">If the method succeeds, it returns **S\_OK**; otherwise, it returns an **HRESULT** error code.</span></span> <span data-ttu-id="aa722-135">Дополнительные сведения о кодах ошибок COM см. в разделе [Обработка ошибок](../com/error-handling-in-com.md).</span><span class="sxs-lookup"><span data-stu-id="aa722-135">For more information about COM error codes, see [Error Handling](../com/error-handling-in-com.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="aa722-136">Требования</span><span class="sxs-lookup"><span data-stu-id="aa722-136">Requirements</span></span>



| <span data-ttu-id="aa722-137">Требование</span><span class="sxs-lookup"><span data-stu-id="aa722-137">Requirement</span></span> | <span data-ttu-id="aa722-138">Значение</span><span class="sxs-lookup"><span data-stu-id="aa722-138">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="aa722-139">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="aa722-139">Minimum supported client</span></span><br/> | <span data-ttu-id="aa722-140">Только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="aa722-140">Windows XP \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="aa722-141">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="aa722-141">Minimum supported server</span></span><br/> | <span data-ttu-id="aa722-142">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="aa722-142">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="aa722-143">DLL</span><span class="sxs-lookup"><span data-stu-id="aa722-143">DLL</span></span><br/>                      | <dl> <span data-ttu-id="aa722-144"><dt>Prntvpt.dll</dt></span><span class="sxs-lookup"><span data-stu-id="aa722-144"><dt>Prntvpt.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="aa722-145">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="aa722-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="aa722-146">Схема печати</span><span class="sxs-lookup"><span data-stu-id="aa722-146">Print Schema</span></span>](./printschema.md)
</dt> <dt>

[<span data-ttu-id="aa722-147">**птконвертпринттиккеттодевмоде**</span><span class="sxs-lookup"><span data-stu-id="aa722-147">**PTConvertPrintTicketToDevMode**</span></span>](/windows/desktop/api/prntvpt/nf-prntvpt-ptconvertprinttickettodevmode)
</dt> <dt>

[<span data-ttu-id="aa722-148">Вывод на печать</span><span class="sxs-lookup"><span data-stu-id="aa722-148">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="aa722-149">Функции API очереди печати принтера</span><span class="sxs-lookup"><span data-stu-id="aa722-149">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> </dl>

 

