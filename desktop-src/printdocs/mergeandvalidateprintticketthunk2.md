---
description: Выполняет слияние двух билетов на печать и возвращает допустимый, действующий билет печати.
ms.assetid: 4aa7b9de-abf2-4781-942e-0b992a6bffed
title: Функция MergeAndValidatePrintTicketThunk2
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MergeAndValidatePrintTicketThunk2
api_type:
- DllExport
api_location:
- prntvpt.dll
ms.openlocfilehash: 4a21b9e505e39d64e8e0c696a3b8a6432a012d76
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105684482"
---
# <a name="mergeandvalidateprintticketthunk2-function"></a><span data-ttu-id="eac75-103">Функция MergeAndValidatePrintTicketThunk2</span><span class="sxs-lookup"><span data-stu-id="eac75-103">MergeAndValidatePrintTicketThunk2 function</span></span>

<span data-ttu-id="eac75-104">\[Эта функция не поддерживается и может быть отключена или удалена в будущих версиях Windows.</span><span class="sxs-lookup"><span data-stu-id="eac75-104">\[This function is not supported and might be disabled or deleted in future versions of Windows.</span></span> <span data-ttu-id="eac75-105">[**Птмержеандвалидатепринттиккет**](/windows/desktop/api/prntvpt/nf-prntvpt-ptmergeandvalidateprintticket) предоставляет эквивалентную функциональность, и вместо нее следует использовать.\]</span><span class="sxs-lookup"><span data-stu-id="eac75-105">[**PTMergeAndValidatePrintTicket**](/windows/desktop/api/prntvpt/nf-prntvpt-ptmergeandvalidateprintticket) provides equivalent functionality and should be used instead.\]</span></span>

<span data-ttu-id="eac75-106">Выполняет слияние двух билетов на печать и возвращает допустимый, действующий билет печати.</span><span class="sxs-lookup"><span data-stu-id="eac75-106">Merges two print tickets and returns a valid, viable print ticket.</span></span>

## <a name="syntax"></a><span data-ttu-id="eac75-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="eac75-107">Syntax</span></span>


```C++
HRESULT MergeAndValidatePrintTicketThunk2(
  _In_      HPTPROVIDER hProvider,
  _In_      BYTE        *pBasePrintTicket,
  _In_      INT         basePrintTicketLength,
  _In_opt_  BYTE        *pDeltaPrintTicket,
  _In_      INT         deltaPrintTicketLength,
  _In_      DWORD       scope,
  _Out_     BYTE        **ppValidatedPrintTicket,
  _Out_     INT         *pValidatedPrintTicketLength,
  _Out_opt_ BSTR        *pbstrErrorMessage
);
```



## <a name="parameters"></a><span data-ttu-id="eac75-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="eac75-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="eac75-109">*хпровидер* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="eac75-109">*hProvider* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="eac75-110">Маркер открытого поставщика билетов на печать.</span><span class="sxs-lookup"><span data-stu-id="eac75-110">A handle to an open print ticket provider.</span></span> <span data-ttu-id="eac75-111">Этот маркер возвращается функцией [**биндптпровидерсунк**](bindptproviderthunk.md) .</span><span class="sxs-lookup"><span data-stu-id="eac75-111">This handle is returned by the [**BindPTProviderThunk**](bindptproviderthunk.md) function.</span></span>

</dd> <dt>

<span data-ttu-id="eac75-112">*пбасепринттиккет* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="eac75-112">*pBasePrintTicket* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="eac75-113">Буфер, содержащий базовые данные билета на печать, выраженные в формате XML, как описано в [схеме печати](./printschema.md).</span><span class="sxs-lookup"><span data-stu-id="eac75-113">The buffer that contains the base print ticket data, expressed in XML as described in the [Print Schema](./printschema.md).</span></span>

</dd> <dt>

<span data-ttu-id="eac75-114">*басепринттиккетленгс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="eac75-114">*basePrintTicketLength* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="eac75-115">Размер (в байтах) буфера, на который ссылается *пбасепринттиккет*.</span><span class="sxs-lookup"><span data-stu-id="eac75-115">The size, in bytes, of the buffer referenced by *pBasePrintTicket*.</span></span>

</dd> <dt>

<span data-ttu-id="eac75-116">*пделтапринттиккет* \[ в необязательное\]</span><span class="sxs-lookup"><span data-stu-id="eac75-116">*pDeltaPrintTicket* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="eac75-117">Буфер, содержащий билет на печать для слияния.</span><span class="sxs-lookup"><span data-stu-id="eac75-117">The buffer that contains the print ticket to merge.</span></span> <span data-ttu-id="eac75-118">Данные билета печати выражаются в формате XML, как описано в [схеме печати](./printschema.md).</span><span class="sxs-lookup"><span data-stu-id="eac75-118">The print ticket data is expressed in XML as described in the [Print Schema](./printschema.md).</span></span> <span data-ttu-id="eac75-119">Значение этого параметра может быть **равно NULL**.</span><span class="sxs-lookup"><span data-stu-id="eac75-119">The value of this parameter can be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="eac75-120">*делтапринттиккетленгс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="eac75-120">*deltaPrintTicketLength* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="eac75-121">Размер (в байтах) буфера, на который ссылается *пделтапринттиккет*.</span><span class="sxs-lookup"><span data-stu-id="eac75-121">The size, in bytes, of the buffer referenced by *pDeltaPrintTicket*.</span></span>

</dd> <dt>

<span data-ttu-id="eac75-122">*область действия* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="eac75-122">*scope* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="eac75-123">Значение типа, указывающее, является ли область *пделтапринттиккет* и *ппвалидатедпринттиккет* одной страницей, целым документом или всеми документами в задании печати.</span><span class="sxs-lookup"><span data-stu-id="eac75-123">The value that specifies whether the scope of *pDeltaPrintTicket* and *ppValidatedPrintTicket* is a single page, an entire document, or all documents in the print job.</span></span> <span data-ttu-id="eac75-124">Значение этого параметра должно быть членом перечисления [**епринттиккетскопе**](/windows/desktop/api/prntvpt/ne-prntvpt-eprintticketscope) , приведенным как **DWORD**.</span><span class="sxs-lookup"><span data-stu-id="eac75-124">The value of this parameter must be a member of the [**EPrintTicketScope**](/windows/desktop/api/prntvpt/ne-prntvpt-eprintticketscope) enumeration, cast as a **DWORD**.</span></span>

</dd> <dt>

<span data-ttu-id="eac75-125">*ппвалидатедпринттиккет* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="eac75-125">*ppValidatedPrintTicket* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="eac75-126">Адрес буфера, содержащего Объединенный и проверенный билет печати.</span><span class="sxs-lookup"><span data-stu-id="eac75-126">The address of the buffer that contains the merged and validated print ticket.</span></span> <span data-ttu-id="eac75-127">Эта функция вызывает функцию [**CoTaskMemAlloc**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemalloc) для выделения буфера.</span><span class="sxs-lookup"><span data-stu-id="eac75-127">This function calls [**CoTaskMemAlloc**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemalloc) to allocate this buffer.</span></span> <span data-ttu-id="eac75-128">Если буфер больше не нужен, вызывающий объект должен освободить его, вызвав [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree).</span><span class="sxs-lookup"><span data-stu-id="eac75-128">When the buffer is no longer needed, the caller must free it by calling [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree).</span></span>

</dd> <dt>

<span data-ttu-id="eac75-129">*пвалидатедпринттиккетленгс* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="eac75-129">*pValidatedPrintTicketLength* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="eac75-130">Размер (в байтах) буфера, на который ссылается *ппвалидатедпринттиккет*.</span><span class="sxs-lookup"><span data-stu-id="eac75-130">The size, in bytes, of the buffer referenced by *ppValidatedPrintTicket*.</span></span>

</dd> <dt>

<span data-ttu-id="eac75-131">*пбстреррормессаже* \[ out, необязательно\]</span><span class="sxs-lookup"><span data-stu-id="eac75-131">*pbstrErrorMessage* \[out, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="eac75-132">Указатель на строку, указывающую, что, если что-либо, является недопустимым для билета печати в *пбасепринттиккет* или *пделтапринттиккет*.</span><span class="sxs-lookup"><span data-stu-id="eac75-132">A pointer to a string that specifies what, if anything, is invalid about the print ticket in *pBasePrintTicket* or *pDeltaPrintTicket*.</span></span> <span data-ttu-id="eac75-133">Если они оба допустимы, это значение равно **null**.</span><span class="sxs-lookup"><span data-stu-id="eac75-133">If they are both valid, this value is **NULL**.</span></span> <span data-ttu-id="eac75-134">Если *пбстреррормессаже* не **равно NULL** , то при возврате функции вызывающий объект должен освободить строку с помощью [**сисфристринг**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring).</span><span class="sxs-lookup"><span data-stu-id="eac75-134">If *pbstrErrorMessage* is not **NULL** when the function returns, the caller must free the string with [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="eac75-135">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="eac75-135">Return value</span></span>

<span data-ttu-id="eac75-136">Если метод завершается успешно, возвращается значение **\_ ОК**. в противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="eac75-136">If the method succeeds, it returns **S\_OK**; otherwise, it returns an **HRESULT** error code.</span></span> <span data-ttu-id="eac75-137">Дополнительные сведения о кодах ошибок COM см. в разделе [Обработка ошибок](../com/error-handling-in-com.md).</span><span class="sxs-lookup"><span data-stu-id="eac75-137">For more information about COM error codes, see [Error Handling](../com/error-handling-in-com.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="eac75-138">Требования</span><span class="sxs-lookup"><span data-stu-id="eac75-138">Requirements</span></span>



| <span data-ttu-id="eac75-139">Требование</span><span class="sxs-lookup"><span data-stu-id="eac75-139">Requirement</span></span> | <span data-ttu-id="eac75-140">Значение</span><span class="sxs-lookup"><span data-stu-id="eac75-140">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="eac75-141">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="eac75-141">Minimum supported client</span></span><br/> | <span data-ttu-id="eac75-142">Только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="eac75-142">Windows XP \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="eac75-143">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="eac75-143">Minimum supported server</span></span><br/> | <span data-ttu-id="eac75-144">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="eac75-144">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="eac75-145">DLL</span><span class="sxs-lookup"><span data-stu-id="eac75-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="eac75-146"><dt>Prntvpt.dll</dt></span><span class="sxs-lookup"><span data-stu-id="eac75-146"><dt>Prntvpt.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="eac75-147">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="eac75-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="eac75-148">Схема печати</span><span class="sxs-lookup"><span data-stu-id="eac75-148">Print Schema</span></span>](./printschema.md)
</dt> <dt>

[<span data-ttu-id="eac75-149">**птмержеандвалидатепринттиккет**</span><span class="sxs-lookup"><span data-stu-id="eac75-149">**PTMergeAndValidatePrintTicket**</span></span>](/windows/desktop/api/prntvpt/nf-prntvpt-ptmergeandvalidateprintticket)
</dt> <dt>

[<span data-ttu-id="eac75-150">Вывод на печать</span><span class="sxs-lookup"><span data-stu-id="eac75-150">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="eac75-151">Функции API очереди печати принтера</span><span class="sxs-lookup"><span data-stu-id="eac75-151">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> </dl>

 

